---
title: Classe Win32_RDMSEnvironment
description: Gestisce un ambiente Desktop remoto Management Services (RDBMS).
ms.assetid: 8a3b10c1-d01d-4e52-8915-29159cc406cc
ms.tgt_platform: multiple
keywords:
- Classe Win32_RDMSEnvironment Servizi Desktop remoto
- Classe Win32_RDMSEnvironment Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- Win32_RDMSEnvironment
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a78acb964471844be74481d1ddfa2d4cf56a173
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301449"
---
# <a name="win32_rdmsenvironment-class"></a><span data-ttu-id="6f81d-105">Win32 \_ RDMSEnvironment (classe)</span><span class="sxs-lookup"><span data-stu-id="6f81d-105">Win32\_RDMSEnvironment class</span></span>

<span data-ttu-id="6f81d-106">Gestisce un ambiente Desktop remoto Management Services (RDBMS).</span><span class="sxs-lookup"><span data-stu-id="6f81d-106">Manages a Remote Desktop Management Services (RDMS) environment.</span></span>

<span data-ttu-id="6f81d-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="6f81d-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f81d-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6f81d-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSEnvironment
{
};
```

## <a name="members"></a><span data-ttu-id="6f81d-109">Members</span><span class="sxs-lookup"><span data-stu-id="6f81d-109">Members</span></span>

<span data-ttu-id="6f81d-110">La classe **Win32 \_ RDMSEnvironment** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="6f81d-110">The **Win32\_RDMSEnvironment** class has these types of members:</span></span>

-   [<span data-ttu-id="6f81d-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="6f81d-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="6f81d-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="6f81d-112">Methods</span></span>

<span data-ttu-id="6f81d-113">La classe **Win32 \_ RDMSEnvironment** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="6f81d-113">The **Win32\_RDMSEnvironment** class has these methods.</span></span>



| <span data-ttu-id="6f81d-114">Metodo</span><span class="sxs-lookup"><span data-stu-id="6f81d-114">Method</span></span>                                                                   | <span data-ttu-id="6f81d-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6f81d-115">Description</span></span>                                                                                          |
|:-------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6f81d-116">**GetActiveServer**</span><span class="sxs-lookup"><span data-stu-id="6f81d-116">**GetActiveServer**</span></span>](getactiveserver-win32-rdmsenvironment.md)         | <span data-ttu-id="6f81d-117">Recupera il nome di dominio completo (FQDN) dell'ambiente RDBMS.</span><span class="sxs-lookup"><span data-stu-id="6f81d-117">Retrieves the fully qualified domain name (FQDN) of the RDMS environment.</span></span><br/>                 |
| [<span data-ttu-id="6f81d-118">**GetClientAccessName**</span><span class="sxs-lookup"><span data-stu-id="6f81d-118">**GetClientAccessName**</span></span>](getclientaccessname-win32-rdmsenvironment.md) | <span data-ttu-id="6f81d-119">Recupera il nome del record di risorse (DNS) di Domain Name System (RR) dell'ambiente RDBMS.</span><span class="sxs-lookup"><span data-stu-id="6f81d-119">Retrieves the Domain Name System (DNS) resource record (RR) name of the RDMS environment.</span></span><br/> |
| [<span data-ttu-id="6f81d-120">**SetActiveServer**</span><span class="sxs-lookup"><span data-stu-id="6f81d-120">**SetActiveServer**</span></span>](setactiveserver-win32-rdmsenvironment.md)         | <span data-ttu-id="6f81d-121">Imposta il nome di dominio completo dell'ambiente RDBMS sul nodo corrente.</span><span class="sxs-lookup"><span data-stu-id="6f81d-121">Sets the FQDN of the RDMS environment to the current node.</span></span><br/>                                |
| [<span data-ttu-id="6f81d-122">**SetClientAccessName**</span><span class="sxs-lookup"><span data-stu-id="6f81d-122">**SetClientAccessName**</span></span>](setclientaccessname-win32-rdmsenvironment.md) | <span data-ttu-id="6f81d-123">Aggiorna il nome RR DNS dell'ambiente RDBMS.</span><span class="sxs-lookup"><span data-stu-id="6f81d-123">Updates the DNS RR name of the RDMS environment.</span></span><br/>                                          |



 

## <a name="requirements"></a><span data-ttu-id="6f81d-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6f81d-124">Requirements</span></span>



| <span data-ttu-id="6f81d-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f81d-125">Requirement</span></span> | <span data-ttu-id="6f81d-126">Valore</span><span class="sxs-lookup"><span data-stu-id="6f81d-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f81d-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6f81d-127">Minimum supported client</span></span><br/> | <span data-ttu-id="6f81d-128">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="6f81d-128">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="6f81d-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6f81d-129">Minimum supported server</span></span><br/> | <span data-ttu-id="6f81d-130">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6f81d-130">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="6f81d-131">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="6f81d-131">Namespace</span></span><br/>                | <span data-ttu-id="6f81d-132">Radice \\ CIMV2 \\ RDBMS</span><span class="sxs-lookup"><span data-stu-id="6f81d-132">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="6f81d-133">MOF</span><span class="sxs-lookup"><span data-stu-id="6f81d-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6f81d-134"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6f81d-134"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="6f81d-135">DLL</span><span class="sxs-lookup"><span data-stu-id="6f81d-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6f81d-136"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6f81d-136"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="6f81d-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6f81d-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f81d-138">Provider di Desktop remoto Management Services</span><span class="sxs-lookup"><span data-stu-id="6f81d-138">Remote Desktop Management Services Provider</span></span>](rdms-api-reference.md)
</dt> </dl>

 

 





