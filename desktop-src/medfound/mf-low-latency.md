---
description: Abilita l'elaborazione a bassa latenza nella pipeline Microsoft Media Foundation pipeline.
ms.assetid: 4D11B4D6-8CFF-4850-BF8F-9019A1F79153
title: MF_LOW_LATENCY attributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c51421b68e23ab3f29c15b0b360a7d189befb45cd9046176e6dcb99f1b0748f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119956451"
---
# <a name="mf_low_latency-attribute"></a>Attributo MF \_ LOW \_ LATENCY

Abilita l'elaborazione a bassa latenza nella pipeline Microsoft Media Foundation pipeline.

## <a name="data-type"></a>Tipo di dati

**BOOL** archiviato come **UINT32**

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Per impostare questo attributo, chiamare [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Commenti

La bassa latenza è definita come il ritardo minimo possibile da quando i dati multimediali vengono generati (o ricevuti) a quando viene eseguito il rendering. La bassa latenza è consigliabile per gli scenari di comunicazione in tempo reale. Per altri scenari, ad esempio la riproduzione locale o la transcoding, in genere non è consigliabile abilitare la modalità a bassa latenza, perché può influire sulla qualità.

> [!Note]  
> Il valore GUID di questo attributo è identico alla proprietà [CODECAPI \_ AVLowLatencyMode](codecapi-avlowlatencymode.md) definita per [**l'interfaccia ICodecAPI.**](/windows/win32/api/strmif/nn-strmif-icodecapi)

 

Impostare questo attributo nei componenti della pipeline come indicato di seguito:

-   Origine multimediale: usare [**il metodo IMFMediaSourceEx::GetSourceAttributes.**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getsourceattributes)
-   Media Foundation trasformazione (MFT): usare il [**metodo IMFTransform::GetAttributes.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) Per i codificatori, il codificatore potrebbe supportare una bassa latenza tramite [**l'interfaccia ICodecAPI.**](/windows/win32/api/strmif/nn-strmif-icodecapi)
-   Sink multimediale: eseguire una query sul sink multimediale per [**l'interfaccia IMFAttributes.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)

Le applicazioni in genere non impostano questo attributo direttamente nei componenti della pipeline, ma impostano invece l'attributo su uno degli oggetti seguenti:

-   [Sessione multimediale:](media-session.md)usare il *parametro pConfiguation* della funzione [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) o [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) oppure impostare l'attributo nella topologia.
-   [Lettore di](source-reader.md)origine: impostare l'attributo con le proprietà di configurazione quando si crea il lettore di origine. Per altre informazioni, vedere [Attributi del lettore di origine.](source-reader-attributes.md)
-   [Sink Writer (Writer sink):](sink-writer.md)impostare l'attributo con le proprietà di configurazione quando si crea il writer di sink. Per altre informazioni, vedere [Attributi del writer di sink.](sink-writer-attributes.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 app desktop \| app UWP\]<br/>                                  |
| Server minimo supportato<br/> | \[Windows Server 2012 app desktop \| app UWP\]<br/>                        |
| Intestazione<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli Media Foundation personalizzati](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributi del writer di sink](sink-writer-attributes.md)
</dt> <dt>

[Attributi del lettore di origine](source-reader-attributes.md)
</dt> <dt>

[Attributi di trasformazione](transform-attributes.md)
</dt> </dl>

 

 
