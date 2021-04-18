---
title: CASELLA. getLineFromChar
description: Il metodo getLineFromChar recupera l'indice di riga per l'indice dei caratteri specificato.
ms.assetid: c3a29bdf-ff63-4b6d-90e8-d414dde87f85
keywords:
- Media Player Windows casella. getLineFromChar
topic_type:
- apiref
api_name:
- EDITBOX.getLineFromChar
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3462ce628da72ca1e55df79e408fc79e0ec8b63a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333852"
---
# <a name="editboxgetlinefromchar"></a><span data-ttu-id="3b5a2-104">CASELLA. getLineFromChar</span><span class="sxs-lookup"><span data-stu-id="3b5a2-104">EDITBOX.getLineFromChar</span></span>

<span data-ttu-id="3b5a2-105">Il metodo **getLineFromChar** recupera l'indice di riga per l'indice dei caratteri specificato.</span><span class="sxs-lookup"><span data-stu-id="3b5a2-105">The **getLineFromChar** method retrieves the line index for the specified character index.</span></span>

``` syntax
        elementID.getLineFromChar(index)
```

## <a name="parameters"></a><span data-ttu-id="3b5a2-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3b5a2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b5a2-107"><span id="index"></span><span id="INDEX"></span>*Indice*</span><span class="sxs-lookup"><span data-stu-id="3b5a2-107"><span id="index"></span><span id="INDEX"></span>*index*</span></span>
</dt> <dd>

<span data-ttu-id="3b5a2-108">**Numero** (**Long**) che contiene l'indice del carattere il cui indice di riga deve essere recuperato.</span><span class="sxs-lookup"><span data-stu-id="3b5a2-108">**Number** (**long**) containing the index of the character whose line index is to be retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b5a2-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3b5a2-109">Return Value</span></span>

<span data-ttu-id="3b5a2-110">Questo metodo restituisce un **numero** (**Long**).</span><span class="sxs-lookup"><span data-stu-id="3b5a2-110">This method returns a **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="3b5a2-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="3b5a2-111">Remarks</span></span>

<span data-ttu-id="3b5a2-112">Se la posizione del carattere specificata è 1, questo metodo recupera l'indice di riga della riga corrente.</span><span class="sxs-lookup"><span data-stu-id="3b5a2-112">If the specified character position is  1, this method retrieves the line index of the current line.</span></span>

<span data-ttu-id="3b5a2-113">Questo metodo può essere chiamato solo dopo che il controllo diventa visibile.</span><span class="sxs-lookup"><span data-stu-id="3b5a2-113">This method can only be called after the control becomes visible.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b5a2-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3b5a2-114">Requirements</span></span>



| <span data-ttu-id="3b5a2-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b5a2-115">Requirement</span></span> | <span data-ttu-id="3b5a2-116">Valore</span><span class="sxs-lookup"><span data-stu-id="3b5a2-116">Value</span></span> |
|--------------------|---------------------------------------------------------|
| <span data-ttu-id="3b5a2-117">Versione</span><span class="sxs-lookup"><span data-stu-id="3b5a2-117">Version</span></span><br/> | <span data-ttu-id="3b5a2-118">Windows Media Player per Windows XP o versione successiva</span><span class="sxs-lookup"><span data-stu-id="3b5a2-118">Windows Media Player for Windows XP or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3b5a2-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3b5a2-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b5a2-120">**Elemento casella**</span><span class="sxs-lookup"><span data-stu-id="3b5a2-120">**EDITBOX Element**</span></span>](editbox-element.md)
</dt> <dt>

[<span data-ttu-id="3b5a2-121">**CASELLA. getline**</span><span class="sxs-lookup"><span data-stu-id="3b5a2-121">**EDITBOX.getLine**</span></span>](editbox-getline.md)
</dt> <dt>

[<span data-ttu-id="3b5a2-122">**CASELLA. getLineIndex**</span><span class="sxs-lookup"><span data-stu-id="3b5a2-122">**EDITBOX.getLineIndex**</span></span>](editbox-getlineindex.md)
</dt> </dl>

 

 





