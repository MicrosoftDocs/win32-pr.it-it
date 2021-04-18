---
title: COLUMN. columnResizeMode
description: L'attributo columnResizeMode specifica o recupera la modalità di ridimensionamento per la colonna.
ms.assetid: 95ece2a3-20a6-4b9d-a2eb-fc69fc612f29
keywords:
- Media Player di Windows COLUMN. columnResizeMode
topic_type:
- apiref
api_name:
- COLUMN.columnResizeMode
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52d17b1a2edd878fb15e69c595e3c061c1963a5b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327782"
---
# <a name="columncolumnresizemode"></a><span data-ttu-id="8113c-104">COLUMN. columnResizeMode</span><span class="sxs-lookup"><span data-stu-id="8113c-104">COLUMN.columnResizeMode</span></span>

<span data-ttu-id="8113c-105">L'attributo **columnResizeMode** specifica o recupera la modalità di ridimensionamento per la colonna.</span><span class="sxs-lookup"><span data-stu-id="8113c-105">The **columnResizeMode** attribute specifies or retrieves the resize mode for this column.</span></span>

``` syntax
        elementID.columnResizeMode
```

## <a name="possible-values"></a><span data-ttu-id="8113c-106">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="8113c-106">Possible Values</span></span>

<span data-ttu-id="8113c-107">Questo attributo è una **stringa** di lettura/scrittura contenente uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="8113c-107">This attribute is a read/write **String** containing one of the following values.</span></span>



| <span data-ttu-id="8113c-108">Valore</span><span class="sxs-lookup"><span data-stu-id="8113c-108">Value</span></span>          | <span data-ttu-id="8113c-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8113c-109">Description</span></span>                                                                                                    |
|----------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8113c-110">AutosizeHeader</span><span class="sxs-lookup"><span data-stu-id="8113c-110">AutosizeHeader</span></span> | <span data-ttu-id="8113c-111">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="8113c-111">Default.</span></span> <span data-ttu-id="8113c-112">La colonna viene ridimensionata per contenere tutti i dati nella colonna e nell'intestazione.</span><span class="sxs-lookup"><span data-stu-id="8113c-112">The column resizes to accommodate all data in both the column and the header.</span></span>                         |
| <span data-ttu-id="8113c-113">AutosizeData</span><span class="sxs-lookup"><span data-stu-id="8113c-113">AutosizeData</span></span>   | <span data-ttu-id="8113c-114">La colonna viene ridimensionata in modo da contenere solo tutti i dati della colonna.</span><span class="sxs-lookup"><span data-stu-id="8113c-114">The column resizes to accommodate all data in the column only.</span></span>                                                 |
| <span data-ttu-id="8113c-115">Fisso</span><span class="sxs-lookup"><span data-stu-id="8113c-115">Fixed</span></span>          | <span data-ttu-id="8113c-116">La colonna è a dimensione fissa.</span><span class="sxs-lookup"><span data-stu-id="8113c-116">The column is a fixed size.</span></span>                                                                                    |
| <span data-ttu-id="8113c-117">Occupa completamente</span><span class="sxs-lookup"><span data-stu-id="8113c-117">Stretches</span></span>      | <span data-ttu-id="8113c-118">La colonna viene ridimensionata in modo da utilizzare lo spazio rimanente del controllo **playlist** dopo che tutte le altre colonne vengono ridimensionate.</span><span class="sxs-lookup"><span data-stu-id="8113c-118">The column resizes to use the remaining space in the **PLAYLIST** control after all other columns are resized.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="8113c-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8113c-119">Requirements</span></span>



| <span data-ttu-id="8113c-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="8113c-120">Requirement</span></span> | <span data-ttu-id="8113c-121">Valore</span><span class="sxs-lookup"><span data-stu-id="8113c-121">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="8113c-122">Versione</span><span class="sxs-lookup"><span data-stu-id="8113c-122">Version</span></span><br/> | <span data-ttu-id="8113c-123">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="8113c-123">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8113c-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8113c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8113c-125">**COLUMN-elemento**</span><span class="sxs-lookup"><span data-stu-id="8113c-125">**COLUMN Element**</span></span>](column-element.md)
</dt> </dl>

 

 





