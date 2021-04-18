---
description: Indica se un'origine supporto supporta il flusso di dati hardware.
ms.assetid: 32FEBC99-0AE0-4FE9-90AB-5FB204BD4C83
title: Attributo MF_SOURCE_STREAM_SUPPORTS_HW_CONNECTION (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 751d672e664ab1849376d839285393075ddf6af6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316433"
---
# <a name="mf_source_stream_supports_hw_connection-attribute"></a>MF \_ source \_ Stream \_ supporta \_ l' \_ attributo di connessione HW

Indica se un'origine supporto supporta il flusso di dati hardware.

## <a name="data-type"></a>Tipo di dati

**Bool** archiviato come **UInt32**

## <a name="remarks"></a>Commenti

Questo attributo viene usato quando un'origine multimediale Invia un proxy a un dispositivo hardware ed è in grado di trasferire i dati a valle su un bus hardware, senza inviare dati alla CPU. Una webcam, ad esempio, può consegnare il video con codifica H. 264 direttamente a un decodificatore hardware integrato.

In questo scenario l'origine e il decodificatore sono ancora rappresentati nel Microsoft Media Foundation da un oggetto di [origine multimediale](media-sources.md) e da una [trasformazione di Media Foundation](media-foundation-transforms.md) (MFT). Tuttavia, nessun flusso di dati tra questi due oggetti a livello di pipeline, solo a livello di hardware, come illustrato nella figura seguente.

![diagramma che mostra un'origine del proxy hardware.](images/proxy-mft3.png)

La connessione tra l'origine multimediale e la MFT è negoziata come indicato di seguito.

1.  La pipeline esegue una query sull'origine multimediale per l'interfaccia [**IMFMediaSourceEx**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex) . Questa interfaccia è facoltativa per supportare le origini multimediali.
2.  La pipeline chiama [**IMFMediaSourceEx:: GetStreamAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) per ottenere un puntatore [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .
3.  Le query della pipeline per il \_ flusso di origine MF \_ supportano l'attributo di \_ \_ \_ connessione HW. Se l'attributo è presente e uguale a **true**, l'origine supporto supporta le connessioni hardware.
4.  La pipeline controlla se il MFT è anche un proxy hardware controllando l'attributo dell' [ \_ \_ \_ \_ attributo dell'URL dell'enumerazione MFT](mft-enum-hardware-url-attribute.md) nell'MFT. Per informazioni dettagliate, vedere [hardware MFTS](hardware-mfts.md).
5.  La pipeline imposta l'attributo dell' [ \_ \_ \_ attributo del flusso connesso MFT](mft-connected-stream-attribute.md) in MFT. Il valore di questo attributo è il puntatore [**IMFAttribute**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) ottenuto dall'origine multimediale nel passaggio 2.
6.  La pipeline imposta il [MFT \_ connesso \_ all'attributo del \_ \_ flusso HW](mft-connected-to-hw-stream.md) su **true** sia nell'origine multimediale che nella MFT.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App desktop di Windows 8 app \[ \| UWP\]<br/>                                  |
| Server minimo supportato<br/> | App UWP per \[ app desktop di Windows Server 2012 \|\]<br/>                        |
| Intestazione<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[MFTs hardware](hardware-mfts.md)
</dt> </dl>

 

 




