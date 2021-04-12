---
description: Un handle HRECOWORDLIST viene usato per gestire un elenco di parole collegato a un contesto di riconoscimento. Per migliorare i risultati del riconoscimento, usare un elenco di parole.
ms.assetid: 7333307b-1857-48a7-bb9f-bdbd8530f093
title: Handle HRECOWORDLIST (riepilogo. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5e5d33862cacb7040a26edc23d7db04c57206c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526574"
---
# <a name="hrecowordlist-handle"></a><span data-ttu-id="5433c-104">Handle HRECOWORDLIST</span><span class="sxs-lookup"><span data-stu-id="5433c-104">HRECOWORDLIST Handle</span></span>

<span data-ttu-id="5433c-105">Un handle **HRECOWORDLIST** viene usato per gestire un elenco di parole collegato a un contesto di riconoscimento.</span><span class="sxs-lookup"><span data-stu-id="5433c-105">An **HRECOWORDLIST** handle is used to manage a word list you attach to a recognizer context.</span></span> <span data-ttu-id="5433c-106">Per migliorare i risultati del riconoscimento, usare un elenco di parole.</span><span class="sxs-lookup"><span data-stu-id="5433c-106">You use a word list to improve recognition results.</span></span>


```C++
typedef HANDLE HRECOWORDLIST;
```



## <a name="remarks"></a><span data-ttu-id="5433c-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="5433c-107">Remarks</span></span>

<span data-ttu-id="5433c-108">La funzione seguente usa un **HRECOWORDLIST**.</span><span class="sxs-lookup"><span data-stu-id="5433c-108">The following function use an **HRECOWORDLIST**.</span></span>



| <span data-ttu-id="5433c-109">Funzione</span><span class="sxs-lookup"><span data-stu-id="5433c-109">Function</span></span>                                         | <span data-ttu-id="5433c-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5433c-110">Description</span></span>                                         |
|--------------------------------------------------|-----------------------------------------------------|
| [<span data-ttu-id="5433c-111">**AddWordsToWordList**</span><span class="sxs-lookup"><span data-stu-id="5433c-111">**AddWordsToWordList**</span></span>](/windows/desktop/api/recapis/nf-recapis-addwordstowordlist) | <span data-ttu-id="5433c-112">Aggiunge una o più parole all'elenco di parole.</span><span class="sxs-lookup"><span data-stu-id="5433c-112">Adds one or more words to the word list.</span></span><br/> |
| [<span data-ttu-id="5433c-113">**DestroyWordList**</span><span class="sxs-lookup"><span data-stu-id="5433c-113">**DestroyWordList**</span></span>](/windows/desktop/api/recapis/nf-recapis-destroywordlist)       | <span data-ttu-id="5433c-114">Elimina definitivamente l'elenco di parole corrente.</span><span class="sxs-lookup"><span data-stu-id="5433c-114">Destroys the current word list.</span></span><br/>          |
| [<span data-ttu-id="5433c-115">**MakeWordList**</span><span class="sxs-lookup"><span data-stu-id="5433c-115">**MakeWordList**</span></span>](/windows/desktop/api/recapis/nf-recapis-makewordlist)             | <span data-ttu-id="5433c-116">Crea un elenco di parole.</span><span class="sxs-lookup"><span data-stu-id="5433c-116">Creates a word list.</span></span><br/>                     |



 

## <a name="requirements"></a><span data-ttu-id="5433c-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5433c-117">Requirements</span></span>



| <span data-ttu-id="5433c-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="5433c-118">Requirement</span></span> | <span data-ttu-id="5433c-119">Valore</span><span class="sxs-lookup"><span data-stu-id="5433c-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="5433c-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5433c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="5433c-121">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="5433c-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                        |
| <span data-ttu-id="5433c-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5433c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="5433c-123">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="5433c-123">None supported</span></span><br/>                                                            |
| <span data-ttu-id="5433c-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5433c-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="5433c-125"><dt>Riepilogo. h</dt></span><span class="sxs-lookup"><span data-stu-id="5433c-125"><dt>Recapis.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5433c-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5433c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5433c-127">**Funzione WordList**</span><span class="sxs-lookup"><span data-stu-id="5433c-127">**SetWordList Function**</span></span>](/windows/desktop/api/recapis/nf-recapis-setwordlist)
</dt> </dl>

 

 




