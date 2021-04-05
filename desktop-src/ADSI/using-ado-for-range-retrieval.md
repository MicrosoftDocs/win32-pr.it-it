---
title: Utilizzo di ADO per il recupero di intervalli
description: Se viene usato un linguaggio di automazione, è necessario usare ADO (ActiveX Directory Objects) per recuperare un intervallo di valori di proprietà. Quando si usa ADO per il recupero di intervalli, è necessario risolvere un problema specifico.
ms.assetid: ca06169d-7de7-4552-aa7d-e9427353e49e
ms.tgt_platform: multiple
keywords:
- Utilizzo di ADO per il recupero di intervalli ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cb8950a71708bd9c824c90842f043808c897554
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707366"
---
# <a name="using-ado-for-range-retrieval"></a><span data-ttu-id="21401-104">Utilizzo di ADO per il recupero di intervalli</span><span class="sxs-lookup"><span data-stu-id="21401-104">Using ADO for Range Retrieval</span></span>

<span data-ttu-id="21401-105">Se viene usato un linguaggio di automazione, è necessario usare ADO (ActiveX Directory Objects) per recuperare un intervallo di valori di proprietà.</span><span class="sxs-lookup"><span data-stu-id="21401-105">If an automation language is used, the ActiveX Directory Objects (ADO) should be used to retrieve a range of property values.</span></span>

<span data-ttu-id="21401-106">Quando si usa ADO per il recupero di intervalli, è necessario risolvere un problema specifico.</span><span class="sxs-lookup"><span data-stu-id="21401-106">When using ADO for range retrieval, there is one problem that must be specifically addressed.</span></span> <span data-ttu-id="21401-107">Quando si esegue una query per il gruppo di valori di proprietà finale, l'oggetto ADO recupererà zero oggetti, anche se rimane.</span><span class="sxs-lookup"><span data-stu-id="21401-107">When querying for the final group of property values, the ADO object will retrieve zero objects, even though more remain.</span></span> <span data-ttu-id="21401-108">Per recuperare i valori rimanenti, usare il carattere jolly di intervallo ' \* '.</span><span class="sxs-lookup"><span data-stu-id="21401-108">To retrieve the remaining values, use the range wildcard '\*'.</span></span> <span data-ttu-id="21401-109">Se, ad esempio, un gruppo contiene 150 membri, è possibile recuperare i valori dei membri 0-100 normalmente utilizzando il recupero con intervallo.</span><span class="sxs-lookup"><span data-stu-id="21401-109">For example, if a group contains 150 members, member values 0-100 can be retrieved normally using ranged retrieval.</span></span> <span data-ttu-id="21401-110">Se viene quindi richiesto l'intervallo 101-200, l'oggetto ADO restituirà zero oggetti.</span><span class="sxs-lookup"><span data-stu-id="21401-110">If range 101-200 is then requested, the ADO object will return zero objects.</span></span> <span data-ttu-id="21401-111">A questo punto è necessario modificare la query in un intervallo di richiesta 101- \* .</span><span class="sxs-lookup"><span data-stu-id="21401-111">At this point, it is necessary to modify the query to request range 101-\*.</span></span> <span data-ttu-id="21401-112">Questa operazione consente di recuperare i valori da 101 a 150.</span><span class="sxs-lookup"><span data-stu-id="21401-112">This will retrieve values from 101 to 150.</span></span> <span data-ttu-id="21401-113">Per ulteriori informazioni e un esempio di codice, vedere [codice di esempio per l'utilizzo di ranging per recuperare i membri di un gruppo](example-code-for-using-ranging-to-retrieve-members-of-a-group.md).</span><span class="sxs-lookup"><span data-stu-id="21401-113">For more information and a code example, see [Example Code for Using Ranging to Retrieve Members of a Group](example-code-for-using-ranging-to-retrieve-members-of-a-group.md).</span></span>

<span data-ttu-id="21401-114">Per ulteriori informazioni sull'utilizzo di ADO per il recupero di intervalli, vedere:</span><span class="sxs-lookup"><span data-stu-id="21401-114">For more information about using ADO for range retrieval, see:</span></span>

-   [<span data-ttu-id="21401-115">Dialetto ADO LDAP</span><span class="sxs-lookup"><span data-stu-id="21401-115">ADO LDAP Ranging Dialect</span></span>](ado-ldap-ranging-dialect.md)
-   [<span data-ttu-id="21401-116">Sottolinguaggio ADO SQL</span><span class="sxs-lookup"><span data-stu-id="21401-116">ADO SQL Ranging Dialect</span></span>](ado-sql-ranging-dialect.md)
-   [<span data-ttu-id="21401-117">Codice di esempio per l'uso della funzione Rang per recuperare i membri di un gruppo</span><span class="sxs-lookup"><span data-stu-id="21401-117">Example Code for Using Ranging to Retrieve Members of a Group</span></span>](example-code-for-using-ranging-to-retrieve-members-of-a-group.md)

 

 




