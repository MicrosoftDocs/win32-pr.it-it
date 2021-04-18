---
title: Metodo DeleteEx della classe Win32_SessionBrokerFarmAccount
description: La \_ classe Win32 SessionBrokerFarmAccount non è più disponibile per l'uso in Windows Server 2012. | Metodo DeleteEx della classe Win32_SessionBrokerFarmAccount
ms.assetid: d30c5d3e-f63c-4b21-85ae-a0b8d5868d64
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo DeleteEx
- Metodo DeleteEx Servizi Desktop remoto, classe Win32_SessionBrokerFarmAccount
- Classe Win32_SessionBrokerFarmAccount Servizi Desktop remoto, metodo DeleteEx
topic_type:
- apiref
api_name:
- Win32_SessionBrokerFarmAccount.DeleteEx
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cdad7b1c7af85337ace59690bb44f4309254eb76
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321188"
---
# <a name="deleteex-method-of-the-win32_sessionbrokerfarmaccount-class"></a><span data-ttu-id="78c58-107">Metodo DeleteEx della \_ classe SessionBrokerFarmAccount Win32</span><span class="sxs-lookup"><span data-stu-id="78c58-107">DeleteEx method of the Win32\_SessionBrokerFarmAccount class</span></span>

<span data-ttu-id="78c58-108">\[La classe [**Win32 \_ SessionBrokerFarmAccount**](win32-sessionbrokerfarmaccount.md) non è più disponibile per l'uso in Windows Server 2012.\]</span><span class="sxs-lookup"><span data-stu-id="78c58-108">\[The [**Win32\_SessionBrokerFarmAccount**](win32-sessionbrokerfarmaccount.md) class is no longer available for use as of Windows Server 2012.\]</span></span>

<span data-ttu-id="78c58-109">Elimina l'account farm.</span><span class="sxs-lookup"><span data-stu-id="78c58-109">Deletes the farm account.</span></span>

## <a name="syntax"></a><span data-ttu-id="78c58-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="78c58-110">Syntax</span></span>


```mof
uint32 DeleteEx(
  [in] boolean DeleteComputerObject
);
```



## <a name="parameters"></a><span data-ttu-id="78c58-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="78c58-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78c58-112">*DeleteComputerObject* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="78c58-112">*DeleteComputerObject* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78c58-113">Indica se l'oggetto computer associato alla farm deve essere rimosso dal Active Directory.</span><span class="sxs-lookup"><span data-stu-id="78c58-113">Indicates whether the computer object associated with the farm is to be removed from Active Directory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78c58-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="78c58-114">Return value</span></span>

<span data-ttu-id="78c58-115">Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="78c58-115">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="78c58-116">Per un elenco di questi valori, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="78c58-116">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="78c58-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="78c58-117">Requirements</span></span>



| <span data-ttu-id="78c58-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="78c58-118">Requirement</span></span> | <span data-ttu-id="78c58-119">Valore</span><span class="sxs-lookup"><span data-stu-id="78c58-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="78c58-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="78c58-120">Minimum supported client</span></span><br/> | <span data-ttu-id="78c58-121">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="78c58-121">None supported</span></span><br/>                                                              |
| <span data-ttu-id="78c58-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="78c58-122">Minimum supported server</span></span><br/> | <span data-ttu-id="78c58-123">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="78c58-123">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="78c58-124">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="78c58-124">End of client support</span></span><br/>    | <span data-ttu-id="78c58-125">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="78c58-125">None supported</span></span><br/>                                                              |
| <span data-ttu-id="78c58-126">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="78c58-126">End of server support</span></span><br/>    | <span data-ttu-id="78c58-127">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="78c58-127">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="78c58-128">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="78c58-128">Namespace</span></span><br/>                | <span data-ttu-id="78c58-129">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="78c58-129">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="78c58-130">MOF</span><span class="sxs-lookup"><span data-stu-id="78c58-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="78c58-131"><dt>TssdWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="78c58-131"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="78c58-132">DLL</span><span class="sxs-lookup"><span data-stu-id="78c58-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="78c58-133"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="78c58-133"><dt>TssdWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78c58-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="78c58-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78c58-135">**\_SessionBrokerFarmAccount Win32**</span><span class="sxs-lookup"><span data-stu-id="78c58-135">**Win32\_SessionBrokerFarmAccount**</span></span>](win32-sessionbrokerfarmaccount.md)
</dt> </dl>

 

 





