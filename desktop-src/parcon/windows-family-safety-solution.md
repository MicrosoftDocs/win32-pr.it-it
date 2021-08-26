---
description: Windows Family Safety soluzione
ms.assetid: b89cf0c7-bf9f-4bcb-b008-8b7c792f3300
title: Windows Family Safety soluzione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cc5e5749201fc849e7c9476c97c6fbd3dc5ee5b2d3f26ed3988eb72ac59c1ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119951651"
---
# <a name="windows-family-safety-solution"></a>Windows Family Safety soluzione

I requisiti chiave definiti da Microsoft per una soluzione più completa sono i seguenti. Si noti che la definizione per online è principalmente una tecnologia con connessione Internet, a differenza di un client offline che in genere è vincolato al computer.

-   Fornire un'unica area facilmente individuabile nell'interfaccia utente del sistema operativo in cui tutti i criteri di controllo genitori, il controllo del monitoraggio delle attività e i dati delle attività per un'identità possono essere individuati immediatamente.

-   Supportare il monitoraggio di un'attività sufficiente dell'utente controllato in modo che un padre o un sorveglianza abbia ragionevole fiducia che potrebbero essere individuate attività rischiose. Inoltre, registrare la riconfigurazione dei criteri dell'utente controllato in modo che le modifiche non intenzionali o non autorizzate siano individuabili.

-   Esporre le funzionalità di monitoraggio delle attività tramite Windows di registrazione eventi di Vista standard e fornire una soluzione di visualizzazione predefinita. Definire gli eventi di attività standard e fornire l'estendibilità alla generazione di eventi personalizzati da parte degli ISV.

-   Promuovere che tutti i monitoramenti e le restrizioni per un utente siano attivati solo in base al consenso esplicito da parte di genitori o guardiani. Laddove possibile, la funzionalità delle restrizioni deve essere completamente inattiva per gli utenti non controllati per ridurre al minimo i rischi di sicurezza e compatibilità delle applicazioni.

-   Microsoft si impegna, laddove possibile, a non pronunciare un giudizio di valore in base all'età o ad altri parametri per l'utente controllato (le terze parti possono scegliere di farlo). Tali decisioni vengono prese dall'elemento padre o dal guardiano, spesso influenzate da community o organizzazioni.

-   Fornire implementazioni nel prodotto per il monitoraggio delle attività offline e restrizioni in cui attualmente sono disponibili poche o nessuna offerta, in cui la funzionalità di rischio di sicurezza associata è disponibile nel prodotto o in cui una soluzione Microsoft offre funzionalità affidabili e idonee completamente integrate con la progettazione del sistema operativo.

-   In genere, alzare di livello le applicazioni per eseguire la registrazione e le restrizioni per un contesto e un'esperienza dell'interfaccia utente ottimali.

    Eccezione: fornire il monitoraggio completo delle attività online e le restrizioni in aree selezionate in cui i vantaggi per i consumatori e il settore superano i costi.

-   Esporre le impostazioni dell'interfaccia utente di controllo genitori e le definizioni degli eventi di attività usando API pubbliche in modo che terze parti possano eseguire query sullo stato, modificare le impostazioni e leggere i log attività se sono in esecuzione con privilegi di account Windows sufficienti.

Un obiettivo generale è promuovere la coesistenza delle soluzioni di controllo genitori di terze parti con le funzionalità integrate e supportare l'aggiunta di valore integrando, estendendo o fornendo funzionalità alternative laddove appropriato.

 

 



