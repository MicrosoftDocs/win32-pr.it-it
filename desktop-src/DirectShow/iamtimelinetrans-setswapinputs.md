---
description: Il metodo SetSwapInputs specifica se gli input di transizione vengono scambiati.
ms.assetid: c7303302-dbc4-41b6-8049-5c4496ee9264
title: 'Metodo IAMTimelineTrans:: SetSwapInputs (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrans.SetSwapInputs
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4b2deecb393d6532015cf1490aacd1bd50501920
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332643"
---
# <a name="iamtimelinetranssetswapinputs-method"></a><span data-ttu-id="3c130-103">Metodo IAMTimelineTrans:: SetSwapInputs</span><span class="sxs-lookup"><span data-stu-id="3c130-103">IAMTimelineTrans::SetSwapInputs method</span></span>

> [!Note]  
> <span data-ttu-id="3c130-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="3c130-104">\[Deprecated.</span></span> <span data-ttu-id="3c130-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="3c130-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="3c130-106">Il `SetSwapInputs` metodo specifica se gli input di transizione vengono scambiati.</span><span class="sxs-lookup"><span data-stu-id="3c130-106">The `SetSwapInputs` method specifies whether the transition inputs are swapped.</span></span>

<span data-ttu-id="3c130-107">Per impostazione predefinita, una transizione passa dalla composizione di tutti i livelli di priorità inferiore al livello in cui risiede la transizione.</span><span class="sxs-lookup"><span data-stu-id="3c130-107">By default, a transition goes from the composite of all lower-priority layers to the layer where the transition resides.</span></span> <span data-ttu-id="3c130-108">È possibile invertire la progressione, in modo che la transizione provenga dal livello in cui risiedono al composito di livelli di priorità inferiore.</span><span class="sxs-lookup"><span data-stu-id="3c130-108">You can reverse this progression, so the transition goes from the layer where it resides back to the composite of lower-priority layers.</span></span> <span data-ttu-id="3c130-109">Per ulteriori informazioni, vedere [direzione di transizione](transition-direction.md).</span><span class="sxs-lookup"><span data-stu-id="3c130-109">For more information, see [Transition Direction](transition-direction.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="3c130-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3c130-110">Syntax</span></span>


```C++
HRESULT SetSwapInputs(
   BOOL Val
);
```



## <a name="parameters"></a><span data-ttu-id="3c130-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="3c130-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c130-112">*Val*</span><span class="sxs-lookup"><span data-stu-id="3c130-112">*Val*</span></span> 
</dt> <dd>

<span data-ttu-id="3c130-113">Specifica se gli input vengono scambiati.</span><span class="sxs-lookup"><span data-stu-id="3c130-113">Specifies whether the inputs are swapped.</span></span> <span data-ttu-id="3c130-114">Se **false**, la transizione passa dalla composizione di tutti i livelli di priorità inferiore al livello di transizione.</span><span class="sxs-lookup"><span data-stu-id="3c130-114">If **FALSE**, the transition goes from the composite of all lower-priority layers to the transition layer.</span></span> <span data-ttu-id="3c130-115">Se **true**, la transizione passa alla direzione opposta.</span><span class="sxs-lookup"><span data-stu-id="3c130-115">If **TRUE**, the transition goes in the opposite direction.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c130-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3c130-116">Return value</span></span>

<span data-ttu-id="3c130-117">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="3c130-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3c130-118">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3c130-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="3c130-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="3c130-119">Remarks</span></span>

<span data-ttu-id="3c130-120">Questo metodo non modifica la direzione dell'effetto visivo.</span><span class="sxs-lookup"><span data-stu-id="3c130-120">This method does not change the direction of the visual effect.</span></span> <span data-ttu-id="3c130-121">Ad esempio, una cancellazione da sinistra a destra continuerà a essere ancora da sinistra a destra.</span><span class="sxs-lookup"><span data-stu-id="3c130-121">For example, a left-to-right wipe will still go from left to right.</span></span> <span data-ttu-id="3c130-122">Per modificare la direzione, impostare la proprietà **Progress** usando l'interfaccia [**IPropertySetter**](ipropertysetter.md) .</span><span class="sxs-lookup"><span data-stu-id="3c130-122">To change the direction, set the **Progress** property using the [**IPropertySetter**](ipropertysetter.md) interface.</span></span>

> [!Note]  
> <span data-ttu-id="3c130-123">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="3c130-123">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="3c130-124">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="3c130-124">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="3c130-125">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="3c130-125">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3c130-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3c130-126">Requirements</span></span>



| <span data-ttu-id="3c130-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="3c130-127">Requirement</span></span> | <span data-ttu-id="3c130-128">Valore</span><span class="sxs-lookup"><span data-stu-id="3c130-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3c130-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3c130-129">Header</span></span><br/>  | <dl> <span data-ttu-id="3c130-130"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="3c130-130"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="3c130-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="3c130-131">Library</span></span><br/> | <dl> <span data-ttu-id="3c130-132"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3c130-132"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c130-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3c130-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c130-134">**Interfaccia IAMTimelineTrans**</span><span class="sxs-lookup"><span data-stu-id="3c130-134">**IAMTimelineTrans Interface**</span></span>](iamtimelinetrans.md)
</dt> <dt>

[<span data-ttu-id="3c130-135">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="3c130-135">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




