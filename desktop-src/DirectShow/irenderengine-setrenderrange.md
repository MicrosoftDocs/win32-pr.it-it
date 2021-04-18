---
description: Il metodo SetRenderRange imposta l'intervallo di tempo nella sequenza temporale di cui eseguire il rendering. Non viene eseguito il rendering degli oggetti che non rientrano nell'intervallo specificato e le risorse non sono allocate.
ms.assetid: 2dcdca6b-2bae-4a27-bfbc-19a9b2ea633a
title: 'Metodo IRenderEngine:: SetRenderRange (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.SetRenderRange
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e715c2c0077a890948cfd5f5026afe98633325ef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330784"
---
# <a name="irenderenginesetrenderrange-method"></a><span data-ttu-id="f8f22-104">Metodo IRenderEngine:: SetRenderRange</span><span class="sxs-lookup"><span data-stu-id="f8f22-104">IRenderEngine::SetRenderRange method</span></span>

> [!Note]  
> <span data-ttu-id="f8f22-105">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="f8f22-105">\[Deprecated.</span></span> <span data-ttu-id="f8f22-106">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f8f22-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="f8f22-107">Il `SetRenderRange` metodo imposta l'intervallo di tempo nella sequenza temporale di cui eseguire il rendering.</span><span class="sxs-lookup"><span data-stu-id="f8f22-107">The `SetRenderRange` method sets the range of time on the timeline to be rendered.</span></span> <span data-ttu-id="f8f22-108">Non viene eseguito il rendering degli oggetti che non rientrano nell'intervallo specificato e le risorse non sono allocate.</span><span class="sxs-lookup"><span data-stu-id="f8f22-108">Objects that lie outside the specified range are not rendered, and resources are not allocated for them.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8f22-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f8f22-109">Syntax</span></span>


```C++
HRESULT SetRenderRange(
   REFERENCE_TIME Start,
   REFERENCE_TIME Stop
);
```



## <a name="parameters"></a><span data-ttu-id="f8f22-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="f8f22-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8f22-111">*Inizia*</span><span class="sxs-lookup"><span data-stu-id="f8f22-111">*Start*</span></span> 
</dt> <dd>

<span data-ttu-id="f8f22-112">Ora di inizio, in unità di 100 nanosecondi.</span><span class="sxs-lookup"><span data-stu-id="f8f22-112">Start time, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="f8f22-113">*Stop*</span><span class="sxs-lookup"><span data-stu-id="f8f22-113">*Stop*</span></span> 
</dt> <dd>

<span data-ttu-id="f8f22-114">Ora di arresto, in unità di 100 nanosecondi.</span><span class="sxs-lookup"><span data-stu-id="f8f22-114">Stop time, in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8f22-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f8f22-115">Return value</span></span>

<span data-ttu-id="f8f22-116">Restituisce uno dei seguenti valori **HRESULT** :</span><span class="sxs-lookup"><span data-stu-id="f8f22-116">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="f8f22-117">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="f8f22-117">Return code</span></span>                                                                                            | <span data-ttu-id="f8f22-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f8f22-118">Description</span></span>                                    |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="f8f22-119"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f8f22-119"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="f8f22-120">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="f8f22-120">Success.</span></span><br/>                            |
| <dl> <span data-ttu-id="f8f22-121"><dt>**E \_ deve \_ inizializzare il \_ RENDERER**</dt></span><span class="sxs-lookup"><span data-stu-id="f8f22-121"><dt>**E\_MUST\_INIT\_RENDERER**</dt></span></span> </dl> | <span data-ttu-id="f8f22-122">Impossibile inizializzare il motore di rendering.</span><span class="sxs-lookup"><span data-stu-id="f8f22-122">Render engine failed to initialize.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f8f22-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="f8f22-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="f8f22-124">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="f8f22-124">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="f8f22-125">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="f8f22-125">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="f8f22-126">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="f8f22-126">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f8f22-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f8f22-127">Requirements</span></span>



| <span data-ttu-id="f8f22-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="f8f22-128">Requirement</span></span> | <span data-ttu-id="f8f22-129">Valore</span><span class="sxs-lookup"><span data-stu-id="f8f22-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f8f22-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f8f22-130">Header</span></span><br/>  | <dl> <span data-ttu-id="f8f22-131"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="f8f22-131"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="f8f22-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="f8f22-132">Library</span></span><br/> | <dl> <span data-ttu-id="f8f22-133"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f8f22-133"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8f22-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f8f22-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8f22-135">**Interfaccia IRenderEngine**</span><span class="sxs-lookup"><span data-stu-id="f8f22-135">**IRenderEngine Interface**</span></span>](irenderengine.md)
</dt> <dt>

[<span data-ttu-id="f8f22-136">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="f8f22-136">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




