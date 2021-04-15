---
title: Metodo GetTStoLSConnectivityStatus della classe Win32_TerminalServiceSetting
description: Determina lo stato di connettività tra Servizi Desktop remoto e un server licenze.
ms.assetid: 11fc5865-47e8-4be8-a526-53e29f72d0a4
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo GetTStoLSConnectivityStatus
- Metodo GetTStoLSConnectivityStatus Servizi Desktop remoto, classe Win32_TerminalServiceSetting
- Classe Win32_TerminalServiceSetting Servizi Desktop remoto, metodo GetTStoLSConnectivityStatus
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.GetTStoLSConnectivityStatus
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0fb73cd62c5ab5c343f44f24bbbd8de7f6343a21
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477447"
---
# <a name="gettstolsconnectivitystatus-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="b9871-106">Metodo GetTStoLSConnectivityStatus della \_ classe TerminalServiceSetting Win32</span><span class="sxs-lookup"><span data-stu-id="b9871-106">GetTStoLSConnectivityStatus method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="b9871-107">Determina lo stato di connettività tra Servizi Desktop remoto e un server licenze.</span><span class="sxs-lookup"><span data-stu-id="b9871-107">Determines the connectivity status between Remote Desktop Services and a license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9871-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b9871-108">Syntax</span></span>


```mof
uint32 GetTStoLSConnectivityStatus(
  [in]  string ServerName,
  [out] uint32 TStoLSConnectivityStatus
);
```



## <a name="parameters"></a><span data-ttu-id="b9871-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="b9871-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b9871-110">*Nomeserver* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b9871-110">*ServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b9871-111">Nome del server licenze di cui verificare lo stato di connettività.</span><span class="sxs-lookup"><span data-stu-id="b9871-111">The name of the license server to check the connectivity status of.</span></span>

</dd> <dt>

<span data-ttu-id="b9871-112">*TStoLSConnectivityStatus* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b9871-112">*TStoLSConnectivityStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b9871-113">Valore che indica lo stato di connettività del server licenze.</span><span class="sxs-lookup"><span data-stu-id="b9871-113">A value that indicates the connectivity status of the license server.</span></span> <span data-ttu-id="b9871-114">Può corrispondere a uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="b9871-114">This can be one of the following values.</span></span>

<dt>

<span id="LS_CONNECTABLE_UNKNOWN"></span><span id="ls_connectable_unknown"></span>

<span data-ttu-id="b9871-115"><span id="LS_CONNECTABLE_UNKNOWN"></span><span id="ls_connectable_unknown"></span>**Ls \_ Con connessione \_ sconosciuta** (0)</span><span class="sxs-lookup"><span data-stu-id="b9871-115"><span id="LS_CONNECTABLE_UNKNOWN"></span><span id="ls_connectable_unknown"></span>**LS\_CONNECTABLE\_UNKNOWN** (0)</span></span>


</dt> <dd>

<span data-ttu-id="b9871-116">Impossibile determinare lo stato di connettività.</span><span class="sxs-lookup"><span data-stu-id="b9871-116">The connectivity status cannot be determined.</span></span>

</dd> <dt>

<span id="LS_CONNECTABLE_VALID_WS08R2"></span><span id="ls_connectable_valid_ws08r2"></span>

<span data-ttu-id="b9871-117"><span id="LS_CONNECTABLE_VALID_WS08R2"></span><span id="ls_connectable_valid_ws08r2"></span>**Ls \_ \_ \_ WS08R2 valido collegabile** (1)</span><span class="sxs-lookup"><span data-stu-id="b9871-117"><span id="LS_CONNECTABLE_VALID_WS08R2"></span><span id="ls_connectable_valid_ws08r2"></span>**LS\_CONNECTABLE\_VALID\_WS08R2** (1)</span></span>


</dt> <dd>

<span data-ttu-id="b9871-118">Servizi Desktop remoto possibile connettersi al server licenze Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="b9871-118">Remote Desktop Services can connect to the Windows Server 2008 R2 license server.</span></span>

