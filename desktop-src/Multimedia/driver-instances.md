---
title: Istanze di driver
description: Istanze di driver
ms.assetid: 93dba9e8-bfb3-4714-9466-cf5c78babcf2
keywords:
- driver installabili, istanze
- driver installabili, più istanze
- più istanze di driver
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37148dcb12fbfa2984d4e55424102b5985165d9d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709589"
---
# <a name="driver-instances"></a>Istanze di driver

Windows consente di eseguire più istanze di un driver installabile. Il sistema crea un'istanza del driver ogni volta che il driver viene aperto ed Elimina l'istanza quando il driver viene chiuso. Le istanze del driver sono particolarmente utili per i driver installabili che supportano più dispositivi o aperti da più applicazioni o dalla stessa applicazione più volte.

Per consentire al driver di tenere traccia delle istanze, il sistema invia un handle di istanza di driver con ogni messaggio di driver dopo la creazione dell'istanza. Poiché questo handle identifica in modo univoco l'istanza, i driver installabili spesso associano l'handle alla memoria e ad altre risorse allocate in modo specifico per l'istanza.

Quando viene aperta la prima istanza, il sistema invia al driver i messaggi di [**\_ caricamento DRV**](drv-load.md), [**\_ Abilita DRV**](drv-enable.md)e [**drv \_**](drv-open.md) , in questo ordine. I \_ messaggi di attivazione DRV Load e DRV \_ segnalano al driver che è ora in memoria ed è abilitata per l'operazione. Il \_ messaggio aperto DRV identifica l'handle dell'istanza e può includere informazioni di configurazione per l'istanza. A ogni apertura successiva di un'istanza dello stesso driver, il sistema invia solo un messaggio di \_ apertura DRV.

Quando si elabora un \_ messaggio di caricamento DRV, un driver legge in genere le impostazioni di configurazione dal registro di sistema, configura il driver e qualsiasi hardware associato e alloca memoria per l'utilizzo da parte di tutte le istanze del driver. Se un driver non è in grado di completare la configurazione o di allocare memoria, restituisce zero per indicare al sistema di rimuovere immediatamente il driver dalla memoria e impedire l'invio di messaggi successivi. Quando si elabora il \_ messaggio di abilitazione DRV, il driver prepara l'hardware per la ricezione e l'elaborazione delle richieste di input e output (I/O). La preparazione può includere l'installazione di gestori di interrupt.

Quando si elabora il \_ messaggio aperto DRV, il driver alloca memoria o risorse richieste dall'istanza specificata del driver e quindi restituisce un valore diverso da zero. Il sistema utilizza questo valore diverso da zero come *identificatore del driver* nei messaggi di driver successivi per l'istanza. Il driver può utilizzare questo identificatore per qualsiasi scopo. Alcuni driver, ad esempio, utilizzano un handle di memoria per l'identificatore per ottenere accesso rapido alla memoria contenente le informazioni sull'istanza specificata.

Molti driver installabili elaborano il secondo parametro del \_ messaggio di apertura DRV, fornendo al sistema e alle applicazioni il mezzo per inviare informazioni aggiuntive al driver all'apertura di un'istanza. Il parametro può essere un singolo valore o un indirizzo di una struttura che contiene un set di valori. Quando si elabora DRV \_ aperto, il driver controlla il parametro per determinare se è un valore e utilizza i valori specificati, se presenti, per completare la creazione dell'istanza.

Il sistema invia un messaggio di [**\_ chiusura DRV**](drv-close.md) ogni volta che un'istanza viene chiusa. L'handle dell'istanza inviato con il messaggio identifica l'istanza da chiudere. Quando viene chiusa l'ultima istanza rimanente, il sistema invia i \_ messaggi DRV Close, [**drv \_ Disable**](drv-disable.md)e [**drv \_ disponibili**](drv-free.md) nell'ordine specificato. Il \_ messaggio di chiusura di DRV indica al driver di chiudere l'istanza di e i \_ messaggi di disabilitazione e di DRV non sono in grado di \_ notificare al driver che è ora disabilitato e che verranno immediatamente liberati dalla memoria.

Quando si elabora il \_ messaggio di chiusura DRV, il driver libera in genere qualsiasi memoria o risorsa allocata per l'istanza. Quando si elabora il \_ messaggio di disabilitazione DRV, il driver posiziona qualsiasi hardware in uno stato inattivo, che può includere la rimozione dei gestori di interrupt. Quando si elabora il \_ messaggio privo di DRV, il driver libera la memoria o le risorse ancora allocate.

I driver installabili non sono necessari per supportare più istanze. Un driver può impedire la creazione di un'istanza restituendo zero per il [**messaggio \_ aperto DRV**](drv-open.md) .

 

 




