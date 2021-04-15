---
title: Metodo StopService della classe MicrosoftDNS_Server
description: Il metodo StopService arresta il server DNS.
ms.assetid: 80637d5b-e43a-4710-b3ab-eec246587788
keywords:
- DNS del metodo StopService
- DNS del metodo StopService, classe MicrosoftDNS_Server
- Classe MicrosoftDNS_Server DNS, metodo StopService
topic_type:
- apiref
api_name:
- MicrosoftDNS_Server.StopService
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f811533c66185304c5c674fdfff2eda8cf5bef69
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477267"
---
# <a name="stopservice-method-of-the-microsoftdns_server-class"></a><span data-ttu-id="79c62-106">Metodo StopService della \_ classe server MicrosoftDNS</span><span class="sxs-lookup"><span data-stu-id="79c62-106">StopService method of the MicrosoftDNS\_Server class</span></span>

<span data-ttu-id="79c62-107">Il metodo **StopService** arresta il server DNS.</span><span class="sxs-lookup"><span data-stu-id="79c62-107">The **StopService** method stops the DNS Server.</span></span>

## <a name="syntax"></a><span data-ttu-id="79c62-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="79c62-108">Syntax</span></span>


```mof
uint32 StopService();
```



## <a name="parameters"></a><span data-ttu-id="79c62-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="79c62-109">Parameters</span></span>

<span data-ttu-id="79c62-110">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="79c62-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="79c62-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="79c62-111">Return value</span></span>

<span data-ttu-id="79c62-112">ERRORE \_ indica che il servizio è stato arrestato correttamente.</span><span class="sxs-lookup"><span data-stu-id="79c62-112">ERROR\_SUCCESS indicates the service was successfully stopped.</span></span> <span data-ttu-id="79c62-113">Qualsiasi altro valore è un codice di errore.</span><span class="sxs-lookup"><span data-stu-id="79c62-113">Any other value is an error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="79c62-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="79c62-114">Requirements</span></span>



| <span data-ttu-id="79c62-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="79c62-115">Requirement</span></span> | <span data-ttu-id="79c62-116">Valore</span><span class="sxs-lookup"><span data-stu-id="79c62-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="79c62-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="79c62-117">Minimum supported client</span></span><br/> | <span data-ttu-id="79c62-118">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="79c62-118">None supported</span></span><br/>                                                              |
| <span data-ttu-id="79c62-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="79c62-119">Minimum supported server</span></span><br/> | <span data-ttu-id="79c62-120">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="79c62-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="79c62-121">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="79c62-121">Namespace</span></span><br/>                | <span data-ttu-id="79c62-122">\\MicrosoftDNS radice</span><span class="sxs-lookup"><span data-stu-id="79c62-122">Root\\MicrosoftDNS</span></span><br/>                                                          |
| <span data-ttu-id="79c62-123">MOF</span><span class="sxs-lookup"><span data-stu-id="79c62-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="79c62-124"><dt>Dnsprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="79c62-124"><dt>Dnsprov.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79c62-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="79c62-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79c62-126">**\_Server MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="79c62-126">**MicrosoftDNS\_Server**</span></span>](microsoftdns-server.md)
</dt> <dt>

[<span data-ttu-id="79c62-127">**Metodo StartService della \_ classe server MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="79c62-127">**StartService Method of the MicrosoftDNS\_Server Class**</span></span>](microsoftdns-server-startservice.md)
</dt> <dt>

[<span data-ttu-id="79c62-128">**Metodo StartScavenging della \_ classe server MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="79c62-128">**StartScavenging Method of the MicrosoftDNS\_Server Class**</span></span>](microsoftdns-server-startscavenging.md)
</dt> <dt>

[<span data-ttu-id="79c62-129">**Metodo getdistinguishname della \_ classe server MicrosoftDNS**</span><span class="sxs-lookup"><span data-stu-id="79c62-129">**GetDistinguishedName Method of the MicrosoftDNS\_Server Class**</span></span>](microsoftdns-server-getdistinguishedname.md)
</dt> </dl>

 

 





