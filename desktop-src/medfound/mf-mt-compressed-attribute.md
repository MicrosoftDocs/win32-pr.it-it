---
description: Specifica se i dati multimediali sono compressi per un tipo di supporto.
ms.assetid: b44fb757-4390-4392-b1cb-37772b4ae3fb
title: Attributo MF_MT_COMPRESSED (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d049795f09845b5d32daf29ef033ab2e4b23007f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528237"
---
# <a name="mf_mt_compressed-attribute"></a>\_ \_ Attributo compresso MF mt

Specifica se i dati multimediali sono compressi per un tipo di supporto.

## <a name="data-type"></a>Tipo di dati

**UINT32**

Considera come valore booleano.

## <a name="remarks"></a>Commenti

Se questo attributo è **true**, il tipo di supporto è un formato compresso. In caso contrario, il tipo di supporto non è compresso o il tipo di compressione non è noto.

Non è garantito che l'attributo sia impostato su **true** per tutti i formati compressi, quindi le applicazioni in genere non si basano su questo attributo. Il modo più affidabile per determinare se un formato è compresso consiste nel mantenere un elenco di formati noti. Se un'applicazione non riconosce un formato, come specificato nell'attributo del [**\_ \_ sottotipo MF mt**](mf-mt-subtype-attribute.md) , non dovrebbe presupporre nulla sulla compressione del formato.

Per determinare se un formato usa la compressione temporale (ad esempio, alcuni esempi vengono calcolati come Delta degli esempi precedenti), controllare l'attributo [**indipendente da tutti i campioni di MF \_ mt \_ All \_ \_**](mf-mt-all-samples-independent-attribute.md) .

La costante GUID per questo attributo viene esportata da mfuuid. lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App desktop di Windows Vista app \[ \| UWP\]<br/>                              |
| Server minimo supportato<br/> | App UWP per \[ app desktop di Windows Server 2008 \|\]<br/>                        |
| Intestazione<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes:: seuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Attributi del tipo di supporto](media-type-attributes.md)
</dt> </dl>

 

 




