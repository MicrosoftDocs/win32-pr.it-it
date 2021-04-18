---
description: I riferimenti dell'istruzione recuperano tutte le istanze di associazione che fanno riferimento a una particolare istanza di origine.
ms.assetid: 674be546-e7fd-4150-9d7c-2888d24bf1b3
ms.tgt_platform: multiple
title: RIFERIMENTI dell'istruzione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1c7cc624a1e91220fc6bfc89ef0a75878a9cfb1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309918"
---
# <a name="references-of-statement"></a><span data-ttu-id="1ccaa-103">RIFERIMENTI dell'istruzione</span><span class="sxs-lookup"><span data-stu-id="1ccaa-103">REFERENCES OF Statement</span></span>

<span data-ttu-id="1ccaa-104">I riferimenti dell'istruzione recuperano tutte le istanze di associazione che fanno riferimento a una particolare istanza di origine.</span><span class="sxs-lookup"><span data-stu-id="1ccaa-104">The REFERENCES OF statement retrieves all association instances that refer to a particular source instance.</span></span> <span data-ttu-id="1ccaa-105">La sintassi dei riferimenti all'istruzione è simile a quella dell'oggetto ASSOCIATOrs OF Statement.</span><span class="sxs-lookup"><span data-stu-id="1ccaa-105">The REFERENCES OF statement is similar to the ASSOCIATORS OF statement in its syntax.</span></span> <span data-ttu-id="1ccaa-106">Tuttavia, anziché recuperare le istanze dell'endpoint, vengono recuperate le istanze di associazione coinvolte.</span><span class="sxs-lookup"><span data-stu-id="1ccaa-106">However, rather than retrieving endpoint instances, it retrieves the intervening association instances.</span></span>

<span data-ttu-id="1ccaa-107">I riferimenti della clausola WHERE possono includere una o più delle seguenti parole chiave predefinite e i relativi valori:</span><span class="sxs-lookup"><span data-stu-id="1ccaa-107">The REFERENCES OF WHERE clause can include one or more of the following predefined keywords and their values:</span></span>


```sql
REFERENCES OF {SourceObject} WHERE 
    ClassDefsOnly
    RequiredQualifier = QualifierName
    ResultClass = ClassName
    Role = PropertyName
```



<span data-ttu-id="1ccaa-108">Per specificare un oggetto di origine, usare qualsiasi percorso di oggetto valido per SourceObject.</span><span class="sxs-lookup"><span data-stu-id="1ccaa-108">To specify a source object, use any valid object path for SourceObject.</span></span> <span data-ttu-id="1ccaa-109">Come per l'istruzione SELECT, la clausola WHERE è facoltativa e viene utilizzata per definire ulteriormente la query.</span><span class="sxs-lookup"><span data-stu-id="1ccaa-109">As with the SELECT statement, the WHERE clause is optional and is used to further define the query.</span></span> <span data-ttu-id="1ccaa-110">In altre parole, l'istruzione seguente è perfettamente valida:</span><span class="sxs-lookup"><span data-stu-id="1ccaa-110">That is, the following statement is perfectly valid:</span></span>


```sql
REFERENCES OF {Adapter="AHA-294X"}
```



<span data-ttu-id="1ccaa-111">La parola chiave **ClassDefsOnly** indica che l'istruzione restituisce un set di risultati di oggetti definizione di classe anziché le istanze effettive delle classi di associazione.</span><span class="sxs-lookup"><span data-stu-id="1ccaa-111">The **ClassDefsOnly** keyword indicates that the statement returns a result set of class definition objects rather than actual instances of the association classes.</span></span> <span data-ttu-id="1ccaa-112">Questi oggetti contengono le definizioni delle classi a cui appartengono le istanze che fanno riferimento all'oggetto di origine.</span><span class="sxs-lookup"><span data-stu-id="1ccaa-112">These objects contain definitions of classes to which the instances that reference the source object belong.</span></span> <span data-ttu-id="1ccaa-113">Ad esempio, l'istruzione seguente restituisce le definizioni per le classi **AdapterDriver** e **AdapterProtocol** :</span><span class="sxs-lookup"><span data-stu-id="1ccaa-113">For example, the following statement returns definitions for the **AdapterDriver** and **AdapterProtocol** classes:</span></span>


```sql
REFERENCES OF {Adapter="AHA-294X"} WHERE ClassDefsOnly
```



<span data-ttu-id="1ccaa-114">La parola chiave **RequiredQualifier** indica che gli oggetti Association restituiti devono includere il qualificatore specificato.</span><span class="sxs-lookup"><span data-stu-id="1ccaa-114">The **RequiredQualifier** keyword indicates that the returned association objects must include the specified qualifier.</span></span> <span data-ttu-id="1ccaa-115">La parola chiave **RequiredQualifier** può essere utilizzata per includere specifiche istanze di associazioni nel set di risultati.</span><span class="sxs-lookup"><span data-stu-id="1ccaa-115">The **RequiredQualifier** keyword can be used to include particular instances of associations in the result set.</span></span> <span data-ttu-id="1ccaa-116">Ad esempio, l'istruzione seguente restituisce le istanze di associazione che includono un qualificatore denominato **AdapterTag**:</span><span class="sxs-lookup"><span data-stu-id="1ccaa-116">For example, the following statement returns association instances that include a qualifier called **AdapterTag**:</span></span>


```sql
REFERENCES OF {Adapter="AHA-294X"}  WHERE RequiredQualifier = AdapterTag
```



