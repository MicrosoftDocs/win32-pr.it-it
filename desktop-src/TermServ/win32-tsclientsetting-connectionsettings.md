---
title: Metodo ConnectionSettings della classe Win32_TSClientSetting
description: Il Metodo ConnectionSettings imposta le impostazioni di sessione che si applicano al processo di connessione e accesso.
ms.assetid: 603807fe-f341-4358-a3b0-0300785cbdb1
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del Metodo ConnectionSettings
- Metodo ConnectionSettings Servizi Desktop remoto, classe Win32_TSClientSetting
- Classe Win32_TSClientSetting Servizi Desktop remoto, Metodo ConnectionSettings
topic_type:
- apiref
api_name:
- Win32_TSClientSetting.ConnectionSettings
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec255f00656684751b750e92d7a3df8290e3573e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517674"
---
# <a name="connectionsettings-method-of-the-win32_tsclientsetting-class"></a><span data-ttu-id="a210b-106">Metodo ConnectionSettings della \_ classe TSClientSetting Win32</span><span class="sxs-lookup"><span data-stu-id="a210b-106">ConnectionSettings method of the Win32\_TSClientSetting class</span></span>

<span data-ttu-id="a210b-107">Il metodo **ConnectionSettings** imposta le impostazioni di sessione che si applicano al processo di connessione e accesso.</span><span class="sxs-lookup"><span data-stu-id="a210b-107">The **ConnectionSettings** method sets the session settings that apply to the connection and logon process.</span></span>

## <a name="syntax"></a><span data-ttu-id="a210b-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a210b-108">Syntax</span></span>


```mof
uint32 ConnectionSettings(
  [in] uint32 ConnectClientDrivesAtLogon,
  [in] uint32 ConnectPrinterAtLogon,
  [in] uint32 DefaultToClientPrinter
);
```



## <a name="parameters"></a><span data-ttu-id="a210b-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="a210b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a210b-110">*ConnectClientDrivesAtLogon* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a210b-110">*ConnectClientDrivesAtLogon* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a210b-111">Flag che Abilita o Disabilita la proprietà **ConnectClientDrivesAtLogon** che specifica se le unità del client vengono connesse automaticamente durante la procedura di accesso.</span><span class="sxs-lookup"><span data-stu-id="a210b-111">Flag enabling or disabling the **ConnectClientDrivesAtLogon** property which specifies whether the client's drives are automatically connected during the logon procedure.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="a210b-112"><span id="0"></span>**0**</span><span class="sxs-lookup"><span data-stu-id="a210b-112"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="a210b-113">Le unità del client non vengono connesse automaticamente.</span><span class="sxs-lookup"><span data-stu-id="a210b-113">The client's drives are not automatically connected.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="a210b-114"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="a210b-114"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="a210b-115">Le unità del client vengono connesse automaticamente.</span><span class="sxs-lookup"><span data-stu-id="a210b-115">The client's drives are automatically connected.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="a210b-116">*ConnectPrinterAtLogon* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a210b-116">*ConnectPrinterAtLogon* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a210b-117">Flag che Abilita o Disabilita la proprietà **ConnectPrinterAtLogon** , che specifica se tutte le stampanti client locali mappate vengono connesse automaticamente durante la procedura di accesso.</span><span class="sxs-lookup"><span data-stu-id="a210b-117">Flag enabling or disabling the **ConnectPrinterAtLogon** property, which specifies whether all mapped local client printers are automatically connected during the logon procedure.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="a210b-118"><span id="0"></span>**0**</span><span class="sxs-lookup"><span data-stu-id="a210b-118"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="a210b-119">Tutte le stampanti locali mappate non vengono connesse automaticamente.</span><span class="sxs-lookup"><span data-stu-id="a210b-119">All mapped local printers are not automatically connected.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="a210b-120"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="a210b-120"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="a210b-121">Tutte le stampanti locali mappate vengono connesse automaticamente.</span><span class="sxs-lookup"><span data-stu-id="a210b-121">All mapped local printers are automatically connected.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="a210b-122">*DefaultToClientPrinter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a210b-122">*DefaultToClientPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a210b-123">Flag che Abilita o Disabilita la proprietà **DefaultToClientPrinter** che specifica se i processi di stampa vengono inviati automaticamente alla stampante locale del client.</span><span class="sxs-lookup"><span data-stu-id="a210b-123">Flag enabling or disabling the **DefaultToClientPrinter** property which specifies whether print jobs are automatically sent to the client's local printer.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="a210b-124"><span id="0"></span>**0**</span><span class="sxs-lookup"><span data-stu-id="a210b-124"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="a210b-125">I processi di stampa non vengono inviati automaticamente.</span><span class="sxs-lookup"><span data-stu-id="a210b-125">Print jobs are not automatically sent.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="a210b-126"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="a210b-126"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="a210b-127">I processi di stampa vengono inviati automaticamente.</span><span class="sxs-lookup"><span data-stu-id="a210b-127">Print jobs are automatically sent.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a210b-128">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a210b-128">Return value</span></span>

<span data-ttu-id="a210b-129">Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="a210b-129">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="a210b-130">Per un elenco di questi valori, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="a210b-130">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="a210b-131">Il metodo restituisce un errore se le impostazioni di connessione dell'utente vengono sostituite dal server.</span><span class="sxs-lookup"><span data-stu-id="a210b-131">The method returns an error if the user's connection settings are overridden by the server.</span></span>

## <a name="remarks"></a><span data-ttu-id="a210b-132">Commenti</span><span class="sxs-lookup"><span data-stu-id="a210b-132">Remarks</span></span>

<span data-ttu-id="a210b-133">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="a210b-133">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="a210b-134">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="a210b-134">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="a210b-135">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="a210b-135">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="a210b-136">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="a210b-136">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="a210b-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a210b-137">Requirements</span></span>



| <span data-ttu-id="a210b-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="a210b-138">Requirement</span></span> | <span data-ttu-id="a210b-139">Valore</span><span class="sxs-lookup"><span data-stu-id="a210b-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a210b-140">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a210b-140">Minimum supported client</span></span><br/> | <span data-ttu-id="a210b-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a210b-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a210b-142">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a210b-142">Minimum supported server</span></span><br/> | <span data-ttu-id="a210b-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a210b-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a210b-144">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="a210b-144">Namespace</span></span><br/>                | <span data-ttu-id="a210b-145">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="a210b-145">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="a210b-146">MOF</span><span class="sxs-lookup"><span data-stu-id="a210b-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a210b-147"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a210b-147"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="a210b-148">DLL</span><span class="sxs-lookup"><span data-stu-id="a210b-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a210b-149"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a210b-149"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a210b-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a210b-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a210b-151">**\_TSClientSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="a210b-151">**Win32\_TSClientSetting**</span></span>](win32-tsclientsetting.md)
</dt> </dl>

 

