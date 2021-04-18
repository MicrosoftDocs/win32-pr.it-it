---
title: Metodo SetClientAccessName della classe Win32_RDMSEnvironment
description: Aggiorna il nome del record di risorse Domain Name System (DNS) di un ambiente Desktop remoto Management Services (RDBMS).
ms.assetid: bbce3fc1-d2c5-4874-bdd0-be27fb5981d1
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SetClientAccessName
- Metodo SetClientAccessName Servizi Desktop remoto, classe Win32_RDMSEnvironment
- Classe Win32_RDMSEnvironment Servizi Desktop remoto, metodo SetClientAccessName
topic_type:
- apiref
api_name:
- Win32_RDMSEnvironment.SetClientAccessName
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13f9087fe2c2139833baeb21bc62da508c6e5989
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302596"
---
# <a name="setclientaccessname-method-of-the-win32_rdmsenvironment-class"></a><span data-ttu-id="e07ab-106">Metodo SetClientAccessName della \_ classe RDMSEnvironment Win32</span><span class="sxs-lookup"><span data-stu-id="e07ab-106">SetClientAccessName method of the Win32\_RDMSEnvironment class</span></span>

<span data-ttu-id="e07ab-107">Aggiorna il nome del record di risorse Domain Name System (DNS) di un ambiente Desktop remoto Management Services (RDBMS).</span><span class="sxs-lookup"><span data-stu-id="e07ab-107">Updates the Domain Name System (DNS) resource record (RR) name of an Remote Desktop Management Services (RDMS) environment.</span></span>

## <a name="syntax"></a><span data-ttu-id="e07ab-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e07ab-108">Syntax</span></span>


```mof
uint32 SetClientAccessName(
  [in] string ClientAccessName
);
```



## <a name="parameters"></a><span data-ttu-id="e07ab-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="e07ab-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e07ab-110">*ClientAccessName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e07ab-110">*ClientAccessName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e07ab-111">Nome del nuovo RR.</span><span class="sxs-lookup"><span data-stu-id="e07ab-111">The new RR name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e07ab-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e07ab-112">Return value</span></span>

<span data-ttu-id="e07ab-113">Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="e07ab-113">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="e07ab-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e07ab-114">Requirements</span></span>



| <span data-ttu-id="e07ab-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="e07ab-115">Requirement</span></span> | <span data-ttu-id="e07ab-116">Valore</span><span class="sxs-lookup"><span data-stu-id="e07ab-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="e07ab-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e07ab-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e07ab-118">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="e07ab-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="e07ab-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e07ab-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e07ab-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e07ab-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="e07ab-121">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="e07ab-121">Namespace</span></span><br/>                | <span data-ttu-id="e07ab-122">Radice \\ CIMv2 \\ RDBMS</span><span class="sxs-lookup"><span data-stu-id="e07ab-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="e07ab-123">MOF</span><span class="sxs-lookup"><span data-stu-id="e07ab-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e07ab-124"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e07ab-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="e07ab-125">DLL</span><span class="sxs-lookup"><span data-stu-id="e07ab-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e07ab-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e07ab-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="e07ab-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e07ab-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e07ab-128">**\_RDMSEnvironment Win32**</span><span class="sxs-lookup"><span data-stu-id="e07ab-128">**Win32\_RDMSEnvironment**</span></span>](win32-rdmsenvironment.md)
</dt> </dl>

 

 





