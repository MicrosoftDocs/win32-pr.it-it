---
title: Metodo GetBaseVHDPath della classe Win32_RDMSDeploymentSettings
description: Recupera il percorso di base della directory in cui vengono distribuiti i VHD dell'insieme di desktop virtuali. | Metodo GetBaseVHDPath della classe Win32_RDMSDeploymentSettings
ms.assetid: d3629a08-ef16-4aab-b74b-f837a8ba00d0
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo GetBaseVHDPath
- Metodo GetBaseVHDPath Servizi Desktop remoto, classe Win32_RDMSDeploymentSettings
- Classe Win32_RDMSDeploymentSettings Servizi Desktop remoto, metodo GetBaseVHDPath
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.GetBaseVHDPath
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 595c6459148a0270bed2328c70e15ef74a69acf3
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "103969153"
---
# <a name="getbasevhdpath-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="a7480-107">Metodo GetBaseVHDPath della \_ classe RDMSDeploymentSettings Win32</span><span class="sxs-lookup"><span data-stu-id="a7480-107">GetBaseVHDPath method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="a7480-108">Recupera il percorso di base della directory in cui vengono distribuiti i VHD dell'insieme di desktop virtuali.</span><span class="sxs-lookup"><span data-stu-id="a7480-108">Retrieves the base path to the directory to which VHDs of the virtual desktop collection are deployed.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7480-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a7480-109">Syntax</span></span>


```mof
uint32 GetBaseVHDPath(
  [out] string DirectoryPath
);
```



## <a name="parameters"></a><span data-ttu-id="a7480-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="a7480-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7480-111">*DirectoryPath* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="a7480-111">*DirectoryPath* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a7480-112">Riceve il percorso di distribuzione del disco rigido virtuale.</span><span class="sxs-lookup"><span data-stu-id="a7480-112">Receives the VHD deployment path.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a7480-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a7480-113">Return value</span></span>

<span data-ttu-id="a7480-114">Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="a7480-114">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7480-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a7480-115">Requirements</span></span>



| <span data-ttu-id="a7480-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="a7480-116">Requirement</span></span> | <span data-ttu-id="a7480-117">Valore</span><span class="sxs-lookup"><span data-stu-id="a7480-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7480-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a7480-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a7480-119">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="a7480-119">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="a7480-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a7480-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a7480-121">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a7480-121">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="a7480-122">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="a7480-122">Namespace</span></span><br/>                | <span data-ttu-id="a7480-123">Radice \\ CIMv2 \\ RDBMS</span><span class="sxs-lookup"><span data-stu-id="a7480-123">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="a7480-124">MOF</span><span class="sxs-lookup"><span data-stu-id="a7480-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a7480-125"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a7480-125"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="a7480-126">DLL</span><span class="sxs-lookup"><span data-stu-id="a7480-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a7480-127"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a7480-127"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="a7480-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a7480-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7480-129">**\_RDMSDeploymentSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="a7480-129">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





