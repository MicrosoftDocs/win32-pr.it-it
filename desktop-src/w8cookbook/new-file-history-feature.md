---
title: Nuova funzionalità Cronologia file
description: Nuova funzionalità Cronologia file
ms.assetid: B1EE4638-5591-483B-AA09-600E242ED50B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a70aad84f4d052d6a872c7b0cfc979d0fa05cb84
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/01/2020
ms.locfileid: "104118579"
---
# <a name="new-file-history-feature"></a>Nuova funzionalità Cronologia file

## <a name="platform"></a>Piattaforma

**Client** -Windows 8 


## <a name="description"></a>Descrizione

La nuova funzionalità Cronologia file sostituisce la funzione di backup e ripristino esistente e offre protezione per i file utente archiviati nelle librerie utente. Viene fornito un set di API che consente agli sviluppatori di abilitare a livello di codice la cronologia dei file e selezionare una destinazione di archiviazione specifica. La documentazione per queste API è disponibile in MSDN.

Potrebbe influire sui flussi di lavoro correlati alla protezione dei dati e alla documentazione che dipendono dalla funzionalità di backup e ripristino di Windows.

Non è consigliabile usare entrambe le funzionalità nello stesso momento. Cronologia file controlla se esiste una pianificazione di backup ed è attiva e se ne trova una, non consente agli utenti di attivarla. In questo caso, gli utenti che desiderano utilizzare la cronologia file dovranno eliminare la pianificazione di backup di Windows.

## <a name="manifestation"></a>Manifestazione

I flussi di lavoro possono essere interrotti e la documentazione relativa al metodo precedente per accedere alla funzionalità di backup e ripristino di Windows deve essere aggiornata per riflettere queste modifiche.

## <a name="solution"></a>Soluzione

Rivedere le app che contengono flussi di lavoro che incidono negativamente sulla nuova funzionalità di cronologia file per rimuovere eventuali conflitti e incorporare il nuovo set di API.

## <a name="tests"></a>Test

L'API consente agli sviluppatori di determinare se è attivata la cronologia file.

 

 




