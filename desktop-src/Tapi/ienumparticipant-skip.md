---
description: Il metodo Skip ignora il successivo numero specificato di elementi nella sequenza di enumerazione. Questo metodo è nascosto Visual Basic e linguaggi di scripting.
ms.assetid: 7f641354-c3f5-4eb3-ad1c-98abf7694106
title: 'Metodo IEnumParticipant:: Skip (Confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6dc406a69c126c25b1c554679595868a595b839b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330751"
---
# <a name="ienumparticipantskip-method"></a><span data-ttu-id="c334e-104">Metodo IEnumParticipant:: Skip</span><span class="sxs-lookup"><span data-stu-id="c334e-104">IEnumParticipant::Skip method</span></span>

<span data-ttu-id="c334e-105">\[**Skip** non è disponibile per l'utilizzo in Windows Vista, windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="c334e-105">\[**Skip** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="c334e-106">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="c334e-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="c334e-107">Il metodo **Skip** ignora il successivo numero specificato di elementi nella sequenza di enumerazione.</span><span class="sxs-lookup"><span data-stu-id="c334e-107">The **Skip** method skips over the next specified number of elements in the enumeration sequence.</span></span> <span data-ttu-id="c334e-108">Questo metodo è nascosto Visual Basic e linguaggi di scripting.</span><span class="sxs-lookup"><span data-stu-id="c334e-108">This method is hidden from Visual Basic and scripting languages.</span></span>

## <a name="syntax"></a><span data-ttu-id="c334e-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c334e-109">Syntax</span></span>


```C++
HRESULT Skip(
  [in] ULONG celt
);
```



## <a name="parameters"></a><span data-ttu-id="c334e-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="c334e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c334e-111">*celt* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c334e-111">*celt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c334e-112">Numero di elementi da ignorare.</span><span class="sxs-lookup"><span data-stu-id="c334e-112">Number of elements to skip.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c334e-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c334e-113">Return value</span></span>

<span data-ttu-id="c334e-114">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="c334e-114">This method can return one of these values.</span></span>



| <span data-ttu-id="c334e-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="c334e-115">Return code</span></span>                                                                                   | <span data-ttu-id="c334e-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c334e-116">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="c334e-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c334e-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="c334e-118">Il numero di elementi ignorati è *celt*.</span><span class="sxs-lookup"><span data-stu-id="c334e-118">Number of elements skipped was *celt*.</span></span><br/>               |
| <dl> <span data-ttu-id="c334e-119"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="c334e-119"><dt>**S\_FALSE**</dt></span></span> </dl>       | <span data-ttu-id="c334e-120">Il numero di elementi ignorati non è *celt*.</span><span class="sxs-lookup"><span data-stu-id="c334e-120">Number of elements skipped was not *celt*.</span></span><br/>           |
| <dl> <span data-ttu-id="c334e-121"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="c334e-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="c334e-122">La memoria disponibile non è sufficiente per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="c334e-122">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="c334e-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c334e-123">Requirements</span></span>



| <span data-ttu-id="c334e-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="c334e-124">Requirement</span></span> | <span data-ttu-id="c334e-125">Valore</span><span class="sxs-lookup"><span data-stu-id="c334e-125">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c334e-126">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="c334e-126">TAPI version</span></span><br/> | <span data-ttu-id="c334e-127">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="c334e-127">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="c334e-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c334e-128">Header</span></span><br/>       | <dl> <span data-ttu-id="c334e-129"><dt>Confpriv. h</dt></span><span class="sxs-lookup"><span data-stu-id="c334e-129"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="c334e-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="c334e-130">Library</span></span><br/>      | <dl> <span data-ttu-id="c334e-131"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c334e-131"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="c334e-132">DLL</span><span class="sxs-lookup"><span data-stu-id="c334e-132">DLL</span></span><br/>          | <dl> <span data-ttu-id="c334e-133"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c334e-133"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="c334e-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c334e-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c334e-135">**IEnumParticipant**</span><span class="sxs-lookup"><span data-stu-id="c334e-135">**IEnumParticipant**</span></span>](ienumparticipant.md)
</dt> <dt>

[<span data-ttu-id="c334e-136">**ITParticipant**</span><span class="sxs-lookup"><span data-stu-id="c334e-136">**ITParticipant**</span></span>](itparticipant.md)
</dt> </dl>

 

 




