---
title: Metodo INapEnforcementClientConnection2 SetIsolationInfoEx (NapEnforcementClient. h)
description: Viene usato da NapAgent per impostare le informazioni di isolamento per il client.
ms.assetid: 1b1a41a1-73a6-4c81-8366-15d06c67e228
keywords:
- NAP metodo SetIsolationInfoEx
- Metodo SetIsolationInfoEx NAP, interfaccia INapEnforcementClientConnection2
- Interfaccia INapEnforcementClientConnection2 NAP, metodo SetIsolationInfoEx
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection2.SetIsolationInfoEx
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 711b4bfd27c3bd92d48a78f4767f5ed452b2d4f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302768"
---
# <a name="inapenforcementclientconnection2setisolationinfoex-method"></a><span data-ttu-id="abd54-106">Metodo INapEnforcementClientConnection2:: SetIsolationInfoEx</span><span class="sxs-lookup"><span data-stu-id="abd54-106">INapEnforcementClientConnection2::SetIsolationInfoEx method</span></span>

> [!Note]  
> <span data-ttu-id="abd54-107">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="abd54-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="abd54-108">Il metodo **INapEnforcementClientConnection2:: SetIsolationInfoEx** viene usato da napagent per impostare le informazioni di isolamento per il client.</span><span class="sxs-lookup"><span data-stu-id="abd54-108">The **INapEnforcementClientConnection2::SetIsolationInfoEx** method is used by the NapAgent to set the isolation information for the client.</span></span>

## <a name="syntax"></a><span data-ttu-id="abd54-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="abd54-109">Syntax</span></span>


```C++
HRESULT SetIsolationInfoEx(
  [in] const IsolationInfoEx *isolationInfo
);
```



## <a name="parameters"></a><span data-ttu-id="abd54-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="abd54-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="abd54-111">*isolationInfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="abd54-111">*isolationInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="abd54-112">Puntatore a una struttura [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) che contiene lo stato di connettività del client.</span><span class="sxs-lookup"><span data-stu-id="abd54-112">A pointer to an [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) structure that contains the connectivity state of the client.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="abd54-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="abd54-113">Return value</span></span>

<span data-ttu-id="abd54-114">È possibile che vengano restituiti anche altri codici di errore specifici di COM.</span><span class="sxs-lookup"><span data-stu-id="abd54-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="abd54-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="abd54-115">Return code</span></span>                                                                                     | <span data-ttu-id="abd54-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="abd54-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="abd54-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="abd54-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="abd54-118">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="abd54-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="abd54-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="abd54-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="abd54-120">Errore delle autorizzazioni, accesso negato.</span><span class="sxs-lookup"><span data-stu-id="abd54-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="abd54-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="abd54-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="abd54-122">Limite di risorse di sistema. Impossibile eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="abd54-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="abd54-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="abd54-123">Remarks</span></span>

<span data-ttu-id="abd54-124">Queste informazioni vengono impostate da NapAgent dopo l'elaborazione di un [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) e non devono essere impostate dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="abd54-124">This information is set by NapAgent after processing an [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) and must not be set by the enforcer.</span></span>

## <a name="requirements"></a><span data-ttu-id="abd54-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="abd54-125">Requirements</span></span>



| <span data-ttu-id="abd54-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="abd54-126">Requirement</span></span> | <span data-ttu-id="abd54-127">Valore</span><span class="sxs-lookup"><span data-stu-id="abd54-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="abd54-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="abd54-128">Minimum supported client</span></span><br/> | <span data-ttu-id="abd54-129">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="abd54-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="abd54-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="abd54-130">Minimum supported server</span></span><br/> | <span data-ttu-id="abd54-131">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="abd54-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="abd54-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="abd54-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="abd54-133"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="abd54-133"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="abd54-134">IDL</span><span class="sxs-lookup"><span data-stu-id="abd54-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="abd54-135"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="abd54-135"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="abd54-136">DLL</span><span class="sxs-lookup"><span data-stu-id="abd54-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="abd54-137"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="abd54-137"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="abd54-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="abd54-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="abd54-139">**INapEnforcementClientConnection2**</span><span class="sxs-lookup"><span data-stu-id="abd54-139">**INapEnforcementClientConnection2**</span></span>](inapenforcementclientconnection2.md)
</dt> </dl>

 

 





