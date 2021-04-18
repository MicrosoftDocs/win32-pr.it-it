---
description: Il metodo SetMediaTypeForVB specifica il tipo di supporto di gruppo per i client di automazione.
ms.assetid: 86f52088-a0dd-40be-98a0-8adc09b264dd
title: 'Metodo IAMTimelineGroup:: SetMediaTypeForVB (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.SetMediaTypeForVB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 1371b1d6c906666ca30e5df2d26dbe20eddf1745
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331629"
---
# <a name="iamtimelinegroupsetmediatypeforvb-method"></a><span data-ttu-id="8a16c-103">Metodo IAMTimelineGroup:: SetMediaTypeForVB</span><span class="sxs-lookup"><span data-stu-id="8a16c-103">IAMTimelineGroup::SetMediaTypeForVB method</span></span>

> [!Note]  
> <span data-ttu-id="8a16c-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="8a16c-104">\[Deprecated.</span></span> <span data-ttu-id="8a16c-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="8a16c-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="8a16c-106">Il `SetMediaTypeForVB` metodo specifica il tipo di supporto di gruppo per i client di automazione.</span><span class="sxs-lookup"><span data-stu-id="8a16c-106">The `SetMediaTypeForVB` method specifies the group media type, for Automation clients.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a16c-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8a16c-107">Syntax</span></span>


```C++
HRESULT SetMediaTypeForVB(
  [in] long Val
);
```



## <a name="parameters"></a><span data-ttu-id="8a16c-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="8a16c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a16c-109">*Val* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8a16c-109">*Val* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a16c-110">Valore che specifica il tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="8a16c-110">Value that specifies the media type.</span></span> <span data-ttu-id="8a16c-111">Impostare il valore su 0 per video o 1 per audio.</span><span class="sxs-lookup"><span data-stu-id="8a16c-111">Set the value to 0 for video, or 1 for audio.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a16c-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8a16c-112">Return value</span></span>

<span data-ttu-id="8a16c-113">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="8a16c-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8a16c-114">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8a16c-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="8a16c-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="8a16c-115">Remarks</span></span>

<span data-ttu-id="8a16c-116">Questo metodo è destinato ai client di automazione.</span><span class="sxs-lookup"><span data-stu-id="8a16c-116">This method is intended for Automation clients.</span></span> <span data-ttu-id="8a16c-117">Per le applicazioni C++, usare il metodo [**IAMTimelineGroup:: SetMediaType**](iamtimelinegroup-setmediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="8a16c-117">For C++ applications, use the [**IAMTimelineGroup::SetMediaType**](iamtimelinegroup-setmediatype.md) method.</span></span>

> [!Note]  
> <span data-ttu-id="8a16c-118">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="8a16c-118">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="8a16c-119">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="8a16c-119">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="8a16c-120">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="8a16c-120">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8a16c-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8a16c-121">Requirements</span></span>



| <span data-ttu-id="8a16c-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="8a16c-122">Requirement</span></span> | <span data-ttu-id="8a16c-123">Valore</span><span class="sxs-lookup"><span data-stu-id="8a16c-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8a16c-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8a16c-124">Header</span></span><br/>  | <dl> <span data-ttu-id="8a16c-125"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="8a16c-125"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="8a16c-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="8a16c-126">Library</span></span><br/> | <dl> <span data-ttu-id="8a16c-127"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8a16c-127"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8a16c-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8a16c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a16c-129">**Interfaccia IAMTimelineGroup**</span><span class="sxs-lookup"><span data-stu-id="8a16c-129">**IAMTimelineGroup Interface**</span></span>](iamtimelinegroup.md)
</dt> <dt>

[<span data-ttu-id="8a16c-130">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="8a16c-130">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




