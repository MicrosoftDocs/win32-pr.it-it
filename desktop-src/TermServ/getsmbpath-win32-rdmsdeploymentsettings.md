---
title: Metodo GetSMBPath della classe Win32_RDMSDeploymentSettings
description: Recupera il percorso UNC della condivisione SMB a cui vengono distribuite le macchine virtuali dell'insieme di desktop virtuali.
ms.assetid: 0a5d3c11-6a77-48f7-a3ea-6f82725ff01f
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo GetSMBPath
- Metodo GetSMBPath Servizi Desktop remoto, classe Win32_RDMSDeploymentSettings
- Classe Win32_RDMSDeploymentSettings Servizi Desktop remoto, metodo GetSMBPath
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.GetSMBPath
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa1738faf82a6405018495dd762ba9585daa3e1b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400940"
---
# <a name="getsmbpath-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="a221e-106">Metodo GetSMBPath della \_ classe RDMSDeploymentSettings Win32</span><span class="sxs-lookup"><span data-stu-id="a221e-106">GetSMBPath method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="a221e-107">Recupera il percorso UNC della condivisione SMB a cui vengono distribuite le macchine virtuali dell'insieme di desktop virtuali.</span><span class="sxs-lookup"><span data-stu-id="a221e-107">Retrieves the UNC path to the SMB share to which virtual machines of the virtual desktop collection are deployed.</span></span>

## <a name="syntax"></a><span data-ttu-id="a221e-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a221e-108">Syntax</span></span>


```mof
uint32 GetSMBPath(
  [out] string DirectoryPath
);
```



## <a name="parameters"></a><span data-ttu-id="a221e-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="a221e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a221e-110">*DirectoryPath* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="a221e-110">*DirectoryPath* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a221e-111">Riceve un percorso formattato UNC della condivisione SMB.</span><span class="sxs-lookup"><span data-stu-id="a221e-111">Receives a UNC formatted path to the SMB share.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a221e-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a221e-112">Return value</span></span>

<span data-ttu-id="a221e-113">Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="a221e-113">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="a221e-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a221e-114">Requirements</span></span>



| <span data-ttu-id="a221e-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="a221e-115">Requirement</span></span> | <span data-ttu-id="a221e-116">Valore</span><span class="sxs-lookup"><span data-stu-id="a221e-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="a221e-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a221e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a221e-118">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="a221e-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="a221e-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a221e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a221e-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a221e-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="a221e-121">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="a221e-121">Namespace</span></span><br/>                | <span data-ttu-id="a221e-122">Radice \\ CIMv2 \\ RDBMS</span><span class="sxs-lookup"><span data-stu-id="a221e-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="a221e-123">MOF</span><span class="sxs-lookup"><span data-stu-id="a221e-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a221e-124"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a221e-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="a221e-125">DLL</span><span class="sxs-lookup"><span data-stu-id="a221e-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a221e-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a221e-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="a221e-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a221e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a221e-128">**\_RDMSDeploymentSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="a221e-128">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