</dd> <dt>

<span id="LS_CONNECTABLE_VALID_WS08"></span><span id="ls_connectable_valid_ws08"></span>

<span data-ttu-id="b9871-119"><span id="LS_CONNECTABLE_VALID_WS08"></span><span id="ls_connectable_valid_ws08"></span>**Ls \_ \_ \_ WS08 valido collegabile** (2)</span><span class="sxs-lookup"><span data-stu-id="b9871-119"><span id="LS_CONNECTABLE_VALID_WS08"></span><span id="ls_connectable_valid_ws08"></span>**LS\_CONNECTABLE\_VALID\_WS08** (2)</span></span>


</dt> <dd>

<span data-ttu-id="b9871-120">Servizi Desktop remoto possibile connettersi al server licenze Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="b9871-120">Remote Desktop Services can connect to the Windows Server 2008 license server.</span></span>

</dd> <dt>

<span id="LS_CONNECTABLE_BETA_RTM_MISMATCH"></span><span id="ls_connectable_beta_rtm_mismatch"></span>

<span data-ttu-id="b9871-121"><span id="LS_CONNECTABLE_BETA_RTM_MISMATCH"></span><span id="ls_connectable_beta_rtm_mismatch"></span>**Ls \_ \_ \_ \_ Mancata corrispondenza RTM della versione beta** (3)</span><span class="sxs-lookup"><span data-stu-id="b9871-121"><span id="LS_CONNECTABLE_BETA_RTM_MISMATCH"></span><span id="ls_connectable_beta_rtm_mismatch"></span>**LS\_CONNECTABLE\_BETA\_RTM\_MISMATCH** (3)</span></span>


</dt> <dd>

<span data-ttu-id="b9871-122">Servizi Desktop remoto possibile connettersi al server licenze, ma uno dei server esegue una versione beta del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="b9871-122">Remote Desktop Services can connect to the license server, but one of the servers is running a beta version of the operating system.</span></span>

</dd> <dt>

<span id="LS_CONNECTABLE_LOWER_VERSION"></span><span id="ls_connectable_lower_version"></span>

<span data-ttu-id="b9871-123"><span id="LS_CONNECTABLE_LOWER_VERSION"></span><span id="ls_connectable_lower_version"></span>**Ls \_ \_ \_ Versione precedente collegabile** (4)</span><span class="sxs-lookup"><span data-stu-id="b9871-123"><span id="LS_CONNECTABLE_LOWER_VERSION"></span><span id="ls_connectable_lower_version"></span>**LS\_CONNECTABLE\_LOWER\_VERSION** (4)</span></span>


</dt> <dd>

<span data-ttu-id="b9871-124">Servizi Desktop remoto possibile connettersi al server licenze, ma esiste un'incompatibilità tra il server licenze e il server host Servizi Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="b9871-124">Remote Desktop Services can connect to the license server, but there is an incompatibility between the license server and the Remote Desktop Services host server.</span></span>

</dd> <dt>

<span id="LS_CONNECTABLE_NOT_IN_TSCGROUP"></span><span id="ls_connectable_not_in_tscgroup"></span>

<span data-ttu-id="b9871-125"><span id="LS_CONNECTABLE_NOT_IN_TSCGROUP"></span><span id="ls_connectable_not_in_tscgroup"></span>**Ls \_ CONNESSIONE \_ non \_ in \_ TSCGROUP** (5)</span><span class="sxs-lookup"><span data-stu-id="b9871-125"><span id="LS_CONNECTABLE_NOT_IN_TSCGROUP"></span><span id="ls_connectable_not_in_tscgroup"></span>**LS\_CONNECTABLE\_NOT\_IN\_TSCGROUP** (5)</span></span>


</dt> <dd>

<span data-ttu-id="b9871-126">I criteri del gruppo di sicurezza sono abilitati nel server licenze, ma Servizi Desktop remoto non fa parte dei criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="b9871-126">Security group policy is enabled in license server, but Remote Desktop Services is not a part of the group policy.</span></span>

