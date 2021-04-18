---
description: Si verifica quando l'utente preme e rilascia un tasto mentre il controllo InkEdit dispone dello stato attivo.
ms.assetid: 8284ab41-dfac-4da2-b101-6968a43b15d7
title: Evento InkEdit. KeyPress (inchiostrata. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e49264f82b2cfe3c6998666339f08340a540791
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313945"
---
# <a name="inkeditkeypress-event"></a><span data-ttu-id="13e55-103">Evento InkEdit. KeyPress</span><span class="sxs-lookup"><span data-stu-id="13e55-103">InkEdit.KeyPress event</span></span>

<span data-ttu-id="13e55-104">Si verifica quando l'utente preme e rilascia un tasto mentre il controllo [InkEdit](inkedit-control-reference.md) dispone dello stato attivo.</span><span class="sxs-lookup"><span data-stu-id="13e55-104">Occurs when the user presses and releases a key while the [InkEdit](inkedit-control-reference.md) control has focus.</span></span>

## <a name="syntax"></a><span data-ttu-id="13e55-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="13e55-105">Syntax</span></span>


```C++
HRESULT KeyPress(
   Long *Char
);
```



## <a name="parameters"></a><span data-ttu-id="13e55-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="13e55-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13e55-107">*Char*</span><span class="sxs-lookup"><span data-stu-id="13e55-107">*Char*</span></span> 
</dt> <dd>

<span data-ttu-id="13e55-108">Intero che restituisce un codice ANSI numerico standard.</span><span class="sxs-lookup"><span data-stu-id="13e55-108">An integer that returns a standard numeric ANSI keycode.</span></span> <span data-ttu-id="13e55-109">Il parametro *char* viene passato per riferimento. Se lo si modifica, viene inviato un carattere diverso al controllo.</span><span class="sxs-lookup"><span data-stu-id="13e55-109">The *Char* parameter is passed by reference; changing it sends a different character to the control.</span></span> <span data-ttu-id="13e55-110">Se si modifica il parametro *char* in 0, l'evento viene annullato.</span><span class="sxs-lookup"><span data-stu-id="13e55-110">Changing the *Char* parameter to 0 cancels the event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13e55-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="13e55-111">Return value</span></span>

<span data-ttu-id="13e55-112">Se l'evento ha esito positivo, viene restituito **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="13e55-112">If this event succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="13e55-113">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="13e55-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="13e55-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="13e55-114">Remarks</span></span>

<span data-ttu-id="13e55-115">Questo metodo di evento è definito nell'interfaccia **\_ IInkEditEvents** .</span><span class="sxs-lookup"><span data-stu-id="13e55-115">This event method is defined in the **\_IInkEditEvents** interface.</span></span> <span data-ttu-id="13e55-116">L'interfaccia **\_ IInkEditEvents** implementa l'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) con un identificatore di DISPID \_ IeeKeyPress.</span><span class="sxs-lookup"><span data-stu-id="13e55-116">The **\_IInkEditEvents** interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_IeeKeyPress.</span></span>

## <a name="requirements"></a><span data-ttu-id="13e55-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="13e55-117">Requirements</span></span>



| <span data-ttu-id="13e55-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="13e55-118">Requirement</span></span> | <span data-ttu-id="13e55-119">Valore</span><span class="sxs-lookup"><span data-stu-id="13e55-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13e55-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="13e55-120">Minimum supported client</span></span><br/> | <span data-ttu-id="13e55-121">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="13e55-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="13e55-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="13e55-122">Minimum supported server</span></span><br/> | <span data-ttu-id="13e55-123">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="13e55-123">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="13e55-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="13e55-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="13e55-125"><dt>Inchiostrato. h (richiede anche il \_ . c)</dt></span><span class="sxs-lookup"><span data-stu-id="13e55-125"><dt>Inked.h (also requires inked\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="13e55-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="13e55-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="13e55-127"><dt>InkEd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="13e55-127"><dt>InkEd.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="13e55-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="13e55-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13e55-129">InkEdit</span><span class="sxs-lookup"><span data-stu-id="13e55-129">InkEdit</span></span>](inkedit-control-reference.md)
</dt> <dt>

<span data-ttu-id="13e55-130">[**\[Controllo InkEdit evento KeyDown\]**](inkedit-keydown.md)</span><span class="sxs-lookup"><span data-stu-id="13e55-130">[**KeyDown Event \[InkEdit Control\]**](inkedit-keydown.md)</span></span>
</dt> <dt>

<span data-ttu-id="13e55-131">[**\[Controllo InkEdit evento KeyUp\]**](inkedit-keyup.md)</span><span class="sxs-lookup"><span data-stu-id="13e55-131">[**KeyUp Event \[InkEdit Control\]**](inkedit-keyup.md)</span></span>
</dt> </dl>

 

