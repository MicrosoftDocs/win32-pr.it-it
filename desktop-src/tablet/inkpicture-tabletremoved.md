---
description: Si verifica quando un IInkTablet viene rimosso dal sistema.
ms.assetid: 9a4640a7-cbd9-4304-88c6-86036423628d
title: Evento InkPicture. TabletRemoved (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e05b097b4dcf15c618e3316066be962b52803e27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233879"
---
# <a name="inkpicturetabletremoved-event"></a><span data-ttu-id="cef62-103">Evento InkPicture. TabletRemoved</span><span class="sxs-lookup"><span data-stu-id="cef62-103">InkPicture.TabletRemoved event</span></span>

<span data-ttu-id="cef62-104">Si verifica quando un [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) viene rimosso dal sistema.</span><span class="sxs-lookup"><span data-stu-id="cef62-104">Occurs when a [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) is removed from the system.</span></span>

## <a name="syntax"></a><span data-ttu-id="cef62-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cef62-105">Syntax</span></span>


```C++
void TabletRemoved(
  [in] long TabletId
);
```



## <a name="parameters"></a><span data-ttu-id="cef62-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="cef62-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cef62-107">*TabletId* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cef62-107">*TabletId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cef62-108">Valore Long utilizzato come ID per l'oggetto [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) che è stato rimosso.</span><span class="sxs-lookup"><span data-stu-id="cef62-108">The long value that was used as the ID for the [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) object that was removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cef62-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cef62-109">Return value</span></span>

<span data-ttu-id="cef62-110">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="cef62-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cef62-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="cef62-111">Remarks</span></span>

<span data-ttu-id="cef62-112">Questo metodo di evento è definito nelle interfacce **\_ IInkCollectorEvents**, **\_ IInkOverlayEvents** e **\_ IInkPictureEvents** dispatch (dispinterfaces) con ID DISPID \_ ICETabletRemoved.</span><span class="sxs-lookup"><span data-stu-id="cef62-112">This event method is defined in the **\_IInkCollectorEvents**, **\_IInkOverlayEvents**, and **\_IInkPictureEvents** dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICETabletRemoved.</span></span>

## <a name="requirements"></a><span data-ttu-id="cef62-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cef62-113">Requirements</span></span>



| <span data-ttu-id="cef62-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="cef62-114">Requirement</span></span> | <span data-ttu-id="cef62-115">Valore</span><span class="sxs-lookup"><span data-stu-id="cef62-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cef62-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cef62-116">Minimum supported client</span></span><br/> | <span data-ttu-id="cef62-117">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="cef62-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="cef62-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cef62-118">Minimum supported server</span></span><br/> | <span data-ttu-id="cef62-119">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="cef62-119">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="cef62-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cef62-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="cef62-121"><dt>Msinkaut. h (richiede anche Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="cef62-121"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="cef62-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="cef62-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="cef62-123"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cef62-123"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="cef62-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cef62-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cef62-125">InkPicture</span><span class="sxs-lookup"><span data-stu-id="cef62-125">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

[<span data-ttu-id="cef62-126">**Interfaccia IInkTablet**</span><span class="sxs-lookup"><span data-stu-id="cef62-126">**IInkTablet Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet)
</dt> </dl>

 

 




