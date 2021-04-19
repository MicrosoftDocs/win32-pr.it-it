---
description: Il metodo ValidateSourceNames convalida i nomi di origine nella sequenza temporale, usando il localizzatore multimediale. Facoltativamente, questo metodo aggiorna anche tutti gli oggetti di origine per i quali individua un file.
ms.assetid: 8f4b9ff0-f283-4bcb-83f4-92410cead7db
title: 'Metodo IAMTimeline:: ValidateSourceNames (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.ValidateSourceNames
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 5154926cb9f814c94762b556721c7580e5b0d82c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330186"
---
# <a name="iamtimelinevalidatesourcenames-method"></a><span data-ttu-id="28de6-104">Metodo IAMTimeline:: ValidateSourceNames</span><span class="sxs-lookup"><span data-stu-id="28de6-104">IAMTimeline::ValidateSourceNames method</span></span>

> [!Note]  
> <span data-ttu-id="28de6-105">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="28de6-105">\[Deprecated.</span></span> <span data-ttu-id="28de6-106">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="28de6-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="28de6-107">Il `ValidateSourceNames` metodo convalida i nomi di origine nella sequenza temporale, usando il localizzatore multimediale.</span><span class="sxs-lookup"><span data-stu-id="28de6-107">The `ValidateSourceNames` method validates source names in the timeline, using the media locator.</span></span> <span data-ttu-id="28de6-108">Facoltativamente, questo metodo aggiorna anche tutti gli oggetti di origine per i quali individua un file.</span><span class="sxs-lookup"><span data-stu-id="28de6-108">Optionally, this method also updates any source object for which it locates a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="28de6-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="28de6-109">Syntax</span></span>


```C++
HRESULT ValidateSourceNames(
   long          ValidateFlags,
   IMediaLocator *pOverride,
   long          NotifyEventHandle
);
```



## <a name="parameters"></a><span data-ttu-id="28de6-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="28de6-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28de6-111">*ValidateFlags*</span><span class="sxs-lookup"><span data-stu-id="28de6-111">*ValidateFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="28de6-112">Combinazione bit per bit dei [**flag di convalida dei nomi di file**](file-name-validation-flags.md) che specificano il comportamento del localizzatore multimediale.</span><span class="sxs-lookup"><span data-stu-id="28de6-112">Bitwise combination of [**File Name Validation Flags**](file-name-validation-flags.md) specifying the behavior of the media locator.</span></span> <span data-ttu-id="28de6-113">I \_ flag di controllo SFN VALIDATEF \_ Replace e SFN \_ VALIDATEF \_ devono essere presenti oppure il metodo restituisce e \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="28de6-113">The SFN\_VALIDATEF\_REPLACE and SFN\_VALIDATEF\_CHECK flags must be present, or the method returns E\_INVALIDARG.</span></span>

</dd> <dt>

<span data-ttu-id="28de6-114">*pOverride*</span><span class="sxs-lookup"><span data-stu-id="28de6-114">*pOverride*</span></span> 
</dt> <dd>

<span data-ttu-id="28de6-115">Puntatore facoltativo all'interfaccia [**IMediaLocator**](imedialocator.md) di un localizzatore multimediale da usare al posto del valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="28de6-115">Optional pointer to the [**IMediaLocator**](imedialocator.md) interface of a media locator to use in place of the default.</span></span> <span data-ttu-id="28de6-116">Per usare il localizzatore multimediale predefinito, impostare il valore di questo parametro su **null**.</span><span class="sxs-lookup"><span data-stu-id="28de6-116">To use the default media locator, set the value of this parameter to **NULL**.</span></span> <span data-ttu-id="28de6-117">Per ulteriori informazioni, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="28de6-117">See Remarks for more information.</span></span>

</dd> <dt>

<span data-ttu-id="28de6-118">*NotifyEventHandle*</span><span class="sxs-lookup"><span data-stu-id="28de6-118">*NotifyEventHandle*</span></span> 
</dt> <dd>

<span data-ttu-id="28de6-119">Handle per un evento.</span><span class="sxs-lookup"><span data-stu-id="28de6-119">Handle to an event.</span></span> <span data-ttu-id="28de6-120">Il metodo segnala l'evento dopo aver completato la convalida.</span><span class="sxs-lookup"><span data-stu-id="28de6-120">The method signals the event after it has completed the validation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28de6-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="28de6-121">Return value</span></span>

<span data-ttu-id="28de6-122">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="28de6-122">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="28de6-123">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="28de6-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="28de6-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="28de6-124">Remarks</span></span>

<span data-ttu-id="28de6-125">Utilizzando il parametro *pOverride* , è possibile fornire un'implementazione personalizzata dell'interfaccia [**IMediaLocator**](imedialocator.md) .</span><span class="sxs-lookup"><span data-stu-id="28de6-125">Using the *pOverride* parameter, you can supply your own custom implementation of the [**IMediaLocator**](imedialocator.md) interface.</span></span> <span data-ttu-id="28de6-126">Ad esempio, il localizzatore multimediale predefinito non invierà una notifica all'applicazione sui file che trova (o non è in grado di trovare).</span><span class="sxs-lookup"><span data-stu-id="28de6-126">For example, the default media locator will not notify your application about the files that it finds (or cannot find).</span></span> <span data-ttu-id="28de6-127">Per aggirare questa limitazione, è possibile implementare un localizzatore multimediale personalizzato, rendendolo un wrapper per la versione predefinita.</span><span class="sxs-lookup"><span data-stu-id="28de6-127">To get around this limitation, you could implement a custom media locator, making it a wrapper for the default version.</span></span> <span data-ttu-id="28de6-128">Nella versione personalizzata passare [**IMediaLocator:: FindMediaFile**](imedialocator-findmediafile.md) chiamate direttamente alla versione predefinita ed esaminare il valore restituito.</span><span class="sxs-lookup"><span data-stu-id="28de6-128">In your custom version, pass [**IMediaLocator::FindMediaFile**](imedialocator-findmediafile.md) calls directly to the default version, and examine the return value.</span></span>

> [!Note]  
> <span data-ttu-id="28de6-129">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="28de6-129">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="28de6-130">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="28de6-130">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="28de6-131">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="28de6-131">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="28de6-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="28de6-132">Requirements</span></span>



| <span data-ttu-id="28de6-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="28de6-133">Requirement</span></span> | <span data-ttu-id="28de6-134">Valore</span><span class="sxs-lookup"><span data-stu-id="28de6-134">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="28de6-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="28de6-135">Header</span></span><br/>  | <dl> <span data-ttu-id="28de6-136"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="28de6-136"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="28de6-137">Libreria</span><span class="sxs-lookup"><span data-stu-id="28de6-137">Library</span></span><br/> | <dl> <span data-ttu-id="28de6-138"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="28de6-138"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28de6-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="28de6-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28de6-140">**Interfaccia IAMTimeline**</span><span class="sxs-lookup"><span data-stu-id="28de6-140">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="28de6-141">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="28de6-141">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




