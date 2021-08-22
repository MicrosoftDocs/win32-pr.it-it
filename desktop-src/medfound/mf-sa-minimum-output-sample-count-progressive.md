---
description: Indica il numero minimo di campioni progressivi che la trasformazione Microsoft Media Foundation (MFT) deve consentire in qualsiasi momento.
ms.assetid: C1F27F39-FADA-4644-ACD6-B02EAD9CFFE7
title: MF_SA_MINIMUM_OUTPUT_SAMPLE_COUNT_PROGRESSIVE attributo (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48df5262e225b8768d3251f9768cf2156ee2acacb19ca70752ae5bf989b682ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119955431"
---
# <a name="mf_sa_minimum_output_sample_count_progressive-attribute"></a>Attributo MF \_ SA MINIMUM OUTPUT SAMPLE COUNT \_ \_ \_ \_ \_ PROGRESSIVE

Indica il numero minimo di campioni progressivi che la trasformazione Microsoft Media Foundation (MFT) deve consentire in qualsiasi momento.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="remarks"></a>Commenti

Questo attributo si applica solo alle MFT che usano un buffer circolare per allocare i propri campioni di output. Altri MFT ignorano questo attributo.

Per impostare questo attributo:

1.  Chiamare [**IMFTransform::GetAttributes sul**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) decodificatore per ottenere un [**puntatore IMFAttributes.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)
2.  Chiamare [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) per aggiungere l'attributo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 app desktop \| app UWP\]<br/>                                        |
| Server minimo supportato<br/> | \[Windows Server 2012 app desktop \| app UWP\]<br/>                              |
| Intestazione<br/>                   | <dl> <dt>Mftransform.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico di Media Foundation attributi](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




