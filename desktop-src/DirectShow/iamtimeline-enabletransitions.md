---
description: Il metodo EnableTransitions Abilita o Disabilita tutte le transizioni nella sequenza temporale.
ms.assetid: 8610337a-a247-44f0-8674-3cbc43f636d5
title: 'Metodo IAMTimeline:: EnableTransitions (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.EnableTransitions
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: c05d3a00a57b8008789b83b16eee155eea974e6e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326797"
---
# <a name="iamtimelineenabletransitions-method"></a><span data-ttu-id="cc916-103">Metodo IAMTimeline:: EnableTransitions</span><span class="sxs-lookup"><span data-stu-id="cc916-103">IAMTimeline::EnableTransitions method</span></span>

> [!Note]  
> <span data-ttu-id="cc916-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="cc916-104">\[Deprecated.</span></span> <span data-ttu-id="cc916-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="cc916-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="cc916-106">Il `EnableTransitions` Metodo Abilita o Disabilita tutte le transizioni nella sequenza temporale.</span><span class="sxs-lookup"><span data-stu-id="cc916-106">The `EnableTransitions` method enables or disables all transitions in the timeline.</span></span> <span data-ttu-id="cc916-107">Se le transizioni sono disabilitate, i motori di rendering li considerano come tagli; ovvero, l'output sottoposto a rendering passa immediatamente da una traccia alla successiva.</span><span class="sxs-lookup"><span data-stu-id="cc916-107">If transitions are disabled, the render engines treats them as cuts; that is, the rendered output jumps instantly from one track to the next.</span></span> <span data-ttu-id="cc916-108">Il punto di taglio predefinito è a metà della durata della transizione.</span><span class="sxs-lookup"><span data-stu-id="cc916-108">The default cut point is halfway through the duration of the transition.</span></span> <span data-ttu-id="cc916-109">È possibile modificare il punto di taglio chiamando il metodo [**IAMTimelineTrans:: SetCutPoint**](iamtimelinetrans-setcutpoint.md) sulla transizione.</span><span class="sxs-lookup"><span data-stu-id="cc916-109">You can change the cut point by calling the [**IAMTimelineTrans::SetCutPoint**](iamtimelinetrans-setcutpoint.md) method on the transition.</span></span> <span data-ttu-id="cc916-110">Le transizioni disabilitate non vengono rimosse dalla sequenza temporale.</span><span class="sxs-lookup"><span data-stu-id="cc916-110">Disabled transitions are not removed from the timeline.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc916-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cc916-111">Syntax</span></span>


```C++
HRESULT EnableTransitions(
   BOOL fEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="cc916-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="cc916-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc916-113">*fEnabled*</span><span class="sxs-lookup"><span data-stu-id="cc916-113">*fEnabled*</span></span> 
</dt> <dd>

<span data-ttu-id="cc916-114">Valore booleano che specifica se abilitare o disabilitare le transizioni.</span><span class="sxs-lookup"><span data-stu-id="cc916-114">Boolean value that specifies whether to enable or disable transitions.</span></span> <span data-ttu-id="cc916-115">Se **true**, le transizioni sono abilitate.</span><span class="sxs-lookup"><span data-stu-id="cc916-115">If **TRUE**, transitions are enabled.</span></span> <span data-ttu-id="cc916-116">Se **false**, le transizioni sono disabilitate.</span><span class="sxs-lookup"><span data-stu-id="cc916-116">If **FALSE**, transitions are disabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc916-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cc916-117">Return value</span></span>

<span data-ttu-id="cc916-118">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="cc916-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="cc916-119">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="cc916-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="cc916-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="cc916-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="cc916-121">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="cc916-121">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="cc916-122">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="cc916-122">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="cc916-123">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="cc916-123">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="cc916-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cc916-124">Requirements</span></span>



| <span data-ttu-id="cc916-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="cc916-125">Requirement</span></span> | <span data-ttu-id="cc916-126">Valore</span><span class="sxs-lookup"><span data-stu-id="cc916-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cc916-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cc916-127">Header</span></span><br/>  | <dl> <span data-ttu-id="cc916-128"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="cc916-128"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="cc916-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="cc916-129">Library</span></span><br/> | <dl> <span data-ttu-id="cc916-130"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cc916-130"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc916-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cc916-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc916-132">**Interfaccia IAMTimeline**</span><span class="sxs-lookup"><span data-stu-id="cc916-132">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="cc916-133">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="cc916-133">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




