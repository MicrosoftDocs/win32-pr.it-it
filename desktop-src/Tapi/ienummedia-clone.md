---
description: Il metodo Clone crea un altro enumeratore che contiene lo stesso stato di enumerazione di quello corrente.
ms.assetid: b48399f5-daaa-40e4-bd80-a918539d25c6
title: 'Metodo IEnumMedia:: Clone (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c29671819db202643506cbdf90a1550abb305718
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333149"
---
# <a name="ienummediaclone-method"></a><span data-ttu-id="574d3-103">Metodo IEnumMedia:: Clone</span><span class="sxs-lookup"><span data-stu-id="574d3-103">IEnumMedia::Clone method</span></span>

<span data-ttu-id="574d3-104">\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="574d3-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="574d3-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="574d3-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="574d3-106">Il metodo **Clone** crea un altro enumeratore che contiene lo stesso stato di enumerazione di quello corrente.</span><span class="sxs-lookup"><span data-stu-id="574d3-106">The **Clone** method creates another enumerator that contains the same enumeration state as the current one.</span></span>

## <a name="syntax"></a><span data-ttu-id="574d3-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="574d3-107">Syntax</span></span>


```C++
HRESULT Clone(
  [out] IEnumMedia **ppEnum
);
```



## <a name="parameters"></a><span data-ttu-id="574d3-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="574d3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="574d3-109">*ppEnum* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="574d3-109">*ppEnum* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="574d3-110">Puntatore al nuovo oggetto [**IEnumMedia**](ienummedia.md) .</span><span class="sxs-lookup"><span data-stu-id="574d3-110">Pointer to the new [**IEnumMedia**](ienummedia.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="574d3-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="574d3-111">Return value</span></span>

<span data-ttu-id="574d3-112">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="574d3-112">This method can return one of these values.</span></span>



| <span data-ttu-id="574d3-113">Valore</span><span class="sxs-lookup"><span data-stu-id="574d3-113">Value</span></span>                                                                                         | <span data-ttu-id="574d3-114">Significato</span><span class="sxs-lookup"><span data-stu-id="574d3-114">Meaning</span></span>                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="574d3-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="574d3-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="574d3-116">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="574d3-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="574d3-117"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="574d3-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="574d3-118">Il parametro *ppEnum* non è un puntatore valido.</span><span class="sxs-lookup"><span data-stu-id="574d3-118">The *ppEnum* parameter is not a valid pointer.</span></span><br/>       |
| <dl> <span data-ttu-id="574d3-119"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="574d3-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="574d3-120">La memoria disponibile non è sufficiente per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="574d3-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="574d3-121"><dt>**E \_ imprevisto**</dt></span><span class="sxs-lookup"><span data-stu-id="574d3-121"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>  | <span data-ttu-id="574d3-122">Operazione non riuscita per motivi sconosciuti.</span><span class="sxs-lookup"><span data-stu-id="574d3-122">Failed for unknown reasons.</span></span><br/>                          |



 

## <a name="remarks"></a><span data-ttu-id="574d3-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="574d3-123">Remarks</span></span>

<span data-ttu-id="574d3-124">TAPI chiama il metodo **AddRef** sull'interfaccia [**IEnumMedia**](ienummedia.md) restituita da **IEnumMedia:: Clone**.</span><span class="sxs-lookup"><span data-stu-id="574d3-124">TAPI calls the **AddRef** method on the [**IEnumMedia**](ienummedia.md) interface returned by **IEnumMedia::Clone**.</span></span> <span data-ttu-id="574d3-125">L'applicazione deve chiamare **Release** sull'interfaccia **IEnumMedia** per liberare risorse associate.</span><span class="sxs-lookup"><span data-stu-id="574d3-125">The application must call **Release** on the **IEnumMedia** interface to free resources associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="574d3-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="574d3-126">Requirements</span></span>



| <span data-ttu-id="574d3-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="574d3-127">Requirement</span></span> | <span data-ttu-id="574d3-128">Valore</span><span class="sxs-lookup"><span data-stu-id="574d3-128">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="574d3-129">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="574d3-129">TAPI version</span></span><br/> | <span data-ttu-id="574d3-130">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="574d3-130">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="574d3-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="574d3-131">Header</span></span><br/>       | <dl> <span data-ttu-id="574d3-132"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="574d3-132"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="574d3-133">Libreria</span><span class="sxs-lookup"><span data-stu-id="574d3-133">Library</span></span><br/>      | <dl> <span data-ttu-id="574d3-134"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="574d3-134"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="574d3-135">DLL</span><span class="sxs-lookup"><span data-stu-id="574d3-135">DLL</span></span><br/>          | <dl> <span data-ttu-id="574d3-136"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="574d3-136"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="574d3-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="574d3-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="574d3-138">**IEnumMedia**</span><span class="sxs-lookup"><span data-stu-id="574d3-138">**IEnumMedia**</span></span>](ienummedia.md)
</dt> </dl>

 

 




