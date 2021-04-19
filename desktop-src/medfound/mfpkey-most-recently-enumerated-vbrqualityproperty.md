---
description: Specifica il livello di qualità VBR del tipo di output enumerato più di recente.
ms.assetid: 7d67e41f-060b-49a1-9e17-5db081ef4210
title: Proprietà MFPKEY_MOST_RECENT_ENUMERATED_VBRQUALITY (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccd3b5f3aae6dc5347672cf6697c3431163dcbd1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332713"
---
# <a name="mfpkey_most_recent_enumerated_vbrquality-property"></a>MFPKEY \_ \_ \_ Proprietà VBRQUALITY enumerata più recente \_

Specifica il livello di qualità VBR del tipo di output enumerato più di recente. Di sola lettura.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

Disponibile solo tramite [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo di dati

**\_UI4 VT**

## <a name="remarks"></a>Commenti

Quando il codificatore funge da trasformazione Media Foundation (MFT) ed enumera un tipo di output in una chiamata a [**IMFTransform:: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype), è possibile eseguire una query su MFT per la **proprietà \_ \_ \_ \_ VBRQUALITY enumerata MFPKEY più di recente** . Il valore restituito indica la qualità VBR del tipo di supporto di output restituito più di recente. È quindi possibile usare tale valore per impostare la [**proprietà \_ \_ VBRQUALITY desiderata MFPKEY**](mfpkey-desired-vbrqualityproperty.md) del codificatore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-----------------------------------------------------------------------------------------|
| Client<br/> | Windows Vista o Windows 7<br/>                                                   |
| Intestazione<br/> | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_VBRENABLED MFPKEY**](mfpkey-vbrenabledproperty.md)
</dt> <dt>

[**MFPKEY \_ vincolato \_ VBRQUALITY enumerato \_**](mfpkey-constrain-enumerated-vbrqualityproperty.md)
</dt> <dt>

[Proprietà Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
