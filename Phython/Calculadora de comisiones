# Declaración de variables (costos)

cft3cs = 5.32 # CFT Cuota Simple 3
cft6cs = 10.14 # CFT Cuota Simple 6
cft3 = 12 # CFT Cuota convencional absorción 3
cft6 = 20 # CFT Cuota convencional absorción 6
comlinkposctv = 4.9 # Comisión venta link de pago, POS con tarjeta de credito y tiendas virtuales
comet = 4.4 # Comisión venta Empretienda
composdeb = 2.9 # Comisión venta POS debito
comqr = 0.8 # Comisión venta QR
comisionsumada = 0
comisiontotal = 0
monto = 0
comisioniva = 0
comisionsiniva = 0
comisionporcentaje = 0
comisioncft = 0
conPOS = "m"


# Solicitud de información

print("• Calculadora comisiones ventas con Ualá Bis •")
print("")
print("")

print("Medio de la venta. ")
print("a) Empretienda")
print("b) POS")
print("c) Link de pago")
print("d) QR")
print("e) Tiendas virtuales / API")
print("")

medio = input("Seleccionar opcion (a, b, c, d, e): ")

while medio.lower() != "a" and medio.lower() != "b" and medio.lower() != "c" and medio.lower() != "d" and medio.lower() != "e":
    print("Error. Por favor ingresar letra.")
    medio = input("Vuelva a seleccionar opción (a, b, c, d, e): ")

if medio.lower() == "a":
    comision = comet
else:
    if medio.lower() == "b":
        print("")
        print("▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬")
        print("")
        print("Tipo de tarjeta. ")
        print("a) Débito")
        print("b) Crédito")
        print("")

        conPOS = input("Seleccionar opción (a, b): ")
        while conPOS.lower() != "a" and conPOS.lower() != "b":
            print("Error. Por favor ingresar letra.")
            conPOS = input("Vuelva a seleccionar opción (a, b): ")

        if conPOS.lower() == "a":
            comision = composdeb
        else:
            comision = comlinkposctv
    else:
        if medio.lower() == "d":
            comision = comqr
        else:
            comision = comlinkposctv

if conPOS.lower() == "a" or medio.lower() == "d":
    comisioncft = 0
else:
    print("")
    print("▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬")
    print("")
    print("¿La venta se hizo en cuotas sin interés?")
    print("a) Si")
    print("b) No")
    print("")

    csi = input("Seleccionar opción (a, b): ")
    while csi.lower() != "a" and csi.lower() != "b":
            print("Error. Por favor ingresar letra.")
            csi = input("Vuelva a seleccionar opción (a, b): ")

    if csi.lower() == "a":
        print("")
        print("▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬")
        print("")
        print("¿Cuántas cuotas?")
        print("a) 3")
        print("b) 6")
        print("")

        cantcuo = input("Seleccionar opción (a, b): ")

        while cantcuo.lower() != "a" and cantcuo.lower() != "b":
            print("Error. Por favor ingresar letra.")
            cantcuo = input("Vuelva a seleccionar opción (a, b): ")

        print("")
        print("▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬")
        print("")
        print("¿Cuota Simple?")
        print("a) Si")
        print("b) No")
        print("")

        cs = input("Seleccionar opción (a, b): ")

        while cs.lower() != "a" and cs.lower() != "b":
            print("Error. Por favor ingresar letra.")
            cs = input("Vuelva a seleccionar opción (a, b): ")

        if cs.lower() == "a" and cantcuo == "a":
            comisioncft = cft3cs
        elif cs.lower() == "a" and cantcuo == "b":
            comisioncft = cft6cs
        elif cs.lower() == "b" and cantcuo == "a":
            comisioncft = cft3
        elif cs.lower() == "b" and cantcuo == "b":
            comisioncft = cft6

print("")
print("▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬")
print("")
monto = float(input("¿Monto bruto de la venta? $"))


# Cálculos

comisionsumada = comision + comisioncft

comisiontotal = ((comisionsumada * 1.21) * monto) / 100

comisioniva = (((comisionsumada * 0.21) * monto) / 100)

comisionsiniva = (comisionsumada * monto) / 100

comisionporcentaje = comisionsumada * 1.21


# Muestra de resultados

print("")
print("")
print("")
print("")
print("")
print("")
print("▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬▬")
print("")
print("El porcentaje de la comision cobrada es de → ", comisionsumada,"% + IVA")
print("")
print("El porcentaje de la comision cobrada es de → ", comisionporcentaje,"% ya teniendo en cuenta el IVA")
print("")

print("------------------")

print("")
print("Arancel → ", comisionsiniva)
print("IVA Arancel →", comisioniva)
print("")

print("------------------")

print("")
print("La comisión total cobrada es de → $", comisiontotal)
print("")
