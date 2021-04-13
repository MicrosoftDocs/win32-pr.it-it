---
title: Metodo PingLicenseServer della classe Win32_TerminalServiceSetting
description: PingLicenseServer non è più disponibile.
ms.assetid: d2a9f273-1ff9-4391-889b-a3b9c9f95c3b
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo PingLicenseServer
- Metodo PingLicenseServer Servizi Desktop remoto, classe Win32_TerminalServiceSetting
- Classe Win32_TerminalServiceSetting Servizi Desktop remoto, metodo PingLicenseServer
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.PingLicenseServer
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2fe7277b3130c88c1aec7716c1a3bf560b81db64
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400582"
---
# <a name="pinglicenseserver-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="5aa9e-106">Metodo PingLicenseServer della \_ classe TerminalServiceSetting Win32</span><span class="sxs-lookup"><span data-stu-id="5aa9e-106">PingLicenseServer method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="5aa9e-107">\[**PingLicenseServer** non è più disponibile per l'uso a partire da Windows Server 2008 R2.\]</span><span class="sxs-lookup"><span data-stu-id="5aa9e-107">\[**PingLicenseServer** is no longer available for use as of Windows Server 2008 R2.\]</span></span>

<span data-ttu-id="5aa9e-108">**Windows Server 2008:** Effettua il ping del server licenze per determinare se si tratta di un server licenze valido.</span><span class="sxs-lookup"><span data-stu-id="5aa9e-108">**Windows Server 2008:** Pings the license server to determine if it is a valid license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="5aa9e-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5aa9e-109">Syntax</span></span>


```mof
uint32 PingLicenseServer(
  [in] string ServerName
);
```



## <a name="parameters"></a><span data-ttu-id="5aa9e-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="5aa9e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5aa9e-111">*Nomeserver* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5aa9e-111">*ServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5aa9e-112">Nome del server licenze.</span><span class="sxs-lookup"><span data-stu-id="5aa9e-112">Name of the license server.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5aa9e-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5aa9e-113">Return value</span></span>

<dl> <dt>

<span data-ttu-id="5aa9e-114">**\_OK**</span><span class="sxs-lookup"><span data-stu-id="5aa9e-114">**S\_OK**</span></span>
</dt> <dd>

<span data-ttu-id="5aa9e-115">Il server è un server licenze valido.</span><span class="sxs-lookup"><span data-stu-id="5aa9e-115">The server is a valid license server.</span></span>

</dd> <dt>

<span data-ttu-id="5aa9e-116">**S \_ false**</span><span class="sxs-lookup"><span data-stu-id="5aa9e-116">**S\_FALSE**</span></span>
</dt> <dd>

<span data-ttu-id="5aa9e-117">Il server licenze non è valido.</span><span class="sxs-lookup"><span data-stu-id="5aa9e-117">The license server is not valid.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5aa9e-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="5aa9e-118">Remarks</span></span>

<span data-ttu-id="5aa9e-119">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="5aa9e-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="5aa9e-120">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="5aa9e-120">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="5aa9e-121">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="5aa9e-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="5aa9e-122">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="5aa9e-122">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="5aa9e-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5aa9e-123">Requirements</span></span>



| <span data-ttu-id="5aa9e-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="5aa9e-124">Requirement</span></span> | <span data-ttu-id="5aa9e-125">Valore</span><span class="sxs-lookup"><span data-stu-id="5aa9e-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5aa9e-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5aa9e-126">Minimum supported client</span></span><br/> | <span data-ttu-id="5aa9e-127">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="5aa9e-127">None supported</span></span><br/>                                                               |
| <span data-ttu-id="5aa9e-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5aa9e-128">Minimum supported server</span></span><br/> | <span data-ttu-id="5aa9e-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5aa9e-129">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5aa9e-130">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="5aa9e-130">End of client support</span></span><br/>    | <span data-ttu-id="5aa9e-131">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="5aa9e-131">None supported</span></span><br/>                                                               |
| <span data-ttu-id="5aa9e-132">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="5aa9e-132">End of server support</span></span><br/>    | <span data-ttu-id="5aa9e-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5aa9e-133">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5aa9e-134">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="5aa9e-134">Namespace</span></span><br/>                | <span data-ttu-id="5aa9e-135">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="5aa9e-135">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="5aa9e-136">MOF</span><span class="sxs-lookup"><span data-stu-id="5aa9e-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5aa9e-137"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5aa9e-137"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="5aa9e-138">DLL</span><span class="sxs-lookup"><span data-stu-id="5aa9e-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5aa9e-139"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5aa9e-139"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5aa9e-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5aa9e-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5aa9e-141">**\_TerminalServiceSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="5aa9e-141">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

