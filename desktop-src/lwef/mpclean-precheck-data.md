---
title: MPCLEAN_PRECHECK_DATA (MpClient.h)
description: Dati di notifica passati alla funzione di callback di controllo preliminare pulita.
ms.assetid: 65B3B116-6E83-46F5-AE2B-92A41AE39480
keywords:
- MPCLEAN_PRECHECK_DATA funzionalità dell'ambiente Windows legacy
- PMPCLEAN_PRECHECK_DATA puntatore alla struttura Legacy Windows Environment Features
topic_type:
- apiref
api_name:
- MPCLEAN_PRECHECK_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc272ed230a67811497f0eebb99624d74369c8c55419fba970f326fba502e8b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118747927"
---
# <a name="mpclean_precheck_data-structure"></a>Struttura MPCLEAN \_ PRECHECK \_ DATA

Dati di notifica passati alla funzione di callback di controllo preliminare pulita.

## <a name="syntax"></a>Sintassi


```C++
typedef struct tagMPCLEAN_PRECHECK_DATA {
  PMPRESOURCE_INFO     BlockedResourceInfo;
  BlockingResourceInfo PMPRESOURCE_INFO;
} MPCLEAN_PRECHECK_DATA, *PMPCLEAN_PRECHECK_DATA;
```



## <a name="members"></a>Members

<dl> <dt>

**BlockedResourceInfo**
</dt> <dd>

Tipo: **PMPRESOURCE \_ INFO**

</dd> <dd>

Informazioni sulla risorsa bloccata. Ad esempio, quando lo stato di avanzamento **è MPNOTIFY \_ PRECHECK \_ RESOURCE \_ BLOCKED**. Vedere [**MPRESOURCE \_ INFO**](mpresource-info.md).

</dd> <dt>

**PMPRESOURCE \_ INFO**
</dt> <dd>

Tipo: **BlockingResourceInfo**

</dd> <dd>

Informazioni sulle risorse bloccate. Ad esempio, quando lo stato di avanzamento **è MPNOTIFY \_ PRECHECK \_ RESOURCE \_ BLOCKED**. Vedere [**MPRESOURCE \_ INFO**](mpresource-info.md).

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                            |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MPRESOURCE \_ INFO**](mpresource-info.md)
</dt> </dl>

 

 





