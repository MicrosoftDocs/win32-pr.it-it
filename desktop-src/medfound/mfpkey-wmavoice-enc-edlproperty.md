---
description: Specifica le parti di contenuto da codificare come musica dal codec vocale.
ms.assetid: c63034ce-33d7-4f2f-9498-fc16e25b6d4d
title: Proprietà MFPKEY_WMAVOICE_ENC_EDL (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f3ac85ebd3a0542fbcf6554205d0b2f2623957c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755306"
---
# <a name="mfpkey_wmavoice_enc_edl-property"></a>MFPKEY \_ WMAVOICE \_ enc ( \_ Proprietà EDL)

Specifica le parti di contenuto da codificare come musica dal codec vocale.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

g \_ wszWMACVoiceBuffer

## <a name="data-type"></a>Tipo di dati

\_BSTR VT

## <a name="default-value"></a>Valore predefinito

Nessun valore predefinito. Se questa proprietà non è impostata, il codec utilizzerà il valore della proprietà [MFPKEY \_ WMAVOICE \_ enc \_ MusicSpeechClassMode](mfpkey-wmavoice-enc-musicspeechclassmodeproperty.md) per determinare come codificare il contenuto.

## <a name="remarks"></a>Commenti

È possibile usare questa proprietà se la modalità automatica del codec non fornisce risultati soddisfacenti.

Questo valore è una stringa delimitata da virgole che contiene almeno quattro numeri interi. Il primo valore integer è il numero di versione; usare sempre 1 per questo valore. Il secondo Integer è il numero di sezioni che devono essere codificate come musica. Il secondo numero intero è costituito da un numero di coppie di valori che rappresentano intervalli in millisecondi, una coppia per ogni sezione di contenuto che deve essere codificata come musica.

Ad esempio, "1, 2100200500600" informa il codificatore di usare la versione 1 con due sezioni di musica. La prima sezione Music inizia a 100 ms e termina con 200 ms. La seconda sezione Music inizia a 500 ms e termina con 600 ms.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                             |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




