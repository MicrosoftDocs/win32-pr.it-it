---
title: CASELLA. getLineIndex
description: Il metodo getLineIndex recupera l'indice dei caratteri del primo carattere nella riga con l'indice di riga specificato.
ms.assetid: 1298227a-d839-44fc-bacb-44c3c968bd94
keywords:
- Media Player Windows casella. getLineIndex
topic_type:
- apiref
api_name:
- EDITBOX.getLineIndex
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5f55027bb7d577b7080ad2f006a5a006e718c2d5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333853"
---
# <a name="editboxgetlineindex"></a><span data-ttu-id="7c950-104">CASELLA. getLineIndex</span><span class="sxs-lookup"><span data-stu-id="7c950-104">EDITBOX.getLineIndex</span></span>

<span data-ttu-id="7c950-105">Il metodo **getLineIndex** recupera l'indice dei caratteri del primo carattere nella riga con l'indice di riga specificato.</span><span class="sxs-lookup"><span data-stu-id="7c950-105">The **getLineIndex** method retrieves the character index of the first character on the line with the specified line index.</span></span>

``` syntax
        elementID.getLineIndex(index)
```

## <a name="parameters"></a><span data-ttu-id="7c950-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="7c950-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c950-107"><span id="index"></span><span id="INDEX"></span>*Indice*</span><span class="sxs-lookup"><span data-stu-id="7c950-107"><span id="index"></span><span id="INDEX"></span>*index*</span></span>
</dt> <dd>

<span data-ttu-id="7c950-108">**Numero** (**Long**) che contiene l'indice della riga di cui deve essere recuperato l'indice dei caratteri.</span><span class="sxs-lookup"><span data-stu-id="7c950-108">**Number** (**long**) containing the index of the line whose character index is to be retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c950-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7c950-109">Return Value</span></span>

<span data-ttu-id="7c950-110">Questo metodo restituisce un **numero** (**Long**).</span><span class="sxs-lookup"><span data-stu-id="7c950-110">This method returns a **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="7c950-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="7c950-111">Remarks</span></span>

<span data-ttu-id="7c950-112">Se l'indice di riga specificato è 1, viene utilizzata la riga contenente il punto di inserimento.</span><span class="sxs-lookup"><span data-stu-id="7c950-112">If the specified line index is  1, the line containing the insertion point is used.</span></span>

<span data-ttu-id="7c950-113">Questo metodo può essere chiamato solo dopo che il controllo diventa visibile.</span><span class="sxs-lookup"><span data-stu-id="7c950-113">This method can only be called after the control becomes visible.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c950-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7c950-114">Requirements</span></span>



| <span data-ttu-id="7c950-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c950-115">Requirement</span></span> | <span data-ttu-id="7c950-116">Valore</span><span class="sxs-lookup"><span data-stu-id="7c950-116">Value</span></span> |
|--------------------|---------------------------------------------------------|
| <span data-ttu-id="7c950-117">Versione</span><span class="sxs-lookup"><span data-stu-id="7c950-117">Version</span></span><br/> | <span data-ttu-id="7c950-118">Windows Media Player per Windows XP o versione successiva</span><span class="sxs-lookup"><span data-stu-id="7c950-118">Windows Media Player for Windows XP or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7c950-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7c950-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c950-120">**Elemento casella**</span><span class="sxs-lookup"><span data-stu-id="7c950-120">**EDITBOX Element**</span></span>](editbox-element.md)
</dt> <dt>

[<span data-ttu-id="7c950-121">**CASELLA. getline**</span><span class="sxs-lookup"><span data-stu-id="7c950-121">**EDITBOX.getLine**</span></span>](editbox-getline.md)
</dt> <dt>

[<span data-ttu-id="7c950-122">**CASELLA. getLineFromChar**</span><span class="sxs-lookup"><span data-stu-id="7c950-122">**EDITBOX.getLineFromChar**</span></span>](editbox-getlinefromchar.md)
</dt> </dl>

 

 





