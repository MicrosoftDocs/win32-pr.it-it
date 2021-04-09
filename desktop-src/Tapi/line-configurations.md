---
description: Un dispositivo a linee può rappresentare un pool di risorse omogenee (canali) che vengono usate per stabilire le chiamate. In un computer client, un TSP fornisce in genere l'accesso a uno o più dispositivi linea.
ms.assetid: cb599a4d-80dd-40fe-b448-f9ea58f01124
title: Configurazioni di linea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8722dab15763822f6535783ecc8bc18e681e13ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879734"
---
# <a name="line-configurations"></a>Configurazioni di linea

Un dispositivo a linee può rappresentare un pool di risorse omogenee (canali) che vengono usate per stabilire le chiamate. In un computer client, un TSP fornisce in genere l'accesso a uno o più dispositivi linea.

Di seguito sono riportati alcuni esempi di come un provider di servizi può modellare diverse configurazioni:

**Esempio 1:** Una singola linea di POT nei modelli di connessione incentrata sul computer o sul telefono. Il modello più semplice è un dispositivo a linea singola con un canale.

**Esempio 2:** Una singola riga BRI-ISDN nei modelli di connessione incentrata sul computer o sul telefono. Il provider di servizi dispone di una serie di opzioni relative a come può essere utile modellare questo, ad esempio:

-   Modellare la linea BRI come un dispositivo a linea singola con un pool di due canali B che consente la combinazione di entrambi i canali per la creazione di chiamate a 128 kbps.
-   Modellare ciascun canale B come dispositivo a linee distinte e impedire che entrambi i canali vengano combinati in un singolo canale a 128 kbps.
-   Modellare la connessione BRI come due dispositivi a linee separate, ciascuno dei quali disegna fino a due canali da un pool condiviso di due canali B.
-   Modello come dispositivo a tre linee, uno per ogni canale B e uno per la combinazione. Chiaramente negli ultimi due modelli, le risorse possono essere assegnate a diversi dispositivi a linee in momenti diversi.

**Esempio 3:** Nei sistemi client/server, un pool di porte telefoniche collegate a un server può essere condiviso tra più computer client in una rete locale. Il pool può essere amministrato per assegnare un numero massimo di dispositivi lineari (quota) a ogni workstation client. Non è insolito che la somma di tutte le quote superi il numero totale di righe. Inoltre, un client specificato con una quota uguale a 2 può essere soddisfatto usando le porte 1 e 2 alla volta e le porte 7 e 11 in un secondo momento. Il provider di servizi per il pool può modellare questa disposizione assegnando a ogni workstation client l'accesso a due dispositivi linea.

Si supponga che la configurazione dei provider di servizi per un determinato computer sia tale che questo provider di servizi specifico ottenga **DeviceIDBase** 3. Ciò implica che gli identificatori di dispositivo (fissi) per questo client sono 3 e 4. Se l'applicazione chiama successivamente la funzione TAPI 2 [**lineGetDevCaps**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps) per il dispositivo 3 e di nuovo per il dispositivo 4, dovrebbe essere in grado di presumere che le funzionalità del dispositivo per ognuno di questi dispositivi siano costanti, perché questo è il modello del dispositivo. Fino a quando la configurazione del provider di servizi del computer specificato rimane costante, gli identificatori di dispositivo visualizzati a livello di TSPI rimangono costanti, anche se il server modifica le allocazioni delle porte. Per i dispositivi basati su server che vengono raggruppati come descritto nell'esempio 3, questo contiene solo i dispositivi linea con funzionalità del dispositivo identiche. Naturalmente, se la configurazione del provider di servizi del computer specificato viene modificata, in modo che questo provider di servizi ottenga un **DeviceIDBase** diverso, gli identificatori di dispositivo cambiano in modo corrispondente.

**Esempio 4:** Collegamento switch a host:

-   Per fornire la telefonia personale a ogni desktop, il provider di servizi potrebbe modellare la linea PBX abbinata al computer come un dispositivo a linea singola con un canale. In ogni computer client sarà disponibile un dispositivo a linee.
-   Ogni stazione di terze parti può essere modellata come un dispositivo a linee distinto. Ciò consente all'applicazione di controllare le chiamate su altre stazioni. Per questa soluzione è necessario che l'applicazione apra ogni riga che si desidera manipolare o monitorare, operazione che può essere corretta se solo un numero ridotto di righe è di interesse, ma può generare un sovraccarico se è necessario un numero elevato di righe.
-   Il set di tutte le stazioni di terze parti può essere modellato come un dispositivo a linea singola con un indirizzo (numero di telefono) assegnato per ogni stazione. Viene aperto un solo dispositivo, che fornisce il monitoraggio e il controllo di tutti gli indirizzi sulla riga (tutte le stazioni). Per originare una chiamata su una di queste stazioni, l'applicazione deve solo specificare l'indirizzo della stazione per l'operazione che effettua la chiamata. Non sono necessarie operazioni di apertura aggiuntive. Questa modellazione implica che tutte le stazioni hanno le stesse funzionalità del dispositivo di linea, anche se le funzionalità di indirizzi potrebbero essere diverse.

> [!Note]  
> Tutti questi esempi sono semplicemente diversi perché un provider di servizi può scegliere di implementare il mapping del comportamento del dispositivo line in una realizzazione fisica.

 

 

 
