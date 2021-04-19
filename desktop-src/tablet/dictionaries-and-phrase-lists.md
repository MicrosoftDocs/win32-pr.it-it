---
description: Il lessico o l'elenco di parole possibili usate dal modello di linguaggio di un particolare riconoscitore sono contenuti in uno o più dizionari.
ms.assetid: e975a75f-ab88-4164-afc8-3b817988504d
title: Dizionari ed elenchi di frasi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1f88dc2f6b05eea322b6e88dda1f986b3c54b7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316854"
---
# <a name="dictionaries-and-phrase-lists"></a>Dizionari ed elenchi di frasi

Il lessico o l'elenco di parole possibili usate dal modello di linguaggio di un particolare riconoscitore sono contenuti in uno o più dizionari. Il riconoscitore Cerca tutti i dizionari disponibili nel sistema durante la compilazione delle corrispondenze di riconoscimento. Per modificare alcuni di questi dizionari, è possibile usare le API Microsoft Speech (SAPI).

Un elenco di frasi fornisce un altro mezzo per modificare il vocabolario del riconoscitore. L'aggiunta di parole a un elenco di frasi estende il vocabolario; l'aggiunta di parole e la limitazione del riconoscimento per l'utilizzo solo dell'elenco di frasi (in contrapposizione all'elenco di frasi e ai dizionari) limitano il vocabolario.

Le versioni precedenti delle API della tecnologia Tablet PC si basavano sul concetto di elenchi di parole. Gli elenchi di parole sono quasi identici agli elenchi di frasi e vengono usati per lo stesso scopo quando si lavora direttamente con un oggetto [**RecognizerContext**](inkrecognizercontext-class.md) in un'applicazione abilitata per l'input penna. Per altre informazioni su dove e quando usare gli elenchi di parole, vedere [impostazione del contesto per i controlli Ink-Enabled](setting-context-for-ink-enabled-controls.md).

Quando le dimensioni dell'elenco con cui si desidera estendere il lessico superano 100.000 parole, è consigliabile utilizzare un dizionario anziché un elenco di parole o una frase.

 

 



