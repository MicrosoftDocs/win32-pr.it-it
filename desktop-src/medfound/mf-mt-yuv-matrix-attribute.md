---
description: Per i tipi di supporti YUV, definisce la matrice di conversione dallo spazio colori YCbCr allo spazio colori RGB.
ms.assetid: b268d16d-b4cc-4026-9ba7-805cc5409b95
title: MF_MT_YUV_MATRIX attributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20f055490873bf1af07b8278c249679da53bc24b1a76be7a0384a010edff81c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117876505"
---
# <a name="mf_mt_yuv_matrix-attribute"></a>Attributo \_ MF MT \_ YUV \_ MATRIX

Per i tipi di supporti YUV, definisce la matrice di conversione dallo spazio colori Y'Cb'Cr' allo spazio colore R'G'B'.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="remarks"></a>Commenti

Il valore di questo attributo è un membro [**dell'enumerazione MFVideoTransferMatrix.**](/windows/desktop/api/mfobjects/ne-mfobjects-mfvideotransfermatrix)

La costante GUID per questo attributo viene esportata da mfuuid.lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows App desktop Di Vista \[ \| app UWP\]<br/>                              |
| Server minimo supportato<br/> | Windows App UWP per app desktop server 2008 \[ \|\]<br/>                        |
| Intestazione<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico di Media Foundation attributi](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Attributi del tipo di supporto](media-type-attributes.md)
</dt> <dt>

[Informazioni estese sui colori](extended-color-information.md)
</dt> </dl>

 

 




