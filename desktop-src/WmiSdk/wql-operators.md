---
description: Vengono descritti gli operatori WQL utilizzati nella clausola WHERE o nell'istruzione SELECT.
ms.assetid: a62de66d-d5ba-49a1-8262-bfa10ac2db75
ms.tgt_platform: multiple
title: Operatori WQL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f5cc37d03884a3609abf3f76d2c78ba22b3c9f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313156"
---
# <a name="wql-operators"></a><span data-ttu-id="8683d-103">Operatori WQL</span><span class="sxs-lookup"><span data-stu-id="8683d-103">WQL Operators</span></span>

<span data-ttu-id="8683d-104">Il linguaggio WQL (Strumentazione gestione Windows Query Language) supporta un set di operatori standard utilizzati nella [clausola WHERE](where-clause.md) di un'istruzione SELECT, come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="8683d-104">The Windows Management Instrumentation Query Language (WQL) supports a set of standard operators that are used in the [WHERE clause](where-clause.md) of a SELECT statement, as follows.</span></span>



| <span data-ttu-id="8683d-105">Operatore</span><span class="sxs-lookup"><span data-stu-id="8683d-105">Operator</span></span>       | <span data-ttu-id="8683d-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8683d-106">Description</span></span>              |
|----------------|--------------------------|
| =              | <span data-ttu-id="8683d-107">Uguale a</span><span class="sxs-lookup"><span data-stu-id="8683d-107">Equal to</span></span>                 |
| <           | <span data-ttu-id="8683d-108">Minore di</span><span class="sxs-lookup"><span data-stu-id="8683d-108">Less than</span></span>                |
| >           | <span data-ttu-id="8683d-109">Maggiore di</span><span class="sxs-lookup"><span data-stu-id="8683d-109">Greater than</span></span>             |
| <=          | <span data-ttu-id="8683d-110">Minore o uguale a</span><span class="sxs-lookup"><span data-stu-id="8683d-110">Less than or equal to</span></span>    |
| >=          | <span data-ttu-id="8683d-111">Maggiore o uguale a</span><span class="sxs-lookup"><span data-stu-id="8683d-111">Greater than or equal to</span></span> |
| <span data-ttu-id="8683d-112">! = o <></span><span class="sxs-lookup"><span data-stu-id="8683d-112">!= or <></span></span> | <span data-ttu-id="8683d-113">Diverso da</span><span class="sxs-lookup"><span data-stu-id="8683d-113">Not equal to</span></span>             |



 

<span data-ttu-id="8683d-114">Sono disponibili alcuni operatori aggiuntivi specifici di WQL: è, non è, ISA e LIKE.</span><span class="sxs-lookup"><span data-stu-id="8683d-114">There are a few additional WQL-specific operators: IS, IS NOT, ISA, and LIKE.</span></span> <span data-ttu-id="8683d-115">Gli operatori IS e IS NOT sono validi nella clausola WHERE solo se la costante è **null**.</span><span class="sxs-lookup"><span data-stu-id="8683d-115">The IS and IS NOT operators are valid in the WHERE clause only if the constant is **NULL**.</span></span> <span data-ttu-id="8683d-116">Ad esempio, le query seguenti sono valide:</span><span class="sxs-lookup"><span data-stu-id="8683d-116">For example, the following queries are valid:</span></span>


```sql
SELECT * FROM Win32_LogicalDisk WHERE FileSystem IS NULL
SELECT * FROM Win32_LogicalDisk WHERE FileSystem IS NOT NULL
```



<span data-ttu-id="8683d-117">Le query seguenti mostrano usi non validi di IS e NOT:</span><span class="sxs-lookup"><span data-stu-id="8683d-117">The following queries show invalid uses of IS and IS NOT:</span></span>


```sql
SELECT * FROM Win32_LogicalDisk WHERE DriveType IS 5
SELECT * FROM Win32_LogicalDisk WHERE FileSystem IS NOT "NTFS"
```



<span data-ttu-id="8683d-118">L'operatore ISA viene utilizzato nella clausola WHERE di query di dati e di eventi per testare oggetti incorporati per una gerarchia di classi.</span><span class="sxs-lookup"><span data-stu-id="8683d-118">The ISA operator is used in the WHERE clause of data and event queries to test embedded objects for a class hierarchy.</span></span> <span data-ttu-id="8683d-119">L'operatore ISA Elimina la necessità di tenere traccia delle nuove classi derivate quando si richiede una gerarchia di classi.</span><span class="sxs-lookup"><span data-stu-id="8683d-119">The ISA operator eliminates the need for keeping track of newly derived classes when requesting a hierarchy of classes.</span></span> <span data-ttu-id="8683d-120">Quando si utilizza ISA, le sottoclassi appena create e quelle esistenti della classe richiesta vengono incluse automaticamente nel set di risultati.</span><span class="sxs-lookup"><span data-stu-id="8683d-120">When you use ISA, newly created and existing subclasses of the requested class are automatically included in the result set.</span></span>

<span data-ttu-id="8683d-121">Per ulteriori informazioni sulla sintassi e sull'utilizzo di questo operatore, vedere gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="8683d-121">For more information about the syntax and use of this operator, see the following topics:</span></span>

-   [<span data-ttu-id="8683d-122">Operatore ISA per query di dati</span><span class="sxs-lookup"><span data-stu-id="8683d-122">ISA Operator for Data Queries</span></span>](isa-operator-for-data-queries.md)
-   [<span data-ttu-id="8683d-123">Operatore ISA per le query di eventi</span><span class="sxs-lookup"><span data-stu-id="8683d-123">ISA Operator for Event Queries</span></span>](isa-operator-for-event-queries.md)
-   [<span data-ttu-id="8683d-124">Operatore ISA per query dello schema</span><span class="sxs-lookup"><span data-stu-id="8683d-124">ISA Operator for Schema Queries</span></span>](isa-operator-for-schema-queries.md)

<span data-ttu-id="8683d-125">L'operatore LIKE è valido nella clausola WHERE e viene usato per determinare se una determinata stringa di caratteri corrisponde a un modello specificato.</span><span class="sxs-lookup"><span data-stu-id="8683d-125">The LIKE operator is valid in the WHERE clause and is used to determine whether a given character string matches a specified pattern.</span></span> <span data-ttu-id="8683d-126">Ad esempio, la query seguente restituisce tutte le istanze delle \_ classi Win32.</span><span class="sxs-lookup"><span data-stu-id="8683d-126">For example, the following query returns all instances of Win32\_ classes.</span></span>


```sql
SELECT * FROM Meta_Class WHERE __Class LIKE "%Win32%"
```



<span data-ttu-id="8683d-127">Per ulteriori informazioni sulla sintassi e sull'utilizzo di questo operatore, vedere [operatore like](like-operator.md).</span><span class="sxs-lookup"><span data-stu-id="8683d-127">For more information about the syntax and use of this operator, see [LIKE Operator](like-operator.md).</span></span>

 

 



