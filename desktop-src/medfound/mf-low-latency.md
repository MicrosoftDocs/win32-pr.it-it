---
description: Abilita l'elaborazione a bassa latenza nella pipeline Microsoft Media Foundation.
ms.assetid: 4D11B4D6-8CFF-4850-BF8F-9019A1F79153
title: Attributo MF_LOW_LATENCY (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02d1b0a89452256f01fc893ced7dc191fd064bbe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757865"
---
# <a name="mf_low_latency-attribute"></a>\_Attributo MF low \_ latence

Abilita l'elaborazione a bassa latenza nella pipeline Microsoft Media Foundation.

## <a name="data-type"></a>Tipo di dati

**Bool** archiviato come **UInt32**

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)SetAttribute.

## <a name="remarks"></a>Commenti

La bassa latenza è definita come il minimo possibile ritardo da quando i dati multimediali vengono generati (o ricevuti) a quando viene eseguito il rendering. Per gli scenari di comunicazione in tempo reale è consigliabile una bassa latenza. Per altri scenari, ad esempio la riproduzione o la transcodifica locale, in genere non è consigliabile abilitare la modalità a bassa latenza, in quanto può influire sulla qualità.

> [!Note]  
> Il valore GUID di questo attributo è identico alla proprietà [ \_ AVLowLatencyMode di codecapis](codecapi-avlowlatencymode.md) definita per l'interfaccia [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) .

 

Impostare questo attributo sui componenti della pipeline come indicato di seguito:

-   Origine supporto: usare il metodo [**IMFMediaSourceEx:: GetSourceAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getsourceattributes) .
-   Trasformazione Media Foundation (MFT): usare il metodo [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) . Per i codificatori, il codificatore potrebbe supportare una bassa latenza tramite l'interfaccia [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) .
-   Sink multimediale: eseguire una query sul sink multimediale per l'interfaccia [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .

Le applicazioni in genere non impostano questo attributo direttamente sui componenti della pipeline, ma impostano invece l'attributo su uno degli oggetti seguenti:

-   [Sessione multimediale](media-session.md): utilizzare il parametro *PConfiguation* della funzione [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) o [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) oppure impostare l'attributo sulla topologia.
-   [Lettore di origine](source-reader.md): impostare l'attributo con le proprietà di configurazione quando si crea il lettore di origine. Per altre informazioni, vedere [attributi del lettore di origine](source-reader-attributes.md).
-   [Sink writer](sink-writer.md): impostare l'attributo con le proprietà di configurazione quando si crea il writer del sink. Per altre informazioni, vedere [sink writer Attributes](sink-writer-attributes.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App desktop di Windows 8 app \[ \| UWP\]<br/>                                  |
| Server minimo supportato<br/> | App UWP per \[ app desktop di Windows Server 2012 \|\]<br/>                        |
| Intestazione<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributi del writer di sink](sink-writer-attributes.md)
</dt> <dt>

[Attributi lettore di origine](source-reader-attributes.md)
</dt> <dt>

[Attributi di trasformazione](transform-attributes.md)
</dt> </dl>

 

 
