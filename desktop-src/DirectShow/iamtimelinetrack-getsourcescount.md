---
description: Il metodo GetSourcesCount Recupera il numero di origini nella traccia.
ms.assetid: eb7f249f-355f-454d-9fe6-c3271fd13fc7
title: 'Metodo IAMTimelineTrack:: GetSourcesCount (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.GetSourcesCount
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 0e143b16e5cdc1e193760c0b97846be07eb72c0e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325634"
---
# <a name="iamtimelinetrackgetsourcescount-method"></a><span data-ttu-id="ec286-103">Metodo IAMTimelineTrack:: GetSourcesCount</span><span class="sxs-lookup"><span data-stu-id="ec286-103">IAMTimelineTrack::GetSourcesCount method</span></span>

> [!Note]  
> <span data-ttu-id="ec286-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="ec286-104">\[Deprecated.</span></span> <span data-ttu-id="ec286-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="ec286-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="ec286-106">Il `GetSourcesCount` metodo recupera il numero di origini nella traccia.</span><span class="sxs-lookup"><span data-stu-id="ec286-106">The `GetSourcesCount` method retrieves the number of sources in the track.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec286-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ec286-107">Syntax</span></span>


```C++
HRESULT GetSourcesCount(
   long *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="ec286-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="ec286-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec286-109">*pVal*</span><span class="sxs-lookup"><span data-stu-id="ec286-109">*pVal*</span></span> 
</dt> <dd>

<span data-ttu-id="ec286-110">Riceve il numero di origini nella traccia.</span><span class="sxs-lookup"><span data-stu-id="ec286-110">Receives the number of sources in the track.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec286-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ec286-111">Return value</span></span>

<span data-ttu-id="ec286-112">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="ec286-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ec286-113">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ec286-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="ec286-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="ec286-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="ec286-115">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="ec286-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="ec286-116">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="ec286-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="ec286-117">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="ec286-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ec286-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ec286-118">Requirements</span></span>



| <span data-ttu-id="ec286-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="ec286-119">Requirement</span></span> | <span data-ttu-id="ec286-120">Valore</span><span class="sxs-lookup"><span data-stu-id="ec286-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ec286-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ec286-121">Header</span></span><br/>  | <dl> <span data-ttu-id="ec286-122"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="ec286-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="ec286-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="ec286-123">Library</span></span><br/> | <dl> <span data-ttu-id="ec286-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ec286-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec286-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ec286-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec286-126">**Interfaccia IAMTimelineTrack**</span><span class="sxs-lookup"><span data-stu-id="ec286-126">**IAMTimelineTrack Interface**</span></span>](iamtimelinetrack.md)
</dt> <dt>

[<span data-ttu-id="ec286-127">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="ec286-127">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




