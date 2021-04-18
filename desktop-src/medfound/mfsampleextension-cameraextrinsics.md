---
description: Contiene la fotocamera estrinseca per l'esempio.
ms.assetid: C970E958-3866-491A-9806-DB300834360E
title: Attributo MFSampleExtension_CameraExtrinsics (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3340f1ab84061fa00e12fa65960f1b2902690816
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309098"
---
# <a name="mfsampleextension_cameraextrinsics-attribute"></a>\_Attributo CameraExtrinsics di MFSampleExtension

Contiene la fotocamera estrinseca per l'esempio.

## <a name="data-type"></a>Tipo di dati

Matrice di byte

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes:: GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).

Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)SetAttribute.

## <a name="applies-to"></a>Si applica a

[**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a>Commenti

Il valore dell'attributo è un [**MFCameraExtrinsics**](/windows/desktop/api/mfapi/ns-mfapi-mfcameraextrinsics).

Questo attributo è facoltativo per supportare le fotocamere non calibrate.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows 10\]<br/>                                        |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2012 R2 \[\]<br/>                            |
| Intestazione<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




