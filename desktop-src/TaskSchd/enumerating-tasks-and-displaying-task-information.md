---
title: Enumerazione di attività e visualizzazione di informazioni sulle attività
description: La visualizzazione di informazioni su un'attività, ad esempio il nome, lo stato o l'ultima esecuzione dell'attività, viene eseguita enumerando le attività in esecuzione o le attività in una cartella di attività e visualizzando le informazioni desiderate.
ms.assetid: a0305089-89ff-42b7-b3f1-99a6484d2e5e
keywords:
- enumerazione di attività Utilità di pianificazione
- Utilità di pianificazione esempi Utilità di pianificazione , enumerazione delle attività
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4859122218ead4d18c1f9e83de0f55ce9373306cd2762e5608cf4d1841019b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002449"
---
# <a name="enumerating-tasks-and-displaying-task-information"></a>Enumerazione di attività e visualizzazione di informazioni sulle attività

La visualizzazione di informazioni su un'attività, ad esempio il nome, lo stato o l'ultima esecuzione dell'attività, viene eseguita enumerando le attività in esecuzione o le attività in una cartella di attività e visualizzando le informazioni desiderate.

## <a name="accessing-properties-of-registered-tasks"></a>Accesso alle proprietà delle attività registrate

Per visualizzare il valore della proprietà di un'attività registrata, è necessario connettersi al servizio Utilità di pianificazione e quindi ottenere un'istanza della cartella delle attività contenente le attività su cui si desiderano informazioni. Si ottiene quindi una raccolta di tutte le attività registrate nella cartella delle attività. È quindi possibile enumerare ogni attività registrata e ottenere e visualizzare un valore di proprietà per ogni attività.

## <a name="accessing-properties-of-running-tasks"></a>Accesso alle proprietà delle attività in esecuzione

Per visualizzare il valore della proprietà di un'attività in esecuzione, è necessario connettersi al servizio Utilità di pianificazione e quindi ottenere una raccolta di tutte le attività in esecuzione (incluse o escluse le attività nascoste). Enumerare quindi ogni attività in esecuzione e ottenere e visualizzare un valore di proprietà per ogni attività.

## <a name="example"></a>Esempio

Gli esempi seguenti enumerano le attività e visualizzano il nome e lo stato delle attività:

-   [Visualizzazione di nomi e stati delle attività (scripting)](displaying-task-names-and-state--scripting-.md)
-   [Visualizzazione dei nomi e dello stato delle attività (C++)](displaying-task-names-and-state--c---.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso del Utilità di pianificazione](using-the-task-scheduler.md)
</dt> </dl>

 

 




