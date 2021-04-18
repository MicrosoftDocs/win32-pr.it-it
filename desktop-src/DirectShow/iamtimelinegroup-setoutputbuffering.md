---
description: Il metodo SetOutputBuffering specifica il numero di frame di cui è stato eseguito il rendering in anticipo durante l'anteprima.
ms.assetid: 6e69b196-a6ce-4ce0-8c48-58b1738fb197
title: 'Metodo IAMTimelineGroup:: SetOutputBuffering (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.SetOutputBuffering
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ab249c1a6af63b0fc0f2ee535daeab1dec9cd558
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331628"
---
# <a name="iamtimelinegroupsetoutputbuffering-method"></a><span data-ttu-id="fa906-103">Metodo IAMTimelineGroup:: SetOutputBuffering</span><span class="sxs-lookup"><span data-stu-id="fa906-103">IAMTimelineGroup::SetOutputBuffering method</span></span>

> [!Note]  
> <span data-ttu-id="fa906-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="fa906-104">\[Deprecated.</span></span> <span data-ttu-id="fa906-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="fa906-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="fa906-106">Il `SetOutputBuffering` metodo specifica il numero di frame di cui è stato eseguito il rendering in anticipo durante l'anteprima.</span><span class="sxs-lookup"><span data-stu-id="fa906-106">The `SetOutputBuffering` method specifies the number of frames rendered in advance during preview.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa906-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fa906-107">Syntax</span></span>


```C++
HRESULT SetOutputBuffering(
  [in] int nBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="fa906-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="fa906-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa906-109">*nBuffer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fa906-109">*nBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa906-110">Numero di frame da memorizzare nel buffer durante l'anteprima.</span><span class="sxs-lookup"><span data-stu-id="fa906-110">Number of frames to buffer during preview.</span></span> <span data-ttu-id="fa906-111">Deve essere maggiore o uguale a due.</span><span class="sxs-lookup"><span data-stu-id="fa906-111">Must be two or greater.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa906-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fa906-112">Return value</span></span>

<span data-ttu-id="fa906-113">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="fa906-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="fa906-114">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="fa906-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="fa906-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="fa906-115">Remarks</span></span>

<span data-ttu-id="fa906-116">Un buffer più grande richiede più memoria, ma può comportare una visualizzazione in anteprima più uniforme, soprattutto durante gli effetti o le transizioni che richiedono più tempo per il rendering.</span><span class="sxs-lookup"><span data-stu-id="fa906-116">A larger buffer requires more memory but can result in smoother previewing, especially during effects or transitions that require more time to render.</span></span> <span data-ttu-id="fa906-117">Il buffer predefinito è 30 fotogrammi.</span><span class="sxs-lookup"><span data-stu-id="fa906-117">The default buffer is 30 frames.</span></span>

> [!Note]  
> <span data-ttu-id="fa906-118">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="fa906-118">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="fa906-119">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="fa906-119">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="fa906-120">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="fa906-120">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="fa906-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fa906-121">Requirements</span></span>



| <span data-ttu-id="fa906-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="fa906-122">Requirement</span></span> | <span data-ttu-id="fa906-123">Valore</span><span class="sxs-lookup"><span data-stu-id="fa906-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fa906-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fa906-124">Header</span></span><br/>  | <dl> <span data-ttu-id="fa906-125"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="fa906-125"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="fa906-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="fa906-126">Library</span></span><br/> | <dl> <span data-ttu-id="fa906-127"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fa906-127"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fa906-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fa906-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa906-129">**Interfaccia IAMTimelineGroup**</span><span class="sxs-lookup"><span data-stu-id="fa906-129">**IAMTimelineGroup Interface**</span></span>](iamtimelinegroup.md)
</dt> <dt>

[<span data-ttu-id="fa906-130">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="fa906-130">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




