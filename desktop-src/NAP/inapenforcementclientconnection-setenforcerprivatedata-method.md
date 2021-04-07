---
title: Metodo INapEnforcementClientConnection SetEnforcerPrivateData (NapEnforcementClient. h)
description: Viene usato dall'applicazione per impostare i dati privati.
ms.assetid: 56f6fec7-47ec-4b2c-b8c8-a4d519ba0f91
keywords:
- NAP metodo SetEnforcerPrivateData
- Metodo SetEnforcerPrivateData NAP, interfaccia INapEnforcementClientConnection
- Interfaccia INapEnforcementClientConnection NAP, metodo SetEnforcerPrivateData
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.SetEnforcerPrivateData
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef5773294e229a59ff07db8ef546d9d691b369b2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048158"
---
# <a name="inapenforcementclientconnectionsetenforcerprivatedata-method"></a><span data-ttu-id="79829-106">Metodo INapEnforcementClientConnection:: SetEnforcerPrivateData</span><span class="sxs-lookup"><span data-stu-id="79829-106">INapEnforcementClientConnection::SetEnforcerPrivateData method</span></span>

> [!Note]  
> <span data-ttu-id="79829-107">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="79829-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="79829-108">Il metodo **INapEnforcementClientConnection:: SetEnforcerPrivateData** viene usato dall'applicazione per impostare i dati privati.</span><span class="sxs-lookup"><span data-stu-id="79829-108">The **INapEnforcementClientConnection::SetEnforcerPrivateData** method is used by the enforcer to set private data.</span></span>

## <a name="syntax"></a><span data-ttu-id="79829-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="79829-109">Syntax</span></span>


```C++
HRESULT SetEnforcerPrivateData(
  [in] const PrivateData *privateData
);
```



## <a name="parameters"></a><span data-ttu-id="79829-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="79829-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79829-111">*PrivateData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="79829-111">*privateData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79829-112">Puntatore a un BLOB di dati opachi [**PrivateData**](/windows/win32/api/naptypes/ns-naptypes-privatedata) che può essere interpretato solo dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="79829-112">A pointer to a [**PrivateData**](/windows/win32/api/naptypes/ns-naptypes-privatedata) opaque data blob that only the enforcer can interpret.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79829-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="79829-113">Return value</span></span>

<span data-ttu-id="79829-114">È possibile che vengano restituiti anche altri codici di errore specifici di COM.</span><span class="sxs-lookup"><span data-stu-id="79829-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="79829-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="79829-115">Return code</span></span>                                                                                     | <span data-ttu-id="79829-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="79829-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="79829-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="79829-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="79829-118">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="79829-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="79829-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="79829-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="79829-120">Errore delle autorizzazioni, accesso negato.</span><span class="sxs-lookup"><span data-stu-id="79829-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="79829-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="79829-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="79829-122">Limite di risorse di sistema. Impossibile eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="79829-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="79829-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="79829-123">Requirements</span></span>



| <span data-ttu-id="79829-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="79829-124">Requirement</span></span> | <span data-ttu-id="79829-125">Valore</span><span class="sxs-lookup"><span data-stu-id="79829-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="79829-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="79829-126">Minimum supported client</span></span><br/> | <span data-ttu-id="79829-127">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="79829-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="79829-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="79829-128">Minimum supported server</span></span><br/> | <span data-ttu-id="79829-129">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="79829-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="79829-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="79829-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="79829-131"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="79829-131"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="79829-132">IDL</span><span class="sxs-lookup"><span data-stu-id="79829-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="79829-133"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="79829-133"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="79829-134">DLL</span><span class="sxs-lookup"><span data-stu-id="79829-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="79829-135"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="79829-135"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="79829-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="79829-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79829-137">**INapEnforcementClientConnection**</span><span class="sxs-lookup"><span data-stu-id="79829-137">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





