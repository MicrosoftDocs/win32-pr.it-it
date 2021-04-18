---
title: Metodo StartService della classe MicrosoftDNS_Server
description: Il metodo StartService avvia il server DNS.
ms.assetid: f6343a34-9d1b-4f82-897e-289650af6be9
keywords:
- DNS del metodo StartService
- DNS del metodo StartService, classe MicrosoftDNS_Server
- Classe MicrosoftDNS_Server DNS, metodo StartService
topic_type:
- apiref
api_name:
- MicrosoftDNS_Server.StartService
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2e103b3d2648bf2c061eb047090cfdfeb907518
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301832"
---
# <a name="startservice-method-of-the-microsoftdns_server-class"></a><span data-ttu-id="79969-106">Metodo StartService della \_ classe server MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="79969-106">StartService method of the MicrosoftDNS\_Server class</span></span>

<span data-ttu-id="79969-107">Il metodo **StartService** avvia il server DNS.</span><span class="sxs-lookup"><span data-stu-id="79969-107">The **StartService** method starts the DNS Server.</span></span>

## <a name="syntax"></a><span data-ttu-id="79969-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="79969-108">Syntax</span></span>


```mof
uint32 StartService();
```



## <a name="parameters"></a><span data-ttu-id="79969-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="79969-109">Parameters</span></span>

<span data-ttu-id="79969-110">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="79969-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="79969-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="79969-111">Return value</span></span>

<span data-ttu-id="79969-112">ERRORE \_ con esito positivo indica che il servizio è stato avviato correttamente.</span><span class="sxs-lookup"><span data-stu-id="79969-112">ERROR\_SUCCESS indicates the service was successfully started.</span></span> <span data-ttu-id="79969-113">Qualsiasi altro valore è un codice di errore.</span><span class="sxs-lookup"><span data-stu-id="79969-113">Any other value is an error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="79969-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="79969-114">Requirements</span></span>



| <span data-ttu-id="79969-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="79969-115">Requirement</span></span> | <span data-ttu-id="79969-116">Valore</span><span class="sxs-lookup"><span data-stu-id="79969-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="79969-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="79969-117">Minimum supported client</span></span><br/> | <span data-ttu-id="79969-118">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="79969-118">None supported</span></span><br/>                                                              |
| <span data-ttu-id="79969-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="79969-119">Minimum supported server</span></span><br/> | <span data-ttu-id="79969-120">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="79969-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="79969-121">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="79969-121">Namespace</span></span><br/>                | <span data-ttu-id="79969-122">\\MicrosoftDNS radice</span><span class="sxs-lookup"><span data-stu-id="79969-122">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="79969-123">MOF</span><span class="sxs-lookup"><span data-stu-id="79969-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="79969-124"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="79969-124"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79969-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="79969-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79969-126">**\_Server MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="79969-126">**MicrosoftDNS\_Server**</span></span>](microsoftdns-server.md)
</dt> <dt>

[<span data-ttu-id="79969-127">**Metodo StopService della \_ classe server MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="79969-127">**StopService Method of the MicrosoftDNS\_Server Class**</span></span>](microsoftdns-server-stopservice.md)
</dt> <dt>

[<span data-ttu-id="79969-128">**Metodo StartScavenging della \_ classe server MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="79969-128">**StartScavenging Method of the MicrosoftDNS\_Server Class**</span></span>](microsoftdns-server-startscavenging.md)
</dt> <dt>

[<span data-ttu-id="79969-129">**Metodo getdistinguishname della \_ classe server MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="79969-129">**GetDistinguishedName Method of the MicrosoftDNS\_Server Class**</span></span>](microsoftdns-server-getdistinguishedname.md)
</dt> </dl>

 

 





