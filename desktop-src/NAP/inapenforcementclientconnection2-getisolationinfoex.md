---
title: Metodo INapEnforcementClientConnection2 GetIsolationInfoEx (NapEnforcementClient. h)
description: Viene utilizzato per ottenere informazioni di isolamento relative al client.
ms.assetid: ebacd056-5ab8-4096-821c-8f2987d853c4
keywords:
- NAP metodo GetIsolationInfoEx
- Metodo GetIsolationInfoEx NAP, interfaccia INapEnforcementClientConnection2
- Interfaccia INapEnforcementClientConnection2 NAP, metodo GetIsolationInfoEx
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection2.GetIsolationInfoEx
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6586dd5fc277e62d4478e685f49ac132e744bcc6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479348"
---
# <a name="inapenforcementclientconnection2getisolationinfoex-method"></a><span data-ttu-id="279e4-106">Metodo INapEnforcementClientConnection2:: GetIsolationInfoEx</span><span class="sxs-lookup"><span data-stu-id="279e4-106">INapEnforcementClientConnection2::GetIsolationInfoEx method</span></span>

> [!Note]  
> <span data-ttu-id="279e4-107">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="279e4-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="279e4-108">Il metodo **INapEnforcementClientConnection2:: GetIsolationInfoEx** viene usato per ottenere informazioni di isolamento relative al client.</span><span class="sxs-lookup"><span data-stu-id="279e4-108">The **INapEnforcementClientConnection2::GetIsolationInfoEx** method is used to get isolation information about the client.</span></span>

## <a name="syntax"></a><span data-ttu-id="279e4-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="279e4-109">Syntax</span></span>


```C++
HRESULT GetIsolationInfoEx(
  [out] IsolationInfoEx **isolationInfo
) const;
```



## <a name="parameters"></a><span data-ttu-id="279e4-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="279e4-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="279e4-111">*isolationInfo* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="279e4-111">*isolationInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="279e4-112">Puntatore a un puntatore a una struttura [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) che contiene le informazioni sulla connettività e sullo stato esteso del client.</span><span class="sxs-lookup"><span data-stu-id="279e4-112">A pointer to a pointer to an [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) structure that contains the connectivity and extended state information of the client.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="279e4-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="279e4-113">Return value</span></span>

<span data-ttu-id="279e4-114">È possibile che vengano restituiti anche altri codici di errore specifici di COM.</span><span class="sxs-lookup"><span data-stu-id="279e4-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="279e4-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="279e4-115">Return code</span></span>                                                                                     | <span data-ttu-id="279e4-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="279e4-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="279e4-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="279e4-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="279e4-118">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="279e4-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="279e4-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="279e4-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="279e4-120">Errore delle autorizzazioni, accesso negato.</span><span class="sxs-lookup"><span data-stu-id="279e4-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="279e4-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="279e4-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="279e4-122">Limite di risorse di sistema. Impossibile eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="279e4-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="279e4-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="279e4-123">Remarks</span></span>

<span data-ttu-id="279e4-124">Queste informazioni vengono impostate da NapAgent dopo l'elaborazione di un [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) e non devono essere impostate dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="279e4-124">This information is set by NapAgent after processing an [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) and must not be set by the enforcer.</span></span>

<span data-ttu-id="279e4-125">SHA deve liberare la struttura [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) chiamando [**FreeIsolationInfoEx**](freeisolationinfoex.md).</span><span class="sxs-lookup"><span data-stu-id="279e4-125">The SHA must free the [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) structure by calling [**FreeIsolationInfoEx**](freeisolationinfoex.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="279e4-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="279e4-126">Requirements</span></span>



| <span data-ttu-id="279e4-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="279e4-127">Requirement</span></span> | <span data-ttu-id="279e4-128">Valore</span><span class="sxs-lookup"><span data-stu-id="279e4-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="279e4-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="279e4-129">Minimum supported client</span></span><br/> | <span data-ttu-id="279e4-130">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="279e4-130">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="279e4-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="279e4-131">Minimum supported server</span></span><br/> | <span data-ttu-id="279e4-132">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="279e4-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="279e4-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="279e4-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="279e4-134"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="279e4-134"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="279e4-135">IDL</span><span class="sxs-lookup"><span data-stu-id="279e4-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="279e4-136"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="279e4-136"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="279e4-137">DLL</span><span class="sxs-lookup"><span data-stu-id="279e4-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="279e4-138"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="279e4-138"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="279e4-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="279e4-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="279e4-140">**INapEnforcementClientConnection2**</span><span class="sxs-lookup"><span data-stu-id="279e4-140">**INapEnforcementClientConnection2**</span></span>](inapenforcementclientconnection2.md)
</dt> </dl>

 

 





