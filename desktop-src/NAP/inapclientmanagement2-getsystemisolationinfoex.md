---
title: Metodo INapClientManagement2 GetSystemIsolationInfoEx (NapManagement. h)
description: Recupera le informazioni sullo stato di isolamento e sullo stato di isolamento esteso di NapClient.
ms.assetid: 614bcf19-873e-4043-98b2-dcb152bae3e2
keywords:
- NAP metodo GetSystemIsolationInfoEx
- Metodo GetSystemIsolationInfoEx NAP, interfaccia INapClientManagement2
- Interfaccia INapClientManagement2 NAP, metodo GetSystemIsolationInfoEx
topic_type:
- apiref
api_name:
- INapClientManagement2.GetSystemIsolationInfoEx
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e75a6554ea7e55c3bebe35b797f888494a55627
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048162"
---
# <a name="inapclientmanagement2getsystemisolationinfoex-method"></a><span data-ttu-id="f101e-106">Metodo INapClientManagement2:: GetSystemIsolationInfoEx</span><span class="sxs-lookup"><span data-stu-id="f101e-106">INapClientManagement2::GetSystemIsolationInfoEx method</span></span>

> [!Note]  
> <span data-ttu-id="f101e-107">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="f101e-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="f101e-108">Il metodo **GetSystemIsolationInfoEx** recupera le informazioni sullo stato di isolamento e sullo stato di isolamento esteso di NapClient.</span><span class="sxs-lookup"><span data-stu-id="f101e-108">The **GetSystemIsolationInfoEx** method retrieves information about the isolation state and extended isolation state of the NapClient.</span></span>

## <a name="syntax"></a><span data-ttu-id="f101e-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f101e-109">Syntax</span></span>


```C++
HRESULT GetSystemIsolationInfoEx(
  [out] IsolationInfoEx **isolationInfo,
  [out] BOOL            *unknownConnections
) const;
```



## <a name="parameters"></a><span data-ttu-id="f101e-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="f101e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f101e-111">*isolationInfo* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="f101e-111">*isolationInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f101e-112">Puntatore a un puntatore a una struttura [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) che contiene informazioni sullo stato di isolamento.</span><span class="sxs-lookup"><span data-stu-id="f101e-112">A pointer to a pointer to an [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) structure that contains isolation state information.</span></span>

</dd> <dt>

<span data-ttu-id="f101e-113">*unknownConnections* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="f101e-113">*unknownConnections* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f101e-114">Puntatore a un BOOL che è **true** se una delle connessioni è in uno stato sconosciuto e **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="f101e-114">A pointer to a BOOL that is **TRUE** if any of the connections are in an unknown state and **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f101e-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f101e-115">Return value</span></span>

<span data-ttu-id="f101e-116">Il metodo restituisce un codice di stato HRESULT incluso ma non limitato a uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="f101e-116">The method returns an HRESULT status code including but not limited to one of the following.</span></span>



| <span data-ttu-id="f101e-117">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="f101e-117">Return code</span></span>                                                                                         | <span data-ttu-id="f101e-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f101e-118">Description</span></span>                                                        |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="f101e-119"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f101e-119"><dt>**S\_OK**</dt></span></span> </dl>                | <span data-ttu-id="f101e-120">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="f101e-120">Operation successful.</span></span><br/>                                   |
| <dl> <span data-ttu-id="f101e-121"><dt>**E \_ AccessDenied**</dt></span><span class="sxs-lookup"><span data-stu-id="f101e-121"><dt>**E\_ACCESSDENIED**</dt></span></span> </dl>      | <span data-ttu-id="f101e-122">Errore delle autorizzazioni, accesso negato.</span><span class="sxs-lookup"><span data-stu-id="f101e-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="f101e-123"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="f101e-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>       | <span data-ttu-id="f101e-124">Limite di risorse di sistema. Impossibile eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="f101e-124">System resource limit, could not perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="f101e-125"><dt>**RPC \_ E \_ disconnessa**</dt></span><span class="sxs-lookup"><span data-stu-id="f101e-125"><dt>**RPC\_E\_DISCONNECTED**</dt></span></span> </dl> | <span data-ttu-id="f101e-126">NapAgent non è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="f101e-126">The NapAgent is not running.</span></span><br/>                            |



 

## <a name="remarks"></a><span data-ttu-id="f101e-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="f101e-127">Remarks</span></span>

<span data-ttu-id="f101e-128">Le informazioni di isolamento recuperate non riflettono gli stati sconosciuti.</span><span class="sxs-lookup"><span data-stu-id="f101e-128">The isolation information that is retrieved does not reflect unknown states.</span></span>

<span data-ttu-id="f101e-129">SHA deve liberare la struttura [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) chiamando [**FreeIsolationInfoEx**](freeisolationinfoex.md).</span><span class="sxs-lookup"><span data-stu-id="f101e-129">The SHA must free the [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) structure by calling [**FreeIsolationInfoEx**](freeisolationinfoex.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f101e-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f101e-130">Requirements</span></span>



| <span data-ttu-id="f101e-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="f101e-131">Requirement</span></span> | <span data-ttu-id="f101e-132">Valore</span><span class="sxs-lookup"><span data-stu-id="f101e-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f101e-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f101e-133">Minimum supported client</span></span><br/> | <span data-ttu-id="f101e-134">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f101e-134">Windows Vista \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="f101e-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f101e-135">Minimum supported server</span></span><br/> | <span data-ttu-id="f101e-136">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f101e-136">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="f101e-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f101e-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="f101e-138"><dt>NapManagement. h</dt></span><span class="sxs-lookup"><span data-stu-id="f101e-138"><dt>NapManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="f101e-139">IDL</span><span class="sxs-lookup"><span data-stu-id="f101e-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f101e-140"><dt>NapManagement. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f101e-140"><dt>NapManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="f101e-141">DLL</span><span class="sxs-lookup"><span data-stu-id="f101e-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f101e-142"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f101e-142"><dt>Qagent.dll</dt></span></span> </dl>        |



## <a name="see-also"></a><span data-ttu-id="f101e-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f101e-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f101e-144">**INapClientManagement2**</span><span class="sxs-lookup"><span data-stu-id="f101e-144">**INapClientManagement2**</span></span>](inapclientmanagement2.md)
</dt> </dl>

 

 





