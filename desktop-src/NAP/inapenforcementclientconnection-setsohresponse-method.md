---
title: Metodo INapEnforcementClientConnection SetSoHResponse (NapEnforcementClient. h)
description: Imposta il SoH-Response e viene utilizzato dal client di imposizione per la ricezione di un pacchetto.
ms.assetid: 718669c7-73cf-44f4-8463-c59fdbe215cc
keywords:
- NAP metodo SetSoHResponse
- Metodo SetSoHResponse NAP, interfaccia INapEnforcementClientConnection
- Interfaccia INapEnforcementClientConnection NAP, metodo SetSoHResponse
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.SetSoHResponse
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0fdc403a1ff68e28f7d262e64ebe558226741b22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478034"
---
# <a name="inapenforcementclientconnectionsetsohresponse-method"></a><span data-ttu-id="5018d-106">Metodo INapEnforcementClientConnection:: SetSoHResponse</span><span class="sxs-lookup"><span data-stu-id="5018d-106">INapEnforcementClientConnection::SetSoHResponse method</span></span>

> [!Note]  
> <span data-ttu-id="5018d-107">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="5018d-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="5018d-108">Il metodo **INapEnforcementClientConnection:: SetSoHResponse** imposta il SoH-Response e viene utilizzato dal client di imposizione per la ricezione di un pacchetto.</span><span class="sxs-lookup"><span data-stu-id="5018d-108">The **INapEnforcementClientConnection::SetSoHResponse** method sets the SoH-Response and is used by the enforcement client on receiving a packet.</span></span>

## <a name="syntax"></a><span data-ttu-id="5018d-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5018d-109">Syntax</span></span>


```C++
HRESULT SetSoHResponse(
  [in] const NetworkSoHResponse *sohResponse
);
```



## <a name="parameters"></a><span data-ttu-id="5018d-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="5018d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5018d-111">*sohResponse* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5018d-111">*sohResponse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5018d-112">Puntatore a una struttura [**NetworkSoHResponse**](/windows/win32/api/naptypes/ns-naptypes-networksoh) univoca, ovvero un BLOB di dati opachi per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="5018d-112">A pointer to a unique [**NetworkSoHResponse**](/windows/win32/api/naptypes/ns-naptypes-networksoh) structure, which is an opaque data blob to the enforcer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5018d-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5018d-113">Return value</span></span>

<span data-ttu-id="5018d-114">È possibile che vengano restituiti anche altri codici di errore specifici di COM.</span><span class="sxs-lookup"><span data-stu-id="5018d-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="5018d-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="5018d-115">Return code</span></span>                                                                                     | <span data-ttu-id="5018d-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5018d-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="5018d-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="5018d-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="5018d-118">Il pacchetto del rapporto di integrità è valido.</span><span class="sxs-lookup"><span data-stu-id="5018d-118">The SoH packet is valid.</span></span><br/>                                |
| <dl> <span data-ttu-id="5018d-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="5018d-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="5018d-120">Errore delle autorizzazioni, accesso negato.</span><span class="sxs-lookup"><span data-stu-id="5018d-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="5018d-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="5018d-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="5018d-122">Limite di risorse di sistema. Impossibile eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="5018d-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5018d-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="5018d-123">Remarks</span></span>

<span data-ttu-id="5018d-124">Un pacchetto di dimensioni pari A zero è valido.</span><span class="sxs-lookup"><span data-stu-id="5018d-124">A zero-sized packet is valid.</span></span>

## <a name="requirements"></a><span data-ttu-id="5018d-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5018d-125">Requirements</span></span>



| <span data-ttu-id="5018d-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="5018d-126">Requirement</span></span> | <span data-ttu-id="5018d-127">Valore</span><span class="sxs-lookup"><span data-stu-id="5018d-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5018d-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5018d-128">Minimum supported client</span></span><br/> | <span data-ttu-id="5018d-129">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5018d-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="5018d-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5018d-130">Minimum supported server</span></span><br/> | <span data-ttu-id="5018d-131">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5018d-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="5018d-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5018d-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="5018d-133"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="5018d-133"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="5018d-134">IDL</span><span class="sxs-lookup"><span data-stu-id="5018d-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5018d-135"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5018d-135"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="5018d-136">DLL</span><span class="sxs-lookup"><span data-stu-id="5018d-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5018d-137"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5018d-137"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="5018d-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5018d-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5018d-139">**INapEnforcementClientConnection**</span><span class="sxs-lookup"><span data-stu-id="5018d-139">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





