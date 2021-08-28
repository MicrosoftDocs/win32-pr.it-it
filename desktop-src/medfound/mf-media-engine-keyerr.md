---
description: Definisce i codici di errore della chiave multimediale per il motore multimediale.
ms.assetid: F6E13260-74A2-40D0-A704-4E1CDB16B8D8
title: MF_MEDIA_ENGINE_KEYERR enumerazione
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MF_MEDIA_ENGINE_KEYERR
api_type:
- HeaderDef
api_location:
- mfmediaengine.h
ms.openlocfilehash: 5a3573f721f31ffbe3858c7d6fb3c713468bc347f04a1b5d85c5839a1e18511b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113931"
---
# <a name="mf_media_engine_keyerr-enumeration"></a>Enumerazione MF \_ MEDIA \_ ENGINE \_ KEYERR

Definisce i codici di errore della chiave multimediale per il motore multimediale.

## <a name="syntax"></a>Sintassi


```C++
typedef enum _MF_MEDIA_ENGINE_KEYERR { 
  MF_MEDIAENGINE_KEYERR_UNKNOWN          = 1,
  MF_MEDIAENGINE_KEYERR_CLIENT           = 2,
  MF_MEDIAENGINE_KEYERR_SERVICE          = 3,
  MF_MEDIAENGINE_KEYERR_OUTPUT           = 4,
  MF_MEDIAENGINE_KEYERR_HARDWARECHANGE   = 5,
  MF_MEDIAENGINE_KEYERR_DOMAIN           = 6
} MF_MEDIA_ENGINE_KEYERR;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="MF_MEDIAENGINE_KEYERR_UNKNOWN"></span><span id="mf_mediaengine_keyerr_unknown"></span>**MF \_ MEDIAENGINE \_ KEYERR \_ UNKNOWN**
</dt> <dd>

Si è verificato un errore sconosciuto.

</dd> <dt>

<span id="MF_MEDIAENGINE_KEYERR_CLIENT"></span><span id="mf_mediaengine_keyerr_client"></span>**MF \_ MEDIAENGINE \_ KEYERR \_ CLIENT**
</dt> <dd>

Si è verificato un errore con il client.

</dd> <dt>

<span id="MF_MEDIAENGINE_KEYERR_SERVICE"></span><span id="mf_mediaengine_keyerr_service"></span>**SERVIZIO MF \_ MEDIAENGINE \_ \_ KEYERR**
</dt> <dd>

Si è verificato un errore con il servizio.

</dd> <dt>

<span id="MF_MEDIAENGINE_KEYERR_OUTPUT"></span><span id="mf_mediaengine_keyerr_output"></span>**OUTPUT DI \_ MF MEDIAENGINE \_ \_ KEYERR**
</dt> <dd>

Si è verificato un errore con l'output.

</dd> <dt>

<span id="MF_MEDIAENGINE_KEYERR_HARDWARECHANGE_"></span><span id="mf_mediaengine_keyerr_hardwarechange_"></span>**MF \_ MEDIAENGINE \_ KEYERR \_ HARDWARECHANGE** 
</dt> <dd>

Si è verificato un errore correlato a una modifica hardware.

</dd> <dt>

<span id="MF_MEDIAENGINE_KEYERR_DOMAIN"></span><span id="mf_mediaengine_keyerr_domain"></span>**DOMINIO MF \_ MEDIAENGINE \_ \_ KEYERR**
</dt> <dd>

Si è verificato un errore con il dominio.

</dd> </dl>

## <a name="remarks"></a>Commenti

**MF \_ MEDIA \_ ENGINE \_ KEYERR** viene usato con il parametro *di* codice [**IMFMediaKeySessionNotify::KeyError**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediakeysessionnotify-keyerror) e il valore del codice restituito da [**IMFMediaKeySession::GetError**](imfmediakeysession-geterror.md). 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8.1 solo app desktop\]<br/>                                                 |
| Server minimo supportato<br/> | Windows Server 2012 Solo app desktop R2 \[\]<br/>                                      |
| Idl<br/>                      | <dl> <dt>Mfmediaengine.idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Media Foundation enumerazioni](media-foundation-enumerations.md)
</dt> </dl>

 

 




