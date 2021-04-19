---
description: Il Metodo LogError registra un errore. Le applicazioni non devono chiamare questo metodo. Viene chiamato internamente in risposta agli errori di rendering.
ms.assetid: 08765c8a-21ca-4c40-84a8-d13da87d9c5f
title: 'Metodo IAMErrorLog:: LogError (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMErrorLog.LogError
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: dc94532639f325b53db850ebe8a5af489a8b3cf2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326822"
---
# <a name="iamerrorloglogerror-method"></a><span data-ttu-id="80a73-105">Metodo IAMErrorLog:: LogError</span><span class="sxs-lookup"><span data-stu-id="80a73-105">IAMErrorLog::LogError method</span></span>

> [!Note]  
> <span data-ttu-id="80a73-106">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="80a73-106">\[Deprecated.</span></span> <span data-ttu-id="80a73-107">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="80a73-107">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="80a73-108">Il metodo **LogError** registra un errore.</span><span class="sxs-lookup"><span data-stu-id="80a73-108">The **LogError** method logs an error.</span></span> <span data-ttu-id="80a73-109">Le applicazioni non devono chiamare questo metodo.</span><span class="sxs-lookup"><span data-stu-id="80a73-109">Applications do not need to call this method.</span></span> <span data-ttu-id="80a73-110">Viene chiamato internamente in risposta agli errori di rendering.</span><span class="sxs-lookup"><span data-stu-id="80a73-110">It is called internally in response to rendering errors.</span></span>

## <a name="syntax"></a><span data-ttu-id="80a73-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="80a73-111">Syntax</span></span>


```C++
HRESULT LogError(
       LONG    Severity,
       BSTR    ErrorString,
       LONG    ErrorCode,
       HRESULT hresult,
  [in] VARIANT *pExtraInfo
);
```



## <a name="parameters"></a><span data-ttu-id="80a73-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="80a73-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80a73-113">*Gravità*</span><span class="sxs-lookup"><span data-stu-id="80a73-113">*Severity*</span></span> 
</dt> <dd>

<span data-ttu-id="80a73-114">Riservato.</span><span class="sxs-lookup"><span data-stu-id="80a73-114">Reserved.</span></span> <span data-ttu-id="80a73-115">Non usare.</span><span class="sxs-lookup"><span data-stu-id="80a73-115">Do not use.</span></span>

</dd> <dt>

<span data-ttu-id="80a73-116">*ErrorString*</span><span class="sxs-lookup"><span data-stu-id="80a73-116">*ErrorString*</span></span> 
</dt> <dd>

<span data-ttu-id="80a73-117">Valore stringa contenente il testo dell'errore.</span><span class="sxs-lookup"><span data-stu-id="80a73-117">String value containing the text of the error.</span></span>

</dd> <dt>

<span data-ttu-id="80a73-118">*ErrorCode*</span><span class="sxs-lookup"><span data-stu-id="80a73-118">*ErrorCode*</span></span> 
</dt> <dd>

<span data-ttu-id="80a73-119">Codice di errore.</span><span class="sxs-lookup"><span data-stu-id="80a73-119">Error code.</span></span>

</dd> <dt>

<span data-ttu-id="80a73-120">*HRESULT*</span><span class="sxs-lookup"><span data-stu-id="80a73-120">*hresult*</span></span> 
</dt> <dd>

<span data-ttu-id="80a73-121">Valore HRESULT restituito dalla chiamata al metodo che ha causato l'errore.</span><span class="sxs-lookup"><span data-stu-id="80a73-121">The HRESULT value that was returned by the method call that caused the error.</span></span>

</dd> <dt>

<span data-ttu-id="80a73-122">*pExtraInfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="80a73-122">*pExtraInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80a73-123">Puntatore a una variante che contiene informazioni aggiuntive sull'errore.</span><span class="sxs-lookup"><span data-stu-id="80a73-123">Pointer to a VARIANT that contains any additional information about the error.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="80a73-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="80a73-124">Return value</span></span>

<span data-ttu-id="80a73-125">Restituisce il valore del parametro *HRESULT* .</span><span class="sxs-lookup"><span data-stu-id="80a73-125">Return the value of the *hresult* parameter.</span></span>

## <a name="remarks"></a><span data-ttu-id="80a73-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="80a73-126">Remarks</span></span>

<span data-ttu-id="80a73-127">All'interno di questo metodo, non liberare il **Variant** a cui punta *pExtraInfo*.</span><span class="sxs-lookup"><span data-stu-id="80a73-127">Within this method, do not free the **VARIANT** pointed to by *pExtraInfo*.</span></span> <span data-ttu-id="80a73-128">Inoltre, la **variante** diventa non valida dopo la restituzione del metodo, pertanto non tentare di farvi riferimento in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="80a73-128">Also, the **VARIANT** becomes invalid after the method returns, so do not try to reference it later.</span></span>

<span data-ttu-id="80a73-129">Implementare questo metodo per restituire il più rapidamente possibile.</span><span class="sxs-lookup"><span data-stu-id="80a73-129">Implement this method to return as quickly as possible.</span></span> <span data-ttu-id="80a73-130">Non eseguire chiamate di funzione dall'interno di questo metodo che potrebbero bloccare l'esecuzione del programma.</span><span class="sxs-lookup"><span data-stu-id="80a73-130">Do not make function calls from inside this method that might block program execution.</span></span> <span data-ttu-id="80a73-131">Ad esempio, non chiamare funzioni che inviano messaggi della finestra, bloccano gli eventi o altrimenti potrebbero bloccare l'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="80a73-131">For example, do not call functions that send window messages, block on events, or otherwise might block execution.</span></span> <span data-ttu-id="80a73-132">Questa operazione potrebbe causare l'interruzione della risposta del computer.</span><span class="sxs-lookup"><span data-stu-id="80a73-132">Doing so could cause the computer to stop responding.</span></span>

<span data-ttu-id="80a73-133">Per un elenco degli errori definiti da DES, oltre al significato e al tipo di dati della **variante** a cui punta *PExtraInfo*, vedere [errori di rendering](rendering-errors.md).</span><span class="sxs-lookup"><span data-stu-id="80a73-133">For a list of errors defined by DES, along with the meaning and data type of the **VARIANT** pointed to by *pExtraInfo*, see [Rendering Errors](rendering-errors.md).</span></span>

> [!Note]  
> <span data-ttu-id="80a73-134">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="80a73-134">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="80a73-135">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="80a73-135">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="80a73-136">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="80a73-136">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="80a73-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="80a73-137">Requirements</span></span>



| <span data-ttu-id="80a73-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="80a73-138">Requirement</span></span> | <span data-ttu-id="80a73-139">Valore</span><span class="sxs-lookup"><span data-stu-id="80a73-139">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="80a73-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="80a73-140">Header</span></span><br/>  | <dl> <span data-ttu-id="80a73-141"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="80a73-141"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="80a73-142">Libreria</span><span class="sxs-lookup"><span data-stu-id="80a73-142">Library</span></span><br/> | <dl> <span data-ttu-id="80a73-143"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="80a73-143"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="80a73-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="80a73-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80a73-145">**Interfaccia IAMErrorLog**</span><span class="sxs-lookup"><span data-stu-id="80a73-145">**IAMErrorLog Interface**</span></span>](iamerrorlog.md)
</dt> <dt>

[<span data-ttu-id="80a73-146">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="80a73-146">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




