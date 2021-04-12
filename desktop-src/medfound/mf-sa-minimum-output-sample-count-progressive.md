---
description: Indica il numero minimo di campioni progressivi che la trasformazione Microsoft Media Foundation (MFT) deve consentire di oustanding in un determinato momento.
ms.assetid: C1F27F39-FADA-4644-ACD6-B02EAD9CFFE7
title: Attributo MF_SA_MINIMUM_OUTPUT_SAMPLE_COUNT_PROGRESSIVE (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b452f9fa4016705ed90a7f5b07abcaa6ff11983
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232381"
---
# <a name="mf_sa_minimum_output_sample_count_progressive-attribute"></a>\_ \_ \_ \_ \_ \_ Attributo progressivo numero minimo di output sa di MF

Indica il numero minimo di campioni progressivi che la trasformazione Microsoft Media Foundation (MFT) deve consentire di oustanding in un determinato momento.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="remarks"></a>Commenti

Questo attributo si applica solo a MFTs che usano un buffer circolare per allocare i propri esempi di output. Altri MFTs ignorano questo attributo.

Per impostare l'attributo:

1.  Chiamare [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) nel decodificatore per ottenere un puntatore [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .
2.  Chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) SetAttribute per aggiungere l'attributo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App desktop di Windows 8 app \[ \| UWP\]<br/>                                        |
| Server minimo supportato<br/> | App UWP per \[ app desktop di Windows Server 2012 \|\]<br/>                              |
| Intestazione<br/>                   | <dl> <dt>Mftransform. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




