---
title: Interfaccia IVMVirtualMachineCollection (VPCCOMInterfaces. h)
description: Definisce la raccolta di macchine virtuali all'interno di Windows Virtual PC. Per ottenere un oggetto IVMVirtualMachineCollection, usare la proprietà IVMVirtualPC VirtualMachines.
ms.assetid: 3d34e791-2dba-4529-b489-96a0c6227294
keywords:
- Interfaccia IVMVirtualMachineCollection Virtual PC
- Interfaccia IVMVirtualMachineCollection Virtual PC, descritta
topic_type:
- apiref
api_name:
- IVMVirtualMachineCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e27426f96e409a1e67eb519e7a864ee7461879a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121082"
---
# <a name="ivmvirtualmachinecollection-interface"></a>Interfaccia IVMVirtualMachineCollection

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Definisce la raccolta di macchine virtuali all'interno di Windows Virtual PC. Per ottenere un oggetto **IVMVirtualMachineCollection** , usare la proprietà [**IVMVirtualPC:: VirtualMachines**](ivmvirtualpc-virtualmachines.md) .

## <a name="members"></a>Membri

L'interfaccia **IVMVirtualMachineCollection** eredita dall'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVMVirtualMachineCollection** dispone anche di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

L'interfaccia **IVMVirtualMachineCollection** ha queste proprietà.



| Proprietà                                                             | Tipo di accesso          | Descrizione                                                                    |
|:---------------------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------------|
| [**\_NewEnum**](ivmvirtualmachinecollection--newenum.md)<br/> | Sola lettura<br/> | Enumeratore per la raccolta.<br/>                                   |
| [**Conteggio**](ivmvirtualmachinecollection-count.md)<br/>        | Sola lettura<br/> | Numero di macchine virtuali in questa raccolta.<br/>                  |
| [**Elemento**](ivmvirtualmachinecollection-item.md)<br/>          | Sola lettura<br/> | Oggetto macchina virtuale che corrisponde all'indice specificato.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                     |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                      |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                           |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                  |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl>  |
| IID<br/>                      | IID \_ IVMVirtualMachineCollection è definito come 59f31786-2a3d-4FBF-9896-d85338ca0da1<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMVirtualMachine**](ivmvirtualmachine.md)
</dt> <dt>

[**IVMVirtualPC:: VirtualMachines**](ivmvirtualpc-virtualmachines.md)
</dt> </dl>

 

