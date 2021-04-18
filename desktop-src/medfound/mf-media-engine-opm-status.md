---
description: Definisce lo stato di output Protection Manager (OPM).
ms.assetid: 7C4D88F6-369B-4364-90C4-6D0F8DD1523B
title: Enumerazione MF_MEDIA_ENGINE_OPM_STATUS
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MF_MEDIA_ENGINE_OPM_STATUS
api_type:
- HeaderDef
api_location:
- mfmediaengine.h
ms.openlocfilehash: 73585bf63bc559f30ce114730274e30518497b05
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320545"
---
# <a name="mf_media_engine_opm_status-enumeration"></a>\_ \_ \_ Enumerazione stato OPM del motore multimediale MF \_

Definisce lo stato di [Output Protection Manager](output-protection-manager.md) (OPM).

## <a name="syntax"></a>Sintassi


```C++
typedef enum _MF_MEDIA_ENGINE_OPM_STATUS { 
  MF_MEDIA_ENGINE_OPM_NOT_REQUESTED           =  0,
  MF_MEDIA_ENGINE_OPM_ESTABLISHED             = 1,
  MF_MEDIA_ENGINE_OPM_FAILED_VM               = 2,
  MF_MEDIA_ENGINE_OPM_FAILED_BDA              = 3,
  MF_MEDIA_ENGINE_OPM_FAILED_UNSIGNED_DRIVER  = 4,
  MF_MEDIA_ENGINE_OPM_FAILED                  = 5
} MF_MEDIA_ENGINE_OPM_STATUS;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="MF_MEDIA_ENGINE_OPM_NOT_REQUESTED"></span><span id="mf_media_engine_opm_not_requested"></span>**MF \_ media \_ Engine \_ OPM \_ non \_ richiesto**
</dt> <dd>

Stato predefinito. Utilizzato per restituire lo stato corretto quando il contenuto non è protetto.

</dd> <dt>

<span id="MF_MEDIA_ENGINE_OPM_ESTABLISHED"></span><span id="mf_media_engine_opm_established"></span>**MF \_ media \_ Engine \_ OPM \_ stabilito**
</dt> <dd>

La creazione di OPM è stata completata.

</dd> <dt>

<span id="MF_MEDIA_ENGINE_OPM_FAILED_VM"></span><span id="mf_media_engine_opm_failed_vm"></span>**\_ \_ \_ \_ VM non riuscita del motore multimediale MF \_**
</dt> <dd>

OPM non riuscito perché è in esecuzione in una macchina virtuale (VM).

</dd> <dt>

<span id="MF_MEDIA_ENGINE_OPM_FAILED_BDA"></span><span id="mf_media_engine_opm_failed_bda"></span>**MF \_ media \_ Engine \_ OPM \_ non riuscito \_ BDA**
</dt> <dd>

OPM non riuscito perché non è presente alcun driver grafico e il sistema usa la scheda di visualizzazione di base (BDA).

</dd> <dt>

<span id="MF_MEDIA_ENGINE_OPM_FAILED_UNSIGNED_DRIVER"></span><span id="mf_media_engine_opm_failed_unsigned_driver"></span>**\_ \_ \_ \_ \_ driver non firmato \_ per MF Media Engine OPM**
</dt> <dd>

L'accesso ad OPM non è riuscito perché il driver di grafica non è firmato PE e viene eseguito il fallback a WARP.

</dd> <dt>

<span id="MF_MEDIA_ENGINE_OPM_FAILED"></span><span id="mf_media_engine_opm_failed"></span>**MF \_ media \_ Engine \_ OPM \_ non riuscito**
</dt> <dd>

OPM non riuscito per altri motivi.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8.1 \[ solo app desktop\]<br/>                                                 |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2012 R2 \[\]<br/>                                      |
| IDL<br/>                      | <dl> <dt>Mfmediaengine. idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni di Media Foundation](media-foundation-enumerations.md)
</dt> </dl>

 

 




