---
description: Contiene un puntatore all'interfaccia di callback delle applicazioni per il writer del sink.
ms.assetid: 22df1fa0-469d-4501-aaf0-a0379b7ed096
title: Attributo MF_SINK_WRITER_ASYNC_CALLBACK (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f11bed051df9107ca3a2247b6c3d0cf2058224c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759569"
---
# <a name="mf_sink_writer_async_callback-attribute"></a>\_Attributo di \_ \_ callback asincrono del writer di sink MF \_

Contiene un puntatore all'interfaccia di callback dell'applicazione per il writer del sink.

## <a name="data-type"></a>Tipo di dati

**[](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwritercallback) IMFSinkWriterCallback \** _ archiviato come _*IUnknown \**_

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [_ *IMFAttributes:: getunknown* *](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).

Per impostare questo attributo, chiamare [**IMFAttributes:: seunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).

## <a name="remarks"></a>Commenti

Il valore di questo attributo è un puntatore all'interfaccia [**IMFSinkWriterCallback**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwritercallback) dell'applicazione.

Utilizzare questo attributo con le funzioni seguenti:

-   [**MFCreateSinkWriterFromMediaSink**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink)
-   [**MFCreateSinkWriterFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App desktop di Windows 7 \[ \| UWP\]<br/>                                        |
| Server minimo supportato<br/> | App desktop di Windows Server 2008 R2 \[ \| UWP\]<br/>                           |
| Intestazione<br/>                   | <dl> <dt>Mfreadwrite. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributi del writer di sink](sink-writer-attributes.md)
</dt> </dl>

 

 




