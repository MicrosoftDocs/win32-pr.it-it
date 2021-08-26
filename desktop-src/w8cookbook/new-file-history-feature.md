---
title: Nuova Cronologia file funzionalità
description: Nuova Cronologia file funzionalità
ms.assetid: B1EE4638-5591-483B-AA09-600E242ED50B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1502450c1376a57f9de99badc5188c8ce07761e0c28ae3ac2245a84437b5e66d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119932191"
---
# <a name="new-file-history-feature"></a>Nuova Cronologia file funzionalità

## <a name="platform"></a>Piattaforma

**Client** : Windows 8 


## <a name="description"></a>Descrizione

La nuova Cronologia file sostituisce la funzione Di backup e ripristino esistente e offre protezione per i file utente archiviati nelle librerie utente. Viene fornito un set di API che consente agli sviluppatori di abilitare Cronologia file e selezionare una destinazione di archiviazione specifica. La documentazione per queste API è disponibile in MSDN.

Può influire sui flussi di lavoro correlati alla protezione dei dati e alla documentazione che dipendono dalla funzionalità Windows Backup e ripristino.

Non è consigliabile usare entrambe le funzionalità contemporaneamente. Cronologia file verifica se una pianificazione di backup esiste ed è attiva e, se ne trova una, non consente agli utenti di attivarla. In questo caso, gli utenti che Cronologia file necessario eliminare la Windows Backup pianificazione.

## <a name="manifestation"></a>Manifestazione

È possibile che i flussi di lavoro siano interrotti e che sia necessario aggiornare la documentazione per il metodo precedente per l'accesso alla funzionalità Windows Backup e ripristino per riflettere queste modifiche.

## <a name="solution"></a>Soluzione

Rivedere le app che contengono flussi di lavoro che sono influenzati negativamente dalla nuova funzionalità Cronologia file per rimuovere eventuali conflitti e incorporare il nuovo set di API.

## <a name="tests"></a>Test

L'API consente agli sviluppatori di determinare se Cronologia file è attivata.

 

 




