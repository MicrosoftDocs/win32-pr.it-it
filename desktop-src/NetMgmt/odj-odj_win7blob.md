---
title: ODJ_WIN7BLOB
description: Definizione di ODJ_WIN7BLOB IDL
ms.assetid: 5802e00c-b943-45d8-8298-5c2b4b996b85
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 2083648636bd58c64314ba22852839f89ed4461d
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/14/2020
ms.locfileid: "104339563"
---
# <a name="odj_win7blob-structure"></a><span data-ttu-id="e844a-103">Struttura ODJ_WIN7BLOB</span><span class="sxs-lookup"><span data-stu-id="e844a-103">ODJ_WIN7BLOB structure</span></span>

<span data-ttu-id="e844a-104">Contiene le informazioni di base necessarie per aggiungere un client a un dominio.</span><span class="sxs-lookup"><span data-stu-id="e844a-104">Contains the basic information required to join a client to a domain.</span></span>

## <a name="syntax"></a><span data-ttu-id="e844a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e844a-105">Syntax</span></span>

```C++
typedef struct _ODJ_WIN7BLOB
{
    [string] wchar_t *lpDomain;
    [string] wchar_t *lpMachineName;
    [string] wchar_t *lpMachinePassword;
    ODJ_POLICY_DNS_DOMAIN_INFO  DnsDomainInfo;
    DOMAIN_CONTROLLER_INFOW DcInfo;
    DWORD Options;
} ODJ_WIN7BLOB;
```

## <a name="members"></a><span data-ttu-id="e844a-106">Members</span><span class="sxs-lookup"><span data-stu-id="e844a-106">Members</span></span>

### <a name="lpdomain"></a><span data-ttu-id="e844a-107">lpDomain</span><span class="sxs-lookup"><span data-stu-id="e844a-107">lpDomain</span></span>

<span data-ttu-id="e844a-108">Deve essere impostato sul nome di dominio.</span><span class="sxs-lookup"><span data-stu-id="e844a-108">Must be set to the domain name.</span></span>

### <a name="lpmachinename"></a><span data-ttu-id="e844a-109">lpMachineName</span><span class="sxs-lookup"><span data-stu-id="e844a-109">lpMachineName</span></span>

<span data-ttu-id="e844a-110">Deve essere impostato sul nome del computer.</span><span class="sxs-lookup"><span data-stu-id="e844a-110">Must be set to the machine name.</span></span>

### <a name="lpmachinepassword"></a><span data-ttu-id="e844a-111">lpMachinePassword</span><span class="sxs-lookup"><span data-stu-id="e844a-111">lpMachinePassword</span></span>

<span data-ttu-id="e844a-112">Deve essere impostato su una password non crittografata per l'account del computer identificato da lpMachineName</span><span class="sxs-lookup"><span data-stu-id="e844a-112">Must be set to a cleartext password for the machine account identified by lpMachineName</span></span>

### <a name="dnsdomaininfo"></a><span data-ttu-id="e844a-113">DnsDomainInfo</span><span class="sxs-lookup"><span data-stu-id="e844a-113">DnsDomainInfo</span></span>

<span data-ttu-id="e844a-114">Contiene informazioni sul dominio da unire.</span><span class="sxs-lookup"><span data-stu-id="e844a-114">Contains information about the domain being joined.</span></span>

### <a name="dcinfo"></a><span data-ttu-id="e844a-115">DcInfo</span><span class="sxs-lookup"><span data-stu-id="e844a-115">DcInfo</span></span>

<span data-ttu-id="e844a-116">Contiene informazioni sulla denominazione e sull'indirizzamento del controller di dominio utilizzato per creare l'account del computer Active Directory.</span><span class="sxs-lookup"><span data-stu-id="e844a-116">Contains naming and addressing information about the domain controller that was used to create the machine account Active Directory.</span></span>

### <a name="options"></a><span data-ttu-id="e844a-117">Opzioni</span><span class="sxs-lookup"><span data-stu-id="e844a-117">Options</span></span>

<span data-ttu-id="e844a-118">Deve essere impostato su zero.</span><span class="sxs-lookup"><span data-stu-id="e844a-118">Must be set to zero.</span></span>

## <a name="see-also"></a><span data-ttu-id="e844a-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e844a-119">See also</span></span>

[<span data-ttu-id="e844a-120">**Definizioni IDL di aggiunta al dominio offline**</span><span class="sxs-lookup"><span data-stu-id="e844a-120">**Offline Domain Join IDL Definitions**</span></span>](odj-idl.md)

[<span data-ttu-id="e844a-121">**\_informazioni sul \_ \_ dominio DNS del criterio \_ ODJ**</span><span class="sxs-lookup"><span data-stu-id="e844a-121">**ODJ\_POLICY\_DNS\_DOMAIN\_INFO**</span></span>](odj-odj_policy_dns_domain_info.md)

[<span data-ttu-id="e844a-122">**DOMAIN_CONTROLLER_INFOW**</span><span class="sxs-lookup"><span data-stu-id="e844a-122">**DOMAIN_CONTROLLER_INFOW**</span></span>](/windows/win32/api/dsgetdc/ns-dsgetdc-domain_controller_infow)



