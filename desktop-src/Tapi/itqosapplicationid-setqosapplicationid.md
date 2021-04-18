---
description: Il metodo SetQOSApplicationID imposta l'identificatore QOS per l'applicazione.
ms.assetid: e25cf749-6673-47eb-b843-4066f475b8f1
title: 'Metodo ITQOSApplicationID:: SetQOSApplicationID (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7893c8038fd7a47fc1978a20e5aba5cc8293d9a3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333662"
---
# <a name="itqosapplicationidsetqosapplicationid-method"></a><span data-ttu-id="7fc23-103">Metodo ITQOSApplicationID:: SetQOSApplicationID</span><span class="sxs-lookup"><span data-stu-id="7fc23-103">ITQOSApplicationID::SetQOSApplicationID method</span></span>

<span data-ttu-id="7fc23-104">\[ Questo metodo non è disponibile per l'utilizzo in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="7fc23-104">\[ This method is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="7fc23-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="7fc23-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="7fc23-106">Il metodo **SetQOSApplicationID** imposta l'identificatore QoS per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7fc23-106">The **SetQOSApplicationID** method sets the QOS identifier for the application.</span></span>

## <a name="syntax"></a><span data-ttu-id="7fc23-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7fc23-107">Syntax</span></span>


```C++
HRESULT SetQOSApplicationID(
  [in] BSTR pApplicationID,
  [in] BSTR pApplicationGUID,
  [in] BSTR pSubIDs
);
```



## <a name="parameters"></a><span data-ttu-id="7fc23-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="7fc23-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7fc23-109">*pApplicationID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7fc23-109">*pApplicationID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7fc23-110">Identificatore univoco del processo dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7fc23-110">Unique identifier for the application process.</span></span>

</dd> <dt>

<span data-ttu-id="7fc23-111">*pApplicationGUID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7fc23-111">*pApplicationGUID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7fc23-112">GUID dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7fc23-112">Application GUID.</span></span>

</dd> <dt>

<span data-ttu-id="7fc23-113">*pSubIDs* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7fc23-113">*pSubIDs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7fc23-114">Sub-IDs associato alla chiamata corrente.</span><span class="sxs-lookup"><span data-stu-id="7fc23-114">Sub-IDs associated with the current call.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7fc23-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7fc23-115">Return value</span></span>

<span data-ttu-id="7fc23-116">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="7fc23-116">This method can return one of these values.</span></span>



| <span data-ttu-id="7fc23-117">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="7fc23-117">Return code</span></span>                                                                                   | <span data-ttu-id="7fc23-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7fc23-118">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="7fc23-119"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="7fc23-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="7fc23-120">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="7fc23-120">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="7fc23-121"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="7fc23-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="7fc23-122">La memoria disponibile non è sufficiente per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="7fc23-122">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="7fc23-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7fc23-123">Requirements</span></span>



| <span data-ttu-id="7fc23-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="7fc23-124">Requirement</span></span> | <span data-ttu-id="7fc23-125">Valore</span><span class="sxs-lookup"><span data-stu-id="7fc23-125">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="7fc23-126">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="7fc23-126">TAPI version</span></span><br/> | <span data-ttu-id="7fc23-127">Richiede TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="7fc23-127">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="7fc23-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7fc23-128">Header</span></span><br/>       | <dl> <span data-ttu-id="7fc23-129"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="7fc23-129"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="7fc23-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="7fc23-130">Library</span></span><br/>      | <dl> <span data-ttu-id="7fc23-131"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7fc23-131"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="7fc23-132">DLL</span><span class="sxs-lookup"><span data-stu-id="7fc23-132">DLL</span></span><br/>          | <dl> <span data-ttu-id="7fc23-133"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7fc23-133"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7fc23-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7fc23-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7fc23-135">**ITQOSApplicationID**</span><span class="sxs-lookup"><span data-stu-id="7fc23-135">**ITQOSApplicationID**</span></span>](itqosapplicationid.md)
</dt> </dl>

 

 




