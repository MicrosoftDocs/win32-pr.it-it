---
description: 'Evento InkCollector.TabletAdded: si verifica quando viene aggiunto un oggetto IInkTablet al sistema.'
ms.assetid: c5f90fce-faf7-411b-a4d6-deb5d0f22f4a
title: Evento InkCollector.TabletAdded (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad3088eff151d9857f8a1449d3c99805c949b790
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110009"
---
# <a name="inkcollectortabletadded-event"></a><span data-ttu-id="20621-103">Evento InkCollector.TabletAdded</span><span class="sxs-lookup"><span data-stu-id="20621-103">InkCollector.TabletAdded event</span></span>

<span data-ttu-id="20621-104">Si verifica quando [**un oggetto IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) viene aggiunto al sistema.</span><span class="sxs-lookup"><span data-stu-id="20621-104">Occurs when a [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) is added to the system.</span></span>

## <a name="syntax"></a><span data-ttu-id="20621-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="20621-105">Syntax</span></span>


```C++
void TabletAdded(
  [in] IInkTablet *Tablet
);
```



## <a name="parameters"></a><span data-ttu-id="20621-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="20621-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20621-107">*Tablet* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="20621-107">*Tablet* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20621-108">Oggetto [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) aggiunto al sistema.</span><span class="sxs-lookup"><span data-stu-id="20621-108">The [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) object that has been added to the system.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20621-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="20621-109">Return value</span></span>

<span data-ttu-id="20621-110">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="20621-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="20621-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="20621-111">Remarks</span></span>

<span data-ttu-id="20621-112">Questo metodo di evento è definito nelle interfacce di solo invio \_ IInkCollectorEvents, \_ IInkOverlayEvents e \_ IInkPictureEvents (interfacce dispatch) con ID \_ DISPID ICETabletAdded.</span><span class="sxs-lookup"><span data-stu-id="20621-112">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICETabletAdded.</span></span>

## <a name="requirements"></a><span data-ttu-id="20621-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="20621-113">Requirements</span></span>



| <span data-ttu-id="20621-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="20621-114">Requirement</span></span> | <span data-ttu-id="20621-115">Valore</span><span class="sxs-lookup"><span data-stu-id="20621-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20621-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="20621-116">Minimum supported client</span></span><br/> | <span data-ttu-id="20621-117">Solo app desktop Windows XP Tablet PC \[ Edition\]</span><span class="sxs-lookup"><span data-stu-id="20621-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="20621-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="20621-118">Minimum supported server</span></span><br/> | <span data-ttu-id="20621-119">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="20621-119">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="20621-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="20621-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="20621-121"><dt>Msinkaut.h (richiede anche Msinkaut \_ i.c)</dt></span><span class="sxs-lookup"><span data-stu-id="20621-121"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="20621-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="20621-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="20621-123"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="20621-123"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="20621-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="20621-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20621-125">**Classe InkCollector**</span><span class="sxs-lookup"><span data-stu-id="20621-125">**InkCollector Class**</span></span>](inkcollector-class.md)
</dt> <dt>

[<span data-ttu-id="20621-126">**Interfaccia IInkTablet**</span><span class="sxs-lookup"><span data-stu-id="20621-126">**IInkTablet Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet)
</dt> </dl>

 

 




