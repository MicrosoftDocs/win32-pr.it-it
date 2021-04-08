---
title: Struttura RAS_PPP_PROJECTION_RESULT (rassapi. h)
description: La struttura dei risultati della \_ proiezione PPP RAS \_ \_ viene usata per segnalare i risultati delle varie operazioni di proiezione PPP per una porta.
ms.assetid: 061b1b51-4b6f-4127-8ee5-8a1913a2aa99
keywords:
- RAS struttura RAS_PPP_PROJECTION_RESULT
topic_type:
- apiref
api_name:
- RAS_PPP_PROJECTION_RESULT
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a9aa3aef828249b5c72f9e7cdd1bd3b69c96832
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741794"
---
# <a name="ras_ppp_projection_result-structure"></a><span data-ttu-id="57de5-104">\_Struttura di \_ Risultati della proiezione PPP RAS \_</span><span class="sxs-lookup"><span data-stu-id="57de5-104">RAS\_PPP\_PROJECTION\_RESULT structure</span></span>

<span data-ttu-id="57de5-105">\[La struttura dei **\_ \_ \_ Risultati della proiezione PPP RAS** non è supportata a partire da Windows Vista.\]</span><span class="sxs-lookup"><span data-stu-id="57de5-105">\[The **RAS\_PPP\_PROJECTION\_RESULT** structure is not supported as of Windows Vista.\]</span></span>

<span data-ttu-id="57de5-106">La struttura dei risultati della **\_ \_ proiezione \_ PPP RAS** viene usata per segnalare i risultati delle varie operazioni di proiezione PPP per una porta.</span><span class="sxs-lookup"><span data-stu-id="57de5-106">The **RAS\_PPP\_PROJECTION\_RESULT** structure is used to report the results of the various PPP projection operations for a port.</span></span>

## <a name="syntax"></a><span data-ttu-id="57de5-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="57de5-107">Syntax</span></span>


```C++
typedef struct _RAS_PPP_PROJECTION_RESULT {
  RAS_PPP_NBFCP_RESULT nbf;
  RAS_PPP_IPCP_RESULT  ip;
  RAS_PPP_IPXCP_RESULT ipx;
  RAS_PPP_ATCP_RESULT  at;
} RAS_PPP_PROJECTION_RESULT;
```



## <a name="members"></a><span data-ttu-id="57de5-108">Members</span><span class="sxs-lookup"><span data-stu-id="57de5-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="57de5-109">**nbf**</span><span class="sxs-lookup"><span data-stu-id="57de5-109">**nbf**</span></span>
</dt> <dd>

<span data-ttu-id="57de5-110">Una struttura di [**\_ \_ \_ risultati NBFCP di Ras PPP**](ras-ppp-nbfcp-result-str.md) che segnala il risultato di un'operazione di proiezione di NBF (PPP NetBEUI Framer).</span><span class="sxs-lookup"><span data-stu-id="57de5-110">A [**RAS\_PPP\_NBFCP\_RESULT**](ras-ppp-nbfcp-result-str.md) structure that reports the result of a PPP NetBEUI Framer (NBF) projection operation.</span></span>

</dd> <dt>

<span data-ttu-id="57de5-111">**IP**</span><span class="sxs-lookup"><span data-stu-id="57de5-111">**ip**</span></span>
</dt> <dd>

<span data-ttu-id="57de5-112">Una struttura di [**\_ \_ \_ risultati protocollo IPCP RAS PPP**](ras-ppp-ipcp-result-str.md) che segnala il risultato di un'operazione di proiezione IP (Internet Protocol) PPP.</span><span class="sxs-lookup"><span data-stu-id="57de5-112">A [**RAS\_PPP\_IPCP\_RESULT**](ras-ppp-ipcp-result-str.md) structure that reports the result of a PPP Internet Protocol (IP) projection operation.</span></span>

</dd> <dt>

<span data-ttu-id="57de5-113">**IPX**</span><span class="sxs-lookup"><span data-stu-id="57de5-113">**ipx**</span></span>
</dt> <dd>

<span data-ttu-id="57de5-114">Struttura [**di \_ \_ \_ risultato IPXCP di Ras PPP**](ras-ppp-ipxcp-result-str.md) che indica il risultato di un'operazione di proiezione IPX (Internet-Packet Exchange) PPP.</span><span class="sxs-lookup"><span data-stu-id="57de5-114">A [**RAS\_PPP\_IPXCP\_RESULT**](ras-ppp-ipxcp-result-str.md) structure that reports the result of a PPP Internetwork Packet Exchange (IPX) projection operation.</span></span>

</dd> <dt>

<span data-ttu-id="57de5-115">**at**</span><span class="sxs-lookup"><span data-stu-id="57de5-115">**at**</span></span>
</dt> <dd>

