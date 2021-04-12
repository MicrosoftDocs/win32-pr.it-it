---
title: Metodo RdvCopyBaseVmLocally della classe Win32_RdvhManagement
description: Copia una macchina virtuale di base locale in un server host di virtualizzazione Desktop remoto (RDV) specificato.
ms.assetid: 13c0c629-42c6-4689-9740-f13f31688e42
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo RdvCopyBaseVmLocally
- Metodo RdvCopyBaseVmLocally Servizi Desktop remoto, classe Win32_RdvhManagement
- Classe Win32_RdvhManagement Servizi Desktop remoto, metodo RdvCopyBaseVmLocally
topic_type:
- apiref
api_name:
- Win32_RdvhManagement.RdvCopyBaseVmLocally
api_location:
- TSVmHostWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d96e01038a4b41edcf32a6a5a9b353403fa6021
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400880"
---
# <a name="rdvcopybasevmlocally-method-of-the-win32_rdvhmanagement-class"></a><span data-ttu-id="7c8bf-106">Metodo RdvCopyBaseVmLocally della \_ classe RdvhManagement Win32</span><span class="sxs-lookup"><span data-stu-id="7c8bf-106">RdvCopyBaseVmLocally method of the Win32\_RdvhManagement class</span></span>

<span data-ttu-id="7c8bf-107">Copia una macchina virtuale di base locale in un server host di virtualizzazione Desktop remoto (RDV) specificato.</span><span class="sxs-lookup"><span data-stu-id="7c8bf-107">Copies a local base virtual machine to a specified remote desktop virtualization (RDV) host server.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c8bf-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7c8bf-108">Syntax</span></span>


```mof
uint32 RdvCopyBaseVmLocally(
  [in] string BaseVmLocation,
  [in] string FarmName,
  [in] string GoldCacheLocation
);
```



## <a name="parameters"></a><span data-ttu-id="7c8bf-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="7c8bf-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c8bf-110">*BaseVmLocation* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7c8bf-110">*BaseVmLocation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c8bf-111">Posizione della macchina virtuale di base.</span><span class="sxs-lookup"><span data-stu-id="7c8bf-111">The base virtual machine location.</span></span>

</dd> <dt>

<span data-ttu-id="7c8bf-112">*Farmname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7c8bf-112">*FarmName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c8bf-113">Nome della farm host in cui eseguire la copia.</span><span class="sxs-lookup"><span data-stu-id="7c8bf-113">The name of the host farm to copy to.</span></span>

</dd> <dt>

<span data-ttu-id="7c8bf-114">*GoldCacheLocation* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7c8bf-114">*GoldCacheLocation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c8bf-115">Percorso della cache Gold.</span><span class="sxs-lookup"><span data-stu-id="7c8bf-115">The gold cache location.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c8bf-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7c8bf-116">Return value</span></span>

<span data-ttu-id="7c8bf-117">Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="7c8bf-117">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="7c8bf-118">Per un elenco di questi valori, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="7c8bf-118">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c8bf-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7c8bf-119">Requirements</span></span>



| <span data-ttu-id="7c8bf-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c8bf-120">Requirement</span></span> | <span data-ttu-id="7c8bf-121">Valore</span><span class="sxs-lookup"><span data-stu-id="7c8bf-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c8bf-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7c8bf-122">Minimum supported client</span></span><br/> | <span data-ttu-id="7c8bf-123">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="7c8bf-123">None supported</span></span><br/>                                                                  |
| <span data-ttu-id="7c8bf-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7c8bf-124">Minimum supported server</span></span><br/> | <span data-ttu-id="7c8bf-125">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7c8bf-125">Windows Server 2012</span></span><br/>                                                             |
| <span data-ttu-id="7c8bf-126">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="7c8bf-126">Namespace</span></span><br/>                | <span data-ttu-id="7c8bf-127">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="7c8bf-127">Root\\CIMv2\\TerminalServices</span></span><br/>                                                   |
| <span data-ttu-id="7c8bf-128">MOF</span><span class="sxs-lookup"><span data-stu-id="7c8bf-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7c8bf-129"><dt>TSVmHost. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7c8bf-129"><dt>TSVmHost.mof</dt></span></span> </dl>    |
| <span data-ttu-id="7c8bf-130">DLL</span><span class="sxs-lookup"><span data-stu-id="7c8bf-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7c8bf-131"><dt>TSVmHostWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7c8bf-131"><dt>TSVmHostWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c8bf-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7c8bf-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c8bf-133">**\_RdvhManagement Win32**</span><span class="sxs-lookup"><span data-stu-id="7c8bf-133">**Win32\_RdvhManagement**</span></span>](win32-rdvhmanagement.md)
</dt> </dl>

 

 





