---
title: Metodo Update della classe Win32_TSGatewayConnectionAuthorizationPolicy
description: Aggiorna i criteri di autorizzazione della connessione di Desktop remoto correnti (RD \ 160; LIMITE).
ms.assetid: 6d13d1b7-1c7d-4d22-b42c-36e0f4446e86
ms.tgt_platform: multiple
keywords:
- Metodo di aggiornamento Servizi Desktop remoto
- Metodo Update Servizi Desktop remoto, classe Win32_TSGatewayConnectionAuthorizationPolicy
- Classe Win32_TSGatewayConnectionAuthorizationPolicy Servizi Desktop remoto, metodo Update
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.Update
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87b982030170e954342dc5ff99754dcb89afd0e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048438"
---
# <a name="update-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="969f4-106">Metodo Update della classe Win32 \_ TSGatewayConnectionAuthorizationPolicy</span><span class="sxs-lookup"><span data-stu-id="969f4-106">Update method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="969f4-107">Aggiorna i criteri di autorizzazione della connessione del Desktop remoto corrente.</span><span class="sxs-lookup"><span data-stu-id="969f4-107">Updates the current Remote Desktop connection authorization policy (RD CAP).</span></span>

## <a name="syntax"></a><span data-ttu-id="969f4-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="969f4-108">Syntax</span></span>


```mof
uint32 Update(
  [in] string  Name,
  [in] string  UserGroupNames,
  [in] string  ComputerGroupNames,
  [in] boolean SmartCard,
  [in] boolean Password,
  [in] boolean SecureId,
  [in] boolean Enabled,
  [in] uint32  DeviceRedirectionType,
  [in] boolean DiskDrivesDisabled,
  [in] boolean PrintersDisabled,
  [in] boolean SerialPortsDisabled,
  [in] boolean ClipboardDisabled,
  [in] boolean PlugAndPlayDevicesDisabled,
  [in] uint32  IdleTimeout,
  [in] uint32  SessionTimeout,
  [in] uint32  SessionTimeoutAction,
  [in] boolean AllowOnlySDRServers,
  [in] boolean CookieAuthentication
);
```



## <a name="parameters"></a><span data-ttu-id="969f4-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="969f4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="969f4-110">*Nome* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="969f4-110">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="969f4-111">Nome del CAP di desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="969f4-111">Name of the RD CAP.</span></span> <span data-ttu-id="969f4-112">Il nome deve essere composto da un massimo di 64 caratteri, univoco (caso ignorato) e non può contenere i caratteri riservati seguenti:</span><span class="sxs-lookup"><span data-stu-id="969f4-112">The name must be 64 characters or less, unique (case is ignored), and cannot contain the following reserved characters:</span></span>

<span data-ttu-id="969f4-113"><> :; " / \\ \| ?</span><span class="sxs-lookup"><span data-stu-id="969f4-113"><> : ; " / \\ \| ?</span></span> <span data-ttu-id="969f4-114">\*\[Scheda\]</span><span class="sxs-lookup"><span data-stu-id="969f4-114">\* \[TAB\]</span></span>

</dd> <dt>

<span data-ttu-id="969f4-115">*UserGroupNames* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="969f4-115">*UserGroupNames* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="969f4-116">Elenco di nomi di gruppi di utenti separati da punti e virgola.</span><span class="sxs-lookup"><span data-stu-id="969f4-116">List of semicolon-separated user group names.</span></span> <span data-ttu-id="969f4-117">I nomi sono nel formato *dominio \\ nomegruppoutenti*.</span><span class="sxs-lookup"><span data-stu-id="969f4-117">The names are of the format *Domain\\UserGroupName*.</span></span> <span data-ttu-id="969f4-118">Se l'utente appartiene a uno di questi gruppi di utenti, l'utente sarà autorizzato ad accedere al server Gateway Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="969f4-118">If the user belongs to any one of these user groups, the user will be permitted access to the RD Gateway server.</span></span>

</dd> <dt>

<span data-ttu-id="969f4-119">*ComputerGroupNames* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="969f4-119">*ComputerGroupNames* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="969f4-120">Elenco di nomi di gruppi di computer separati da punto e virgola.</span><span class="sxs-lookup"><span data-stu-id="969f4-120">List of semicolon-separated machine group names.</span></span> <span data-ttu-id="969f4-121">Questo valore può essere vuoto.</span><span class="sxs-lookup"><span data-stu-id="969f4-121">This value can be empty.</span></span> <span data-ttu-id="969f4-122">I nomi sono nel formato *dominio \\ ComputerGroupName*.</span><span class="sxs-lookup"><span data-stu-id="969f4-122">The names are of the format *Domain\\ComputerGroupName*.</span></span> <span data-ttu-id="969f4-123">Se viene specificato un valore, il computer client deve appartenere a uno di questi gruppi di computer affinché l'utente acceda al server Gateway Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="969f4-123">If a value is specified, the client computer must belong to one of these computer groups for the user to access the RD Gateway server.</span></span>

