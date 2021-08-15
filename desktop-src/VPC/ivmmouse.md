---
title: Interfaccia IVMMouse (VPCCOMInterfaces.h)
description: Controlla il dispositivo mouse all'interno di una macchina virtuale.
ms.assetid: 13bbf980-aafd-4c63-b1cb-60f00b738d1f
keywords:
- Interfaccia IVMMouse Virtual PC
- Interfaccia IVMMouse Virtual PC, descritto
topic_type:
- apiref
api_name:
- IVMMouse
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 912365065b639f3c970390746c8e23ae1fc33648ecdf14278365290c503da26d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998851"
---
# <a name="ivmmouse-interface"></a>Interfaccia IVMMouse

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Controlla il dispositivo mouse all'interno di una macchina virtuale. **L'oggetto IVMMouse** per una macchina virtuale può essere recuperato usando la [**proprietà IVMVirtualMachine::Mouse.**](ivmvirtualmachine-mouse.md) Le coordinate per il dispositivo mouse possono essere rappresentate in coordinate assolute o in coordinate delta. Usare la [**proprietà UsingAbsoluteCoordinates**](ivmmouse-usingabsolutecoordinates.md) per distinguere tra i due metodi di rappresentazione delle coordinate. Si noti che il recupero della posizione corrente del cursore e l'uso di coordinate assolute sono supportati solo se nel sistema operativo guest sono installati i componenti di integrazione.

## <a name="members"></a>Membri

**L'interfaccia IVMMouse** eredita dall'interfaccia [**IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **IVMMouse** include anche questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

**L'interfaccia IVMMouse** include questi metodi.



| Metodo                                  | Descrizione                                                                        |
|:----------------------------------------|:-----------------------------------------------------------------------------------|
| [**Clic**](ivmmouse-click.md)         | Simula il clic di un pulsante del mouse.<br/>                                         |
| [**GetButton**](ivmmouse-getbutton.md) | Recupera lo stato corrente (verso l'alto o verso il basso) del pulsante del mouse specificato.<br/> |
| [**SetButton**](ivmmouse-setbutton.md) | Imposta lo stato corrente (su o giù) del pulsante del mouse specificato.<br/>      |



 

### <a name="properties"></a>Proprietà

**L'interfaccia IVMMouse** ha queste proprietà.



| Proprietà                                                                         | Tipo di accesso           | Descrizione                                                                                |
|:---------------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------|
| [**HorizontalPosition**](ivmmouse-horizontalposition.md)<br/>             | Lettura/Scrittura<br/> | Coordinata x assoluta del mouse.<br/>                                         |
| [**ScrollWheelPosition**](ivmmouse-scrollwheelposition.md)<br/>           | Sola scrittura<br/> | Coordinata z del mouse (solo relativa).<br/>                                  |
| [**Uso diAbsoluteCoordinates**](ivmmouse-usingabsolutecoordinates.md)<br/> | Lettura/Scrittura<br/> | Indica se le coordinate del mouse rappresentano coordinate assolute o relative.<br/> |
| [**VerticalPosition**](ivmmouse-verticalposition.md)<br/>                 | Lettura/Scrittura<br/> | Coordinata y assoluta del mouse.<br/>                                         |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMmouse è definito come ac903f6d-6346-4f29-8875-5d511a13895e<br/>                   |



 

