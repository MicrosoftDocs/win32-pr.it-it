---
title: Metodo GetDiffVHDPath della classe Win32_RDMSDeploymentSettings
description: Recupera il percorso della directory in cui vengono distribuiti i dischi differenze per un insieme di desktop virtuali.
ms.assetid: 4340c817-2276-48a1-a856-b4c9e91ea981
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo GetDiffVHDPath
- Metodo GetDiffVHDPath Servizi Desktop remoto, classe Win32_RDMSDeploymentSettings
- Classe Win32_RDMSDeploymentSettings Servizi Desktop remoto, metodo GetDiffVHDPath
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.GetDiffVHDPath
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7391315013cf8487d93b32f645933d14f06db2d6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400322"
---
# <a name="getdiffvhdpath-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="edc00-106">Metodo GetDiffVHDPath della \_ classe RDMSDeploymentSettings Win32</span><span class="sxs-lookup"><span data-stu-id="edc00-106">GetDiffVHDPath method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="edc00-107">Recupera il percorso della directory in cui vengono distribuiti i dischi differenze per un insieme di desktop virtuali.</span><span class="sxs-lookup"><span data-stu-id="edc00-107">Retrieves the directory path to which the differencing disks are deployed for a virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="edc00-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="edc00-108">Syntax</span></span>


```mof
uint32 GetDiffVHDPath(
  [out] string DirectoryPath
);
```



## <a name="parameters"></a><span data-ttu-id="edc00-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="edc00-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="edc00-110">*DirectoryPath* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="edc00-110">*DirectoryPath* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="edc00-111">Riceve il nuovo percorso del disco differenze.</span><span class="sxs-lookup"><span data-stu-id="edc00-111">Receives the new differencing disk path.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="edc00-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="edc00-112">Return value</span></span>

<span data-ttu-id="edc00-113">Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="edc00-113">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="edc00-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="edc00-114">Requirements</span></span>



| <span data-ttu-id="edc00-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="edc00-115">Requirement</span></span> | <span data-ttu-id="edc00-116">Valore</span><span class="sxs-lookup"><span data-stu-id="edc00-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="edc00-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="edc00-117">Minimum supported client</span></span><br/> | <span data-ttu-id="edc00-118">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="edc00-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="edc00-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="edc00-119">Minimum supported server</span></span><br/> | <span data-ttu-id="edc00-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="edc00-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="edc00-121">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="edc00-121">Namespace</span></span><br/>                | <span data-ttu-id="edc00-122">Radice \\ CIMv2 \\ RDBMS</span><span class="sxs-lookup"><span data-stu-id="edc00-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="edc00-123">MOF</span><span class="sxs-lookup"><span data-stu-id="edc00-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="edc00-124"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="edc00-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="edc00-125">DLL</span><span class="sxs-lookup"><span data-stu-id="edc00-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="edc00-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="edc00-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="edc00-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="edc00-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="edc00-128">**\_RDMSDeploymentSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="edc00-128">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





