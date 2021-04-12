---
description: Definisce i codici di errore della chiave multimediale per il motore multimediale.
ms.assetid: F6E13260-74A2-40D0-A704-4E1CDB16B8D8
title: Enumerazione MF_MEDIA_ENGINE_KEYERR
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
ms.openlocfilehash: 22dd22a7771f5d1e9466709f0b0da9ee936ef2b9
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351346"
---
# <a name="mf_media_engine_keyerr-enumeration"></a>\_ \_ Enumerazione KEYERR del motore multimediale MF \_

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

<span id="MF_MEDIAENGINE_KEYERR_UNKNOWN"></span><span id="mf_mediaengine_keyerr_unknown"></span>**MF \_ MEDIAENGINE \_ KEYERR \_ sconosciuto**
</dt> <dd>

Si è verificato un errore sconosciuto.

</dd> <dt>

<span id="MF_MEDIAENGINE_KEYERR_CLIENT"></span><span id="mf_mediaengine_keyerr_client"></span>**\_ \_ client KEYERR MF \_ MEDIAENGINE**
</dt> <dd>

Si è verificato un errore con il client.

</dd> <dt>

<span id="MF_MEDIAENGINE_KEYERR_SERVICE"></span><span id="mf_mediaengine_keyerr_service"></span>**\_ \_ servizio KEYERR MF \_ MEDIAENGINE**
</dt> <dd>

Si è verificato un errore con il servizio.

</dd> <dt>

<span id="MF_MEDIAENGINE_KEYERR_OUTPUT"></span><span id="mf_mediaengine_keyerr_output"></span>**\_ \_ output KEYERR MF \_ MEDIAENGINE**
</dt> <dd>

Si è verificato un errore con l'output.

</dd> <dt>

<span id="MF_MEDIAENGINE_KEYERR_HARDWARECHANGE_"></span><span id="mf_mediaengine_keyerr_hardwarechange_"></span>**MF \_ MEDIAENGINE \_ KEYERR \_ HARDWARECHANGE** 
</dt> <dd>

Si è verificato un errore relativo a una modifica dell'hardware.

</dd> <dt>

<span id="MF_MEDIAENGINE_KEYERR_DOMAIN"></span><span id="mf_mediaengine_keyerr_domain"></span>**\_dominio MF MEDIAENGINE \_ KEYERR \_**
</dt> <dd>

Si è verificato un errore relativo al dominio.

</dd> </dl>

## <a name="remarks"></a>Commenti

**MF \_ Il \_ motore multimediale \_ KEYERR** viene usato con il parametro *Code* di [**IMFMediaKeySessionNotify:: Error**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediakeysessionnotify-keyerror) e il valore del *codice* restituito da [**IMFMediaKeySession:: GetError**](imfmediakeysession-geterror.md).

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

 

 




