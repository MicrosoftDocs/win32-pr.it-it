---
title: Metodo StartScavenging della classe MicrosoftDNS_Server
description: Il metodo StartScavenging avvia lo scavenging dei record non aggiornati nelle zone soggette allo scavenging.
ms.assetid: ee1bc0e0-9334-4971-a524-4bb8a9015b5b
keywords:
- DNS del metodo StartScavenging
- DNS del metodo StartScavenging, classe MicrosoftDNS_Server
- Classe MicrosoftDNS_Server DNS, metodo StartScavenging
topic_type:
- apiref
api_name:
- MicrosoftDNS_Server.StartScavenging
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c8e1927ed069d3e3e3cf27fd94b1ffd54e6bb2d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964370"
---
# <a name="startscavenging-method-of-the-microsoftdns_server-class"></a><span data-ttu-id="96a64-106">Metodo StartScavenging della \_ classe server MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="96a64-106">StartScavenging method of the MicrosoftDNS\_Server class</span></span>

<span data-ttu-id="96a64-107">Il metodo **StartScavenging** avvia lo scavenging dei record non aggiornati nelle zone soggette allo scavenging.</span><span class="sxs-lookup"><span data-stu-id="96a64-107">The **StartScavenging** method starts scavenging stale records in the zones subjected to scavenging.</span></span>

## <a name="syntax"></a><span data-ttu-id="96a64-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="96a64-108">Syntax</span></span>


```mof
uint32 StartScavenging();
```



## <a name="parameters"></a><span data-ttu-id="96a64-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="96a64-109">Parameters</span></span>

<span data-ttu-id="96a64-110">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="96a64-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="96a64-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="96a64-111">Return value</span></span>

<span data-ttu-id="96a64-112">ERRORE \_ indica che l'operazione di scavenging è stata avviata correttamente.</span><span class="sxs-lookup"><span data-stu-id="96a64-112">ERROR\_SUCCESS indicates the scavenging was successfully started.</span></span> <span data-ttu-id="96a64-113">Qualsiasi altro valore è un codice di errore.</span><span class="sxs-lookup"><span data-stu-id="96a64-113">Any other value is an error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="96a64-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="96a64-114">Requirements</span></span>



| <span data-ttu-id="96a64-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="96a64-115">Requirement</span></span> | <span data-ttu-id="96a64-116">Valore</span><span class="sxs-lookup"><span data-stu-id="96a64-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="96a64-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="96a64-117">Minimum supported client</span></span><br/> | <span data-ttu-id="96a64-118">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="96a64-118">None supported</span></span><br/>                                                              |
| <span data-ttu-id="96a64-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="96a64-119">Minimum supported server</span></span><br/> | <span data-ttu-id="96a64-120">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="96a64-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="96a64-121">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="96a64-121">Namespace</span></span><br/>                | <span data-ttu-id="96a64-122">\\MicrosoftDNS radice</span><span class="sxs-lookup"><span data-stu-id="96a64-122">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="96a64-123">MOF</span><span class="sxs-lookup"><span data-stu-id="96a64-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="96a64-124"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="96a64-124"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96a64-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="96a64-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96a64-126">**\_Server MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="96a64-126">**MicrosoftDNS\_Server**</span></span>](microsoftdns-server.md)
</dt> <dt>

[<span data-ttu-id="96a64-127">**Metodo StartService della \_ classe server MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="96a64-127">**StartService Method of the MicrosoftDNS\_Server Class**</span></span>](microsoftdns-server-startservice.md)
</dt> <dt>

[<span data-ttu-id="96a64-128">**Metodo StopService della \_ classe server MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="96a64-128">**StopService Method of the MicrosoftDNS\_Server Class**</span></span>](microsoftdns-server-stopservice.md)
</dt> <dt>

[<span data-ttu-id="96a64-129">**Metodo getdistinguishname della \_ classe server MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="96a64-129">**GetDistinguishedName Method of the MicrosoftDNS\_Server Class**</span></span>](microsoftdns-server-getdistinguishedname.md)
</dt> </dl>

 

 





