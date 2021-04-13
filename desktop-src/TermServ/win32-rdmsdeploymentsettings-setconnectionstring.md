---
title: Metodo seconnectionstring della classe Win32_RDMSDeploymentSettings
description: Imposta la stringa di connessione del database a livello di distribuzione.
ms.assetid: c8902ab9-72a6-4d69-ab22-f6074205deb4
ms.tgt_platform: multiple
keywords:
- Metodo seconnectionstring Servizi Desktop remoto
- Metodo seconnectionstring Servizi Desktop remoto, classe Win32_RDMSDeploymentSettings
- Classe Win32_RDMSDeploymentSettings Servizi Desktop remoto, metodo seconnectionstring
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.SetConnectionString
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10ccb3f618f6a08dcb95bb7dc04c1494be6a7b5a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400518"
---
# <a name="setconnectionstring-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="29bc0-106">Metodo seconnectionstring della classe Win32 \_ RDMSDeploymentSettings</span><span class="sxs-lookup"><span data-stu-id="29bc0-106">SetConnectionString method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="29bc0-107">Imposta la stringa di connessione del database a livello di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="29bc0-107">Sets the deployment-level database connection string.</span></span>

## <a name="syntax"></a><span data-ttu-id="29bc0-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="29bc0-108">Syntax</span></span>


```mof
uint32 SetConnectionString(
  [in] string ConnectionString
);
```



## <a name="parameters"></a><span data-ttu-id="29bc0-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="29bc0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29bc0-110">*ConnectionString* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="29bc0-110">*ConnectionString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29bc0-111">Stringa di connessione da impostare</span><span class="sxs-lookup"><span data-stu-id="29bc0-111">The connection string to set</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29bc0-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="29bc0-112">Return value</span></span>

<span data-ttu-id="29bc0-113">Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="29bc0-113">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="29bc0-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="29bc0-114">Requirements</span></span>



| <span data-ttu-id="29bc0-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="29bc0-115">Requirement</span></span> | <span data-ttu-id="29bc0-116">Valore</span><span class="sxs-lookup"><span data-stu-id="29bc0-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="29bc0-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="29bc0-117">Minimum supported client</span></span><br/> | <span data-ttu-id="29bc0-118">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="29bc0-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="29bc0-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="29bc0-119">Minimum supported server</span></span><br/> | <span data-ttu-id="29bc0-120">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="29bc0-120">Windows Server 2016</span></span><br/>                                                              |
| <span data-ttu-id="29bc0-121">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="29bc0-121">Namespace</span></span><br/>                | <span data-ttu-id="29bc0-122">Radice \\ CIMV2 \\ RDBMS</span><span class="sxs-lookup"><span data-stu-id="29bc0-122">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="29bc0-123">MOF</span><span class="sxs-lookup"><span data-stu-id="29bc0-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="29bc0-124"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="29bc0-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="29bc0-125">DLL</span><span class="sxs-lookup"><span data-stu-id="29bc0-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="29bc0-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="29bc0-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="29bc0-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="29bc0-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29bc0-128">**\_RDMSDeploymentSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="29bc0-128">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





