---
title: Convenzioni di denominazione degli oggetti di archiviazione
description: Gli oggetti di archiviazione e di flusso vengono denominati in base a un set di convenzioni.
ms.assetid: 72e87c6a-cce5-4456-8336-c657e65c0a34
keywords:
- Archivio strutturato Strctd STG, nozioni fondamentali, convenzioni di denominazione degli oggetti di archiviazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2e828674f4165bdb54dc2ec06748ab4165e75e2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395462"
---
# <a name="storage-object-naming-conventions"></a>Convenzioni di denominazione degli oggetti di archiviazione

Gli oggetti di archiviazione e di flusso vengono denominati in base a un set di convenzioni.

Il nome di un oggetto di archiviazione radice è il nome effettivo del file nel file system sottostante. È conforme alle convenzioni e alle restrizioni imposte dal file system. Le stringhe di nomi di file passate a funzioni e metodi correlati all'archiviazione vengono passate, non interpretate e non modificate, al file system.

Il nome di un elemento annidato contenuto in un oggetto di archiviazione è gestito dall'implementazione dell'oggetto di archiviazione specifico. Tutte le implementazioni di oggetti di archiviazione devono supportare i nomi di elemento annidati di 32 caratteri, incluso il terminatore **null** , sebbene alcune implementazioni possano supportare nomi più lunghi. Indica se l'oggetto di archiviazione esegue qualsiasi conversione del case in modo definito dall'implementazione. Di conseguenza, le applicazioni che definiscono i nomi degli elementi devono scegliere nomi accettabili indipendentemente dal fatto che venga eseguita o meno la conversione del case. L'implementazione COM dei file composti supporta nomi con una lunghezza massima di 32 caratteri e non esegue alcuna conversione di maiuscole e minuscole.

 

 




