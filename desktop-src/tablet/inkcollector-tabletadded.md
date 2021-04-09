---
description: Si verifica quando un IInkTablet viene aggiunto al sistema.
ms.assetid: c5f90fce-faf7-411b-a4d6-deb5d0f22f4a
title: Evento InkCollector. TabletAdded (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f18f66a45570b269d36efc012f543a8b25e23f70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966510"
---
# <a name="inkcollectortabletadded-event"></a><span data-ttu-id="64c8e-103">Evento InkCollector. TabletAdded</span><span class="sxs-lookup"><span data-stu-id="64c8e-103">InkCollector.TabletAdded event</span></span>

<span data-ttu-id="64c8e-104">Si verifica quando un [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) viene aggiunto al sistema.</span><span class="sxs-lookup"><span data-stu-id="64c8e-104">Occurs when a [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) is added to the system.</span></span>

## <a name="syntax"></a><span data-ttu-id="64c8e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="64c8e-105">Syntax</span></span>


```C++
void TabletAdded(
  [in] IInkTablet *Tablet
);
```



## <a name="parameters"></a><span data-ttu-id="64c8e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="64c8e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64c8e-107">*Tablet* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="64c8e-107">*Tablet* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64c8e-108">Oggetto [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) aggiunto al sistema.</span><span class="sxs-lookup"><span data-stu-id="64c8e-108">The [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) object that has been added to the system.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="64c8e-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="64c8e-109">Return value</span></span>

<span data-ttu-id="64c8e-110">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="64c8e-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="64c8e-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="64c8e-111">Remarks</span></span>

<span data-ttu-id="64c8e-112">Questo metodo di evento è definito nelle \_ interfacce IInkCollectorEvents, \_ IInkOverlayEvents e \_ IInkPictureEvents dispatch (DISPINTERFACES) con ID DISPID \_ ICETabletAdded.</span><span class="sxs-lookup"><span data-stu-id="64c8e-112">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICETabletAdded.</span></span>

## <a name="requirements"></a><span data-ttu-id="64c8e-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="64c8e-113">Requirements</span></span>



| <span data-ttu-id="64c8e-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="64c8e-114">Requirement</span></span> | <span data-ttu-id="64c8e-115">Valore</span><span class="sxs-lookup"><span data-stu-id="64c8e-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="64c8e-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="64c8e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="64c8e-117">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="64c8e-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="64c8e-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="64c8e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="64c8e-119">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="64c8e-119">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="64c8e-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="64c8e-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="64c8e-121"><dt>Msinkaut. h (richiede anche Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="64c8e-121"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="64c8e-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="64c8e-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="64c8e-123"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="64c8e-123"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="64c8e-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="64c8e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64c8e-125">**Classe InkCollector**</span><span class="sxs-lookup"><span data-stu-id="64c8e-125">**InkCollector Class**</span></span>](inkcollector-class.md)
</dt> <dt>

[<span data-ttu-id="64c8e-126">**Interfaccia IInkTablet**</span><span class="sxs-lookup"><span data-stu-id="64c8e-126">**IInkTablet Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet)
</dt> </dl>

 

 




