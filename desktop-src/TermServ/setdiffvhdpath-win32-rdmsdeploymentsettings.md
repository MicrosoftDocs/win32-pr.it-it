---
title: Metodo SetDiffVHDPath della classe Win32_RDMSDeploymentSettings
description: Aggiorna il percorso della directory in cui vengono distribuiti i dischi differenze per un insieme di desktop virtuali.
ms.assetid: 665ffbf9-0250-4956-9bce-f5a6714b47e4
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SetDiffVHDPath
- Metodo SetDiffVHDPath Servizi Desktop remoto, classe Win32_RDMSDeploymentSettings
- Classe Win32_RDMSDeploymentSettings Servizi Desktop remoto, metodo SetDiffVHDPath
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.SetDiffVHDPath
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e52d206c9e0cbff19f26e38a2a02f04ea0acc03d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400575"
---
# <a name="setdiffvhdpath-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="235c9-106">Metodo SetDiffVHDPath della \_ classe RDMSDeploymentSettings Win32</span><span class="sxs-lookup"><span data-stu-id="235c9-106">SetDiffVHDPath method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="235c9-107">Aggiorna il percorso della directory in cui vengono distribuiti i dischi differenze per un insieme di desktop virtuali.</span><span class="sxs-lookup"><span data-stu-id="235c9-107">Updates the directory path to which the differencing disks are deployed for a virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="235c9-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="235c9-108">Syntax</span></span>


```mof
uint32 SetDiffVHDPath(
  [in] string DirectoryPath
);
```



## <a name="parameters"></a><span data-ttu-id="235c9-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="235c9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="235c9-110">*DirectoryPath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="235c9-110">*DirectoryPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="235c9-111">Nuovo percorso del disco differenze.</span><span class="sxs-lookup"><span data-stu-id="235c9-111">The new differencing disk path.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="235c9-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="235c9-112">Return value</span></span>

<span data-ttu-id="235c9-113">Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="235c9-113">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="235c9-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="235c9-114">Requirements</span></span>



| <span data-ttu-id="235c9-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="235c9-115">Requirement</span></span> | <span data-ttu-id="235c9-116">Valore</span><span class="sxs-lookup"><span data-stu-id="235c9-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="235c9-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="235c9-117">Minimum supported client</span></span><br/> | <span data-ttu-id="235c9-118">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="235c9-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="235c9-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="235c9-119">Minimum supported server</span></span><br/> | <span data-ttu-id="235c9-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="235c9-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="235c9-121">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="235c9-121">Namespace</span></span><br/>                | <span data-ttu-id="235c9-122">Radice \\ CIMv2 \\ RDBMS</span><span class="sxs-lookup"><span data-stu-id="235c9-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="235c9-123">MOF</span><span class="sxs-lookup"><span data-stu-id="235c9-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="235c9-124"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="235c9-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="235c9-125">DLL</span><span class="sxs-lookup"><span data-stu-id="235c9-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="235c9-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="235c9-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="235c9-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="235c9-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="235c9-128">**\_RDMSDeploymentSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="235c9-128">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





