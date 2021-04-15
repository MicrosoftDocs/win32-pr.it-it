---
title: Metodo GetActiveServer della classe Win32_RDMSEnvironment
description: Recupera il nome di dominio completo (FQDN) dell'ambiente Desktop remoto Management Services (RDBMS).
ms.assetid: 87e25d11-de1d-41d1-974d-2871dde444b5
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo GetActiveServer
- Metodo GetActiveServer Servizi Desktop remoto, classe Win32_RDMSEnvironment
- Classe Win32_RDMSEnvironment Servizi Desktop remoto, metodo GetActiveServer
topic_type:
- apiref
api_name:
- Win32_RDMSEnvironment.GetActiveServer
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4265315e3ed2de87e564adab87c023401bbd55e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477458"
---
# <a name="getactiveserver-method-of-the-win32_rdmsenvironment-class"></a><span data-ttu-id="2ebc7-106">Metodo GetActiveServer della \_ classe RDMSEnvironment Win32</span><span class="sxs-lookup"><span data-stu-id="2ebc7-106">GetActiveServer method of the Win32\_RDMSEnvironment class</span></span>

<span data-ttu-id="2ebc7-107">Recupera il nome di dominio completo (FQDN) dell'ambiente Desktop remoto Management Services (RDBMS).</span><span class="sxs-lookup"><span data-stu-id="2ebc7-107">Retrieves the fully qualified domain name (FQDN) of the Remote Desktop Management Services (RDMS) environment.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ebc7-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2ebc7-108">Syntax</span></span>


```mof
uint32 GetActiveServer(
  [out] string ServerName
);
```



## <a name="parameters"></a><span data-ttu-id="2ebc7-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="2ebc7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ebc7-110">*Nomeserver* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="2ebc7-110">*ServerName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2ebc7-111">Riceve il nome di dominio completo recuperato.</span><span class="sxs-lookup"><span data-stu-id="2ebc7-111">Receives the retrieved FQDN.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ebc7-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2ebc7-112">Return value</span></span>

<span data-ttu-id="2ebc7-113">Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="2ebc7-113">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ebc7-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2ebc7-114">Requirements</span></span>



| <span data-ttu-id="2ebc7-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="2ebc7-115">Requirement</span></span> | <span data-ttu-id="2ebc7-116">Valore</span><span class="sxs-lookup"><span data-stu-id="2ebc7-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ebc7-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2ebc7-117">Minimum supported client</span></span><br/> | <span data-ttu-id="2ebc7-118">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="2ebc7-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="2ebc7-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2ebc7-119">Minimum supported server</span></span><br/> | <span data-ttu-id="2ebc7-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2ebc7-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="2ebc7-121">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="2ebc7-121">Namespace</span></span><br/>                | <span data-ttu-id="2ebc7-122">Radice \\ CIMv2 \\ RDBMS</span><span class="sxs-lookup"><span data-stu-id="2ebc7-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="2ebc7-123">MOF</span><span class="sxs-lookup"><span data-stu-id="2ebc7-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2ebc7-124"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2ebc7-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="2ebc7-125">DLL</span><span class="sxs-lookup"><span data-stu-id="2ebc7-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2ebc7-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2ebc7-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="2ebc7-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2ebc7-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ebc7-128">**\_RDMSEnvironment Win32**</span><span class="sxs-lookup"><span data-stu-id="2ebc7-128">**Win32\_RDMSEnvironment**</span></span>](win32-rdmsenvironment.md)
</dt> </dl>

 

 





