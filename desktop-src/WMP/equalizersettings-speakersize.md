---
title: EQUALIZERSETTINGS.speakerSize
description: L'attributo speakerSize specifica o Recupera il numero di indice della dimensione del relatore corrente.
ms.assetid: 454d07bf-49cd-48a5-9724-6415a925367a
keywords:
- Media Player Windows EQUALIZERSETTINGS. speakerSize
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.speakerSize
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26dc49af55e96d3ef8de4e8a4567b3a4296ca214
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327303"
---
# <a name="equalizersettingsspeakersize"></a>EQUALIZERSETTINGS.speakerSize

L'attributo **speakerSize** specifica o Recupera il numero di indice della dimensione del relatore corrente.

``` syntax
        elementID.speakerSize
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è un **numero** di lettura/scrittura (Long) contenente uno dei valori seguenti.



| Valore | Descrizione                              |
|-------|------------------------------------------|
| 0     | Gli altoparlanti correnti sono cuffie.     |
| 1     | Gli altoparlanti correnti hanno dimensioni normali. |
| 2     | Gli altoparlanti correnti sono di grandi dimensioni.          |



 

## <a name="remarks"></a>Commenti

Il nome descrittivo della dimensione del relatore può essere recuperato usando l'attributo **currentSpeakerName** .

Questo attributo viene ignorato se **enhancedAudio** è impostato su false.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------|
| Versione<br/> | Windows Media Player 9 serie o versione successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento EQUALIZERSETTINGS**](equalizersettings-element.md)
</dt> <dt>

[**EQUALIZERSETTINGS.currentSpeakerName**](equalizersettings-currentspeakername.md)
</dt> <dt>

[**EQUALIZERSETTINGS.enhancedAudio**](equalizersettings-enhancedaudio.md)
</dt> </dl>

 

 





