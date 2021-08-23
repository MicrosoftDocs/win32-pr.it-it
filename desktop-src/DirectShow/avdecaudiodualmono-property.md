---
description: "Proprietà AVDecAudioDualMono: specifica se l'audio a 2 canali è codificato come stereo o doppio mono."
ms.assetid: 96cb9e17-588c-4a1a-a7ba-7f8439d5b79a
title: Proprietà AVDecAudioDualMono (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a26bd6685cb9c9f326babbc01120019c93760fd7e1f9bf33f2a540d488300ad
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119873391"
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
| Client minimo supportato<br/> | Windows 2000 Professional \[ app desktop app \| UWP\]<br/>                     |
| Server minimo supportato<br/> | Windows 2000 App desktop UWP per le app \[ desktop di 2000 \| Server\]<br/>                           |
| Intestazione<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà API codec](codec-api-properties.md)
</dt> <dt>

[**Interfaccia ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




