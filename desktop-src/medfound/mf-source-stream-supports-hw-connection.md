---
description: Indica se un'origine supporto supporta il flusso di dati hardware.
ms.assetid: 32FEBC99-0AE0-4FE9-90AB-5FB204BD4C83
title: MF_SOURCE_STREAM_SUPPORTS_HW_CONNECTION attributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 659672b11cbcaa51f543eec8239f56ba792584a4b1ac44af25ed76016cdeb2a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119955147"
---
# <a name="mf_source_stream_supports_hw_connection-attribute"></a>MF \_ SOURCE STREAM SUPPORTA \_ \_ \_ l'attributo \_ HW CONNECTION

Indica se un'origine supporto supporta il flusso di dati hardware.

## <a name="data-type"></a>Tipo di dati

**BOOL** archiviato come **UINT32**

## <a name="remarks"></a>Commenti

Questo attributo viene usato quando un'origine multimediale esegue il proxy di un dispositivo hardware ed è in grado di trasferire i dati downstream tramite un bus hardware, senza inviare dati alla CPU. Ad esempio, una webcam potrebbe distribuire video con codifica H.264 direttamente a un decodificatore hardware integrato.

In questo scenario, l'origine e il decodificatore sono [](media-sources.md) ancora rappresentati nel Microsoft Media Foundation da un oggetto di origine multimediale e da una trasformazione Media Foundation [](media-foundation-transforms.md) (MFT). Tuttavia, nessun flusso di dati tra questi due oggetti a livello di pipeline, solo a livello hardware, come illustrato nel diagramma seguente.

![diagramma che mostra un'origine proxy hardware.](images/proxy-mft3.png)

La connessione tra l'origine del supporto e MFT viene negoziata nel modo seguente.

1.  La pipeline esegue una query sull'origine multimediale per [**l'interfaccia IMFMediaSourceEx.**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex) Questa interfaccia è facoltativa per supportare le origini multimediali.
2.  La pipeline chiama [**IMFMediaSourceEx::GetStreamAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) per ottenere un [**puntatore IMFAttributes.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)
3.  La pipeline esegue query per l'attributo \_ MF SOURCE \_ STREAM \_ SUPPORTS \_ HW \_ CONNECTION. Se l'attributo è presente ed è uguale a **TRUE,** l'origine del supporto supporta le connessioni hardware.
4.  La pipeline controlla se anche MFT è un proxy hardware, controllando l'attributo [MFT \_ ENUM \_ HARDWARE URL \_ \_ Attribute](mft-enum-hardware-url-attribute.md) in MFT. Per informazioni dettagliate, vedere [MFT hardware.](hardware-mfts.md)
5.  La pipeline imposta [l'attributo \_ MFT CONNECTED \_ STREAM \_ ATTRIBUTE](mft-connected-stream-attribute.md) in MFT. Il valore di questo attributo è il [**puntatore IMFAttribute**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) ottenuto dall'origine multimediale nel passaggio 2.
6.  La pipeline imposta [l'attributo MFT \_ CONNECTED TO \_ \_ HW \_ STREAM](mft-connected-to-hw-stream.md) su **TRUE** sia nell'origine multimediale che in MFT.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 app desktop \| app UWP\]<br/>                                  |
| Server minimo supportato<br/> | \[Windows Server 2012 app desktop \| app UWP\]<br/>                        |
| Intestazione<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli Media Foundation personalizzati](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[MFT hardware](hardware-mfts.md)
</dt> </dl>

 

 




