---
description: Il metodo GetDefaultEffect recupera l'effetto predefinito. Se il motore di rendering non è in grado di eseguire il rendering di un effetto, sostituisce l'effetto predefinito.
ms.assetid: 27eec6e8-702f-4e56-8d81-aa0633b8ec68
title: 'Metodo IAMTimeline:: GetDefaultEffect (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.GetDefaultEffect
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a0b1cf356a9c067ccae246814d2e1f381d7f78e5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331102"
---
# <a name="iamtimelinegetdefaulteffect-method"></a><span data-ttu-id="55892-104">Metodo IAMTimeline:: GetDefaultEffect</span><span class="sxs-lookup"><span data-stu-id="55892-104">IAMTimeline::GetDefaultEffect method</span></span>

> [!Note]  
> <span data-ttu-id="55892-105">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="55892-105">\[Deprecated.</span></span> <span data-ttu-id="55892-106">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="55892-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="55892-107">Il `GetDefaultEffect` metodo recupera l'effetto predefinito.</span><span class="sxs-lookup"><span data-stu-id="55892-107">The `GetDefaultEffect` method retrieves the default effect.</span></span> <span data-ttu-id="55892-108">Se il motore di rendering non è in grado di eseguire il rendering di un effetto, sostituisce l'effetto predefinito.</span><span class="sxs-lookup"><span data-stu-id="55892-108">If the render engine cannot render an effect, it substitutes the default effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="55892-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="55892-109">Syntax</span></span>


```C++
HRESULT GetDefaultEffect(
   GUID *pGuid
);
```



## <a name="parameters"></a><span data-ttu-id="55892-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="55892-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55892-111">*pGuid*</span><span class="sxs-lookup"><span data-stu-id="55892-111">*pGuid*</span></span> 
</dt> <dd>

<span data-ttu-id="55892-112">Riceve l'identificatore univoco globale (GUID) dell'effetto predefinito.</span><span class="sxs-lookup"><span data-stu-id="55892-112">Receives the globally unique identifier (GUID) of the default effect.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55892-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="55892-113">Return value</span></span>

<span data-ttu-id="55892-114">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="55892-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="55892-115">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="55892-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="55892-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="55892-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="55892-117">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="55892-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="55892-118">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="55892-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="55892-119">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="55892-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="55892-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="55892-120">Requirements</span></span>



| <span data-ttu-id="55892-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="55892-121">Requirement</span></span> | <span data-ttu-id="55892-122">Valore</span><span class="sxs-lookup"><span data-stu-id="55892-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="55892-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="55892-123">Header</span></span><br/>  | <dl> <span data-ttu-id="55892-124"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="55892-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="55892-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="55892-125">Library</span></span><br/> | <dl> <span data-ttu-id="55892-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="55892-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55892-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="55892-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55892-128">**Interfaccia IAMTimeline**</span><span class="sxs-lookup"><span data-stu-id="55892-128">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="55892-129">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="55892-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