</dd> <dt>

<span id="LS_NOT_CONNECTABLE"></span><span id="ls_not_connectable"></span>

<span data-ttu-id="b9871-127"><span id="LS_NOT_CONNECTABLE"></span><span id="ls_not_connectable"></span>**Ls \_ NON \_ collegabile** (6)</span><span class="sxs-lookup"><span data-stu-id="b9871-127"><span id="LS_NOT_CONNECTABLE"></span><span id="ls_not_connectable"></span>**LS\_NOT\_CONNECTABLE** (6)</span></span>


</dt> <dd>

<span data-ttu-id="b9871-128">Servizi Desktop remoto non è in grado di connettersi al server licenze.</span><span class="sxs-lookup"><span data-stu-id="b9871-128">Remote Desktop Services cannot connect to the license server.</span></span>

</dd> <dt>

<span id="LS_CONNECTABLE_UNKNOWN_VALIDITY"></span><span id="ls_connectable_unknown_validity"></span>

<span data-ttu-id="b9871-129"><span id="LS_CONNECTABLE_UNKNOWN_VALIDITY"></span><span id="ls_connectable_unknown_validity"></span>**Ls \_ \_ \_ Validità di connessione sconosciuta** (7)</span><span class="sxs-lookup"><span data-stu-id="b9871-129"><span id="LS_CONNECTABLE_UNKNOWN_VALIDITY"></span><span id="ls_connectable_unknown_validity"></span>**LS\_CONNECTABLE\_UNKNOWN\_VALIDITY** (7)</span></span>


</dt> <dd>

<span data-ttu-id="b9871-130">Il server licenze può essere connesso a, ma non è possibile determinare la validità della connessione.</span><span class="sxs-lookup"><span data-stu-id="b9871-130">The license server can be connected to, but the validity of the connection cannot be determined.</span></span>

</dd> <dt>

<span id="LS_CONNECTABLE_BUT_ACCESS_DENIED"></span><span id="ls_connectable_but_access_denied"></span>

<span data-ttu-id="b9871-131"><span id="LS_CONNECTABLE_BUT_ACCESS_DENIED"></span><span id="ls_connectable_but_access_denied"></span>**Ls \_ CONNETTIbile \_ ma \_ accesso \_ negato** (8)</span><span class="sxs-lookup"><span data-stu-id="b9871-131"><span id="LS_CONNECTABLE_BUT_ACCESS_DENIED"></span><span id="ls_connectable_but_access_denied"></span>**LS\_CONNECTABLE\_BUT\_ACCESS\_DENIED** (8)</span></span>


</dt> <dd>

<span data-ttu-id="b9871-132">Servizi Desktop remoto possibile connettersi al server licenze, ma l'account utente non dispone dei privilegi di amministratore per il server licenze.</span><span class="sxs-lookup"><span data-stu-id="b9871-132">Remote Desktop Services can connect to the license server, but the user account does not have administrator privileges on the license server.</span></span>

</dd> <dt>

<span id="LS_CONNECTABLE_VALID_WS08R2_VDI"></span><span id="ls_connectable_valid_ws08r2_vdi"></span>

<span data-ttu-id="b9871-133"><span id="LS_CONNECTABLE_VALID_WS08R2_VDI"></span><span id="ls_connectable_valid_ws08r2_vdi"></span>**Ls \_ WS08R2 valido per la connessione \_ \_ \_ VDI** (9)</span><span class="sxs-lookup"><span data-stu-id="b9871-133"><span id="LS_CONNECTABLE_VALID_WS08R2_VDI"></span><span id="ls_connectable_valid_ws08r2_vdi"></span>**LS\_CONNECTABLE\_VALID\_WS08R2\_VDI** (9)</span></span>


</dt> <dd>

<span data-ttu-id="b9871-134">Servizi Desktop remoto possibile connettersi al server Virtual Desktop Infrastructure (VDI) di Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="b9871-134">Remote Desktop Services can connect to the Windows Server 2008 R2 Virtual Desktop Infrastructure (VDI) server.</span></span>

