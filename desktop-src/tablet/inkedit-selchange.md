---
description: Si verifica quando la selezione corrente del testo nel controllo InkEdit è stata modificata o se il punto di inserimento è stato spostato.
ms.assetid: 14ddffe7-bdfe-4a35-82c7-b3401b5b720c
title: Evento InkEdit. SelChange (inchiostrata. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66b51ef4edbf7d7fb02be17dc416c0a777a9519a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313939"
---
# <a name="inkeditselchange-event"></a><span data-ttu-id="8becb-103">Evento InkEdit. SelChange</span><span class="sxs-lookup"><span data-stu-id="8becb-103">InkEdit.SelChange event</span></span>

<span data-ttu-id="8becb-104">Si verifica quando la selezione corrente del testo nel controllo [InkEdit](inkedit-control-reference.md) è stata modificata o se il punto di inserimento è stato spostato.</span><span class="sxs-lookup"><span data-stu-id="8becb-104">Occurs when the current selection of text in the [InkEdit](inkedit-control-reference.md) control has changed or the insertion point has moved.</span></span>

## <a name="syntax"></a><span data-ttu-id="8becb-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8becb-105">Syntax</span></span>


```C++
void SelChange();
```



## <a name="parameters"></a><span data-ttu-id="8becb-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="8becb-106">Parameters</span></span>

<span data-ttu-id="8becb-107">Questo evento non contiene parametri.</span><span class="sxs-lookup"><span data-stu-id="8becb-107">This event has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8becb-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8becb-108">Return value</span></span>

<span data-ttu-id="8becb-109">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="8becb-109">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8becb-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="8becb-110">Remarks</span></span>

<span data-ttu-id="8becb-111">È possibile utilizzare l'evento **selChange** per verificare le varie proprietà che forniscono informazioni sulla selezione corrente (ad esempio [**Selbold**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selbold)), in modo che sia possibile aggiornare i pulsanti in una barra degli strumenti, ad esempio.</span><span class="sxs-lookup"><span data-stu-id="8becb-111">You can use the **SelChange** event to check the various properties that give information about the current selection (such as [**SelBold**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selbold)) so you can update buttons in a toolbar, for example.</span></span>

## <a name="requirements"></a><span data-ttu-id="8becb-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8becb-112">Requirements</span></span>



| <span data-ttu-id="8becb-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="8becb-113">Requirement</span></span> | <span data-ttu-id="8becb-114">Valore</span><span class="sxs-lookup"><span data-stu-id="8becb-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8becb-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8becb-115">Minimum supported client</span></span><br/> | <span data-ttu-id="8becb-116">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="8becb-116">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="8becb-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8becb-117">Minimum supported server</span></span><br/> | <span data-ttu-id="8becb-118">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="8becb-118">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="8becb-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8becb-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="8becb-120"><dt>Inchiostrato. h (richiede anche il \_ . c)</dt></span><span class="sxs-lookup"><span data-stu-id="8becb-120"><dt>Inked.h (also requires inked\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="8becb-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="8becb-121">Library</span></span><br/>                  | <dl> <span data-ttu-id="8becb-122"><dt>InkEd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8becb-122"><dt>InkEd.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="8becb-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8becb-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8becb-124">InkEdit</span><span class="sxs-lookup"><span data-stu-id="8becb-124">InkEdit</span></span>](inkedit-control-reference.md)
</dt> </dl>

 

 




