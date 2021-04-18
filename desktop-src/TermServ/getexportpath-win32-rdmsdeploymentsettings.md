---
title: Metodo GetExportPath della classe Win32_RDMSDeploymentSettings
description: Recupera il percorso della directory in cui vengono distribuite le macchine virtuali per un insieme di desktop virtuali.
ms.assetid: 8df79e31-b960-46ae-b49c-8052b356e1a8
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo GetExportPath
- Metodo GetExportPath Servizi Desktop remoto, classe Win32_RDMSDeploymentSettings
- Classe Win32_RDMSDeploymentSettings Servizi Desktop remoto, metodo GetExportPath
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.GetExportPath
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: baf96d1d71554f1b8ea310759d36d0918a511cbf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301117"
---
# <a name="getexportpath-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="4082c-106">Metodo GetExportPath della \_ classe RDMSDeploymentSettings Win32</span><span class="sxs-lookup"><span data-stu-id="4082c-106">GetExportPath method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="4082c-107">Recupera il percorso della directory in cui vengono distribuite le macchine virtuali per un insieme di desktop virtuali.</span><span class="sxs-lookup"><span data-stu-id="4082c-107">Retrieves the directory path to which virtual machines are deployed for a virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="4082c-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4082c-108">Syntax</span></span>


```mof
uint32 GetExportPath(
  [out] string DirectoryPath
);
```



## <a name="parameters"></a><span data-ttu-id="4082c-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="4082c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4082c-110">*DirectoryPath* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="4082c-110">*DirectoryPath* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4082c-111">Riceve il percorso della directory.</span><span class="sxs-lookup"><span data-stu-id="4082c-111">Receives the directory path.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4082c-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4082c-112">Return value</span></span>

<span data-ttu-id="4082c-113">Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="4082c-113">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="4082c-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4082c-114">Requirements</span></span>



| <span data-ttu-id="4082c-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="4082c-115">Requirement</span></span> | <span data-ttu-id="4082c-116">Valore</span><span class="sxs-lookup"><span data-stu-id="4082c-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="4082c-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4082c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="4082c-118">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="4082c-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="4082c-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4082c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="4082c-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4082c-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="4082c-121">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="4082c-121">Namespace</span></span><br/>                | <span data-ttu-id="4082c-122">Radice \\ CIMv2 \\ RDBMS</span><span class="sxs-lookup"><span data-stu-id="4082c-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="4082c-123">MOF</span><span class="sxs-lookup"><span data-stu-id="4082c-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4082c-124"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4082c-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="4082c-125">DLL</span><span class="sxs-lookup"><span data-stu-id="4082c-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4082c-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4082c-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="4082c-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4082c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4082c-128">**\_RDMSDeploymentSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="4082c-128">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





