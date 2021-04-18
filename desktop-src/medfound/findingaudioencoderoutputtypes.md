---
description: Ricerca di tipi di output del codificatore audio
ms.assetid: cd47d45b-ea47-4dec-867e-d51145d7f084
title: Ricerca di tipi di output del codificatore audio (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5389274cca1178ebc0ae03e21f7a804f73a5db48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305379"
---
# <a name="finding-audio-encoder-output-types-microsoft-media-foundation"></a>Ricerca di tipi di output del codificatore audio (Microsoft Media Foundation)

Poiché è necessario usare un formato di output del codificatore audio enumerato dal codificatore audio, è necessario disporre di un modo per trovare il formato più adatto alle proprie esigenze. Il numero di canali, i bit per campione e la frequenza di campionamento dell'output che si sceglie devono corrispondere ai valori per il contenuto compresso. Tuttavia, il codificatore può supportare diversi tipi all'interno di questi vincoli.

Il fattore decisivo per la scelta di un tipo è la velocità in bit del flusso codificato; si desidera trovare un tipo di supporto che corrisponda all'input e ha una velocità in bit più vicina possibile a un valore di destinazione. Se si enumerano i tipi di output VBR a passaggio singolo, è il valore di qualità che deciderà il tipo usato. Per ulteriori informazioni sui valori di qualità nei tipi di output enumerati, vedere [enumerazione di tipi audio per modalità di codifica specifiche](enumeratingaudiotypesforspecificencodingmodes.md).

> [!Note]  
>    Il codificatore audio enumera alcuni tipi che sono duplicati di altri tipi in quasi tutti i modi. Questi duplicati sono disponibili per i formati in cui il numero di pacchetti al secondo non soddisfa i requisiti per l'archiviazione nei file ASF se sincronizzati con il video. L'audio sincronizzato con video in un file ASF deve avere tre o più pacchetti al secondo per velocità in bit inferiori a 32000 e 5 o più pacchetti al secondo per velocità in bit maggiori o uguali a 32000.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Configurazione della codifica audio](configuringaudioencoding.md)
</dt> <dt>

[Enumerazione dei tipi audio per modalità di codifica specifiche](enumeratingaudiotypesforspecificencodingmodes.md)
</dt> </dl>

 

 



