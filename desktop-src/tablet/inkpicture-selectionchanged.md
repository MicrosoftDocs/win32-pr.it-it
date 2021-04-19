---
description: Si verifica in seguito alla modifica della selezione dell'input penna all'interno del controllo InkPicture, ad esempio tramite le modifiche all'interfaccia utente, le procedure taglia e incolla o la proprietà di selezione.
ms.assetid: e300ec91-e8f3-473f-b526-efeafafaa32a
title: Evento InkPicture. SelectionChanged (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14594efe4e5ecda64167ec9a0e075fc60d8e9a19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317943"
---
# <a name="inkpictureselectionchanged-event"></a><span data-ttu-id="db56c-103">Evento InkPicture. SelectionChanged</span><span class="sxs-lookup"><span data-stu-id="db56c-103">InkPicture.SelectionChanged event</span></span>

<span data-ttu-id="db56c-104">Si verifica in seguito alla modifica della selezione dell'input penna all'interno del controllo [InkPicture](inkpicture-control-reference.md) , ad esempio tramite le modifiche all'interfaccia utente, le procedure taglia e incolla o la proprietà di [**selezione**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) .</span><span class="sxs-lookup"><span data-stu-id="db56c-104">Occurs when the selection of ink within the [InkPicture](inkpicture-control-reference.md) control has changed, such as through alterations to the user interface, cut-and-paste procedures, or the [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="db56c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="db56c-105">Syntax</span></span>


```C++
void SelectionChanged();
```



## <a name="parameters"></a><span data-ttu-id="db56c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="db56c-106">Parameters</span></span>

<span data-ttu-id="db56c-107">Questo evento non contiene parametri.</span><span class="sxs-lookup"><span data-stu-id="db56c-107">This event has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="db56c-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="db56c-108">Return value</span></span>

<span data-ttu-id="db56c-109">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="db56c-109">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="db56c-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="db56c-110">Remarks</span></span>

<span data-ttu-id="db56c-111">Per ulteriori informazioni su questo evento, vedere l'evento [**SelectionChanged**](inkoverlay-selectionchanged.md) dell'oggetto [**InkOverlay**](inkoverlay-class.md) , che ha la stessa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="db56c-111">For further details about this event, refer to the [**InkOverlay**](inkoverlay-class.md) object's [**SelectionChanged**](inkoverlay-selectionchanged.md) event, which has the same functionality.</span></span>

## <a name="requirements"></a><span data-ttu-id="db56c-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="db56c-112">Requirements</span></span>



| <span data-ttu-id="db56c-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="db56c-113">Requirement</span></span> | <span data-ttu-id="db56c-114">Valore</span><span class="sxs-lookup"><span data-stu-id="db56c-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="db56c-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="db56c-115">Minimum supported client</span></span><br/> | <span data-ttu-id="db56c-116">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="db56c-116">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="db56c-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="db56c-117">Minimum supported server</span></span><br/> | <span data-ttu-id="db56c-118">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="db56c-118">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="db56c-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="db56c-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="db56c-120"><dt>Msinkaut. h (richiede anche Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="db56c-120"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="db56c-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="db56c-121">Library</span></span><br/>                  | <dl> <span data-ttu-id="db56c-122"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="db56c-122"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="db56c-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="db56c-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db56c-124">InkPicture</span><span class="sxs-lookup"><span data-stu-id="db56c-124">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

<span data-ttu-id="db56c-125">[**Controllo InkPicture della proprietà Selection \[\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)</span><span class="sxs-lookup"><span data-stu-id="db56c-125">[**Selection Property \[InkPicture Control\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)</span></span>
</dt> </dl>

 

 




