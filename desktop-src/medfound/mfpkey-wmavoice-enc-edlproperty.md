---
description: Specifica le parti di contenuto da codificare come musica dal codec vocale.
ms.assetid: c63034ce-33d7-4f2f-9498-fc16e25b6d4d
title: MFPKEY_WMAVOICE_ENC_EDL proprietà (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ffc9f68c7122897c9f5032e9ac0e4fc93c596b5ce65f18d44fb6af6dff2dd2d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119713721"
---
# <a name="mfpkey_wmavoice_enc_edl-property"></a>Proprietà \_ EDL MFPKEY WMAVOICE \_ \_ ENC

Specifica le parti di contenuto da codificare come musica dal codec vocale.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

g \_ wszWMACVoiceBuffer

## <a name="data-type"></a>Tipo di dati

VT \_ BSTR

## <a name="default-value"></a>Valore predefinito

Nessun valore predefinito. Se questa proprietà non è impostata, il codec userà il valore della proprietà [MFPKEY \_ WMAVOICE \_ ENC \_ MusicSpeechClassMode](mfpkey-wmavoice-enc-musicspeechclassmodeproperty.md) per determinare come codificare il contenuto.

## <a name="remarks"></a>Commenti

È possibile usare questa proprietà se la modalità automatica del codec non restituisce risultati soddisfacenti.

Questo valore è una stringa delimitata da virgole contenente almeno quattro numeri interi. Il primo numero intero è il numero di versione. usare sempre 1 per questo valore. Il secondo numero intero è il numero di sezioni che devono essere codificate come musica. Dopo il secondo numero intero sono presenti diverse coppie di valori che rappresentano intervalli in millisecondi, una coppia per ogni sezione di contenuto che deve essere codificata come musica.

Ad esempio, "1,2,100,200,500,600" indica al codificatore di usare la versione 1 con 2 sezioni di musica. La prima sezione musica inizia a 100 ms e termina a 200 ms. La seconda sezione musica inizia a 500 ms e termina a 600 ms.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                             |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Media Foundation proprietà](media-foundation-properties.md)
</dt> </dl>

 

 




