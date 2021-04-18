---
description: Per la nuova lingua, è necessario aggiornare la proprietà ProductLanguage all'identificatore di lingua numerico (LANGID).
ms.assetid: e00ef69b-c54b-41de-9230-a7582b260891
title: Aggiornamento delle proprietà ProductLanguage e ProductCode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37a7537cdb0295075fbfd1b8b58e45a051610cf6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318274"
---
# <a name="updating-productlanguage-and-productcode-properties"></a><span data-ttu-id="e4b09-103">Aggiornamento delle proprietà ProductLanguage e ProductCode</span><span class="sxs-lookup"><span data-stu-id="e4b09-103">Updating ProductLanguage and ProductCode Properties</span></span>

<span data-ttu-id="e4b09-104">Per la nuova lingua, è necessario aggiornare la proprietà [**ProductLanguage**](productlanguage.md) all'identificatore di lingua numerico (LangID).</span><span class="sxs-lookup"><span data-stu-id="e4b09-104">The [**ProductLanguage**](productlanguage.md) property must be updated to the numeric language identifier (LANGID) for the new language.</span></span> <span data-ttu-id="e4b09-105">Nel caso dell'esempio di localizzazione, il valore della proprietà **ProductLanguage** deve essere modificato da LangID per la lingua inglese (1033) a LangID per il francese (1036) nella tabella delle [Proprietà](property-table.md).</span><span class="sxs-lookup"><span data-stu-id="e4b09-105">In the case of the localization example, the value of the **ProductLanguage** property must be changed from the LANGID for English (1033) to the LANGID for French (1036) in the [Property table](property-table.md).</span></span>

<span data-ttu-id="e4b09-106">Il valore della proprietà [**ProductCode**](productcode.md) nella tabella delle [Proprietà](property-table.md) deve essere modificato in un nuovo valore univoco quando si localizza un database perché un prodotto localizzato è considerato un prodotto diverso.</span><span class="sxs-lookup"><span data-stu-id="e4b09-106">The value of the [**ProductCode**](productcode.md) property in the [Property table](property-table.md) must be changed to a new, unique value when localizing a database because a localized product is considered a different product.</span></span> <span data-ttu-id="e4b09-107">Ad esempio, le versioni tedesche e in inglese di un'applicazione sono considerate due prodotti diversi e devono avere codici prodotto diversi.</span><span class="sxs-lookup"><span data-stu-id="e4b09-107">For example, the German and English versions of an application are considered two different products and must have different product codes.</span></span> <span data-ttu-id="e4b09-108">Vedere [codici prodotto](product-codes.md).</span><span class="sxs-lookup"><span data-stu-id="e4b09-108">See [Product Codes](product-codes.md).</span></span>

<span data-ttu-id="e4b09-109">Utilizzare l'Editor tabella di database per aggiornare i valori delle proprietà ProductCode e ProductLanguage nella tabella delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="e4b09-109">Use your database table editor to update the values of the ProductCode and ProductLanguage properties in the Property table.</span></span> <span data-ttu-id="e4b09-110">Non riutilizzare il GUID visualizzato se si copia questo esempio.</span><span class="sxs-lookup"><span data-stu-id="e4b09-110">Do not reuse the GUID shown if you copy this example.</span></span>

[<span data-ttu-id="e4b09-111">Tabella delle proprietà</span><span class="sxs-lookup"><span data-stu-id="e4b09-111">Property Table</span></span>](property-table.md)



| <span data-ttu-id="e4b09-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e4b09-112">Property</span></span>                                   | <span data-ttu-id="e4b09-113">Valore</span><span class="sxs-lookup"><span data-stu-id="e4b09-113">Value</span></span>                                  |
|--------------------------------------------|----------------------------------------|
| [<span data-ttu-id="e4b09-114">**ProductCode**</span><span class="sxs-lookup"><span data-stu-id="e4b09-114">**ProductCode**</span></span>](productcode.md)         | <span data-ttu-id="e4b09-115">{EE389960-E426-4EEA-B669-AD8129249881}</span><span class="sxs-lookup"><span data-stu-id="e4b09-115">{EE389960-E426-4EEA-B669-AD8129249881}</span></span> |
| [<span data-ttu-id="e4b09-116">**ProductLanguage**</span><span class="sxs-lookup"><span data-stu-id="e4b09-116">**ProductLanguage**</span></span>](productlanguage.md) | <span data-ttu-id="e4b09-117">1036</span><span class="sxs-lookup"><span data-stu-id="e4b09-117">1036</span></span>                                   |



 

[<span data-ttu-id="e4b09-118">Continua</span><span class="sxs-lookup"><span data-stu-id="e4b09-118">Continue</span></span>](updating-a-summary-information-stream.md)

 

 



