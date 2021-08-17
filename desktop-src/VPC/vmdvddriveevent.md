---
title: Enumerazione VMDVDDriveEvent (VPCCOMInterfaces.h)
description: Specifica gli eventi dell'unità DVD.
ms.assetid: 17126138-614f-42d9-937e-1aca9393557c
keywords:
- Enumerazione VMDVDDriveEvent Virtual PC
topic_type:
- apiref
api_name:
- VMDVDDriveEvent
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 125e2f8f9d126e582d47376f5c23b56051d3f75d9af6493a1f273cc5be93195c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117751983"
---
# <a name="vmdvddriveevent-enumeration"></a>Enumerazione VMDVDDriveEvent

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Specifica gli eventi dell'unità DVD.

## <a name="syntax"></a>Sintassi


```C++
typedef enum  { 
  vmDVDDriveEvent_OnInsert  = 1,
  vmDVDDriveEvent_OnEject   = 2
} VMDVDDriveEvent;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="vmDVDDriveEvent_OnInsert"></span><span id="vmdvddriveevent_oninsert"></span><span id="VMDVDDRIVEEVENT_ONINSERT"></span>**vmDVDDriveEvent \_ OnInsert**
</dt> <dd>

Un'immagine ISO è collegata o viene inserito un supporto reale in un'unità host.

</dd> <dt>

<span id="vmDVDDriveEvent_OnEject"></span><span id="vmdvddriveevent_oneject"></span><span id="VMDVDDRIVEEVENT_ONEJECT"></span>**vmDVDDriveEvent \_ OnEject**
</dt> <dd>

Il supporto è stato espulso.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMDVDDriveEvents**](ivmdvddriveevents.md)
</dt> </dl>

 

