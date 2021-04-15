---
title: Metodo Enable della classe Win32_Terminal
description: Il metodo Enable Disabilita o Abilita il terminale.
ms.assetid: f249563b-6fa0-413c-9fc7-01dd16d5c561
ms.tgt_platform: multiple
keywords:
- Abilita Servizi Desktop remoto metodo
- Enable Servizi Desktop remoto metodo, classe Win32_Terminal
- Classe Win32_Terminal Servizi Desktop remoto, metodo Enable
topic_type:
- apiref
api_name:
- Win32_Terminal.Enable
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: afedef572c65f249c48da850172bb9fc4d222c19
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400368"
---
# <a name="enable-method-of-the-win32_terminal-class"></a><span data-ttu-id="80252-106">Metodo Enable della \_ classe terminale Win32</span><span class="sxs-lookup"><span data-stu-id="80252-106">Enable method of the Win32\_Terminal class</span></span>

<span data-ttu-id="80252-107">Il metodo **Enable** Disabilita o Abilita il terminale.</span><span class="sxs-lookup"><span data-stu-id="80252-107">The **Enable** method disables or enables the terminal.</span></span>

## <a name="syntax"></a><span data-ttu-id="80252-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="80252-108">Syntax</span></span>


```mof
uint32 Enable(
  [in] uint32 fEnableTerminal
);
```



## <a name="parameters"></a><span data-ttu-id="80252-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="80252-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80252-110">*fEnableTerminal* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="80252-110">*fEnableTerminal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80252-111">Flag che disabilita o Abilita il terminale.</span><span class="sxs-lookup"><span data-stu-id="80252-111">Flag that disables or enables the terminal.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="80252-112"><span id="0"></span>**0**</span><span class="sxs-lookup"><span data-stu-id="80252-112"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="80252-113">Il terminale è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="80252-113">The terminal is disabled.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="80252-114"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="80252-114"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="80252-115">Il terminale è abilitato.</span><span class="sxs-lookup"><span data-stu-id="80252-115">The terminal is enabled.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="80252-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="80252-116">Return value</span></span>

<span data-ttu-id="80252-117">Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="80252-117">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="80252-118">Per un elenco di questi valori, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="80252-118">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="80252-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="80252-119">Remarks</span></span>

<span data-ttu-id="80252-120">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="80252-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="80252-121">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="80252-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="80252-122">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="80252-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="80252-123">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="80252-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="80252-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="80252-124">Requirements</span></span>



| <span data-ttu-id="80252-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="80252-125">Requirement</span></span> | <span data-ttu-id="80252-126">Valore</span><span class="sxs-lookup"><span data-stu-id="80252-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="80252-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="80252-127">Minimum supported client</span></span><br/> | <span data-ttu-id="80252-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="80252-128">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="80252-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="80252-129">Minimum supported server</span></span><br/> | <span data-ttu-id="80252-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="80252-130">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="80252-131">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="80252-131">Namespace</span></span><br/>                | <span data-ttu-id="80252-132">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="80252-132">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="80252-133">MOF</span><span class="sxs-lookup"><span data-stu-id="80252-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="80252-134"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="80252-134"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="80252-135">DLL</span><span class="sxs-lookup"><span data-stu-id="80252-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="80252-136"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="80252-136"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="80252-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="80252-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80252-138">**\_Terminale Win32**</span><span class="sxs-lookup"><span data-stu-id="80252-138">**Win32\_Terminal**</span></span>](win32-terminal.md)
</dt> </dl>

 