<span data-ttu-id="b9871-135">**Windows Server 2008 R2:** Questo valore non è supportato prima di Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="b9871-135">**Windows Server 2008 R2:** This value is not supported before Windows Server 2012.</span></span>

</dd> <dt>

<span id="LS_CONNECTABLE_FEATURE_NOT_SUPPORTED"></span><span id="ls_connectable_feature_not_supported"></span>

<span data-ttu-id="b9871-136"><span id="LS_CONNECTABLE_FEATURE_NOT_SUPPORTED"></span><span id="ls_connectable_feature_not_supported"></span>**Ls \_ \_Funzionalità connettibile \_ non \_ supportata** (10)</span><span class="sxs-lookup"><span data-stu-id="b9871-136"><span id="LS_CONNECTABLE_FEATURE_NOT_SUPPORTED"></span><span id="ls_connectable_feature_not_supported"></span>**LS\_CONNECTABLE\_FEATURE\_NOT\_SUPPORTED** (10)</span></span>


</dt> <dd>

<span data-ttu-id="b9871-137">La funzionalità non è supportata.</span><span class="sxs-lookup"><span data-stu-id="b9871-137">The feature is not supported.</span></span>

<span data-ttu-id="b9871-138">**Windows server 2008 R2 e Windows server 2008 R2 con SP1:** Questo valore non è supportato prima di Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="b9871-138">**Windows Server 2008 R2 and Windows Server 2008 R2 with SP1:** This value is not supported before Windows Server 2012.</span></span>

</dd> <dt>

<span id="LS_CONNECTABLE_VALID_LS"></span><span id="ls_connectable_valid_ls"></span>

<span data-ttu-id="b9871-139"><span id="LS_CONNECTABLE_VALID_LS"></span><span id="ls_connectable_valid_ls"></span>**Ls \_ \_ \_ Ls valido collegabile** (11)</span><span class="sxs-lookup"><span data-stu-id="b9871-139"><span id="LS_CONNECTABLE_VALID_LS"></span><span id="ls_connectable_valid_ls"></span>**LS\_CONNECTABLE\_VALID\_LS** (11)</span></span>


</dt> <dd>

<span data-ttu-id="b9871-140">Il server licenze è valido.</span><span class="sxs-lookup"><span data-stu-id="b9871-140">The license server is valid.</span></span>

<span data-ttu-id="b9871-141">**Windows server 2008 R2 e Windows server 2008 R2 con SP1:** Questo valore non è supportato prima di Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="b9871-141">**Windows Server 2008 R2 and Windows Server 2008 R2 with SP1:** This value is not supported before Windows Server 2012.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b9871-142">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b9871-142">Return value</span></span>

<span data-ttu-id="b9871-143">Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="b9871-143">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="b9871-144">Per un elenco di questi valori, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="b9871-144">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="b9871-145">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b9871-145">Requirements</span></span>



| <span data-ttu-id="b9871-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="b9871-146">Requirement</span></span> | <span data-ttu-id="b9871-147">Valore</span><span class="sxs-lookup"><span data-stu-id="b9871-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b9871-148">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b9871-148">Minimum supported client</span></span><br/> | <span data-ttu-id="b9871-149">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="b9871-149">None supported</span></span><br/>                                                               |
| <span data-ttu-id="b9871-150">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b9871-150">Minimum supported server</span></span><br/> | <span data-ttu-id="b9871-151">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b9871-151">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="b9871-152">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b9871-152">Namespace</span></span><br/>                | <span data-ttu-id="b9871-153">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="b9871-153">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="b9871-154">MOF</span><span class="sxs-lookup"><span data-stu-id="b9871-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b9871-155"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b9871-155"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="b9871-156">DLL</span><span class="sxs-lookup"><span data-stu-id="b9871-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b9871-157"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b9871-157"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b9871-158">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b9871-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9871-159">**\_TerminalServiceSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="b9871-159">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

 





