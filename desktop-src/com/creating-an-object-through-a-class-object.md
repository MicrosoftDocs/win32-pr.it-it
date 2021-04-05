---
title: Creazione di un oggetto tramite un oggetto classe
description: Creazione di un oggetto tramite un oggetto classe
ms.assetid: cecf21b0-e509-425f-8dd6-ca6b1ac04f5e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38787e7bc32151446cda6ff0a4cfe3f23a0f6eda
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955821"
---
# <a name="creating-an-object-through-a-class-object"></a>Creazione di un oggetto tramite un oggetto classe

Con la crescente importanza delle reti informatiche, è necessario che i client e i server interagiscano in modo semplice ed efficiente, indipendentemente dal fatto che si trovino nello stesso computer o in una rete. Fondamentale per questo è la capacità di un client di avviare un server, creare un'istanza dell'oggetto del server e accedere ai metodi delle interfacce sull'oggetto.

COM fornisce estensioni a questo processo COM di base che lo rendono virtualmente trasparente in una rete. Se un client è in grado di identificare il server tramite il relativo CLSID, chiamando alcune funzioni semplici si consente a COM di eseguire tutte le operazioni di individuazione e avvio del server e di attivazione dell'oggetto. Le sottochiavi nel registro di sistema consentono ai server remoti di registrare il proprio percorso, in modo che il client non richieda tali informazioni. Per le applicazioni che desiderano sfruttare le funzionalità di rete, le funzioni di creazione di oggetti COM consentono una maggiore flessibilità ed efficienza.

Per altre informazioni, vedere i seguenti argomenti:

-   [Oggetti classe COM e CLSID](com-class-objects-and-clsids.md)
-   [Individuazione di un oggetto remoto](locating-a-remote-object.md)
-   [Funzioni di supporto per la creazione di istanze](instance-creation-helper-functions.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Client e server COM](com-clients-and-servers.md)
</dt> </dl>

 

 




