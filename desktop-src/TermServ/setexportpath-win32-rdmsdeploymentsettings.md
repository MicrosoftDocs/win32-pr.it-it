---
title: Metodo SetExportPath della classe Win32_RDMSDeploymentSettings
description: Aggiorna il percorso della directory in cui vengono distribuite le macchine virtuali per un insieme di desktop virtuali.
ms.assetid: e52b79c8-6724-4264-93d5-4a2a14c89b6b
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SetExportPath
- Metodo SetExportPath Servizi Desktop remoto, classe Win32_RDMSDeploymentSettings
- Classe Win32_RDMSDeploymentSettings Servizi Desktop remoto, metodo SetExportPath
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.SetExportPath
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32dbc844aecf86d4c62fada6c5cd68d514a69272
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301516"
---
# <a name="setexportpath-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="2c073-106">Metodo SetExportPath della \_ classe RDMSDeploymentSettings Win32</span><span class="sxs-lookup"><span data-stu-id="2c073-106">SetExportPath method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="2c073-107">Aggiorna il percorso della directory in cui vengono distribuite le macchine virtuali per un insieme di desktop virtuali.</span><span class="sxs-lookup"><span data-stu-id="2c073-107">Updates the directory path to which virtual machines are deployed for a virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c073-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2c073-108">Syntax</span></span>


```mof
uint32 SetExportPath(
  [in] string DirectoryPath
);
```



## <a name="parameters"></a><span data-ttu-id="2c073-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="2c073-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c073-110">*DirectoryPath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2c073-110">*DirectoryPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c073-111">Nuovo percorso della directory.</span><span class="sxs-lookup"><span data-stu-id="2c073-111">The new directory path.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c073-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2c073-112">Return value</span></span>

<span data-ttu-id="2c073-113">Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="2c073-113">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c073-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2c073-114">Requirements</span></span>



| <span data-ttu-id="2c073-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="2c073-115">Requirement</span></span> | <span data-ttu-id="2c073-116">Valore</span><span class="sxs-lookup"><span data-stu-id="2c073-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c073-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2c073-117">Minimum supported client</span></span><br/> | <span data-ttu-id="2c073-118">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="2c073-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="2c073-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2c073-119">Minimum supported server</span></span><br/> | <span data-ttu-id="2c073-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2c073-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="2c073-121">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="2c073-121">Namespace</span></span><br/>                | <span data-ttu-id="2c073-122">Radice \\ CIMv2 \\ RDBMS</span><span class="sxs-lookup"><span data-stu-id="2c073-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="2c073-123">MOF</span><span class="sxs-lookup"><span data-stu-id="2c073-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2c073-124"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2c073-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="2c073-125">DLL</span><span class="sxs-lookup"><span data-stu-id="2c073-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2c073-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2c073-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="2c073-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2c073-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c073-128">**\_RDMSDeploymentSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="2c073-128">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





