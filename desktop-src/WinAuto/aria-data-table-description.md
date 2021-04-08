---
title: Avviso tabella dati ARIA
description: Avviso tabella dati ARIA
ms.assetid: 3CFCF248-6A66-4140-B3E7-133E3809B287
keywords:
- AriaDataTableWarningId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dcd77983092983649d8bcd41357afb4756120e6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045236"
---
# <a name="aria-data-table-warning"></a><span data-ttu-id="7c1f9-104">Avviso tabella dati ARIA</span><span class="sxs-lookup"><span data-stu-id="7c1f9-104">ARIA Data Table Warning</span></span>

## <a name="text"></a><span data-ttu-id="7c1f9-105">Testo</span><span class="sxs-lookup"><span data-stu-id="7c1f9-105">Text</span></span>

<span data-ttu-id="7c1f9-106">La tabella contiene dati ma non include alcun Riepilogo né un attributo **aria-describedby** valido.</span><span class="sxs-lookup"><span data-stu-id="7c1f9-106">Table contains data but has neither summary nor a valid **aria-describedby** attribute.</span></span>

## <a name="type"></a><span data-ttu-id="7c1f9-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="7c1f9-107">Type</span></span>

<span data-ttu-id="7c1f9-108">Avviso</span><span class="sxs-lookup"><span data-stu-id="7c1f9-108">Warning</span></span>

## <a name="description"></a><span data-ttu-id="7c1f9-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7c1f9-109">Description</span></span>

<span data-ttu-id="7c1f9-110">Questo avviso si applica alle tabelle HTML con più di una cella.</span><span class="sxs-lookup"><span data-stu-id="7c1f9-110">This warning applies to HTML tables with more than one cell.</span></span> <span data-ttu-id="7c1f9-111">Non si applica alle tabelle con `role="presentation"` poiché queste sono considerate tabelle di layout.</span><span class="sxs-lookup"><span data-stu-id="7c1f9-111">It does not apply to tables with `role="presentation"` since these are considered to be layout tables.</span></span>

<span data-ttu-id="7c1f9-112">Questo avviso indica che la tabella è stata identificata come tabella dati, ma non è stata definita una descrizione accessibile.</span><span class="sxs-lookup"><span data-stu-id="7c1f9-112">This warning indicates that the table is identified as a data table but it doesn’t have an accessible description defined.</span></span>

> [!Note]  
> <span data-ttu-id="7c1f9-113">Non è necessario che tutte le tabelle dati dispongano di una descrizione accessibile.</span><span class="sxs-lookup"><span data-stu-id="7c1f9-113">Not all data tables are required to have an accessible description.</span></span> <span data-ttu-id="7c1f9-114">È necessario definire una descrizione accessibile se gli utenti necessitano di ulteriori informazioni per comprendere la struttura e il contenuto della tabella di dati.</span><span class="sxs-lookup"><span data-stu-id="7c1f9-114">You should define an accessible description if users need more information to understand the data table structure and content.</span></span>

 

<span data-ttu-id="7c1f9-115">Per risolvere il problema, definire una descrizione accessibile per la tabella usando l'attributo summary o l'attributo **aria-describedby** .</span><span class="sxs-lookup"><span data-stu-id="7c1f9-115">To address this warning, define a table accessible description by using the summary attribute or the **aria-describedby** attribute.</span></span>

## <a name="example"></a><span data-ttu-id="7c1f9-116">Esempio</span><span class="sxs-lookup"><span data-stu-id="7c1f9-116">Example</span></span>


```HTML
<!-- Define a table description by using the summary attribute. -->
<table summary="The first column contains the list of examples. In the second column ...">
...
</table>

<!-- Define a table description using the aria-describedby attribute. -->
<p id="tableHeader" >The first column contains the list of examples. In the second column ...</p>
<table aria-describedby="tableHeader" >
...
</table>
```



 

 




