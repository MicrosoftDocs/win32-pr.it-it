---
title: Non considerare attendibile il peer
description: '\ 0034; non considerare attendibile il peer \ 0034; è una regola di sicurezza di base, ma è spesso trascurata.'
ms.assetid: 776c1c99-feb1-415c-9a18-e9bf581bc3ff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4c5c7ba3760e14a66fb4765000c7a6698599b50
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709964"
---
# <a name="do-not-trust-your-peer"></a>Non considerare attendibile il peer

"Non considerare attendibile il peer" è una regola di sicurezza di base, ma è spesso trascurata. Non presupporre che l'altra parte di una comunicazione si comporterà correttamente e non presupporre che il peer superi i dati previsti. MIDL e RPC eseguono alcuni controlli per conto dell'utente, ma non tutti i controlli.

Conoscere l'aspetto dei parametri che viene verificato da MIDL o RPC e quali aspetti è necessario verificare autonomamente. Per gli handle di contesto in/out, ad esempio, RPC verifica che l'handle del contesto non sia un valore non null non valido. Consente valori null e valori validi, ma molti sviluppatori non sono consapevoli del fatto che i valori null sono consentiti. Si tratta di un elemento da controllare.

Anche se in genere si considera attendibile il peer, assicurarsi di non introdurre nuovi percorsi in base ai quali un computer compromesso o un account principale può attaccare altri computer. Si supponga che un utente scelga il suo compleanno come password ed è indovinato da un utente malintenzionato. Anche dopo l'autenticazione delle richieste provenienti dall'utente e l'accesso ai relativi dati, assicurarsi che non esistano vulnerabilità sfruttabili, ad esempio sovraccarichi dello stack che possono consentire a un utente malintenzionato di assumere il controllo del server ed estendere la violazione della sicurezza.

 

 




