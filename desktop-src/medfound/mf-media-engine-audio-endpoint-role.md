---
description: Specifica il ruolo del dispositivo per il flusso audio.
ms.assetid: E4B7660D-5F41-495A-B77D-94B7981F4C2C
title: MF_MEDIA_ENGINE_AUDIO_ENDPOINT_ROLE attributo
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53a15a973aef342e3d37cde3e6d9f3dd7d61c553fecaa943215dbcc77a319950
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119104777"
---
# <a name="mf_media_engine_audio_endpoint_role-attribute"></a>Attributo DEL RUOLO \_ \_ ENDPOINT \_ AUDIO \_ \_ DEL MOTORE MULTIMEDIALE MF

Specifica il ruolo del dispositivo per il flusso audio.

## <a name="data-type"></a>Tipo di dati

**[**ERole**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole)** archiviato come **UINT32**

## <a name="remarks"></a>Commenti

Il valore di questo attributo è un membro [**dell'enumerazione ERole.**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole)

Questo attributo viene usato con il [**metodo IMFMediaEngineClassFactory::CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) per inizializzare il motore multimediale. L'attributo è facoltativo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 app desktop \| app UWP\]<br/>                                            |
| Server minimo supportato<br/> | \[Windows Server 2012 app desktop \| app UWP\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Mfmediaengine.idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico di Media Foundation attributi](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
