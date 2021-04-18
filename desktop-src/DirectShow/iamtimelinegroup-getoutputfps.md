---
description: Il metodo GetOutputFPS recupera la frequenza dei fotogrammi di output di questo gruppo.
ms.assetid: e6dfa4a9-4d44-4ce7-9aec-3564fd337ff6
title: 'Metodo IAMTimelineGroup:: GetOutputFPS (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.GetOutputFPS
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 2f02e7db36e5ea61e3c738b4c2d92678674bfcec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333681"
---
# <a name="iamtimelinegroupgetoutputfps-method"></a><span data-ttu-id="8f87c-103">Metodo IAMTimelineGroup:: GetOutputFPS</span><span class="sxs-lookup"><span data-stu-id="8f87c-103">IAMTimelineGroup::GetOutputFPS method</span></span>

> [!Note]  
> <span data-ttu-id="8f87c-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="8f87c-104">\[Deprecated.</span></span> <span data-ttu-id="8f87c-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="8f87c-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="8f87c-106">Il `GetOutputFPS` metodo recupera la frequenza dei fotogrammi di output di questo gruppo.</span><span class="sxs-lookup"><span data-stu-id="8f87c-106">The `GetOutputFPS` method retrieves the output frame rate of this group.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f87c-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8f87c-107">Syntax</span></span>


```C++
HRESULT GetOutputFPS(
   double *pFPS
);
```



## <a name="parameters"></a><span data-ttu-id="8f87c-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="8f87c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f87c-109">*pFPS*</span><span class="sxs-lookup"><span data-stu-id="8f87c-109">*pFPS*</span></span> 
</dt> <dd>

<span data-ttu-id="8f87c-110">Riceve la frequenza dei fotogrammi di output, in frame al secondo.</span><span class="sxs-lookup"><span data-stu-id="8f87c-110">Receives the output frame rate, in frames per second.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8f87c-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8f87c-111">Return value</span></span>

<span data-ttu-id="8f87c-112">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="8f87c-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8f87c-113">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8f87c-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="8f87c-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="8f87c-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="8f87c-115">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="8f87c-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="8f87c-116">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="8f87c-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="8f87c-117">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="8f87c-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8f87c-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8f87c-118">Requirements</span></span>



| <span data-ttu-id="8f87c-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="8f87c-119">Requirement</span></span> | <span data-ttu-id="8f87c-120">Valore</span><span class="sxs-lookup"><span data-stu-id="8f87c-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8f87c-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8f87c-121">Header</span></span><br/>  | <dl> <span data-ttu-id="8f87c-122"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="8f87c-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="8f87c-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="8f87c-123">Library</span></span><br/> | <dl> <span data-ttu-id="8f87c-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8f87c-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f87c-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8f87c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f87c-126">**Interfaccia IAMTimelineGroup**</span><span class="sxs-lookup"><span data-stu-id="8f87c-126">**IAMTimelineGroup Interface**</span></span>](iamtimelinegroup.md)
</dt> <dt>

[<span data-ttu-id="8f87c-127">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="8f87c-127">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




