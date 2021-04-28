---
title: Metodo SetDisableForcibleLogoff della Win32_TerminalServiceSetting classe
description: 'Metodo SetDisableForcibleLogoff della Win32_TerminalServiceSetting: questo metodo non è supportato.'
ms.assetid: 1b7ac0f2-c242-4ca8-bc4d-8111e63851eb
ms.tgt_platform: multiple
keywords:
- Metodo SetDisableForcibleLogoff Servizi Desktop remoto
- Metodo SetDisableForcibleLogoff Servizi Desktop remoto , Win32_TerminalServiceSetting classe
- Win32_TerminalServiceSetting classe Servizi Desktop remoto, metodo SetDisableForcibleLogoff
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.SetDisableForcibleLogoff
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4be6ace10853ec282f5ab17b1f5f5921ef2c0d6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103709"
---
# <a name="setdisableforciblelogoff-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="f0872-106">Metodo SetDisableForcibleLogoff della classe TerminalServiceSetting Win32 \_</span><span class="sxs-lookup"><span data-stu-id="f0872-106">SetDisableForcibleLogoff method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="f0872-107">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="f0872-107">This method is not supported.</span></span>

<span data-ttu-id="f0872-108">**Windows Vista e Windows Server 2008:** Abilita o disabilita se un amministratore connesso alla console può essere disconnesso forzatamente.</span><span class="sxs-lookup"><span data-stu-id="f0872-108">**Windows Vista and Windows Server 2008:** Enables or disables whether an administrator logged onto the console can be forcibly logged off.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0872-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f0872-109">Syntax</span></span>


```mof
uint32 SetDisableForcibleLogoff(
  [in] uint32 DisableForcibleLogoff
);
```



## <a name="parameters"></a><span data-ttu-id="f0872-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="f0872-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0872-111">*DisableForcibleLogoff* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="f0872-111">*DisableForcibleLogoff* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0872-112">Flag che disabilita o abilita la **proprietà DisableForcibleLogoff,** che determina se un amministratore connesso alla console può essere disconnesso forzatamente.</span><span class="sxs-lookup"><span data-stu-id="f0872-112">Flag disabling or enabling the **DisableForcibleLogoff** property, which determines whether an administrator that is logged on to the console can be forcibly logged off.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="f0872-113"><span id="0"></span>**0**</span><span class="sxs-lookup"><span data-stu-id="f0872-113"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="f0872-114">Disabilitare la proprietà .</span><span class="sxs-lookup"><span data-stu-id="f0872-114">Disable the property.</span></span> <span data-ttu-id="f0872-115">L'amministratore connesso può essere disconnesso forzatamente.</span><span class="sxs-lookup"><span data-stu-id="f0872-115">The connected administrator can be forcibly logged off.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="f0872-116"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="f0872-116"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="f0872-117">Abilitare la proprietà .</span><span class="sxs-lookup"><span data-stu-id="f0872-117">Enable the property.</span></span> <span data-ttu-id="f0872-118">L'amministratore connesso non può essere disconnesso forzatamente.</span><span class="sxs-lookup"><span data-stu-id="f0872-118">The connected administrator cannot be forcibly logged off.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0872-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f0872-119">Return value</span></span>

<span data-ttu-id="f0872-120">Restituisce Success in esito positivo; In caso contrario, restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="f0872-120">Returns Success on success; otherwise, returns a WMI error code.</span></span> <span data-ttu-id="f0872-121">Per un [elenco Servizi Desktop remoto di questi valori,](terminal-services-wmi-provider-error-codes.md) fare riferimento Servizi Desktop remoto di errore del provider WMI.</span><span class="sxs-lookup"><span data-stu-id="f0872-121">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0872-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f0872-122">Requirements</span></span>



| <span data-ttu-id="f0872-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="f0872-123">Requirement</span></span> | <span data-ttu-id="f0872-124">Valore</span><span class="sxs-lookup"><span data-stu-id="f0872-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f0872-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f0872-125">Minimum supported client</span></span><br/> | <span data-ttu-id="f0872-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f0872-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f0872-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f0872-127">Minimum supported server</span></span><br/> | <span data-ttu-id="f0872-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f0872-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f0872-129">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="f0872-129">End of client support</span></span><br/>    | <span data-ttu-id="f0872-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f0872-130">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f0872-131">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="f0872-131">End of server support</span></span><br/>    | <span data-ttu-id="f0872-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f0872-132">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f0872-133">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f0872-133">Namespace</span></span><br/>                | <span data-ttu-id="f0872-134">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="f0872-134">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="f0872-135">MOF</span><span class="sxs-lookup"><span data-stu-id="f0872-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f0872-136"><dt>TSCfgWmi.mof</dt></span><span class="sxs-lookup"><span data-stu-id="f0872-136"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="f0872-137">DLL</span><span class="sxs-lookup"><span data-stu-id="f0872-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f0872-138"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f0872-138"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0872-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f0872-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0872-140">**\_Terminale Win32ServiceSetting**</span><span class="sxs-lookup"><span data-stu-id="f0872-140">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

 





