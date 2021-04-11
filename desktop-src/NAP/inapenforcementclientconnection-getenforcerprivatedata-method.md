---
title: Metodo INapEnforcementClientConnection GetEnforcerPrivateData (NapEnforcementClient. h)
description: Viene usato dall'applicazione per ottenere i dati privati.
ms.assetid: a1f5b5a7-c862-4e5b-bf9c-b137f99f6165
keywords:
- NAP metodo GetEnforcerPrivateData
- Metodo GetEnforcerPrivateData NAP, interfaccia INapEnforcementClientConnection
- Interfaccia INapEnforcementClientConnection NAP, metodo GetEnforcerPrivateData
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.GetEnforcerPrivateData
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d592ad0b11abf2b349b0810d67b05f2ee4086060
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121598"
---
# <a name="inapenforcementclientconnectiongetenforcerprivatedata-method"></a><span data-ttu-id="344f7-106">Metodo INapEnforcementClientConnection:: GetEnforcerPrivateData</span><span class="sxs-lookup"><span data-stu-id="344f7-106">INapEnforcementClientConnection::GetEnforcerPrivateData method</span></span>

> [!Note]  
> <span data-ttu-id="344f7-107">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="344f7-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="344f7-108">Il metodo **INapEnforcementClientConnection:: GetEnforcerPrivateData** viene usato dall'applicazione per ottenere i dati privati.</span><span class="sxs-lookup"><span data-stu-id="344f7-108">The **INapEnforcementClientConnection::GetEnforcerPrivateData** method is used by the enforcer to get private data.</span></span>

## <a name="syntax"></a><span data-ttu-id="344f7-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="344f7-109">Syntax</span></span>


```C++
HRESULT GetEnforcerPrivateData(
  [out] PrivateData **privateData
);
```



## <a name="parameters"></a><span data-ttu-id="344f7-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="344f7-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="344f7-111">*PrivateData* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="344f7-111">*privateData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="344f7-112">Puntatore a un puntatore a un BLOB di dati opachi [**PrivateData**](/windows/win32/api/naptypes/ns-naptypes-privatedata) che può essere interpretato solo dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="344f7-112">A pointer to a pointer to a [**PrivateData**](/windows/win32/api/naptypes/ns-naptypes-privatedata) opaque data blob that only the enforcer can interpret.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="344f7-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="344f7-113">Return value</span></span>

<span data-ttu-id="344f7-114">È possibile che vengano restituiti anche altri codici di errore specifici di COM.</span><span class="sxs-lookup"><span data-stu-id="344f7-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="344f7-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="344f7-115">Return code</span></span>                                                                                     | <span data-ttu-id="344f7-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="344f7-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="344f7-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="344f7-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="344f7-118">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="344f7-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="344f7-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="344f7-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="344f7-120">Errore delle autorizzazioni, accesso negato.</span><span class="sxs-lookup"><span data-stu-id="344f7-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="344f7-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="344f7-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="344f7-122">Limite di risorse di sistema. Impossibile eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="344f7-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="344f7-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="344f7-123">Requirements</span></span>



| <span data-ttu-id="344f7-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="344f7-124">Requirement</span></span> | <span data-ttu-id="344f7-125">Valore</span><span class="sxs-lookup"><span data-stu-id="344f7-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="344f7-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="344f7-126">Minimum supported client</span></span><br/> | <span data-ttu-id="344f7-127">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="344f7-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="344f7-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="344f7-128">Minimum supported server</span></span><br/> | <span data-ttu-id="344f7-129">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="344f7-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="344f7-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="344f7-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="344f7-131"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="344f7-131"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="344f7-132">IDL</span><span class="sxs-lookup"><span data-stu-id="344f7-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="344f7-133"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="344f7-133"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="344f7-134">DLL</span><span class="sxs-lookup"><span data-stu-id="344f7-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="344f7-135"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="344f7-135"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="344f7-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="344f7-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="344f7-137">**INapEnforcementClientConnection**</span><span class="sxs-lookup"><span data-stu-id="344f7-137">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





