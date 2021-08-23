---
title: DRM_INDIVIDUALIZATION_STATUS enumerazione (Drmexternals.h)
description: Il tipo di enumerazione DRM \_ INDIVIDUALIZATION \_ STATUS definisce gli stati validi per l'individualizzazione DRM. | DRM_INDIVIDUALIZATION_STATUS enumerazione (Drmexternals.h)
ms.assetid: 76748fb3-340e-47e2-969d-5e857bb4e4d8
keywords:
- DRM_INDIVIDUALIZATION_STATUS enumerazione Windows Media Format
- enumeration windows Media Format
topic_type:
- apiref
api_name:
- DRM_INDIVIDUALIZATION_STATUS
api_location:
- Drmexternals.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 081a8714d29cb48236bdb9191c15e92db96b18a9f8c1d9c2388c5baee7783296
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119705651"
---
# <a name="drm_individualization_status-enumeration-drmexternalsh"></a>DRM_INDIVIDUALIZATION_STATUS enumerazione (Drmexternals.h)

Il **tipo di enumerazione DRM \_ INDIVIDUALIZATION \_ STATUS** definisce gli stati validi per la [*individualizzazione*](wmformat-glossary.md)DRM. Quando un'applicazione avvia l'individualizzazione con una chiamata a [**IWMDRMReader::Individualize,**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-individualize)lo stato di avanzamento della richiesta di individualizzazione viene trasmesso all'applicazione tramite chiamate al metodo [**IWMStatusCallback::OnStatus.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) Tutti i messaggi di stato di individualizzazione useranno il membro WMT \_ INDIVIDUALIZE del tipo [**di enumerazione \_ WMT STATUS**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_status) come *parametro* Status. Lo stato dell'individualizzazione viene passato **a OnStatus** nel *parametro pValue.*

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

Indica che il processo di individualizzazione è stato annullato come risultato di una chiamata a [**IWMDRMReader::CancelIndividualization.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-cancelindividualization)

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

[**STATO \_ HTTP \_ DRM**](drm-http-status.md)
</dt> <dt>

[**Tipi di enumerazione**](enumeration-types.md)
</dt> </dl>

 

 





