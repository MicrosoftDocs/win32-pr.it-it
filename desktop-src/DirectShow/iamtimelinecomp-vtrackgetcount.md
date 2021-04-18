---
description: Il metodo VTrackGetCount Recupera il numero di tracce virtuali contenute nella composizione.
ms.assetid: a8117b06-4f42-45da-9b93-f547cb70aa5d
title: 'Metodo IAMTimelineComp:: VTrackGetCount (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineComp.VTrackGetCount
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 36800381ce50ea60d5252841d9731b2657fc22cd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332036"
---
# <a name="iamtimelinecompvtrackgetcount-method"></a><span data-ttu-id="a16a5-103">Metodo IAMTimelineComp:: VTrackGetCount</span><span class="sxs-lookup"><span data-stu-id="a16a5-103">IAMTimelineComp::VTrackGetCount method</span></span>

> [!Note]  
> <span data-ttu-id="a16a5-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="a16a5-104">\[Deprecated.</span></span> <span data-ttu-id="a16a5-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a16a5-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="a16a5-106">Il `VTrackGetCount` metodo recupera il numero di tracce virtuali contenute nella composizione.</span><span class="sxs-lookup"><span data-stu-id="a16a5-106">The `VTrackGetCount` method retrieves the number of virtual tracks contained in the composition.</span></span>

## <a name="syntax"></a><span data-ttu-id="a16a5-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a16a5-107">Syntax</span></span>


```C++
HRESULT VTrackGetCount(
   long *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="a16a5-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="a16a5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a16a5-109">*pVal*</span><span class="sxs-lookup"><span data-stu-id="a16a5-109">*pVal*</span></span> 
</dt> <dd>

<span data-ttu-id="a16a5-110">Riceve il numero di tracce virtuali.</span><span class="sxs-lookup"><span data-stu-id="a16a5-110">Receives the number of virtual tracks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a16a5-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a16a5-111">Return value</span></span>

<span data-ttu-id="a16a5-112">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="a16a5-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a16a5-113">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a16a5-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a16a5-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="a16a5-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="a16a5-115">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="a16a5-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="a16a5-116">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="a16a5-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="a16a5-117">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="a16a5-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a16a5-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a16a5-118">Requirements</span></span>



| <span data-ttu-id="a16a5-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="a16a5-119">Requirement</span></span> | <span data-ttu-id="a16a5-120">Valore</span><span class="sxs-lookup"><span data-stu-id="a16a5-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a16a5-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a16a5-121">Header</span></span><br/>  | <dl> <span data-ttu-id="a16a5-122"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="a16a5-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="a16a5-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="a16a5-123">Library</span></span><br/> | <dl> <span data-ttu-id="a16a5-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a16a5-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a16a5-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a16a5-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a16a5-126">**Interfaccia IAMTimelineComp**</span><span class="sxs-lookup"><span data-stu-id="a16a5-126">**IAMTimelineComp Interface**</span></span>](iamtimelinecomp.md)
</dt> <dt>

[<span data-ttu-id="a16a5-127">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="a16a5-127">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




