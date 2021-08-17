---
description: Il processo di creazione di una richiesta di certificato comporta la raccolta di determinate informazioni dal richiedente.
ms.assetid: b03efa83-e255-4427-a796-63d5841664a9
title: Creazione della richiesta di certificato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 607ebbfd5d230c216c2b7ebc4d3b217e1f8c0d2a375d39cdd6b311ec145be361
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117768882"
---
# <a name="creating-the-certificate-request"></a>Creazione della richiesta di certificato

Il processo di creazione di una richiesta di certificato comporta la raccolta di determinate informazioni dal richiedente. In genere, questa operazione viene eseguita tramite una sorta di interfaccia utente, anche se le informazioni potrebbero essere prese direttamente da un database senza la necessità di un'interfaccia utente. Il livello di informazioni necessarie viene impostato dai criteri [*dell'autorità di certificazione*](../secgloss/c-gly.md) (CA).

Di seguito è riportato un esempio delle informazioni necessarie:

-   Nome comune
-   Nome unità
-   Nome società
-   City
-   State
-   Paese/Area geografica

> [!Note]  
> L'interfaccia è progettata per effettuare una singola richiesta per ogni istanza di xenroll. Per creare ogni richiesta di certificato, è necessario creare un'istanza xenroll [*separata.*](../secgloss/c-gly.md)

 

Per informazioni su come usare il controllo di registrazione certificati per richiedere un certificato in linguaggi di programmazione specifici, vedere gli argomenti seguenti:

-   [Esempio di richiesta in C++](request-sample-in-c-.md)
-   [Esempio di richiesta in VBScript](request-sample-in-vbscript.md)

 

 
