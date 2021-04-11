---
title: Struttura RAS_PPP_ATCP_RESULT (rassapi. h)
description: La struttura dei risultati di RAS \_ PPP \_ ATCP \_ viene utilizzata per segnalare il risultato di un'operazione di proiezione del protocollo AppleTalk per una porta.
ms.assetid: ac9df618-f79c-4066-a37e-f92e64e951dd
keywords:
- RAS struttura RAS_PPP_ATCP_RESULT
topic_type:
- apiref
api_name:
- RAS_PPP_ATCP_RESULT
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66f3f950af9d5bdde8feef085457a895212ad04b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964326"
---
# <a name="ras_ppp_atcp_result-structure"></a><span data-ttu-id="a9d4f-104">\_Struttura di \_ \_ risultati ATCP di Ras PPP</span><span class="sxs-lookup"><span data-stu-id="a9d4f-104">RAS\_PPP\_ATCP\_RESULT structure</span></span>

<span data-ttu-id="a9d4f-105">\[La struttura dei **risultati di Ras \_ PPP \_ ATCP \_** non è supportata a partire da Windows Vista.\]</span><span class="sxs-lookup"><span data-stu-id="a9d4f-105">\[The **RAS\_PPP\_ATCP\_RESULT** structure is not supported as of Windows Vista.\]</span></span>

<span data-ttu-id="a9d4f-106">La struttura dei **risultati di Ras \_ PPP \_ ATCP \_** viene utilizzata per segnalare il risultato di un'operazione di proiezione del protocollo AppleTalk per una porta.</span><span class="sxs-lookup"><span data-stu-id="a9d4f-106">The **RAS\_PPP\_ATCP\_RESULT** structure is used to report the result of an AppleTalk protocol projection operation for a port.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9d4f-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a9d4f-107">Syntax</span></span>


```C++
typedef struct _RAS_PPP_ATCP_RESULT {
  DWORD dwError;
  WCHAR wszAddress[RAS_ATADDRESSLEN + 1];
} RAS_PPP_ATCP_RESULT;
```



## <a name="members"></a><span data-ttu-id="a9d4f-108">Members</span><span class="sxs-lookup"><span data-stu-id="a9d4f-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="a9d4f-109">**dwError**</span><span class="sxs-lookup"><span data-stu-id="a9d4f-109">**dwError**</span></span>
</dt> <dd>

<span data-ttu-id="a9d4f-110">Specifica un valore che indica i risultati dell'operazione di proiezione AppleTalk.</span><span class="sxs-lookup"><span data-stu-id="a9d4f-110">Specifies a value that indicates the results of the AppleTalk projection operation.</span></span> <span data-ttu-id="a9d4f-111">Il valore nessun \_ errore indica l'esito positivo, nel qual caso il membro **wszAddress** è valido.</span><span class="sxs-lookup"><span data-stu-id="a9d4f-111">A value of NO\_ERROR indicates success, in which case, the **wszAddress** member is valid.</span></span> <span data-ttu-id="a9d4f-112">Se l'operazione di proiezione ha esito negativo, **dwError** è un codice di errore di Winerror. h o Raserror. h.</span><span class="sxs-lookup"><span data-stu-id="a9d4f-112">If the projection operation is not successful, **dwError** is an error code from Winerror.h or Raserror.h.</span></span>

</dd> <dt>

<span data-ttu-id="a9d4f-113">**wszAddress**</span><span class="sxs-lookup"><span data-stu-id="a9d4f-113">**wszAddress**</span></span>
</dt> <dd>

<span data-ttu-id="a9d4f-114">Specifica una stringa Unicode con terminazione null che specifica l'indirizzo IP assegnato al client remoto.</span><span class="sxs-lookup"><span data-stu-id="a9d4f-114">Specifies a null-terminated Unicode string that specifies the IP address assigned to the remote client.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a9d4f-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a9d4f-115">Requirements</span></span>



| <span data-ttu-id="a9d4f-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="a9d4f-116">Requirement</span></span> | <span data-ttu-id="a9d4f-117">Valore</span><span class="sxs-lookup"><span data-stu-id="a9d4f-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="a9d4f-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a9d4f-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a9d4f-119">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a9d4f-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="a9d4f-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a9d4f-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a9d4f-121">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a9d4f-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="a9d4f-122">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="a9d4f-122">End of client support</span></span><br/>    | <span data-ttu-id="a9d4f-123">Windows XP</span><span class="sxs-lookup"><span data-stu-id="a9d4f-123">Windows XP</span></span><br/>                                                                |
| <span data-ttu-id="a9d4f-124">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="a9d4f-124">End of server support</span></span><br/>    | <span data-ttu-id="a9d4f-125">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a9d4f-125">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="a9d4f-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a9d4f-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="a9d4f-127"><dt>Rassapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="a9d4f-127"><dt>Rassapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9d4f-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a9d4f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9d4f-129">Panoramica del servizio di accesso remoto (RAS)</span><span class="sxs-lookup"><span data-stu-id="a9d4f-129">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="a9d4f-130">Strutture di amministrazione del server RAS</span><span class="sxs-lookup"><span data-stu-id="a9d4f-130">RAS Server Administration Structures</span></span>](ras-server-administration-structures.md)
</dt> <dt>

[<span data-ttu-id="a9d4f-131">**\_risultato della \_ proiezione \_ PPP RAS**</span><span class="sxs-lookup"><span data-stu-id="a9d4f-131">**RAS\_PPP\_PROJECTION\_RESULT**</span></span>](ras-ppp-projection-result-str.md)
</dt> </dl>

 

 





