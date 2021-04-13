---
title: Struttura CB_TARGET_INFO (Cbclient. h)
description: Contiene informazioni sul computer di destinazione e sugli indirizzi IP in cui devono essere reindirizzate le connessioni in ingresso.
ms.assetid: 60612E10-9D82-4F38-87F7-B24F51E6EBDA
ms.tgt_platform: multiple
keywords:
- Struttura CB_TARGET_INFO Servizi Desktop remoto
- Puntatore alla struttura PCB_TARGET_INFO Servizi Desktop remoto
topic_type:
- apiref
api_name:
- CB_TARGET_INFO
api_location:
- Cbclient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9bbb982636449075b758ac61178f5e97da47ce7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400400"
---
# <a name="cb_target_info-structure"></a><span data-ttu-id="e7ba8-105">Struttura delle informazioni di \_ destinazione CB \_</span><span class="sxs-lookup"><span data-stu-id="e7ba8-105">CB\_TARGET\_INFO structure</span></span>

<span data-ttu-id="e7ba8-106">Contiene informazioni sul computer di destinazione e sugli indirizzi IP in cui devono essere reindirizzate le connessioni in ingresso.</span><span class="sxs-lookup"><span data-stu-id="e7ba8-106">Contains information about the target computer and IP addresses where incoming connections should be redirected.</span></span> <span data-ttu-id="e7ba8-107">Questa struttura viene utilizzata con il metodo [**IConnectionBrokerClient:: GetTargetInfo**](iconnectionbrokerclient-gettargetinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="e7ba8-107">This structure is used with the [**IConnectionBrokerClient::GetTargetInfo**](iconnectionbrokerclient-gettargetinfo.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7ba8-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e7ba8-108">Syntax</span></span>


```C++
typedef struct {
  WCHAR ServerName[128];
  DWORD AddressCount;
  WCHAR Addresses[CB_MAX_ADDRESSES][CB_IPADDRESS_LEN];
} CB_TARGET_INFO, *PCB_TARGET_INFO;
```



## <a name="members"></a><span data-ttu-id="e7ba8-109">Members</span><span class="sxs-lookup"><span data-stu-id="e7ba8-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="e7ba8-110">**ServerName**</span><span class="sxs-lookup"><span data-stu-id="e7ba8-110">**ServerName**</span></span>
</dt> <dd>

<span data-ttu-id="e7ba8-111">Rappresenta il nome di dominio completo del server di destinazione.</span><span class="sxs-lookup"><span data-stu-id="e7ba8-111">Represents the fully qualified domain name of the target server.</span></span> <span data-ttu-id="e7ba8-112">Per uno scenario di RDV (Desktop remoto Virtualization), questo membro è **null**.</span><span class="sxs-lookup"><span data-stu-id="e7ba8-112">For a Remote Desktop virtualization (RDV) scenario, this member is **NULL**.</span></span> <span data-ttu-id="e7ba8-113">Per uno scenario RDSH (Desktop remoto Session Host), questo membro contiene il nome del server in cui viene reindirizzata la connessione in ingresso.</span><span class="sxs-lookup"><span data-stu-id="e7ba8-113">For a Remote Desktop session host (RDSH) scenario, this member contains the server name where the incoming connection is redirected.</span></span>

</dd> <dt>

<span data-ttu-id="e7ba8-114">**AddressCount**</span><span class="sxs-lookup"><span data-stu-id="e7ba8-114">**AddressCount**</span></span>
</dt> <dd>

<span data-ttu-id="e7ba8-115">Numero di voci valide nella matrice di **indirizzi** .</span><span class="sxs-lookup"><span data-stu-id="e7ba8-115">The number of valid entries in the **Addresses** array.</span></span>

</dd> <dt>

<span data-ttu-id="e7ba8-116">**Indirizzi**</span><span class="sxs-lookup"><span data-stu-id="e7ba8-116">**Addresses**</span></span>
</dt> <dd>

<span data-ttu-id="e7ba8-117">Matrice di stringhe che contengono gli indirizzi IP in cui vengono reindirizzate le connessioni in ingresso.</span><span class="sxs-lookup"><span data-stu-id="e7ba8-117">An array of strings that contain the IP addresses where the incoming connections are redirected.</span></span> <span data-ttu-id="e7ba8-118">Il numero di elementi validi in questa matrice è specificato nel membro **AddressCount** .</span><span class="sxs-lookup"><span data-stu-id="e7ba8-118">The number of valid elements in this array is specified in the **AddressCount** member.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e7ba8-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e7ba8-119">Requirements</span></span>



| <span data-ttu-id="e7ba8-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="e7ba8-120">Requirement</span></span> | <span data-ttu-id="e7ba8-121">Valore</span><span class="sxs-lookup"><span data-stu-id="e7ba8-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e7ba8-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e7ba8-122">Minimum supported client</span></span><br/> | <span data-ttu-id="e7ba8-123">Windows 8</span><span class="sxs-lookup"><span data-stu-id="e7ba8-123">Windows 8</span></span><br/>                                                                  |
| <span data-ttu-id="e7ba8-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e7ba8-124">Minimum supported server</span></span><br/> | <span data-ttu-id="e7ba8-125">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e7ba8-125">Windows Server 2012</span></span><br/>                                                        |
| <span data-ttu-id="e7ba8-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e7ba8-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="e7ba8-127"><dt>Cbclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="e7ba8-127"><dt>Cbclient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7ba8-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e7ba8-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7ba8-129">**IConnectionBrokerClient::GetTargetInfo**</span><span class="sxs-lookup"><span data-stu-id="e7ba8-129">**IConnectionBrokerClient::GetTargetInfo**</span></span>](iconnectionbrokerclient-gettargetinfo.md)
</dt> </dl>

 

 





