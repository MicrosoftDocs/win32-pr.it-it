---
description: "Il metodo SetRenderRange2 imposta l'intervallo di tempo nella sequenza temporale di cui eseguire il rendering. Questo metodo è equivalente a IRenderEngine:: SetRenderRange, ma accetta valori di tipo Double."
ms.assetid: 07df97a8-aa83-405d-91a0-45cd99185588
title: 'Metodo IRenderEngine:: SetRenderRange2 (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.SetRenderRange2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 555533b11c96073763af0d2b52823af44e3797be
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330783"
---
# <a name="irenderenginesetrenderrange2-method"></a><span data-ttu-id="1c999-104">Metodo IRenderEngine:: SetRenderRange2</span><span class="sxs-lookup"><span data-stu-id="1c999-104">IRenderEngine::SetRenderRange2 method</span></span>

> [!Note]  
> <span data-ttu-id="1c999-105">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="1c999-105">\[Deprecated.</span></span> <span data-ttu-id="1c999-106">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="1c999-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="1c999-107">Il `SetRenderRange2` metodo imposta l'intervallo di tempo nella sequenza temporale di cui eseguire il rendering.</span><span class="sxs-lookup"><span data-stu-id="1c999-107">The `SetRenderRange2` method sets the range of time on the timeline to be rendered.</span></span> <span data-ttu-id="1c999-108">Questo metodo è equivalente a [**IRenderEngine:: SetRenderRange**](irenderengine-setrenderrange.md), ma accetta valori di tipo **Double**.</span><span class="sxs-lookup"><span data-stu-id="1c999-108">This method is equivalent to [**IRenderEngine::SetRenderRange**](irenderengine-setrenderrange.md), but takes values of type **double**.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c999-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1c999-109">Syntax</span></span>


```C++
HRESULT SetRenderRange2(
   double Start,
   double Stop
);
```



## <a name="parameters"></a><span data-ttu-id="1c999-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="1c999-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c999-111">*Inizia*</span><span class="sxs-lookup"><span data-stu-id="1c999-111">*Start*</span></span> 
</dt> <dd>

<span data-ttu-id="1c999-112">Ora di inizio, in secondi.</span><span class="sxs-lookup"><span data-stu-id="1c999-112">Start time, in seconds.</span></span>

</dd> <dt>

<span data-ttu-id="1c999-113">*Stop*</span><span class="sxs-lookup"><span data-stu-id="1c999-113">*Stop*</span></span> 
</dt> <dd>

<span data-ttu-id="1c999-114">Tempo di arresto, in secondi.</span><span class="sxs-lookup"><span data-stu-id="1c999-114">Stop time, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c999-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1c999-115">Return value</span></span>

<span data-ttu-id="1c999-116">Restituisce uno dei seguenti valori **HRESULT** :</span><span class="sxs-lookup"><span data-stu-id="1c999-116">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="1c999-117">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="1c999-117">Return code</span></span>                                                                                            | <span data-ttu-id="1c999-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1c999-118">Description</span></span>                                    |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="1c999-119"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="1c999-119"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="1c999-120">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="1c999-120">Success.</span></span><br/>                            |
| <dl> <span data-ttu-id="1c999-121"><dt>**E \_ deve \_ inizializzare il \_ RENDERER**</dt></span><span class="sxs-lookup"><span data-stu-id="1c999-121"><dt>**E\_MUST\_INIT\_RENDERER**</dt></span></span> </dl> | <span data-ttu-id="1c999-122">Impossibile inizializzare il motore di rendering.</span><span class="sxs-lookup"><span data-stu-id="1c999-122">Render engine failed to initialize.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="1c999-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="1c999-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="1c999-124">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="1c999-124">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="1c999-125">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="1c999-125">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="1c999-126">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="1c999-126">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="1c999-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1c999-127">Requirements</span></span>



| <span data-ttu-id="1c999-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="1c999-128">Requirement</span></span> | <span data-ttu-id="1c999-129">Valore</span><span class="sxs-lookup"><span data-stu-id="1c999-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1c999-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1c999-130">Header</span></span><br/>  | <dl> <span data-ttu-id="1c999-131"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="1c999-131"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="1c999-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="1c999-132">Library</span></span><br/> | <dl> <span data-ttu-id="1c999-133"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1c999-133"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c999-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1c999-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c999-135">**Interfaccia IRenderEngine**</span><span class="sxs-lookup"><span data-stu-id="1c999-135">**IRenderEngine Interface**</span></span>](irenderengine.md)
</dt> <dt>

[<span data-ttu-id="1c999-136">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="1c999-136">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




