---
description: Si verifica quando il controllo InkPicture ha completato il ridisegno.
ms.assetid: a8194cff-ed94-402e-8564-08d370f958b4
title: Evento InkPicture. Painted (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60188ef87d88ba7412a07300e708718bedc947fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313926"
---
# <a name="inkpicturepainted-event"></a><span data-ttu-id="9a53e-103">Evento InkPicture. Painted</span><span class="sxs-lookup"><span data-stu-id="9a53e-103">InkPicture.Painted event</span></span>

<span data-ttu-id="9a53e-104">Si verifica quando il controllo [InkPicture](inkpicture-control-reference.md) ha completato il ridisegno.</span><span class="sxs-lookup"><span data-stu-id="9a53e-104">Occurs when the [InkPicture](inkpicture-control-reference.md) control has completed redrawing itself.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a53e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9a53e-105">Syntax</span></span>


```C++
void Painted(
  [in] long         hDC,
  [in] InkRectangle *Rect
);
```



## <a name="parameters"></a><span data-ttu-id="9a53e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="9a53e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a53e-107">*HDC* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9a53e-107">*hDC* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a53e-108">Contesto di dispositivo in cui si è verificato l'evento.</span><span class="sxs-lookup"><span data-stu-id="9a53e-108">The device context on which the event occurred.</span></span>

</dd> <dt>

<span data-ttu-id="9a53e-109">*Rect* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9a53e-109">*Rect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a53e-110">[**InkRectangle**](inkrectangle-class.md) ridisegnato.</span><span class="sxs-lookup"><span data-stu-id="9a53e-110">The [**InkRectangle**](inkrectangle-class.md) that was repainted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a53e-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9a53e-111">Return value</span></span>

<span data-ttu-id="9a53e-112">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="9a53e-112">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9a53e-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="9a53e-113">Remarks</span></span>

<span data-ttu-id="9a53e-114">Questo metodo di evento viene definito in **\_ IInkOverlayEvents** e **\_ IInkPictureEvents** dispinterfaces con ID DISPID \_ IOEPainted.</span><span class="sxs-lookup"><span data-stu-id="9a53e-114">This event method is defined in the **\_IInkOverlayEvents** and **\_IInkPictureEvents** dispinterfaces with an ID of DISPID\_IOEPainted.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a53e-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9a53e-115">Requirements</span></span>



| <span data-ttu-id="9a53e-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="9a53e-116">Requirement</span></span> | <span data-ttu-id="9a53e-117">Valore</span><span class="sxs-lookup"><span data-stu-id="9a53e-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a53e-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9a53e-118">Minimum supported client</span></span><br/> | <span data-ttu-id="9a53e-119">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="9a53e-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="9a53e-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9a53e-120">Minimum supported server</span></span><br/> | <span data-ttu-id="9a53e-121">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="9a53e-121">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="9a53e-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9a53e-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="9a53e-123"><dt>Msinkaut. h (richiede anche Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="9a53e-123"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="9a53e-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="9a53e-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="9a53e-125"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9a53e-125"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="9a53e-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9a53e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a53e-127">InkPicture</span><span class="sxs-lookup"><span data-stu-id="9a53e-127">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> </dl>

 

 




