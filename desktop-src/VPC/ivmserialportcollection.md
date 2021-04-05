---
title: Interfaccia IVMSerialPortCollection (VPCCOMInterfaces. h)
description: Definisce la raccolta di porte seriali all'interno della macchina virtuale. Per ottenere un oggetto IVMSerialPortCollection, usare la proprietà IVMVirtualMachine SerialPorts.
ms.assetid: c0ee9799-f3f7-477e-b33b-52f424752aad
keywords:
- Interfaccia IVMSerialPortCollection Virtual PC
- Interfaccia IVMSerialPortCollection Virtual PC, descritta
topic_type:
- apiref
api_name:
- IVMSerialPortCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1d2ec37789423b5f9446d667da69eca346a2286
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741738"
---
# <a name="ivmserialportcollection-interface"></a>Interfaccia IVMSerialPortCollection

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Definisce la raccolta di porte seriali all'interno della macchina virtuale. Per ottenere un oggetto **IVMSerialPortCollection** , usare la proprietà [**IVMVirtualMachine:: Serialports**](ivmvirtualmachine-serialports.md) .

## <a name="members"></a>Membri

L'interfaccia **IVMSerialPortCollection** eredita dall'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVMSerialPortCollection** dispone anche di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

L'interfaccia **IVMSerialPortCollection** ha queste proprietà.



| Proprietà                                                         | Tipo di accesso          | Descrizione                                                                |
|:-----------------------------------------------------------------|:---------------------|:---------------------------------------------------------------------------|
| [**\_NewEnum**](ivmserialportcollection--newenum.md)<br/> | Sola lettura<br/> | Enumeratore per la raccolta.<br/>                               |
| [**Conteggio**](ivmserialportcollection-count.md)<br/>        | Sola lettura<br/> | Numero di porte seriali in questa raccolta.<br/>                  |
| [**Elemento**](ivmserialportcollection-item.md)<br/>          | Sola lettura<br/> | Oggetto porta seriale che corrisponde all'indice specificato.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMSerialPortCollection è definito come dd3c6175-1F04-4341-9f85-104074880289<br/>    |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMSerialPort**](ivmserialport.md)
</dt> <dt>

[**IVMVirtualMachine:: SerialPorts**](ivmvirtualmachine-serialports.md)
</dt> </dl>

 

