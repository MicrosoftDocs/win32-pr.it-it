---
description: Il \_ metodo di offset put specifica l'offset verticale dell'origine della cancellazione.
ms.assetid: 1dfd18cf-06ae-46eb-80d7-078efc243bb1
title: 'IDxtJpeg: metodo:p ut_OffsetY (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.put_OffsetY
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 2f68a18d01acf519032bce31c28515bc7ac81c92
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331918"
---
# <a name="idxtjpegput_offsety-method"></a><span data-ttu-id="aa88b-103">IDxtJpeg::p \_ metodo di offset UT</span><span class="sxs-lookup"><span data-stu-id="aa88b-103">IDxtJpeg::put\_OffsetY method</span></span>

> [!Note]  
> <span data-ttu-id="aa88b-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="aa88b-104">\[Deprecated.</span></span> <span data-ttu-id="aa88b-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="aa88b-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="aa88b-106">Il `put_OffsetY` metodo specifica l'offset verticale dell'origine della cancellazione.</span><span class="sxs-lookup"><span data-stu-id="aa88b-106">The `put_OffsetY` method specifies the vertical offset of the wipe origin.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa88b-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="aa88b-107">Syntax</span></span>


```C++
HRESULT put_OffsetY(
  [in] long newVal
);
```



## <a name="parameters"></a><span data-ttu-id="aa88b-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="aa88b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa88b-109">*newVal* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aa88b-109">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa88b-110">Offset verticale dell'origine della cancellazione, espresso in pixel.</span><span class="sxs-lookup"><span data-stu-id="aa88b-110">The vertical offset of the wipe origin, in pixels.</span></span> <span data-ttu-id="aa88b-111">Il centro della cancellazione viene sottoposta a offset in base a questa quantità.</span><span class="sxs-lookup"><span data-stu-id="aa88b-111">The center of the wipe is offset by this amount.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa88b-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="aa88b-112">Return value</span></span>

<span data-ttu-id="aa88b-113">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="aa88b-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="aa88b-114">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="aa88b-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="aa88b-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="aa88b-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="aa88b-116">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="aa88b-116">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="aa88b-117">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="aa88b-117">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="aa88b-118">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="aa88b-118">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="aa88b-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="aa88b-119">Requirements</span></span>



| <span data-ttu-id="aa88b-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="aa88b-120">Requirement</span></span> | <span data-ttu-id="aa88b-121">Valore</span><span class="sxs-lookup"><span data-stu-id="aa88b-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="aa88b-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="aa88b-122">Header</span></span><br/>  | <dl> <span data-ttu-id="aa88b-123"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="aa88b-123"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="aa88b-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="aa88b-124">Library</span></span><br/> | <dl> <span data-ttu-id="aa88b-125"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="aa88b-125"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa88b-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="aa88b-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa88b-127">**Interfaccia IDxtJpeg**</span><span class="sxs-lookup"><span data-stu-id="aa88b-127">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> </dl>

 

 




