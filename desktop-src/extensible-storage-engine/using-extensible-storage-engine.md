---
description: 'Altre informazioni su: uso di Extensible Storage Engine'
title: Uso di Extensible Storage Engine
TOCTitle: Using Extensible Storage Engine
ms:assetid: d0249519-4c7c-49c1-9c80-b3cae2537d61
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294096(v=EXCHG.10)
ms:contentKeyID: 32765711
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 636c3fa96692b8c48f9a175b5fa7d34c53314e1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309653"
---
# <a name="using-extensible-storage-engine"></a><span data-ttu-id="672b3-103">Uso di Extensible Storage Engine</span><span class="sxs-lookup"><span data-stu-id="672b3-103">Using Extensible Storage Engine</span></span>


<span data-ttu-id="672b3-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="672b3-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="using-extensible-storage-engine"></a><span data-ttu-id="672b3-105">Uso di Extensible Storage Engine</span><span class="sxs-lookup"><span data-stu-id="672b3-105">Using Extensible Storage Engine</span></span>

<span data-ttu-id="672b3-106">In questa sezione vengono fornite informazioni generali sull'utilizzo delle parti seguenti dell'API ESE.</span><span class="sxs-lookup"><span data-stu-id="672b3-106">This section contains general information about how to use the following parts of the ESE API.</span></span>

  - [<span data-ttu-id="672b3-107">Colonne</span><span class="sxs-lookup"><span data-stu-id="672b3-107">Columns</span></span>](./columns.md)

  - [<span data-ttu-id="672b3-108">Indicizzazione nella tabella</span><span class="sxs-lookup"><span data-stu-id="672b3-108">Indexing in the Table</span></span>](./indexing-in-the-table.md)

  - [<span data-ttu-id="672b3-109">Creazione di database</span><span class="sxs-lookup"><span data-stu-id="672b3-109">Creating Databases</span></span>](./creating-databases.md)

  - [<span data-ttu-id="672b3-110">Transazioni</span><span class="sxs-lookup"><span data-stu-id="672b3-110">Transactions</span></span>](./transactions.md)

  - [<span data-ttu-id="672b3-111">Errori ESE</span><span class="sxs-lookup"><span data-stu-id="672b3-111">ESE Errors</span></span>](./extensible-storage-engine-errors.md)

  - [<span data-ttu-id="672b3-112">File ESE</span><span class="sxs-lookup"><span data-stu-id="672b3-112">ESE Files</span></span>](./extensible-storage-engine-files.md)

<span data-ttu-id="672b3-113">I file di origine del programma devono includere il file di intestazione esent. h per accedere ai prototipi di funzione e alle definizioni di struttura per l'API del motore di archiviazione estendibile.</span><span class="sxs-lookup"><span data-stu-id="672b3-113">Your program source files should include the esent.h header file to access function prototypes and structure definitions for the Extensible Storage Engine API.</span></span> <span data-ttu-id="672b3-114">Gli sviluppatori possono utilizzare il file di libreria esent. lib per compilare applicazioni che utilizzano l'API del motore di archiviazione estendibile.</span><span class="sxs-lookup"><span data-stu-id="672b3-114">Developers can use the esent.lib library file to build applications that use the Extensible Storage Engine API.</span></span> <span data-ttu-id="672b3-115">In fase di esecuzione, le applicazioni si collegano al esent.dll.</span><span class="sxs-lookup"><span data-stu-id="672b3-115">At runtime, applications link to the esent.dll.</span></span>
