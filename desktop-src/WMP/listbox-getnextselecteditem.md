---
title: LISTBOX. getNextSelectedItem
description: Il metodo getNextSelectedItem Recupera il successivo elemento selezionato nel controllo casella di riepilogo a partire dall'elemento dopo quello con l'indice specificato.
ms.assetid: 060d196d-2b14-4386-ba01-34256c137db5
keywords:
- Media Player di Windows LISTBOX. getNextSelectedItem
topic_type:
- apiref
api_name:
- LISTBOX.getNextSelectedItem
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8afb3df1f1b6a6adc528e02dd6531ac4fc1a9a3e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327742"
---
# <a name="listboxgetnextselecteditem"></a><span data-ttu-id="37717-104">LISTBOX. getNextSelectedItem</span><span class="sxs-lookup"><span data-stu-id="37717-104">LISTBOX.getNextSelectedItem</span></span>

<span data-ttu-id="37717-105">Il metodo **getNextSelectedItem** Recupera il successivo elemento selezionato nel controllo casella di riepilogo a partire dall'elemento dopo quello con l'indice specificato.</span><span class="sxs-lookup"><span data-stu-id="37717-105">The **getNextSelectedItem** method retrieves the next selected item in the list box control starting at the item after the one with the specified index.</span></span>

``` syntax
        elementID.getNextSelectedItem(startIndex)
```

## <a name="parameters"></a><span data-ttu-id="37717-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="37717-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37717-107"><span id="startIndex"></span><span id="startindex"></span><span id="STARTINDEX"></span>*startIndex*</span><span class="sxs-lookup"><span data-stu-id="37717-107"><span id="startIndex"></span><span id="startindex"></span><span id="STARTINDEX"></span>*startIndex*</span></span>
</dt> <dd>

<span data-ttu-id="37717-108">**Numero** (**Long**) che contiene l'indice dell'elemento che precede l'elemento recuperato.</span><span class="sxs-lookup"><span data-stu-id="37717-108">**Number** (**long**) containing the index of the item that precedes the item being retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37717-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="37717-109">Return Value</span></span>

<span data-ttu-id="37717-110">Questo metodo restituisce un **numero** (**Long**) che contiene l'indice del successivo elemento selezionato.</span><span class="sxs-lookup"><span data-stu-id="37717-110">This method returns a **Number** (**long**) containing the index of the next selected item.</span></span>

## <a name="remarks"></a><span data-ttu-id="37717-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="37717-111">Remarks</span></span>

<span data-ttu-id="37717-112">Per avviare la ricerca dall'inizio, utilizzare 1 per l'indice iniziale.</span><span class="sxs-lookup"><span data-stu-id="37717-112">To start search from the beginning, use  1 for the start index.</span></span>

## <a name="requirements"></a><span data-ttu-id="37717-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="37717-113">Requirements</span></span>



| <span data-ttu-id="37717-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="37717-114">Requirement</span></span> | <span data-ttu-id="37717-115">Valore</span><span class="sxs-lookup"><span data-stu-id="37717-115">Value</span></span> |
|--------------------|---------------------------------------------------------|
| <span data-ttu-id="37717-116">Versione</span><span class="sxs-lookup"><span data-stu-id="37717-116">Version</span></span><br/> | <span data-ttu-id="37717-117">Windows Media Player per Windows XP o versione successiva</span><span class="sxs-lookup"><span data-stu-id="37717-117">Windows Media Player for Windows XP or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="37717-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="37717-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37717-119">**LISTBOX (elemento)**</span><span class="sxs-lookup"><span data-stu-id="37717-119">**LISTBOX Element**</span></span>](listbox-element.md)
</dt> </dl>

 

 





