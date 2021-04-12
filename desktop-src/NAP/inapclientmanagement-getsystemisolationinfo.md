---
title: Metodo INapClientManagement GetSystemIsolationInfo (NapManagement. h)
description: Recupera le informazioni sullo stato di isolamento del NapClient.
ms.assetid: e1f69e66-71ca-402e-9c94-8af159d00b21
keywords:
- NAP metodo GetSystemIsolationInfo
- Metodo GetSystemIsolationInfo NAP, interfaccia INapClientManagement
- Interfaccia INapClientManagement NAP, metodo GetSystemIsolationInfo
topic_type:
- apiref
api_name:
- INapClientManagement.GetSystemIsolationInfo
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73b3d446e0a8068353be6656c16f0e6796df8922
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400803"
---
# <a name="inapclientmanagementgetsystemisolationinfo-method"></a><span data-ttu-id="c0406-106">Metodo INapClientManagement:: GetSystemIsolationInfo</span><span class="sxs-lookup"><span data-stu-id="c0406-106">INapClientManagement::GetSystemIsolationInfo method</span></span>

> [!Note]  
> <span data-ttu-id="c0406-107">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="c0406-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="c0406-108">Il metodo **GetSystemIsolationInfo** recupera le informazioni sullo stato di isolamento di NapClient.</span><span class="sxs-lookup"><span data-stu-id="c0406-108">The **GetSystemIsolationInfo** method retrieves information about the isolation state of the NapClient.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0406-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c0406-109">Syntax</span></span>


```C++
HRESULT GetSystemIsolationInfo(
  [out] IsolationInfo **isolationInfo,
  [out] BOOL          *unknownConnections
) const;
```



## <a name="parameters"></a><span data-ttu-id="c0406-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="c0406-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0406-111">*isolationInfo* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="c0406-111">*isolationInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c0406-112">Puntatore a un puntatore a una struttura [**IsolationInfo**](/windows/win32/api/naptypes/ns-naptypes-isolationinfo) che contiene informazioni sullo stato di isolamento.</span><span class="sxs-lookup"><span data-stu-id="c0406-112">A pointer to a pointer to an [**IsolationInfo**](/windows/win32/api/naptypes/ns-naptypes-isolationinfo) structure that contains isolation state information.</span></span>

</dd> <dt>

<span data-ttu-id="c0406-113">*unknownConnections* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="c0406-113">*unknownConnections* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c0406-114">Puntatore a un flag che indica se una o più connessioni sono in uno stato sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="c0406-114">A pointer to a flag that indicates whether any of the connections are in an unknown state.</span></span> <span data-ttu-id="c0406-115">Se uno di essi è, il flag viene impostato su **true**; in caso contrario, il flag è impostato su **false**.</span><span class="sxs-lookup"><span data-stu-id="c0406-115">If any of them are, the flag is set to **TRUE**; otherwise the flag is set to **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0406-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c0406-116">Return value</span></span>

<span data-ttu-id="c0406-117">Il metodo restituisce un codice di stato HRESULT incluso ma non limitato a uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="c0406-117">The method returns an HRESULT status code including but not limited to one of the following.</span></span>



| <span data-ttu-id="c0406-118">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="c0406-118">Return code</span></span>                                                                                         | <span data-ttu-id="c0406-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c0406-119">Description</span></span>                                                        |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="c0406-120"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c0406-120"><dt>**S\_OK**</dt></span></span> </dl>                | <span data-ttu-id="c0406-121">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="c0406-121">Operation successful.</span></span><br/>                                   |
| <dl> <span data-ttu-id="c0406-122"><dt>**E \_ AccessDenied**</dt></span><span class="sxs-lookup"><span data-stu-id="c0406-122"><dt>**E\_ACCESSDENIED**</dt></span></span> </dl>      | <span data-ttu-id="c0406-123">Errore delle autorizzazioni, accesso negato.</span><span class="sxs-lookup"><span data-stu-id="c0406-123">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="c0406-124"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="c0406-124"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>       | <span data-ttu-id="c0406-125">Limite di risorse di sistema. Impossibile eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="c0406-125">System resource limit, could not perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="c0406-126"><dt>**RPC \_ E \_ disconnessa**</dt></span><span class="sxs-lookup"><span data-stu-id="c0406-126"><dt>**RPC\_E\_DISCONNECTED**</dt></span></span> </dl> | <span data-ttu-id="c0406-127">NapAgent non è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="c0406-127">The NapAgent is not running.</span></span><br/>                            |



 

## <a name="remarks"></a><span data-ttu-id="c0406-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="c0406-128">Remarks</span></span>

<span data-ttu-id="c0406-129">Le informazioni di isolamento recuperate non riflettono gli stati sconosciuti.</span><span class="sxs-lookup"><span data-stu-id="c0406-129">The isolation information that is retrieved does not reflect unknown states.</span></span>

## <a name="requirements"></a><span data-ttu-id="c0406-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c0406-130">Requirements</span></span>



| <span data-ttu-id="c0406-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="c0406-131">Requirement</span></span> | <span data-ttu-id="c0406-132">Valore</span><span class="sxs-lookup"><span data-stu-id="c0406-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0406-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c0406-133">Minimum supported client</span></span><br/> | <span data-ttu-id="c0406-134">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c0406-134">Windows Vista \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="c0406-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c0406-135">Minimum supported server</span></span><br/> | <span data-ttu-id="c0406-136">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c0406-136">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="c0406-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c0406-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="c0406-138"><dt>NapManagement. h</dt></span><span class="sxs-lookup"><span data-stu-id="c0406-138"><dt>NapManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="c0406-139">IDL</span><span class="sxs-lookup"><span data-stu-id="c0406-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c0406-140"><dt>NapManagement. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c0406-140"><dt>NapManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="c0406-141">DLL</span><span class="sxs-lookup"><span data-stu-id="c0406-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c0406-142"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c0406-142"><dt>Qagent.dll</dt></span></span> </dl>        |



## <a name="see-also"></a><span data-ttu-id="c0406-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c0406-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0406-144">**INapClientManagement**</span><span class="sxs-lookup"><span data-stu-id="c0406-144">**INapClientManagement**</span></span>](inapclientmanagement.md)
</dt> </dl>

 

 





