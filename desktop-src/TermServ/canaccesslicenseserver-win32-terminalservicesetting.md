---
title: Metodo CanAccessLicenseServer della classe Win32_TerminalServiceSetting
description: CanAccessLicenseServer non è più disponibile.
ms.assetid: b09fa901-8ae1-431e-8d97-27ee84a84779
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo CanAccessLicenseServer
- Metodo CanAccessLicenseServer Servizi Desktop remoto, classe Win32_TerminalServiceSetting
- Classe Win32_TerminalServiceSetting Servizi Desktop remoto, metodo CanAccessLicenseServer
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.CanAccessLicenseServer
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ffa5bd0e108c0ccceed6890adedea7901834804
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119279"
---
# <a name="canaccesslicenseserver-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="93a1a-106">Metodo CanAccessLicenseServer della \_ classe TerminalServiceSetting Win32</span><span class="sxs-lookup"><span data-stu-id="93a1a-106">CanAccessLicenseServer method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="93a1a-107">\[**CanAccessLicenseServer** non è più disponibile per l'uso a partire da Windows Server 2008 R2.\]</span><span class="sxs-lookup"><span data-stu-id="93a1a-107">\[**CanAccessLicenseServer** is no longer available for use as of Windows Server 2008 R2.\]</span></span>

<span data-ttu-id="93a1a-108">\* \* Windows Server 2008: \* \*</span><span class="sxs-lookup"><span data-stu-id="93a1a-108">\*\*Windows Server 2008:  \*\*</span></span>

<span data-ttu-id="93a1a-109">Determina se il server di host sessione Desktop remoto (host sessione Desktop remoto) può richiedere Servizi Desktop remoto licenze CAL (Client Access License) da un server Desktop remoto License basato sui seguenti elementi:</span><span class="sxs-lookup"><span data-stu-id="93a1a-109">Determines whether the Remote Desktop Session Host (RD Session Host) server is allowed to request Remote Desktop Services client access licenses (RDS CALs) from a Remote Desktop license server based on the following:</span></span>

-   <span data-ttu-id="93a1a-110">Impostazione dei criteri di gruppo "gruppo di sicurezza del server licenze" nel server licenze Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="93a1a-110">The "license server security group" group policy setting on the Remote Desktop license server.</span></span>
-   <span data-ttu-id="93a1a-111">Appartenenza al gruppo locale computer Terminal Server nel server licenze.</span><span class="sxs-lookup"><span data-stu-id="93a1a-111">Membership in the Terminal Server Computers local group on the license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="93a1a-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="93a1a-112">Syntax</span></span>


```mof
uint32 CanAccessLicenseServer(
  [in]  string ServerName,
  [out] uint32 AccessAllowed
);
```



## <a name="parameters"></a><span data-ttu-id="93a1a-113">Parametri</span><span class="sxs-lookup"><span data-stu-id="93a1a-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93a1a-114">*Nomeserver* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="93a1a-114">*ServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93a1a-115">Nome del server licenze Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="93a1a-115">The name of the Remote Desktop license server.</span></span>

</dd> <dt>

<span data-ttu-id="93a1a-116">*AccessAllowed* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="93a1a-116">*AccessAllowed* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="93a1a-117">Indica se il server Host sessione Desktop remoto è autorizzato a richiedere licenze CAL Servizi Desktop remoto dal server licenze.</span><span class="sxs-lookup"><span data-stu-id="93a1a-117">Whether the RD Session Host server is allowed to request RDS CALs from the license server.</span></span>

<dt>

<span data-ttu-id="93a1a-118">0</span><span class="sxs-lookup"><span data-stu-id="93a1a-118">0</span></span>
</dt> <dd>

<span data-ttu-id="93a1a-119">La richiesta è consentita.</span><span class="sxs-lookup"><span data-stu-id="93a1a-119">The request is allowed.</span></span>

</dd> <dt>

<span data-ttu-id="93a1a-120">1</span><span class="sxs-lookup"><span data-stu-id="93a1a-120">1</span></span>
</dt> <dd>

<span data-ttu-id="93a1a-121">La richiesta non è consentita.</span><span class="sxs-lookup"><span data-stu-id="93a1a-121">The request is not allowed.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93a1a-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="93a1a-122">Return value</span></span>

