---
title: Metodo SetTimeZoneRedirection della classe Win32_TerminalServiceSetting
description: Il metodo SetTimeZoneRedirection imposta la proprietà TimeZoneRedirection, che consente al computer client di reindirizzare le impostazioni del fuso orario al Servizi Desktop remoto sessione.
ms.assetid: 4ae149b7-b7de-4530-a142-7253dd1e0d07
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SetTimeZoneRedirection
- Metodo SetTimeZoneRedirection Servizi Desktop remoto, classe Win32_TerminalServiceSetting
- Classe Win32_TerminalServiceSetting Servizi Desktop remoto, metodo SetTimeZoneRedirection
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.SetTimeZoneRedirection
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2761567c724abf129ac881188bc468b228d7fd11
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301510"
---
# <a name="settimezoneredirection-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="b7be3-106">Metodo SetTimeZoneRedirection della \_ classe TerminalServiceSetting Win32</span><span class="sxs-lookup"><span data-stu-id="b7be3-106">SetTimeZoneRedirection method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="b7be3-107">Il metodo **SetTimeZoneRedirection** imposta la proprietà **TimeZoneRedirection** , che consente al computer client di reindirizzare le impostazioni del fuso orario al Servizi Desktop remoto sessione.</span><span class="sxs-lookup"><span data-stu-id="b7be3-107">The **SetTimeZoneRedirection** method sets the **TimeZoneRedirection** property, which allows the client computer to redirect its time zone settings to the Remote Desktop Services session.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7be3-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b7be3-108">Syntax</span></span>


```mof
uint32 SetTimeZoneRedirection(
  [in] uint32 TimeZoneRedirection
);
```



## <a name="parameters"></a><span data-ttu-id="b7be3-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="b7be3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7be3-110">*TimeZoneRedirection* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b7be3-110">*TimeZoneRedirection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7be3-111">Nuovo valore per la proprietà **TimeZoneRedirection** .</span><span class="sxs-lookup"><span data-stu-id="b7be3-111">The new value for the **TimeZoneRedirection** property.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="b7be3-112"><span id="0"></span>**0**</span><span class="sxs-lookup"><span data-stu-id="b7be3-112"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="b7be3-113">Disabilita la proprietà **TimeZoneRedirection** .</span><span class="sxs-lookup"><span data-stu-id="b7be3-113">Disables the **TimeZoneRedirection** property.</span></span> <span data-ttu-id="b7be3-114">Non si verifica alcun reindirizzamento del fuso orario.</span><span class="sxs-lookup"><span data-stu-id="b7be3-114">No time zone redirection occurs.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="b7be3-115"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="b7be3-115"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="b7be3-116">Abilita la proprietà **TimeZoneRedirection** .</span><span class="sxs-lookup"><span data-stu-id="b7be3-116">Enables the **TimeZoneRedirection** property.</span></span> <span data-ttu-id="b7be3-117">Il fuso orario del client viene reindirizzato al fuso orario della sessione.</span><span class="sxs-lookup"><span data-stu-id="b7be3-117">The client's time zone is redirected to the session's time zone.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7be3-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b7be3-118">Return value</span></span>

<span data-ttu-id="b7be3-119">Restituisce 0 in caso di esito positivo; in caso contrario, restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="b7be3-119">Returns 0 on success; otherwise returns a WMI error code.</span></span> <span data-ttu-id="b7be3-120">Per un elenco di questi valori, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="b7be3-120">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="b7be3-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="b7be3-121">Remarks</span></span>

<span data-ttu-id="b7be3-122">Per impostazione predefinita, il fuso orario per la sessione di Servizi Desktop remoto corrisponde al fuso orario del server di host sessione Desktop remoto (host sessione Desktop remoto).</span><span class="sxs-lookup"><span data-stu-id="b7be3-122">By default, the time zone for the Remote Desktop Services session is the same as the time zone for the Remote Desktop Session Host (RD Session Host) server.</span></span> <span data-ttu-id="b7be3-123">I computer client non possono reindirizzare le informazioni sul fuso orario.</span><span class="sxs-lookup"><span data-stu-id="b7be3-123">Client computers cannot redirect time zone information.</span></span>

<span data-ttu-id="b7be3-124">Se il reindirizzamento del fuso orario è disabilitato, le nuove sessioni ereditano il fuso orario del server.</span><span class="sxs-lookup"><span data-stu-id="b7be3-124">If time zone redirection is disabled, new sessions inherit the server time zone.</span></span> <span data-ttu-id="b7be3-125">Quando una sessione viene riconnessa, la sessione mantiene il fuso orario precedente alla disconnessione.</span><span class="sxs-lookup"><span data-stu-id="b7be3-125">When a session reconnects, the session retains the time zone it had prior to disconnecting.</span></span>

<span data-ttu-id="b7be3-126">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="b7be3-126">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="b7be3-127">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="b7be3-127">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="b7be3-128">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="b7be3-128">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="b7be3-129">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="b7be3-129">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="b7be3-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b7be3-130">Requirements</span></span>



| <span data-ttu-id="b7be3-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="b7be3-131">Requirement</span></span> | <span data-ttu-id="b7be3-132">Valore</span><span class="sxs-lookup"><span data-stu-id="b7be3-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b7be3-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b7be3-133">Minimum supported client</span></span><br/> | <span data-ttu-id="b7be3-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b7be3-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b7be3-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b7be3-135">Minimum supported server</span></span><br/> | <span data-ttu-id="b7be3-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b7be3-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b7be3-137">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b7be3-137">Namespace</span></span><br/>                | <span data-ttu-id="b7be3-138">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="b7be3-138">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="b7be3-139">MOF</span><span class="sxs-lookup"><span data-stu-id="b7be3-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b7be3-140"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b7be3-140"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="b7be3-141">DLL</span><span class="sxs-lookup"><span data-stu-id="b7be3-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b7be3-142"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b7be3-142"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7be3-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b7be3-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7be3-144">**\_TerminalServiceSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="b7be3-144">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

