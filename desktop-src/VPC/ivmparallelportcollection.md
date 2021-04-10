---
title: Interfaccia IVMParallelPortCollection (VPCCOMInterfaces. h)
description: Definisce la raccolta di porte parallele all'interno della macchina virtuale. Per ottenere un oggetto IVMParallelPortCollection, usare la proprietà IVMVirtualMachine ParallelPorts.
ms.assetid: 038a5c08-cd92-426f-a059-9a4c2110548d
keywords:
- Interfaccia IVMParallelPortCollection Virtual PC
- Interfaccia IVMParallelPortCollection Virtual PC, descritta
topic_type:
- apiref
api_name:
- IVMParallelPortCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8284b3720e0272147c932cfbfd70448babf5606f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121351"
---
# <a name="ivmparallelportcollection-interface"></a>Interfaccia IVMParallelPortCollection

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Definisce la raccolta di porte parallele all'interno della macchina virtuale. Per ottenere un oggetto **IVMParallelPortCollection** , usare la proprietà [**IVMVirtualMachine::P arallelports**](ivmvirtualmachine-parallelports.md) .

## <a name="members"></a>Membri

L'interfaccia **IVMParallelPortCollection** eredita dall'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVMParallelPortCollection** dispone anche di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

L'interfaccia **IVMParallelPortCollection** ha queste proprietà.



| Proprietà                                                           | Tipo di accesso          | Descrizione                                                                  |
|:-------------------------------------------------------------------|:---------------------|:-----------------------------------------------------------------------------|
| [**\_NewEnum**](ivmparallelportcollection--newenum.md)<br/> | Sola lettura<br/> | Enumeratore per la raccolta.<br/>                                 |
| [**Conteggio**](ivmparallelportcollection-count.md)<br/>        | Sola lettura<br/> | Numero di porte parallele in questa raccolta.<br/>                  |
| [**Elemento**](ivmparallelportcollection-item.md)<br/>          | Sola lettura<br/> | Oggetto porta parallela che corrisponde all'indice specificato.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMParallelPortCollection è definito come 27c3e036-198f-430C-8735-6e652f7203fd<br/>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMParallelPort**](ivmparallelport.md)
</dt> <dt>

[**IVMVirtualMachine::P arallelPorts**](ivmvirtualmachine-parallelports.md)
</dt> </dl>

 

