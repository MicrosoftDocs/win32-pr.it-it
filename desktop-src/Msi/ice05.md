---
description: 'ICE05 verifica che in alcune tabelle siano contenute voci obbligatorie. Questo include, ma non è limitato a, il controllo della tabella delle proprietà per le proprietà obbligatorie: ProductName, ProductLanguage, ProductVersion, ProductCode e manufacturer.'
ms.assetid: 90b35758-c9d9-4104-a352-f0b17b04b571
title: ICE05
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e9710a81eca3da7ac947afb90a1d6788c0ddd74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314245"
---
# <a name="ice05"></a><span data-ttu-id="197b7-104">ICE05</span><span class="sxs-lookup"><span data-stu-id="197b7-104">ICE05</span></span>

<span data-ttu-id="197b7-105">ICE05 verifica che in alcune tabelle siano contenute voci obbligatorie.</span><span class="sxs-lookup"><span data-stu-id="197b7-105">ICE05 validates that certain tables contain required entries.</span></span> <span data-ttu-id="197b7-106">Questo include, ma non è limitato a, il controllo [della tabella delle proprietà](property-table.md) per le proprietà obbligatorie: [**ProductName**](productname.md), [**ProductLanguage**](productlanguage.md), [**ProductVersion**](productversion.md), [**ProductCode**](productcode.md)e [**Manufacturer**](manufacturer.md).</span><span class="sxs-lookup"><span data-stu-id="197b7-106">This includes, but is not restricted to, checking the [Property table](property-table.md) for the required properties: [**ProductName**](productname.md), [**ProductLanguage**](productlanguage.md), [**ProductVersion**](productversion.md), [**ProductCode**](productcode.md), and [**Manufacturer**](manufacturer.md).</span></span>

## <a name="result"></a><span data-ttu-id="197b7-107">Risultato</span><span class="sxs-lookup"><span data-stu-id="197b7-107">Result</span></span>

<span data-ttu-id="197b7-108">ICE05 Invia un errore se manca una voce obbligatoria.</span><span class="sxs-lookup"><span data-stu-id="197b7-108">ICE05 posts an error if a required entry is missing.</span></span>

## <a name="example"></a><span data-ttu-id="197b7-109">Esempio</span><span class="sxs-lookup"><span data-stu-id="197b7-109">Example</span></span>

<span data-ttu-id="197b7-110">Per l'esempio illustrato, ICE05 segnala che la voce ' ProductVersion ' è obbligatoria nella tabella ' Property '.</span><span class="sxs-lookup"><span data-stu-id="197b7-110">For the example shown, ICE05 would report that the entry: 'ProductVersion' is required in the 'Property' table.</span></span>

<span data-ttu-id="197b7-111">[Tabella delle proprietà](property-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="197b7-111">[Property Table](property-table.md) (partial)</span></span>



| <span data-ttu-id="197b7-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="197b7-112">Property</span></span>                           | <span data-ttu-id="197b7-113">Valore</span><span class="sxs-lookup"><span data-stu-id="197b7-113">Value</span></span>     |
|------------------------------------|-----------|
| [<span data-ttu-id="197b7-114">**ProductName**</span><span class="sxs-lookup"><span data-stu-id="197b7-114">**ProductName**</span></span>](productname.md) | <span data-ttu-id="197b7-115">MyProduct</span><span class="sxs-lookup"><span data-stu-id="197b7-115">MyProduct</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="197b7-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="197b7-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="197b7-117">Riferimento ghiaccio</span><span class="sxs-lookup"><span data-stu-id="197b7-117">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



