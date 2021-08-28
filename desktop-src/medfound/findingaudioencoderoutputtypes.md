---
description: Ricerca dei tipi di output del codificatore audio
ms.assetid: cd47d45b-ea47-4dec-867e-d51145d7f084
title: Ricerca dei tipi di output del codificatore audio (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f80dd5aa5204887472e08c6ec5ff375a99b8788924ed0848764cde9ba4b5b97
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120061576"
---
# <a name="finding-audio-encoder-output-types-microsoft-media-foundation"></a>Ricerca dei tipi di output del codificatore audio (Microsoft Media Foundation)

Poiché è necessario usare un formato di output del codificatore audio enumerato dal codificatore audio, è necessario avere un modo per trovare il formato più adatto alle proprie esigenze. Il numero di canali, i bit per campione e la frequenza di campionamento dell'output scelto devono corrispondere ai valori per il contenuto compresso. Tuttavia, il codificatore può supportare diversi tipi all'interno di questi vincoli.

Il fattore determinante per la scelta di un tipo è la velocità in bit del flusso codificato. si vuole trovare un tipo di supporto che corrisponda all'input e abbia una velocità in bit il più vicina possibile a un valore di destinazione. Se si enumerano i tipi di output VBR con un solo passaggio, è il valore di qualità a decidere il tipo in uso. Per altre informazioni sui valori di qualità nei tipi di output enumerati, vedere Enumerazione dei tipi [audio per modalità di codifica specifiche.](enumeratingaudiotypesforspecificencodingmodes.md)

> [!Note]  
>    Il codificatore audio enumera alcuni tipi duplicati di altri tipi in quasi tutti i modi. Questi duplicati esistono per i formati in cui il numero di pacchetti al secondo non soddisfa i requisiti per l'archiviazione nei file ASF quando viene sincronizzato con video. L'audio sincronizzato con video in un file ASF deve avere 3 o più pacchetti al secondo per velocità in bit inferiori a 32000 e 5 o più pacchetti al secondo per velocità in bit maggiori o uguali a 32000.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Configurazione della codifica audio](configuringaudioencoding.md)
</dt> <dt>

[Enumerazione dei tipi audio per modalità di codifica specifiche](enumeratingaudiotypesforspecificencodingmodes.md)
</dt> </dl>

 

 



