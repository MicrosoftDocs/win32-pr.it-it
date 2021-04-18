---
description: "Contiene l'URL del file IFO (informazioni DVD) specificato dal server HTTP nell'intestazione HTTP &\\# 0034; Pragma: ifoFileURI.dlna.org&\\# 0034;."
ms.assetid: 007e0f4d-fb37-4dec-96a7-311df567eb04
title: Attributo MF_BYTESTREAM_IFO_FILE_URI (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1c80e015b68272b073c442b4064c80a6787b811
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309588"
---
# <a name="mf_bytestream_ifo_file_uri-attribute"></a>\_ \_ \_ Attributo URI del file MF BYTESTREAM IFO \_

Contiene l'URL del file IFO (informazioni DVD) specificato dal server HTTP nell'intestazione HTTP "pragma: ifoFileURI.dlna.org".

## <a name="data-type"></a>Tipo di dati

**LPWSTR**

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes:: GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).

Per impostare questo attributo, chiamare [**IMFAttributes:: sestring**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).

## <a name="applies-to"></a>Si applica a

[**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)

## <a name="remarks"></a>Commenti

Il flusso di byte HTTP cerca la stringa "ifoFileURI.dlna.org" nell'intestazione HTTP. Se la stringa viene trovata, viene copiata in questo attributo nel flusso di byte.

La costante GUID per questo attributo viene esportata da mfuuid. lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App desktop di Windows 7 \[ \| UWP\]<br/>                                                        |
| Server minimo supportato<br/> | App desktop di Windows Server 2008 R2 \[ \| UWP\]<br/>                                           |
| Intestazione<br/>                   | <dl> <dt>Mfobjects. h (include Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributi del flusso di byte](byte-stream-attributes.md)
</dt> <dt>

[**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)
</dt> </dl>

 

 




