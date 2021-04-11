---
description: Contiene un puntatore al descrittore di presentazione dal percorso multimediale protetto (PMP).
ms.assetid: cf12552e-0963-46fa-9a26-44dd601ab68c
title: Attributo MF_PD_APP_CONTEXT (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8971ead121407ff1a7793c16b14f6b02d3dd102e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233045"
---
# <a name="mf_pd_app_context-attribute"></a>\_Attributo di \_ contesto dell'app MF PD \_

Contiene un puntatore al descrittore di presentazione dal percorso multimediale protetto (PMP).

## <a name="data-type"></a>Tipo di dati

**IUnknown \** _

## <a name="remarks"></a>Commenti

Il proxy di origine multimediale, creato nel processo PMP, usa questo attributo per archiviare il descrittore della presentazione remota nel descrittore di presentazione dell'applicazione.

Il valore di questo attributo è un puntatore all'interfaccia [_ *IMFPresentationDescriptor* *](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) .

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

[**IMFAttributes:: getunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)
</dt> <dt>

[**IMFAttributes:: Unknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)
</dt> <dt>

[Attributi del descrittore della presentazione](presentation-descriptor-attributes.md)
</dt> </dl>

 

 




