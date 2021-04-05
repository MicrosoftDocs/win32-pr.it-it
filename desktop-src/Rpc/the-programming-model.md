---
title: Modello di programmazione
description: Nei primi giorni della programmazione del computer, ogni programma è stato scritto come un blocco monolitico di grandi dimensioni, riempito con istruzioni GOTO.
ms.assetid: b64d5338-a06a-4a27-bedb-c9011fa5a5a3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bcc0fd51404290b3d673982001cb3ee91bf1747
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710894"
---
# <a name="the-programming-model"></a>Modello di programmazione

Nei primi giorni della programmazione del computer, ogni programma è stato scritto come un blocco monolitico di grandi dimensioni, riempito con istruzioni **goto** . Ogni programma doveva gestire un input e un output propri a dispositivi hardware diversi. Con la maturità della disciplina di programmazione, questo codice monolitico è stato organizzato in procedure, con le procedure utilizzate più di frequente nelle librerie per la condivisione e il riutilizzo.

![istruzioni goto monolitiche rispetto alle procedure compresse in librerie condivise](images/prog-a06.png)

Il linguaggio di programmazione C supporta la programmazione orientata a procedure. In C, la procedura principale si riferisce a tutte le altre procedure come caselle nere. La procedura principale, ad esempio, non è in grado di determinare il funzionamento delle procedure A, B e X. La routine Main chiama solo un'altra procedura. non sono disponibili informazioni sulla modalità di implementazione di tale procedura.

![isolamento delle attività eseguite in procedure esterne](images/prog-a08.png)

I linguaggi di programmazione orientati alle procedure forniscono semplici meccanismi per specificare e scrivere procedure. Il prototipo di funzione C-standard ANSI, ad esempio, è un costrutto usato per specificare il nome di una routine, il tipo del risultato restituito (se presente) e il numero, la sequenza e il tipo dei relativi parametri. L'utilizzo del prototipo di funzione è un metodo formale per specificare un'interfaccia tra le routine.

Microsoft RPC si basa sul modello di programmazione, consentendo alle procedure, raggruppate in interfacce, di risiedere in processi diversi rispetto al chiamante. Microsoft RPC aggiunge inoltre un approccio più formale alla definizione della procedura che consente al chiamante e alla routine chiamata di adottare un contratto per lo scambio remoto di dati e la chiamata di funzionalità. Nel modello di programmazione RPC Microsoft, le chiamate di funzione tradizionali sono integrate con due elementi aggiuntivi.

-   Il primo elemento è un file. idl/. ACF che descrive esattamente lo scambio di dati e il meccanismo di passaggio del parametro tra il chiamante e la routine chiamata.
-   Il secondo elemento è un set di API di runtime che forniscono agli sviluppatori un controllo granulare della chiamata di procedura remota, inclusi gli aspetti di sicurezza, la gestione dello stato sul server, l'indicazione dei client che possono comunicare con il server e così via.

 

 




