---
title: Metodo GetClientAccessName della classe Win32_RDMSEnvironment
description: Recupera il nome del record di risorse Domain Name System (DNS) dell'ambiente Desktop remoto Management Services (RDBMS).
ms.assetid: 16f9d00d-a398-4a73-a641-ac552ba6a9d3
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo GetClientAccessName
- Metodo GetClientAccessName Servizi Desktop remoto, classe Win32_RDMSEnvironment
- Classe Win32_RDMSEnvironment Servizi Desktop remoto, metodo GetClientAccessName
topic_type:
- apiref
api_name:
- Win32_RDMSEnvironment.GetClientAccessName
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f54662cf1f27c53f3bf69398a203bfdfce1e53c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301119"
---
# <a name="getclientaccessname-method-of-the-win32_rdmsenvironment-class"></a><span data-ttu-id="eb9aa-106">Metodo GetClientAccessName della \_ classe RDMSEnvironment Win32</span><span class="sxs-lookup"><span data-stu-id="eb9aa-106">GetClientAccessName method of the Win32\_RDMSEnvironment class</span></span>

<span data-ttu-id="eb9aa-107">Recupera il nome del record di risorse Domain Name System (DNS) dell'ambiente Desktop remoto Management Services (RDBMS).</span><span class="sxs-lookup"><span data-stu-id="eb9aa-107">Retrieves the Domain Name System (DNS) resource record (RR) name of the Remote Desktop Management Services (RDMS) environment.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb9aa-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="eb9aa-108">Syntax</span></span>


```mof
uint32 GetClientAccessName(
  [out] string ClientAccessName
);
```



## <a name="parameters"></a><span data-ttu-id="eb9aa-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="eb9aa-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb9aa-110">*ClientAccessName* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="eb9aa-110">*ClientAccessName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="eb9aa-111">Riceve il nome RR recuperato.</span><span class="sxs-lookup"><span data-stu-id="eb9aa-111">Receives the retrieved RR name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb9aa-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="eb9aa-112">Return value</span></span>

<span data-ttu-id="eb9aa-113">Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="eb9aa-113">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb9aa-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="eb9aa-114">Requirements</span></span>



| <span data-ttu-id="eb9aa-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="eb9aa-115">Requirement</span></span> | <span data-ttu-id="eb9aa-116">Valore</span><span class="sxs-lookup"><span data-stu-id="eb9aa-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb9aa-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="eb9aa-117">Minimum supported client</span></span><br/> | <span data-ttu-id="eb9aa-118">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="eb9aa-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="eb9aa-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="eb9aa-119">Minimum supported server</span></span><br/> | <span data-ttu-id="eb9aa-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="eb9aa-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="eb9aa-121">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="eb9aa-121">Namespace</span></span><br/>                | <span data-ttu-id="eb9aa-122">Radice \\ CIMv2 \\ RDBMS</span><span class="sxs-lookup"><span data-stu-id="eb9aa-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="eb9aa-123">MOF</span><span class="sxs-lookup"><span data-stu-id="eb9aa-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="eb9aa-124"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="eb9aa-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="eb9aa-125">DLL</span><span class="sxs-lookup"><span data-stu-id="eb9aa-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eb9aa-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eb9aa-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="eb9aa-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="eb9aa-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb9aa-128">**\_RDMSEnvironment Win32**</span><span class="sxs-lookup"><span data-stu-id="eb9aa-128">**Win32\_RDMSEnvironment**</span></span>](win32-rdmsenvironment.md)
</dt> </dl>

 

 