<span data-ttu-id="1ccaa-117">La parola chiave **ResultClass** indica che gli oggetti Association restituiti devono appartenere o essere derivati dalla classe specificata.</span><span class="sxs-lookup"><span data-stu-id="1ccaa-117">The **ResultClass** keyword indicates that the returned association objects must belong to or be derived from the specified class.</span></span> <span data-ttu-id="1ccaa-118">Ad esempio, l'istruzione seguente restituisce le associazioni della classe **AdapterDriver** o delle sottoclassi di **AdapterDriver**:</span><span class="sxs-lookup"><span data-stu-id="1ccaa-118">For example, the following statement returns associations of the **AdapterDriver** class or subclasses of **AdapterDriver**:</span></span>


```sql
REFERENCES OF {Adapter="AHA-294X"} WHERE ResultClass = AdapterDriver
```



<span data-ttu-id="1ccaa-119">Le parole chiave **ClassDefsOnly** e **ResultClass** si escludono a vicenda.</span><span class="sxs-lookup"><span data-stu-id="1ccaa-119">The **ClassDefsOnly** and **ResultClass** keywords are mutually exclusive.</span></span> <span data-ttu-id="1ccaa-120">Il loro utilizzo combinato causa un errore di query non valido.</span><span class="sxs-lookup"><span data-stu-id="1ccaa-120">Using them together causes an invalid query error.</span></span>

<span data-ttu-id="1ccaa-121">La parola chiave **Role** indica che le associazioni restituite sono solo quelle in cui l'oggetto di origine svolge un particolare ruolo.</span><span class="sxs-lookup"><span data-stu-id="1ccaa-121">The **Role** keyword indicates that the returned associations are only those in which the source object plays a particular role.</span></span> <span data-ttu-id="1ccaa-122">Il ruolo viene definito dalla proprietà specificata, una proprietà Reference di tipo [ref](references.md). La parola chiave **Role** è utile nelle associazioni in cui un determinato oggetto può riprodurre un ruolo in alcuni casi e un altro ruolo in altri, ad esempio in associazioni gerarchiche.</span><span class="sxs-lookup"><span data-stu-id="1ccaa-122">The role is defined by the specified property, a reference property of type [ref](references.md). The **Role** keyword is useful in associations where a certain object can play one role in some cases and another role in others, such as in hierarchical associations.</span></span> <span data-ttu-id="1ccaa-123">È possibile utilizzare la parola chiave **Role** per recuperare tutte le associazioni in cui l'oggetto di origine svolge il ruolo di padre, ad esempio.</span><span class="sxs-lookup"><span data-stu-id="1ccaa-123">The **Role** keyword can be used to retrieve all of the associations in which the source object plays the role of parent, for example.</span></span> <span data-ttu-id="1ccaa-124">Nell'istruzione seguente viene illustrata la sintassi per recuperare le associazioni con una proprietà **padre** che fa riferimento all'oggetto di origine come elemento padre:</span><span class="sxs-lookup"><span data-stu-id="1ccaa-124">The following statement illustrates the syntax for retrieving associations that have a **parent** property referencing the source object as the parent:</span></span>


```sql
REFERENCES OF {Adapter="AHA-294X"} WHERE Role = parent
```



> [!Note]  
> <span data-ttu-id="1ccaa-125">Le query complesse non possono usare "and" o "or" per separare le parole chiave per gli ASSOCIATOri di e i riferimenti delle istruzioni.</span><span class="sxs-lookup"><span data-stu-id="1ccaa-125">Complex queries cannot use "And" or "Or" to separate keywords for ASSOCIATORS OF and REFERENCES OF statements.</span></span> <span data-ttu-id="1ccaa-126">Inoltre, il segno di uguale è l'unico operatore valido che può essere utilizzato con le parole chiave in queste query.</span><span class="sxs-lookup"><span data-stu-id="1ccaa-126">Furthermore, the equal sign is the only valid operator that can be used with the keywords in these queries.</span></span> <span data-ttu-id="1ccaa-127">Viene ad esempio considerata valida la query seguente:</span><span class="sxs-lookup"><span data-stu-id="1ccaa-127">For example, the following query is valid:</span></span>

 


```sql
"REFERENCES OF {Win32_NetworkAdapter.DeviceID="0"} " +
    "WHERE resultclass = Win32_NetworkAdapterSetting " +
    "requiredQualifier = Dynamic"
```



> [!Note]  
> <span data-ttu-id="1ccaa-128">Gli esempi successivi non sono validi.</span><span class="sxs-lookup"><span data-stu-id="1ccaa-128">The next examples are not valid.</span></span> <span data-ttu-id="1ccaa-129">Il primo esempio non usa il segno di uguale e il secondo esempio tenta erroneamente di usare la parola chiave **and** :</span><span class="sxs-lookup"><span data-stu-id="1ccaa-129">The first example does not use the equal sign and the second example erroneously attempts to use the **AND** keyword:</span></span>

 


```sql
"REFERENCES OF {Win32_NetworkAdapter.DeviceID="0"} " +
    "WHERE resultclass = Win32_NetworkAdapterSetting " +
    "requiredQualifier <> Dynamic"

"REFERENCES OF {Win32_NetworkAdapter.DeviceID="0"} " +
"WHERE resultclass = Win32_NetworkAdapterSetting " +
"AND requiredQualifier = Dynamic"
```



 

 



