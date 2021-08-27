---
description: Illustra i mezzi con cui un'applicazione o un provider di servizi può connettersi a un smart card usando il sottosistema smart card servizio.
ms.assetid: 27f8f25f-1883-4070-94a4-0d3c51032378
title: Accesso a una smart card
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ae7a7954d9a48191884c8ed0fd7ee65ad3bb007aae18b00efc6581e5f2e6221
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120101471"
---
# <a name="accessing-a-smart-card"></a>Accesso a una smart card

Il [*sottosistema*](/windows/desktop/SecGloss/s-gly) smart card fornisce diversi mezzi per connettere un'applicazione o un [*provider*](/windows/desktop/SecGloss/c-gly) di servizi a un smart card:

-   Un'applicazione può chiamare [**SCardConnect**](/windows/desktop/api/Winscard/nf-winscard-scardconnecta) per connettersi a una scheda che risiede in un determinato lettore. Questo è il modo più semplice per stabilire la comunicazione con un smart card.
-   Un'applicazione può cercare uno specifico smart card all'interno di un determinato gruppo di lettori. L'applicazione identifica la scheda in base al nome visualizzato e specifica un elenco di lettori in cui può essere visualizzata la scheda. Resource [*Manager cerca nell'elenco*](/windows/desktop/SecGloss/r-gly) di lettori le schede con una stringa [*ATR*](/windows/desktop/SecGloss/a-gly) corrispondente alla scheda denominata e restituisce le informazioni sullo stato all'applicazione. Il [*smart card sottosistema*](/windows/desktop/SecGloss/s-gly) non inserisce mai un'interfaccia utente grafica o interagisce con la scheda oltre a ottenere la stringa ATR. Fornisce tuttavia informazioni sufficienti per l'applicazione o un controllo comune per poter individuare la scheda o il tipo di scheda desiderato. Ciò comporta il mapping della richiesta a un lettore specifico, a cui viene indirizzata un'ulteriore operazione di I/O.
-   Un'applicazione può richiedere un elenco di schede che supportano un determinato set smart card interfacce. L'applicazione può quindi usare l'elenco nel caso precedente. In questo modo le applicazioni possono connettersi alle schede in base alle funzionalità, indipendentemente dal nome.

Quando un'applicazione cerca una scheda, fornisce una matrice di nomi di reader in cui cercare. Per ogni elemento reader nella matrice, resource manager fornisce le informazioni seguenti:

-   Indica se il lettore è disponibile per l'uso da parte di questa applicazione.
-   Indica se è presente una scheda inserita in questo lettore e, in tal caso, qual è la relativa stringa ATR.
-   Indica se la stringa ATR della scheda corrisponde a una delle stringhe ATR delle schede richieste.

L'applicazione usa le informazioni restituite per applicare altri filtri alle schede o per richiedere all'utente di selezionare la scheda desiderata. Si noti che uno o più dell'elenco restituito di lettori possono essere aperti per l'uso esclusivo da parte di altre applicazioni, pertanto l'accesso a questo elenco di lettori non è garantito.

 

 
