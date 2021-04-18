---
title: Metodo SetInt32Property della classe Win32_RDMSDeploymentSettings
description: Aggiorna una proprietà integer per le impostazioni di distribuzione di un insieme di desktop virtuali.
ms.assetid: c5e6dbd5-7db7-4409-bf53-c2680e4a5319
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SetInt32Property
- Metodo SetInt32Property Servizi Desktop remoto, classe Win32_RDMSDeploymentSettings
- Classe Win32_RDMSDeploymentSettings Servizi Desktop remoto, metodo SetInt32Property
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.SetInt32Property
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fecdc42031514d5219fc03172b951602ad021ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302448"
---
# <a name="setint32property-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="dc9d9-106">Metodo SetInt32Property della \_ classe RDMSDeploymentSettings Win32</span><span class="sxs-lookup"><span data-stu-id="dc9d9-106">SetInt32Property method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="dc9d9-107">Aggiorna una proprietà integer per le impostazioni di distribuzione di un insieme di desktop virtuali.</span><span class="sxs-lookup"><span data-stu-id="dc9d9-107">Updates an integer property for the deployment settings of a virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc9d9-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dc9d9-108">Syntax</span></span>


```mof
uint32 SetInt32Property(
  [in] string Key,
  [in] sint32 Value
);
```



## <a name="parameters"></a><span data-ttu-id="dc9d9-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="dc9d9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc9d9-110">*Chiave* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="dc9d9-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc9d9-111">Alias dell'insieme di desktop virtuali.</span><span class="sxs-lookup"><span data-stu-id="dc9d9-111">The alias to the virtual desktop collection.</span></span>

</dd> <dt>

<span data-ttu-id="dc9d9-112">*Valore* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="dc9d9-112">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc9d9-113">Nuovo valore della proprietà.</span><span class="sxs-lookup"><span data-stu-id="dc9d9-113">The new property value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dc9d9-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dc9d9-114">Requirements</span></span>



| <span data-ttu-id="dc9d9-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="dc9d9-115">Requirement</span></span> | <span data-ttu-id="dc9d9-116">Valore</span><span class="sxs-lookup"><span data-stu-id="dc9d9-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc9d9-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dc9d9-117">Minimum supported client</span></span><br/> | <span data-ttu-id="dc9d9-118">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="dc9d9-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="dc9d9-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dc9d9-119">Minimum supported server</span></span><br/> | <span data-ttu-id="dc9d9-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="dc9d9-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="dc9d9-121">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="dc9d9-121">Namespace</span></span><br/>                | <span data-ttu-id="dc9d9-122">Radice \\ CIMv2 \\ RDBMS</span><span class="sxs-lookup"><span data-stu-id="dc9d9-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="dc9d9-123">MOF</span><span class="sxs-lookup"><span data-stu-id="dc9d9-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dc9d9-124"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dc9d9-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="dc9d9-125">DLL</span><span class="sxs-lookup"><span data-stu-id="dc9d9-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dc9d9-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dc9d9-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="dc9d9-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dc9d9-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc9d9-128">**\_RDMSDeploymentSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="dc9d9-128">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





