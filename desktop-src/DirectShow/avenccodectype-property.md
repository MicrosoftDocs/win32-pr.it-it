---
description: Specifica lo schema di codifica.
ms.assetid: a26951d6-67fb-43fb-849f-331416e9d7c2
title: Proprietà AVEncCodecType (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3727ff8cc2a59208d63874de173e3e44e89e3e6f2ebc37201218f9656aa09cd4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084611"
---
# <a name="avenccodectype-property"></a>AVEncCodecType - proprietà

Specifica lo schema di codifica.

Si tratta di una proprietà di lettura/scrittura.

## <a name="data-type"></a>Tipo di dati

**BSTR** (**VT \_ BSTR**)

## <a name="property-guid"></a>GUID proprietà

**CODECAPI \_ AVEncCodecType**

## <a name="property-value"></a>Valore proprietà

Il valore di questa proprietà è un **BSTR che** contiene la rappresentazione di stringa di un GUID. Vengono definiti i GUID seguenti.



| GUID                                      | Descrizione                                        |
|-------------------------------------------|----------------------------------------------------|
| CODECAPI \_ GUID \_ AVEncDolbyDigitalConsumer | Dolby Digital Consumer audio                       |
| CODECAPI \_ GUID \_ AVEncDolbyDigitalPlus     | Audio Dolby Digital Plus                           |
| CODECAPI \_ GUID \_ AVEncDolbyDigitalPro      | Dolby Digital Pro audio                            |
| CODECAPI \_ GUID \_ AVEncDTS                  | Audio DTS                                          |
| CODECAPI \_ GUID \_ AVEncDTSHD                | Audio DTS-HD                                       |
| CODECAPI \_ GUID \_ AVEncDV                   | Video DV                                           |
| CODECAPI \_ GUID \_ AVEncH264Video            | Video H.264                                        |
| CODECAPI \_ GUID \_ AVEncMLP                  | Audio meridian Lossless Packing (MLP)              |
| CODECAPI \_ GUID \_ AVEncMPEG1Audio           | Audio MPEG-1                                       |
| CODECAPI \_ GUID \_ AVEncMPEG1Video           | Video MPEG-1                                       |
| CODECAPI \_ GUID \_ AVEncMPEG2Audio           | Audio MPEG-2                                       |
| CODECAPI \_ GUID \_ AVEncMPEG2Video           | Video MPEG-2                                       |
| CODECAPI \_ GUID \_ AVEncPCM                  | Audio PCM                                          |
| CODECAPI \_ GUID \_ AVEncSDDS                 | Audio SDDS (Dynamic Digital Sound) di Digital Sound (SDDS)            |
| CODECAPI \_ GUID \_ AVEncWMALossless          | Windows Audio senza perdita di dati audio 9 multimediale               |
| CODECAPI \_ GUID \_ AVEncWMAPro               | Windows Audio audio Professional (WMA Pro) |
| CODECAPI \_ GUID \_ AVEncWMAVoice             | Windows Audio audio 9 voce multimediale                  |
| CODECAPI \_ GUID \_ AVEncWMV                  | Windows Video multimediale                                |
| CODECAPI \_ GUID \_ AVEndMPEG4Video           | Video MPEG-4                                       |



 

## <a name="remarks"></a>Commenti

Le applicazioni possono impostare questa proprietà per specificare lo schema di codifica da usare. I codec possono anche restituire questa proprietà come funzionalità.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[ app desktop \| UWP\]<br/>                     |
| Server minimo supportato<br/> | app \[ desktop UWP di Windows 2000 Server \|\]<br/>                           |
| Intestazione<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà dell'API Codec](codec-api-properties.md)
</dt> <dt>

[**Interfaccia ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




