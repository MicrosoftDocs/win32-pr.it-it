---
title: Metodo GetSecondaryConnectionString della classe Win32_RDMSDeploymentSettings
description: Recupera la stringa di connessione secondaria del database a livello di distribuzione, che può essere utilizzata per supportare la scadenza della password.
ms.assetid: 0de02752-6cbf-4c21-b752-a57ed58aeef1
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo GetSecondaryConnectionString
- Metodo GetSecondaryConnectionString Servizi Desktop remoto, classe Win32_RDMSDeploymentSettings
- Classe Win32_RDMSDeploymentSettings Servizi Desktop remoto, metodo GetSecondaryConnectionString
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.GetSecondaryConnectionString
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2c09f4fcacabbe928fcda00447e252077bd8a51
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340642"
---
# <a name="getsecondaryconnectionstring-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="1c49c-106">Metodo GetSecondaryConnectionString della \_ classe RDMSDeploymentSettings Win32</span><span class="sxs-lookup"><span data-stu-id="1c49c-106">GetSecondaryConnectionString method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="1c49c-107">Recupera la stringa di connessione secondaria del database a livello di distribuzione, che può essere utilizzata per supportare la scadenza della password.</span><span class="sxs-lookup"><span data-stu-id="1c49c-107">Retrieves the deployment-level database secondary connection string, which may be used to support password expiration.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c49c-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1c49c-108">Syntax</span></span>


```mof
uint32 GetSecondaryConnectionString(
  [out] string SecondaryConnectionString
);
```



## <a name="parameters"></a><span data-ttu-id="1c49c-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="1c49c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c49c-110">*SecondaryConnectionString* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="1c49c-110">*SecondaryConnectionString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1c49c-111">Stringa di connessione da recuperare</span><span class="sxs-lookup"><span data-stu-id="1c49c-111">The connection string to retrieve</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c49c-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1c49c-112">Return value</span></span>

<span data-ttu-id="1c49c-113">Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="1c49c-113">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c49c-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1c49c-114">Requirements</span></span>



| <span data-ttu-id="1c49c-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="1c49c-115">Requirement</span></span> | <span data-ttu-id="1c49c-116">Valore</span><span class="sxs-lookup"><span data-stu-id="1c49c-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c49c-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1c49c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="1c49c-118">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="1c49c-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="1c49c-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1c49c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="1c49c-120">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="1c49c-120">Windows Server 2016</span></span><br/>                                                              |
| <span data-ttu-id="1c49c-121">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="1c49c-121">Namespace</span></span><br/>                | <span data-ttu-id="1c49c-122">Radice \\ CIMV2 \\ RDBMS</span><span class="sxs-lookup"><span data-stu-id="1c49c-122">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="1c49c-123">MOF</span><span class="sxs-lookup"><span data-stu-id="1c49c-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1c49c-124"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1c49c-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="1c49c-125">DLL</span><span class="sxs-lookup"><span data-stu-id="1c49c-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1c49c-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1c49c-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="1c49c-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1c49c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c49c-128">**\_RDMSDeploymentSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="1c49c-128">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





