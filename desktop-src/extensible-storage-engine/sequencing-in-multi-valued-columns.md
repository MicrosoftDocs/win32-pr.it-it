---
description: 'Altre informazioni su: sequenziazione in colonne multivalore'
title: Sequenziazione in colonne multivalore
TOCTitle: Sequencing in Multi-Valued Columns
ms:assetid: 825a1e51-6b18-4bcf-87f2-4223f302186c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269319(v=EXCHG.10)
ms:contentKeyID: 32765609
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 54f4bd7734cb8c1bf5a87eb444c3205d89f4a6ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104555725"
---
# <a name="sequencing-in-multi-valued-columns"></a><span data-ttu-id="e7be3-103">Sequenziazione in colonne multivalore</span><span class="sxs-lookup"><span data-stu-id="e7be3-103">Sequencing in Multi-Valued Columns</span></span>


<span data-ttu-id="e7be3-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="e7be3-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="sequencing-in-multi-valued-columns"></a><span data-ttu-id="e7be3-105">Sequenziazione in colonne multivalore</span><span class="sxs-lookup"><span data-stu-id="e7be3-105">Sequencing in Multi-Valued Columns</span></span>

<span data-ttu-id="e7be3-106">I valori in una colonna multivalore sono identificati da un numero di indice denominato *itagSequence*.</span><span class="sxs-lookup"><span data-stu-id="e7be3-106">The values in a multi-valued column are identified by an index number called the *itagSequence*.</span></span> <span data-ttu-id="e7be3-107">Questo numero è un riferimento a un singolo valore della colonna.</span><span class="sxs-lookup"><span data-stu-id="e7be3-107">This number is a reference to a single value of the column.</span></span> <span data-ttu-id="e7be3-108">Questo numero viene utilizzato quando i nuovi valori vengono impostati, recuperati o enumerati nella colonna.</span><span class="sxs-lookup"><span data-stu-id="e7be3-108">This number is used when new values are set, retrieved, or enumerated in the column.</span></span> <span data-ttu-id="e7be3-109">*ItagSequence* viene utilizzato in varie strutture, tra cui:</span><span class="sxs-lookup"><span data-stu-id="e7be3-109">The *itagSequence* is used in various structures, including:</span></span>

  - [<span data-ttu-id="e7be3-110">JET_RETINFO</span><span class="sxs-lookup"><span data-stu-id="e7be3-110">JET_RETINFO</span></span>](./jet-retinfo-structure.md)

  - [<span data-ttu-id="e7be3-111">JET_SETINFO</span><span class="sxs-lookup"><span data-stu-id="e7be3-111">JET_SETINFO</span></span>](./jet-setinfo-structure.md)

  - [<span data-ttu-id="e7be3-112">JET_SETCOLUMN</span><span class="sxs-lookup"><span data-stu-id="e7be3-112">JET_SETCOLUMN</span></span>](./jet-setcolumn-structure.md)

  - [<span data-ttu-id="e7be3-113">JET_RETRIEVECOLUMN</span><span class="sxs-lookup"><span data-stu-id="e7be3-113">JET_RETRIEVECOLUMN</span></span>](./jet-retrievecolumn-structure.md)

  - [<span data-ttu-id="e7be3-114">JET_ENUMCOLUMNVALUE</span><span class="sxs-lookup"><span data-stu-id="e7be3-114">JET_ENUMCOLUMNVALUE</span></span>](./jet-enumcolumnvalue-structure.md)

<span data-ttu-id="e7be3-115">Questo *itagSequence* inizia da 1 per ogni valore nella colonna multivalore.</span><span class="sxs-lookup"><span data-stu-id="e7be3-115">This *itagSequence* starts at 1 for every value in the multi-valued column.</span></span> <span data-ttu-id="e7be3-116">Il numero di sequenza viene aumentato quando vengono aggiunti nuovi valori alla colonna.</span><span class="sxs-lookup"><span data-stu-id="e7be3-116">The sequence number is increased when new values are added to the column.</span></span> <span data-ttu-id="e7be3-117">L'impostazione di un valore in una colonna con un valore di *itagSequence* pari a 0 indica che il valore deve essere aggiunto al set di valori già presenti in tale colonna.</span><span class="sxs-lookup"><span data-stu-id="e7be3-117">Setting a value in a column with an *itagSequence* of 0 indicates that the value is to be appended to the set of values already in that column.</span></span> <span data-ttu-id="e7be3-118">L'utilizzo di un *itagSequence* maggiore del numero di valori attualmente impostati per una colonna avrà lo stesso effetto.</span><span class="sxs-lookup"><span data-stu-id="e7be3-118">Using an *itagSequence* greater than the number of values currently set for a column will have the same effect.</span></span> <span data-ttu-id="e7be3-119">Se si specifica il valore di *itagSequence* di un valore esistente, questo valore non viene inserito.</span><span class="sxs-lookup"><span data-stu-id="e7be3-119">Specifying the *itagSequence* of an existing value will overwrite that value, not insert a new one.</span></span> <span data-ttu-id="e7be3-120">Se si imposta un valore esistente su NULL, il valore viene rimosso dal set di valori già presenti in tale colonna.</span><span class="sxs-lookup"><span data-stu-id="e7be3-120">Setting an existing value to NULL will remove that value from the set of values already in that column.</span></span> <span data-ttu-id="e7be3-121">In questo modo, tutti i valori successivi nella colonna verranno spostati di uno slot, in modo che il successivo accesso a tali valori da parte di *itagSequence* sarà di un numero uno inferiore rispetto a quello usato in precedenza.</span><span class="sxs-lookup"><span data-stu-id="e7be3-121">This will move all the subsequent values in the column down by one slot such that subsequent access to those values by *itagSequence* will be by a number one less than what was previously used.</span></span>

<span data-ttu-id="e7be3-122">Nel diagramma seguente viene illustrato un *itagSequence* in una colonna multivalore.</span><span class="sxs-lookup"><span data-stu-id="e7be3-122">The following diagram shows an *itagSequence* in a multi-valued column.</span></span> <span data-ttu-id="e7be3-123">La colonna denominata ColA include tre voci: val1, val2 e Val3 con *itagSequence* rispettivamente 1, 2 e 3.</span><span class="sxs-lookup"><span data-stu-id="e7be3-123">The column named ColA has three entries: Val1, Val2 and Val3 with *itagSequence* of 1, 2, and 3 respectively.</span></span>

<span data-ttu-id="e7be3-124">![ESE_Documentation_TagFixVar](images/Gg269304.ESE_Documentation_TagFixVar(EXCHG.10).gif "ESE_Documentation_TagFixVar")</span><span class="sxs-lookup"><span data-stu-id="e7be3-124">![ESE_Documentation_TagFixVar](images/Gg269304.ESE_Documentation_TagFixVar(EXCHG.10).gif "ESE_Documentation_TagFixVar")</span></span>
