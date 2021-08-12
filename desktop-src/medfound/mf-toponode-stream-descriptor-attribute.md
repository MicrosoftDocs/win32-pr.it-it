---
description: Contiene un puntatore al descrittore di flusso per l'origine multimediale.
ms.assetid: 5acafbc1-823f-4b6d-8737-04b3a6a0cf87
title: MF_TOPONODE_STREAM_DESCRIPTOR attributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92517560f0a1f60681afc1209d6d14d3e3c5d663958d365d18b20558c0003199
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118244325"
---
# <a name="mf_toponode_stream_descriptor-attribute"></a>Attributo MF \_ TOPONODE \_ STREAM \_ DESCRIPTOR

Contiene un puntatore al descrittore di flusso per l'origine multimediale.

## <a name="data-type"></a>Tipo di dati

**IUnknown\***

## <a name="remarks"></a>Commenti

Questo attributo si applica ai nodi di origine (**MF \_ TOPOLOGY \_ SOURCESTREAM \_ NODE**).

Il valore dell'attributo è un puntatore all'interfaccia [**IMFStreamDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor) del descrittore di flusso. Questo attributo è obbligatorio.

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

[**IMFAttributes::GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)
</dt> <dt>

[**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)
</dt> <dt>

[**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[Attributi del nodo della topologia](topology-node-attributes.md)
</dt> </dl>

 

 




