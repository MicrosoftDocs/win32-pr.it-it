---
description: Consente al motore di acquisizione di usare un codificatore con restrizioni sul campo di utilizzo.
ms.assetid: 28421875-9629-4F14-8159-2D86012F517F
title: MF_CAPTURE_ENGINE_ENCODER_MFT_FIELDOFUSE_UNLOCK_Attribute attributo (Mfcaptureengine.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32f2fb9d85c68adbc726fa4b36f2ea960a33e68c4dff836fac0370c8e9e4e3a1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060821"
---
# <a name="mf_capture_engine_encoder_mft_fieldofuse_unlock_attribute-attribute"></a>Attributo MF \_ CAPTURE \_ ENGINE ENCODER \_ \_ MFT \_ FIELDOFUSE \_ UNLOCK \_

Consente al motore di acquisizione di usare un codificatore con restrizioni sul campo di utilizzo.

## <a name="data-type"></a>Tipo di dati

**IUnknown\***

## <a name="remarks"></a>Commenti

Il valore di questo attributo è un puntatore [**all'interfaccia IMFFieldOfUseMFTUnlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) implementata dal chiamante. L'implementazione del chiamante di questa interfaccia deve eseguire un handshake con il codificatore, come descritto in [Field of Use Restrictions](field-of-use-restrictions.md). Microsoft Media Foundation definisce l'handshake, in genere comporterebbe uno scambio crittografico.

Internamente, il motore di acquisizione imposta il puntatore [**IMFFieldOfUseMFTUnlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) sul codificatore impostando l'attributo [MFT \_ FIELDOFUSE \_ UNLOCK \_ del](mft-fieldofuse-unlock-attribute.md) codificatore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                                   |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                         |
| Intestazione<br/>                   | <dl> <dt>Mfcaptureengine.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli Media Foundation personalizzati](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributi del motore di acquisizione](capture-engine-attributes.md)
</dt> <dt>

[**IMFCaptureEngine::Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




