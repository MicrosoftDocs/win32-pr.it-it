---
description: Specifica se l'audio a 2 canali è codificato come stereo o doppia mono.
ms.assetid: 96cb9e17-588c-4a1a-a7ba-7f8439d5b79a
title: Proprietà AVDecAudioDualMono (codecapis. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 107adb00eb68cbb9ec19331b0c0f3f9db916a306
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103876854"
---
# <a name="avdecaudiodualmono-property"></a>Proprietà AVDecAudioDualMono

Specifica se l'audio a 2 canali è codificato come stereo o doppia mono.

Questa proprietà è di sola lettura.

## <a name="data-type"></a>Tipo di dati

**UInt32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID proprietà

**Codecapis \_ AVDecAudioDualMono**

## <a name="property-value"></a>Valore proprietà

Il valore di questa proprietà è un membro dell'enumerazione [**eAVDecAudioDualMono**](/windows/desktop/api/codecapi/ne-codecapi-eavdecaudiodualmono) .

## <a name="remarks"></a>Commenti

Questa proprietà si applica solo quando il flusso di bit di input del decodificatore contiene audio a due canali. Un flusso audio a due canali può essere codificato come stereo o come doppio mono. Se l'audio è dual mono, è possibile impostare la proprietà [**AVDecAudioDualMonoReproMode**](avdecaudiodualmonorepromode-property.md) per configurare la modalità di riproduzione dell'audio da parte del decodificatore.

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

 

 




