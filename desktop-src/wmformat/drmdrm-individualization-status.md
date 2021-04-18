---
title: Enumerazione DRM_INDIVIDUALIZATION_STATUS (wmdrmsdk. h)
description: Il \_ \_ tipo di enumerazione dello stato di individualizzazione DRM definisce gli stati validi per l'individualizzazione DRM. | Enumerazione DRM_INDIVIDUALIZATION_STATUS (wmdrmsdk. h)
ms.assetid: 4e6712e2-3297-4636-9b0c-07269bd63d52
keywords:
- Formato Windows Media enumerazione DRM_INDIVIDUALIZATION_STATUS
- Enumerazione formato Windows Media
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
ms.openlocfilehash: b395d3ad4271ccef9964f0d39c74a1e0ba158257
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331989"
---
# <a name="drm_individualization_status-enumeration-wmdrmsdkh"></a>Enumerazione DRM_INDIVIDUALIZATION_STATUS (wmdrmsdk. h)

Il tipo di enumerazione **\_ \_ dello stato di individualizzazione DRM** definisce gli stati validi per l'individualizzazione DRM.

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

<span id="INDI_UNDEFINED"></span><span id="indi_undefined"></span>**INDI non \_ definito**
</dt> <dd>

Questo valore è riservato per l'uso futuro.

</dd> <dt>

<span id="INDI_BEGIN"></span><span id="indi_begin"></span>**\_inizio indi**
</dt> <dd>

Indica l'inizio del processo di individualizzazione.

</dd> <dt>

<span id="INDI_SUCCEED"></span><span id="indi_succeed"></span>**operazione INDI \_ riuscita**
</dt> <dd>

Indica che il processo di individualizzazione è stato completato.

</dd> <dt>

<span id="INDI_FAIL"></span><span id="indi_fail"></span>**\_errore indi**
</dt> <dd>

Indica che il processo di individualizzazione non è riuscito.

</dd> <dt>

<span id="INDI_CANCEL"></span><span id="indi_cancel"></span>**\_Annulla indi**
</dt> <dd>

Indica che il processo di individualizzazione è stato annullato dall'applicazione.

</dd> <dt>

<span id="INDI_DOWNLOAD"></span><span id="indi_download"></span>**\_download indi**
</dt> <dd>

Indica che è in corso il download dell'aggiornamento della sicurezza.

</dd> <dt>

<span id="INDI_INSTALL"></span><span id="indi_install"></span>**\_installazione indi**
</dt> <dd>

Indica che è in corso l'installazione dell'aggiornamento della sicurezza.

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

 

 





