---
description: Il \_ metodo Get ParticipantTypedInfo ottiene una rappresentazione BSTR del tipo di informazioni necessarie, ad esempio PTI \_ EMAILADDRESS.
ms.assetid: 8dcc6182-ad3c-47f2-b4a0-e18a3c9f6888
title: 'Metodo ITParticipant:: get_ParticipantTypedInfo (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c9936f49e6daa05702699487e4313a918c545a7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325595"
---
# <a name="itparticipantget_participanttypedinfo-method"></a><span data-ttu-id="53a4d-103">Metodo ITParticipant:: Get \_ ParticipantTypedInfo</span><span class="sxs-lookup"><span data-stu-id="53a4d-103">ITParticipant::get\_ParticipantTypedInfo method</span></span>

<span data-ttu-id="53a4d-104">\[**ottenere \_ ParticipantTypedInfo** non è disponibile per l'utilizzo in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="53a4d-104">\[**get\_ParticipantTypedInfo** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="53a4d-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="53a4d-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="53a4d-106">Il metodo **get \_ ParticipantTypedInfo** ottiene una rappresentazione **BSTR** del tipo di informazioni necessarie, ad esempio PTI \_ EMAILADDRESS.</span><span class="sxs-lookup"><span data-stu-id="53a4d-106">The **get\_ParticipantTypedInfo** method gets a **BSTR** representation of the type of information needed, such as PTI\_EMAILADDRESS.</span></span>

## <a name="syntax"></a><span data-ttu-id="53a4d-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="53a4d-107">Syntax</span></span>


```C++
HRESULT get_ParticipantTypedInfo(
  [in]  PARTICIPANT_TYPED_INFO InfoType,
  [out] BSTR                   *ppInfo
);
```



## <a name="parameters"></a><span data-ttu-id="53a4d-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="53a4d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53a4d-109">*InfoType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="53a4d-109">*InfoType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53a4d-110">[**Partecipante \_ Descrittore di \_ informazioni tipizzato**](participant-typed-info.md) del tipo di informazioni necessarie.</span><span class="sxs-lookup"><span data-stu-id="53a4d-110">[**PARTICIPANT\_TYPED\_INFO**](participant-typed-info.md) descriptor of the type of information needed.</span></span>

</dd> <dt>

<span data-ttu-id="53a4d-111">*ppInfo* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="53a4d-111">*ppInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="53a4d-112">Puntatore alla rappresentazione **BSTR** delle informazioni necessarie.</span><span class="sxs-lookup"><span data-stu-id="53a4d-112">Pointer to **BSTR** representation of the information needed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53a4d-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="53a4d-113">Return value</span></span>

<span data-ttu-id="53a4d-114">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="53a4d-114">This method can return one of these values.</span></span>



| <span data-ttu-id="53a4d-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="53a4d-115">Return code</span></span>                                                                                    | <span data-ttu-id="53a4d-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="53a4d-116">Description</span></span>                                                     |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="53a4d-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="53a4d-117"><dt>**S\_OK**</dt></span></span> </dl>           | <span data-ttu-id="53a4d-118">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="53a4d-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="53a4d-119"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="53a4d-119"><dt>**E\_FAIL**</dt></span></span> </dl>         | <span data-ttu-id="53a4d-120">L'archiviazione delle informazioni in *ppInfo* non è riuscita.</span><span class="sxs-lookup"><span data-stu-id="53a4d-120">Storage of information into *ppInfo* failed.</span></span><br/>         |
| <dl> <span data-ttu-id="53a4d-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="53a4d-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>   | <span data-ttu-id="53a4d-122">Il parametro *InfoType* non è valido.</span><span class="sxs-lookup"><span data-stu-id="53a4d-122">The *InfoType* parameter is not valid.</span></span><br/>               |
| <dl> <span data-ttu-id="53a4d-123"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="53a4d-123"><dt>**E\_POINTER**</dt></span></span> </dl>      | <span data-ttu-id="53a4d-124">Il parametro *ppInfo* non è un puntatore valido.</span><span class="sxs-lookup"><span data-stu-id="53a4d-124">The *ppInfo* parameter is not a valid pointer.</span></span><br/>       |
| <dl> <span data-ttu-id="53a4d-125"><dt>**TAPI \_ E \_ noitem**</dt></span><span class="sxs-lookup"><span data-stu-id="53a4d-125"><dt>**TAPI\_E\_NOITEM**</dt></span></span> </dl> | <span data-ttu-id="53a4d-126">TAPI non contiene informazioni sul tipo specificato.</span><span class="sxs-lookup"><span data-stu-id="53a4d-126">TAPI has no information on the specified type.</span></span><br/>       |
| <dl> <span data-ttu-id="53a4d-127"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="53a4d-127"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>  | <span data-ttu-id="53a4d-128">La memoria disponibile non è sufficiente per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="53a4d-128">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="53a4d-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="53a4d-129">Remarks</span></span>

<span data-ttu-id="53a4d-130">L'applicazione deve usare [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) per liberare la memoria allocata per il parametro *ppInfo* .</span><span class="sxs-lookup"><span data-stu-id="53a4d-130">The application must use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory allocated for the *ppInfo* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="53a4d-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="53a4d-131">Requirements</span></span>



| <span data-ttu-id="53a4d-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="53a4d-132">Requirement</span></span> | <span data-ttu-id="53a4d-133">Valore</span><span class="sxs-lookup"><span data-stu-id="53a4d-133">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="53a4d-134">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="53a4d-134">TAPI version</span></span><br/> | <span data-ttu-id="53a4d-135">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="53a4d-135">Requires TAPI 3.0 or later</span></span><br/>                                                |
| <span data-ttu-id="53a4d-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="53a4d-136">Header</span></span><br/>       | <dl> <span data-ttu-id="53a4d-137"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="53a4d-137"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="53a4d-138">Libreria</span><span class="sxs-lookup"><span data-stu-id="53a4d-138">Library</span></span><br/>      | <dl> <span data-ttu-id="53a4d-139"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="53a4d-139"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="53a4d-140">DLL</span><span class="sxs-lookup"><span data-stu-id="53a4d-140">DLL</span></span><br/>          | <dl> <span data-ttu-id="53a4d-141"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="53a4d-141"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53a4d-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="53a4d-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53a4d-143">**ITParticipant**</span><span class="sxs-lookup"><span data-stu-id="53a4d-143">**ITParticipant**</span></span>](itparticipant.md)
</dt> <dt>

[<span data-ttu-id="53a4d-144">**\_informazioni digitate del partecipante \_**</span><span class="sxs-lookup"><span data-stu-id="53a4d-144">**PARTICIPANT\_TYPED\_INFO**</span></span>](participant-typed-info.md)
</dt> <dt>

[<span data-ttu-id="53a4d-145">**tipi di supporto**</span><span class="sxs-lookup"><span data-stu-id="53a4d-145">**media types**</span></span>](tapimediatype--constants.md)
</dt> </dl>

 

