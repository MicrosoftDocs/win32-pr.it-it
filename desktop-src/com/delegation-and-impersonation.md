---
title: Delega e rappresentazione
description: Negli scenari client/server è comune che un server chiami un altro server per eseguire alcune attività per conto di un client. La situazione in cui a un server viene data l'autorità di agire per conto di un client è detta delega.
ms.assetid: 245bff1a-31d3-49ce-847e-c37d0c96f9d1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b00f878c7bc0a37e7d60c246550ff404ed4d0c31312610ab63d1863b34aa52be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117919477"
---
# <a name="delegation-and-impersonation"></a>Delega e rappresentazione

Negli scenari client/server è comune che un server chiami un altro server per eseguire alcune attività per conto di un client. La situazione in cui a un server viene data l'autorità di agire per conto di un client è denominata *delega*.

Dal punto di vista della sicurezza, si verificano due problemi relativi alla delega:

-   Cosa deve essere consentito al server quando agisce per conto del client?
-   Quale identità viene presentata dal server quando chiama altri server per conto di un client?

Per risolvere questi problemi, COM fornisce le funzionalità seguenti. Il client può impostare un *livello di rappresentazione* che determina in quale misura il server potrà fungere da client. Se il client concede al server un'autorità sufficiente, il server può *rappresentare* (fingere di essere) il client. Quando si rappresenta il client, al server viene assegnato l'accesso solo agli oggetti o alle risorse che il client è autorizzato a utilizzare. Il server, che funge da  client, può anche abilitare la clonazione per mascherare la propria identità e proiettare l'identità del client nelle chiamate ad altri componenti COM.

![Diagramma che illustra in che modo il server che funge da client può abilitare la clonazione.](images/172e04f7-568d-450b-9785-2c1a2b40e549.png)

Si consideri lo scenario illustrato nella figura precedente, in cui A e B sono processi in un computer diverso da C. Il processo A chiama B e B chiama C. Il client A imposta il livello di rappresentazione. B imposta la funzionalità di cloaking. Se A imposta un livello di rappresentazione che consente la rappresentazione, B può rappresentare A quando chiama C per conto di A. L'identità presentata per l'elaborazione C sarà l'identità di A o l'identità di B, a seconda che la clonazione sia stata abilitata da B. Se la clonazione è abilitata, l'identità presentata al processo C sarà quella di A. Se la clonazione non è abilitata, l'identità di B verrà presentata a C.

Per altre informazioni, vedere i seguenti argomenti:

-   [Rappresentazione](impersonation.md)
-   [Livelli di rappresentazione](impersonation-levels.md)
-   [Cloaking](cloaking.md)

 

 




