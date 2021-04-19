---
description: Il \_ metodo Get OffsetY recupera l'offset verticale dell'origine della cancellazione.
ms.assetid: 0d8b8df2-b916-4143-b1f1-7912ef3fa025
title: 'Metodo IDxtJpeg:: get_OffsetY (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.get_OffsetY
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 76c0d60ac5150fcec1bde63ccb4e03d820c38ddf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326778"
---
# <a name="idxtjpegget_offsety-method"></a><span data-ttu-id="0a2b9-103">Metodo IDxtJpeg:: Get \_ OffsetY</span><span class="sxs-lookup"><span data-stu-id="0a2b9-103">IDxtJpeg::get\_OffsetY method</span></span>

> [!Note]  
> <span data-ttu-id="0a2b9-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="0a2b9-104">\[Deprecated.</span></span> <span data-ttu-id="0a2b9-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="0a2b9-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="0a2b9-106">Il `get_OffsetY` metodo recupera l'offset verticale dell'origine della cancellazione.</span><span class="sxs-lookup"><span data-stu-id="0a2b9-106">The `get_OffsetY` method retrieves the vertical offset of the wipe origin.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a2b9-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0a2b9-107">Syntax</span></span>


```C++
HRESULT get_OffsetY(
  [out, retval] long *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="0a2b9-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="0a2b9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a2b9-109">*pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="0a2b9-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="0a2b9-110">Riceve l'offset verticale dell'origine della cancellazione, in pixel.</span><span class="sxs-lookup"><span data-stu-id="0a2b9-110">Receives the vertical offset of the wipe origin, in pixels.</span></span> <span data-ttu-id="0a2b9-111">Il centro della cancellazione viene sottoposta a offset in base a questa quantità.</span><span class="sxs-lookup"><span data-stu-id="0a2b9-111">The center of the wipe is offset by this amount.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a2b9-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0a2b9-112">Return value</span></span>

<span data-ttu-id="0a2b9-113">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="0a2b9-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0a2b9-114">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0a2b9-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="0a2b9-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="0a2b9-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="0a2b9-116">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="0a2b9-116">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="0a2b9-117">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="0a2b9-117">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="0a2b9-118">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="0a2b9-118">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="0a2b9-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0a2b9-119">Requirements</span></span>



| <span data-ttu-id="0a2b9-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="0a2b9-120">Requirement</span></span> | <span data-ttu-id="0a2b9-121">Valore</span><span class="sxs-lookup"><span data-stu-id="0a2b9-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0a2b9-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0a2b9-122">Header</span></span><br/>  | <dl> <span data-ttu-id="0a2b9-123"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="0a2b9-123"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="0a2b9-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="0a2b9-124">Library</span></span><br/> | <dl> <span data-ttu-id="0a2b9-125"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0a2b9-125"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a2b9-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0a2b9-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a2b9-127">**Interfaccia IDxtJpeg**</span><span class="sxs-lookup"><span data-stu-id="0a2b9-127">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> </dl>

 

 




