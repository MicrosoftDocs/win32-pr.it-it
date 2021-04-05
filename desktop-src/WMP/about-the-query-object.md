---
title: Informazioni sull'oggetto query
description: Informazioni sull'oggetto query
ms.assetid: 41488036-bdcf-4fe6-8f7e-f0897157d3d9
keywords:
- Windows Media Player, oggetto query
- Modello a oggetti di Windows Media Player, oggetto query
- modello a oggetti, oggetto query
- Controllo ActiveX Windows Media Player, oggetto query
- Controllo ActiveX, oggetto query
- Controllo ActiveX Windows Media Player Mobile, oggetto query
- Windows Media Player Mobile, oggetto query
- Oggetto query
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54a26f60c38e053b91c7e56f5cbd7ccaf2ba0fe2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710792"
---
# <a name="about-the-query-object"></a><span data-ttu-id="90f89-111">Informazioni sull'oggetto query</span><span class="sxs-lookup"><span data-stu-id="90f89-111">About the Query Object</span></span>

<span data-ttu-id="90f89-112">L'oggetto **query** rappresenta una query composta.</span><span class="sxs-lookup"><span data-stu-id="90f89-112">The **Query** object represents a compound query.</span></span> <span data-ttu-id="90f89-113">Si crea un nuovo oggetto **query** vuoto chiamando *mediacollection*. **CreateQuery**.</span><span class="sxs-lookup"><span data-stu-id="90f89-113">You create a new, empty **Query** object by calling *mediaCollection*.**createQuery**.</span></span> <span data-ttu-id="90f89-114">Dopo aver creato un oggetto **query** , è possibile chiamare **addCondition** per aggiungere una condizione alla query composta.</span><span class="sxs-lookup"><span data-stu-id="90f89-114">After you have created a **Query** object, you can call **addCondition** to add a condition to the compound query.</span></span> <span data-ttu-id="90f89-115">Ogni chiamata successiva a **addCondition** aggiunge una nuova condizione alla query esistente usando la logica and.</span><span class="sxs-lookup"><span data-stu-id="90f89-115">Each subsequent call to **addCondition** appends a new condition to the existing query using AND logic.</span></span>

<span data-ttu-id="90f89-116">Si supponga, ad esempio, di voler creare una query che rappresenti tutti i supporti digitali in cui **WM/genre** è uguale a "Jazz" e l' **autore** contiene "Jim".</span><span class="sxs-lookup"><span data-stu-id="90f89-116">For example, suppose you want to create a query that represents all digital media where **WM/Genre** equals "Jazz" and **Author** contains "Jim".</span></span> <span data-ttu-id="90f89-117">È possibile creare una query composta per rappresentare queste condizioni usando il codice JScript seguente:</span><span class="sxs-lookup"><span data-stu-id="90f89-117">You could create a compound query to represent these conditions by using the following JScript code:</span></span>


```C++
// Create the query object.
var Query = player.mediaCollection.createQuery();

// Add the conditions.
Query.addCondition("WM/Genre", "Equals", "Jazz");
Query.addCondition("Author", "Contains", "Jim");
```



<span data-ttu-id="90f89-118">Per aggiungere una condizione a una query composta usando la logica o, è necessario chiamare **query. beginNextGroup**.</span><span class="sxs-lookup"><span data-stu-id="90f89-118">To add a condition to a compound query using OR logic, you must call **Query.beginNextGroup**.</span></span> <span data-ttu-id="90f89-119">Questo metodo segnala che il gruppo di condizioni precedente è stato completato e che la chiamata successiva a **addCondition** rappresenta l'inizio di un nuovo gruppo di condizioni.</span><span class="sxs-lookup"><span data-stu-id="90f89-119">This method signals that the previous condition group is completed and that the next call to **addCondition** represents the start of a new condition group.</span></span>

<span data-ttu-id="90f89-120">Ad esempio, per creare una query che rappresenti tutti i supporti digitali in cui **WM/genre** è uguale a "Jazz" e l' **autore** contiene "Jim" o l' **autore** contiene "Dave", è possibile usare il codice di esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="90f89-120">For example, to create a query that represents all digital media where **WM/Genre** equals "Jazz" and **Author** contains "Jim" or **Author** contains "Dave", you could use the following example code:</span></span>


```C++
// Create the query object.
var Query = player.mediaCollection.createQuery();

// Add the conditions.
Query.addCondition("WM/Genre", "Equals", "Jazz");
Query.addCondition("Author", "Contains", "Jim");

// Start the next condition group. This group will be
// combined with the previous group using a logical OR operation.
Query.beginNextGroup();

// Add the conditions.
Query.addCondition("WM/Genre", "Equals", "Jazz");
Query.addCondition("Author", "Contains", "Dave");
```



<span data-ttu-id="90f89-121">Per eseguire la query composta, chiamare **mediacollection. getPlaylistByQuery**.</span><span class="sxs-lookup"><span data-stu-id="90f89-121">To execute your compound query, call **MediaCollection.getPlaylistByQuery**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="90f89-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="90f89-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="90f89-123">**Mediacollection. getPlaylistByQuery**</span><span class="sxs-lookup"><span data-stu-id="90f89-123">**MediaCollection.getPlaylistByQuery**</span></span>](mediacollection-getplaylistbyquery.md)
</dt> <dt>

[<span data-ttu-id="90f89-124">**Modello a oggetti del lettore per i linguaggi di scripting**</span><span class="sxs-lookup"><span data-stu-id="90f89-124">**Player Object Model for Scripting Languages**</span></span>](player-object-model-for-scripting-languages.md)
</dt> <dt>

[<span data-ttu-id="90f89-125">**Oggetto query**</span><span class="sxs-lookup"><span data-stu-id="90f89-125">**Query Object**</span></span>](query-object.md)
</dt> </dl>

 

 




