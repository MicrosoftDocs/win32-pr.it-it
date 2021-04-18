---
description: Specifica il ruolo del dispositivo per il flusso audio.
ms.assetid: E4B7660D-5F41-495A-B77D-94B7981F4C2C
title: Attributo MF_MEDIA_ENGINE_AUDIO_ENDPOINT_ROLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b1b00115a28592140e41463cf296acf54ad7cde
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320552"
---
# <a name="mf_media_engine_audio_endpoint_role-attribute"></a>\_Attributo del \_ \_ ruolo dell' \_ endpoint audio del motore multimediale \_ MF

Specifica il ruolo del dispositivo per il flusso audio.

## <a name="data-type"></a>Tipo di dati

**[**ERole**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole)** archiviato come **UInt32**

## <a name="remarks"></a>Commenti

Il valore di questo attributo è un membro dell'enumerazione [**ERole**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole) .

Questo attributo viene usato con il metodo [**IMFMediaEngineClassFactory:: CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) per inizializzare il motore multimediale. L'attributo è facoltativo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App desktop di Windows 8 app \[ \| UWP\]<br/>                                            |
| Server minimo supportato<br/> | App UWP per \[ app desktop di Windows Server 2012 \|\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Mfmediaengine. idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
