---
description: Definisce i valori che determinano come recuperare le credenziali di un account del servizio gestito del gruppo (gMSA).
ms.assetid: 90891448-22F6-497A-A612-3DAB8622C325
title: Enumerazione CRED_FETCH (Secpkg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRED_FETCH
api_type:
- HeaderDef
api_location:
- Secpkg.h
ms.openlocfilehash: 6a7c30f29826b017bc7a3badd796955ec31a1ca7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968010"
---
# <a name="cred_fetch-enumeration"></a><span data-ttu-id="5b3c9-103">\_Enumerazione recupero cred</span><span class="sxs-lookup"><span data-stu-id="5b3c9-103">CRED\_FETCH enumeration</span></span>

<span data-ttu-id="5b3c9-104">Definisce i valori che determinano come recuperare le credenziali di un account del servizio gestito del gruppo (gMSA).</span><span class="sxs-lookup"><span data-stu-id="5b3c9-104">Defines values that determine how to fetch the credential of a Group Managed Service Account (gMSA).</span></span>

## <a name="syntax"></a><span data-ttu-id="5b3c9-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5b3c9-105">Syntax</span></span>


```C++
typedef enum _CRED_FETCH { 
  CredFetchDefault  = 0,
  CredFetchDPAPI    = 1,
  CredFetchForced   = 2
} CRED_FETCH;
```



## <a name="constants"></a><span data-ttu-id="5b3c9-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="5b3c9-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="5b3c9-107"><span id="CredFetchDefault"></span><span id="credfetchdefault"></span><span id="CREDFETCHDEFAULT"></span>**CredFetchDefault**</span><span class="sxs-lookup"><span data-stu-id="5b3c9-107"><span id="CredFetchDefault"></span><span id="credfetchdefault"></span><span id="CREDFETCHDEFAULT"></span>**CredFetchDefault**</span></span>
</dt> <dd>

<span data-ttu-id="5b3c9-108">Indica che il sistema operativo deve prima tentare di recuperare la password dalla cache locale.</span><span class="sxs-lookup"><span data-stu-id="5b3c9-108">Signifies that the operating system should first attempt to retrieve the password from the local cache.</span></span> <span data-ttu-id="5b3c9-109">Se è il momento di recuperare la password, il sistema operativo deve contattare un controller di dominio per la password.</span><span class="sxs-lookup"><span data-stu-id="5b3c9-109">If it is time to fetch the password, then the operating system should contact a domain controller for the password.</span></span> <span data-ttu-id="5b3c9-110">Se l'operazione ha esito negativo, restituire le password memorizzate nella cache con il valore di stato success.</span><span class="sxs-lookup"><span data-stu-id="5b3c9-110">If that fails, then return any cached passwords with the status value of success.</span></span>

</dd> <dt>

<span data-ttu-id="5b3c9-111"><span id="CredFetchDPAPI"></span><span id="credfetchdpapi"></span><span id="CREDFETCHDPAPI"></span>**CredFetchDPAPI**</span><span class="sxs-lookup"><span data-stu-id="5b3c9-111"><span id="CredFetchDPAPI"></span><span id="credfetchdpapi"></span><span id="CREDFETCHDPAPI"></span>**CredFetchDPAPI**</span></span>
</dt> <dd>

<span data-ttu-id="5b3c9-112">Restituisce le credenziali DPAPI locali al chiamante.</span><span class="sxs-lookup"><span data-stu-id="5b3c9-112">Returns the local DPAPI credential to the caller.</span></span> <span data-ttu-id="5b3c9-113">Gli SSP ( [*Security Support Provider*](/windows/desktop/SecGloss/s-gly) ) in genere non richiedono l'utilizzo di questa enumerazione.</span><span class="sxs-lookup"><span data-stu-id="5b3c9-113">[*Security support providers*](/windows/desktop/SecGloss/s-gly) (SSPs) generally would not require the use of this enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="5b3c9-114"><span id="CredFetchForced"></span><span id="credfetchforced"></span><span id="CREDFETCHFORCED"></span>**CredFetchForced**</span><span class="sxs-lookup"><span data-stu-id="5b3c9-114"><span id="CredFetchForced"></span><span id="credfetchforced"></span><span id="CREDFETCHFORCED"></span>**CredFetchForced**</span></span>
</dt> <dd>

<span data-ttu-id="5b3c9-115">Impone al sistema operativo di provare a leggere la password dal controller di dominio.</span><span class="sxs-lookup"><span data-stu-id="5b3c9-115">Forces the operating system to attempt to read the password from the domain controller.</span></span> <span data-ttu-id="5b3c9-116">Durante il tempo di rollover della password, è possibile che la password sia stata modificata nel controller di dominio e in altri host membro, ma l'host membro gMSA riconosce la password come ancora valida.</span><span class="sxs-lookup"><span data-stu-id="5b3c9-116">During the password rollover time, the password may have changed at the domain controller and other member hosts, but the gMSA member host recognizes the password as still valid.</span></span> <span data-ttu-id="5b3c9-117">Ciò può verificarsi a causa di problemi di sfasamento dell'orologio tra controller di dominio diversi.</span><span class="sxs-lookup"><span data-stu-id="5b3c9-117">This can happen due to clock skew issues between different domain controllers.</span></span> <span data-ttu-id="5b3c9-118">Quando si specifica questo valore, il sistema operativo determina se è possibile che si verifichi una modifica della password a causa dello sfasamento dell'orologio e, in caso affermativo, recupera la password.</span><span class="sxs-lookup"><span data-stu-id="5b3c9-118">When this value is specified, the operating system determines if there could be a possible password change due to clock skew, and if so, retrieves the password.</span></span> <span data-ttu-id="5b3c9-119">In caso contrario, vengono restituite le credenziali memorizzate nella cache.</span><span class="sxs-lookup"><span data-stu-id="5b3c9-119">Otherwise, the cached credential is returned.</span></span> <span data-ttu-id="5b3c9-120">Se non sono presenti credenziali memorizzate nella cache, il sistema operativo tenta di ottenerne uno dal controller di dominio.</span><span class="sxs-lookup"><span data-stu-id="5b3c9-120">If there is no cached credential, then the operating system attempts to get one from the domain controller.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5b3c9-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5b3c9-121">Requirements</span></span>



| <span data-ttu-id="5b3c9-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b3c9-122">Requirement</span></span> | <span data-ttu-id="5b3c9-123">Valore</span><span class="sxs-lookup"><span data-stu-id="5b3c9-123">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="5b3c9-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5b3c9-124">Minimum supported client</span></span><br/> | <span data-ttu-id="5b3c9-125">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="5b3c9-125">Windows 8 \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="5b3c9-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5b3c9-126">Minimum supported server</span></span><br/> | <span data-ttu-id="5b3c9-127">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="5b3c9-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="5b3c9-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5b3c9-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="5b3c9-129"><dt>Secpkg. h</dt></span><span class="sxs-lookup"><span data-stu-id="5b3c9-129"><dt>Secpkg.h</dt></span></span> </dl> |



 

