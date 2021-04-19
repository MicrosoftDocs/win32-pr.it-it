---
description: Il metodo successivo ottiene il numero specificato successivo di elementi nella sequenza di enumerazione. Questo metodo è nascosto Visual Basic e linguaggi di scripting.
ms.assetid: bd94f592-ac6f-48b7-8190-352a5e18f224
title: 'Metodo IEnumParticipant:: Next (Confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89586370d01aaac54f05242e0eb3c53eb938c47b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333142"
---
# <a name="ienumparticipantnext-method"></a><span data-ttu-id="8ca05-104">IEnumParticipant:: Next (metodo)</span><span class="sxs-lookup"><span data-stu-id="8ca05-104">IEnumParticipant::Next method</span></span>

<span data-ttu-id="8ca05-105">\[Il passaggio **successivo** non è disponibile per l'utilizzo in Windows Vista, windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="8ca05-105">\[**Next** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="8ca05-106">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="8ca05-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="8ca05-107">Il metodo **successivo** ottiene il numero specificato successivo di elementi nella sequenza di enumerazione.</span><span class="sxs-lookup"><span data-stu-id="8ca05-107">The **Next** method gets the next specified number of elements in the enumeration sequence.</span></span> <span data-ttu-id="8ca05-108">Questo metodo è nascosto Visual Basic e linguaggi di scripting.</span><span class="sxs-lookup"><span data-stu-id="8ca05-108">This method is hidden from Visual Basic and scripting languages.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ca05-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8ca05-109">Syntax</span></span>


```C++
HRESULT Next(
  [in]  ULONG         celt,
  [out] ITParticipant **ppElements,
  [out] ULONG         *pceltFetched
);
```



## <a name="parameters"></a><span data-ttu-id="8ca05-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="8ca05-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ca05-111">*celt* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8ca05-111">*celt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ca05-112">Numero di elementi richiesti.</span><span class="sxs-lookup"><span data-stu-id="8ca05-112">Number of elements requested.</span></span>

</dd> <dt>

<span data-ttu-id="8ca05-113">*ppElements* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="8ca05-113">*ppElements* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8ca05-114">Puntatore a interfacce [**ITAgentHandler**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagenthandler) .</span><span class="sxs-lookup"><span data-stu-id="8ca05-114">Pointer to [**ITAgentHandler**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagenthandler) interfaces.</span></span>

</dd> <dt>

<span data-ttu-id="8ca05-115">*pceltFetched* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="8ca05-115">*pceltFetched* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8ca05-116">Puntatore al numero di elementi effettivamente forniti.</span><span class="sxs-lookup"><span data-stu-id="8ca05-116">Pointer to number of elements actually supplied.</span></span> <span data-ttu-id="8ca05-117">Può essere **null** se *celt* è uno.</span><span class="sxs-lookup"><span data-stu-id="8ca05-117">May be **NULL** if *celt* is one.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ca05-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8ca05-118">Return value</span></span>

<span data-ttu-id="8ca05-119">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="8ca05-119">This method can return one of these values.</span></span>



| <span data-ttu-id="8ca05-120">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="8ca05-120">Return code</span></span>                                                                                   | <span data-ttu-id="8ca05-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8ca05-121">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="8ca05-122"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="8ca05-122"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="8ca05-123">Il metodo ha restituito il numero *celt* di elementi.</span><span class="sxs-lookup"><span data-stu-id="8ca05-123">Method returned *celt* number of elements.</span></span><br/>           |
| <dl> <span data-ttu-id="8ca05-124"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="8ca05-124"><dt>**S\_FALSE**</dt></span></span> </dl>       | <span data-ttu-id="8ca05-125">Il numero di elementi rimanenti è minore di *celt*.</span><span class="sxs-lookup"><span data-stu-id="8ca05-125">Number of elements remaining was less than *celt*.</span></span><br/>   |
| <dl> <span data-ttu-id="8ca05-126"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="8ca05-126"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="8ca05-127">Il parametro *ppElements* non è un puntatore valido.</span><span class="sxs-lookup"><span data-stu-id="8ca05-127">The *ppElements* parameter is not a valid pointer.</span></span><br/>   |
| <dl> <span data-ttu-id="8ca05-128"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="8ca05-128"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="8ca05-129">La memoria disponibile non è sufficiente per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="8ca05-129">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="8ca05-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="8ca05-130">Remarks</span></span>

<span data-ttu-id="8ca05-131">TAPI chiama il metodo [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) sull'interfaccia [**ITAgentHandler**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagenthandler) restituita da **IEnumParticipant:: Next**.</span><span class="sxs-lookup"><span data-stu-id="8ca05-131">TAPI calls the [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) method on the [**ITAgentHandler**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagenthandler) interface returned by **IEnumParticipant::Next**.</span></span> <span data-ttu-id="8ca05-132">L'applicazione deve chiamare [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) sull'interfaccia **ITAgentHandler** per liberare risorse associate.</span><span class="sxs-lookup"><span data-stu-id="8ca05-132">The application must call [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) on the **ITAgentHandler** interface to free resources associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ca05-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8ca05-133">Requirements</span></span>



| <span data-ttu-id="8ca05-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="8ca05-134">Requirement</span></span> | <span data-ttu-id="8ca05-135">Valore</span><span class="sxs-lookup"><span data-stu-id="8ca05-135">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8ca05-136">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="8ca05-136">TAPI version</span></span><br/> | <span data-ttu-id="8ca05-137">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="8ca05-137">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="8ca05-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8ca05-138">Header</span></span><br/>       | <dl> <span data-ttu-id="8ca05-139"><dt>Confpriv. h</dt></span><span class="sxs-lookup"><span data-stu-id="8ca05-139"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="8ca05-140">Libreria</span><span class="sxs-lookup"><span data-stu-id="8ca05-140">Library</span></span><br/>      | <dl> <span data-ttu-id="8ca05-141"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8ca05-141"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="8ca05-142">DLL</span><span class="sxs-lookup"><span data-stu-id="8ca05-142">DLL</span></span><br/>          | <dl> <span data-ttu-id="8ca05-143"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8ca05-143"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="8ca05-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8ca05-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ca05-145">**IEnumParticipant**</span><span class="sxs-lookup"><span data-stu-id="8ca05-145">**IEnumParticipant**</span></span>](ienumparticipant.md)
</dt> <dt>

[<span data-ttu-id="8ca05-146">**ITParticipant**</span><span class="sxs-lookup"><span data-stu-id="8ca05-146">**ITParticipant**</span></span>](itparticipant.md)
</dt> </dl>

 

