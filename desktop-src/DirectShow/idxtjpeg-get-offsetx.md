---
description: Il \_ metodo Get OffsetX recupera l'offset orizzontale dell'origine della cancellazione.
ms.assetid: 0ca97bb9-9359-4098-9e80-1847da4154ec
title: 'Metodo IDxtJpeg:: get_OffsetX (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.get_OffsetX
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: d18d8ede94700f2de2fe49e44031675c7c91c930
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330642"
---
# <a name="idxtjpegget_offsetx-method"></a><span data-ttu-id="4d7e8-103">Metodo IDxtJpeg:: Get \_ offsetX</span><span class="sxs-lookup"><span data-stu-id="4d7e8-103">IDxtJpeg::get\_OffsetX method</span></span>

> [!Note]  
> <span data-ttu-id="4d7e8-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="4d7e8-104">\[Deprecated.</span></span> <span data-ttu-id="4d7e8-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="4d7e8-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="4d7e8-106">Il `get_OffsetX` metodo recupera l'offset orizzontale dell'origine della cancellazione.</span><span class="sxs-lookup"><span data-stu-id="4d7e8-106">The `get_OffsetX` method retrieves the horizontal offset of the wipe origin.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d7e8-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4d7e8-107">Syntax</span></span>


```C++
HRESULT get_OffsetX(
  [out, retval] long *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="4d7e8-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="4d7e8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d7e8-109">*pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="4d7e8-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="4d7e8-110">Riceve l'offset orizzontale dell'origine della cancellazione, espresso in pixel.</span><span class="sxs-lookup"><span data-stu-id="4d7e8-110">Receives the horizontal offset of the wipe origin, in pixels.</span></span> <span data-ttu-id="4d7e8-111">Il centro della cancellazione viene sottoposta a offset in base a questa quantità.</span><span class="sxs-lookup"><span data-stu-id="4d7e8-111">The center of the wipe is offset by this amount.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4d7e8-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4d7e8-112">Return value</span></span>

<span data-ttu-id="4d7e8-113">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="4d7e8-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4d7e8-114">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4d7e8-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="4d7e8-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="4d7e8-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="4d7e8-116">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="4d7e8-116">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="4d7e8-117">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="4d7e8-117">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="4d7e8-118">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="4d7e8-118">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4d7e8-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4d7e8-119">Requirements</span></span>



| <span data-ttu-id="4d7e8-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="4d7e8-120">Requirement</span></span> | <span data-ttu-id="4d7e8-121">Valore</span><span class="sxs-lookup"><span data-stu-id="4d7e8-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4d7e8-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4d7e8-122">Header</span></span><br/>  | <dl> <span data-ttu-id="4d7e8-123"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="4d7e8-123"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="4d7e8-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="4d7e8-124">Library</span></span><br/> | <dl> <span data-ttu-id="4d7e8-125"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4d7e8-125"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4d7e8-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4d7e8-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d7e8-127">**Interfaccia IDxtJpeg**</span><span class="sxs-lookup"><span data-stu-id="4d7e8-127">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> </dl>

 

 




