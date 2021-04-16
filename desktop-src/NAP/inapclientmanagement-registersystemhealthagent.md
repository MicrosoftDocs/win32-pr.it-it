---
title: Metodo INapClientManagement RegisterSystemHealthAgent (NapManagement. h)
description: Registra un SHA con il sistema NAP.
ms.assetid: 37acfd11-8282-42ba-ae02-9a45c4509b8b
keywords:
- NAP metodo RegisterSystemHealthAgent
- Metodo RegisterSystemHealthAgent NAP, interfaccia INapClientManagement
- Interfaccia INapClientManagement NAP, metodo RegisterSystemHealthAgent
topic_type:
- apiref
api_name:
- INapClientManagement.RegisterSystemHealthAgent
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 581c49a117a2b8aaa2c4dda2c6573e4a6327b688
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477818"
---
# <a name="inapclientmanagementregistersystemhealthagent-method"></a><span data-ttu-id="9a3da-106">Metodo INapClientManagement:: RegisterSystemHealthAgent</span><span class="sxs-lookup"><span data-stu-id="9a3da-106">INapClientManagement::RegisterSystemHealthAgent method</span></span>

> [!Note]  
> <span data-ttu-id="9a3da-107">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="9a3da-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="9a3da-108">Il metodo **RegisterSystemHealthAgent** registra un Sha con il sistema NAP.</span><span class="sxs-lookup"><span data-stu-id="9a3da-108">The **RegisterSystemHealthAgent** method registers an SHA with the NAP system.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a3da-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9a3da-109">Syntax</span></span>


```C++
HRESULT RegisterSystemHealthAgent(
  [in] const NapComponentRegistrationInfo *agent
);
```



## <a name="parameters"></a><span data-ttu-id="9a3da-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="9a3da-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a3da-111">*agente* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="9a3da-111">*agent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a3da-112">Puntatore a una struttura [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) che contiene le informazioni di registrazione per l'SHA.</span><span class="sxs-lookup"><span data-stu-id="9a3da-112">A pointer to a [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) structure that contains the registration information for the SHA.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a3da-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9a3da-113">Return value</span></span>

<span data-ttu-id="9a3da-114">Il metodo restituisce un codice di stato HRESULT incluso ma non limitato a uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="9a3da-114">The method returns an HRESULT status code including but not limited to one of the following.</span></span>



| <span data-ttu-id="9a3da-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="9a3da-115">Return code</span></span>                                                                                            | <span data-ttu-id="9a3da-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9a3da-116">Description</span></span>                                                        |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="9a3da-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="9a3da-117"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="9a3da-118">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="9a3da-118">Operation successful.</span></span><br/>                                   |
| <dl> <span data-ttu-id="9a3da-119"><dt>**E \_ AccessDenied**</dt></span><span class="sxs-lookup"><span data-stu-id="9a3da-119"><dt>**E\_ACCESSDENIED**</dt></span></span> </dl>         | <span data-ttu-id="9a3da-120">Errore delle autorizzazioni, accesso negato.</span><span class="sxs-lookup"><span data-stu-id="9a3da-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="9a3da-121"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="9a3da-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>          | <span data-ttu-id="9a3da-122">Limite di risorse di sistema. Impossibile eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="9a3da-122">System resource limit, could not perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="9a3da-123"><dt>**protezione accesso alla rete \_ E \_ ID in conflitto \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9a3da-123"><dt>**NAP\_E\_CONFLICTING\_ID**</dt></span></span> </dl> | <span data-ttu-id="9a3da-124">Un SHA che usa questo ID è già registrato.</span><span class="sxs-lookup"><span data-stu-id="9a3da-124">An SHA that uses this ID is already registered.</span></span><br/>         |



 

## <a name="requirements"></a><span data-ttu-id="9a3da-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9a3da-125">Requirements</span></span>



| <span data-ttu-id="9a3da-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="9a3da-126">Requirement</span></span> | <span data-ttu-id="9a3da-127">Valore</span><span class="sxs-lookup"><span data-stu-id="9a3da-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a3da-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9a3da-128">Minimum supported client</span></span><br/> | <span data-ttu-id="9a3da-129">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9a3da-129">Windows Vista \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="9a3da-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9a3da-130">Minimum supported server</span></span><br/> | <span data-ttu-id="9a3da-131">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9a3da-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="9a3da-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9a3da-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="9a3da-133"><dt>NapManagement. h</dt></span><span class="sxs-lookup"><span data-stu-id="9a3da-133"><dt>NapManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="9a3da-134">IDL</span><span class="sxs-lookup"><span data-stu-id="9a3da-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9a3da-135"><dt>NapManagement. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9a3da-135"><dt>NapManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="9a3da-136">DLL</span><span class="sxs-lookup"><span data-stu-id="9a3da-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9a3da-137"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9a3da-137"><dt>Qagent.dll</dt></span></span> </dl>        |



## <a name="see-also"></a><span data-ttu-id="9a3da-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9a3da-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a3da-139">**INapClientManagement**</span><span class="sxs-lookup"><span data-stu-id="9a3da-139">**INapClientManagement**</span></span>](inapclientmanagement.md)
</dt> </dl>

 

 





