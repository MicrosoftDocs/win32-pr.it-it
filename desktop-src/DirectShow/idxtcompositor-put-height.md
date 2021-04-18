---
description: Il \_ metodo Put Height specifica l'altezza del rettangolo di destinazione.
ms.assetid: 032b5468-bce8-4492-abbe-e442131ebe3a
title: 'IDxtCompositor: metodo:p ut_Height (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtCompositor.put_Height
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 883a3261b6322a69e0e1612b724a9f570953dc97
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328152"
---
# <a name="idxtcompositorput_height-method"></a><span data-ttu-id="9dddf-103">IDxtCompositor::p \_ metodo di altezza UT</span><span class="sxs-lookup"><span data-stu-id="9dddf-103">IDxtCompositor::put\_Height method</span></span>

> [!Note]  
> <span data-ttu-id="9dddf-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="9dddf-104">\[Deprecated.</span></span> <span data-ttu-id="9dddf-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="9dddf-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="9dddf-106">Il `put_Height` metodo specifica l'altezza del rettangolo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="9dddf-106">The `put_Height` method specifies the height of the target rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="9dddf-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9dddf-107">Syntax</span></span>


```C++
HRESULT put_Height(
  [in] long newVal
);
```



## <a name="parameters"></a><span data-ttu-id="9dddf-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="9dddf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9dddf-109">*newVal* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9dddf-109">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9dddf-110">Altezza, in pixel, del rettangolo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="9dddf-110">The height of the target rectangle, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9dddf-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9dddf-111">Return value</span></span>

<span data-ttu-id="9dddf-112">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="9dddf-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9dddf-113">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9dddf-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="9dddf-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="9dddf-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="9dddf-115">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="9dddf-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="9dddf-116">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="9dddf-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="9dddf-117">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="9dddf-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9dddf-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9dddf-118">Requirements</span></span>



| <span data-ttu-id="9dddf-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="9dddf-119">Requirement</span></span> | <span data-ttu-id="9dddf-120">Valore</span><span class="sxs-lookup"><span data-stu-id="9dddf-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9dddf-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9dddf-121">Header</span></span><br/>  | <dl> <span data-ttu-id="9dddf-122"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="9dddf-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="9dddf-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="9dddf-123">Library</span></span><br/> | <dl> <span data-ttu-id="9dddf-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9dddf-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9dddf-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9dddf-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9dddf-126">**Interfaccia IDxtCompositor**</span><span class="sxs-lookup"><span data-stu-id="9dddf-126">**IDxtCompositor Interface**</span></span>](idxtcompositor.md)
</dt> </dl>

 

 




