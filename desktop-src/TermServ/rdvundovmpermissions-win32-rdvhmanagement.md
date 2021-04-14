---
title: Metodo RdvUndoVMPermissions della classe Win32_RdvhManagement
description: Ripristina le autorizzazioni impostate da RdvSetupVMPermissions nella macchina virtuale specificata.
ms.assetid: 3331430e-7427-42f7-ab09-27fece8dc3ca
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo RdvUndoVMPermissions
- Metodo RdvUndoVMPermissions Servizi Desktop remoto, classe Win32_RdvhManagement
- Classe Win32_RdvhManagement Servizi Desktop remoto, metodo RdvUndoVMPermissions
topic_type:
- apiref
api_name:
- Win32_RdvhManagement.RdvUndoVMPermissions
api_location:
- TSVmHostWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d1dc8892435522dcd2c7457fe4b74a0d9671740
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478868"
---
# <a name="rdvundovmpermissions-method-of-the-win32_rdvhmanagement-class"></a><span data-ttu-id="97970-106">Metodo RdvUndoVMPermissions della \_ classe RdvhManagement Win32</span><span class="sxs-lookup"><span data-stu-id="97970-106">RdvUndoVMPermissions method of the Win32\_RdvhManagement class</span></span>

<span data-ttu-id="97970-107">Ripristina le autorizzazioni impostate da [**RdvSetupVMPermissions**](rdvsetupvmpermissions-win32-rdvhmanagement.md) nella macchina virtuale specificata.</span><span class="sxs-lookup"><span data-stu-id="97970-107">Reverts permissions set by [**RdvSetupVMPermissions**](rdvsetupvmpermissions-win32-rdvhmanagement.md) on the specified virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="97970-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="97970-108">Syntax</span></span>


```mof
uint32 RdvUndoVMPermissions(
  [in] string VmName
);
```



## <a name="parameters"></a><span data-ttu-id="97970-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="97970-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97970-110">*VmName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="97970-110">*VmName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97970-111">Nome della macchina virtuale su cui annullare le autorizzazioni.</span><span class="sxs-lookup"><span data-stu-id="97970-111">Name of the virtual machine to undo permissions on.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97970-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="97970-112">Return value</span></span>

<span data-ttu-id="97970-113">Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="97970-113">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="97970-114">Per un elenco di questi valori, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="97970-114">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="97970-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="97970-115">Requirements</span></span>



| <span data-ttu-id="97970-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="97970-116">Requirement</span></span> | <span data-ttu-id="97970-117">Valore</span><span class="sxs-lookup"><span data-stu-id="97970-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="97970-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="97970-118">Minimum supported client</span></span><br/> | <span data-ttu-id="97970-119">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="97970-119">None supported</span></span><br/>                                                                  |
| <span data-ttu-id="97970-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="97970-120">Minimum supported server</span></span><br/> | <span data-ttu-id="97970-121">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="97970-121">Windows Server 2012</span></span><br/>                                                             |
| <span data-ttu-id="97970-122">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="97970-122">Namespace</span></span><br/>                | <span data-ttu-id="97970-123">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="97970-123">Root\\CIMv2\\TerminalServices</span></span><br/>                                                   |
| <span data-ttu-id="97970-124">MOF</span><span class="sxs-lookup"><span data-stu-id="97970-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="97970-125"><dt>TSVmHost. mof</dt></span><span class="sxs-lookup"><span data-stu-id="97970-125"><dt>TSVmHost.mof</dt></span></span> </dl>    |
| <span data-ttu-id="97970-126">DLL</span><span class="sxs-lookup"><span data-stu-id="97970-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="97970-127"><dt>TSVmHostWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="97970-127"><dt>TSVmHostWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97970-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="97970-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97970-129">**\_RdvhManagement Win32**</span><span class="sxs-lookup"><span data-stu-id="97970-129">**Win32\_RdvhManagement**</span></span>](win32-rdvhmanagement.md)
</dt> </dl>

 

 





