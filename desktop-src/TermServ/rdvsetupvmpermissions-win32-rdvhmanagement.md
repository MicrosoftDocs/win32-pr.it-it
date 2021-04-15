---
title: Metodo RdvSetupVMPermissions della classe Win32_RdvhManagement
description: Imposta le autorizzazioni in una macchina virtuale per l'utente corrente.
ms.assetid: 6ac45983-d468-4a3b-875f-48717ba23ed0
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo RdvSetupVMPermissions
- Metodo RdvSetupVMPermissions Servizi Desktop remoto, classe Win32_RdvhManagement
- Classe Win32_RdvhManagement Servizi Desktop remoto, metodo RdvSetupVMPermissions
topic_type:
- apiref
api_name:
- Win32_RdvhManagement.RdvSetupVMPermissions
api_location:
- TSVmHostWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd8028a33bc772f9dd37f25a1dc22074baf771b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476714"
---
# <a name="rdvsetupvmpermissions-method-of-the-win32_rdvhmanagement-class"></a><span data-ttu-id="7c6dd-106">Metodo RdvSetupVMPermissions della \_ classe RdvhManagement Win32</span><span class="sxs-lookup"><span data-stu-id="7c6dd-106">RdvSetupVMPermissions method of the Win32\_RdvhManagement class</span></span>

<span data-ttu-id="7c6dd-107">Imposta le autorizzazioni in una macchina virtuale per l'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="7c6dd-107">Sets the permissions on a virtual machine for the current user.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c6dd-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7c6dd-108">Syntax</span></span>


```mof
uint32 RdvSetupVMPermissions(
  [in] string VmName
);
```



## <a name="parameters"></a><span data-ttu-id="7c6dd-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="7c6dd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c6dd-110">*VmName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7c6dd-110">*VmName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c6dd-111">Nome della macchina virtuale in cui impostare le autorizzazioni.</span><span class="sxs-lookup"><span data-stu-id="7c6dd-111">The name of the virtual machine to set permissions on.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c6dd-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7c6dd-112">Return value</span></span>

<span data-ttu-id="7c6dd-113">Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="7c6dd-113">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="7c6dd-114">Per un elenco di questi valori, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="7c6dd-114">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c6dd-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7c6dd-115">Requirements</span></span>



| <span data-ttu-id="7c6dd-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c6dd-116">Requirement</span></span> | <span data-ttu-id="7c6dd-117">Valore</span><span class="sxs-lookup"><span data-stu-id="7c6dd-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c6dd-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7c6dd-118">Minimum supported client</span></span><br/> | <span data-ttu-id="7c6dd-119">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="7c6dd-119">None supported</span></span><br/>                                                                  |
| <span data-ttu-id="7c6dd-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7c6dd-120">Minimum supported server</span></span><br/> | <span data-ttu-id="7c6dd-121">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7c6dd-121">Windows Server 2012</span></span><br/>                                                             |
| <span data-ttu-id="7c6dd-122">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="7c6dd-122">Namespace</span></span><br/>                | <span data-ttu-id="7c6dd-123">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="7c6dd-123">Root\\CIMv2\\TerminalServices</span></span><br/>                                                   |
| <span data-ttu-id="7c6dd-124">MOF</span><span class="sxs-lookup"><span data-stu-id="7c6dd-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7c6dd-125"><dt>TSVmHost. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7c6dd-125"><dt>TSVmHost.mof</dt></span></span> </dl>    |
| <span data-ttu-id="7c6dd-126">DLL</span><span class="sxs-lookup"><span data-stu-id="7c6dd-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7c6dd-127"><dt>TSVmHostWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7c6dd-127"><dt>TSVmHostWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c6dd-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7c6dd-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c6dd-129">**\_RdvhManagement Win32**</span><span class="sxs-lookup"><span data-stu-id="7c6dd-129">**Win32\_RdvhManagement**</span></span>](win32-rdvhmanagement.md)
</dt> </dl>

 

 





