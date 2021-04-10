---
description: Si verifica quando la selezione dell'input penna all'interno del controllo InkPicture sta per essere modificata, ad esempio tramite le modifiche all'interfaccia utente, le procedure taglia e incolla o la proprietà di selezione.
ms.assetid: a8ae30ff-fb0d-44cc-a5d3-295117addafd
title: Evento InkPicture. SelectionChanging (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37b8a35d57aeb9367bb9d30647cb074a7e0e6fbd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884933"
---
# <a name="inkpictureselectionchanging-event"></a><span data-ttu-id="17ef8-103">Evento InkPicture. SelectionChanging</span><span class="sxs-lookup"><span data-stu-id="17ef8-103">InkPicture.SelectionChanging event</span></span>

<span data-ttu-id="17ef8-104">Si verifica quando la selezione dell'input penna all'interno del controllo [InkPicture](inkpicture-control-reference.md) sta per essere modificata, ad esempio tramite le modifiche all'interfaccia utente, le procedure taglia e incolla o la proprietà di [**selezione**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) .</span><span class="sxs-lookup"><span data-stu-id="17ef8-104">Occurs when the selection of ink within the [InkPicture](inkpicture-control-reference.md) control is about to change, such as through alterations to the user interface, cut-and-paste procedures, or the [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="17ef8-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="17ef8-105">Syntax</span></span>


```C++
void SelectionChanging(
  [in] IInkStrokes *NewSelection
);
```



## <a name="parameters"></a><span data-ttu-id="17ef8-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="17ef8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17ef8-107">*NewSelection* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="17ef8-107">*NewSelection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17ef8-108">Nuova raccolta di [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) in corso di selezione.</span><span class="sxs-lookup"><span data-stu-id="17ef8-108">The new collection of [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) that is being selected.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17ef8-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="17ef8-109">Return value</span></span>

<span data-ttu-id="17ef8-110">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="17ef8-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="17ef8-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="17ef8-111">Remarks</span></span>

<span data-ttu-id="17ef8-112">Questo metodo di evento è definito nelle interfacce **\_ IInkOverlayEvents** e **\_ IInkPictureEvents** dispatch-only (dispinterfaces) con ID DISPID \_ IOESelectionChanging.</span><span class="sxs-lookup"><span data-stu-id="17ef8-112">This event method is defined in the **\_IInkOverlayEvents** and **\_IInkPictureEvents** dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IOESelectionChanging.</span></span>

## <a name="requirements"></a><span data-ttu-id="17ef8-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="17ef8-113">Requirements</span></span>



| <span data-ttu-id="17ef8-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="17ef8-114">Requirement</span></span> | <span data-ttu-id="17ef8-115">Valore</span><span class="sxs-lookup"><span data-stu-id="17ef8-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17ef8-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="17ef8-116">Minimum supported client</span></span><br/> | <span data-ttu-id="17ef8-117">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="17ef8-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="17ef8-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="17ef8-118">Minimum supported server</span></span><br/> | <span data-ttu-id="17ef8-119">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="17ef8-119">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="17ef8-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="17ef8-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="17ef8-121"><dt>Msinkaut. h (richiede anche Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="17ef8-121"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="17ef8-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="17ef8-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="17ef8-123"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="17ef8-123"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="17ef8-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="17ef8-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17ef8-125">InkPicture</span><span class="sxs-lookup"><span data-stu-id="17ef8-125">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

<span data-ttu-id="17ef8-126">[**Controllo InkPicture della proprietà Selection \[\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)</span><span class="sxs-lookup"><span data-stu-id="17ef8-126">[**Selection Property \[InkPicture Control\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)</span></span>
</dt> </dl>

 

