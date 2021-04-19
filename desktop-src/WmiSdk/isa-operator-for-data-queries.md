---
description: Utilizzare l'operatore ISA nella clausola WHERE di una query di dati per richiedere oggetti incorporati in una gerarchia di classi.
ms.assetid: a4eb4c34-2ed0-4e85-84c6-6b8f17c8b07d
ms.tgt_platform: multiple
title: Operatore ISA per query di dati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b4c063c99f50a57c8b22a5bbe7040aa3fe96ba5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315209"
---
# <a name="isa-operator-for-data-queries"></a><span data-ttu-id="dc742-103">Operatore ISA per query di dati</span><span class="sxs-lookup"><span data-stu-id="dc742-103">ISA Operator for Data Queries</span></span>

<span data-ttu-id="dc742-104">Utilizzare l'operatore ISA nella clausola WHERE di una query di dati per richiedere oggetti incorporati in una gerarchia di classi.</span><span class="sxs-lookup"><span data-stu-id="dc742-104">Use the ISA operator in the WHERE clause of a data query to request embedded objects in a class hierarchy.</span></span>

<span data-ttu-id="dc742-105">Nell'esempio seguente viene illustrata la sintassi per richiedere oggetti incorporati in una gerarchia di classi.</span><span class="sxs-lookup"><span data-stu-id="dc742-105">The following example shows the syntax to request embedded objects in a class hierarchy.</span></span>


```sql
SELECT * FROM Class WHERE EmbeddedProp ISA "ParentClass"
```



<span data-ttu-id="dc742-106">Il risultato include istanze della **classe** con oggetti incorporati derivati da **ParentClass** nella proprietà **EmbeddedProp** .</span><span class="sxs-lookup"><span data-stu-id="dc742-106">The result includes instances of **Class** having embedded objects that are derived from **ParentClass** in the **EmbeddedProp** property.</span></span> <span data-ttu-id="dc742-107">Non tutte le istanze dell'oggetto **classe** sono derivate da **ParentClass**, ma il risultato restituisce gli oggetti incorporati derivati da **ParentClass**.</span><span class="sxs-lookup"><span data-stu-id="dc742-107">Not every instance of the **Class** object is derived from **ParentClass**, but the result returns the embedded objects that are derived from **ParentClass**.</span></span>

<span data-ttu-id="dc742-108">Ad esempio, nella query seguente, **ClassA** include la proprietà **EmbeddedObj** con tipizzazione debole.</span><span class="sxs-lookup"><span data-stu-id="dc742-108">For example, in the following query, **ClassA** includes the weakly typed **EmbeddedObj** property.</span></span> <span data-ttu-id="dc742-109">La classe **ClassA** ha dieci istanze.</span><span class="sxs-lookup"><span data-stu-id="dc742-109">The **ClassA** class has ten instances.</span></span> <span data-ttu-id="dc742-110">Cinque di queste istanze hanno oggetti incorporati con un tipo derivato da **ClassZ**.</span><span class="sxs-lookup"><span data-stu-id="dc742-110">Five of those instances have embedded objects with a type derived from **ClassZ**.</span></span> <span data-ttu-id="dc742-111">Gli altri cinque hanno oggetti incorporati di altri tipi.</span><span class="sxs-lookup"><span data-stu-id="dc742-111">The other five have embedded objects of other types.</span></span>

<span data-ttu-id="dc742-112">Nell'esempio seguente viene illustrata la query che restituisce le cinque istanze di che includono gli oggetti derivati da **ClassZ**.</span><span class="sxs-lookup"><span data-stu-id="dc742-112">The following example shows the query that returns the five instances, which include the objects that are derived from **ClassZ**.</span></span>


```sql
SELECT * FROM ClassA WHERE EmbeddedObj ISA "ClassZ"
```



 

 



