---
description: "Proprietà AVDecAudioDualMono: specifica se l'audio a 2 canali è codificato come stereo o doppio mono."
ms.assetid: 96cb9e17-588c-4a1a-a7ba-7f8439d5b79a
title: Proprietà AVDecAudioDualMono (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: adc84e19d41840b358e3e79576152dbc8527e2bb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096569"
---
# <a name="avdecaudiodualmono-property"></a>AVDecAudioDualMono - proprietà

Specifica se l'audio a 2 canali è codificato come stereo o doppio mono.

Questa proprietà è di sola lettura.

## <a name="data-type"></a>Tipo di dati

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID proprietà

**CODECAPI \_ AVDecAudioDualMono**

## <a name="property-value"></a>Valore proprietà

Il valore di questa proprietà è un membro [**dell'enumerazione eAVDecAudioDualMono.**](/windows/desktop/api/codecapi/ne-codecapi-eavdecaudiodualmono)

## <a name="remarks"></a>Commenti

Questa proprietà si applica solo quando il flusso di bit di input del decodificatore contiene audio a due canali. Un flusso audio a due canali può essere codificato come stereo o come doppio mono. Se l'audio è doppio mono, è possibile impostare la proprietà [**AVDecAudioDualMonoReproMode**](avdecaudiodualmonorepromode-property.md) per configurare il modo in cui il decodificatore riproduce l'audio.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App \[ desktop UWP di Windows 2000 Professional \|\]<br/>                     |
| Server minimo supportato<br/> | App UWP per app desktop di Windows 2000 Server \[ \|\]<br/>                           |
| Intestazione<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà API codec](codec-api-properties.md)
</dt> <dt>

[**Interfaccia ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




