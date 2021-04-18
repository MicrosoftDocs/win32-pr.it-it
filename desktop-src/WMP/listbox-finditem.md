---
title: LISTBOX. findItem
description: Il metodo findItem cerca una determinata stringa a partire dall'elemento che segue l'indice dell'elemento specificato.
ms.assetid: 8d112d99-1866-45e5-b0ef-5d4a3c8b388d
keywords:
- Media Player di Windows LISTBOX. findItem
topic_type:
- apiref
api_name:
- LISTBOX.findItem
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 161f4dd8b93fe4fed6a794dffde3e58e840c74e5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327759"
---
# <a name="listboxfinditem"></a><span data-ttu-id="58025-104">LISTBOX. findItem</span><span class="sxs-lookup"><span data-stu-id="58025-104">LISTBOX.findItem</span></span>

<span data-ttu-id="58025-105">Il metodo **FindItem** cerca una determinata stringa a partire dall'elemento che segue l'indice dell'elemento specificato.</span><span class="sxs-lookup"><span data-stu-id="58025-105">The **findItem** method searches for a given string starting with the item following the specified item index.</span></span>

``` syntax
        elementID.findItem(startIndex, searchString)
```

## <a name="parameters"></a><span data-ttu-id="58025-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="58025-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58025-107"><span id="startIndex"></span><span id="startindex"></span><span id="STARTINDEX"></span>*startIndex*</span><span class="sxs-lookup"><span data-stu-id="58025-107"><span id="startIndex"></span><span id="startindex"></span><span id="STARTINDEX"></span>*startIndex*</span></span>
</dt> <dd>

<span data-ttu-id="58025-108">**Numero** (**Long**) che contiene l'indice dell'elemento da cui iniziare la ricerca.</span><span class="sxs-lookup"><span data-stu-id="58025-108">**Number** (**long**) containing the index of the item at which to start the search.</span></span>

</dd> <dt>

<span data-ttu-id="58025-109"><span id="searchString"></span><span id="searchstring"></span><span id="SEARCHSTRING"></span>*searchString*</span><span class="sxs-lookup"><span data-stu-id="58025-109"><span id="searchString"></span><span id="searchstring"></span><span id="SEARCHSTRING"></span>*searchString*</span></span>
</dt> <dd>

<span data-ttu-id="58025-110">**Stringa** contenente il testo da ricercare.</span><span class="sxs-lookup"><span data-stu-id="58025-110">**String** containing the text to search for.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58025-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="58025-111">Return Value</span></span>

<span data-ttu-id="58025-112">Questo metodo restituisce un **numero** (**Long**) contenente l'indice dell'elemento che contiene la stringa.</span><span class="sxs-lookup"><span data-stu-id="58025-112">This method returns a **Number** (**long**) containing the index of the item that contains the string.</span></span>

## <a name="remarks"></a><span data-ttu-id="58025-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="58025-113">Remarks</span></span>

<span data-ttu-id="58025-114">Per avviare la ricerca nella prima riga del controllo casella di riepilogo, utilizzare 1 come *startIndex*.</span><span class="sxs-lookup"><span data-stu-id="58025-114">To start the search at the first line of the list box control, use  1 as the *startIndex*.</span></span> <span data-ttu-id="58025-115">Per continuare a cercare testo dopo aver trovato la prima riga, usare l'indice di riga restituito come *startIndex* e la ricerca verrà avviata nella riga successiva.</span><span class="sxs-lookup"><span data-stu-id="58025-115">To continue to search for text after the first line is found, use the returned line index as the *startIndex*, and the search will start at the next line.</span></span> <span data-ttu-id="58025-116">Questo metodo effettuerà la ricerca di sottostringhe e non distingue tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="58025-116">This method will search for substrings and is not case-sensitive.</span></span>

## <a name="requirements"></a><span data-ttu-id="58025-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="58025-117">Requirements</span></span>



| <span data-ttu-id="58025-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="58025-118">Requirement</span></span> | <span data-ttu-id="58025-119">Valore</span><span class="sxs-lookup"><span data-stu-id="58025-119">Value</span></span> |
|--------------------|---------------------------------------------------------|
| <span data-ttu-id="58025-120">Versione</span><span class="sxs-lookup"><span data-stu-id="58025-120">Version</span></span><br/> | <span data-ttu-id="58025-121">Windows Media Player per Windows XP o versione successiva</span><span class="sxs-lookup"><span data-stu-id="58025-121">Windows Media Player for Windows XP or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="58025-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="58025-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58025-123">**LISTBOX (elemento)**</span><span class="sxs-lookup"><span data-stu-id="58025-123">**LISTBOX Element**</span></span>](listbox-element.md)
</dt> </dl>

 

 





