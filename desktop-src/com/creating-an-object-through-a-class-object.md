---
title: Creazione di un oggetto tramite un oggetto classe
description: Creazione di un oggetto tramite un oggetto classe
ms.assetid: cecf21b0-e509-425f-8dd6-ca6b1ac04f5e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ea76e8ecb826d8bba6e9f0ea84af894f4632d3d4bb5f41708d84c2f37e416b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119993501"
---
# <a name="creating-an-object-through-a-class-object"></a>Creazione di un oggetto tramite un oggetto classe

Con la crescente importanza delle reti di computer, è diventato necessario che i client e i server interagiscano in modo semplice ed efficiente, indipendentemente dal fatto che risiedano nello stesso computer o in una rete. A tale scopo, un client può avviare un server, creare un'istanza dell'oggetto del server e avere accesso ai metodi delle interfacce nell'oggetto.

COM fornisce estensioni a questo processo COM di base che lo rendono praticamente trasparente in una rete. Se un client è in grado di identificare il server tramite il relativo CLSID, la chiamata di alcune semplici funzioni consente a COM di eseguire tutte le operazioni di individuazione e avvio del server e attivazione dell'oggetto. Le sottochiavi del Registro di sistema consentono ai server remoti di registrare la propria posizione, in modo che il client non richieda queste informazioni. Per le applicazioni che vogliono sfruttare le funzionalità di rete, le funzioni di creazione di oggetti COM offrono maggiore flessibilità ed efficienza.

Per altre informazioni, vedere i seguenti argomenti:

-   [Oggetti classe COM e CLSID](com-class-objects-and-clsids.md)
-   [Individuazione di un oggetto remoto](locating-a-remote-object.md)
-   [Funzioni helper per la creazione di istanze](instance-creation-helper-functions.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Client e server COM](com-clients-and-servers.md)
</dt> </dl>

 

 




