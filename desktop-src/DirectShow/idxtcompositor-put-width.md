---
description: Il \_ metodo Put Width specifica la larghezza del rettangolo di destinazione.
ms.assetid: 16a2d860-6f5d-4f36-ba54-1be2d3fef705
title: 'IDxtCompositor: metodo:p ut_Width (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtCompositor.put_Width
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 55cc3f2f97be2176f13ce3655d3844ef94043409
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330931"
---
# <a name="idxtcompositorput_width-method"></a><span data-ttu-id="e0e51-103">IDxtCompositor: metodo di \_ larghezza ut:p</span><span class="sxs-lookup"><span data-stu-id="e0e51-103">IDxtCompositor::put\_Width method</span></span>

> [!Note]  
> <span data-ttu-id="e0e51-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="e0e51-104">\[Deprecated.</span></span> <span data-ttu-id="e0e51-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e0e51-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="e0e51-106">Il `put_Width` metodo specifica la larghezza del rettangolo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="e0e51-106">The `put_Width` method specifies the width of the target rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0e51-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e0e51-107">Syntax</span></span>


```C++
HRESULT put_Width(
  [in] long newVal
);
```



## <a name="parameters"></a><span data-ttu-id="e0e51-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="e0e51-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0e51-109">*newVal* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e0e51-109">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0e51-110">Larghezza, in pixel, del rettangolo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="e0e51-110">The width of the target rectangle, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0e51-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e0e51-111">Return value</span></span>

<span data-ttu-id="e0e51-112">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="e0e51-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e0e51-113">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e0e51-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e0e51-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="e0e51-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e0e51-115">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="e0e51-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="e0e51-116">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="e0e51-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="e0e51-117">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="e0e51-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e0e51-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e0e51-118">Requirements</span></span>



| <span data-ttu-id="e0e51-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0e51-119">Requirement</span></span> | <span data-ttu-id="e0e51-120">Valore</span><span class="sxs-lookup"><span data-stu-id="e0e51-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e0e51-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e0e51-121">Header</span></span><br/>  | <dl> <span data-ttu-id="e0e51-122"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="e0e51-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="e0e51-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="e0e51-123">Library</span></span><br/> | <dl> <span data-ttu-id="e0e51-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e0e51-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0e51-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e0e51-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0e51-126">**Interfaccia IDxtCompositor**</span><span class="sxs-lookup"><span data-stu-id="e0e51-126">**IDxtCompositor Interface**</span></span>](idxtcompositor.md)
</dt> </dl>

 

 




