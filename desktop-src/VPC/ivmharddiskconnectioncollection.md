---
title: Interfaccia IVMHardDiskConnectionCollection (VPCCOMInterfaces. h)
description: Definisce la raccolta di connessioni del disco rigido all'interno della macchina virtuale. Per ottenere un oggetto IVMHardDiskConnectionCollection, usare la proprietà IVMVirtualMachine HardDiskConnections.
ms.assetid: 3440318c-45f4-4d24-9609-dbe5ca59b005
keywords:
- Interfaccia IVMHardDiskConnectionCollection Virtual PC
- Interfaccia IVMHardDiskConnectionCollection Virtual PC, descritta
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
ms.openlocfilehash: dbde67f226c5b2d8cb86a8764c6dd61c24c2a468
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475034"
---
# <a name="ivmharddiskconnectioncollection-interface"></a>Interfaccia IVMHardDiskConnectionCollection

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Definisce la raccolta di connessioni del disco rigido all'interno della macchina virtuale. Per ottenere un oggetto **IVMHardDiskConnectionCollection** , usare la proprietà [**IVMVirtualMachine:: HardDiskConnections**](ivmvirtualmachine-harddiskconnections.md) .

## <a name="members"></a>Membri

L'interfaccia **IVMHardDiskConnectionCollection** eredita dall'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVMHardDiskConnectionCollection** dispone anche di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

L'interfaccia **IVMHardDiskConnectionCollection** ha queste proprietà.



| Proprietà                                                                 | Tipo di accesso          | Descrizione                                                                         |
|:-------------------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------|
| [**\_NewEnum**](ivmharddiskconnectioncollection--newenum.md)<br/> | Sola lettura<br/> | Enumeratore per la raccolta.<br/>                                        |
| [**Conteggio**](ivmharddiskconnectioncollection-count.md)<br/>        | Sola lettura<br/> | Numero di connessioni del disco rigido in questa raccolta.<br/>                  |
| [**Elemento**](ivmharddiskconnectioncollection-item.md)<br/>          | Sola lettura<br/> | Oggetto connessione al disco rigido che corrisponde all'indice specificato.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                         |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                          |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                               |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                      |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl>      |
| IID<br/>                      | IID \_ IVMHardDiskconnectionCollection è definito come b9f2caf4-0aeb-4085-B105-ceddb90dbf62<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMHardDiskConnection**](ivmharddiskconnection.md)
</dt> <dt>

[**IVMVirtualMachine::HardDiskConnections**](ivmvirtualmachine-harddiskconnections.md)
</dt> </dl>

 

