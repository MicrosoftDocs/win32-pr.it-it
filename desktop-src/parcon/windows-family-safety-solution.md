---
description: Soluzione di sicurezza della famiglia di Windows
ms.assetid: b89cf0c7-bf9f-4bcb-b008-8b7c792f3300
title: Soluzione di sicurezza della famiglia di Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a2d8776893468df4f4877c7220436f505ab1e6f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318392"
---
# <a name="windows-family-safety-solution"></a>Soluzione di sicurezza della famiglia di Windows

Di seguito sono riportati i requisiti chiave definiti da Microsoft per una soluzione più completa. Si noti che la definizione di online è una tecnologia principalmente connessa a Internet, a differenza di un client offline che in genere è limitato al computer.

-   Fornire un'unica area facile da trovare nell'interfaccia utente del sistema operativo in cui tutti i criteri dei controlli padre, il controllo del monitoraggio delle attività e i dati delle attività per un'identità possono essere individuati facilmente.

-   Supportare il monitoraggio di attività sufficienti dell'utente controllato in modo che un genitore o un tutore abbia una ragionevole confidenza per individuare le attività rischiose. Inoltre, riconfigurare il log dei criteri dell'utente controllato in modo che le modifiche non intenzionali o non autorizzate siano individuabili.

-   Esporre le funzionalità di monitoraggio delle attività tramite le interfacce di registrazione eventi standard di Windows Vista e fornire una soluzione di visualizzazione. Definire gli eventi di attività standard e garantire l'estendibilità per la generazione di eventi personalizzati da parte degli ISV.

-   Promuovere che tutti i monitoraggi e le restrizioni per un utente siano attivati solo in base ai genitori o ai tutori. Laddove possibile, la funzionalità delle restrizioni deve essere completamente inattiva per gli utenti non controllati per ridurre al minimo i rischi per la sicurezza e la compatibilità delle applicazioni.

-   Microsoft si impegnerà, laddove possibile, a non prendere decisioni di valore in base all'età o ad altri parametri per l'utente controllato (le terze parti possono scegliere di farlo). Tali decisioni vengono rilasciate al padre o al tutore, spesso influenzato da community o organizzazioni.

-   Fornire le implementazioni nel prodotto per il monitoraggio e le restrizioni delle attività offline, in cui sono attualmente disponibili alcune o nessuna offerta, in cui la funzionalità associata al rischio di sicurezza è disponibile nel prodotto o quando una soluzione Microsoft fornisce funzionalità efficaci e affidabili completamente integrate con la progettazione del sistema operativo.

-   In generale, alzare di livello le applicazioni per eseguire la registrazione e le restrizioni per ottimizzare il contesto e l'esperienza dell'interfaccia utente.

    Eccezione: fornire funzionalità complete di monitoraggio e restrizione delle attività in linea nelle aree selezionate in cui i vantaggi per i consumer e il settore superano i costi.

-   Esporre i controlli padre le impostazioni dell'interfaccia utente e le definizioni degli eventi di attività usando le API pubbliche in modo che le terze parti possano eseguire query per lo stato, modificare le impostazioni e leggere i log attività se sono in esecuzione con privilegi di account di Windows sufficienti.

Un obiettivo fondamentale è promuovere la coesistenza delle soluzioni di controllo parentale di terze parti con la funzionalità integrata e supportare l'aggiunta di valore tramite l'integrazione di, l'estensione o la fornitura di funzionalità alternative laddove appropriato.

 

 



