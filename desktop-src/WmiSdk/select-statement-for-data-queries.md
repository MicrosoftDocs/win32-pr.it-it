---
description: Descrive l'istruzione SELECT per una query di dati.
ms.assetid: 9c1a164e-4728-4fbe-8a49-b571005a46ec
ms.tgt_platform: multiple
title: Istruzione SELECT per le query di dati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06905cfd9ef5e55022b3fc2275ed705a670a0ecc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309883"
---
# <a name="select-statement-for-data-queries"></a><span data-ttu-id="a4ec8-103">Istruzione SELECT per le query di dati</span><span class="sxs-lookup"><span data-stu-id="a4ec8-103">SELECT Statement for Data Queries</span></span>

<span data-ttu-id="a4ec8-104">È possibile utilizzare un'ampia gamma di istruzioni SELECT per eseguire una query per ottenere informazioni.</span><span class="sxs-lookup"><span data-stu-id="a4ec8-104">You can use a variety of SELECT statements to query for information.</span></span> <span data-ttu-id="a4ec8-105">Le istruzioni possono essere istruzioni di base oppure possono essere più restrittive per limitare il set di risultati restituito dalla query.</span><span class="sxs-lookup"><span data-stu-id="a4ec8-105">The statements can be basic statements or they can be more restrictive to narrow the result set that is returned from the query.</span></span>

<span data-ttu-id="a4ec8-106">L'esempio seguente è un'istruzione SELECT di base utilizzata per eseguire una query per i dati.</span><span class="sxs-lookup"><span data-stu-id="a4ec8-106">The following example is a basic SELECT statement that is used to query for data.</span></span>


```sql
SELECT * FROM Class
```



<span data-ttu-id="a4ec8-107">Questa istruzione restituisce le istanze della classe specificata e delle relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="a4ec8-107">This statement returns instances of the specified class and any of its subclasses.</span></span> <span data-ttu-id="a4ec8-108">Sono incluse tutte le proprietà di sistema e definite dall'utente per le classi.</span><span class="sxs-lookup"><span data-stu-id="a4ec8-108">All of the system and user-defined properties for the classes are included.</span></span> <span data-ttu-id="a4ec8-109">Se una proprietà di sistema non è pertinente per una determinata query, contiene **null**.</span><span class="sxs-lookup"><span data-stu-id="a4ec8-109">If a system property is not relevant for a particular query, it contains **NULL**.</span></span>

<span data-ttu-id="a4ec8-110">È possibile utilizzare diverse tecniche per ridurre la larghezza di banda necessaria per recuperare il set di risultati, se l'esecuzione della query comporta un sovraccarico eccessivo e l'utente è interessato solo a un sottoinsieme delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="a4ec8-110">You can use several techniques to reduce the bandwidth required to retrieve the result set, if the execution of the query results in too much overhead and the user is only interested in a subset of the properties.</span></span> <span data-ttu-id="a4ec8-111">In primo luogo, le query possono sostituire l'asterisco con le proprietà desiderate.</span><span class="sxs-lookup"><span data-stu-id="a4ec8-111">First, queries can replace the asterisk with the desired properties.</span></span>

<span data-ttu-id="a4ec8-112">Nell'esempio seguente viene illustrato come eseguire una query per proprietà specifiche.</span><span class="sxs-lookup"><span data-stu-id="a4ec8-112">The following example shows how to query for specific properties.</span></span>


```sql
SELECT property_1, property_2, property_3 FROM class
```



<span data-ttu-id="a4ec8-113">Il set di risultati include tutte le proprietà di sistema e le proprietà non di sistema specificate.</span><span class="sxs-lookup"><span data-stu-id="a4ec8-113">The result set includes all system properties and the specified nonsystem properties.</span></span>

<span data-ttu-id="a4ec8-114">Un'altra tecnica per limitare l'ambito del set di risultati di una query consiste nell'usare la proprietà di sistema della [**\_ \_ classe**](wmi-system-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="a4ec8-114">Another technique for narrowing the scope of a query's result set is to use the [**\_\_CLASS**](wmi-system-properties.md) system property.</span></span> <span data-ttu-id="a4ec8-115">Per impostazione predefinita, le query restituiscono tutte le istanze della classe specificata e delle relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="a4ec8-115">Queries by default return all instances of the specified class and its subclasses.</span></span> <span data-ttu-id="a4ec8-116">È possibile utilizzare la proprietà di sistema della **\_ \_ classe** per richiedere solo istanze della classe specificata, escluse le sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="a4ec8-116">You can use the **\_\_CLASS** system property to request only instances of the specified class, excluding its subclasses.</span></span>

<span data-ttu-id="a4ec8-117">Nell'esempio seguente viene illustrato come utilizzare la proprietà di sistema della [**\_ \_ classe**](wmi-system-properties.md) in una clausola WHERE.</span><span class="sxs-lookup"><span data-stu-id="a4ec8-117">The following example shows how to use the [**\_\_CLASS**](wmi-system-properties.md) system property in a WHERE clause.</span></span>


```sql
SELECT * FROM Device WHERE __CLASS = "Device"
```



<span data-ttu-id="a4ec8-118">È inoltre possibile utilizzare la proprietà di sistema della [**\_ \_ classe**](wmi-system-properties.md) per limitare il set di risultati a istanze di sottoclassi specifiche.</span><span class="sxs-lookup"><span data-stu-id="a4ec8-118">You can also use the [**\_\_CLASS**](wmi-system-properties.md) system property to restrict the result set to instances of particular subclasses.</span></span>

<span data-ttu-id="a4ec8-119">Nell'esempio seguente viene illustrato come limitare il set di risultati a istanze di sottoclassi specifiche.</span><span class="sxs-lookup"><span data-stu-id="a4ec8-119">The following example shows how to restrict the result set to instances of particular subclasses.</span></span>


```sql
SELECT * FROM Device WHERE __CLASS = "Modem" OR __CLASS = "Keyboard"
```



> [!Note]  
> <span data-ttu-id="a4ec8-120">Se si crea una query con un percorso non valido per un oggetto incorporato, la query non restituisce un errore o i risultati.</span><span class="sxs-lookup"><span data-stu-id="a4ec8-120">If you construct a query with an invalid path for an embedded object, your query does not return an error or any results.</span></span>

 

<span data-ttu-id="a4ec8-121">Nell'esempio seguente viene restituita un'istanza di **MainClass**, supponendo che esista un'istanza di **MainClass** contenente l'oggetto incorporato **EmbedObj** con una proprietà **P \_ UInt32** uguale a "70011".</span><span class="sxs-lookup"><span data-stu-id="a4ec8-121">The following example returns an instance of **MainClass**, assuming that an instance of **MainClass** exists containing the embedded object **EmbedObj** with a property **P\_Uint32** that is equal to "70011".</span></span>


```sql
SELECT * FROM MainClass WHERE EmbedObj.P_Uint32 = 70011
```



<span data-ttu-id="a4ec8-122">Nell'esempio seguente non viene restituito alcun risultato e non viene restituito un errore, a condizione che l'oggetto incorporato **EmbedObj** nell'istanza di **MainClass** non disponga di una proprietà non **valida**.</span><span class="sxs-lookup"><span data-stu-id="a4ec8-122">The following example returns no results and does not return an error, assuming that the embedded object **EmbedObj** in the instance of **MainClass** does not have a property **INVALID**.</span></span>


```sql
SELECT * FROM MainClass WHERE StrongEmbedObj.INVALID = 70011
```



 

 



