---
title: CASELLA. getline
description: Il metodo getline Recupera il testo per la riga con l'indice specificato.
ms.assetid: a692c32b-86b9-419e-a3a5-464687be04da
keywords:
- CASELLA. getline Media Player Windows
topic_type:
- apiref
api_name:
- EDITBOX.getLine
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3b0b9a15f9eff8c2612e7a242a205c1d9411a60c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325256"
---
# <a name="editboxgetline"></a><span data-ttu-id="1064d-104">CASELLA. getline</span><span class="sxs-lookup"><span data-stu-id="1064d-104">EDITBOX.getLine</span></span>

<span data-ttu-id="1064d-105">Il metodo **getline** Recupera il testo per la riga con l'indice specificato.</span><span class="sxs-lookup"><span data-stu-id="1064d-105">The **getLine** method retrieves the text for the line with the specified index.</span></span>

``` syntax
        elementID.getLine(index)
```

## <a name="parameters"></a><span data-ttu-id="1064d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="1064d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1064d-107"><span id="index"></span><span id="INDEX"></span>*Indice*</span><span class="sxs-lookup"><span data-stu-id="1064d-107"><span id="index"></span><span id="INDEX"></span>*index*</span></span>
</dt> <dd>

<span data-ttu-id="1064d-108">**Numero** (**Long**) che contiene l'indice della riga da recuperare.</span><span class="sxs-lookup"><span data-stu-id="1064d-108">**Number** (**long**) containing the index of the line to retrieve.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1064d-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1064d-109">Return Value</span></span>

<span data-ttu-id="1064d-110">Questo metodo restituisce una **stringa**.</span><span class="sxs-lookup"><span data-stu-id="1064d-110">This method returns a **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="1064d-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="1064d-111">Remarks</span></span>

<span data-ttu-id="1064d-112">Se l'indice non è valido, viene restituita una stringa vuota.</span><span class="sxs-lookup"><span data-stu-id="1064d-112">If the index is not valid, an empty string is returned.</span></span> <span data-ttu-id="1064d-113">Questo metodo può essere chiamato solo dopo che il controllo diventa visibile.</span><span class="sxs-lookup"><span data-stu-id="1064d-113">This method can only be called after the control becomes visible.</span></span>

## <a name="requirements"></a><span data-ttu-id="1064d-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1064d-114">Requirements</span></span>



| <span data-ttu-id="1064d-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="1064d-115">Requirement</span></span> | <span data-ttu-id="1064d-116">Valore</span><span class="sxs-lookup"><span data-stu-id="1064d-116">Value</span></span> |
|--------------------|---------------------------------------------------------|
| <span data-ttu-id="1064d-117">Versione</span><span class="sxs-lookup"><span data-stu-id="1064d-117">Version</span></span><br/> | <span data-ttu-id="1064d-118">Windows Media Player per Windows XP o versione successiva</span><span class="sxs-lookup"><span data-stu-id="1064d-118">Windows Media Player for Windows XP or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1064d-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1064d-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1064d-120">**Elemento casella**</span><span class="sxs-lookup"><span data-stu-id="1064d-120">**EDITBOX Element**</span></span>](editbox-element.md)
</dt> <dt>

[<span data-ttu-id="1064d-121">**CASELLA. getLineFromChar**</span><span class="sxs-lookup"><span data-stu-id="1064d-121">**EDITBOX.getLineFromChar**</span></span>](editbox-getlinefromchar.md)
</dt> <dt>

[<span data-ttu-id="1064d-122">**CASELLA. getLineIndex**</span><span class="sxs-lookup"><span data-stu-id="1064d-122">**EDITBOX.getLineIndex**</span></span>](editbox-getlineindex.md)
</dt> </dl>

 

 





