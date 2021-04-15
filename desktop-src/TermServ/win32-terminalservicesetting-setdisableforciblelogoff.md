---
title: Metodo SetDisableForcibleLogoff della classe Win32_TerminalServiceSetting
description: Questo metodo non è supportato.
ms.assetid: 1b7ac0f2-c242-4ca8-bc4d-8111e63851eb
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SetDisableForcibleLogoff
- Metodo SetDisableForcibleLogoff Servizi Desktop remoto, classe Win32_TerminalServiceSetting
- Classe Win32_TerminalServiceSetting Servizi Desktop remoto, metodo SetDisableForcibleLogoff
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
ms.openlocfilehash: d4ae62db188d0e3aa31ffd8e3993e793e9bb2bf3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476403"
---
# <a name="setdisableforciblelogoff-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="78beb-106">Metodo SetDisableForcibleLogoff della \_ classe TerminalServiceSetting Win32</span><span class="sxs-lookup"><span data-stu-id="78beb-106">SetDisableForcibleLogoff method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="78beb-107">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="78beb-107">This method is not supported.</span></span>

<span data-ttu-id="78beb-108">**Windows Vista e Windows Server 2008:** Abilita o Disabilita se un amministratore connesso alla console di può essere disconnesso forzatamente.</span><span class="sxs-lookup"><span data-stu-id="78beb-108">**Windows Vista and Windows Server 2008:** Enables or disables whether an administrator logged onto the console can be forcibly logged off.</span></span>

## <a name="syntax"></a><span data-ttu-id="78beb-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="78beb-109">Syntax</span></span>


```mof
uint32 SetDisableForcibleLogoff(
  [in] uint32 DisableForcibleLogoff
);
```



## <a name="parameters"></a><span data-ttu-id="78beb-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="78beb-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78beb-111">*DisableForcibleLogoff* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="78beb-111">*DisableForcibleLogoff* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78beb-112">Contrassegnare la disabilitazione o l'abilitazione della proprietà **DisableForcibleLogoff** , che determina se un amministratore che è connesso alla console può essere disconnesso in modo forzato.</span><span class="sxs-lookup"><span data-stu-id="78beb-112">Flag disabling or enabling the **DisableForcibleLogoff** property, which determines whether an administrator that is logged on to the console can be forcibly logged off.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="78beb-113"><span id="0"></span>**0**</span><span class="sxs-lookup"><span data-stu-id="78beb-113"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="78beb-114">Disabilitare la proprietà.</span><span class="sxs-lookup"><span data-stu-id="78beb-114">Disable the property.</span></span> <span data-ttu-id="78beb-115">L'amministratore connesso può essere disconnesso in modo forzato.</span><span class="sxs-lookup"><span data-stu-id="78beb-115">The connected administrator can be forcibly logged off.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="78beb-116"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="78beb-116"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="78beb-117">Abilitare la proprietà.</span><span class="sxs-lookup"><span data-stu-id="78beb-117">Enable the property.</span></span> <span data-ttu-id="78beb-118">Non è possibile disconnettere forzatamente l'amministratore connesso.</span><span class="sxs-lookup"><span data-stu-id="78beb-118">The connected administrator cannot be forcibly logged off.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78beb-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="78beb-119">Return value</span></span>

<span data-ttu-id="78beb-120">Restituisce esito positivo in caso di esito positivo; in caso contrario, restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="78beb-120">Returns Success on success; otherwise, returns a WMI error code.</span></span> <span data-ttu-id="78beb-121">Per un elenco di questi valori, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="78beb-121">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="78beb-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="78beb-122">Requirements</span></span>



| <span data-ttu-id="78beb-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="78beb-123">Requirement</span></span> | <span data-ttu-id="78beb-124">Valore</span><span class="sxs-lookup"><span data-stu-id="78beb-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="78beb-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="78beb-125">Minimum supported client</span></span><br/> | <span data-ttu-id="78beb-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="78beb-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="78beb-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="78beb-127">Minimum supported server</span></span><br/> | <span data-ttu-id="78beb-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="78beb-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="78beb-129">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="78beb-129">End of client support</span></span><br/>    | <span data-ttu-id="78beb-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="78beb-130">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="78beb-131">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="78beb-131">End of server support</span></span><br/>    | <span data-ttu-id="78beb-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="78beb-132">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="78beb-133">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="78beb-133">Namespace</span></span><br/>                | <span data-ttu-id="78beb-134">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="78beb-134">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="78beb-135">MOF</span><span class="sxs-lookup"><span data-stu-id="78beb-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="78beb-136"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="78beb-136"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="78beb-137">DLL</span><span class="sxs-lookup"><span data-stu-id="78beb-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="78beb-138"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="78beb-138"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78beb-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="78beb-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78beb-140">**\_TerminalServiceSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="78beb-140">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

 





