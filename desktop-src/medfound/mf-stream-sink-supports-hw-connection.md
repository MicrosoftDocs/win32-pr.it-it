---
description: Indica se un sink multimediale supporta il flusso di dati hardware.
ms.assetid: 15838467-D253-4ECE-B9E7-AFD3A21B3AF2
title: Attributo MF_STREAM_SINK_SUPPORTS_HW_CONNECTION (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a95bfecba4cf53b6ef7c8863ec0456e310d8bcb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485205"
---
# <a name="mf_stream_sink_supports_hw_connection-attribute"></a>Il \_ sink di flusso MF \_ supporta l'attributo di \_ \_ \_ connessione HW

Indica se un sink multimediale supporta il flusso di dati hardware.

## <a name="data-type"></a>Tipo di dati

**Bool** archiviato come **UInt32**

## <a name="remarks"></a>Commenti

Questo attributo viene usato quando un sink multimediale delega un dispositivo hardware ed è in grado di ricevere dati tramite un bus hardware. Ad esempio, un decoder audio hardware può inviare dati audio direttamente all'hardware per il rendering audio.

In questo scenario, il decodificatore e il sink sono ancora rappresentati nel Microsoft Media Foundation da una [trasformazione di Media Foundation](media-foundation-transforms.md) (MFT) e da un sink multimediale. Tuttavia, nessun flusso di dati tra questi due oggetti a livello di pipeline, solo a livello di hardware, come illustrato nella figura seguente.

![diagramma che mostra un'origine del proxy hardware.](images/proxy-mft4.png)

La connessione tra il MFT e il sink multimediale viene negoziata come indicato di seguito.

1.  La pipeline controlla se il MFT è un proxy hardware controllando l'attributo dell' [ \_ \_ \_ \_ attributo dell'URL dell'enumerazione MFT](mft-enum-hardware-url-attribute.md) nell'MFT. Per informazioni dettagliate, vedere [hardware MFTS](hardware-mfts.md).
2.  La pipeline ottiene un puntatore all'interfaccia [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) del sink del flusso sul sink multimediale.
3.  La pipeline usa il puntatore [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) per eseguire una query per il \_ sink di flusso MF supporta l'attributo di \_ \_ \_ \_ connessione HW. Se questo attributo è presente e uguale a **true**, l'origine supporto supporta le connessioni hardware.
4.  La pipeline imposta l'attributo dell' [ \_ \_ \_ attributo del flusso connesso a MFT](mft-connected-stream-attribute.md) nel sink di flusso. Il valore di questo attributo è il puntatore [**IMFAttribute**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) da MFT.
5.  La pipeline imposta il [MFT \_ connesso \_ all'attributo del \_ \_ flusso HW](mft-connected-to-hw-stream.md) su **true** sia nel sink di flusso sia in quello MFT.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App desktop di Windows 8 app \[ \| UWP\]<br/>                                  |
| Server minimo supportato<br/> | App UWP per \[ app desktop di Windows Server 2012 \|\]<br/>                        |
| Intestazione<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




