---
description: Viene illustrato il modo in cui un'applicazione o un provider di servizi può connettersi a una Smart Card utilizzando il sottosistema smart card.
ms.assetid: 27f8f25f-1883-4070-94a4-0d3c51032378
title: Accesso a una smart card
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b155d467c9de28b1e02dea01511ea1e71d574eb1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313301"
---
# <a name="accessing-a-smart-card"></a>Accesso a una smart card

Il sottosistema [*Smart Card*](/windows/desktop/SecGloss/s-gly) fornisce diversi mezzi per la connessione di un'applicazione o di un [*provider di servizi*](/windows/desktop/SecGloss/c-gly) a una smart card:

-   Un'applicazione può chiamare [**SCardConnect**](/windows/desktop/api/Winscard/nf-winscard-scardconnecta) per connettersi a una scheda che risiede in un determinato Reader. Questo è il modo più semplice per stabilire la comunicazione con una smart card.
-   Un'applicazione può cercare una smart card specifica all'interno di un determinato gruppo di Reader. L'applicazione identifica la scheda in base al nome visualizzato e specifica un elenco di Reader in cui è possibile che venga visualizzata la scheda. [*Resource Manager*](/windows/desktop/SecGloss/r-gly) Cerca nell'elenco dei lettori le schede con una [*stringa ATR*](/windows/desktop/SecGloss/a-gly) che corrisponde alla scheda denominata e restituisce informazioni sullo stato dell'applicazione. Il [*sottosistema Smart Card*](/windows/desktop/SecGloss/s-gly) non inserisce mai un'interfaccia utente grafica o interagisce con la scheda oltre a ottenere la stringa ATR. Tuttavia, fornisce informazioni sufficienti per l'applicazione o un controllo comune per poter esaminare l'utente attraverso l'individuazione del tipo di scheda o scheda desiderato. Ciò comporta il mapping della richiesta a un lettore specifico, a cui viene indirizzato un ulteriore I/O.
-   Un'applicazione può richiedere un elenco di schede che supportano un determinato set di interfacce smart card. L'applicazione può quindi usare l'elenco nel caso precedente. In questo modo le applicazioni possono connettersi alle schede in base alle rispettive funzionalità, indipendentemente dal loro nome.

Quando un'applicazione cerca una scheda, fornisce una matrice di nomi di Reader in cui cercare. Per ogni elemento Reader nella matrice, Resource Manager fornisce le informazioni seguenti:

-   Indica se il Reader è disponibile per l'utilizzo da parte dell'applicazione.
-   Indica se è presente una scheda inserita nel lettore e, in caso affermativo, qual è la stringa ATR.
-   Indica se la stringa ATR della scheda corrisponde a una delle stringhe ATR delle schede richieste.

L'applicazione utilizza le informazioni restituite per applicare altri filtri alle schede o per richiedere all'utente di selezionare la scheda desiderata. Si noti che uno o più dei Reader restituiti possono essere aperti per l'utilizzo esclusivo da parte di altre applicazioni, pertanto l'accesso a questo elenco di lettori non è garantito.

 

 
