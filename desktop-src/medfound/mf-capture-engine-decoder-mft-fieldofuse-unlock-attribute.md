---
description: Consente al motore di acquisizione di utilizzare un decodificatore con restrizioni per il campo di utilizzo.
ms.assetid: EDE6D207-FD84-4DEB-9BF5-0952C454B00F
title: Attributo MF_CAPTURE_ENGINE_DECODER_MFT_FIELDOFUSE_UNLOCK_Attribute (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d858d4382b669621f6dc43cbfee77b62e9d1124
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309585"
---
# <a name="mf_capture_engine_decoder_mft_fieldofuse_unlock_attribute-attribute"></a>\_Attributo di \_ sblocco \_ dell' \_ \_ attributo di \_ sblocco \_ FIELDOFUSE del motore di acquisizione MF

Consente al motore di acquisizione di utilizzare un decodificatore con restrizioni per il campo di utilizzo.

## <a name="data-type"></a>Tipo di dati

**IUnknown \** _

## <a name="remarks"></a>Commenti

Il valore di questo attributo è un puntatore all'interfaccia [_ *IMFFieldOfUseMFTUnlock* *](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) , implementata dal chiamante. L'implementazione del chiamante di questa interfaccia è prevista per eseguire un handshake con il decodificatore, come descritto in [campo delle restrizioni di utilizzo](field-of-use-restrictions.md). Microsoft Media Foundation non definisce l'handshake, in genere comporta una sorta di scambio crittografico.

Internamente, il motore di acquisizione imposta il puntatore [**IMFFieldOfUseMFTUnlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) sul decodificatore impostando l'attributo di [sblocco dell' \_ \_ \_ attributo MFT FIELDOFUSE](mft-fieldofuse-unlock-attribute.md) del decodificatore.

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

 

 




