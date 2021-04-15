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
# <a name="storage-object-naming-conventions"></a><span data-ttu-id="37717-104">Convenzioni di denominazione degli oggetti di archiviazione</span><span class="sxs-lookup"><span data-stu-id="37717-104">Storage Object Naming Conventions</span></span>

<span data-ttu-id="37717-105">Gli oggetti di archiviazione e di flusso vengono denominati in base a un set di convenzioni.</span><span class="sxs-lookup"><span data-stu-id="37717-105">Storage and stream objects are named according to a set of conventions.</span></span>

<span data-ttu-id="37717-106">Il nome di un oggetto di archiviazione radice è il nome effettivo del file nel file system sottostante.</span><span class="sxs-lookup"><span data-stu-id="37717-106">The name of a root storage object is the actual name of the file in the underlying file system.</span></span> <span data-ttu-id="37717-107">È conforme alle convenzioni e alle restrizioni imposte dal file system.</span><span class="sxs-lookup"><span data-stu-id="37717-107">It conforms to the conventions and restrictions that the file system imposes.</span></span> <span data-ttu-id="37717-108">Le stringhe di nomi di file passate a funzioni e metodi correlati all'archiviazione vengono passate, non interpretate e non modificate, al file system.</span><span class="sxs-lookup"><span data-stu-id="37717-108">File name strings passed to storage-related methods and functions are passed on, uninterpreted and unchanged, to the file system.</span></span>

<span data-ttu-id="37717-109">Il nome di un elemento annidato contenuto in un oggetto di archiviazione è gestito dall'implementazione dell'oggetto di archiviazione specifico.</span><span class="sxs-lookup"><span data-stu-id="37717-109">The name of a nested element contained within a storage object is managed by the implementation of the particular storage object.</span></span> <span data-ttu-id="37717-110">Tutte le implementazioni di oggetti di archiviazione devono supportare i nomi di elemento annidati di 32 caratteri, incluso il terminatore **null** , sebbene alcune implementazioni possano supportare nomi più lunghi.</span><span class="sxs-lookup"><span data-stu-id="37717-110">All implementations of storage objects must support nested element names 32 characters in length (including the **NULL** terminator), although some implementations might support longer names.</span></span> <span data-ttu-id="37717-111">Indica se l'oggetto di archiviazione esegue qualsiasi conversione del case in modo definito dall'implementazione.</span><span class="sxs-lookup"><span data-stu-id="37717-111">Whether the storage object does any case conversion is implementation-defined.</span></span> <span data-ttu-id="37717-112">Di conseguenza, le applicazioni che definiscono i nomi degli elementi devono scegliere nomi accettabili indipendentemente dal fatto che venga eseguita o meno la conversione del case.</span><span class="sxs-lookup"><span data-stu-id="37717-112">As a result, applications that define element names must choose names that are acceptable whether or not case conversion is performed.</span></span> <span data-ttu-id="37717-113">L'implementazione COM dei file composti supporta nomi con una lunghezza massima di 32 caratteri e non esegue alcuna conversione di maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="37717-113">The COM implementation of compound files supports names with a maximum length of 32 characters, and does not perform any case conversion.</span></span>

 

 




