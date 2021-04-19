---
description: Il \_ metodo Put OffsetX specifica l'offset orizzontale del rettangolo di destinazione.
ms.assetid: 057919e1-d65f-487d-b5d7-1c43967ce66d
title: 'IDxtCompositor: metodo:p ut_OffsetX (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtCompositor.put_OffsetX
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 05fe43db86e266ba9ddec32ebd0fd4d59c3df398
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332958"
---
# <a name="idxtcompositorput_offsetx-method"></a><span data-ttu-id="794d9-103">IDxtCompositor::p UT \_ offsetX metodo</span><span class="sxs-lookup"><span data-stu-id="794d9-103">IDxtCompositor::put\_OffsetX method</span></span>

> [!Note]  
> <span data-ttu-id="794d9-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="794d9-104">\[Deprecated.</span></span> <span data-ttu-id="794d9-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="794d9-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="794d9-106">Il `put_OffsetX` metodo specifica l'offset orizzontale del rettangolo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="794d9-106">The `put_OffsetX` method specifies the horizontal offset of the target rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="794d9-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="794d9-107">Syntax</span></span>


```C++
HRESULT put_OffsetX(
  [in] long newVal
);
```



## <a name="parameters"></a><span data-ttu-id="794d9-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="794d9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="794d9-109">*newVal* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="794d9-109">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="794d9-110">Offset orizzontale del rettangolo di destinazione, espresso in pixel.</span><span class="sxs-lookup"><span data-stu-id="794d9-110">The horizontal offset of the target rectangle, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="794d9-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="794d9-111">Return value</span></span>

<span data-ttu-id="794d9-112">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="794d9-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="794d9-113">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="794d9-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="794d9-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="794d9-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="794d9-115">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="794d9-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="794d9-116">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="794d9-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="794d9-117">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="794d9-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="794d9-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="794d9-118">Requirements</span></span>



| <span data-ttu-id="794d9-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="794d9-119">Requirement</span></span> | <span data-ttu-id="794d9-120">Valore</span><span class="sxs-lookup"><span data-stu-id="794d9-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="794d9-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="794d9-121">Header</span></span><br/>  | <dl> <span data-ttu-id="794d9-122"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="794d9-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="794d9-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="794d9-123">Library</span></span><br/> | <dl> <span data-ttu-id="794d9-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="794d9-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="794d9-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="794d9-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="794d9-126">**Interfaccia IDxtCompositor**</span><span class="sxs-lookup"><span data-stu-id="794d9-126">**IDxtCompositor Interface**</span></span>](idxtcompositor.md)
</dt> </dl>

 

 




