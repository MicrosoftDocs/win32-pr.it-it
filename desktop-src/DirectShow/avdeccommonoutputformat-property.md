---
description: Specifica il formato di output per il decodificatore.
ms.assetid: fdccdbfa-2814-4d21-9a7f-4121b79718e6
title: Proprietà AVDecCommonOutputFormat (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 129f9a1171c5870eab243108fc0ed6992be4993b886cbd36d72fe91988f321b5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119586751"
---
# <a name="avdeccommonoutputformat-property"></a>AVDecCommonOutputFormat - proprietà

Specifica il formato di output per il decodificatore.

Si tratta di una proprietà di lettura/scrittura.

## <a name="data-type"></a>Tipo di dati

**BSTR** (**VT \_ BSTR**)

## <a name="property-guid"></a>GUID proprietà

**CODECAPI \_ AVDecCommonOutputFormat**

## <a name="property-value"></a>Valore proprietà



| GUID                                                               | Descrizione                                                                                                                                                                                                         |
|--------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CODECAPI \_ GUID \_ AVDecAudioOutputFormat \_ PCM                        | Audio PCM, con un numero qualsiasi di canali                                                                                                                                                                             |
| GUID CODECAPI \_ \_ AVDecAudioOutputFormat \_ \_ Cuffia PCM            | Audio PCM stereo, con downmix solo a sinistra/solo a destra (Lo/Ro)                                                                                                                                                        |
| CODECAPI \_ GUID \_ AVDecAudioOutputFormat \_ PCM \_ Stereo \_ Auto          | Audio PCM stereo, usando la selezione automatica della modalità downmix stereo (Lo/Ro o Lt/Rt). È possibile usare questo valore per i formati audio in cui il flusso di input definisce la modalità downmix preferita, ad esempio Dolby AC-3. |
| CODECAPI \_ GUID \_ AVDecAudioOutputFormat \_ PCM \_ Stereo \_ MatrixEncoded | Audio PCM stereo, con downmix stereo con codifica matrice (Lt/Rt)                                                                                                                                                       |
| CODECAPI \_ GUID \_ AVDecAudioOutputFormat \_ SPDIF \_ Bitstream           | Flusso di bit compresso S/PDIF (Formato dell'interfaccia digitale di Sony/Philips), come definito da IEC-60958                                                                                                                        |
| CODECAPI \_ GUID \_ AVDecAudioOutputFormat \_ SPDIF \_ PCM                 | S/PDIF PCM stereo, come definito da IEC-60958                                                                                                                                                                          |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional app \[ desktop \| app UWP\]<br/>                     |
| Server minimo supportato<br/> | Windows 2000 App desktop UWP per le app \[ desktop di 2000 \| Server\]<br/>                           |
| Intestazione<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà API codec](codec-api-properties.md)
</dt> <dt>

[**Interfaccia ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




