---
description: Il metodo Add aggiunge l'attributo in corrispondenza dell'indice specificato.
ms.assetid: 5b74c177-bf5c-4547-bebb-034a9a10be13
title: 'Metodo ITAttributeList:: Add (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5504a216549231aca82eac3b3311ae7208eb8432
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333428"
---
# <a name="itattributelistadd-method"></a><span data-ttu-id="88ff4-103">Metodo ITAttributeList:: Add</span><span class="sxs-lookup"><span data-stu-id="88ff4-103">ITAttributeList::Add method</span></span>

<span data-ttu-id="88ff4-104">\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="88ff4-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="88ff4-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="88ff4-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="88ff4-106">Il metodo **Add** aggiunge l'attributo in corrispondenza dell'indice specificato.</span><span class="sxs-lookup"><span data-stu-id="88ff4-106">The **Add** method adds the attribute at the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="88ff4-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="88ff4-107">Syntax</span></span>


```C++
HRESULT Add(
  [in] LONG Index,
  [in] BSTR pAttribute
);
```



## <a name="parameters"></a><span data-ttu-id="88ff4-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="88ff4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88ff4-109">*Indice* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="88ff4-109">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="88ff4-110">Indice dell'attributo da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="88ff4-110">Index of the attribute to add.</span></span>

</dd> <dt>

<span data-ttu-id="88ff4-111">*pAttribute* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="88ff4-111">*pAttribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="88ff4-112">Puntatore a un **BSTR** che contiene il valore dell'attributo da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="88ff4-112">Pointer to a **BSTR** containing the value of the attribute to add.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="88ff4-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="88ff4-113">Return value</span></span>

<span data-ttu-id="88ff4-114">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="88ff4-114">This method can return one of these values.</span></span>



| <span data-ttu-id="88ff4-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="88ff4-115">Return code</span></span>                                                                                   | <span data-ttu-id="88ff4-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="88ff4-116">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="88ff4-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="88ff4-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="88ff4-118">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="88ff4-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="88ff4-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="88ff4-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="88ff4-120">Il parametro *index* o *pAttribute* non è valido.</span><span class="sxs-lookup"><span data-stu-id="88ff4-120">The *Index* or *pAttribute* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="88ff4-121"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="88ff4-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="88ff4-122">La memoria disponibile non è sufficiente per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="88ff4-122">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="88ff4-123"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="88ff4-123"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="88ff4-124">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="88ff4-124">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="88ff4-125"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="88ff4-125"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="88ff4-126">Questo metodo non è ancora implementato.</span><span class="sxs-lookup"><span data-stu-id="88ff4-126">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="88ff4-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="88ff4-127">Remarks</span></span>

<span data-ttu-id="88ff4-128">L'applicazione deve usare [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) per allocare memoria per il parametro *PAttribute* e usare [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) per liberare la memoria quando la variabile non è più necessaria.</span><span class="sxs-lookup"><span data-stu-id="88ff4-128">The application must use [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) to allocate memory for the *pAttribute* parameter and use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory when the variable is no longer needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="88ff4-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="88ff4-129">Requirements</span></span>



| <span data-ttu-id="88ff4-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="88ff4-130">Requirement</span></span> | <span data-ttu-id="88ff4-131">Valore</span><span class="sxs-lookup"><span data-stu-id="88ff4-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="88ff4-132">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="88ff4-132">TAPI version</span></span><br/> | <span data-ttu-id="88ff4-133">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="88ff4-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="88ff4-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="88ff4-134">Header</span></span><br/>       | <dl> <span data-ttu-id="88ff4-135"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="88ff4-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="88ff4-136">Libreria</span><span class="sxs-lookup"><span data-stu-id="88ff4-136">Library</span></span><br/>      | <dl> <span data-ttu-id="88ff4-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="88ff4-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="88ff4-138">DLL</span><span class="sxs-lookup"><span data-stu-id="88ff4-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="88ff4-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="88ff4-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88ff4-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="88ff4-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88ff4-141">**ITAttributeList**</span><span class="sxs-lookup"><span data-stu-id="88ff4-141">**ITAttributeList**</span></span>](itattributelist.md)
</dt> </dl>

 

