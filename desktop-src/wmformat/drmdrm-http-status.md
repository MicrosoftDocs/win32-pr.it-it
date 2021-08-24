---
title: DRM_HTTP_STATUS enumerazione (Wmdrmsdk.h)
description: Il tipo di enumerazione \_ DRM HTTP \_ STATUS definisce un intervallo di stati HTTP per una richiesta DRM.
ms.assetid: 09183ef9-4832-4469-a960-dbeb67381949
keywords:
- DRM_HTTP_STATUS enumerazione windows Media Format
- enumerazione windows Media Format
topic_type:
- apiref
api_name:
- DRM_HTTP_STATUS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 385a52811cc8deb7e1c221737bd97391122160de065ca28111132ee6c5e4a859
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119447761"
---
# <a name="drm_http_status-enumeration-wmdrmsdkh"></a>DRM_HTTP_STATUS enumerazione (Wmdrmsdk.h)

Il **tipo di enumerazione \_ DRM HTTP \_ STATUS** definisce un intervallo di stati HTTP per una richiesta DRM.

## <a name="syntax"></a>Sintassi


```C++
typedef enum DRM_HTTP_STATUS { 
  HTTP_NOTINITIATED  = 0,
  HTTP_CONNECTING    = 1,
  HTTP_REQUESTING    = 2,
  HTTP_RECEIVING     = 3,
  HTTP_COMPLETED     = 4
} ;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="HTTP_NOTINITIATED"></span><span id="http_notinitiated"></span>**HTTP \_ NON AVVIATO**
</dt> <dd>

Le operazioni HTTP non sono state avviate.

</dd> <dt>

<span id="HTTP_CONNECTING"></span><span id="http_connecting"></span>**CONNESSIONE \_ HTTP**
</dt> <dd>

È in corso la connessione.

</dd> <dt>

<span id="HTTP_REQUESTING"></span><span id="http_requesting"></span>**RICHIESTA \_ HTTP**
</dt> <dd>

È in corso la richiesta dei dati.

</dd> <dt>

<span id="HTTP_RECEIVING"></span><span id="http_receiving"></span>**RICEZIONE \_ HTTP**
</dt> <dd>

È in corso la ricezione dei dati.

</dd> <dt>

<span id="HTTP_COMPLETED"></span><span id="http_completed"></span>**HTTP \_ COMPLETATO**
</dt> <dd>

Le operazioni HTTP sono state completate.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa enumerazione viene utilizzata dalla [**struttura WM \_ INDIVIDUALIZE \_ STATUS.**](drmwm-individualize-status.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Tipi di enumerazione**](drm-enumeration-types.md)
</dt> </dl>

 

 





