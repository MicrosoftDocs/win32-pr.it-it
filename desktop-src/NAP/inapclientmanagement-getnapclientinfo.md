---
title: Metodo INapClientManagement GetNapClientInfo (NapManagement. h)
description: Recupera le informazioni sul client di protezione accesso alla rete.
ms.assetid: c0b57cab-729b-40b2-81d2-32a961e377a5
keywords:
- NAP metodo GetNapClientInfo
- Metodo GetNapClientInfo NAP, interfaccia INapClientManagement
- Interfaccia INapClientManagement NAP, metodo GetNapClientInfo
topic_type:
- apiref
api_name:
- INapClientManagement.GetNapClientInfo
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a11fc496374f2a7f0b7842e22212013149f44f22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518244"
---
# <a name="inapclientmanagementgetnapclientinfo-method"></a><span data-ttu-id="d4d4f-106">Metodo INapClientManagement:: GetNapClientInfo</span><span class="sxs-lookup"><span data-stu-id="d4d4f-106">INapClientManagement::GetNapClientInfo method</span></span>

> [!Note]  
> <span data-ttu-id="d4d4f-107">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="d4d4f-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="d4d4f-108">Il metodo **GetNapClientInfo** recupera le informazioni sul client di protezione accesso alla rete.</span><span class="sxs-lookup"><span data-stu-id="d4d4f-108">The **GetNapClientInfo** method retrieves information about the NAP client.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4d4f-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d4d4f-109">Syntax</span></span>


```C++
HRESULT GetNapClientInfo(
  [out] BOOL          *isNapEnabled,
  [out] CountedString **clientName,
  [out] CountedString **clientDescription,
  [out] CountedString **protocolVersion
) const;
```



## <a name="parameters"></a><span data-ttu-id="d4d4f-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="d4d4f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4d4f-111">*isNapEnabled* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="d4d4f-111">*isNapEnabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d4d4f-112">Puntatore a un BOOL che è impostato su **true** se NAP è abilitato; in caso contrario, è impostato su **false**.</span><span class="sxs-lookup"><span data-stu-id="d4d4f-112">A pointer to a BOOL that is set to **TRUE** if NAP is enabled; otherwise it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="d4d4f-113">*clientname* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="d4d4f-113">*clientName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d4d4f-114">Puntatore a un puntatore a una struttura [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) contenente il nome del client.</span><span class="sxs-lookup"><span data-stu-id="d4d4f-114">A pointer to a pointer to a [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) structure that contains the client name.</span></span>

</dd> <dt>

<span data-ttu-id="d4d4f-115">*clientDescription* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="d4d4f-115">*clientDescription* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d4d4f-116">Puntatore a un puntatore a una struttura [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) contenente la descrizione del client.</span><span class="sxs-lookup"><span data-stu-id="d4d4f-116">A pointer to a pointer to a [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) structure that contains the client description.</span></span>

</dd> <dt>

<span data-ttu-id="d4d4f-117">*protocolVersion* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="d4d4f-117">*protocolVersion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d4d4f-118">Puntatore a un puntatore a una struttura [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) contenente la versione del protocollo.</span><span class="sxs-lookup"><span data-stu-id="d4d4f-118">A pointer to a pointer to a [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) structure that contains the protocol version.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4d4f-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d4d4f-119">Return value</span></span>

<span data-ttu-id="d4d4f-120">Il metodo restituisce un codice di stato HRESULT incluso ma non limitato a uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="d4d4f-120">The method returns an HRESULT status code including but not limited to one of the following.</span></span>



| <span data-ttu-id="d4d4f-121">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="d4d4f-121">Return code</span></span>                                                                                         | <span data-ttu-id="d4d4f-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d4d4f-122">Description</span></span>                                                        |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="d4d4f-123"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d4d4f-123"><dt>**S\_OK**</dt></span></span> </dl>                | <span data-ttu-id="d4d4f-124">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="d4d4f-124">Operation successful.</span></span><br/>                                   |
| <dl> <span data-ttu-id="d4d4f-125"><dt>**E \_ AccessDenied**</dt></span><span class="sxs-lookup"><span data-stu-id="d4d4f-125"><dt>**E\_ACCESSDENIED**</dt></span></span> </dl>      | <span data-ttu-id="d4d4f-126">Errore delle autorizzazioni, accesso negato.</span><span class="sxs-lookup"><span data-stu-id="d4d4f-126">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="d4d4f-127"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="d4d4f-127"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>       | <span data-ttu-id="d4d4f-128">Limite di risorse di sistema. Impossibile eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="d4d4f-128">System resource limit, could not perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="d4d4f-129"><dt>**RPC \_ E \_ disconnessa**</dt></span><span class="sxs-lookup"><span data-stu-id="d4d4f-129"><dt>**RPC\_E\_DISCONNECTED**</dt></span></span> </dl> | <span data-ttu-id="d4d4f-130">NapAgent non è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="d4d4f-130">The NapAgent is not running.</span></span><br/>                            |



 

## <a name="requirements"></a><span data-ttu-id="d4d4f-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d4d4f-131">Requirements</span></span>



| <span data-ttu-id="d4d4f-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="d4d4f-132">Requirement</span></span> | <span data-ttu-id="d4d4f-133">Valore</span><span class="sxs-lookup"><span data-stu-id="d4d4f-133">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4d4f-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d4d4f-134">Minimum supported client</span></span><br/> | <span data-ttu-id="d4d4f-135">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d4d4f-135">Windows Vista \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="d4d4f-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d4d4f-136">Minimum supported server</span></span><br/> | <span data-ttu-id="d4d4f-137">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d4d4f-137">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="d4d4f-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d4d4f-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="d4d4f-139"><dt>NapManagement. h</dt></span><span class="sxs-lookup"><span data-stu-id="d4d4f-139"><dt>NapManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="d4d4f-140">IDL</span><span class="sxs-lookup"><span data-stu-id="d4d4f-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d4d4f-141"><dt>NapManagement. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d4d4f-141"><dt>NapManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="d4d4f-142">DLL</span><span class="sxs-lookup"><span data-stu-id="d4d4f-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d4d4f-143"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d4d4f-143"><dt>Qagent.dll</dt></span></span> </dl>        |



## <a name="see-also"></a><span data-ttu-id="d4d4f-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d4d4f-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4d4f-145">**INapClientManagement**</span><span class="sxs-lookup"><span data-stu-id="d4d4f-145">**INapClientManagement**</span></span>](inapclientmanagement.md)
</dt> </dl>

 

 





