---
description: "Contiene l'URL del file IFO (DVD Information) specificato dal server HTTP nell'intestazione HTTP, &\\# 0034; Pragma: ifoFileURI.dlna.org&\\# 0034;."
ms.assetid: 007e0f4d-fb37-4dec-96a7-311df567eb04
title: MF_BYTESTREAM_IFO_FILE_URI attributo (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab4349f3319a875f428921b0a99aefa61e49340c240a87260c1132abcc7c45f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119723471"
---
# <a name="mf_bytestream_ifo_file_uri-attribute"></a>Attributo \_ URI \_ FILE IFO BYTESTREAM MF \_ \_

Contiene l'URL del file IFO (DVD Information) specificato dal server HTTP nell'intestazione HTTP "Pragma: ifoFileURI.dlna.org".

## <a name="data-type"></a>Tipo di dati

**LPWSTR**

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes::GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).

Per impostare questo attributo, chiamare [**IMFAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).

## <a name="applies-to"></a>Si applica a

[**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)

## <a name="remarks"></a>Commenti

Il flusso di byte HTTP cerca la stringa "ifoFileURI.dlna.org" nell'intestazione HTTP. Se la stringa viene trovata, viene copiata in questo attributo nel flusso di byte.

La costante GUID per questo attributo viene esportata da mfuuid.lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop app \| UWP\]<br/>                                                        |
| Server minimo supportato<br/> | Windows App UWP per app desktop server 2008 R2 \[ \|\]<br/>                                           |
| Intestazione<br/>                   | <dl> <dt>Mfobjects.h (includere Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico di Media Foundation attributi](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributi del flusso di byte](byte-stream-attributes.md)
</dt> <dt>

[**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)
</dt> </dl>

 

 




