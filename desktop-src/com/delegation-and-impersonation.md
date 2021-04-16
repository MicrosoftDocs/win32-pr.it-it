---
title: Delega e rappresentazione
description: Negli scenari client/server è normale che un server chiami un altro server per eseguire alcune attività per conto di un client. La situazione in cui un server ha la facoltà di agire per conto di un cliente è detta delega.
ms.assetid: 245bff1a-31d3-49ce-847e-c37d0c96f9d1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 356708008274bdeb2aa80631bec777fbd02fd38d
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/03/2021
ms.locfileid: "104571440"
---
# <a name="delegation-and-impersonation"></a>Delega e rappresentazione

Negli scenari client/server è normale che un server chiami un altro server per eseguire alcune attività per conto di un client. La situazione in cui un server ha la facoltà di agire per conto di un cliente è detta *delega*.

Dal punto di vista della sicurezza, si verificano due problemi relativi alla delega:

-   Cosa può fare il server quando agisce per conto del client?
-   Quale identità viene presentata dal server quando chiama altri server per conto di un client?

Per risolvere questi problemi, COM offre le funzionalità seguenti. Il client può impostare un *livello di rappresentazione* che determina in quale misura il server sarà in grado di fungere da client. Se il client concede un'autorità sufficiente al server, il server può *rappresentare* (fingere) il client. Quando si rappresenta il client, al server viene concesso l'accesso solo agli oggetti o alle risorse che il client è autorizzato a utilizzare. Il server, che funge da client, può anche abilitare il *cloaking* per mascherare la propria identità e proiettare l'identità del client nelle chiamate ad altri componenti com.

![Diagramma che illustra in che modo il server che funge da client può abilitare il mascheramento.](images/172e04f7-568d-450b-9785-2c1a2b40e549.png)

Si consideri lo scenario illustrato nella figura precedente, dove A e B sono processi in un computer diverso da C. elaborare A chiama B e B chiama C. il client A imposta il livello di rappresentazione. B imposta la funzionalità di mascheramento. Se un oggetto imposta un livello di rappresentazione che consente la rappresentazione, B può rappresentare un oggetto quando si chiama C per conto dell'oggetto. L'identità presentata al processo C sarà Identity o B, a seconda che il mascheramento sia stato abilitato da B. Se il mascheramento è abilitato, l'identità presentata al processo C sarà quella di un oggetto. Se il cloaking non è abilitato, l'identità di B verrà visualizzata in C.

Per altre informazioni, vedere i seguenti argomenti:

-   [Rappresentazione](impersonation.md)
-   [Livelli di rappresentazione](impersonation-levels.md)
-   [Cloaking](cloaking.md)

 

 




