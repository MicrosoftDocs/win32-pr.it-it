---
description: Il lessico, o elenco di parole possibili usate dal modello linguistico di un determinato riconoscitore, è contenuto in uno o più dizionari.
ms.assetid: e975a75f-ab88-4164-afc8-3b817988504d
title: Dizionari ed elenchi di frasi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0cc5b97918e1fed384494e887b604f1d08856e27232ed82f09bceff3ce14fe2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120110961"
---
# <a name="dictionaries-and-phrase-lists"></a>Dizionari ed elenchi di frasi

Il lessico, o elenco di parole possibili usate dal modello linguistico di un determinato riconoscitore, è contenuto in uno o più dizionari. Il riconoscimento esegue la ricerca in tutti i dizionari disponibili nel sistema durante la compilazione delle corrispondenze di riconoscimento. È possibile usare le API Riconoscimento vocale Microsoft (SAPI) per modificare alcuni di questi dizionari.

Un elenco di frasi offre un altro modo per modificare il vocabolario del riconoscitore. L'aggiunta di parole a un elenco di frasi estende il vocabolario. L'aggiunta di parole e quindi la limitazione del riconoscimento all'uso solo dell'elenco di frasi (a differenza dell'elenco di frasi e dei dizionari) limita il vocabolario.

Le versioni precedenti delle API per la tecnologia Tablet PC si basano sul concetto di elenchi di parole. Gli elenchi di parole sono quasi identici agli elenchi di frasi e vengono usati per lo stesso scopo quando si lavora direttamente con un oggetto [**RecognizerContext**](inkrecognizercontext-class.md) in un'applicazione abilitata per l'input penna. Per altri dettagli su dove e quando usare gli elenchi di parole, vedere [Setting Context for Ink-Enabled Controls](setting-context-for-ink-enabled-controls.md).

Quando le dimensioni dell'elenco con cui si vuole estendere il lessico superano le 100.000 parole, è consigliabile usare un dizionario anziché un elenco di parole o un elenco di frasi.

 

 



