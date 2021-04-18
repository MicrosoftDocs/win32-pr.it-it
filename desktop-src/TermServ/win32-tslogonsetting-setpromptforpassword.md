---
title: Metodo SetPromptForPassword della classe Win32_TSLogonSetting
description: Il metodo SetPromptForPassword imposta la proprietà PromptForPassword.
ms.assetid: eeeed374-4a8a-4014-833c-d931be3ef455
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SetPromptForPassword
- Metodo SetPromptForPassword Servizi Desktop remoto, classe Win32_TSLogonSetting
- Classe Win32_TSLogonSetting Servizi Desktop remoto, metodo SetPromptForPassword
topic_type:
- apiref
api_name:
- Win32_TSLogonSetting.SetPromptForPassword
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f86dc065a143505ea81bce78d9bf787fae6b0a33
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301962"
---
# <a name="setpromptforpassword-method-of-the-win32_tslogonsetting-class"></a><span data-ttu-id="6699d-106">Metodo SetPromptForPassword della \_ classe TSLogonSetting Win32</span><span class="sxs-lookup"><span data-stu-id="6699d-106">SetPromptForPassword method of the Win32\_TSLogonSetting class</span></span>

<span data-ttu-id="6699d-107">Il metodo **SetPromptForPassword** imposta la proprietà **PromptForPassword** .</span><span class="sxs-lookup"><span data-stu-id="6699d-107">The **SetPromptForPassword** method sets the **PromptForPassword** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="6699d-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6699d-108">Syntax</span></span>


```mof
uint32 SetPromptForPassword(
  [in] uint32 PromptForPassword
);
```



## <a name="parameters"></a><span data-ttu-id="6699d-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="6699d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6699d-110">*PromptForPassword* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6699d-110">*PromptForPassword* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6699d-111">Flag che disabilita o Abilita la proprietà **PromptForPassword** .</span><span class="sxs-lookup"><span data-stu-id="6699d-111">Flag disabling or enabling the **PromptForPassword** property.</span></span>

<dt>

<span data-ttu-id="6699d-112">0</span><span class="sxs-lookup"><span data-stu-id="6699d-112">0</span></span>
</dt> <dd>

<span data-ttu-id="6699d-113">Disabilita la richiesta di conferma della password.</span><span class="sxs-lookup"><span data-stu-id="6699d-113">Disables password-prompting.</span></span>

</dd> <dt>

<span data-ttu-id="6699d-114">1</span><span class="sxs-lookup"><span data-stu-id="6699d-114">1</span></span>
</dt> <dd>

<span data-ttu-id="6699d-115">Abilita la richiesta di conferma della password.</span><span class="sxs-lookup"><span data-stu-id="6699d-115">Enables password-prompting.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6699d-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6699d-116">Return value</span></span>

<span data-ttu-id="6699d-117">Restituisce l'esito positivo, in caso contrario restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="6699d-117">Returns Success on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="6699d-118">Per un elenco di questi valori, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="6699d-118">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="6699d-119">Il metodo restituisce un errore se l'impostazione è sotto il controllo criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="6699d-119">The method returns an error if the setting is under group policy control.</span></span>

<dl> <dt>

<span data-ttu-id="6699d-120">**False** (0)</span><span class="sxs-lookup"><span data-stu-id="6699d-120">**FALSE** (0)</span></span>
</dt> <dt>

<span data-ttu-id="6699d-121">**True** (1)</span><span class="sxs-lookup"><span data-stu-id="6699d-121">**TRUE** (1)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="6699d-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="6699d-122">Remarks</span></span>

<span data-ttu-id="6699d-123">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="6699d-123">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="6699d-124">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="6699d-124">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="6699d-125">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="6699d-125">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="6699d-126">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="6699d-126">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="6699d-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6699d-127">Requirements</span></span>



| <span data-ttu-id="6699d-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="6699d-128">Requirement</span></span> | <span data-ttu-id="6699d-129">Valore</span><span class="sxs-lookup"><span data-stu-id="6699d-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6699d-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6699d-130">Minimum supported client</span></span><br/> | <span data-ttu-id="6699d-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6699d-131">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6699d-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6699d-132">Minimum supported server</span></span><br/> | <span data-ttu-id="6699d-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6699d-133">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6699d-134">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="6699d-134">Namespace</span></span><br/>                | <span data-ttu-id="6699d-135">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="6699d-135">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="6699d-136">MOF</span><span class="sxs-lookup"><span data-stu-id="6699d-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6699d-137"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6699d-137"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="6699d-138">DLL</span><span class="sxs-lookup"><span data-stu-id="6699d-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6699d-139"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6699d-139"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6699d-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6699d-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6699d-141">**\_TSLogonSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="6699d-141">**Win32\_TSLogonSetting**</span></span>](win32-tslogonsetting.md)
</dt> </dl>

 

