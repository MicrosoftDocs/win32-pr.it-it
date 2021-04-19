---
description: Specifica se IMFTransform vuole ricevere notifiche di completamento MEPolicySet.
title: MFT_POLICY_SET_AWARE (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2effa9eab2b0b126c2849d39ce7ffe3f62d81e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310211"
---
# <a name="mft_policy_set_aware-attribute"></a>\_ \_ Attributo Aware del set di criteri MFT \_

Se diverso da zero, indica che **IMFTransform** desidera ricevere notifiche di completamento [MEPolicySet](./mepolicyset.md) .

## <a name="data-type"></a>Tipo di dati

**UInt32** (considerato **bool**)

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/win32/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/win32/api/mfobjects/nf-mfobjects-imfattributes-setuint32)SetAttribute.

## <a name="applies-to"></a>Si applica a

[**IMFInputTrustAuthority**](/windows/win32/api/mfidl/nn-mfidl-imfinputtrustauthority)

## <a name="remarks"></a>Commenti

Questo attributo può essere usato da un **IMFInputTrustAuthority** Decrypter. Un'implementazione di un modulo di decrittografia del contenuto (CDM) può includere un'implementazione di **IMFInputTrustAuthority**. È possibile accedere all'oggetto **IMFInputTrustAuthority** tramite [IMFContentDecryptionModule:: CreateTrustedInput](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmodule-createtrustedinput).


La costante GUID per questo attributo viene esportata da mfuuid. lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Aggiornamento di Windows 10 aprile 2020   <br/>                                        |
| Intestazione<br/>                   | <dl> <dt>Mftransform. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt>  <dt>

[Attributi di trasformazione](transform-attributes.md)
</dt> </dl>

 

 
