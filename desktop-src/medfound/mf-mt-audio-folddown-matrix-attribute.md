---
description: Specifica il modo in cui un decodificatore audio deve trasformare l'audio multicanale nell'output stereo. Questo processo viene anche definito riduzioni.
ms.assetid: 6dfe2b97-1ebc-4954-b478-85b3bbba89e3
title: Attributo MF_MT_AUDIO_FOLDDOWN_MATRIX (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10bb8aa00835ab31f6c05eaa9a1d0e5d9d126b41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309554"
---
# <a name="mf_mt_audio_folddown_matrix-attribute"></a>\_ \_ \_ Attributo Matrix FOLDDOWN audio MF mt \_

Specifica il modo in cui un decodificatore audio deve trasformare l'audio multicanale nell'output stereo. Questo processo viene anche definito *riduzioni*.

## <a name="data-type"></a>Tipo di dati

Matrice di byte

## <a name="remarks"></a>Commenti

Questo attributo si applica ai tipi di supporti audio.

Il valore di questo attributo è una struttura della [**\_ matrice MFFOLDDOWN**](/windows/desktop/api/mfapi/ns-mfapi-mffolddown_matrix) .

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

[**IMFAttributes:: GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**IMFAttributes:: seblob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Attributi del tipo di supporto](media-type-attributes.md)
</dt> </dl>

 

 




