---
title: EQUALIZERSETTINGS.speakerSize
description: L'attributo speakerSize specifica o recupera il numero di indice delle dimensioni correnti del parlante.
ms.assetid: 454d07bf-49cd-48a5-9724-6415a925367a
keywords:
- EQUALIZERSETTINGS.speakerSize Windows Media Player
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.speakerSize
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46d289a89a22e8c10cf669e9b55fc304826acb3ce0f72468f725e7d5fae0dfc8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117748649"
---
# <a name="equalizersettingsspeakersize"></a>EQUALIZERSETTINGS.speakerSize

**L'attributo speakerSize** specifica o recupera il numero di indice delle dimensioni correnti del parlante.

``` syntax
        elementID.speakerSize
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è un numero **di** lettura/scrittura (long) contenente uno dei valori seguenti.



| Valore | Descrizione                              |
|-------|------------------------------------------|
| 0     | Gli altoparlanti correnti sono cuffia.     |
| 1     | I parlanti correnti hanno dimensioni normali. |
| 2     | Gli altoparlanti correnti sono di grandi dimensioni.          |



 

## <a name="remarks"></a>Commenti

Il nome descrittivo delle dimensioni del parlante può essere recuperato usando **l'attributo currentSpeakerName.**

Questo attributo viene ignorato **se enhancedAudio** è impostato su false.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------|
| Versione<br/> | Windows Media Player serie 9 o successive<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento EQUALIZERSETTINGS**](equalizersettings-element.md)
</dt> <dt>

[**EQUALIZERSETTINGS.currentSpeakerName**](equalizersettings-currentspeakername.md)
</dt> <dt>

[**EQUALIZERSETTINGS.enhancedAudio**](equalizersettings-enhancedaudio.md)
</dt> </dl>

 

 





