---
description: 'Evento InkCollector.TabletRemoved: si verifica quando un oggetto IInkTablet viene rimosso dal sistema.'
ms.assetid: 659a9809-fe35-4d34-aa95-af353998c350
title: Evento InkCollector.TabletRemoved (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df76c27b1a0d47e456f69a789d17ef6343706284
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109999"
---
# <a name="inkcollectortabletremoved-event"></a><span data-ttu-id="031fa-103">Evento InkCollector.TabletRemoved</span><span class="sxs-lookup"><span data-stu-id="031fa-103">InkCollector.TabletRemoved event</span></span>

<span data-ttu-id="031fa-104">Si verifica quando [**un oggetto IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) viene rimosso dal sistema.</span><span class="sxs-lookup"><span data-stu-id="031fa-104">Occurs when a [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) is removed from the system.</span></span>

## <a name="syntax"></a><span data-ttu-id="031fa-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="031fa-105">Syntax</span></span>


```C++
void TabletRemoved(
  [in] long TabletId
);
```



## <a name="parameters"></a><span data-ttu-id="031fa-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="031fa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="031fa-107">*TabletId* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="031fa-107">*TabletId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="031fa-108">Valore long utilizzato come ID per [**l'oggetto IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) rimosso.</span><span class="sxs-lookup"><span data-stu-id="031fa-108">The long value that was used as the ID for the [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) object that was removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="031fa-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="031fa-109">Return value</span></span>

<span data-ttu-id="031fa-110">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="031fa-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="031fa-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="031fa-111">Remarks</span></span>

<span data-ttu-id="031fa-112">Questo metodo di evento è definito nelle interfacce di solo invio \_ IInkCollectorEvents, \_ IInkOverlayEvents e \_ IInkPictureEvents (interfacce dispatch) con ID \_ DISPID ICETabletRemoved.</span><span class="sxs-lookup"><span data-stu-id="031fa-112">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICETabletRemoved.</span></span>

## <a name="requirements"></a><span data-ttu-id="031fa-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="031fa-113">Requirements</span></span>



| <span data-ttu-id="031fa-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="031fa-114">Requirement</span></span> | <span data-ttu-id="031fa-115">Valore</span><span class="sxs-lookup"><span data-stu-id="031fa-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="031fa-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="031fa-116">Minimum supported client</span></span><br/> | <span data-ttu-id="031fa-117">Solo app desktop di Windows XP Tablet PC \[ Edition\]</span><span class="sxs-lookup"><span data-stu-id="031fa-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="031fa-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="031fa-118">Minimum supported server</span></span><br/> | <span data-ttu-id="031fa-119">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="031fa-119">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="031fa-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="031fa-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="031fa-121"><dt>Msinkaut.h (richiede anche Msinkaut \_ i.c)</dt></span><span class="sxs-lookup"><span data-stu-id="031fa-121"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="031fa-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="031fa-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="031fa-123"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="031fa-123"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="031fa-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="031fa-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="031fa-125">**Classe InkCollector**</span><span class="sxs-lookup"><span data-stu-id="031fa-125">**InkCollector Class**</span></span>](inkcollector-class.md)
</dt> <dt>

[<span data-ttu-id="031fa-126">**Interfaccia IInkTablet**</span><span class="sxs-lookup"><span data-stu-id="031fa-126">**IInkTablet Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet)
</dt> </dl>

 

 




