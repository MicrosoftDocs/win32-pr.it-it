---
title: Metodo GetStringArrayDeploymentSetting della classe Win32_RDMSDeploymentSettings
description: Recupera le impostazioni di distribuzione per un insieme di desktop virtuali.
ms.assetid: ab380618-560e-425b-9bf0-a7de6b30d01a
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo GetStringArrayDeploymentSetting
- Metodo GetStringArrayDeploymentSetting Servizi Desktop remoto, classe Win32_RDMSDeploymentSettings
- Classe Win32_RDMSDeploymentSettings Servizi Desktop remoto, metodo GetStringArrayDeploymentSetting
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.GetStringArrayDeploymentSetting
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9ac0b82441abef8af1b4f6c8e3bd48b89a8cb6c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119275"
---
# <a name="getstringarraydeploymentsetting-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="c01f1-106">Metodo GetStringArrayDeploymentSetting della \_ classe RDMSDeploymentSettings Win32</span><span class="sxs-lookup"><span data-stu-id="c01f1-106">GetStringArrayDeploymentSetting method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="c01f1-107">Recupera le impostazioni di distribuzione per un insieme di desktop virtuali.</span><span class="sxs-lookup"><span data-stu-id="c01f1-107">Retrieves the deployment settings for a virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="c01f1-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c01f1-108">Syntax</span></span>


```mof
uint32 GetStringArrayDeploymentSetting(
  [in]  string Key,
  [out] string Value[]
);
```



## <a name="parameters"></a><span data-ttu-id="c01f1-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="c01f1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c01f1-110">*Chiave* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="c01f1-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c01f1-111">Alias dell'insieme di desktop virtuali.</span><span class="sxs-lookup"><span data-stu-id="c01f1-111">The alias of the virtual desktop collection.</span></span>

</dd> <dt>

<span data-ttu-id="c01f1-112">*Valore* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="c01f1-112">*Value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c01f1-113">Riceve una matrice di stringhe che contiene le impostazioni di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="c01f1-113">Receives an array of strings that contains the deployment settings.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c01f1-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c01f1-114">Requirements</span></span>



| <span data-ttu-id="c01f1-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="c01f1-115">Requirement</span></span> | <span data-ttu-id="c01f1-116">Valore</span><span class="sxs-lookup"><span data-stu-id="c01f1-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="c01f1-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c01f1-117">Minimum supported client</span></span><br/> | <span data-ttu-id="c01f1-118">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="c01f1-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="c01f1-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c01f1-119">Minimum supported server</span></span><br/> | <span data-ttu-id="c01f1-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c01f1-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="c01f1-121">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="c01f1-121">Namespace</span></span><br/>                | <span data-ttu-id="c01f1-122">Radice \\ CIMv2 \\ RDBMS</span><span class="sxs-lookup"><span data-stu-id="c01f1-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="c01f1-123">MOF</span><span class="sxs-lookup"><span data-stu-id="c01f1-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c01f1-124"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c01f1-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="c01f1-125">DLL</span><span class="sxs-lookup"><span data-stu-id="c01f1-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c01f1-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c01f1-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="c01f1-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c01f1-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c01f1-128">**\_RDMSDeploymentSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="c01f1-128">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





