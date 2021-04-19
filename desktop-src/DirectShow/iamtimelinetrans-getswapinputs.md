---
description: Il metodo GetSwapInputs recupera un valore che indica se gli input di transizione vengono scambiati.
ms.assetid: 84cb5c3d-7c3a-4c35-aac7-97d812d99a38
title: 'Metodo IAMTimelineTrans:: GetSwapInputs (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrans.GetSwapInputs
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a2acdff1007bd26773ce495d024676632eee1767
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333261"
---
# <a name="iamtimelinetransgetswapinputs-method"></a><span data-ttu-id="0495d-103">Metodo IAMTimelineTrans:: GetSwapInputs</span><span class="sxs-lookup"><span data-stu-id="0495d-103">IAMTimelineTrans::GetSwapInputs method</span></span>

> [!Note]  
> <span data-ttu-id="0495d-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="0495d-104">\[Deprecated.</span></span> <span data-ttu-id="0495d-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="0495d-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="0495d-106">Il `GetSwapInputs` metodo recupera un valore che indica se gli input di transizione vengono scambiati.</span><span class="sxs-lookup"><span data-stu-id="0495d-106">The `GetSwapInputs` method retrieves a value that indicates whether the transition inputs are swapped.</span></span>

<span data-ttu-id="0495d-107">Per impostazione predefinita, una transizione passa dalla composizione di tutti i livelli di priorità inferiore al livello in cui risiede la transizione.</span><span class="sxs-lookup"><span data-stu-id="0495d-107">By default, a transition goes from the composite of all lower-priority layers to the layer where the transition resides.</span></span> <span data-ttu-id="0495d-108">È possibile invertire la progressione, in modo che la transizione provenga dal livello in cui risiedono al composito di livelli di priorità inferiore.</span><span class="sxs-lookup"><span data-stu-id="0495d-108">You can reverse this progression, so the transition goes from the layer where it resides back to the composite of lower-priority layers.</span></span>

## <a name="syntax"></a><span data-ttu-id="0495d-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0495d-109">Syntax</span></span>


```C++
HRESULT GetSwapInputs(
   BOOL *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="0495d-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="0495d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0495d-111">*pVal*</span><span class="sxs-lookup"><span data-stu-id="0495d-111">*pVal*</span></span> 
</dt> <dd>

<span data-ttu-id="0495d-112">Riceve un valore booleano.</span><span class="sxs-lookup"><span data-stu-id="0495d-112">Receives a Boolean value.</span></span> <span data-ttu-id="0495d-113">Se il valore è **false**, la transizione passa dalla composizione di tutti i livelli di priorità inferiore al livello di transizione.</span><span class="sxs-lookup"><span data-stu-id="0495d-113">If the value is **FALSE**, the transition goes from the composite of all lower-priority layers to the transition layer.</span></span> <span data-ttu-id="0495d-114">Se il valore è **true**, la transizione passa alla direzione opposta.</span><span class="sxs-lookup"><span data-stu-id="0495d-114">If the value is **TRUE**, the transition goes in the opposite direction.</span></span> <span data-ttu-id="0495d-115">Il valore predefinito è **false**.</span><span class="sxs-lookup"><span data-stu-id="0495d-115">The default value is **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0495d-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0495d-116">Return value</span></span>

<span data-ttu-id="0495d-117">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="0495d-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0495d-118">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0495d-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="0495d-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="0495d-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="0495d-120">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="0495d-120">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="0495d-121">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="0495d-121">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="0495d-122">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="0495d-122">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="0495d-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0495d-123">Requirements</span></span>



| <span data-ttu-id="0495d-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="0495d-124">Requirement</span></span> | <span data-ttu-id="0495d-125">Valore</span><span class="sxs-lookup"><span data-stu-id="0495d-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0495d-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0495d-126">Header</span></span><br/>  | <dl> <span data-ttu-id="0495d-127"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="0495d-127"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="0495d-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="0495d-128">Library</span></span><br/> | <dl> <span data-ttu-id="0495d-129"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0495d-129"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0495d-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0495d-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0495d-131">**Interfaccia IAMTimelineTrans**</span><span class="sxs-lookup"><span data-stu-id="0495d-131">**IAMTimelineTrans Interface**</span></span>](iamtimelinetrans.md)
</dt> <dt>

[<span data-ttu-id="0495d-132">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="0495d-132">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




