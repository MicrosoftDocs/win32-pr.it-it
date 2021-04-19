---
description: Il metodo Clone crea un altro enumeratore che contiene lo stesso stato di enumerazione di quello corrente.
ms.assetid: 0e9973de-d179-4a2d-a9bd-6d5f2523da52
title: 'Metodo IEnumTime:: Clone (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a030fcd90006047e35d9f661f2878dfbc42c112
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332256"
---
# <a name="ienumtimeclone-method"></a><span data-ttu-id="bcb4b-103">Metodo IEnumTime:: Clone</span><span class="sxs-lookup"><span data-stu-id="bcb4b-103">IEnumTime::Clone method</span></span>

<span data-ttu-id="bcb4b-104">\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="bcb4b-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="bcb4b-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="bcb4b-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="bcb4b-106">Il metodo **Clone** crea un altro enumeratore che contiene lo stesso stato di enumerazione di quello corrente.</span><span class="sxs-lookup"><span data-stu-id="bcb4b-106">The **Clone** method creates another enumerator that contains the same enumeration state as the current one.</span></span>

## <a name="syntax"></a><span data-ttu-id="bcb4b-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bcb4b-107">Syntax</span></span>


```C++
HRESULT Clone(
  [out] IEnumTime **ppEnum
);
```



## <a name="parameters"></a><span data-ttu-id="bcb4b-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="bcb4b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bcb4b-109">*ppEnum* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="bcb4b-109">*ppEnum* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bcb4b-110">Puntatore al nuovo oggetto [**IEnumTime**](ienumtime.md) .</span><span class="sxs-lookup"><span data-stu-id="bcb4b-110">Pointer to the new [**IEnumTime**](ienumtime.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bcb4b-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bcb4b-111">Return value</span></span>

<span data-ttu-id="bcb4b-112">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="bcb4b-112">This method can return one of these values.</span></span>



| <span data-ttu-id="bcb4b-113">Valore</span><span class="sxs-lookup"><span data-stu-id="bcb4b-113">Value</span></span>                                                                                         | <span data-ttu-id="bcb4b-114">Significato</span><span class="sxs-lookup"><span data-stu-id="bcb4b-114">Meaning</span></span>                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="bcb4b-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="bcb4b-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="bcb4b-116">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="bcb4b-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="bcb4b-117"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="bcb4b-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="bcb4b-118">Il parametro *ppEnum* non è un puntatore valido.</span><span class="sxs-lookup"><span data-stu-id="bcb4b-118">The *ppEnum* parameter is not a valid pointer.</span></span><br/>       |
| <dl> <span data-ttu-id="bcb4b-119"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="bcb4b-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="bcb4b-120">La memoria disponibile non è sufficiente per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="bcb4b-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="bcb4b-121"><dt>**E \_ imprevisto**</dt></span><span class="sxs-lookup"><span data-stu-id="bcb4b-121"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>  | <span data-ttu-id="bcb4b-122">Operazione non riuscita per motivi sconosciuti.</span><span class="sxs-lookup"><span data-stu-id="bcb4b-122">Failed for unknown reasons.</span></span><br/>                          |



 

## <a name="remarks"></a><span data-ttu-id="bcb4b-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="bcb4b-123">Remarks</span></span>

<span data-ttu-id="bcb4b-124">TAPI chiama il metodo **AddRef** sull'interfaccia [**IEnumTime**](ienumtime.md) restituita da **IEnumTime:: Clone**.</span><span class="sxs-lookup"><span data-stu-id="bcb4b-124">TAPI calls the **AddRef** method on the [**IEnumTime**](ienumtime.md) interface returned by **IEnumTime::Clone**.</span></span> <span data-ttu-id="bcb4b-125">L'applicazione deve chiamare **Release** sull'interfaccia **IEnumTime** per liberare risorse associate.</span><span class="sxs-lookup"><span data-stu-id="bcb4b-125">The application must call **Release** on the **IEnumTime** interface to free resources associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="bcb4b-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bcb4b-126">Requirements</span></span>



| <span data-ttu-id="bcb4b-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="bcb4b-127">Requirement</span></span> | <span data-ttu-id="bcb4b-128">Valore</span><span class="sxs-lookup"><span data-stu-id="bcb4b-128">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bcb4b-129">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="bcb4b-129">TAPI version</span></span><br/> | <span data-ttu-id="bcb4b-130">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="bcb4b-130">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="bcb4b-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bcb4b-131">Header</span></span><br/>       | <dl> <span data-ttu-id="bcb4b-132"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="bcb4b-132"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="bcb4b-133">Libreria</span><span class="sxs-lookup"><span data-stu-id="bcb4b-133">Library</span></span><br/>      | <dl> <span data-ttu-id="bcb4b-134"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bcb4b-134"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="bcb4b-135">DLL</span><span class="sxs-lookup"><span data-stu-id="bcb4b-135">DLL</span></span><br/>          | <dl> <span data-ttu-id="bcb4b-136"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bcb4b-136"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bcb4b-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bcb4b-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bcb4b-138">**IEnumTime**</span><span class="sxs-lookup"><span data-stu-id="bcb4b-138">**IEnumTime**</span></span>](ienumtime.md)
</dt> </dl>

 

 




