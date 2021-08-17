---
description: Specifica il livello di qualità VBR del tipo di output enumerato più di recente.
ms.assetid: 7d67e41f-060b-49a1-9e17-5db081ef4210
title: MFPKEY_MOST_RECENT_ENUMERATED_VBRQUALITY proprietà (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68e609f8dc7b95eb9cfd4bf537af47d1a11cb4ba625f0bbc65897b008ff03a31
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117689795"
---
# <a name="mfpkey_most_recent_enumerated_vbrquality-property"></a>Proprietà \_ \_ \_ VBRQUALITY ENUMERATA MFPKEY \_ PIÙ RECENTE

Specifica il livello di qualità VBR del tipo di output enumerato più di recente. Di sola lettura.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

Disponibile solo tramite [**IPropertyStore.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

## <a name="data-type"></a>Tipo di dati

**VT \_ UI4**

## <a name="remarks"></a>Commenti

Quando il codificatore funge da Media Foundation Transform (MFT) e enumera un tipo di output in una chiamata a [**IMFTransform::GetOutputAvailableType,**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype)è possibile eseguire una query sul MFT per la proprietà **MFPKEY \_ MOST RECENTLY \_ \_ ENUMERATED \_ VBRQUALITY.** Il valore restituito indica la qualità VBR del tipo di supporto di output restituito più di recente. È quindi possibile usare tale valore per impostare la [**proprietà MFPKEY \_ DESIRED \_ VBRQUALITY**](mfpkey-desired-vbrqualityproperty.md) del codificatore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-----------------------------------------------------------------------------------------|
| Client<br/> | Windows Vista o Windows 7<br/>                                                   |
| Intestazione<br/> | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md)
</dt> <dt>

[**MFPKEY \_ VINCOLA \_ \_ VBRQUALITY ENUMERATA**](mfpkey-constrain-enumerated-vbrqualityproperty.md)
</dt> <dt>

[Media Foundation proprietà](media-foundation-properties.md)
</dt> </dl>

 

 
