---
title: Metodo RemoveDeploymentSetting della classe Win32_RDMSDeploymentSettings
description: Elimina le impostazioni di distribuzione per un insieme di desktop virtuali.
ms.assetid: 68e102a3-8f3f-4997-bdf0-c2ae3640ed42
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo RemoveDeploymentSetting
- Metodo RemoveDeploymentSetting Servizi Desktop remoto, classe Win32_RDMSDeploymentSettings
- Classe Win32_RDMSDeploymentSettings Servizi Desktop remoto, metodo RemoveDeploymentSetting
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.RemoveDeploymentSetting
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 336b93f86d6b96074341dde4851813b26eb66fe2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874534"
---
# <a name="removedeploymentsetting-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="546b6-106">Metodo RemoveDeploymentSetting della \_ classe RDMSDeploymentSettings Win32</span><span class="sxs-lookup"><span data-stu-id="546b6-106">RemoveDeploymentSetting method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="546b6-107">Elimina le impostazioni di distribuzione per un insieme di desktop virtuali.</span><span class="sxs-lookup"><span data-stu-id="546b6-107">Deletes the deployment settings for a virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="546b6-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="546b6-108">Syntax</span></span>


```mof
uint32 RemoveDeploymentSetting(
  [in] string Key
);
```



## <a name="parameters"></a><span data-ttu-id="546b6-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="546b6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="546b6-110">*Chiave* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="546b6-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="546b6-111">Alias dell'insieme di desktop virtuali.</span><span class="sxs-lookup"><span data-stu-id="546b6-111">The alias of the virtual desktop collection.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="546b6-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="546b6-112">Requirements</span></span>



| <span data-ttu-id="546b6-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="546b6-113">Requirement</span></span> | <span data-ttu-id="546b6-114">Valore</span><span class="sxs-lookup"><span data-stu-id="546b6-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="546b6-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="546b6-115">Minimum supported client</span></span><br/> | <span data-ttu-id="546b6-116">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="546b6-116">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="546b6-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="546b6-117">Minimum supported server</span></span><br/> | <span data-ttu-id="546b6-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="546b6-118">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="546b6-119">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="546b6-119">Namespace</span></span><br/>                | <span data-ttu-id="546b6-120">Radice \\ CIMv2 \\ RDBMS</span><span class="sxs-lookup"><span data-stu-id="546b6-120">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="546b6-121">MOF</span><span class="sxs-lookup"><span data-stu-id="546b6-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="546b6-122"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="546b6-122"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="546b6-123">DLL</span><span class="sxs-lookup"><span data-stu-id="546b6-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="546b6-124"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="546b6-124"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="546b6-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="546b6-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="546b6-126">**\_RDMSDeploymentSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="546b6-126">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





