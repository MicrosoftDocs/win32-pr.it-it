---
description: 'Metodo IRenderEngine::SetInterestRange: non supportato.'
ms.assetid: 1e4c3bd4-2540-428f-9ca6-dd4c65c53434
title: Metodo IRenderEngine::SetInterestRange
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.SetInterestRange
api_type:
- COM
api_location: ''
ms.openlocfilehash: ec9790e65efa30b83cf324da4153f20c541733b9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084459"
---
# <a name="irenderenginesetinterestrange-method"></a><span data-ttu-id="30f8a-103">Metodo IRenderEngine::SetInterestRange</span><span class="sxs-lookup"><span data-stu-id="30f8a-103">IRenderEngine::SetInterestRange method</span></span>

> [!Note]  
> <span data-ttu-id="30f8a-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="30f8a-104">\[Deprecated.</span></span> <span data-ttu-id="30f8a-105">Questa API potrebbe essere rimossa dalle versioni future di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="30f8a-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="30f8a-106">Non supportata.</span><span class="sxs-lookup"><span data-stu-id="30f8a-106">Not supported.</span></span>

## <a name="syntax"></a><span data-ttu-id="30f8a-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="30f8a-107">Syntax</span></span>


```C++
HRESULT SetInterestRange(
   REFERENCE_TIME Start,
   REFERENCE_TIME Stop
);
```



## <a name="parameters"></a><span data-ttu-id="30f8a-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="30f8a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30f8a-109">*Inizia*</span><span class="sxs-lookup"><span data-stu-id="30f8a-109">*Start*</span></span> 
</dt> <dd>

<span data-ttu-id="30f8a-110">Riservato.</span><span class="sxs-lookup"><span data-stu-id="30f8a-110">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="30f8a-111">*Stop*</span><span class="sxs-lookup"><span data-stu-id="30f8a-111">*Stop*</span></span> 
</dt> <dd>

<span data-ttu-id="30f8a-112">Riservato.</span><span class="sxs-lookup"><span data-stu-id="30f8a-112">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30f8a-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="30f8a-113">Return value</span></span>

<span data-ttu-id="30f8a-114">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="30f8a-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="30f8a-115">In caso contrario, restituisce un **codice di errore HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="30f8a-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="30f8a-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="30f8a-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="30f8a-117">Il file di intestazione Qedit.h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="30f8a-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="30f8a-118">Per ottenere Qedit.h, scaricare Microsoft Windows SDK [Update per Windows Vista e .NET Framework 3.0.](https://msdn.microsoft.com/windowsvista/bb980924.aspx)</span><span class="sxs-lookup"><span data-stu-id="30f8a-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="30f8a-119">Qedit.h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3.5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="30f8a-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="30f8a-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="30f8a-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30f8a-121">**Interfaccia IRenderEngine**</span><span class="sxs-lookup"><span data-stu-id="30f8a-121">**IRenderEngine Interface**</span></span>](irenderengine.md)
</dt> </dl>

 

 



