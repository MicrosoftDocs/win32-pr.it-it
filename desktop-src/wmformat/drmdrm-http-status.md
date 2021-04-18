---
title: Enumerazione DRM_HTTP_STATUS (wmdrmsdk. h)
description: Il \_ \_ tipo di enumerazione stato http DRM definisce un intervallo di stati http per una richiesta DRM.
ms.assetid: 09183ef9-4832-4469-a960-dbeb67381949
keywords:
- Formato Windows Media enumerazione DRM_HTTP_STATUS
- Enumerazione formato Windows Media
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
ms.openlocfilehash: 367c5a40af45fd573f7f5033b9be3b037079cb30
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331990"
---
# <a name="drm_http_status-enumeration-wmdrmsdkh"></a>Enumerazione DRM_HTTP_STATUS (wmdrmsdk. h)

Il tipo di enumerazione **\_ \_ stato http DRM** definisce un intervallo di stati http per una richiesta DRM.

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

<span id="HTTP_NOTINITIATED"></span><span id="http_notinitiated"></span>**\_NOTINITIATED http**
</dt> <dd>

Le operazioni HTTP non sono state avviate.

</dd> <dt>

<span id="HTTP_CONNECTING"></span><span id="http_connecting"></span>**\_connessione http**
</dt> <dd>

Viene stabilita la connessione.

</dd> <dt>

<span id="HTTP_REQUESTING"></span><span id="http_requesting"></span>**\_richiesta http**
</dt> <dd>

I dati sono richiesti.

</dd> <dt>

<span id="HTTP_RECEIVING"></span><span id="http_receiving"></span>**\_ricezione http**
</dt> <dd>

Sono in corso la ricezione dei dati.

</dd> <dt>

<span id="HTTP_COMPLETED"></span><span id="http_completed"></span>**HTTP \_ completato**
</dt> <dd>

Le operazioni HTTP sono state completate.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa enumerazione viene utilizzata dalla struttura [**di \_ \_ stato di personalizzazione WM**](drmwm-individualize-status.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Tipi di enumerazione**](drm-enumeration-types.md)
</dt> </dl>

 

 





