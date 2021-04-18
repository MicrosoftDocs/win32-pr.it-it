---
title: Funzione di callback ICMProgressProcCallback
description: La funzione ICMProgressProcCallback è una funzione di callback fornita dall'applicazione che segnala lo stato di avanzamento e consente all'applicazione di annullare l'elaborazione dei colori.
ms.assetid: 4e0bfa4c-f0eb-4776-98d6-90d9adf71bee
keywords:
- Sistema di colori Windows per la funzione di callback ICMProgressProcCallback
topic_type:
- apiref
api_name:
- ICMProgressProcCallback
api_location:
- Icm.h
api_type:
- UserDefined
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8acf790a135a41e4eabb4a67c2498f1ed914c4c8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324347"
---
# <a name="icmprogressproccallback-callback-function"></a><span data-ttu-id="e1889-104">Funzione di callback ICMProgressProcCallback</span><span class="sxs-lookup"><span data-stu-id="e1889-104">ICMProgressProcCallback callback function</span></span>

<span data-ttu-id="e1889-105">La funzione **ICMProgressProcCallback** è una funzione di callback fornita dall'applicazione che segnala lo stato di avanzamento e consente all'applicazione di annullare l'elaborazione dei colori.</span><span class="sxs-lookup"><span data-stu-id="e1889-105">The **ICMProgressProcCallback** function is an application-supplied callback function that reports progress and permits the application to cancel color processing.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1889-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e1889-106">Syntax</span></span>


```C++
BOOL WINAPI ICMProgressProcCallback(
   ULONG  ulMax,
   ULONG  ulCurrent,
   LPARAM ulCallbackData
);
```



## <a name="parameters"></a><span data-ttu-id="e1889-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="e1889-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1889-108">*ulMax*</span><span class="sxs-lookup"><span data-stu-id="e1889-108">*ulMax*</span></span> 
</dt> <dd>

<span data-ttu-id="e1889-109">Specifica il valore massimo del contatore di stato (utilizzato per stimare il completamento dell'elaborazione della bitmap).</span><span class="sxs-lookup"><span data-stu-id="e1889-109">Specifies the maximum value of the progress counter (used to estimate completion of the bitmap processing).</span></span>

</dd> <dt>

<span data-ttu-id="e1889-110">*ulCurrent*</span><span class="sxs-lookup"><span data-stu-id="e1889-110">*ulCurrent*</span></span> 
</dt> <dd>

<span data-ttu-id="e1889-111">Specifica il valore corrente del contatore di stato (se diviso per il valore massimo, fornisce una stima approssimativa della percentuale di completamento).</span><span class="sxs-lookup"><span data-stu-id="e1889-111">Specifies the current value of the progress counter (when divided by the maximum value, provides a rough estimate of percentage of completion).</span></span>

</dd> <dt>

<span data-ttu-id="e1889-112">*ulCallbackData*</span><span class="sxs-lookup"><span data-stu-id="e1889-112">*ulCallbackData*</span></span> 
</dt> <dd>

<span data-ttu-id="e1889-113">Specifica i dati passati dall'applicazione a una funzione ICM2, che quindi li passa alla funzione di callback.</span><span class="sxs-lookup"><span data-stu-id="e1889-113">Specifies the data which is passed by the application to an ICM2 function, which then passes it on to the callback function.</span></span> <span data-ttu-id="e1889-114">Tali dati possono essere utilizzati, ad esempio, per identificare la bitmap e il processo su cui viene segnalato lo stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="e1889-114">Such data can be used, for example, to identify the bitmap and process about which progress is being reported.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e1889-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e1889-115">Return value</span></span>

<span data-ttu-id="e1889-116">Questa funzione restituisce **true** per continuare l'elaborazione di bitmap.</span><span class="sxs-lookup"><span data-stu-id="e1889-116">This function returns **TRUE** to continue bitmap processing.</span></span> <span data-ttu-id="e1889-117">Il valore restituito è **false** per annullare l'elaborazione.</span><span class="sxs-lookup"><span data-stu-id="e1889-117">The return value is **FALSE** to cancel processing.</span></span> <span data-ttu-id="e1889-118">Se l'elaborazione viene annullata, la funzione chiamante restituisce zero per indicare un errore, anche se il buffer di output può essere riempito parzialmente.</span><span class="sxs-lookup"><span data-stu-id="e1889-118">If processing is canceled, the calling function returns zero to indicate failure, although its output buffer may be partially filled.</span></span>

## <a name="remarks"></a><span data-ttu-id="e1889-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="e1889-119">Remarks</span></span>

<span data-ttu-id="e1889-120">Il nome di questa funzione di callback viene fornito dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e1889-120">The name of this callback function is supplied by the application.</span></span> <span data-ttu-id="e1889-121">Diverse funzioni WCS, tra cui [**TranslateBitmapBits**](/windows/win32/api/icm/nf-icm-translatebitmapbits) e [**CheckBitmapBits**](/windows/win32/api/icm/nf-icm-checkbitmapbits), chiamano questa funzione periodicamente.</span><span class="sxs-lookup"><span data-stu-id="e1889-121">A number of WCS functions, including [**TranslateBitmapBits**](/windows/win32/api/icm/nf-icm-translatebitmapbits) and [**CheckBitmapBits**](/windows/win32/api/icm/nf-icm-checkbitmapbits), call this function periodically.</span></span>

## <a name="requirements"></a><span data-ttu-id="e1889-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e1889-122">Requirements</span></span>



| <span data-ttu-id="e1889-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="e1889-123">Requirement</span></span> | <span data-ttu-id="e1889-124">Valore</span><span class="sxs-lookup"><span data-stu-id="e1889-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="e1889-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e1889-125">Minimum supported client</span></span><br/> | <span data-ttu-id="e1889-126">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e1889-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="e1889-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e1889-127">Minimum supported server</span></span><br/> | <span data-ttu-id="e1889-128">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e1889-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="e1889-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e1889-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="e1889-130"><dt>ICM. h</dt></span><span class="sxs-lookup"><span data-stu-id="e1889-130"><dt>Icm.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e1889-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e1889-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1889-132">Concetti di base sulla gestione dei colori</span><span class="sxs-lookup"><span data-stu-id="e1889-132">Basic color management concepts</span></span>](basic-color-management-concepts.md)
</dt> <dt>

[<span data-ttu-id="e1889-133">Funzioni</span><span class="sxs-lookup"><span data-stu-id="e1889-133">Functions</span></span>](functions.md)
</dt> <dt>

[<span data-ttu-id="e1889-134">**TranslateBitmapBits**</span><span class="sxs-lookup"><span data-stu-id="e1889-134">**TranslateBitmapBits**</span></span>](/windows/win32/api/icm/nf-icm-translatebitmapbits)
</dt> <dt>

[<span data-ttu-id="e1889-135">**CheckBitmapBits**</span><span class="sxs-lookup"><span data-stu-id="e1889-135">**CheckBitmapBits**</span></span>](/windows/win32/api/icm/nf-icm-checkbitmapbits)
</dt> </dl>
