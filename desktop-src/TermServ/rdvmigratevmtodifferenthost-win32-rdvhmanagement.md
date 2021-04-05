---
title: Metodo RdvMigrateVmToDifferentHost della classe Win32_RdvhManagement
description: Avvia una migrazione in tempo reale di una macchina virtuale in un host specificato.
ms.assetid: aa4b1e57-a97c-410b-9b9d-423a1c77de70
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo RdvMigrateVmToDifferentHost
- Metodo RdvMigrateVmToDifferentHost Servizi Desktop remoto, classe Win32_RdvhManagement
- Classe Win32_RdvhManagement Servizi Desktop remoto, metodo RdvMigrateVmToDifferentHost
topic_type:
- apiref
api_name:
- Win32_RdvhManagement.RdvMigrateVmToDifferentHost
api_location:
- TSVmHostWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3def1be6332397fb3830ffe8c90f324afc9f1b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741495"
---
# <a name="rdvmigratevmtodifferenthost-method-of-the-win32_rdvhmanagement-class"></a><span data-ttu-id="c9586-106">Metodo RdvMigrateVmToDifferentHost della \_ classe RdvhManagement Win32</span><span class="sxs-lookup"><span data-stu-id="c9586-106">RdvMigrateVmToDifferentHost method of the Win32\_RdvhManagement class</span></span>

<span data-ttu-id="c9586-107">Avvia una migrazione in tempo reale di una macchina virtuale in un host specificato.</span><span class="sxs-lookup"><span data-stu-id="c9586-107">Initiates a live migration of a virtual machine to a specified host.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9586-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c9586-108">Syntax</span></span>


```mof
uint32 RdvMigrateVmToDifferentHost(
  [in] string VmName,
  [in] string DestinationHost
);
```



## <a name="parameters"></a><span data-ttu-id="c9586-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="c9586-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9586-110">*VmName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c9586-110">*VmName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9586-111">Nome della macchina virtuale da migrare.</span><span class="sxs-lookup"><span data-stu-id="c9586-111">Name of the virtual machine to migrate.</span></span>

</dd> <dt>

<span data-ttu-id="c9586-112">*DestinationHost* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c9586-112">*DestinationHost* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9586-113">nome dell'host di destinazione.</span><span class="sxs-lookup"><span data-stu-id="c9586-113">name of the destination host.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9586-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c9586-114">Return value</span></span>

<span data-ttu-id="c9586-115">Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="c9586-115">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="c9586-116">Per un elenco di questi valori, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="c9586-116">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9586-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c9586-117">Requirements</span></span>



| <span data-ttu-id="c9586-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="c9586-118">Requirement</span></span> | <span data-ttu-id="c9586-119">Valore</span><span class="sxs-lookup"><span data-stu-id="c9586-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9586-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c9586-120">Minimum supported client</span></span><br/> | <span data-ttu-id="c9586-121">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="c9586-121">None supported</span></span><br/>                                                                  |
| <span data-ttu-id="c9586-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c9586-122">Minimum supported server</span></span><br/> | <span data-ttu-id="c9586-123">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c9586-123">Windows Server 2012</span></span><br/>                                                             |
| <span data-ttu-id="c9586-124">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="c9586-124">Namespace</span></span><br/>                | <span data-ttu-id="c9586-125">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="c9586-125">Root\\CIMv2\\TerminalServices</span></span><br/>                                                   |
| <span data-ttu-id="c9586-126">MOF</span><span class="sxs-lookup"><span data-stu-id="c9586-126">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c9586-127"><dt>TSVmHost. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c9586-127"><dt>TSVmHost.mof</dt></span></span> </dl>    |
| <span data-ttu-id="c9586-128">DLL</span><span class="sxs-lookup"><span data-stu-id="c9586-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c9586-129"><dt>TSVmHostWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c9586-129"><dt>TSVmHostWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9586-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c9586-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9586-131">**\_RdvhManagement Win32**</span><span class="sxs-lookup"><span data-stu-id="c9586-131">**Win32\_RdvhManagement**</span></span>](win32-rdvhmanagement.md)
</dt> </dl>

 

 





