---
description: Specifica il formato di output per il decodificatore.
ms.assetid: fdccdbfa-2814-4d21-9a7f-4121b79718e6
title: Proprietà AVDecCommonOutputFormat (codecapis. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b69c536b3c9f1bf75e2a5741d0cdd16569b3dd8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522481"
---
# <a name="avdeccommonoutputformat-property"></a>Proprietà AVDecCommonOutputFormat

Specifica il formato di output per il decodificatore.

Si tratta di una proprietà di lettura/scrittura.

## <a name="data-type"></a>Tipo di dati

**BSTR** (**VT \_ BSTR**)

## <a name="property-guid"></a>GUID proprietà

**Codecapis \_ AVDecCommonOutputFormat**

## <a name="property-value"></a>Valore proprietà



| GUID                                                               | Descrizione                                                                                                                                                                                                         |
|--------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AVDecAudioOutputFormat GUID codecapis \_ \_ \_ PCM                        | Audio PCM, usando un numero qualsiasi di canali                                                                                                                                                                             |
| \_ \_ Cuffie AVDecAudioOutputFormat GUID \_ \_ di codecapi            | Audio PCM stereo, usando solo a sinistra/a destra (lo/ro) downmix                                                                                                                                                        |
| Codecapis \_ GUID \_ AVDecAudioOutputFormat \_ PCM \_ stereo \_ auto          | Audio PCM stereo, usando la selezione automatica della modalità downmix stereo (lo/ro o LT/RT). È possibile usare questo valore per formati audio in cui il flusso di input definisce la modalità downmix preferita, ad esempio Dolby AC-3. |
| Codecapis \_ GUID \_ AVDecAudioOutputFormat \_ PCM \_ stereo \_ MatrixEncoded | Audio PCM stereo, uso di downmix stereo con codifica Matrix (LT/RT)                                                                                                                                                       |
| \_ \_ Bitstream GUID AVDecAudioOutputFormat \_ SPDIF \_           | Bitstream compresso S/PDIF (Sony/Philips Digital Interface Format), come definito da IEC-60958                                                                                                                        |
| Codecapis \_ GUID \_ AVDecAudioOutputFormat \_ SPDIF \_ PCM                 | Stereo PCM S/PDIF, come definito da IEC-60958                                                                                                                                                                          |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App UWP di Windows 2000 Professional \[ desktop apps \|\]<br/>                     |
| Server minimo supportato<br/> | App desktop di Windows 2000 Server \[ \| UWP\]<br/>                           |
| Intestazione<br/>                   | <dl> <dt>Codecapis. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà dell'API codec](codec-api-properties.md)
</dt> <dt>

[**Interfaccia ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




