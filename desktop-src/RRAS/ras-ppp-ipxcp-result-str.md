---
title: Struttura RAS_PPP_IPXCP_RESULT (rassapi. h)
description: La struttura dei risultati di RAS \_ PPP \_ IPXCP \_ viene utilizzata per segnalare il risultato di un'operazione di proiezione IPX (Internet-Packet Exchange) PPP per una porta.
ms.assetid: e1236e1b-f0ef-46cf-a12f-35529215752c
keywords:
- RAS struttura RAS_PPP_IPXCP_RESULT
topic_type:
- apiref
api_name:
- RAS_PPP_IPXCP_RESULT
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bb7ca4d006bd1a1df5a645799998b463c0b14f7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048440"
---
# <a name="ras_ppp_ipxcp_result-structure"></a><span data-ttu-id="dc691-104">\_Struttura di \_ \_ risultati IPXCP di Ras PPP</span><span class="sxs-lookup"><span data-stu-id="dc691-104">RAS\_PPP\_IPXCP\_RESULT structure</span></span>

<span data-ttu-id="dc691-105">\[La struttura dei **risultati di Ras \_ PPP \_ IPXCP \_** non è supportata a partire da Windows Vista.\]</span><span class="sxs-lookup"><span data-stu-id="dc691-105">\[The **RAS\_PPP\_IPXCP\_RESULT** structure is not supported as of Windows Vista.\]</span></span>

<span data-ttu-id="dc691-106">La struttura dei **risultati di Ras \_ PPP \_ IPXCP \_** viene utilizzata per segnalare il risultato di un'operazione di proiezione IPX (Internet-Packet Exchange) PPP per una porta.</span><span class="sxs-lookup"><span data-stu-id="dc691-106">The **RAS\_PPP\_IPXCP\_RESULT** structure is used to report the result of a PPP Internetwork Packet Exchange (IPX) projection operation for a port.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc691-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dc691-107">Syntax</span></span>


```C++
typedef struct _RAS_PPP_IPXCP_RESULT {
  DWORD dwError;
  WCHAR wszAddress[RAS_IPXADDRESSLEN + 1];
} RAS_PPP_IPXCP_RESULT;
```



## <a name="members"></a><span data-ttu-id="dc691-108">Members</span><span class="sxs-lookup"><span data-stu-id="dc691-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="dc691-109">**dwError**</span><span class="sxs-lookup"><span data-stu-id="dc691-109">**dwError**</span></span>
</dt> <dd>

<span data-ttu-id="dc691-110">Indica i risultati dell'operazione di proiezione IPX.</span><span class="sxs-lookup"><span data-stu-id="dc691-110">Indicates the results of the IPX projection operation.</span></span> <span data-ttu-id="dc691-111">Il valore nessun \_ errore indica l'esito positivo, nel qual caso il membro **wszAddress** è valido.</span><span class="sxs-lookup"><span data-stu-id="dc691-111">A value of NO\_ERROR indicates success, in which case, the **wszAddress** member is valid.</span></span> <span data-ttu-id="dc691-112">Se l'operazione di proiezione ha esito negativo, **dwError** è un codice di errore di Winerror. h o Raserror. h.</span><span class="sxs-lookup"><span data-stu-id="dc691-112">If the projection operation was not successful, **dwError** is an error code from Winerror.h or Raserror.h.</span></span>

</dd> <dt>

<span data-ttu-id="dc691-113">**wszAddress**</span><span class="sxs-lookup"><span data-stu-id="dc691-113">**wszAddress**</span></span>
</dt> <dd>

<span data-ttu-id="dc691-114">Stringa Unicode con terminazione null che specifica l'indirizzo IPX assegnato al client remoto.</span><span class="sxs-lookup"><span data-stu-id="dc691-114">A null-terminated Unicode string that specifies the IPX address assigned to the remote client.</span></span> <span data-ttu-id="dc691-115">Questa stringa ha \* NET \***.** form del _nodo_ .</span><span class="sxs-lookup"><span data-stu-id="dc691-115">This string has the \*net\***.**_node_ form.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dc691-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dc691-116">Requirements</span></span>



| <span data-ttu-id="dc691-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="dc691-117">Requirement</span></span> | <span data-ttu-id="dc691-118">Valore</span><span class="sxs-lookup"><span data-stu-id="dc691-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="dc691-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dc691-119">Minimum supported client</span></span><br/> | <span data-ttu-id="dc691-120">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="dc691-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="dc691-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dc691-121">Minimum supported server</span></span><br/> | <span data-ttu-id="dc691-122">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="dc691-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="dc691-123">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="dc691-123">End of client support</span></span><br/>    | <span data-ttu-id="dc691-124">Windows XP</span><span class="sxs-lookup"><span data-stu-id="dc691-124">Windows XP</span></span><br/>                                                                |
| <span data-ttu-id="dc691-125">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="dc691-125">End of server support</span></span><br/>    | <span data-ttu-id="dc691-126">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="dc691-126">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="dc691-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="dc691-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="dc691-128"><dt>Rassapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="dc691-128"><dt>Rassapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc691-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dc691-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc691-130">Panoramica del servizio di accesso remoto (RAS)</span><span class="sxs-lookup"><span data-stu-id="dc691-130">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="dc691-131">Strutture di amministrazione del server RAS</span><span class="sxs-lookup"><span data-stu-id="dc691-131">RAS Server Administration Structures</span></span>](ras-server-administration-structures.md)
</dt> <dt>

[<span data-ttu-id="dc691-132">**\_Porta RAS \_ 1**</span><span class="sxs-lookup"><span data-stu-id="dc691-132">**RAS\_PORT\_1**</span></span>](ras-port-1-str.md)
</dt> <dt>

[<span data-ttu-id="dc691-133">**\_risultato della \_ proiezione \_ PPP RAS**</span><span class="sxs-lookup"><span data-stu-id="dc691-133">**RAS\_PPP\_PROJECTION\_RESULT**</span></span>](ras-ppp-projection-result-str.md)
</dt> <dt>

[<span data-ttu-id="dc691-134">**RasAdminPortGetInfo**</span><span class="sxs-lookup"><span data-stu-id="dc691-134">**RasAdminPortGetInfo**</span></span>](rasadminportgetinfo.md)
</dt> </dl>

 

 





