---
title: Interfaccia IVMParallelPort (VPCCOMInterfaces. h)
description: Definisce una porta parallela all'interno di una macchina virtuale.
ms.assetid: da8daf16-5d22-49be-8fe9-72d5018c0622
keywords:
- Interfaccia IVMParallelPort Virtual PC
- Interfaccia IVMParallelPort Virtual PC, descritta
topic_type:
- apiref
api_name:
- IVMParallelPort
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71b76b23f48e728104a3826afa80a8f272cd7e66
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302557"
---
# <a name="ivmparallelport-interface"></a>Interfaccia IVMParallelPort

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Definisce una porta parallela all'interno di una macchina virtuale. Questa interfaccia consente di configurare le porte parallele all'interno di una macchina virtuale. È possibile recuperare un oggetto **IVMParallelPort** dall'oggetto [**IVMParallelPortCollection**](ivmparallelportcollection.md) restituito dalla proprietà [**IVMVirtualMachine::P arallelports**](ivmvirtualmachine-parallelports.md) .

## <a name="members"></a>Membri

L'interfaccia **IVMParallelPort** eredita dall'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVMParallelPort** dispone anche di questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

L'interfaccia **IVMParallelPort** dispone di questi metodi.



| Metodo                              | Descrizione                                                        |
|:------------------------------------|:-------------------------------------------------------------------|
| [**\_ID**](ivmparallelport--id.md) | Recupera l'identificatore interno della porta parallela.<br/> |



 

### <a name="properties"></a>Proprietà

L'interfaccia **IVMParallelPort** ha queste proprietà.



| Proprietà                                        | Tipo di accesso           | Descrizione                               |
|:------------------------------------------------|:----------------------|:------------------------------------------|
| [**Nome**](ivmparallelport-name.md)<br/> | Lettura/Scrittura<br/> | Nome della porta parallela.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMParallelPort è definito come 097beecb-0A02-474F-abd6-298b22293fc6<br/>            |



 