<span data-ttu-id="57de5-116">Struttura [**di \_ \_ \_ risultati ATCP PPP RAS**](ras-ppp-atcp-result-str.md) .</span><span class="sxs-lookup"><span data-stu-id="57de5-116">A [**RAS\_PPP\_ATCP\_RESULT**](ras-ppp-atcp-result-str.md) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="57de5-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="57de5-117">Remarks</span></span>

<span data-ttu-id="57de5-118">Questa struttura segnala i risultati della proiezione per i protocolli NetBEUI, TCP/IP e IPX.</span><span class="sxs-lookup"><span data-stu-id="57de5-118">This structure reports the projection results for NetBEUI, TCP/IP, and IPX protocols.</span></span> <span data-ttu-id="57de5-119">Ogni struttura PPP dispone di un membro **dwError** che indica se le altre informazioni nella struttura sono valide.</span><span class="sxs-lookup"><span data-stu-id="57de5-119">Each PPP structure has a **dwError** member that indicates whether the other information in the structure is valid.</span></span> <span data-ttu-id="57de5-120">Se **dwError** non è un \_ errore, le altre informazioni sono valide.</span><span class="sxs-lookup"><span data-stu-id="57de5-120">If **dwError** is NO\_ERROR, the other information is valid.</span></span> <span data-ttu-id="57de5-121">Se **dwError** è uno dei codici di errore in Winerror. h o Raserror. h, le altre informazioni non sono valide.</span><span class="sxs-lookup"><span data-stu-id="57de5-121">If **dwError** is one of the error codes in Winerror.h or Raserror.h, the other information is not valid.</span></span>

## <a name="requirements"></a><span data-ttu-id="57de5-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="57de5-122">Requirements</span></span>



| <span data-ttu-id="57de5-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="57de5-123">Requirement</span></span> | <span data-ttu-id="57de5-124">Valore</span><span class="sxs-lookup"><span data-stu-id="57de5-124">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="57de5-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="57de5-125">Minimum supported client</span></span><br/> | <span data-ttu-id="57de5-126">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="57de5-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="57de5-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="57de5-127">Minimum supported server</span></span><br/> | <span data-ttu-id="57de5-128">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="57de5-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="57de5-129">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="57de5-129">End of client support</span></span><br/>    | <span data-ttu-id="57de5-130">Windows XP</span><span class="sxs-lookup"><span data-stu-id="57de5-130">Windows XP</span></span><br/>                                                                |
| <span data-ttu-id="57de5-131">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="57de5-131">End of server support</span></span><br/>    | <span data-ttu-id="57de5-132">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="57de5-132">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="57de5-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="57de5-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="57de5-134"><dt>Rassapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="57de5-134"><dt>Rassapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="57de5-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="57de5-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57de5-136">Panoramica del servizio di accesso remoto (RAS)</span><span class="sxs-lookup"><span data-stu-id="57de5-136">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="57de5-137">Strutture di amministrazione del server RAS</span><span class="sxs-lookup"><span data-stu-id="57de5-137">RAS Server Administration Structures</span></span>](ras-server-administration-structures.md)
</dt> <dt>

[<span data-ttu-id="57de5-138">**\_Porta RAS \_ 1**</span><span class="sxs-lookup"><span data-stu-id="57de5-138">**RAS\_PORT\_1**</span></span>](ras-port-1-str.md)
</dt> <dt>

[<span data-ttu-id="57de5-139">**\_ \_ risultato ATCP PPP \_ RAS**</span><span class="sxs-lookup"><span data-stu-id="57de5-139">**RAS\_PPP\_ATCP\_RESULT**</span></span>](ras-ppp-atcp-result-str.md)
</dt> <dt>

[<span data-ttu-id="57de5-140">**\_ \_ risultato protocollo IPCP PPP \_ RAS**</span><span class="sxs-lookup"><span data-stu-id="57de5-140">**RAS\_PPP\_IPCP\_RESULT**</span></span>](ras-ppp-ipcp-result-str.md)
</dt> <dt>

[<span data-ttu-id="57de5-141">**\_ \_ risultato IPXCP PPP \_ RAS**</span><span class="sxs-lookup"><span data-stu-id="57de5-141">**RAS\_PPP\_IPXCP\_RESULT**</span></span>](ras-ppp-ipxcp-result-str.md)
</dt> <dt>

[<span data-ttu-id="57de5-142">**\_ \_ risultato NBFCP PPP \_ RAS**</span><span class="sxs-lookup"><span data-stu-id="57de5-142">**RAS\_PPP\_NBFCP\_RESULT**</span></span>](ras-ppp-nbfcp-result-str.md)
</dt> <dt>

[<span data-ttu-id="57de5-143">**RasAdminPortGetInfo**</span><span class="sxs-lookup"><span data-stu-id="57de5-143">**RasAdminPortGetInfo**</span></span>](rasadminportgetinfo.md)
</dt> </dl>

 

 