</dd> <dt>

<span data-ttu-id="969f4-124">*Smart Card* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="969f4-124">*SmartCard* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="969f4-125">Specifica se è possibile utilizzare smart card per l'autenticazione con il server Gateway Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="969f4-125">Specifies whether smart cards can be used to authenticate with the RD Gateway server.</span></span>

</dd> <dt>

<span data-ttu-id="969f4-126">*Password* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="969f4-126">*Password* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="969f4-127">Specifica se è possibile utilizzare le password per l'autenticazione con il server Gateway Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="969f4-127">Specifies whether passwords can be used to authenticate with the RD Gateway server.</span></span>

</dd> <dt>

<span data-ttu-id="969f4-128">*SecureId* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="969f4-128">*SecureId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="969f4-129">Questo parametro è riservato per usi futuri.</span><span class="sxs-lookup"><span data-stu-id="969f4-129">This parameter is reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="969f4-130">*Abilitato* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="969f4-130">*Enabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="969f4-131">Specifica se il CAP RD è abilitato.</span><span class="sxs-lookup"><span data-stu-id="969f4-131">Specifies whether this RD CAP is enabled.</span></span>

</dd> <dt>

<span data-ttu-id="969f4-132">*DeviceRedirectionType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="969f4-132">*DeviceRedirectionType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="969f4-133">Specifica i tipi di dispositivo che verranno reindirizzati.</span><span class="sxs-lookup"><span data-stu-id="969f4-133">Specifies which device types will be redirected.</span></span>

<dt>

<span data-ttu-id="969f4-134">0</span><span class="sxs-lookup"><span data-stu-id="969f4-134">0</span></span>
</dt> <dd>

<span data-ttu-id="969f4-135">Verranno reindirizzati tutti i dispositivi.</span><span class="sxs-lookup"><span data-stu-id="969f4-135">All devices will be redirected.</span></span>

</dd> <dt>

<span data-ttu-id="969f4-136">1</span><span class="sxs-lookup"><span data-stu-id="969f4-136">1</span></span>
</dt> <dd>

<span data-ttu-id="969f4-137">Non verrà reindirizzato alcun dispositivo.</span><span class="sxs-lookup"><span data-stu-id="969f4-137">No devices will be redirected.</span></span>

</dd> <dt>

<span data-ttu-id="969f4-138">2</span><span class="sxs-lookup"><span data-stu-id="969f4-138">2</span></span>
</dt> <dd>

<span data-ttu-id="969f4-139">I dispositivi specificati non verranno reindirizzati.</span><span class="sxs-lookup"><span data-stu-id="969f4-139">Specified devices will not be redirected.</span></span> <span data-ttu-id="969f4-140">I parametri *DiskDrivesDisabled*, *PrintersDisabled*, *SerialPortsDisabled*, *ClipboardDisabled* e *PlugAndPlayDevicesDisabled* controllano i dispositivi che non verranno reindirizzati.</span><span class="sxs-lookup"><span data-stu-id="969f4-140">The *DiskDrivesDisabled*, *PrintersDisabled*, *SerialPortsDisabled*, *ClipboardDisabled*, and *PlugAndPlayDevicesDisabled* parameters control which devices will not be redirected.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="969f4-141">*DiskDrivesDisabled* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="969f4-141">*DiskDrivesDisabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="969f4-142">Specifica se disabilitare il reindirizzamento dell'unità disco se il parametro *DeviceRedirectionType* è "2".</span><span class="sxs-lookup"><span data-stu-id="969f4-142">Specifies whether to disable disk drive redirection if the *DeviceRedirectionType* parameter is "2".</span></span>

</dd> <dt>

<span data-ttu-id="969f4-143">*PrintersDisabled* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="969f4-143">*PrintersDisabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="969f4-144">Specifica se disabilitare il reindirizzamento della stampante se il parametro *DeviceRedirectionType* è "2".</span><span class="sxs-lookup"><span data-stu-id="969f4-144">Specifies whether to disable printer redirection if the *DeviceRedirectionType* parameter is "2".</span></span>

</dd> <dt>

<span data-ttu-id="969f4-145">*SerialPortsDisabled* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="969f4-145">*SerialPortsDisabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="969f4-146">Specifica se disabilitare il reindirizzamento della porta seriale se il parametro *DeviceRedirectionType* è "2".</span><span class="sxs-lookup"><span data-stu-id="969f4-146">Specifies whether to disable serial port redirection if the *DeviceRedirectionType* parameter is "2".</span></span>

</dd> <dt>

