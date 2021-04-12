---
description: L'utilità di pianificazione mantiene una coda di thread eseguibili per ogni livello di priorità.
ms.assetid: 82463d71-9cef-4608-b997-25dc9c1e1c0a
title: Cambi di contesto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7628ee9e659cdbc2369b5f69d25847e8864dbd62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104231523"
---
# <a name="context-switches"></a>Cambi di contesto

L'utilità di pianificazione mantiene una coda di thread eseguibili per ogni livello di priorità. Questi sono noti come *thread pronti*. Quando un processore diventa disponibile, il sistema esegue un *cambio di contesto*. I passaggi in un cambio di contesto sono:

1.  Salva il contesto del thread che ha appena terminato l'esecuzione.
2.  Posizionare il thread che ha appena terminato l'esecuzione alla fine della coda per la relativa priorità.
3.  Trovare la coda con priorità più alta che contiene thread pronti.
4.  Rimuovere il thread all'inizio della coda, caricarne il contesto ed eseguirlo.

Le classi di thread seguenti non sono thread pronti.

-   Thread creati con il flag di creazione \_ sospesa
-   Thread interrotti durante l'esecuzione con la funzione [**SuspendThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-suspendthread) o [**SwitchToThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-switchtothread)
-   Thread in attesa di un oggetto o di un input di sincronizzazione.

Finché i thread sospesi o bloccati diventano pronti per l'esecuzione, l'utilità di pianificazione non alloca alcun tempo del processore, indipendentemente dalla loro priorità.

I motivi più comuni per un cambio di contesto sono i seguenti:

-   Intervallo di tempo trascorso.
-   Un thread con una priorità più alta è diventato pronto per l'esecuzione.
-   È necessario attendere un thread in esecuzione.

Quando un thread in esecuzione deve attendere, cede il resto della sezione di tempo.

 

 
