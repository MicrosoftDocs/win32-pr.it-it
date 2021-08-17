---
title: DRM_INDIVIDUALIZATION_STATUS enumerazione (Wmdrmsdk.h)
description: Il tipo di enumerazione DRM \_ INDIVIDUALIZATION \_ STATUS definisce gli stati validi per l'individualizzazione DRM. | DRM_INDIVIDUALIZATION_STATUS enumerazione (Wmdrmsdk.h)
ms.assetid: 4e6712e2-3297-4636-9b0c-07269bd63d52
keywords:
- DRM_INDIVIDUALIZATION_STATUS di enumerazione windows Media Format
- enumerazione windows Media Format
topic_type:
- apiref
api_name:
- DRM_INDIVIDUALIZATION_STATUS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47e339fda95ccf7408ad2f218179cfb591da217b16fbbce9c9870eabd7437eaf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117848227"
---
# <a name="drm_individualization_status-enumeration-wmdrmsdkh"></a>DRM_INDIVIDUALIZATION_STATUS enumerazione (Wmdrmsdk.h)

Il **tipo di enumerazione DRM \_ INDIVIDUALIZATION \_ STATUS** definisce gli stati validi per l'individualizzazione DRM.

## <a name="syntax"></a>Sintassi


```C++
typedef enum DRM_INDIVIDUALIZATION_STATUS { 
  INDI_UNDEFINED  = 0x0000,
  INDI_BEGIN      = 0x0001,
  INDI_SUCCEED    = 0x0002,
  INDI_FAIL       = 0x0004,
  INDI_CANCEL     = 0x0008,
  INDI_DOWNLOAD   = 0x0010,
  INDI_INSTALL    = 0x0020
} ;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="INDI_UNDEFINED"></span><span id="indi_undefined"></span>**INDI \_ UNDEFINED**
</dt> <dd>

Questo valore è riservato per l'uso futuro.

</dd> <dt>

<span id="INDI_BEGIN"></span><span id="indi_begin"></span>**INDI \_ BEGIN**
</dt> <dd>

Indica l'inizio del processo di individualizzazione.

</dd> <dt>

<span id="INDI_SUCCEED"></span><span id="indi_succeed"></span>**INDI \_ SUCCEED**
</dt> <dd>

Indica che il processo di individualizzazione è stato completato.

</dd> <dt>

<span id="INDI_FAIL"></span><span id="indi_fail"></span>**INDI \_ FAIL**
</dt> <dd>

Indica che il processo di individualizzazione non è riuscito.

</dd> <dt>

<span id="INDI_CANCEL"></span><span id="indi_cancel"></span>**INDI \_ CANCEL**
</dt> <dd>

Indica che il processo di individualizzazione è stato annullato dall'applicazione.

</dd> <dt>

<span id="INDI_DOWNLOAD"></span><span id="indi_download"></span>**INDI \_ DOWNLOAD**
</dt> <dd>

Indica che è in corso il download dell'aggiornamento della sicurezza.

</dd> <dt>

<span id="INDI_INSTALL"></span><span id="indi_install"></span>**INDI \_ INSTALL**
</dt> <dd>

Indica che è in corso l'installazione dell'aggiornamento della sicurezza.

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

 

 





