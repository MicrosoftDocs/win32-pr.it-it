---
description: Contiene un puntatore all'oggetto proxy per il descrittore di presentazione delle applicazioni.
ms.assetid: 0cd83204-0d32-417c-8911-1d3358eb0802
title: Attributo MF_PD_PMPHOST_CONTEXT (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70e8903e438a4649ae43d7aa2072e5a5146e3126
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104401751"
---
# <a name="mf_pd_pmphost_context-attribute"></a>\_Attributo di contesto MF PD \_ PMPHOST \_

Contiene un puntatore all'oggetto proxy per il descrittore di presentazione dell'applicazione.

## <a name="data-type"></a>Tipo di dati

**IUnknown \** _

## <a name="remarks"></a>Commenti

L'host del percorso multimediale protetto (PMP) usa questo attributo per archiviare il descrittore di presentazione dell'applicazione nel descrittore della presentazione remota. Il valore dell'attributo è un puntatore all'interfaccia [_ *IMFRemoteProxy* *](/windows/desktop/api/mfidl/nn-mfidl-imfremoteproxy) .

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

[**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[Attributi del descrittore della presentazione](presentation-descriptor-attributes.md)
</dt> </dl>

 

 




