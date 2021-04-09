---
title: Metodo SetStringProperty della classe Win32_RDMSDeploymentSettings (CertEnroll. h)
description: Aggiorna una proprietà di stringa per le impostazioni di distribuzione di un insieme di desktop virtuali.
ms.assetid: 500ab1cb-7336-47a8-adee-790976ea30fe
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del Metodo SetStringProperty
- Metodo SetStringProperty Servizi Desktop remoto, classe Win32_RDMSDeploymentSettings
- Classe Win32_RDMSDeploymentSettings Servizi Desktop remoto, Metodo SetStringProperty
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.SetStringProperty
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 138f6d91ed428caabf8da69e3d958675f879dd15
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120387"
---
# <a name="setstringproperty-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="8c5af-106">Metodo SetStringProperty della \_ classe RDMSDeploymentSettings Win32</span><span class="sxs-lookup"><span data-stu-id="8c5af-106">SetStringProperty method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="8c5af-107">Aggiorna una proprietà di stringa per le impostazioni di distribuzione di un insieme di desktop virtuali.</span><span class="sxs-lookup"><span data-stu-id="8c5af-107">Updates a string property for the deployment settings of a virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c5af-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8c5af-108">Syntax</span></span>


```mof
uint32 SetStringProperty(
  [in] string Key,
  [in] string Value
);
```



## <a name="parameters"></a><span data-ttu-id="8c5af-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="8c5af-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c5af-110">*Chiave* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="8c5af-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c5af-111">Alias dell'insieme di desktop virtuali.</span><span class="sxs-lookup"><span data-stu-id="8c5af-111">The alias to the virtual desktop collection.</span></span>

</dd> <dt>

<span data-ttu-id="8c5af-112">*Valore* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="8c5af-112">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c5af-113">Nuovo valore della proprietà.</span><span class="sxs-lookup"><span data-stu-id="8c5af-113">The new property value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8c5af-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8c5af-114">Requirements</span></span>



| <span data-ttu-id="8c5af-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c5af-115">Requirement</span></span> | <span data-ttu-id="8c5af-116">Valore</span><span class="sxs-lookup"><span data-stu-id="8c5af-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c5af-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8c5af-117">Minimum supported client</span></span><br/> | <span data-ttu-id="8c5af-118">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="8c5af-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="8c5af-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8c5af-119">Minimum supported server</span></span><br/> | <span data-ttu-id="8c5af-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8c5af-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="8c5af-121">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="8c5af-121">Namespace</span></span><br/>                | <span data-ttu-id="8c5af-122">Radice \\ CIMv2 \\ RDBMS</span><span class="sxs-lookup"><span data-stu-id="8c5af-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="8c5af-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8c5af-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="8c5af-124"><dt>CertEnroll. h</dt></span><span class="sxs-lookup"><span data-stu-id="8c5af-124"><dt>Certenroll.h</dt></span></span> </dl>     |
| <span data-ttu-id="8c5af-125">MOF</span><span class="sxs-lookup"><span data-stu-id="8c5af-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8c5af-126"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8c5af-126"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="8c5af-127">DLL</span><span class="sxs-lookup"><span data-stu-id="8c5af-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8c5af-128"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8c5af-128"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="8c5af-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8c5af-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c5af-130">**\_RDMSDeploymentSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="8c5af-130">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





