---
title: DRM_HTTP_STATUS enumerazione (Drmexternals.h)
description: Il tipo di enumerazione \_ DRM HTTP \_ STATUS definisce un intervallo di stati per una richiesta DRM.
ms.assetid: 9e0fb060-3fbf-45d0-872b-4d666ea9a88d
keywords:
- DRM_HTTP_STATUS enumerazione Windows Media Format
- enumeration windows Media Format
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
ms.openlocfilehash: e222cbf24e6333c7105e8564a5ad255693340749aeea32d98bd013bcb40995d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119586301"
---
# <a name="drm_http_status-enumeration-drmexternalsh"></a>DRM_HTTP_STATUS enumerazione (Drmexternals.h)

Il **tipo di enumerazione \_ DRM HTTP \_ STATUS** definisce un intervallo di stati per una [*richiesta DRM.*](wmformat-glossary.md)

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

È in corso la richiesta di dati.

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

Questa enumerazione viene utilizzata dalla [**struttura WM \_ INDIVIDUALIZE \_ STATUS.**](wm-individualize-status.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                      |
| Versione<br/>                  | Windows Media Format 7 SDK o versioni successive dell'SDK<br/>                       |
| Intestazione<br/>                   | <dl> <dt>Drmexternals.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**STATO \_ DI INDIVIDUALIZZAZIONE \_ DRM**](drm-individualization-status.md)
</dt> <dt>

[**Tipi di enumerazione**](enumeration-types.md)
</dt> </dl>

 

 





