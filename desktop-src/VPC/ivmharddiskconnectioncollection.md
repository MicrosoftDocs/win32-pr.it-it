---
title: Interfaccia IVMHardDiskConnectionCollection (VPCCOMInterfaces.h)
description: Definisce la raccolta di connessioni al disco rigido all'interno della macchina virtuale. Per ottenere un oggetto IVMHardDiskConnectionCollection, usare la proprietà IVMVirtualMachine HardDiskConnections.
ms.assetid: 3440318c-45f4-4d24-9609-dbe5ca59b005
keywords:
- Interfaccia IVMHardDiskConnectionCollection Virtual PC
- Interfaccia IVMHardDiskConnectionCollection Virtual PC , descritto
topic_type:
- apiref
api_name:
- IVMHardDiskConnectionCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 997cbe915e7e4addac60c639a7ee6c260f07271ff5981939b25dbefd49fcba1b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118345705"
---
# <a name="ivmharddiskconnectioncollection-interface"></a>Interfaccia IVMHardDiskConnectionCollection

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Definisce la raccolta di connessioni al disco rigido all'interno della macchina virtuale. Per ottenere un **oggetto IVMHardDiskConnectionCollection,** usare la [**proprietà IVMVirtualMachine::HardDiskConnections.**](ivmvirtualmachine-harddiskconnections.md)

## <a name="members"></a>Membri

**L'interfaccia IVMHardDiskConnectionCollection** eredita dall'interfaccia [**IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **IVMHardDiskConnectionCollection** include anche questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

Queste proprietà sono disponibili nell'interfaccia **IVMHardDiskConnectionCollection.**



| Proprietà                                                                 | Tipo di accesso          | Descrizione                                                                         |
|:-------------------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------|
| [**\_NewEnum**](ivmharddiskconnectioncollection--newenum.md)<br/> | Sola lettura<br/> | Enumeratore per la raccolta.<br/>                                        |
| [**Conteggio**](ivmharddiskconnectioncollection-count.md)<br/>        | Sola lettura<br/> | Numero di connessioni al disco rigido in questa raccolta.<br/>                  |
| [**Elemento**](ivmharddiskconnectioncollection-item.md)<br/>          | Sola lettura<br/> | Oggetto di connessione del disco rigido che corrisponde all'indice specificato.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                         |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                          |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                               |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                      |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl>      |
| IID<br/>                      | IID \_ IVMHardDiskconnectionCollection è definito come b9f2caf4-0aeb-4085-b105-ceddb90dbf62<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMHardDiskConnection**](ivmharddiskconnection.md)
</dt> <dt>

[**IVMVirtualMachine::HardDiskConnections**](ivmvirtualmachine-harddiskconnections.md)
</dt> </dl>

 

