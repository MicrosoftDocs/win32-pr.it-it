---
description: Sono disponibili diverse opzioni per il form richiesto da una query quando si esegue una query su una classe di evento contenente oggetti incorporati. I risultati restituiti dalla query variano a seconda del formato della query utilizzata.
ms.assetid: b959a695-be15-4aa7-9368-b840962ae0da
ms.tgt_platform: multiple
title: Esecuzione di query su oggetti incorporati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ed2e13bd9d9dc798891a723a6fed1b1734e1735
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755055"
---
# <a name="querying-embedded-objects"></a><span data-ttu-id="cec2f-104">Esecuzione di query su oggetti incorporati</span><span class="sxs-lookup"><span data-stu-id="cec2f-104">Querying Embedded Objects</span></span>

<span data-ttu-id="cec2f-105">Sono disponibili diverse opzioni per il form richiesto da una query quando si esegue una query su una classe di evento contenente oggetti incorporati.</span><span class="sxs-lookup"><span data-stu-id="cec2f-105">You have several options as to the form a query takes when querying an event class that contains embedded objects.</span></span> <span data-ttu-id="cec2f-106">I risultati restituiti dalla query variano a seconda del formato della query utilizzata.</span><span class="sxs-lookup"><span data-stu-id="cec2f-106">The results returned by the query vary, depending on the form of the query you use.</span></span>

## <a name="class-definitions"></a><span data-ttu-id="cec2f-107">Definizioni di classe</span><span class="sxs-lookup"><span data-stu-id="cec2f-107">Class Definitions</span></span>

<span data-ttu-id="cec2f-108">Nell'esempio seguente vengono illustrate le definizioni di classe utilizzate per le query WQL in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="cec2f-108">The following example shows the class definitions that are used for the WQL queries in this topic.</span></span>

``` syntax
class MyClass
{
   string Prop1;
   string Prop2;
};

class MyEvent : __ExtrinsicEvent
{
   MyClass E1;
   MyClass E2;
};
```

## <a name="examples"></a><span data-ttu-id="cec2f-109">Esempio</span><span class="sxs-lookup"><span data-stu-id="cec2f-109">Examples</span></span>

<span data-ttu-id="cec2f-110">La query seguente restituisce entrambe le classi incorporate, **E1** ed **E2**, ognuna con **Prop1** e **prop2** popolate con i dati.</span><span class="sxs-lookup"><span data-stu-id="cec2f-110">The following query returns both embedded classes, **E1** and **E2**, each having **Prop1** and **Prop2** populated with data.</span></span>

`SELECT * FROM MyEvent`

<span data-ttu-id="cec2f-111">La query seguente restituisce l'oggetto incorporato **E1** , ma senza **Prop1** né **prop2** popolato con i dati.</span><span class="sxs-lookup"><span data-stu-id="cec2f-111">The following query returns the **E1** embedded object, but with neither **Prop1** nor **Prop2** populated with data.</span></span>

`SELECT E1 FROM MyEvent`

<span data-ttu-id="cec2f-112">La query seguente restituisce la classe incorporata **E1** solo con **Prop1** popolati con i dati.</span><span class="sxs-lookup"><span data-stu-id="cec2f-112">The following query returns the embedded class **E1** with only **Prop1** populated with data.</span></span>

`SELECT E1.Prop1 FROM MyEvent`

<span data-ttu-id="cec2f-113">La query seguente restituisce entrambe le classi incorporate, **E1** ed **E2**, ognuna con **Prop1** e **prop2** popolate con i dati.</span><span class="sxs-lookup"><span data-stu-id="cec2f-113">The following query returns both embedded classes, **E1** and **E2**, each having **Prop1** and **Prop2** populated with data.</span></span>

`ELECT E1.Prop1, E1.Prop2, E2.Prop1, E2.Prop2 FROM MyEvent`

<span data-ttu-id="cec2f-114">Equivale alla prima query usando l'asterisco ( \* ) invece di specificare ogni oggetto e proprietà.</span><span class="sxs-lookup"><span data-stu-id="cec2f-114">This is equivalent to the first query using the asterisk (\*) instead of specifying each object and property.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cec2f-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="cec2f-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cec2f-116">Esecuzione di query con WQL</span><span class="sxs-lookup"><span data-stu-id="cec2f-116">Querying with WQL</span></span>](querying-with-wql.md)
</dt> </dl>

 

 



