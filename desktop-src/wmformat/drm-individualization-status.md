---
title: Enumerazione DRM_INDIVIDUALIZATION_STATUS (Drmexternals. h)
description: Il \_ \_ tipo di enumerazione dello stato di individualizzazione DRM definisce gli stati validi per l'individualizzazione DRM. | Enumerazione DRM_INDIVIDUALIZATION_STATUS (Drmexternals. h)
ms.assetid: 76748fb3-340e-47e2-969d-5e857bb4e4d8
keywords:
- Formato Windows Media enumerazione DRM_INDIVIDUALIZATION_STATUS
- Enumerazione formato Windows Media
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
ms.openlocfilehash: e8d59a19c58c775ee22d78e17bc09add2825948e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104401911"
---
# <a name="drm_individualization_status-enumeration-drmexternalsh"></a>Enumerazione DRM_INDIVIDUALIZATION_STATUS (Drmexternals. h)

Il tipo di enumerazione **\_ \_ dello stato di individualizzazione DRM** definisce gli stati validi per l' [*individualizzazione*](wmformat-glossary.md)DRM. Quando un'applicazione avvia l'individualizzazione con una chiamata a [**IWMDRMReader:: individualizzato**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-individualize), lo stato di avanzamento della richiesta di individualizzazione viene trasmesso all'applicazione tramite chiamate al metodo [**IWMStatusCallback:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) . I messaggi di stato di individualizzazione utilizzeranno tutti il \_ membro WMT di individuazione del tipo di enumerazione [**\_ stato WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_status) come parametro *status* . Lo stato della individualizzazione viene passato a **OnStatus** nel parametro *pValue* .

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

Indica che il processo di individualizzazione è stato annullato in seguito a una chiamata a [**IWMDRMReader:: CancelIndividualization**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-cancelindividualization).

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

[**\_stato http \_ DRM**](drm-http-status.md)
</dt> <dt>

[**Tipi di enumerazione**](enumeration-types.md)
</dt> </dl>

 

 





