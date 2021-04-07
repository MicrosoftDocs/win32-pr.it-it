---
title: Metodo INapServerInfo GetRegisteredSystemHealthValidators (NapServerManagement. h)
description: Recupera un elenco di SHV registrati.
ms.assetid: 029c7d5c-b397-415c-a530-0096de1ef771
keywords:
- NAP metodo GetRegisteredSystemHealthValidators
- Metodo GetRegisteredSystemHealthValidators NAP, interfaccia INapServerInfo
- Interfaccia INapServerInfo NAP, metodo GetRegisteredSystemHealthValidators
topic_type:
- apiref
api_name:
- INapServerInfo.GetRegisteredSystemHealthValidators
api_location:
- qsvrmgmt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16ffdd4d363c994efbecdb57fe4ad7203393fd1f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048631"
---
# <a name="inapserverinfogetregisteredsystemhealthvalidators-method"></a><span data-ttu-id="7a02b-106">Metodo INapServerInfo:: GetRegisteredSystemHealthValidators</span><span class="sxs-lookup"><span data-stu-id="7a02b-106">INapServerInfo::GetRegisteredSystemHealthValidators method</span></span>

> [!Note]  
> <span data-ttu-id="7a02b-107">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="7a02b-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="7a02b-108">Il metodo **INapServerInfo:: GetRegisteredSystemHealthValidators** recupera un elenco di SHV registrati.</span><span class="sxs-lookup"><span data-stu-id="7a02b-108">The **INapServerInfo::GetRegisteredSystemHealthValidators** method retrieves a list of registered SHVs.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a02b-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7a02b-109">Syntax</span></span>


```C++
HRESULT GetRegisteredSystemHealthValidators(
  [out] SystemHealthEntityCount      *count,
  [out] NapComponentRegistrationInfo **validators,
  [out] CLSID                        **validatorClsids
);
```



## <a name="parameters"></a><span data-ttu-id="7a02b-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="7a02b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a02b-111">*numero* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="7a02b-111">*count* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7a02b-112">Puntatore a un [**SystemHealthEntityCount**](nap-type-constants.md) contenente il numero di SHV registrati.</span><span class="sxs-lookup"><span data-stu-id="7a02b-112">A pointer to a [**SystemHealthEntityCount**](nap-type-constants.md) that contains the number of registered SHVs.</span></span>

</dd> <dt>

<span data-ttu-id="7a02b-113">*validator* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="7a02b-113">*validators* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7a02b-114">Puntatore a un puntatore a una struttura [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) che contiene le informazioni di registrazione di convalida integrità sistema.</span><span class="sxs-lookup"><span data-stu-id="7a02b-114">A pointer to a pointer to a [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) structure that contains the SHV registration information.</span></span>

</dd> <dt>

<span data-ttu-id="7a02b-115">*validatorClsids* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="7a02b-115">*validatorClsids* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7a02b-116">Puntatore a una matrice di ID per il SHV registrato.</span><span class="sxs-lookup"><span data-stu-id="7a02b-116">Pointer to an array of IDs for the registered SHVs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a02b-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7a02b-117">Return value</span></span>

<span data-ttu-id="7a02b-118">È possibile che vengano restituiti anche altri codici di errore specifici di COM.</span><span class="sxs-lookup"><span data-stu-id="7a02b-118">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="7a02b-119">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="7a02b-119">Return code</span></span>                                                                                     | <span data-ttu-id="7a02b-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7a02b-120">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="7a02b-121"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="7a02b-121"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="7a02b-122">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="7a02b-122">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="7a02b-123"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="7a02b-123"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="7a02b-124">Errore delle autorizzazioni, accesso negato.</span><span class="sxs-lookup"><span data-stu-id="7a02b-124">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="7a02b-125"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="7a02b-125"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="7a02b-126">Limite di risorse di sistema. Impossibile eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="7a02b-126">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="7a02b-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7a02b-127">Requirements</span></span>



| <span data-ttu-id="7a02b-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="7a02b-128">Requirement</span></span> | <span data-ttu-id="7a02b-129">Valore</span><span class="sxs-lookup"><span data-stu-id="7a02b-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a02b-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7a02b-130">Minimum supported client</span></span><br/> | <span data-ttu-id="7a02b-131">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="7a02b-131">None supported</span></span><br/>                                                                          |
| <span data-ttu-id="7a02b-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7a02b-132">Minimum supported server</span></span><br/> | <span data-ttu-id="7a02b-133">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7a02b-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="7a02b-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7a02b-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="7a02b-135"><dt>NapServerManagement. h</dt></span><span class="sxs-lookup"><span data-stu-id="7a02b-135"><dt>NapServerManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="7a02b-136">IDL</span><span class="sxs-lookup"><span data-stu-id="7a02b-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7a02b-137"><dt>NapServerManagement. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7a02b-137"><dt>NapServerManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="7a02b-138">DLL</span><span class="sxs-lookup"><span data-stu-id="7a02b-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7a02b-139"><dt>Qsvrmgmt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7a02b-139"><dt>Qsvrmgmt.dll</dt></span></span> </dl>            |



## <a name="see-also"></a><span data-ttu-id="7a02b-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7a02b-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a02b-141">**NapComponentRegistrationInfo**</span><span class="sxs-lookup"><span data-stu-id="7a02b-141">**NapComponentRegistrationInfo**</span></span>](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo)
</dt> <dt>

[<span data-ttu-id="7a02b-142">**INapServerInfo**</span><span class="sxs-lookup"><span data-stu-id="7a02b-142">**INapServerInfo**</span></span>](inapserverinfo.md)
</dt> </dl>

 

 





