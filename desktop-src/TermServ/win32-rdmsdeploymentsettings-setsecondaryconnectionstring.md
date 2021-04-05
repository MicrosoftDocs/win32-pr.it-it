---
title: Metodo SetSecondaryConnectionString della classe Win32_RDMSDeploymentSettings
description: Imposta la stringa di connessione secondaria del database a livello di distribuzione.
ms.assetid: 154c495e-564e-4d90-a4ff-de683d41aa73
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SetSecondaryConnectionString
- Metodo SetSecondaryConnectionString Servizi Desktop remoto, classe Win32_RDMSDeploymentSettings
- Classe Win32_RDMSDeploymentSettings Servizi Desktop remoto, metodo SetSecondaryConnectionString
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.SetSecondaryConnectionString
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f8060a6f2676b5599bf44672e79ebf48e64e354
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741103"
---
# <a name="setsecondaryconnectionstring-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="fe953-106">Metodo SetSecondaryConnectionString della \_ classe RDMSDeploymentSettings Win32</span><span class="sxs-lookup"><span data-stu-id="fe953-106">SetSecondaryConnectionString method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="fe953-107">Imposta la stringa di connessione secondaria del database a livello di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="fe953-107">Sets the deployment level database secondary connection string.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe953-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fe953-108">Syntax</span></span>


```mof
uint32 SetSecondaryConnectionString(
  [in] string SecondaryConnectionString
);
```



## <a name="parameters"></a><span data-ttu-id="fe953-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="fe953-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe953-110">*SecondaryConnectionString* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fe953-110">*SecondaryConnectionString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe953-111">Stringa di connessione da impostare</span><span class="sxs-lookup"><span data-stu-id="fe953-111">The connection string to set</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe953-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fe953-112">Return value</span></span>

<span data-ttu-id="fe953-113">Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="fe953-113">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe953-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fe953-114">Requirements</span></span>



| <span data-ttu-id="fe953-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="fe953-115">Requirement</span></span> | <span data-ttu-id="fe953-116">Valore</span><span class="sxs-lookup"><span data-stu-id="fe953-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe953-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fe953-117">Minimum supported client</span></span><br/> | <span data-ttu-id="fe953-118">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="fe953-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="fe953-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fe953-119">Minimum supported server</span></span><br/> | <span data-ttu-id="fe953-120">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="fe953-120">Windows Server 2016</span></span><br/>                                                              |
| <span data-ttu-id="fe953-121">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="fe953-121">Namespace</span></span><br/>                | <span data-ttu-id="fe953-122">Radice \\ CIMV2 \\ RDBMS</span><span class="sxs-lookup"><span data-stu-id="fe953-122">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="fe953-123">MOF</span><span class="sxs-lookup"><span data-stu-id="fe953-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fe953-124"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fe953-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="fe953-125">DLL</span><span class="sxs-lookup"><span data-stu-id="fe953-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fe953-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fe953-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="fe953-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fe953-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe953-128">**\_RDMSDeploymentSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="fe953-128">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





