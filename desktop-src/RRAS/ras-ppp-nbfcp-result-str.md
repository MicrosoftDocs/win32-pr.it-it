---
title: Struttura RAS_PPP_NBFCP_RESULT (rassapi. h)
description: La struttura dei risultati di RAS \_ PPP \_ NBFCP \_ viene utilizzata per segnalare il risultato di un'operazione di proiezione NBF (PPP NetBEUI Framer) per una porta.
ms.assetid: 670bf125-cad5-481f-89e4-858e636316bd
keywords:
- RAS struttura RAS_PPP_NBFCP_RESULT
topic_type:
- apiref
api_name:
- RAS_PPP_NBFCP_RESULT
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ddcb1cfe28a72e390cedbcc35fa299dddbfb8634
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119983"
---
# <a name="ras_ppp_nbfcp_result-structure"></a><span data-ttu-id="b7f7f-104">\_Struttura di \_ \_ risultati NBFCP di Ras PPP</span><span class="sxs-lookup"><span data-stu-id="b7f7f-104">RAS\_PPP\_NBFCP\_RESULT structure</span></span>

<span data-ttu-id="b7f7f-105">\[La struttura dei **risultati di Ras \_ PPP \_ NBFCP \_** non è supportata a partire da Windows Vista.\]</span><span class="sxs-lookup"><span data-stu-id="b7f7f-105">\[The **RAS\_PPP\_NBFCP\_RESULT** structure is not supported as of Windows Vista.\]</span></span>

<span data-ttu-id="b7f7f-106">La struttura dei **risultati di Ras \_ PPP \_ NBFCP \_** viene utilizzata per segnalare il risultato di un'operazione di proiezione NBF (PPP NetBEUI Framer) per una porta.</span><span class="sxs-lookup"><span data-stu-id="b7f7f-106">The **RAS\_PPP\_NBFCP\_RESULT** structure is used to report the result of a PPP NetBEUI Framer (NBF) projection operation for a port.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7f7f-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b7f7f-107">Syntax</span></span>


```C++
typedef struct _RAS_PPP_NBFCP_RESULT {
  DWORD dwError;
  DWORD dwNetBiosError;
  CHAR  szName[NETBIOS_NAME_LEN + 1];
  WCHAR wszWksta[NETBIOS_NAME_LEN + 1];
} RAS_PPP_NBFCP_RESULT;
```



## <a name="members"></a><span data-ttu-id="b7f7f-108">Members</span><span class="sxs-lookup"><span data-stu-id="b7f7f-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="b7f7f-109">**dwError**</span><span class="sxs-lookup"><span data-stu-id="b7f7f-109">**dwError**</span></span>
</dt> <dd>

<span data-ttu-id="b7f7f-110">Indica i risultati dell'operazione di proiezione NBF.</span><span class="sxs-lookup"><span data-stu-id="b7f7f-110">Indicates the results of the NBF projection operation.</span></span> <span data-ttu-id="b7f7f-111">Il valore nessun \_ errore indica l'esito positivo, nel qual caso il membro **wszWksta** contiene il nome del computer remoto.</span><span class="sxs-lookup"><span data-stu-id="b7f7f-111">A value of NO\_ERROR indicates success, in which case, the **wszWksta** member contains the name of the remote computer.</span></span> <span data-ttu-id="b7f7f-112">Se l'operazione di proiezione ha esito negativo, **dwError** è un codice di errore di Winerror. h o Raserror. h.</span><span class="sxs-lookup"><span data-stu-id="b7f7f-112">If the projection operation was not successful, **dwError** is an error code from Winerror.h or Raserror.h.</span></span>

</dd> <dt>

<span data-ttu-id="b7f7f-113">**dwNetBiosError**</span><span class="sxs-lookup"><span data-stu-id="b7f7f-113">**dwNetBiosError**</span></span>
</dt> <dd>

<span data-ttu-id="b7f7f-114">Ignora il membro nel server. è rilevante solo per il client.</span><span class="sxs-lookup"><span data-stu-id="b7f7f-114">Ignore this member on the server; it is relevant only on the client.</span></span>

</dd> <dt>

<span data-ttu-id="b7f7f-115">**szName**</span><span class="sxs-lookup"><span data-stu-id="b7f7f-115">**szName**</span></span>
</dt> <dd>

<span data-ttu-id="b7f7f-116">Ignora il membro nel server. è rilevante solo per il client.</span><span class="sxs-lookup"><span data-stu-id="b7f7f-116">Ignore this member on the server; it is relevant only on the client.</span></span>

</dd> <dt>

<span data-ttu-id="b7f7f-117">**wszWksta**</span><span class="sxs-lookup"><span data-stu-id="b7f7f-117">**wszWksta**</span></span>
</dt> <dd>

<span data-ttu-id="b7f7f-118">Stringa Unicode con terminazione null che specifica il nome NetBIOS della workstation client RAS.</span><span class="sxs-lookup"><span data-stu-id="b7f7f-118">A null-terminated Unicode string that specifies the NetBIOS name of the RAS client workstation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b7f7f-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b7f7f-119">Requirements</span></span>



| <span data-ttu-id="b7f7f-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="b7f7f-120">Requirement</span></span> | <span data-ttu-id="b7f7f-121">Valore</span><span class="sxs-lookup"><span data-stu-id="b7f7f-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b7f7f-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b7f7f-122">Minimum supported client</span></span><br/> | <span data-ttu-id="b7f7f-123">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b7f7f-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="b7f7f-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b7f7f-124">Minimum supported server</span></span><br/> | <span data-ttu-id="b7f7f-125">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b7f7f-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="b7f7f-126">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="b7f7f-126">End of client support</span></span><br/>    | <span data-ttu-id="b7f7f-127">Windows XP</span><span class="sxs-lookup"><span data-stu-id="b7f7f-127">Windows XP</span></span><br/>                                                                |
| <span data-ttu-id="b7f7f-128">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="b7f7f-128">End of server support</span></span><br/>    | <span data-ttu-id="b7f7f-129">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b7f7f-129">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="b7f7f-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b7f7f-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="b7f7f-131"><dt>Rassapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="b7f7f-131"><dt>Rassapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7f7f-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b7f7f-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7f7f-133">Panoramica del servizio di accesso remoto (RAS)</span><span class="sxs-lookup"><span data-stu-id="b7f7f-133">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="b7f7f-134">Strutture di amministrazione del server RAS</span><span class="sxs-lookup"><span data-stu-id="b7f7f-134">RAS Server Administration Structures</span></span>](ras-server-administration-structures.md)
</dt> <dt>

[<span data-ttu-id="b7f7f-135">**\_Porta RAS \_ 1**</span><span class="sxs-lookup"><span data-stu-id="b7f7f-135">**RAS\_PORT\_1**</span></span>](ras-port-1-str.md)
</dt> <dt>

[<span data-ttu-id="b7f7f-136">**\_risultato della \_ proiezione \_ PPP RAS**</span><span class="sxs-lookup"><span data-stu-id="b7f7f-136">**RAS\_PPP\_PROJECTION\_RESULT**</span></span>](ras-ppp-projection-result-str.md)
</dt> <dt>

[<span data-ttu-id="b7f7f-137">**RasAdminPortGetInfo**</span><span class="sxs-lookup"><span data-stu-id="b7f7f-137">**RasAdminPortGetInfo**</span></span>](rasadminportgetinfo.md)
</dt> </dl>

 

 





