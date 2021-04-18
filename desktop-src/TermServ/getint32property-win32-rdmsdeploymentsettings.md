---
title: Metodo GetInt32Property della classe Win32_RDMSDeploymentSettings (Microsoft. Diagnostics. appanalysis. h)
description: Recupera una proprietà integer per le impostazioni di distribuzione di un insieme di desktop virtuali.
ms.assetid: 6b8174bb-ffb7-4699-a3fb-d32ab0b202fc
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo GetInt32Property
- Metodo GetInt32Property Servizi Desktop remoto, classe Win32_RDMSDeploymentSettings
- Classe Win32_RDMSDeploymentSettings Servizi Desktop remoto, metodo GetInt32Property
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.GetInt32Property
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f96374c610084c8ef7973d4ac4db603d9c28cff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301901"
---
# <a name="getint32property-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="c404d-106">Metodo GetInt32Property della \_ classe RDMSDeploymentSettings Win32</span><span class="sxs-lookup"><span data-stu-id="c404d-106">GetInt32Property method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="c404d-107">Recupera una proprietà integer per le impostazioni di distribuzione di un insieme di desktop virtuali.</span><span class="sxs-lookup"><span data-stu-id="c404d-107">Retrieves an integer property for the deployment settings of a virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="c404d-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c404d-108">Syntax</span></span>


```mof
uint32 GetInt32Property(
  [in]  string Key,
  [out] sint32 Value
);
```



## <a name="parameters"></a><span data-ttu-id="c404d-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="c404d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c404d-110">*Chiave* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="c404d-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c404d-111">Alias dell'insieme di desktop virtuali.</span><span class="sxs-lookup"><span data-stu-id="c404d-111">The alias to the virtual desktop collection.</span></span>

</dd> <dt>

<span data-ttu-id="c404d-112">*Valore* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="c404d-112">*Value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c404d-113">Intero che riceve il valore recuperato.</span><span class="sxs-lookup"><span data-stu-id="c404d-113">An integer that receives the retrieved value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c404d-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c404d-114">Requirements</span></span>



| <span data-ttu-id="c404d-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="c404d-115">Requirement</span></span> | <span data-ttu-id="c404d-116">Valore</span><span class="sxs-lookup"><span data-stu-id="c404d-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c404d-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c404d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="c404d-118">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="c404d-118">None supported</span></span><br/>                                                                                      |
| <span data-ttu-id="c404d-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c404d-119">Minimum supported server</span></span><br/> | <span data-ttu-id="c404d-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c404d-120">Windows Server 2012</span></span><br/>                                                                                 |
| <span data-ttu-id="c404d-121">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="c404d-121">Namespace</span></span><br/>                | <span data-ttu-id="c404d-122">Radice \\ CIMv2 \\ RDBMS</span><span class="sxs-lookup"><span data-stu-id="c404d-122">Root\\CIMv2\\rdms</span></span><br/>                                                                                   |
| <span data-ttu-id="c404d-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c404d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="c404d-124"><dt>Microsoft. Diagnostics. appanalysis. h</dt></span><span class="sxs-lookup"><span data-stu-id="c404d-124"><dt>Microsoft.diagnostics.appanalysis.h</dt></span></span> </dl> |
| <span data-ttu-id="c404d-125">MOF</span><span class="sxs-lookup"><span data-stu-id="c404d-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c404d-126"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c404d-126"><dt>RDManagement.mof</dt></span></span> </dl>                    |
| <span data-ttu-id="c404d-127">DLL</span><span class="sxs-lookup"><span data-stu-id="c404d-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c404d-128"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c404d-128"><dt>RDMS.dll</dt></span></span> </dl>                            |



## <a name="see-also"></a><span data-ttu-id="c404d-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c404d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c404d-130">**\_RDMSDeploymentSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="c404d-130">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





