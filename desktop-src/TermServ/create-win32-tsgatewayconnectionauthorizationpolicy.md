---
title: Metodo Create della classe Win32_TSGatewayConnectionAuthorizationPolicy
description: Crea un criterio di autorizzazione di connessione Desktop remoto (RD \ 160; Con i valori specificati. Il nuovo RD \ 160; Il CAP verrà inserito nella parte superiore della RD \ 160; Ordine di valutazione CAP, con valore della proprietà Order pari a \ 0034; 1 \ 0034;.
ms.assetid: 0010cd2b-9c23-488a-9337-d2ed338136d3
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto crea metodo
- Create Method Servizi Desktop remoto, classe Win32_TSGatewayConnectionAuthorizationPolicy
- Classe Win32_TSGatewayConnectionAuthorizationPolicy Servizi Desktop remoto, metodo create
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.Create
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: edc027c2f7fc90318bd1af6fd1254077a860a5d8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048029"
---
# <a name="create-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="6640c-107">Metodo Create della classe Win32 \_ TSGatewayConnectionAuthorizationPolicy</span><span class="sxs-lookup"><span data-stu-id="6640c-107">Create method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="6640c-108">Crea un criterio di autorizzazione di connessione Desktop remoto (RD) utilizzando i valori specificati.</span><span class="sxs-lookup"><span data-stu-id="6640c-108">Creates a Remote Desktop connection authorization policy (RD CAP) by using the specified values.</span></span> <span data-ttu-id="6640c-109">Il nuovo criterio di autorizzazione connessioni Desktop remoto verrà inserito all'inizio dell'ordine di valutazione del CAP RD, con un valore della proprietà **Order** pari a "1".</span><span class="sxs-lookup"><span data-stu-id="6640c-109">The new RD CAP will be inserted at the top of the RD CAP evaluation order, with an **Order** property value of "1".</span></span>

## <a name="syntax"></a><span data-ttu-id="6640c-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6640c-110">Syntax</span></span>


```mof
uint32 Create(
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



## <a name="parameters"></a><span data-ttu-id="6640c-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="6640c-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6640c-112">*Nome* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6640c-112">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6640c-113">Nome del CAP di desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="6640c-113">Name of the RD CAP.</span></span> <span data-ttu-id="6640c-114">Il nome deve essere composto da un massimo di 64 caratteri, univoco (caso ignorato) e non può contenere i caratteri riservati seguenti:</span><span class="sxs-lookup"><span data-stu-id="6640c-114">The name must be 64 characters or less, unique (case is ignored), and cannot contain the following reserved characters:</span></span>

<span data-ttu-id="6640c-115"><> :; " / \\ \| ?</span><span class="sxs-lookup"><span data-stu-id="6640c-115"><> : ; " / \\ \| ?</span></span> <span data-ttu-id="6640c-116">\*\[Scheda\]</span><span class="sxs-lookup"><span data-stu-id="6640c-116">\* \[TAB\]</span></span>

</dd> <dt>

<span data-ttu-id="6640c-117">*UserGroupNames* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6640c-117">*UserGroupNames* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6640c-118">Elenco di nomi di gruppi di utenti, separati da punti e virgola, per il nuovo CAP RD.</span><span class="sxs-lookup"><span data-stu-id="6640c-118">List of user group names, separated by semicolons, for the new RD CAP.</span></span>

</dd> <dt>

<span data-ttu-id="6640c-119">*ComputerGroupNames* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6640c-119">*ComputerGroupNames* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6640c-120">Elenco di nomi di gruppi di computer, separati da punti e virgola, per il nuovo CAP RD.</span><span class="sxs-lookup"><span data-stu-id="6640c-120">List of computer group names, separated by semicolons, for the new RD CAP.</span></span>

</dd> <dt>

<span data-ttu-id="6640c-121">*Smart Card* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6640c-121">*SmartCard* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6640c-122">Specifica se è possibile utilizzare smart card per l'autenticazione con il server Gateway Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="6640c-122">Specifies whether smart cards can be used to authenticate with the RD Gateway server.</span></span>

</dd> <dt>

<span data-ttu-id="6640c-123">*Password* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="6640c-123">*Password* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6640c-124">Specifica se è possibile utilizzare le password per l'autenticazione con il server Gateway Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="6640c-124">Specifies whether passwords can be used to authenticate with the RD Gateway server.</span></span>

</dd> <dt>

<span data-ttu-id="6640c-125">*SecureId* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6640c-125">*SecureId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6640c-126">Questo parametro è riservato per usi futuri.</span><span class="sxs-lookup"><span data-stu-id="6640c-126">This parameter is reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="6640c-127">*Abilitato* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6640c-127">*Enabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6640c-128">Specifica se il CAP RD è abilitato.</span><span class="sxs-lookup"><span data-stu-id="6640c-128">Specifies whether this RD CAP is enabled.</span></span>

</dd> <dt>

<span data-ttu-id="6640c-129">*DeviceRedirectionType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6640c-129">*DeviceRedirectionType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6640c-130">Specifica i tipi di dispositivo che verranno reindirizzati.</span><span class="sxs-lookup"><span data-stu-id="6640c-130">Specifies which device types will be redirected.</span></span>

<dt>

<span data-ttu-id="6640c-131">0</span><span class="sxs-lookup"><span data-stu-id="6640c-131">0</span></span>
</dt> <dd>

<span data-ttu-id="6640c-132">Verranno reindirizzati tutti i dispositivi.</span><span class="sxs-lookup"><span data-stu-id="6640c-132">All devices will be redirected.</span></span>

</dd> <dt>

<span data-ttu-id="6640c-133">1</span><span class="sxs-lookup"><span data-stu-id="6640c-133">1</span></span>
</dt> <dd>

<span data-ttu-id="6640c-134">Non verrà reindirizzato alcun dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6640c-134">No devices will be redirected.</span></span>

</dd> <dt>

<span data-ttu-id="6640c-135">2</span><span class="sxs-lookup"><span data-stu-id="6640c-135">2</span></span>
</dt> <dd>

<span data-ttu-id="6640c-136">I dispositivi specificati non verranno reindirizzati.</span><span class="sxs-lookup"><span data-stu-id="6640c-136">Specified devices will not be redirected.</span></span> <span data-ttu-id="6640c-137">I parametri *DiskDrivesDisabled*, *PrintersDisabled*, *SerialPortsDisabled*, *ClipboardDisabled* e *PlugAndPlayDevicesDisabled* controllano i dispositivi che non verranno reindirizzati.</span><span class="sxs-lookup"><span data-stu-id="6640c-137">The *DiskDrivesDisabled*, *PrintersDisabled*, *SerialPortsDisabled*, *ClipboardDisabled*, and *PlugAndPlayDevicesDisabled* parameters control which devices will not be redirected.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="6640c-138">*DiskDrivesDisabled* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6640c-138">*DiskDrivesDisabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6640c-139">Specifica se disabilitare il reindirizzamento dell'unità disco se il parametro *DeviceRedirectionType* è "2".</span><span class="sxs-lookup"><span data-stu-id="6640c-139">Specifies whether to disable disk drive redirection if the *DeviceRedirectionType* parameter is "2".</span></span>

</dd> <dt>

<span data-ttu-id="6640c-140">*PrintersDisabled* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6640c-140">*PrintersDisabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6640c-141">Specifica se disabilitare il reindirizzamento della stampante se il parametro *DeviceRedirectionType* è "2".</span><span class="sxs-lookup"><span data-stu-id="6640c-141">Specifies whether to disable printer redirection if the *DeviceRedirectionType* parameter is "2".</span></span>

</dd> <dt>

<span data-ttu-id="6640c-142">*SerialPortsDisabled* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6640c-142">*SerialPortsDisabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6640c-143">Specifica se disabilitare il reindirizzamento della porta seriale se il parametro *DeviceRedirectionType* è "2".</span><span class="sxs-lookup"><span data-stu-id="6640c-143">Specifies whether to disable serial port redirection if the *DeviceRedirectionType* parameter is "2".</span></span>

</dd> <dt>

<span data-ttu-id="6640c-144">*ClipboardDisabled* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6640c-144">*ClipboardDisabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6640c-145">Specifica se disabilitare il reindirizzamento degli Appunti se il parametro *DeviceRedirectionType* è "2".</span><span class="sxs-lookup"><span data-stu-id="6640c-145">Specifies whether to disable clipboard redirection if the *DeviceRedirectionType* parameter is "2".</span></span>

</dd> <dt>

<span data-ttu-id="6640c-146">*PlugAndPlayDevicesDisabled* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6640c-146">*PlugAndPlayDevicesDisabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6640c-147">Specifica se disabilitare il reindirizzamento dei dispositivi Plug and Play se il parametro *DeviceRedirectionType* è "2".</span><span class="sxs-lookup"><span data-stu-id="6640c-147">Specifies whether to disable redirection of Plug and Play devices if the *DeviceRedirectionType* parameter is "2".</span></span>

</dd> <dt>

<span data-ttu-id="6640c-148">*IdleTimeout* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6640c-148">*IdleTimeout* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6640c-149">Valore di timeout di inattività in minuti</span><span class="sxs-lookup"><span data-stu-id="6640c-149">Idle timeout value in minutes</span></span>

</dd> <dt>

<span data-ttu-id="6640c-150">*SessionTimeout* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6640c-150">*SessionTimeout* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6640c-151">Valore di timeout della sessione in minuti</span><span class="sxs-lookup"><span data-stu-id="6640c-151">Session timeout value in minutes</span></span>

</dd> <dt>

<span data-ttu-id="6640c-152">*SessionTimeoutAction* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6640c-152">*SessionTimeoutAction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6640c-153">Azione di timeout della sessione in minuti</span><span class="sxs-lookup"><span data-stu-id="6640c-153">Session timeout action in minutes</span></span>

</dd> <dt>

<span data-ttu-id="6640c-154">*AllowOnlySDRServers* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6640c-154">*AllowOnlySDRServers* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6640c-155">Indica se le connessioni sono consentite solo ai server TS SDR</span><span class="sxs-lookup"><span data-stu-id="6640c-155">Whether connections allowed only to SDR TS servers</span></span>

</dd> <dt>

<span data-ttu-id="6640c-156">*CookieAuthentication* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6640c-156">*CookieAuthentication* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6640c-157">Indica se l'autenticazione del cookie può essere utilizzata per la connessione al server Gateway Servizi terminal</span><span class="sxs-lookup"><span data-stu-id="6640c-157">Indicates whether cookie authentication can be used to connect to TS Gateway server</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6640c-158">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6640c-158">Return value</span></span>

<span data-ttu-id="6640c-159">Se il metodo ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="6640c-159">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="6640c-160">Se il metodo ha esito negativo, restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="6640c-160">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="6640c-161">Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="6640c-161">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="6640c-162">Commenti</span><span class="sxs-lookup"><span data-stu-id="6640c-162">Remarks</span></span>

<span data-ttu-id="6640c-163">Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.</span><span class="sxs-lookup"><span data-stu-id="6640c-163">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="6640c-164">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="6640c-164">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="6640c-165">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="6640c-165">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="6640c-166">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="6640c-166">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="6640c-167">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="6640c-167">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="6640c-168">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6640c-168">Requirements</span></span>



| <span data-ttu-id="6640c-169">Requisito</span><span class="sxs-lookup"><span data-stu-id="6640c-169">Requirement</span></span> | <span data-ttu-id="6640c-170">Valore</span><span class="sxs-lookup"><span data-stu-id="6640c-170">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6640c-171">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6640c-171">Minimum supported client</span></span><br/> | <span data-ttu-id="6640c-172">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="6640c-172">None supported</span></span><br/>                                                                |
| <span data-ttu-id="6640c-173">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6640c-173">Minimum supported server</span></span><br/> | <span data-ttu-id="6640c-174">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6640c-174">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="6640c-175">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="6640c-175">Namespace</span></span><br/>                | <span data-ttu-id="6640c-176">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="6640c-176">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="6640c-177">MOF</span><span class="sxs-lookup"><span data-stu-id="6640c-177">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6640c-178"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6640c-178"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="6640c-179">DLL</span><span class="sxs-lookup"><span data-stu-id="6640c-179">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6640c-180"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6640c-180"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="6640c-181">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6640c-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6640c-182">**\_TSGatewayConnectionAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="6640c-182">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

