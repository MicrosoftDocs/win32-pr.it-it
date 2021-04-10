---
title: Metodo SetSMBPath della classe Win32_RDMSDeploymentSettings
description: Aggiorna il percorso UNC della condivisione SMB a cui vengono distribuite le macchine virtuali dell'insieme di desktop virtuali.
ms.assetid: 0b0b5b17-7b52-41e5-b9c6-c5f3e51c7853
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SetSMBPath
- Metodo SetSMBPath Servizi Desktop remoto, classe Win32_RDMSDeploymentSettings
- Classe Win32_RDMSDeploymentSettings Servizi Desktop remoto, metodo SetSMBPath
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.SetSMBPath
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d40598a3217ff1ca7c6082b3af09097352962309
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964500"
---
# <a name="setsmbpath-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="577a5-106">Metodo SetSMBPath della \_ classe RDMSDeploymentSettings Win32</span><span class="sxs-lookup"><span data-stu-id="577a5-106">SetSMBPath method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="577a5-107">Aggiorna il percorso UNC della condivisione SMB a cui vengono distribuite le macchine virtuali dell'insieme di desktop virtuali.</span><span class="sxs-lookup"><span data-stu-id="577a5-107">Updates the UNC path to the SMB share to which virtual machines of the virtual desktop collection are deployed.</span></span>

## <a name="syntax"></a><span data-ttu-id="577a5-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="577a5-108">Syntax</span></span>


```mof
uint32 SetSMBPath(
  [in] string DirectoryPath
);
```



## <a name="parameters"></a><span data-ttu-id="577a5-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="577a5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="577a5-110">*DirectoryPath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="577a5-110">*DirectoryPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="577a5-111">Nuovo percorso della condivisione SMB, in formato UNC.</span><span class="sxs-lookup"><span data-stu-id="577a5-111">The new path to the SMB share, in UNC format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="577a5-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="577a5-112">Return value</span></span>

<span data-ttu-id="577a5-113">Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="577a5-113">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="577a5-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="577a5-114">Requirements</span></span>



| <span data-ttu-id="577a5-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="577a5-115">Requirement</span></span> | <span data-ttu-id="577a5-116">Valore</span><span class="sxs-lookup"><span data-stu-id="577a5-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="577a5-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="577a5-117">Minimum supported client</span></span><br/> | <span data-ttu-id="577a5-118">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="577a5-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="577a5-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="577a5-119">Minimum supported server</span></span><br/> | <span data-ttu-id="577a5-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="577a5-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="577a5-121">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="577a5-121">Namespace</span></span><br/>                | <span data-ttu-id="577a5-122">Radice \\ CIMv2 \\ RDBMS</span><span class="sxs-lookup"><span data-stu-id="577a5-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="577a5-123">MOF</span><span class="sxs-lookup"><span data-stu-id="577a5-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="577a5-124"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="577a5-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="577a5-125">DLL</span><span class="sxs-lookup"><span data-stu-id="577a5-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="577a5-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="577a5-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="577a5-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="577a5-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="577a5-128">**\_RDMSDeploymentSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="577a5-128">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





