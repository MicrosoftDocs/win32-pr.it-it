---
description: Contiene le funzioni intrinseche della fotocamera pinhole per l'esempio.
ms.assetid: AF7EA6A0-90C5-49A8-AD68-776BF770A448
title: Attributo MFSampleExtension_PinholeCameraIntrinsics (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bb9e78641c0baab0e9eda3083aafaf8fe92229f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310234"
---
# <a name="mfsampleextension_pinholecameraintrinsics-attribute"></a>\_Attributo PinholeCameraIntrinsics di MFSampleExtension

Contiene le funzioni intrinseche della fotocamera pinhole per l'esempio.

## <a name="data-type"></a>Tipo di dati

Matrice di byte

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes:: GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).

Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)SetAttribute.

## <a name="applies-to"></a>Si applica a

[**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a>Commenti

Il valore dell'attributo è un [**MFPinholeCameraIntrinsics**](/windows/desktop/api/mfapi/ns-mfapi-mfpinholecameraintrinsics).

Questo attributo è facoltativo per supportare le fotocamere non calibrate.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows 10\]<br/>                                        |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2012 R2 \[\]<br/>                            |
| Intestazione<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



 

 