<span data-ttu-id="969f4-147">*ClipboardDisabled* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="969f4-147">*ClipboardDisabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="969f4-148">Specifica se disabilitare il reindirizzamento degli Appunti se il parametro *DeviceRedirectionType* è "2".</span><span class="sxs-lookup"><span data-stu-id="969f4-148">Specifies whether to disable clipboard redirection if the *DeviceRedirectionType* parameter is "2".</span></span>

</dd> <dt>

<span data-ttu-id="969f4-149">*PlugAndPlayDevicesDisabled* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="969f4-149">*PlugAndPlayDevicesDisabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="969f4-150">Specifica se disabilitare il reindirizzamento dei dispositivi Plug and Play se il parametro *DeviceRedirectionType* è "2".</span><span class="sxs-lookup"><span data-stu-id="969f4-150">Specifies whether to disable redirection of Plug and Play devices if the *DeviceRedirectionType* parameter is "2".</span></span>

</dd> <dt>

<span data-ttu-id="969f4-151">*IdleTimeout* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="969f4-151">*IdleTimeout* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="969f4-152">Valore di timeout di inattività in minuti</span><span class="sxs-lookup"><span data-stu-id="969f4-152">Idle timeout value in minutes</span></span>

</dd> <dt>

<span data-ttu-id="969f4-153">*SessionTimeout* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="969f4-153">*SessionTimeout* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="969f4-154">Valore di timeout della sessione in minuti</span><span class="sxs-lookup"><span data-stu-id="969f4-154">Session timeout value in minutes</span></span>

</dd> <dt>

<span data-ttu-id="969f4-155">*SessionTimeoutAction* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="969f4-155">*SessionTimeoutAction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="969f4-156">Azione di timeout della sessione in minuti</span><span class="sxs-lookup"><span data-stu-id="969f4-156">Session timeout action in minutes</span></span>

</dd> <dt>

<span data-ttu-id="969f4-157">*AllowOnlySDRServers* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="969f4-157">*AllowOnlySDRServers* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="969f4-158">Indica se le connessioni sono consentite solo ai server TS SDR</span><span class="sxs-lookup"><span data-stu-id="969f4-158">Whether connections allowed only to SDR TS servers</span></span>

</dd> <dt>

<span data-ttu-id="969f4-159">*CookieAuthentication* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="969f4-159">*CookieAuthentication* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="969f4-160">Indica se l'autenticazione del cookie può essere utilizzata per la connessione al server Gateway Servizi terminal</span><span class="sxs-lookup"><span data-stu-id="969f4-160">Indicates whether cookie authentication can be used to connect to TS Gateway server</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="969f4-161">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="969f4-161">Return value</span></span>

<span data-ttu-id="969f4-162">Se il metodo ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="969f4-162">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="969f4-163">Se il metodo ha esito negativo, restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="969f4-163">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="969f4-164">Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="969f4-164">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="969f4-165">Commenti</span><span class="sxs-lookup"><span data-stu-id="969f4-165">Remarks</span></span>

<span data-ttu-id="969f4-166">Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.</span><span class="sxs-lookup"><span data-stu-id="969f4-166">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="969f4-167">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="969f4-167">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="969f4-168">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="969f4-168">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="969f4-169">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="969f4-169">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="969f4-170">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="969f4-170">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="969f4-171">Requisiti</span><span class="sxs-lookup"><span data-stu-id="969f4-171">Requirements</span></span>



| <span data-ttu-id="969f4-172">Requisito</span><span class="sxs-lookup"><span data-stu-id="969f4-172">Requirement</span></span> | <span data-ttu-id="969f4-173">Valore</span><span class="sxs-lookup"><span data-stu-id="969f4-173">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="969f4-174">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="969f4-174">Minimum supported client</span></span><br/> | <span data-ttu-id="969f4-175">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="969f4-175">None supported</span></span><br/>                                                                |
| <span data-ttu-id="969f4-176">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="969f4-176">Minimum supported server</span></span><br/> | <span data-ttu-id="969f4-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="969f4-177">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="969f4-178">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="969f4-178">Namespace</span></span><br/>                | <span data-ttu-id="969f4-179">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="969f4-179">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="969f4-180">MOF</span><span class="sxs-lookup"><span data-stu-id="969f4-180">MOF</span></span><br/>                      | <dl> <span data-ttu-id="969f4-181"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="969f4-181"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="969f4-182">DLL</span><span class="sxs-lookup"><span data-stu-id="969f4-182">DLL</span></span><br/>                      | <dl> <span data-ttu-id="969f4-183"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="969f4-183"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="969f4-184">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="969f4-184">See also</span></span>

<dl> <dt>

[<span data-ttu-id="969f4-185">**\_TSGatewayConnectionAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="969f4-185">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

