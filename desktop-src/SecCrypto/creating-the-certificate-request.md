---
description: Il processo di creazione di una richiesta di certificato comporta la raccolta di determinate informazioni dal richiedente.
ms.assetid: b03efa83-e255-4427-a796-63d5841664a9
title: Creazione della richiesta di certificato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be29a1fbdbaf9fd956150808471086b7d8ca2815
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306466"
---
# <a name="creating-the-certificate-request"></a>Creazione della richiesta di certificato

Il processo di creazione di una richiesta di certificato comporta la raccolta di determinate informazioni dal richiedente. In genere, questa operazione viene eseguita tramite una sorta di interfaccia utente, sebbene le informazioni possano essere ricavate direttamente da un database senza la necessità di un'interfaccia utente. Il livello delle informazioni richieste viene impostato in base ai criteri dell' [*autorità di certificazione*](../secgloss/c-gly.md) (CA).

Un esempio delle informazioni necessarie potrebbe essere il seguente:

-   Nome comune
-   Nome unità
-   Nome società
-   City
-   State
-   Paese/Area geografica

> [!Note]  
> L'interfaccia è progettata per eseguire una singola richiesta per ogni istanza di Xenroll. Per creare ogni [*richiesta di certificato*](../secgloss/c-gly.md), è necessario creare un'istanza di Xenroll distinta.

 

Per informazioni su come usare il controllo di registrazione certificati per richiedere un certificato in linguaggi di programmazione specifici, vedere gli argomenti seguenti:

-   [Esempio di richiesta in C++](request-sample-in-c-.md)
-   [Esempio di richiesta in VBScript](request-sample-in-vbscript.md)

 

 
