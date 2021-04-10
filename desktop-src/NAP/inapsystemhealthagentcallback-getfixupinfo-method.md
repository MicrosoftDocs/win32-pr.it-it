---
title: Metodo INapSystemHealthAgentCallback GetFixupInfo (NapSystemHealthAgent. h)
description: Viene chiamato da NapAgent per determinare lo stato dell'agente integrità sistema durante l'elaborazione di un SoHResponse.
ms.assetid: cf919b56-3d40-4c49-9c91-25c20ae5ccda
keywords:
- NAP metodo GetFixupInfo
- Metodo GetFixupInfo NAP, interfaccia INapSystemHealthAgentCallback
- Interfaccia INapSystemHealthAgentCallback NAP, metodo GetFixupInfo
topic_type:
- apiref
api_name:
- INapSystemHealthAgentCallback.GetFixupInfo
api_location:
- NapSystemHealthAgent.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1227cbe870c722189c995bff0c967eb187548cd1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120078"
---
# <a name="inapsystemhealthagentcallbackgetfixupinfo-method"></a><span data-ttu-id="1ccbd-106">Metodo INapSystemHealthAgentCallback:: GetFixupInfo</span><span class="sxs-lookup"><span data-stu-id="1ccbd-106">INapSystemHealthAgentCallback::GetFixupInfo method</span></span>

> [!Note]  
> <span data-ttu-id="1ccbd-107">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="1ccbd-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="1ccbd-108">Il metodo **INapSystemHealthAgentCallback:: GetFixupInfo** viene chiamato da napagent per determinare lo stato dell'agente integrità sistema durante l'elaborazione di un [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh).</span><span class="sxs-lookup"><span data-stu-id="1ccbd-108">The **INapSystemHealthAgentCallback::GetFixupInfo** method is called by the NapAgent to determine the state of the system health agent, while it is processing a [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh).</span></span>

## <a name="syntax"></a><span data-ttu-id="1ccbd-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1ccbd-109">Syntax</span></span>


```C++
HRESULT GetFixupInfo(
  [out] FixupInfo **info
);
```



## <a name="parameters"></a><span data-ttu-id="1ccbd-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="1ccbd-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ccbd-111">*informazioni* \[ su out\]</span><span class="sxs-lookup"><span data-stu-id="1ccbd-111">*info* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1ccbd-112">Puntatore a un puntatore a una struttura [**FixupInfo**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo) che contiene lo stato di correzione dell'agente.</span><span class="sxs-lookup"><span data-stu-id="1ccbd-112">A pointer to a pointer to a [**FixupInfo**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo) structure that contains the fix-up status of the agent.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ccbd-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1ccbd-113">Return value</span></span>

<span data-ttu-id="1ccbd-114">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="1ccbd-114">This method can return one of these values.</span></span>



| <span data-ttu-id="1ccbd-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="1ccbd-115">Return code</span></span>                                                                          | <span data-ttu-id="1ccbd-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1ccbd-116">Description</span></span>                   |
|--------------------------------------------------------------------------------------|-------------------------------|
| <dl> <span data-ttu-id="1ccbd-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="1ccbd-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="1ccbd-118">Indica l'esito positivo dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="1ccbd-118">Indicates success.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="1ccbd-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="1ccbd-119">Remarks</span></span>

<span data-ttu-id="1ccbd-120">Questo metodo di callback viene dichiarato dal sistema NAP e deve essere implementato dal writer SHA.</span><span class="sxs-lookup"><span data-stu-id="1ccbd-120">This callback method is declared by the NAP system and is to be implemented by the SHA writer.</span></span>

<span data-ttu-id="1ccbd-121">L'agente integrità sistema deve restituire immediatamente **S \_ OK** senza bloccarsi.</span><span class="sxs-lookup"><span data-stu-id="1ccbd-121">The system health agent must return **S\_OK** immediately without blocking.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ccbd-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1ccbd-122">Requirements</span></span>



| <span data-ttu-id="1ccbd-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="1ccbd-123">Requirement</span></span> | <span data-ttu-id="1ccbd-124">Valore</span><span class="sxs-lookup"><span data-stu-id="1ccbd-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ccbd-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1ccbd-125">Minimum supported client</span></span><br/> | <span data-ttu-id="1ccbd-126">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1ccbd-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="1ccbd-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1ccbd-127">Minimum supported server</span></span><br/> | <span data-ttu-id="1ccbd-128">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="1ccbd-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="1ccbd-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1ccbd-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="1ccbd-130"><dt>NapSystemHealthAgent. h</dt></span><span class="sxs-lookup"><span data-stu-id="1ccbd-130"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="1ccbd-131">IDL</span><span class="sxs-lookup"><span data-stu-id="1ccbd-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1ccbd-132"><dt>NapSystemHealthAgent. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1ccbd-132"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ccbd-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1ccbd-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ccbd-134">**INapSystemHealthAgentCallback**</span><span class="sxs-lookup"><span data-stu-id="1ccbd-134">**INapSystemHealthAgentCallback**</span></span>](inapsystemhealthagentcallback.md)
</dt> </dl>

 

 





