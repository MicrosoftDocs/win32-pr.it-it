---
description: Un dispositivo a linee può rappresentare un pool di risorse omogenee (canali) usate per stabilire chiamate. In un computer client un provider di servizi di configurazione fornisce in genere l'accesso a uno o più dispositivi line.
ms.assetid: cb599a4d-80dd-40fe-b448-f9ea58f01124
title: Configurazioni di riga
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d3705854a5bd485dba01452a3885e52c3c2d0baf0d495a65a2db24d75894eeb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120126251"
---
# <a name="line-configurations"></a>Configurazioni di riga

Un dispositivo a linee può rappresentare un pool di risorse omogenee (canali) usate per stabilire chiamate. In un computer client un provider di servizi di configurazione fornisce in genere l'accesso a uno o più dispositivi line.

Ecco alcuni esempi di come un provider di servizi potrebbe modellare diverse configurazioni:

**Esempio 1:** Singola linea POTS nei modelli di connessione incentrati sul computer o sul telefono. Il modello più semplice è un dispositivo a linea singola con un solo canale.

**Esempio 2:** Singola linea BRI-ISDN nei modelli di connessione incentrati sul computer o sul telefono. Il provider di servizi dispone di diverse opzioni per la modellazione, ad esempio:

-   Modellare la linea BRI come dispositivo a linea singola con un pool di due canali B che consente di combinare entrambi i canali per stabilire chiamate a 128 kbps.
-   Modellare ogni canale B come dispositivo linea separato e non consentire la combinazione di entrambi i canali in un singolo canale a 128 kbps.
-   Modellare la connessione BRI come due dispositivi linea separati, ognuno dei quali disegna fino a due canali da un pool condiviso di due canali B.
-   Modellare come dispositivi a tre linee, uno per ogni canale B e uno per la combinazione. Chiaramente negli ultimi due modelli, le risorse possono essere assegnate a dispositivi line diversi in momenti diversi.

**Esempio 3:** Nei sistemi client/server, un pool di porte telefoniche collegate a un server può essere condiviso tra più computer client su una rete locale. Il pool può essere amministrato per assegnare un numero massimo di dispositivi line (quota) a ogni workstation client. Non è insolito che la somma di tutte le quote superi il numero totale di righe. Inoltre, un determinato client con una quota uguale a 2 può essere soddisfatto usando le porte 1 e 2 contemporaneamente e le porte 7 e 11 in un secondo momento. Il provider di servizi per il pool può modellare questa disposizione fornendo a ogni workstation client l'accesso a due dispositivi line.

Si supponga che la configurazione dei provider di servizi per un determinato computer sia tale che questo particolare provider di servizi o ottiene **un deviceIDBase** di 3. Ciò implica che gli identificatori di dispositivo (fissi) per questo client sono 3 e 4. Se in seguito l'applicazione chiama la riga della funzione TAPI [**2GetDevCaps**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps) per il dispositivo 3 e di nuovo per il dispositivo 4, dovrebbe essere in grado di presupporre che le funzionalità del dispositivo per ognuno di questi dispositivi siano costanti, perché si tratta del modello di dispositivo. Finché la configurazione del provider di servizi del computer specificato rimane costante, gli identificatori di dispositivo visualizzati a livello TSPI rimangono costanti, anche se il server modifica le allocazioni delle porte. Per i dispositivi basati su server in pool, come descritto nell'esempio 3, questo vale solo per i dispositivi line con funzionalità di dispositivo identiche. Naturalmente, se la configurazione del provider di servizi del computer specificato viene modificata, in modo che questo provider di servizi osezioni **un Valore DeviceIDBase** diverso, gli identificatori dei dispositivi cambiano di conseguenza.

**Esempio 4:** Collegamento da commutatore a host:

-   Per fornire la telefonia personale a ogni desktop, il provider di servizi può modellare la linea DELLE ABBINATE al computer come dispositivo a linea singola con un solo canale. Ogni computer client avrebbe un dispositivo line disponibile.
-   Ogni stazione di terze parti può essere modellata come dispositivo linea separato. In questo modo l'applicazione può controllare le chiamate su altre stazioni. Questa soluzione richiede l'apertura da parte dell'applicazione di ogni riga da modificare o monitorare, operazione che può essere utile se è interessato solo un numero ridotto di righe, ma può generare un sovraccarico elevato se è coinvolto un numero elevato di righe.
-   Il set di tutte le stazioni di terze parti può essere modellato come dispositivo a linea singola con un indirizzo (numero di telefono) assegnato per ogni stazione. Deve essere aperto un solo dispositivo, che fornisce il monitoraggio e il controllo di tutti gli indirizzi sulla linea (tutte le stazioni). Per avere origine da una chiamata su una di queste stazioni, l'applicazione deve specificare solo l'indirizzo della stazione per l'operazione che effettua la chiamata. Non sono necessarie operazioni di apertura aggiuntive. Questa modellazione implica che tutte le stazioni hanno le stesse funzionalità del dispositivo linea, anche se le relative funzionalità di indirizzo potrebbero essere diverse.

> [!Note]  
> Tutti questi esempi sono semplicemente modi diversi in cui un provider di servizi può scegliere di implementare il mapping del comportamento del dispositivo linea in una realizzazione fisica.

 

 

 
