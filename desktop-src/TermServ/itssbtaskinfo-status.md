---
title: Proprietà Status di ITsSbTaskInfo
description: Recupera un valore di enumerazione \_ RDV TASK \_ STATUS che rappresenta lo stato dell'attività.
ms.assetid: 779af127-133c-47ff-8fca-bfd2c96c9768
ms.tgt_platform: multiple
keywords:
- Proprietà status Servizi Desktop remoto
- Proprietà status Servizi Desktop remoto, interfaccia ITsSbTaskInfo
- Interfaccia ITsSbTaskInfo Servizi Desktop remoto proprietà , Status
topic_type:
- apiref
api_name:
- ITsSbTaskInfo.Status
- ITsSbTaskInfo.get_Status
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d497bd46d1adfca88cce3a4b5c58cf72619ef1c38a03823ff26a14f2e6dfebd0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120009241"
---
# <a name="itssbtaskinfostatus-property"></a>Proprietà ITsSbTaskInfo::Status

Recupera un valore [**di enumerazione \_ RDV TASK \_ STATUS**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status) che rappresenta lo stato dell'attività.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_Status(
  [out, retval] RDV_TASK_STATUS *pStatus
);
```



## <a name="property-value"></a>Valore proprietà

Valore [**di enumerazione \_ RDV TASK \_ STATUS**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status) che rappresenta lo stato dell'attività.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                            |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                       |
| Idl<br/>                      | <dl> <dt>Sbtsv.idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ITsSbTaskInfo**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtaskinfo)
</dt> </dl>

 

 





