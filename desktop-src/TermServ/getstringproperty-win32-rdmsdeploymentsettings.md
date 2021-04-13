---
title: Metodo GetStringProperty della classe Win32_RDMSDeploymentSettings
description: Recupera una proprietà di stringa per le impostazioni di distribuzione di un insieme di desktop virtuali.
ms.assetid: 468ffdea-57a9-4478-adae-3629e4522762
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del Metodo GetStringProperty
- Metodo GetStringProperty Servizi Desktop remoto, classe Win32_RDMSDeploymentSettings
- Classe Win32_RDMSDeploymentSettings Servizi Desktop remoto, Metodo GetStringProperty
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.GetStringProperty
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f26a570becbbae6b0d768c399acd3dd2954ecdc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400458"
---
# <a name="getstringproperty-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="9f157-106">Metodo GetStringProperty della \_ classe RDMSDeploymentSettings Win32</span><span class="sxs-lookup"><span data-stu-id="9f157-106">GetStringProperty method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="9f157-107">Recupera una proprietà di stringa per le impostazioni di distribuzione di un insieme di desktop virtuali.</span><span class="sxs-lookup"><span data-stu-id="9f157-107">Retrieves a string property for the deployment settings of a virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f157-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9f157-108">Syntax</span></span>


```mof
uint32 GetStringProperty(
  [in]  string Key,
  [out] string Value
);
```



## <a name="parameters"></a><span data-ttu-id="9f157-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="9f157-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f157-110">*Chiave* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="9f157-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f157-111">Alias dell'insieme di desktop virtuali.</span><span class="sxs-lookup"><span data-stu-id="9f157-111">The alias to the virtual desktop collection.</span></span>

</dd> <dt>

<span data-ttu-id="9f157-112">*Valore* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="9f157-112">*Value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9f157-113">Stringa che riceve il valore recuperato.</span><span class="sxs-lookup"><span data-stu-id="9f157-113">A string that receives the retrieved value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9f157-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9f157-114">Requirements</span></span>



| <span data-ttu-id="9f157-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="9f157-115">Requirement</span></span> | <span data-ttu-id="9f157-116">Valore</span><span class="sxs-lookup"><span data-stu-id="9f157-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f157-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9f157-117">Minimum supported client</span></span><br/> | <span data-ttu-id="9f157-118">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="9f157-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="9f157-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9f157-119">Minimum supported server</span></span><br/> | <span data-ttu-id="9f157-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9f157-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="9f157-121">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="9f157-121">Namespace</span></span><br/>                | <span data-ttu-id="9f157-122">Radice \\ CIMv2 \\ RDBMS</span><span class="sxs-lookup"><span data-stu-id="9f157-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="9f157-123">MOF</span><span class="sxs-lookup"><span data-stu-id="9f157-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9f157-124"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9f157-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="9f157-125">DLL</span><span class="sxs-lookup"><span data-stu-id="9f157-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9f157-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9f157-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="9f157-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9f157-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f157-128">**\_RDMSDeploymentSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="9f157-128">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





