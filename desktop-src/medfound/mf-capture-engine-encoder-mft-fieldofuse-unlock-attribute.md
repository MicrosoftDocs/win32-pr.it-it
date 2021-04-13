---
description: Consente al motore di acquisizione di usare un codificatore con restrizioni di campo per l'utilizzo.
ms.assetid: 28421875-9629-4F14-8159-2D86012F517F
title: Attributo MF_CAPTURE_ENGINE_ENCODER_MFT_FIELDOFUSE_UNLOCK_Attribute (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b29a9466162ff5551ee155343800d938276823ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226650"
---
# <a name="mf_capture_engine_encoder_mft_fieldofuse_unlock_attribute-attribute"></a>\_Attributo dell' \_ \_ \_ \_ \_ \_ attributo Unlock del codificatore MFT FIELDOFUSE di MF Capture Engine

Consente al motore di acquisizione di usare un codificatore con restrizioni di campo per l'utilizzo.

## <a name="data-type"></a>Tipo di dati

**IUnknown \** _

## <a name="remarks"></a>Commenti

Il valore di questo attributo è un puntatore all'interfaccia [_ *IMFFieldOfUseMFTUnlock* *](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) , implementata dal chiamante. L'implementazione del chiamante di questa interfaccia è prevista per l'esecuzione di un handshake con il codificatore, come descritto in [campo delle restrizioni di utilizzo](field-of-use-restrictions.md). Microsoft Media Foundation non definisce l'handshake, in genere comporta una sorta di scambio crittografico.

Internamente, il motore di acquisizione imposta il puntatore [**IMFFieldOfUseMFTUnlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) sul codificatore impostando l'attributo di [sblocco dell' \_ \_ \_ attributo MFT FIELDOFUSE](mft-fieldofuse-unlock-attribute.md) del codificatore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                                   |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                         |
| Intestazione<br/>                   | <dl> <dt>Mfcaptureengine. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributi del motore di acquisizione](capture-engine-attributes.md)
</dt> <dt>

[**IMFCaptureEngine:: Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




