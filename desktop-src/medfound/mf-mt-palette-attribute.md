---
description: Contiene le voci della tavolozza per un tipo di supporto video. Usare questo attributo per i formati video svasati, ad esempio RGB 8.
ms.assetid: 3efc124b-073e-4c48-9550-c100e29f2d6f
title: MF_MT_PALETTE attributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a20623262be0129cabf5675fd4cd1a37ec2fb61b6b9a0dd5e135fa9e48e1abb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118741656"
---
# <a name="mf_mt_palette-attribute"></a>Attributo MF \_ MT \_ PALETTE

Contiene le voci della tavolozza per un tipo di supporto video. Usare questo attributo per i formati video svasati, ad esempio RGB 8.

## <a name="data-type"></a>Tipo di dati

Matrice di byte

## <a name="remarks"></a>Commenti

I dati dell'attributo sono una matrice [**di unioni MFPaletteEntry.**](/windows/win32/api/mfobjects/ns-mfobjects-mfpaletteentry)

La costante GUID per questo attributo viene esportata da mfuuid.lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows App desktop vista \[ \| app UWP\]<br/>                              |
| Server minimo supportato<br/> | Windows App desktop di Server 2008 \[ \| app UWP\]<br/>                        |
| Intestazione<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli Media Foundation personalizzati](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**IMFAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Attributi del tipo di supporto](media-type-attributes.md)
</dt> </dl>

 

 




