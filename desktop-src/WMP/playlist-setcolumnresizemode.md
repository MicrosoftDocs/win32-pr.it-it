---
title: PLAYLIST. setColumnResizeMode
description: Il metodo setColumnResizeMode specifica il modo in cui la colonna indicizzata si ridimensiona.
ms.assetid: 84ca0e60-ca24-4058-ae08-5b9cf3d7c38f
keywords:
- PLAYLIST. setColumnResizeMode Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.setColumnResizeMode
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9a1b83020f4400f4f1095c84e281fe498f2b67da
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333841"
---
# <a name="playlistsetcolumnresizemode"></a><span data-ttu-id="46710-104">PLAYLIST. setColumnResizeMode</span><span class="sxs-lookup"><span data-stu-id="46710-104">PLAYLIST.setColumnResizeMode</span></span>

<span data-ttu-id="46710-105">Il metodo **setColumnResizeMode** specifica il modo in cui la colonna indicizzata si ridimensiona.</span><span class="sxs-lookup"><span data-stu-id="46710-105">The **setColumnResizeMode** method specifies how the indexed column sizes itself.</span></span>

``` syntax
        elementID.setColumnResizeMode(column, mode)
```

## <a name="parameters"></a><span data-ttu-id="46710-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="46710-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46710-107"><span id="column"></span><span id="COLUMN"></span>*colonna*</span><span class="sxs-lookup"><span data-stu-id="46710-107"><span id="column"></span><span id="COLUMN"></span>*column*</span></span>
</dt> <dd>

<span data-ttu-id="46710-108">**Numero** (**Long**) che indica l'indice della colonna da modificare.</span><span class="sxs-lookup"><span data-stu-id="46710-108">**Number** (**long**) indicating the index of the column to be changed.</span></span>

</dd> <dt>

<span data-ttu-id="46710-109"><span id="mode"></span><span id="MODE"></span>*modalità*</span><span class="sxs-lookup"><span data-stu-id="46710-109"><span id="mode"></span><span id="MODE"></span>*mode*</span></span>
</dt> <dd>

<span data-ttu-id="46710-110">**Stringa** che indica la modalità di ridimensionamento.</span><span class="sxs-lookup"><span data-stu-id="46710-110">**String** indicating the sizing mode.</span></span> <span data-ttu-id="46710-111">Contiene uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="46710-111">Contains one of the following values.</span></span>



| <span data-ttu-id="46710-112">Valore</span><span class="sxs-lookup"><span data-stu-id="46710-112">Value</span></span>          | <span data-ttu-id="46710-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="46710-113">Description</span></span>                                                                                                    |
|----------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46710-114">AutosizeHeader</span><span class="sxs-lookup"><span data-stu-id="46710-114">AutosizeHeader</span></span> | <span data-ttu-id="46710-115">La colonna viene ridimensionata per contenere tutti i dati nella colonna e nell'intestazione.</span><span class="sxs-lookup"><span data-stu-id="46710-115">The column resizes to accommodate all data in both the column and the header.</span></span>                                  |
| <span data-ttu-id="46710-116">AutosizeData</span><span class="sxs-lookup"><span data-stu-id="46710-116">AutosizeData</span></span>   | <span data-ttu-id="46710-117">La colonna viene ridimensionata in modo da contenere solo tutti i dati della colonna.</span><span class="sxs-lookup"><span data-stu-id="46710-117">The column resizes to accommodate all data in the column only.</span></span>                                                 |
| <span data-ttu-id="46710-118">Fisso</span><span class="sxs-lookup"><span data-stu-id="46710-118">Fixed</span></span>          | <span data-ttu-id="46710-119">La colonna è a dimensione fissa.</span><span class="sxs-lookup"><span data-stu-id="46710-119">The column is a fixed size.</span></span>                                                                                    |
| <span data-ttu-id="46710-120">Occupa completamente</span><span class="sxs-lookup"><span data-stu-id="46710-120">Stretches</span></span>      | <span data-ttu-id="46710-121">La colonna viene ridimensionata in modo da utilizzare lo spazio rimanente nell'elemento della **playlist** dopo che tutte le altre colonne vengono ridimensionate.</span><span class="sxs-lookup"><span data-stu-id="46710-121">The column resizes to use the remaining space in the **PLAYLIST** element after all other columns are resized.</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46710-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="46710-122">Return Value</span></span>

<span data-ttu-id="46710-123">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="46710-123">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="46710-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="46710-124">Requirements</span></span>



| <span data-ttu-id="46710-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="46710-125">Requirement</span></span> | <span data-ttu-id="46710-126">Valore</span><span class="sxs-lookup"><span data-stu-id="46710-126">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="46710-127">Versione</span><span class="sxs-lookup"><span data-stu-id="46710-127">Version</span></span><br/> | <span data-ttu-id="46710-128">Windows Media Player versione 7,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="46710-128">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="46710-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="46710-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46710-130">**PLAYLIST (elemento)**</span><span class="sxs-lookup"><span data-stu-id="46710-130">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> </dl>

 

 





