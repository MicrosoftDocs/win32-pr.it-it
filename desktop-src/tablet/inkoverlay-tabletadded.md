---
description: 'Evento InkOverlay.TabletAdded: si verifica quando un oggetto IInkTablet viene aggiunto al sistema.'
ms.assetid: 2076a520-bd37-43b5-b57f-030828b096cb
title: Evento InkOverlay.TabletAdded (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c22630430622c98026c81adb1c6a131a53277a4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116789"
---
# <a name="inkoverlaytabletadded-event"></a><span data-ttu-id="66d16-103">Evento InkOverlay.TabletAdded</span><span class="sxs-lookup"><span data-stu-id="66d16-103">InkOverlay.TabletAdded event</span></span>

<span data-ttu-id="66d16-104">Si verifica quando [**un oggetto IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) viene aggiunto al sistema.</span><span class="sxs-lookup"><span data-stu-id="66d16-104">Occurs when a [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) is added to the system.</span></span>

## <a name="syntax"></a><span data-ttu-id="66d16-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="66d16-105">Syntax</span></span>


```C++
void TabletAdded(
  [in] IInkTablet *Tablet
);
```



## <a name="parameters"></a><span data-ttu-id="66d16-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="66d16-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66d16-107">*Tablet* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="66d16-107">*Tablet* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66d16-108">Oggetto [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) aggiunto al sistema.</span><span class="sxs-lookup"><span data-stu-id="66d16-108">The [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) object that has been added to the system.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66d16-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="66d16-109">Return value</span></span>

<span data-ttu-id="66d16-110">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="66d16-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="66d16-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="66d16-111">Remarks</span></span>

<span data-ttu-id="66d16-112">Questo metodo di evento è definito nelle interfacce di solo invio \_ IInkCollectorEvents, \_ IInkOverlayEvents e \_ IInkPictureEvents (interfacce dispatch) con ID DISPID \_ ICETabletAdded.</span><span class="sxs-lookup"><span data-stu-id="66d16-112">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICETabletAdded.</span></span>

## <a name="requirements"></a><span data-ttu-id="66d16-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="66d16-113">Requirements</span></span>



| <span data-ttu-id="66d16-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="66d16-114">Requirement</span></span> | <span data-ttu-id="66d16-115">Valore</span><span class="sxs-lookup"><span data-stu-id="66d16-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66d16-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="66d16-116">Minimum supported client</span></span><br/> | <span data-ttu-id="66d16-117">Solo app desktop di Windows XP Tablet PC \[ Edition\]</span><span class="sxs-lookup"><span data-stu-id="66d16-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="66d16-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="66d16-118">Minimum supported server</span></span><br/> | <span data-ttu-id="66d16-119">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="66d16-119">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="66d16-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="66d16-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="66d16-121"><dt>Msinkaut.h (richiede anche Msinkaut \_ i.c)</dt></span><span class="sxs-lookup"><span data-stu-id="66d16-121"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="66d16-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="66d16-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="66d16-123"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="66d16-123"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="66d16-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="66d16-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66d16-125">**Classe InkOverlay**</span><span class="sxs-lookup"><span data-stu-id="66d16-125">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="66d16-126">**Interfaccia IInkTablet**</span><span class="sxs-lookup"><span data-stu-id="66d16-126">**IInkTablet Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet)
</dt> </dl>

 

 




