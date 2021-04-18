---
title: PLAYLIST. sortColumn
description: Il metodo sortColumn Ordina i dati nella colonna specificata.
ms.assetid: 1563fee8-044a-4cb4-a9c2-11d4533536da
keywords:
- PLAYLIST. sortColumn Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.sortColumn
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f21f0032ee4db4c7af46b5dda814bb11db551330
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333835"
---
# <a name="playlistsortcolumn"></a><span data-ttu-id="e65e2-104">PLAYLIST. sortColumn</span><span class="sxs-lookup"><span data-stu-id="e65e2-104">PLAYLIST.sortColumn</span></span>

<span data-ttu-id="e65e2-105">Il metodo **SortColumn** Ordina i dati nella colonna specificata.</span><span class="sxs-lookup"><span data-stu-id="e65e2-105">The **sortColumn** method sorts the data in the specified column.</span></span>

``` syntax
        elementID.sortColumn(column)
```

## <a name="parameters"></a><span data-ttu-id="e65e2-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e65e2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e65e2-107"><span id="column"></span><span id="COLUMN"></span>*colonna*</span><span class="sxs-lookup"><span data-stu-id="e65e2-107"><span id="column"></span><span id="COLUMN"></span>*column*</span></span>
</dt> <dd>

<span data-ttu-id="e65e2-108">**Numero** (**Long**) che indica l'indice della colonna da ordinare.</span><span class="sxs-lookup"><span data-stu-id="e65e2-108">**Number** (**long**) indicating the index of the column to sort.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e65e2-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e65e2-109">Return Value</span></span>

<span data-ttu-id="e65e2-110">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="e65e2-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e65e2-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="e65e2-111">Remarks</span></span>

<span data-ttu-id="e65e2-112">Questo metodo ordina la colonna specificata nello stesso modo dei pulsanti di intestazione di colonna nell'elemento **playlist** .</span><span class="sxs-lookup"><span data-stu-id="e65e2-112">This method sorts the specified column in the same way as the column header buttons in the **PLAYLIST** element.</span></span> <span data-ttu-id="e65e2-113">Se la colonna non è ancora stata ordinata, viene ordinata in ordine alfanumerico.</span><span class="sxs-lookup"><span data-stu-id="e65e2-113">If the column has not yet been sorted, it is sorted in alphanumeric order.</span></span> <span data-ttu-id="e65e2-114">Se è stato ordinato, l'ordine viene invertito.</span><span class="sxs-lookup"><span data-stu-id="e65e2-114">If it has been sorted, its order is reversed.</span></span>

<span data-ttu-id="e65e2-115">Per il corretto funzionamento di questo metodo, l'attributo **allowColumnSorting** deve essere impostato su true.</span><span class="sxs-lookup"><span data-stu-id="e65e2-115">For this method to work, the **allowColumnSorting** attribute must be set to true.</span></span>

## <a name="requirements"></a><span data-ttu-id="e65e2-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e65e2-116">Requirements</span></span>



| <span data-ttu-id="e65e2-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="e65e2-117">Requirement</span></span> | <span data-ttu-id="e65e2-118">Valore</span><span class="sxs-lookup"><span data-stu-id="e65e2-118">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="e65e2-119">Versione</span><span class="sxs-lookup"><span data-stu-id="e65e2-119">Version</span></span><br/> | <span data-ttu-id="e65e2-120">Windows Media Player versione 7,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="e65e2-120">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e65e2-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e65e2-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e65e2-122">**PLAYLIST (elemento)**</span><span class="sxs-lookup"><span data-stu-id="e65e2-122">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> <dt>

[<span data-ttu-id="e65e2-123">**PLAYLIST. allowColumnSorting**</span><span class="sxs-lookup"><span data-stu-id="e65e2-123">**PLAYLIST.allowColumnSorting**</span></span>](playlist-allowcolumnsorting.md)
</dt> </dl>

 

 





