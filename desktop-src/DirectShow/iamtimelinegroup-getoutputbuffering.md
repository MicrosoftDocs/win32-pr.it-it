---
description: Il metodo GetOutputBuffering Recupera il numero di frame di cui è stato eseguito il rendering in anticipo durante l'anteprima.
ms.assetid: 93cb8d18-f1b7-48f9-af41-97f010304b05
title: 'Metodo IAMTimelineGroup:: GetOutputBuffering (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.GetOutputBuffering
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8213be882ca445775137a946d9064487b25f48af
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333684"
---
# <a name="iamtimelinegroupgetoutputbuffering-method"></a><span data-ttu-id="56914-103">Metodo IAMTimelineGroup:: GetOutputBuffering</span><span class="sxs-lookup"><span data-stu-id="56914-103">IAMTimelineGroup::GetOutputBuffering method</span></span>

> [!Note]  
> <span data-ttu-id="56914-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="56914-104">\[Deprecated.</span></span> <span data-ttu-id="56914-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="56914-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="56914-106">Il `GetOutputBuffering` metodo recupera il numero di frame di cui è stato eseguito il rendering in anticipo durante l'anteprima.</span><span class="sxs-lookup"><span data-stu-id="56914-106">The `GetOutputBuffering` method retrieves the number of frames rendered in advance during preview.</span></span>

## <a name="syntax"></a><span data-ttu-id="56914-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="56914-107">Syntax</span></span>


```C++
HRESULT GetOutputBuffering(
  [out] int *pnBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="56914-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="56914-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56914-109">*pnBuffer* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="56914-109">*pnBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="56914-110">Riceve il numero di frame memorizzati nel buffer.</span><span class="sxs-lookup"><span data-stu-id="56914-110">Receives the number of buffered frames.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56914-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="56914-111">Return value</span></span>

<span data-ttu-id="56914-112">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="56914-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="56914-113">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="56914-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="56914-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="56914-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="56914-115">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="56914-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="56914-116">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="56914-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="56914-117">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="56914-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="56914-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="56914-118">Requirements</span></span>



| <span data-ttu-id="56914-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="56914-119">Requirement</span></span> | <span data-ttu-id="56914-120">Valore</span><span class="sxs-lookup"><span data-stu-id="56914-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="56914-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="56914-121">Header</span></span><br/>  | <dl> <span data-ttu-id="56914-122"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="56914-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="56914-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="56914-123">Library</span></span><br/> | <dl> <span data-ttu-id="56914-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="56914-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56914-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="56914-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56914-126">**Interfaccia IAMTimelineGroup**</span><span class="sxs-lookup"><span data-stu-id="56914-126">**IAMTimelineGroup Interface**</span></span>](iamtimelinegroup.md)
</dt> <dt>

[<span data-ttu-id="56914-127">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="56914-127">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




