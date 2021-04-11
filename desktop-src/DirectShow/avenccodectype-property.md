---
description: Specifica lo schema di codifica.
ms.assetid: a26951d6-67fb-43fb-849f-331416e9d7c2
title: Proprietà AVEncCodecType (codecapis. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8643c0624b7d82381e2008f2adbd6804e9af9881
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104341996"
---
# <a name="avenccodectype-property"></a>Proprietà AVEncCodecType

Specifica lo schema di codifica.

Si tratta di una proprietà di lettura/scrittura.

## <a name="data-type"></a>Tipo di dati

**BSTR** (**VT \_ BSTR**)

## <a name="property-guid"></a>GUID proprietà

**Codecapis \_ AVEncCodecType**

## <a name="property-value"></a>Valore proprietà

Il valore di questa proprietà è un **BSTR** che contiene la rappresentazione di stringa di un GUID. Sono definiti i seguenti GUID.



| GUID                                      | Descrizione                                        |
|-------------------------------------------|----------------------------------------------------|
| \_GUID AVEncDolbyDigitalConsumer di CODEcapi \_ | Audio Dolby Digital Consumer                       |
| \_GUID AVEncDolbyDigitalPlus di CODEcapi \_     | Audio Dolby Digital Plus                           |
| \_GUID AVEncDolbyDigitalPro di CODEcapi \_      | Audio Dolby Digital Pro                            |
| \_GUID AVEncDTS di CODEcapi \_                  | Audio DTS                                          |
| \_GUID AVEncDTSHD di CODEcapi \_                | DTS-audio HD                                       |
| \_GUID AVEncDV di CODEcapi \_                   | Video DV                                           |
| \_GUID AVEncH264Video di CODEcapi \_            | Video H. 264                                        |
| \_GUID AVEncMLP di CODEcapi \_                  | Audio di compressione meridiano (MLP)              |
| \_GUID AVEncMPEG1Audio di CODEcapi \_           | Audio MPEG-1                                       |
| \_GUID AVEncMPEG1Video di CODEcapi \_           | Video MPEG-1                                       |
| \_GUID AVEncMPEG2Audio di CODEcapi \_           | Audio MPEG-2                                       |
| \_GUID AVEncMPEG2Video di CODEcapi \_           | Video MPEG-2                                       |
| \_GUID AVEncPCM di CODEcapi \_                  | Audio PCM                                          |
| \_GUID AVEncSDDS di CODEcapi \_                 | Audio di Sony Dynamic Digital Sound (SDD)            |
| \_GUID AVEncWMALossless di CODEcapi \_          | Audio senza perdita di Windows Media Audio 9               |
| \_GUID AVEncWMAPro di CODEcapi \_               | Audio Windows Media Audio 9 Professional (WMA Pro) |
| \_GUID AVEncWMAVoice di CODEcapi \_             | Audio Windows Media Audio 9                  |
| \_GUID AVEncWMV di CODEcapi \_                  | Windows Media Video                                |
| \_GUID AVEndMPEG4Video di CODEcapi \_           | Video MPEG-4                                       |



 

## <a name="remarks"></a>Commenti

Le applicazioni possono impostare questa proprietà per specificare lo schema di codifica da usare. I codec possono inoltre restituire questa proprietà come funzionalità.

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

 

 




