---
title: Metodo GetConnectionString della classe Win32_RDMSDeploymentSettings
description: Recupera la stringa di connessione del database a livello di distribuzione.
ms.assetid: 91a90883-9b87-42e5-af52-90226f0344bf
ms.tgt_platform: multiple
keywords:
- Metodo GetConnectionString Servizi Desktop remoto
- Metodo GetConnectionString Servizi Desktop remoto, classe Win32_RDMSDeploymentSettings
- Classe Win32_RDMSDeploymentSettings Servizi Desktop remoto, metodo GetConnectionString
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.GetConnectionString
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6476c938f62e0cd0e1f9d034c89fded50994946
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477081"
---
# <a name="getconnectionstring-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="b68be-106">Metodo GetConnectionString della classe Win32 \_ RDMSDeploymentSettings</span><span class="sxs-lookup"><span data-stu-id="b68be-106">GetConnectionString method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="b68be-107">Recupera la stringa di connessione del database a livello di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="b68be-107">Retrieves the deployment-level database connection string.</span></span>

## <a name="syntax"></a><span data-ttu-id="b68be-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b68be-108">Syntax</span></span>


```mof
uint32 GetConnectionString(
  [out] string ConnectionString
);
```



## <a name="parameters"></a><span data-ttu-id="b68be-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="b68be-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b68be-110">*ConnectionString* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b68be-110">*ConnectionString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b68be-111">Stringa di connessione</span><span class="sxs-lookup"><span data-stu-id="b68be-111">The connection string</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b68be-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b68be-112">Return value</span></span>

<span data-ttu-id="b68be-113">Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="b68be-113">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="b68be-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b68be-114">Requirements</span></span>



| <span data-ttu-id="b68be-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="b68be-115">Requirement</span></span> | <span data-ttu-id="b68be-116">Valore</span><span class="sxs-lookup"><span data-stu-id="b68be-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="b68be-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b68be-117">Minimum supported client</span></span><br/> | <span data-ttu-id="b68be-118">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="b68be-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="b68be-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b68be-119">Minimum supported server</span></span><br/> | <span data-ttu-id="b68be-120">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="b68be-120">Windows Server 2016</span></span><br/>                                                              |
| <span data-ttu-id="b68be-121">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b68be-121">Namespace</span></span><br/>                | <span data-ttu-id="b68be-122">Radice \\ CIMV2 \\ RDBMS</span><span class="sxs-lookup"><span data-stu-id="b68be-122">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="b68be-123">MOF</span><span class="sxs-lookup"><span data-stu-id="b68be-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b68be-124"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b68be-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="b68be-125">DLL</span><span class="sxs-lookup"><span data-stu-id="b68be-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b68be-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b68be-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="b68be-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b68be-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b68be-128">**\_RDMSDeploymentSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="b68be-128">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





