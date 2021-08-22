---
description: Specifica il numero massimo di campioni di output che una trasformazione Microsoft Media Foundation (MFT) sarà in sospeso nella pipeline in qualsiasi momento.
ms.assetid: 53D393B4-BFF1-430F-9CD1-5071336E6F04
title: MF_SA_MINIMUM_OUTPUT_SAMPLE_COUNT attributo (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79a7d00fcb5a11d756ed4848e3e600a6fd1cca32203ff7234cb01963dfcb5149
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119663911"
---
# <a name="mf_sa_minimum_output_sample_count-attribute"></a>Attributo MF \_ SA MINIMUM OUTPUT SAMPLE \_ \_ \_ \_ COUNT

Specifica il numero massimo di campioni di output che una trasformazione Microsoft Media Foundation (MFT) sarà in sospeso nella pipeline in qualsiasi momento.

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
</dt> <dt>

[Attributi di trasformazione](transform-attributes.md)
</dt> </dl>

 

 




