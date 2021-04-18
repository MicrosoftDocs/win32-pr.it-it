---
title: Metodo SetBaseVHDPath della classe Win32_RDMSDeploymentSettings
description: Recupera il percorso di base della directory in cui vengono distribuiti i VHD dell'insieme di desktop virtuali. | Metodo SetBaseVHDPath della classe Win32_RDMSDeploymentSettings
ms.assetid: 1ea4cd93-ef17-4ec9-82f9-382c549f189c
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SetBaseVHDPath
- Metodo SetBaseVHDPath Servizi Desktop remoto, classe Win32_RDMSDeploymentSettings
- Classe Win32_RDMSDeploymentSettings Servizi Desktop remoto, metodo SetBaseVHDPath
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.SetBaseVHDPath
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7907640a9641cff3c94475318bf499415b25184
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321205"
---
# <a name="setbasevhdpath-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="d2cd3-107">Metodo SetBaseVHDPath della \_ classe RDMSDeploymentSettings Win32</span><span class="sxs-lookup"><span data-stu-id="d2cd3-107">SetBaseVHDPath method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="d2cd3-108">Recupera il percorso di base della directory in cui vengono distribuiti i VHD dell'insieme di desktop virtuali.</span><span class="sxs-lookup"><span data-stu-id="d2cd3-108">Retrieves the base path to the directory to which VHDs of the virtual desktop collection are deployed.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2cd3-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d2cd3-109">Syntax</span></span>


```mof
uint32 SetBaseVHDPath(
  [in] string DirectoryPath
);
```



## <a name="parameters"></a><span data-ttu-id="d2cd3-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="d2cd3-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2cd3-111">*DirectoryPath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d2cd3-111">*DirectoryPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2cd3-112">Nuovo percorso di distribuzione del disco rigido virtuale.</span><span class="sxs-lookup"><span data-stu-id="d2cd3-112">The new VHD deployment path.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2cd3-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d2cd3-113">Return value</span></span>

<span data-ttu-id="d2cd3-114">Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="d2cd3-114">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2cd3-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d2cd3-115">Requirements</span></span>



| <span data-ttu-id="d2cd3-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2cd3-116">Requirement</span></span> | <span data-ttu-id="d2cd3-117">Valore</span><span class="sxs-lookup"><span data-stu-id="d2cd3-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2cd3-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d2cd3-118">Minimum supported client</span></span><br/> | <span data-ttu-id="d2cd3-119">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="d2cd3-119">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="d2cd3-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d2cd3-120">Minimum supported server</span></span><br/> | <span data-ttu-id="d2cd3-121">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d2cd3-121">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="d2cd3-122">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="d2cd3-122">Namespace</span></span><br/>                | <span data-ttu-id="d2cd3-123">Radice \\ CIMv2 \\ RDBMS</span><span class="sxs-lookup"><span data-stu-id="d2cd3-123">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="d2cd3-124">MOF</span><span class="sxs-lookup"><span data-stu-id="d2cd3-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d2cd3-125"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d2cd3-125"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="d2cd3-126">DLL</span><span class="sxs-lookup"><span data-stu-id="d2cd3-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d2cd3-127"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d2cd3-127"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="d2cd3-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d2cd3-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2cd3-129">**\_RDMSDeploymentSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="d2cd3-129">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





