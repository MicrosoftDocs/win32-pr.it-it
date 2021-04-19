---
description: Il \_ metodo Put AlphaRamp specifica la proprietà della rampa Alpha. La rampa alfa è la percentuale in base alla quale vengono modificati i valori alfa nell'immagine originale. Se ad esempio la rampa alfa è 0,5, i valori alfa nell'immagine vengono ridotti 50%.
ms.assetid: 19ea5828-54fc-43a1-be7c-f6c12cf84648
title: 'IDxtAlphaSetter: metodo:p ut_AlphaRamp (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtAlphaSetter.put_AlphaRamp
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: fc6c0eb4d5286081de9abe0c7c6d58092d111573
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333432"
---
# <a name="idxtalphasetterput_alpharamp-method"></a><span data-ttu-id="9de45-105">IDxtAlphaSetter::p UT \_ AlphaRamp metodo</span><span class="sxs-lookup"><span data-stu-id="9de45-105">IDxtAlphaSetter::put\_AlphaRamp method</span></span>

> [!Note]  
> <span data-ttu-id="9de45-106">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="9de45-106">\[Deprecated.</span></span> <span data-ttu-id="9de45-107">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="9de45-107">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="9de45-108">Il `put_AlphaRamp` metodo specifica la proprietà della rampa alfa.</span><span class="sxs-lookup"><span data-stu-id="9de45-108">The `put_AlphaRamp` method specifies the alpha ramp property.</span></span> <span data-ttu-id="9de45-109">La rampa alfa è la percentuale in base alla quale vengono modificati i valori alfa nell'immagine originale.</span><span class="sxs-lookup"><span data-stu-id="9de45-109">The alpha ramp is the percentage by which the alpha values in the original image are adjusted.</span></span> <span data-ttu-id="9de45-110">Se ad esempio la rampa alfa è 0,5, i valori alfa nell'immagine vengono ridotti 50%.</span><span class="sxs-lookup"><span data-stu-id="9de45-110">For example, if the alpha ramp is 0.5, the alpha values in the image are reduced 50%.</span></span>

## <a name="syntax"></a><span data-ttu-id="9de45-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9de45-111">Syntax</span></span>


```C++
HRESULT put_AlphaRamp(
  [in] double Alpha
);
```



## <a name="parameters"></a><span data-ttu-id="9de45-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="9de45-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9de45-113">*Alfa* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9de45-113">*Alpha* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9de45-114">La rampa alfa come percentuale.</span><span class="sxs-lookup"><span data-stu-id="9de45-114">The alpha ramp as a percentage.</span></span> <span data-ttu-id="9de45-115">Ad esempio, 1,0 è 100%.</span><span class="sxs-lookup"><span data-stu-id="9de45-115">For example, 1.0 is 100%.</span></span> <span data-ttu-id="9de45-116">Per disabilitare questa proprietà, impostare un valore negativo.</span><span class="sxs-lookup"><span data-stu-id="9de45-116">To disable this property, set a negative value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9de45-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9de45-117">Return value</span></span>

<span data-ttu-id="9de45-118">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="9de45-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9de45-119">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9de45-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="9de45-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="9de45-120">Remarks</span></span>

<span data-ttu-id="9de45-121">Se si imposta questa proprietà su un valore non negativo, è necessario disabilitare anche la proprietà Alpha, chiamando **put \_ Alpha** con un valore negativo.</span><span class="sxs-lookup"><span data-stu-id="9de45-121">If you set this property to a non-negative value, you must also disable the alpha property, by calling **put\_Alpha** with a negative value.</span></span> <span data-ttu-id="9de45-122">In caso contrario, non viene eseguito il rendering corretto dell'effetto.</span><span class="sxs-lookup"><span data-stu-id="9de45-122">Otherwise the effect will not render correctly.</span></span>

> [!Note]  
> <span data-ttu-id="9de45-123">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="9de45-123">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="9de45-124">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="9de45-124">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="9de45-125">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="9de45-125">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9de45-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9de45-126">Requirements</span></span>



| <span data-ttu-id="9de45-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="9de45-127">Requirement</span></span> | <span data-ttu-id="9de45-128">Valore</span><span class="sxs-lookup"><span data-stu-id="9de45-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9de45-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9de45-129">Header</span></span><br/>  | <dl> <span data-ttu-id="9de45-130"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="9de45-130"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="9de45-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="9de45-131">Library</span></span><br/> | <dl> <span data-ttu-id="9de45-132"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9de45-132"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9de45-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9de45-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9de45-134">**Interfaccia IDxtAlphaSetter**</span><span class="sxs-lookup"><span data-stu-id="9de45-134">**IDxtAlphaSetter Interface**</span></span>](idxtalphasetter.md)
</dt> <dt>

[<span data-ttu-id="9de45-135">**IDxtAlphaSetter::p UT \_ Alpha**</span><span class="sxs-lookup"><span data-stu-id="9de45-135">**IDxtAlphaSetter::put\_Alpha**</span></span>](idxtalphasetter-put-alpha.md)
</dt> </dl>

 

 




