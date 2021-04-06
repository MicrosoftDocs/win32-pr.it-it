---
title: Metodo SetStringArrayDeploymentSetting della classe Win32_RDMSDeploymentSettings
description: Aggiorna le impostazioni di distribuzione per un insieme di desktop virtuali.
ms.assetid: 386594bd-a793-4e5d-ad2c-217951bee9f6
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SetStringArrayDeploymentSetting
- Metodo SetStringArrayDeploymentSetting Servizi Desktop remoto, classe Win32_RDMSDeploymentSettings
- Classe Win32_RDMSDeploymentSettings Servizi Desktop remoto, metodo SetStringArrayDeploymentSetting
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.SetStringArrayDeploymentSetting
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: beb5ecc6d1238b739f8fe19d02e96ba427ed09b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743490"
---
# <a name="setstringarraydeploymentsetting-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="98537-106">Metodo SetStringArrayDeploymentSetting della \_ classe RDMSDeploymentSettings Win32</span><span class="sxs-lookup"><span data-stu-id="98537-106">SetStringArrayDeploymentSetting method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="98537-107">Aggiorna le impostazioni di distribuzione per un insieme di desktop virtuali.</span><span class="sxs-lookup"><span data-stu-id="98537-107">Updates the deployment settings for a virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="98537-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="98537-108">Syntax</span></span>


```mof
uint32 SetStringArrayDeploymentSetting(
  [in] string Key,
  [in] string Value[]
);
```



## <a name="parameters"></a><span data-ttu-id="98537-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="98537-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98537-110">*Chiave* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="98537-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="98537-111">Alias dell'insieme di desktop virtuali.</span><span class="sxs-lookup"><span data-stu-id="98537-111">The alias of the virtual desktop collection.</span></span>

</dd> <dt>

<span data-ttu-id="98537-112">*Valore* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="98537-112">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="98537-113">Matrice di stringhe che contiene le nuove impostazioni di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="98537-113">An array of strings that contains the new deployment settings.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="98537-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="98537-114">Requirements</span></span>



| <span data-ttu-id="98537-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="98537-115">Requirement</span></span> | <span data-ttu-id="98537-116">Valore</span><span class="sxs-lookup"><span data-stu-id="98537-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="98537-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="98537-117">Minimum supported client</span></span><br/> | <span data-ttu-id="98537-118">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="98537-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="98537-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="98537-119">Minimum supported server</span></span><br/> | <span data-ttu-id="98537-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="98537-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="98537-121">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="98537-121">Namespace</span></span><br/>                | <span data-ttu-id="98537-122">Radice \\ CIMv2 \\ RDBMS</span><span class="sxs-lookup"><span data-stu-id="98537-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="98537-123">MOF</span><span class="sxs-lookup"><span data-stu-id="98537-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="98537-124"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="98537-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="98537-125">DLL</span><span class="sxs-lookup"><span data-stu-id="98537-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="98537-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="98537-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="98537-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="98537-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98537-128">**\_RDMSDeploymentSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="98537-128">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