<span data-ttu-id="93a1a-123">Restituisce **\_ OK** se il server Host sessione Desktop remoto ha accesso al server licenze.</span><span class="sxs-lookup"><span data-stu-id="93a1a-123">Returns **S\_OK** if the RD Session Host server has access to the license server.</span></span> <span data-ttu-id="93a1a-124">Restituisce **\_ false** se il server Host sessione Desktop remoto non dispone dell'accesso al server licenze.</span><span class="sxs-lookup"><span data-stu-id="93a1a-124">Returns **S\_FALSE** if the RD Session Host server does not have access to the license server.</span></span>

## <a name="remarks"></a><span data-ttu-id="93a1a-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="93a1a-125">Remarks</span></span>

<span data-ttu-id="93a1a-126">L'impostazione dei criteri "gruppo di sicurezza del server licenze" consente di specificare i server Host sessione Desktop remoto autorizzati a contattare il server licenze per ottenere le licenze CAL Servizi Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="93a1a-126">The "license server security group" policy setting allows you to specify the RD Session Host servers that are permitted to contact the license server to obtain RDS CALs.</span></span> <span data-ttu-id="93a1a-127">Se l'impostazione dei criteri è abilitata nel server licenze, il server licenze risponderà solo alle richieste CAL Servizi Desktop remoto dei server Host sessione Desktop remoto i cui account computer sono membri del gruppo locale computer Terminal Server nel server licenze.</span><span class="sxs-lookup"><span data-stu-id="93a1a-127">If the policy setting is enabled on the license server, the license server will only respond to RDS CAL requests from RD Session Host servers whose computer accounts are members of the Terminal Server Computers local group on the license server.</span></span>

<span data-ttu-id="93a1a-128">Per connettersi allo \\ \\ \\ spazio dei nomi CIMV2 TerminalServices radice, il livello di autenticazione deve includere la riservatezza dei pacchetti.</span><span class="sxs-lookup"><span data-stu-id="93a1a-128">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="93a1a-129">Per le chiamate C/C++, si tratta di un livello di autenticazione del livello di autenticazione **RPC \_ C \_ \_ \_ PKT \_ privacy**.</span><span class="sxs-lookup"><span data-stu-id="93a1a-129">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="93a1a-130">Per Visual Basic e le chiamate di scripting, si tratta di un livello di autenticazione di **WbemAuthenticationLevelPktPrivacy** o "su PktPrivacy", con un valore pari a 6.</span><span class="sxs-lookup"><span data-stu-id="93a1a-130">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="93a1a-131">Il seguente esempio di Visual Basic Scripting Edition (VBScript) illustra come connettersi a un computer remoto con la privacy dei pacchetti.</span><span class="sxs-lookup"><span data-stu-id="93a1a-131">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="93a1a-132">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="93a1a-132">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="93a1a-133">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="93a1a-133">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="93a1a-134">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="93a1a-134">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="93a1a-135">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="93a1a-135">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="93a1a-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="93a1a-136">Requirements</span></span>



| <span data-ttu-id="93a1a-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="93a1a-137">Requirement</span></span> | <span data-ttu-id="93a1a-138">Valore</span><span class="sxs-lookup"><span data-stu-id="93a1a-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="93a1a-139">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="93a1a-139">Minimum supported client</span></span><br/> | <span data-ttu-id="93a1a-140">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="93a1a-140">None supported</span></span><br/>                                                               |
| <span data-ttu-id="93a1a-141">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="93a1a-141">Minimum supported server</span></span><br/> | <span data-ttu-id="93a1a-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="93a1a-142">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="93a1a-143">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="93a1a-143">End of client support</span></span><br/>    | <span data-ttu-id="93a1a-144">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="93a1a-144">None supported</span></span><br/>                                                               |
| <span data-ttu-id="93a1a-145">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="93a1a-145">End of server support</span></span><br/>    | <span data-ttu-id="93a1a-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="93a1a-146">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="93a1a-147">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="93a1a-147">Namespace</span></span><br/>                | <span data-ttu-id="93a1a-148">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="93a1a-148">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="93a1a-149">MOF</span><span class="sxs-lookup"><span data-stu-id="93a1a-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="93a1a-150"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="93a1a-150"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="93a1a-151">DLL</span><span class="sxs-lookup"><span data-stu-id="93a1a-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="93a1a-152"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="93a1a-152"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93a1a-153">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="93a1a-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93a1a-154">**\_TerminalServiceSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="93a1a-154">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

