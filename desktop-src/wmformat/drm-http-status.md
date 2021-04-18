---
title: Enumerazione DRM_HTTP_STATUS (Drmexternals. h)
description: Il \_ \_ tipo di enumerazione stato http DRM definisce un intervallo di stati per una richiesta DRM.
ms.assetid: 9e0fb060-3fbf-45d0-872b-4d666ea9a88d
keywords:
- Formato Windows Media enumerazione DRM_HTTP_STATUS
- Enumerazione formato Windows Media
topic_type:
- apiref
api_name:
- DRM_HTTP_STATUS
api_location:
- Drmexternals.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93d61803cab6cb80932402e429e77228a1611fd9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302064"
---
# <a name="drm_http_status-enumeration-drmexternalsh"></a>Enumerazione DRM_HTTP_STATUS (Drmexternals. h)

Il tipo di enumerazione **\_ \_ stato http DRM** definisce un intervallo di stati per una richiesta [*DRM*](wmformat-glossary.md) .

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

Questa enumerazione viene utilizzata dalla struttura [**di \_ \_ stato di personalizzazione WM**](wm-individualize-status.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                      |
| Versione<br/>                  | Windows Media Format 7 SDK o versioni successive dell'SDK<br/>                       |
| Intestazione<br/>                   | <dl> <dt>Drmexternals. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_stato di individualizzazione DRM \_**](drm-individualization-status.md)
</dt> <dt>

[**Tipi di enumerazione**](enumeration-types.md)
</dt> </dl>

 

 





