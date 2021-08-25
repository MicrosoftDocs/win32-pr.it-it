---
title: Interfaccia IVMTaskCollection (VPCCOMInterfaces.h)
description: Definisce la raccolta di oggetti attività. Per ottenere un oggetto IVMTaskCollection, usare la proprietà IVMVirtualPC Tasks.
ms.assetid: 5cfc543c-81a1-49d2-93a9-9b1db1cb5070
keywords:
- Interfaccia IVMTaskCollection Virtual PC
- Interfaccia IVMTaskCollection Virtual PC , descritta
topic_type:
- apiref
api_name:
- IVMTaskCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 150f5079258e551360f574cfd9fa0a8895d3673f5d6b38ea6a5e1c866cfbf1ba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119958801"
---
# <a name="ivmtaskcollection-interface"></a>Interfaccia IVMTaskCollection

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Definisce la raccolta di oggetti attività. Per ottenere un **oggetto IVMTaskCollection,** usare la [**proprietà IVMVirtualPC::Tasks.**](ivmvirtualpc-tasks.md)

## <a name="members"></a>Membri

**L'interfaccia IVMTaskCollection** eredita dall'interfaccia [**IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **IVMTaskCollection** include anche questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

Queste proprietà sono disponibili nell'interfaccia **IVMTaskCollection.**



| Proprietà                                                   | Tipo di accesso          | Descrizione                                                         |
|:-----------------------------------------------------------|:---------------------|:--------------------------------------------------------------------|
| [**\_NewEnum**](ivmtaskcollection--newenum.md)<br/> | Sola lettura<br/> | Enumeratore per la raccolta.<br/>                        |
| [**Conteggio**](ivmtaskcollection-count.md)<br/>        | Sola lettura<br/> | Numero di attività in questa raccolta.<br/>                  |
| [**Elemento**](ivmtaskcollection-item.md)<br/>          | Sola lettura<br/> | Oggetto attività che corrisponde all'indice specificato.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMTaskCollection è definito come 5c4387c8-0e8b-4b97-8058-84679adf4c40<br/>          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Attività IVM**](ivmtask.md)
</dt> <dt>

[**IVMVirtualPC::Tasks**](ivmvirtualpc-tasks.md)
</dt> </dl>

 

