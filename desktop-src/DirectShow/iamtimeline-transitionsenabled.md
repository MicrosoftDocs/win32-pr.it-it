---
description: Il metodo TransitionsEnabled determina se le transizioni sono abilitate.
ms.assetid: c961d8d7-4509-444b-a49f-6ab79fc31f7e
title: 'Metodo IAMTimeline:: TransitionsEnabled (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.TransitionsEnabled
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 7116ccf4ff2015934c9071f4ce2ef073656b89c5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330189"
---
# <a name="iamtimelinetransitionsenabled-method"></a><span data-ttu-id="f09b4-103">Metodo IAMTimeline:: TransitionsEnabled</span><span class="sxs-lookup"><span data-stu-id="f09b4-103">IAMTimeline::TransitionsEnabled method</span></span>

> [!Note]  
> <span data-ttu-id="f09b4-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="f09b4-104">\[Deprecated.</span></span> <span data-ttu-id="f09b4-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f09b4-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="f09b4-106">Il metodo **TransitionsEnabled** determina se le transizioni sono abilitate.</span><span class="sxs-lookup"><span data-stu-id="f09b4-106">The **TransitionsEnabled** method determines whether transitions are enabled.</span></span>

## <a name="syntax"></a><span data-ttu-id="f09b4-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f09b4-107">Syntax</span></span>


```C++
HRESULT TransitionsEnabled(
   BOOL *pfEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="f09b4-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="f09b4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f09b4-109">*pfEnabled*</span><span class="sxs-lookup"><span data-stu-id="f09b4-109">*pfEnabled*</span></span> 
</dt> <dd>

<span data-ttu-id="f09b4-110">Riceve un valore booleano.</span><span class="sxs-lookup"><span data-stu-id="f09b4-110">Receives a Boolean value.</span></span> <span data-ttu-id="f09b4-111">Se **true**, le transizioni sono abilitate.</span><span class="sxs-lookup"><span data-stu-id="f09b4-111">If **TRUE**, transitions are enabled.</span></span> <span data-ttu-id="f09b4-112">In caso contrario, le transizioni sono disabilitate.</span><span class="sxs-lookup"><span data-stu-id="f09b4-112">Otherwise, transitions are disabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f09b4-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f09b4-113">Return value</span></span>

<span data-ttu-id="f09b4-114">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="f09b4-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f09b4-115">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f09b4-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f09b4-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="f09b4-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="f09b4-117">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="f09b4-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="f09b4-118">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="f09b4-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="f09b4-119">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="f09b4-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f09b4-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f09b4-120">Requirements</span></span>



| <span data-ttu-id="f09b4-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="f09b4-121">Requirement</span></span> | <span data-ttu-id="f09b4-122">Valore</span><span class="sxs-lookup"><span data-stu-id="f09b4-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f09b4-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f09b4-123">Header</span></span><br/>  | <dl> <span data-ttu-id="f09b4-124"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="f09b4-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="f09b4-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="f09b4-125">Library</span></span><br/> | <dl> <span data-ttu-id="f09b4-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f09b4-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f09b4-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f09b4-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f09b4-128">**Interfaccia IAMTimeline**</span><span class="sxs-lookup"><span data-stu-id="f09b4-128">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="f09b4-129">**IAMTimeline::EnableTransitions**</span><span class="sxs-lookup"><span data-stu-id="f09b4-129">**IAMTimeline::EnableTransitions**</span></span>](iamtimeline-enabletransitions.md)
</dt> <dt>

[<span data-ttu-id="f09b4-130">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="f09b4-130">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




