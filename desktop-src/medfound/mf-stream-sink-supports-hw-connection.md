---
description: Indica se un sink multimediale supporta il flusso di dati hardware.
ms.assetid: 15838467-D253-4ECE-B9E7-AFD3A21B3AF2
title: MF_STREAM_SINK_SUPPORTS_HW_CONNECTION attributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a9f663c492e5ae15590cc9240762e90298122790fa350fae51d09dd1199f6d4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119714377"
---
# <a name="mf_stream_sink_supports_hw_connection-attribute"></a>IL SINK DI FLUSSO MF \_ \_ SUPPORTA \_ \_ L'attributo \_ HW CONNECTION

Indica se un sink multimediale supporta il flusso di dati hardware.

## <a name="data-type"></a>Tipo di dati

**BOOL** archiviato come **UINT32**

## <a name="remarks"></a>Commenti

Questo attributo viene usato quando un sink multimediale esegue il proxy di un dispositivo hardware ed è in grado di ricevere dati tramite un bus hardware. Ad esempio, un decodificatore audio hardware potrebbe inviare dati audio direttamente all'hardware per il rendering audio.

In questo scenario, il decodificatore e il sink sono [](media-foundation-transforms.md) ancora rappresentati nel Microsoft Media Foundation da una trasformazione Media Foundation (MFT) e da un sink multimediale. Tuttavia, nessun flusso di dati tra questi due oggetti a livello di pipeline, solo a livello hardware, come illustrato nel diagramma seguente.

![diagramma che mostra un'origine proxy hardware.](images/proxy-mft4.png)

La connessione tra MFT e il sink multimediale viene negoziata come indicato di seguito.

1.  La pipeline controlla se MFT è un proxy hardware, controllando l'attributo [ \_ MFT ENUM \_ HARDWARE URL \_ \_ Attribute](mft-enum-hardware-url-attribute.md) in MFT. Per informazioni dettagliate, vedere [MFT hardware](hardware-mfts.md).
2.  La pipeline ottiene un puntatore [**all'interfaccia IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) del sink di flusso sul sink multimediale.
3.  La pipeline usa il [**puntatore IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) per eseguire una query per l'attributo \_ MF STREAM \_ SINK \_ SUPPORTS \_ HW \_ CONNECTION. Se questo attributo è presente e uguale a **TRUE,** l'origine multimediale supporta le connessioni hardware.
4.  La pipeline imposta [l'attributo \_ MFT CONNECTED \_ STREAM \_ ATTRIBUTE](mft-connected-stream-attribute.md) nel sink di flusso. Il valore di questo attributo è il [**puntatore IMFAttribute**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) da MFT.
5.  La pipeline imposta [l'attributo MFT \_ CONNECTED TO \_ \_ HW \_ STREAM](mft-connected-to-hw-stream.md) su **TRUE** sia nel sink di flusso che in MFT.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 app desktop \| app UWP\]<br/>                                  |
| Server minimo supportato<br/> | \[Windows Server 2012 app desktop \| app UWP\]<br/>                        |
| Intestazione<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico di Media Foundation attributi](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




