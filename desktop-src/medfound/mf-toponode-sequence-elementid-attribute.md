---
description: Specifica l'elemento che contiene questo nodo di origine.
ms.assetid: f5fa5c10-8f30-43bd-8054-a39996f807a3
title: MF_TOPONODE_SEQUENCE_ELEMENTID attributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e00af7212013d26c51ecdf7d2ea4a22855f9b52524c5188d3514d34b5d6976b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118739936"
---
# <a name="mf_toponode_sequence_elementid-attribute"></a>Attributo MF \_ TOPONODE \_ SEQUENCE \_ ELEMENTID

Specifica l'elemento che contiene questo nodo di origine.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="remarks"></a>Commenti

Questo attributo si applica ai nodi di origine (**MF \_ TOPOLOGY \_ SOURCESTREAM \_ NODE**).

La pipeline multimediale usa questo attributo per individuare quando le origini multimediali fanno parte dello stesso elemento. La pipeline considera tutti i nodi di origine che fanno parte dello stesso elemento con lo stesso clock.

Quando la pipeline accoda una nuova topologia che contiene nodi di origine che fanno parte di un elemento presente nella topologia precedente, la pipeline considera questi nodi di origine come con lo stesso clock dei nodi di origine di tale elemento nella topologia precedente.

> [!Note]  
> La pipeline multimediale non corregge i timestamp per i nodi di origine con frequenze di clock diverse.

 

Un'origine multimediale che può fornire topologie deve implementare [**l'interfaccia IMFMediaSourceTopologyProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider) o [**L'interfaccia IMFSequencerSource.**](/windows/desktop/api/mfidl/nn-mfidl-imfsequencersource) Un'origine multimediale che fornisce topologie deve impostare l'attributo **MF \_ TOPONODE \_ SEQUENCE \_ ELEMENTID** in ogni nodo di origine creato.

La costante GUID per questo attributo viene esportata da mfuuid.lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                     |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli Media Foundation personalizzati](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFMediaSourceTopologyProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider)
</dt> <dt>

[**IMFSequencerSource**](/windows/desktop/api/mfidl/nn-mfidl-imfsequencersource)
</dt> <dt>

[**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[Attributi del nodo della topologia](topology-node-attributes.md)
</dt> <dt>

[Origine Sequencer](sequencer-source.md)
</dt> </dl>

 

 




