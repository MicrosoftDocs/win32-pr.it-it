---
description: Specifica l'elemento che contiene il nodo di origine.
ms.assetid: f5fa5c10-8f30-43bd-8054-a39996f807a3
title: Attributo MF_TOPONODE_SEQUENCE_ELEMENTID (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a3cd2c66c40a0bc3776d2fd2b7d78535cf24b6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308439"
---
# <a name="mf_toponode_sequence_elementid-attribute"></a>\_ \_ Attributo ElementID della sequenza MF TOPONODE \_

Specifica l'elemento che contiene il nodo di origine.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="remarks"></a>Commenti

Questo attributo si applica ai nodi di origine (**\_ \_ \_ nodo SOURCESTREAM topologia MF**).

La pipeline multimediale usa questo attributo per individuare quando le origini multimediali fanno parte dello stesso elemento. La pipeline considera tutti i nodi di origine che fanno parte dello stesso elemento che hanno lo stesso clock.

Quando la pipeline Accoda una nuova topologia che contiene nodi di origine che fanno parte di un elemento presente nella topologia precedente, la pipeline considera questi nodi di origine come aventi lo stesso clock dei nodi di origine di tale elemento nella topologia precedente.

> [!Note]  
> La pipeline multimediale non corregge i timestamp per i nodi di origine con frequenze di clock diverse.

 

Un'origine multimediale che può fornire topologie deve implementare l'interfaccia [**IMFMediaSourceTopologyProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider) o l'interfaccia [**IMFSequencerSource**](/windows/desktop/api/mfidl/nn-mfidl-imfsequencersource) . Un'origine multimediale che fornisce topologie deve impostare l' **attributo \_ \_ \_ ElementID della sequenza MF TOPONODE** in ogni nodo di origine creato.

La costante GUID per questo attributo viene esportata da mfuuid. lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                     |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes:: seuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFMediaSourceTopologyProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider)
</dt> <dt>

[**IMFSequencerSource**](/windows/desktop/api/mfidl/nn-mfidl-imfsequencersource)
</dt> <dt>

[**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[Attributi del nodo della topologia](topology-node-attributes.md)
</dt> <dt>

[Origine sequencer](sequencer-source.md)
</dt> </dl>

 

 




