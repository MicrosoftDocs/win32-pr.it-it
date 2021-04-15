---
title: Metodo SetHomeDirectory della classe Win32_TerminalServiceSetting
description: Imposta la proprietà TerminalServicesHomeDirectory per la classe.
ms.assetid: 8173cd5b-965e-41bc-97cf-70d8729b8cea
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SetHomeDirectory
- Metodo SetHomeDirectory Servizi Desktop remoto, classe Win32_TerminalServiceSetting
- Classe Win32_TerminalServiceSetting Servizi Desktop remoto, metodo SetHomeDirectory
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.SetHomeDirectory
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1be732cae76b0681afd77693a07f673ef37c4a12
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517679"
---
# <a name="sethomedirectory-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="e11e8-106">Metodo SetHomeDirectory della \_ classe TerminalServiceSetting Win32</span><span class="sxs-lookup"><span data-stu-id="e11e8-106">SetHomeDirectory method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="e11e8-107">Il metodo **SetHomeDirectory** imposta la proprietà **TerminalServicesHomeDirectory** per la classe.</span><span class="sxs-lookup"><span data-stu-id="e11e8-107">The **SetHomeDirectory** method sets the **TerminalServicesHomeDirectory** property for the class.</span></span>

## <a name="syntax"></a><span data-ttu-id="e11e8-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e11e8-108">Syntax</span></span>


```mof
uint32 SetHomeDirectory(
  [in] string HomeDirectory
);
```



## <a name="parameters"></a><span data-ttu-id="e11e8-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="e11e8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e11e8-110">*HomeDirectory* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e11e8-110">*HomeDirectory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e11e8-111">Nuovo valore per la proprietà **TerminalServicesHomeDirectory** , che specifica la directory radice del computer.</span><span class="sxs-lookup"><span data-stu-id="e11e8-111">The new value for the **TerminalServicesHomeDirectory** property, which specifies the computer's root directory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e11e8-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e11e8-112">Return value</span></span>

<span data-ttu-id="e11e8-113">Restituisce esito positivo in caso di esito positivo; in caso contrario, restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="e11e8-113">Returns Success on success; otherwise, returns a WMI error code.</span></span> <span data-ttu-id="e11e8-114">Per un elenco di codici di errore WMI, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="e11e8-114">For a list of WMI error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e11e8-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="e11e8-115">Remarks</span></span>

<span data-ttu-id="e11e8-116">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="e11e8-116">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="e11e8-117">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="e11e8-117">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="e11e8-118">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="e11e8-118">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="e11e8-119">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="e11e8-119">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="e11e8-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e11e8-120">Requirements</span></span>



| <span data-ttu-id="e11e8-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="e11e8-121">Requirement</span></span> | <span data-ttu-id="e11e8-122">Valore</span><span class="sxs-lookup"><span data-stu-id="e11e8-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e11e8-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e11e8-123">Minimum supported client</span></span><br/> | <span data-ttu-id="e11e8-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e11e8-124">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e11e8-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e11e8-125">Minimum supported server</span></span><br/> | <span data-ttu-id="e11e8-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e11e8-126">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e11e8-127">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="e11e8-127">Namespace</span></span><br/>                | <span data-ttu-id="e11e8-128">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="e11e8-128">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="e11e8-129">MOF</span><span class="sxs-lookup"><span data-stu-id="e11e8-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e11e8-130"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e11e8-130"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="e11e8-131">DLL</span><span class="sxs-lookup"><span data-stu-id="e11e8-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e11e8-132"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e11e8-132"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e11e8-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e11e8-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e11e8-134">**\_TerminalServiceSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="e11e8-134">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

