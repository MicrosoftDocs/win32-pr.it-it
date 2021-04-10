---
description: Le query dello schema sono istruzioni WQL che richiedono definizioni di classe e informazioni sulle associazioni dello schema.
ms.assetid: cb65e99f-9046-4c63-ab56-60dedc45bcef
ms.tgt_platform: multiple
title: Recupero di definizioni di classe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d865b1a85eefa7e67b12ed4c0acc16ea9e19f9a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131011"
---
# <a name="retrieving-class-definitions"></a><span data-ttu-id="0b49a-103">Recupero di definizioni di classe</span><span class="sxs-lookup"><span data-stu-id="0b49a-103">Retrieving Class Definitions</span></span>

<span data-ttu-id="0b49a-104">Le query dello schema sono istruzioni WQL che richiedono definizioni di classe e informazioni sulle [associazioni dello schema](schema-associations.md).</span><span class="sxs-lookup"><span data-stu-id="0b49a-104">Schema queries are WQL statements that request class definitions and information about [schema associations](schema-associations.md).</span></span> <span data-ttu-id="0b49a-105">I provider di classi utilizzano query dello schema nelle istanze della classe [**\_ \_ ClassProviderRegistration**](--classproviderregistration.md) per specificare le classi supportate durante la registrazione con WMI.</span><span class="sxs-lookup"><span data-stu-id="0b49a-105">Class providers use schema queries in their instances of the [**\_\_ClassProviderRegistration**](--classproviderregistration.md) class to specify the classes that they support when they register with WMI.</span></span> <span data-ttu-id="0b49a-106">Le query dello schema vengono inserite nelle proprietà **ResultSetQueries**, **ReferencedSetQueries** e **UnsupportedQueries** dell'istanza di **\_ \_ ClassProviderRegistration** .</span><span class="sxs-lookup"><span data-stu-id="0b49a-106">Schema queries are placed in the **ResultSetQueries**, **ReferencedSetQueries**, and **UnsupportedQueries** properties of the **\_\_ClassProviderRegistration** instance.</span></span>

<span data-ttu-id="0b49a-107">Le query di schema sono simili alle query di dati perché supportano le istruzioni WQL seguenti:</span><span class="sxs-lookup"><span data-stu-id="0b49a-107">Schema queries are similar to data queries in that they support the following WQL statements:</span></span>

-   [<span data-ttu-id="0b49a-108">SELECT</span><span class="sxs-lookup"><span data-stu-id="0b49a-108">SELECT</span></span>](select-statement-for-schema-queries.md)
-   [<span data-ttu-id="0b49a-109">ASSOCIATORI DI</span><span class="sxs-lookup"><span data-stu-id="0b49a-109">ASSOCIATORS OF</span></span>](schema-associations.md)
-   [<span data-ttu-id="0b49a-110">RIFERIMENTI DI</span><span class="sxs-lookup"><span data-stu-id="0b49a-110">REFERENCES OF</span></span>](schema-associations.md)
-   [<span data-ttu-id="0b49a-111">ISA</span><span class="sxs-lookup"><span data-stu-id="0b49a-111">ISA</span></span>](isa-operator-for-schema-queries.md)

<span data-ttu-id="0b49a-112">Una query di schema è simile a un [riferimento della query di](references-of-statement.md) dati che specifica la parola chiave **ClassDefsOnly** . in altre parole, restituisce un set di risultati di oggetti di definizione di classe anziché le istanze effettive delle classi di associazione.</span><span class="sxs-lookup"><span data-stu-id="0b49a-112">A schema query is similar to a [REFERENCES OF](references-of-statement.md) data query that specifies the **ClassDefsOnly** keyword; in other words, that returns a result set of class definition objects rather than actual instances of association classes.</span></span> <span data-ttu-id="0b49a-113">Tuttavia, i riferimenti di restituiscono le definizioni della classe solo se sono presenti istanze.</span><span class="sxs-lookup"><span data-stu-id="0b49a-113">However, REFERENCES OF returns class definitions only if there are instances present.</span></span> <span data-ttu-id="0b49a-114">Una query di schema restituisce le definizioni delle classi se le istanze sono presenti o meno.</span><span class="sxs-lookup"><span data-stu-id="0b49a-114">A schema query returns class definitions whether or not instances are present.</span></span>

 

 



