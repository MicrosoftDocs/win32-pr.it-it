---
description: Contiene un puntatore al Gestione dispositivi DXGI per il writer del sink.
ms.assetid: 0328FC02-2D32-480B-BB03-9C78BF317AF5
title: Attributo MF_SINK_WRITER_D3D_MANAGER (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23dea964be1a0ff726a974deaf1949863331df1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318053"
---
# <a name="mf_sink_writer_d3d_manager-attribute"></a>\_ \_ \_ Attributo gestione D3D del writer di sink MF \_

Contiene un puntatore al Gestione dispositivi DXGI per il [writer del sink](sink-writer.md).

## <a name="data-type"></a>Tipo di dati

**IMFDXGIDeviceManager \** _ archiviato come _*IUnknown \**_

## <a name="remarks"></a>Commenti

Il valore di questo attributo è un puntatore all'interfaccia [_ *IMFDXGIDeviceManager* *](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) .

Usare questo attributo per fornire un dispositivo Direct3D per tutti i codificatori video o i sink di supporto caricati dal writer del sink.

Utilizzare questo attributo con le funzioni seguenti:

-   [**MFCreateSinkWriterFromMediaSink**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink)
-   [**MFCreateSinkWriterFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App desktop di Windows 8 app \[ \| UWP\]<br/>                                        |
| Server minimo supportato<br/> | App UWP per \[ app desktop di Windows Server 2012 \|\]<br/>                              |
| Intestazione<br/>                   | <dl> <dt>Mfreadwrite. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Writer sink](sink-writer.md)
</dt> </dl>

 

 




