---
description: Contiene gli intrinseci della fotocamera pinhole per l'esempio.
ms.assetid: AF7EA6A0-90C5-49A8-AD68-776BF770A448
title: MFSampleExtension_PinholeCameraIntrinsics attributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebb26cd7931b1dfe2e17dcd1b8dfff8ee7f972f6dad066bee6879f0de12b3609
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113081"
---
# <a name="mfsampleextension_pinholecameraintrinsics-attribute"></a>Attributo MFSampleExtension \_ PinholeCameraIntrinsics

Contiene gli intrinseci della fotocamera pinhole per l'esempio.

## <a name="data-type"></a>Tipo di dati

Matrice di byte

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).

Per impostare questo attributo, chiamare [**IMFAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).

## <a name="applies-to"></a>Si applica a

[**Esempio IMF**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a>Commenti

Il valore dell'attributo è [**MFPinholeCameraIntrinsics**](/windows/desktop/api/mfapi/ns-mfapi-mfpinholecameraintrinsics).

Questo attributo è facoltativo per supportare fotocamere non calibrate.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 10 solo app desktop\]<br/>                                        |
| Server minimo supportato<br/> | Windows Server 2012 Solo app desktop R2 \[\]<br/>                            |
| Intestazione<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



 

 




