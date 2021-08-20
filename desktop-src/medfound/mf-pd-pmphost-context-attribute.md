---
description: Contiene un puntatore all'oggetto proxy per il descrittore di presentazione delle applicazioni.
ms.assetid: 0cd83204-0d32-417c-8911-1d3358eb0802
title: MF_PD_PMPHOST_CONTEXT attributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3bad1e033bfd3d6b87fc0dd9d5b4da89aee2eedae6b4bfc570e68dd87428dfb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117691800"
---
# <a name="mf_pd_pmphost_context-attribute"></a>Attributo MF \_ PD \_ PMPHOST \_ CONTEXT

Contiene un puntatore all'oggetto proxy per il descrittore di presentazione dell'applicazione.

## <a name="data-type"></a>Tipo di dati

**IUnknown\***

## <a name="remarks"></a>Commenti

L'host PMP (Protected Media Path) usa questo attributo per archiviare il descrittore di presentazione dell'applicazione nel descrittore di presentazione remoto. Il valore dell'attributo è un puntatore [**all'interfaccia IMFRemoteProxy.**](/windows/desktop/api/mfidl/nn-mfidl-imfremoteproxy)

La costante GUID per questo attributo viene esportata da mfuuid.lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                     |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico di Media Foundation attributi](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes::GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)
</dt> <dt>

[**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)
</dt> <dt>

[**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[Attributi del descrittore di presentazione](presentation-descriptor-attributes.md)
</dt> </dl>

 

 




