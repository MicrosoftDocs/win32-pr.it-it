---
title: Struttura RAS_PPP_IPCP_RESULT (rassapi. h)
description: La struttura dei risultati di RAS \_ PPP \_ protocollo IPCP \_ viene utilizzata per segnalare il risultato di un'operazione di proiezione IP (Internet Protocol) PPP per una porta.
ms.assetid: edbdc8f2-ba56-4d34-8908-f7eccc2ebf61
keywords:
- RAS struttura RAS_PPP_IPCP_RESULT
topic_type:
- apiref
api_name:
- RAS_PPP_IPCP_RESULT
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eedcd7c7390e01849371eee2cbb24ffa2593900d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517878"
---
# <a name="ras_ppp_ipcp_result-structure"></a><span data-ttu-id="99956-104">\_Struttura di \_ \_ risultati protocollo IPCP di Ras PPP</span><span class="sxs-lookup"><span data-stu-id="99956-104">RAS\_PPP\_IPCP\_RESULT structure</span></span>

<span data-ttu-id="99956-105">\[La struttura dei **risultati di Ras \_ PPP \_ protocollo IPCP \_** non è supportata a partire da Windows Vista.\]</span><span class="sxs-lookup"><span data-stu-id="99956-105">\[The **RAS\_PPP\_IPCP\_RESULT** structure is not supported as of Windows Vista.\]</span></span>

<span data-ttu-id="99956-106">La struttura dei **risultati di Ras \_ PPP \_ protocollo IPCP \_** viene utilizzata per segnalare il risultato di un'operazione di proiezione IP (Internet Protocol) PPP per una porta.</span><span class="sxs-lookup"><span data-stu-id="99956-106">The **RAS\_PPP\_IPCP\_RESULT** structure is used to report the result of a PPP Internet Protocol (IP) projection operation for a port.</span></span>

## <a name="syntax"></a><span data-ttu-id="99956-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="99956-107">Syntax</span></span>


```C++
typedef struct _RAS_PPP_IPCP_RESULT {
  DWORD dwError;
  WCHAR wszAddress[RAS_IPADDRESSLEN + 1];
} RAS_PPP_IPCP_RESULT;
```



## <a name="members"></a><span data-ttu-id="99956-108">Members</span><span class="sxs-lookup"><span data-stu-id="99956-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="99956-109">**dwError**</span><span class="sxs-lookup"><span data-stu-id="99956-109">**dwError**</span></span>
</dt> <dd>

<span data-ttu-id="99956-110">Indica i risultati dell'operazione di proiezione IP.</span><span class="sxs-lookup"><span data-stu-id="99956-110">Indicates the results of the IP projection operation.</span></span> <span data-ttu-id="99956-111">Il valore nessun \_ errore indica l'esito positivo, nel qual caso il membro **wszAddress** è valido.</span><span class="sxs-lookup"><span data-stu-id="99956-111">A value of NO\_ERROR indicates success, in which case, the **wszAddress** member is valid.</span></span> <span data-ttu-id="99956-112">Se l'operazione di proiezione ha esito negativo, **dwError** è un codice di errore di Winerror. h o Raserror. h.</span><span class="sxs-lookup"><span data-stu-id="99956-112">If the projection operation was not successful, **dwError** is an error code from Winerror.h or Raserror.h.</span></span>

</dd> <dt>

<span data-ttu-id="99956-113">**wszAddress**</span><span class="sxs-lookup"><span data-stu-id="99956-113">**wszAddress**</span></span>
</dt> <dd>

<span data-ttu-id="99956-114">Stringa Unicode con terminazione null che specifica l'indirizzo IP assegnato al client remoto.</span><span class="sxs-lookup"><span data-stu-id="99956-114">A null-terminated Unicode string that specifies the IP address assigned to the remote client.</span></span> <span data-ttu-id="99956-115">Il formato di questa stringa è \*\*\*\*.\*\* _b_\* _._ *_c_*_._ \* _d_.</span><span class="sxs-lookup"><span data-stu-id="99956-115">This string has the form *a\***.**_b_*_._*_c_*_._\*_d_.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="99956-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="99956-116">Requirements</span></span>



| <span data-ttu-id="99956-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="99956-117">Requirement</span></span> | <span data-ttu-id="99956-118">Valore</span><span class="sxs-lookup"><span data-stu-id="99956-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="99956-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="99956-119">Minimum supported client</span></span><br/> | <span data-ttu-id="99956-120">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="99956-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="99956-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="99956-121">Minimum supported server</span></span><br/> | <span data-ttu-id="99956-122">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="99956-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="99956-123">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="99956-123">End of client support</span></span><br/>    | <span data-ttu-id="99956-124">Windows XP</span><span class="sxs-lookup"><span data-stu-id="99956-124">Windows XP</span></span><br/>                                                                |
| <span data-ttu-id="99956-125">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="99956-125">End of server support</span></span><br/>    | <span data-ttu-id="99956-126">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="99956-126">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="99956-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="99956-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="99956-128"><dt>Rassapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="99956-128"><dt>Rassapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="99956-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="99956-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99956-130">Panoramica del servizio di accesso remoto (RAS)</span><span class="sxs-lookup"><span data-stu-id="99956-130">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="99956-131">Strutture di amministrazione del server RAS</span><span class="sxs-lookup"><span data-stu-id="99956-131">RAS Server Administration Structures</span></span>](ras-server-administration-structures.md)
</dt> <dt>

[<span data-ttu-id="99956-132">**\_Porta RAS \_ 1**</span><span class="sxs-lookup"><span data-stu-id="99956-132">**RAS\_PORT\_1**</span></span>](ras-port-1-str.md)
</dt> <dt>

[<span data-ttu-id="99956-133">**\_risultato della \_ proiezione \_ PPP RAS**</span><span class="sxs-lookup"><span data-stu-id="99956-133">**RAS\_PPP\_PROJECTION\_RESULT**</span></span>](ras-ppp-projection-result-str.md)
</dt> <dt>

[<span data-ttu-id="99956-134">**RasAdminPortGetInfo**</span><span class="sxs-lookup"><span data-stu-id="99956-134">**RasAdminPortGetInfo**</span></span>](rasadminportgetinfo.md)
</dt> </dl>

 

 





