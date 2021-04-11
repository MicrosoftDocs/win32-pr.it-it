---
description: Si verifica prima che il controllo InkPicture venga ridisegnato.
ms.assetid: 97d017ce-fdab-49e5-9ea6-0bcc5d7b14fb
title: Evento InkPicture. painting (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3dc76bbf3079d61c84ac14d1b22690d645a7cce4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232092"
---
# <a name="inkpicturepainting-event"></a><span data-ttu-id="435b0-103">Evento InkPicture. painting</span><span class="sxs-lookup"><span data-stu-id="435b0-103">InkPicture.Painting event</span></span>

<span data-ttu-id="435b0-104">Si verifica prima che il controllo [InkPicture](inkpicture-control-reference.md) venga ridisegnato.</span><span class="sxs-lookup"><span data-stu-id="435b0-104">Occurs before the [InkPicture](inkpicture-control-reference.md) control redraws itself.</span></span>

## <a name="syntax"></a><span data-ttu-id="435b0-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="435b0-105">Syntax</span></span>


```C++
void Painting(
  [in]      long          hDC,
  [in]      IInkRectangle *Rect,
  [in, out] VARIANT_BOOL  *Allow
);
```



## <a name="parameters"></a><span data-ttu-id="435b0-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="435b0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="435b0-107">*HDC* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="435b0-107">*hDC* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="435b0-108">Contesto di dispositivo in cui si verificherà il disegno.</span><span class="sxs-lookup"><span data-stu-id="435b0-108">The device context on which painting will occur.</span></span>

</dd> <dt>

<span data-ttu-id="435b0-109">*Rect* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="435b0-109">*Rect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="435b0-110">Rettangolo di input penna da ridisegnare.</span><span class="sxs-lookup"><span data-stu-id="435b0-110">The ink rectangle that is to be repainted.</span></span>

</dd> <dt>

<span data-ttu-id="435b0-111">*Consenti* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="435b0-111">*Allow* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="435b0-112">Indica se si verificherà il ridisegno.</span><span class="sxs-lookup"><span data-stu-id="435b0-112">Whether the repaint will occur.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="435b0-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="435b0-113">Return value</span></span>

<span data-ttu-id="435b0-114">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="435b0-114">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="435b0-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="435b0-115">Remarks</span></span>

<span data-ttu-id="435b0-116">Questo metodo di evento è definito nelle interfacce **\_ IInkOverlayEvents** e **\_ IInkPictureEvents** dispatch-only (dispinterfaces) con ID DISPID \_ IOEPainting.</span><span class="sxs-lookup"><span data-stu-id="435b0-116">This event method is defined in the **\_IInkOverlayEvents** and **\_IInkPictureEvents** dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IOEPainting.</span></span>

## <a name="requirements"></a><span data-ttu-id="435b0-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="435b0-117">Requirements</span></span>



| <span data-ttu-id="435b0-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="435b0-118">Requirement</span></span> | <span data-ttu-id="435b0-119">Valore</span><span class="sxs-lookup"><span data-stu-id="435b0-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="435b0-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="435b0-120">Minimum supported client</span></span><br/> | <span data-ttu-id="435b0-121">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="435b0-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="435b0-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="435b0-122">Minimum supported server</span></span><br/> | <span data-ttu-id="435b0-123">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="435b0-123">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="435b0-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="435b0-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="435b0-125"><dt>Msinkaut. h (richiede anche Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="435b0-125"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="435b0-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="435b0-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="435b0-127"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="435b0-127"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="435b0-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="435b0-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="435b0-129">InkPicture</span><span class="sxs-lookup"><span data-stu-id="435b0-129">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> </dl>

 

 




