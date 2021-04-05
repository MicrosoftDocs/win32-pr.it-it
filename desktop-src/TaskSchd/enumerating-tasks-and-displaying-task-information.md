---
title: Enumerazione delle attività e visualizzazione delle informazioni sulle attività
description: La visualizzazione delle informazioni su un'attività, ad esempio il nome dell'attività, lo stato o l'ultima esecuzione dell'attività, viene eseguita tramite l'enumerazione delle attività in esecuzione o delle attività in una cartella di attività e la visualizzazione delle informazioni desiderate.
ms.assetid: a0305089-89ff-42b7-b3f1-99a6484d2e5e
keywords:
- Enumerazione delle attività Utilità di pianificazione
- Esempi di Utilità di pianificazione Utilità di pianificazione, enumerazione delle attività
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58e4c1bbad0a1fa8892e38a001ff54e665f0c144
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707279"
---
# <a name="enumerating-tasks-and-displaying-task-information"></a>Enumerazione delle attività e visualizzazione delle informazioni sulle attività

La visualizzazione delle informazioni su un'attività, ad esempio il nome dell'attività, lo stato o l'ultima esecuzione dell'attività, viene eseguita tramite l'enumerazione delle attività in esecuzione o delle attività in una cartella di attività e la visualizzazione delle informazioni desiderate.

## <a name="accessing-properties-of-registered-tasks"></a>Accesso alle proprietà delle attività registrate

Per visualizzare il valore della proprietà di un'attività registrata, è necessario connettersi al servizio Utilità di pianificazione e quindi ottenere un'istanza della cartella attività che contiene le attività per le quali si desiderano informazioni. Si otterrà quindi una raccolta di tutte le attività registrate nella cartella delle attività. È quindi possibile enumerare ogni attività registrata e ottenere e visualizzare un valore di proprietà per ogni attività.

## <a name="accessing-properties-of-running-tasks"></a>Accesso alle proprietà delle attività in esecuzione

Per visualizzare il valore della proprietà di un'attività in esecuzione, è necessario connettersi al servizio Utilità di pianificazione e quindi ottenere una raccolta di tutte le attività in esecuzione (incluse o escluse le attività nascoste). È quindi possibile enumerare ogni attività in esecuzione e ottenere e visualizzare un valore di proprietà per ogni attività.

## <a name="example"></a>Esempio

Negli esempi seguenti vengono enumerate le attività e vengono visualizzati il nome e lo stato delle attività:

-   [Visualizzazione di nomi e Stati delle attività (scripting)](displaying-task-names-and-state--scripting-.md)
-   [Visualizzazione di nomi e stato delle attività (C++)](displaying-task-names-and-state--c---.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso della Utilità di pianificazione](using-the-task-scheduler.md)
</dt> </dl>

 

 




