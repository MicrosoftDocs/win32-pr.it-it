---
title: Istanze del driver
description: Istanze del driver
ms.assetid: 93dba9e8-bfb3-4714-9466-cf5c78babcf2
keywords:
- driver installabili, istanze
- driver installabili,più istanze
- più istanze di driver
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: deea546ffb7cd848993f8aac569d3624f87988b583ea47cab7bb16451cc6ed1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118941198"
---
# <a name="driver-instances"></a>Istanze del driver

Windows consente più istanze di un driver installabile. Il sistema crea un'istanza del driver ogni volta che il driver viene aperto ed elimina l'istanza quando il driver viene chiuso. Le istanze di driver sono particolarmente utili per i driver installabili che supportano più dispositivi o che vengono aperti da più applicazioni o dalla stessa applicazione più volte.

Per consentire al driver di tenere traccia delle istanze, il sistema invia un handle di istanza del driver con ogni messaggio del driver dopo la creazione dell'istanza. Poiché questo handle identifica in modo univoco l'istanza, i driver installabili spesso associano l'handle alla memoria e ad altre risorse allocate in modo specifico per l'istanza.

Quando viene aperta la prima istanza, il sistema invia i messaggi [**DRV \_ LOAD,**](drv-load.md) [**DRV \_ ENABLE**](drv-enable.md)e [**DRV \_ OPEN**](drv-open.md) al driver in tale ordine. I messaggi DRV LOAD e DRV ENABLE notificano al driver che è \_ ora in memoria ed è abilitato per il \_ funzionamento. Il messaggio DRV \_ OPEN identifica l'handle dell'istanza e può includere informazioni di configurazione per l'istanza. A ogni apertura successiva di un'istanza dello stesso driver, il sistema invia solo un messaggio DRV \_ OPEN.

Quando si elabora un messaggio DRV LOAD, un driver legge in genere le impostazioni di configurazione dal Registro di sistema, configura il driver e l'hardware associato e alloca memoria per l'uso da parte di tutte le istanze \_ del driver. Se un driver non può completare la configurazione o allocare memoria, restituisce zero per indirizzare il sistema a rimuovere immediatamente il driver dalla memoria e impedire l'invio di eventuali messaggi successivi. Durante l'elaborazione del messaggio DRV ENABLE, il driver prepara l'hardware per ricevere ed elaborare le richieste \_ di input e output (I/O). La preparazione può includere l'installazione di gestori di interrupt.

Durante l'elaborazione del messaggio DRV OPEN, il driver alloca la memoria o le risorse richieste dall'istanza specificata del driver e quindi restituisce \_ un valore diverso da zero. Il sistema usa questo valore diverso da zero come identificatore *del driver* nei messaggi del driver successivi per l'istanza. Il driver può usare questo identificatore per qualsiasi scopo. Ad esempio, alcuni driver usano un handle di memoria per l'identificatore per ottenere un accesso rapido alla memoria contenente informazioni sull'istanza specificata.

Molti driver installabili elaborano il secondo parametro del messaggio DRV OPEN, offrendo al sistema e alle applicazioni lo strumento per inviare informazioni aggiuntive al driver all'apertura di \_ un'istanza. Il parametro può essere un singolo valore o un indirizzo di una struttura contenente un set di valori. Durante l'elaborazione di DRV OPEN, il driver controlla il parametro per determinare se si tratta di un valore e usa i valori specificati, se presenti, per completare la creazione \_ dell'istanza.

Il sistema invia un [**messaggio DRV \_ CLOSE**](drv-close.md) ogni volta che un'istanza viene chiusa. L'handle di istanza inviato con il messaggio identifica l'istanza da chiudere. Quando l'ultima istanza rimanente viene chiusa, il sistema invia i messaggi \_ DRV CLOSE, [**DRV \_ DISABLE**](drv-disable.md)e [**DRV \_ FREE**](drv-free.md) nell'ordine indicato. Il messaggio DRV CLOSE indica al driver di chiudere l'istanza e i messaggi DRV DISABLE e DRV FREE notificano al driver che è ora disabilitato e verrà immediatamente liberato \_ \_ dalla \_ memoria.

Quando si elabora il messaggio DRV CLOSE, il driver libera in genere \_ qualsiasi memoria o risorsa allocata per l'istanza. Quando si elabora il messaggio DRV DISABLE, il driver inserisce l'hardware in uno stato inattivo, che può includere la \_ rimozione dei gestori di interrupt. Durante l'elaborazione del messaggio DRV FREE, il driver libera la memoria o le \_ risorse ancora allocate.

I driver installabili non sono necessari per supportare più istanze. Un driver può impedire la creazione di qualsiasi istanza restituisce zero per il [**messaggio DRV \_ OPEN.**](drv-open.md)

 

 




