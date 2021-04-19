---
description: Il metodo Clone crea un altro enumeratore che contiene lo stesso stato di enumerazione di quello corrente. Questo metodo è nascosto Visual Basic e linguaggi di scripting.
ms.assetid: 551e0ddc-7ebf-4fc2-a155-0c9ee2f406d4
title: 'Metodo IEnumParticipant:: Clone (Confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5b094f47738fd23f2762b7012a4e23c8b89da57
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333144"
---
# <a name="ienumparticipantclone-method"></a><span data-ttu-id="084ad-104">Metodo IEnumParticipant:: Clone</span><span class="sxs-lookup"><span data-stu-id="084ad-104">IEnumParticipant::Clone method</span></span>

<span data-ttu-id="084ad-105">\[Il **Clone** non è disponibile per l'utilizzo in Windows Vista, windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="084ad-105">\[**Clone** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="084ad-106">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="084ad-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="084ad-107">Il metodo **Clone** crea un altro enumeratore che contiene lo stesso stato di enumerazione di quello corrente.</span><span class="sxs-lookup"><span data-stu-id="084ad-107">The **Clone** method creates another enumerator that contains the same enumeration state as the current one.</span></span> <span data-ttu-id="084ad-108">Questo metodo è nascosto Visual Basic e linguaggi di scripting.</span><span class="sxs-lookup"><span data-stu-id="084ad-108">This method is hidden from Visual Basic and scripting languages.</span></span>

## <a name="syntax"></a><span data-ttu-id="084ad-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="084ad-109">Syntax</span></span>


```C++
HRESULT Clone(
  [out] IEnumParticipant **ppEnum
);
```



## <a name="parameters"></a><span data-ttu-id="084ad-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="084ad-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="084ad-111">*ppEnum* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="084ad-111">*ppEnum* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="084ad-112">Puntatore alla nuova interfaccia [**IEnumParticipant**](ienumparticipant.md) .</span><span class="sxs-lookup"><span data-stu-id="084ad-112">Pointer to new [**IEnumParticipant**](ienumparticipant.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="084ad-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="084ad-113">Return value</span></span>

<span data-ttu-id="084ad-114">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="084ad-114">This method can return one of these values.</span></span>



| <span data-ttu-id="084ad-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="084ad-115">Return code</span></span>                                                                                   | <span data-ttu-id="084ad-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="084ad-116">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="084ad-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="084ad-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="084ad-118">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="084ad-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="084ad-119"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="084ad-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="084ad-120">Il parametro *ppEnum* non è un puntatore valido.</span><span class="sxs-lookup"><span data-stu-id="084ad-120">The *ppEnum* parameter is not a valid pointer.</span></span><br/>       |
| <dl> <span data-ttu-id="084ad-121"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="084ad-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="084ad-122">La memoria disponibile non è sufficiente per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="084ad-122">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="084ad-123"><dt>**E \_ imprevisto**</dt></span><span class="sxs-lookup"><span data-stu-id="084ad-123"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>  | <span data-ttu-id="084ad-124">Operazione non riuscita per motivi sconosciuti.</span><span class="sxs-lookup"><span data-stu-id="084ad-124">Failed for unknown reasons.</span></span><br/>                          |



 

## <a name="remarks"></a><span data-ttu-id="084ad-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="084ad-125">Remarks</span></span>

<span data-ttu-id="084ad-126">TAPI chiama il metodo [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) sull'interfaccia [**IEnumParticipant**](ienumparticipant.md) restituita da **IEnumParticipant:: Clone**.</span><span class="sxs-lookup"><span data-stu-id="084ad-126">TAPI calls the [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) method on the [**IEnumParticipant**](ienumparticipant.md) interface returned by **IEnumParticipant::Clone**.</span></span> <span data-ttu-id="084ad-127">L'applicazione deve chiamare [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) sull'interfaccia **IEnumParticipant** per liberare risorse associate.</span><span class="sxs-lookup"><span data-stu-id="084ad-127">The application must call [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) on the **IEnumParticipant** interface to free resources associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="084ad-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="084ad-128">Requirements</span></span>



| <span data-ttu-id="084ad-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="084ad-129">Requirement</span></span> | <span data-ttu-id="084ad-130">Valore</span><span class="sxs-lookup"><span data-stu-id="084ad-130">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="084ad-131">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="084ad-131">TAPI version</span></span><br/> | <span data-ttu-id="084ad-132">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="084ad-132">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="084ad-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="084ad-133">Header</span></span><br/>       | <dl> <span data-ttu-id="084ad-134"><dt>Confpriv. h</dt></span><span class="sxs-lookup"><span data-stu-id="084ad-134"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="084ad-135">Libreria</span><span class="sxs-lookup"><span data-stu-id="084ad-135">Library</span></span><br/>      | <dl> <span data-ttu-id="084ad-136"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="084ad-136"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="084ad-137">DLL</span><span class="sxs-lookup"><span data-stu-id="084ad-137">DLL</span></span><br/>          | <dl> <span data-ttu-id="084ad-138"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="084ad-138"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="084ad-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="084ad-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="084ad-140">**IEnumParticipant**</span><span class="sxs-lookup"><span data-stu-id="084ad-140">**IEnumParticipant**</span></span>](ienumparticipant.md)
</dt> <dt>

[<span data-ttu-id="084ad-141">**ITParticipant**</span><span class="sxs-lookup"><span data-stu-id="084ad-141">**ITParticipant**</span></span>](itparticipant.md)
</dt> </dl>

 

