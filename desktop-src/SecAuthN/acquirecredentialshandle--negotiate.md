---
description: Acquisisce un handle per le credenziali preesistenti di un'entità di sicurezza che utilizza Negotiate.
ms.assetid: ff372163-c73b-41bb-afcb-7d5de7720967
title: Funzione AcquireCredentialsHandle (Negotiate) (SSPI. h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 80ab4b67866b60831dadb7d8eb9bf9f632c0661c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316240"
---
# <a name="acquirecredentialshandle-negotiate-function"></a><span data-ttu-id="c3f67-103">Funzione AcquireCredentialsHandle (Negotiate)</span><span class="sxs-lookup"><span data-stu-id="c3f67-103">AcquireCredentialsHandle (Negotiate) function</span></span>

<span data-ttu-id="c3f67-104">La funzione **AcquireCredentialsHandle (Negotiate)** acquisisce un handle per le credenziali preesistenti di un' [*entità di sicurezza*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="c3f67-104">The **AcquireCredentialsHandle (Negotiate)** function acquires a handle to preexisting credentials of a [*security principal*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="c3f67-105">Questo handle è richiesto dalle funzioni [**InitializeSecurityContext (Negotiate)**](initializesecuritycontext--negotiate.md) e [**AcceptSecurityContext (Negotiate)**](acceptsecuritycontext--negotiate.md) .</span><span class="sxs-lookup"><span data-stu-id="c3f67-105">This handle is required by the [**InitializeSecurityContext (Negotiate)**](initializesecuritycontext--negotiate.md) and [**AcceptSecurityContext (Negotiate)**](acceptsecuritycontext--negotiate.md) functions.</span></span> <span data-ttu-id="c3f67-106">Possono essere *credenziali* preesistenti, stabilite tramite un accesso di sistema non descritto in questo argomento, oppure il chiamante può fornire credenziali alternative.</span><span class="sxs-lookup"><span data-stu-id="c3f67-106">These can be either preexisting *credentials*, which are established through a system logon that is not described here, or the caller can provide alternative credentials.</span></span>

> [!Note]  
> <span data-ttu-id="c3f67-107">Non si tratta di un "accesso alla rete" e non implica la raccolta delle credenziali.</span><span class="sxs-lookup"><span data-stu-id="c3f67-107">This is not a "log on to the network" and does not imply gathering of credentials.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="c3f67-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c3f67-108">Syntax</span></span>


```C++
SECURITY_STATUS SEC_Entry AcquireCredentialsHandle(
  _In_  SEC_CHAR       *pszPrincipal,
  _In_  SEC_CHAR       *pszPackage,
  _In_  ULONG          fCredentialUse,
  _In_  PLUID          pvLogonID,
  _In_  PVOID          pAuthData,
  _In_  SEC_GET_KEY_FN pGetKeyFn,
  _In_  PVOID          pvGetKeyArgument,
  _Out_ PCredHandle    phCredential,
  _Out_ PTimeStamp     ptsExpiry
);
```



## <a name="parameters"></a><span data-ttu-id="c3f67-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="c3f67-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3f67-110">*pszPrincipal* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c3f67-110">*pszPrincipal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3f67-111">Puntatore a una stringa con terminazione null che specifica il nome dell'entità le cui credenziali faranno riferimento all'handle.</span><span class="sxs-lookup"><span data-stu-id="c3f67-111">A pointer to a null-terminated string that specifies the name of the principal whose credentials the handle will reference.</span></span>

> [!Note]  
> <span data-ttu-id="c3f67-112">Se il processo che richiede l'handle non ha accesso alle credenziali, la funzione restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="c3f67-112">If the process that requests the handle does not have access to the credentials, the function returns an error.</span></span> <span data-ttu-id="c3f67-113">Una stringa null indica che il processo richiede un handle per le credenziali dell'utente con il [*contesto di sicurezza*](../secgloss/s-gly.md) in cui è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="c3f67-113">A null string indicates that the process requires a handle to the credentials of the user under whose [*security context*](../secgloss/s-gly.md) it is executing.</span></span>

 

</dd> <dt>

<span data-ttu-id="c3f67-114">*pszPackage* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c3f67-114">*pszPackage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3f67-115">Puntatore a una stringa con terminazione null che specifica il nome del [*pacchetto di sicurezza*](../secgloss/s-gly.md) con cui verranno utilizzate queste credenziali.</span><span class="sxs-lookup"><span data-stu-id="c3f67-115">A pointer to a null-terminated string that specifies the name of the [*security package*](../secgloss/s-gly.md) with which these credentials will be used.</span></span> <span data-ttu-id="c3f67-116">Nome del [*pacchetto di sicurezza*](../secgloss/s-gly.md) restituito nel membro del **nome** di una struttura [**SecPkgInfo**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) restituita dalla funzione [**EnumerateSecurityPackages**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) .</span><span class="sxs-lookup"><span data-stu-id="c3f67-116">This is a [*security package*](../secgloss/s-gly.md) name returned in the **Name** member of a [**SecPkgInfo**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) structure returned by the [**EnumerateSecurityPackages**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) function.</span></span> <span data-ttu-id="c3f67-117">Dopo aver stabilito un contesto, è possibile chiamare [**QueryContextAttributes (Negotiate)**](querycontextattributes--negotiate.md) con *ULATTRIBUTE* impostato su SECPKG \_ attr \_ package \_ info per restituire informazioni sul [*pacchetto di sicurezza*](../secgloss/s-gly.md) in uso.</span><span class="sxs-lookup"><span data-stu-id="c3f67-117">After a context is established, [**QueryContextAttributes (Negotiate)**](querycontextattributes--negotiate.md) can be called with *ulAttribute* set to SECPKG\_ATTR\_PACKAGE\_INFO to return information on the [*security package*](../secgloss/s-gly.md) in use.</span></span>

<span data-ttu-id="c3f67-118">Per chiamare correttamente questa funzione utilizzando il provider di servizi condivisi Negotiate, impostare questo parametro su "Negotiate".</span><span class="sxs-lookup"><span data-stu-id="c3f67-118">To successfully call this function using the Negotiate SSP, set this parameter to "Negotiate".</span></span>

</dd> <dt>

<span data-ttu-id="c3f67-119">*fCredentialUse* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c3f67-119">*fCredentialUse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3f67-120">Flag che indica il modo in cui verranno utilizzate queste credenziali.</span><span class="sxs-lookup"><span data-stu-id="c3f67-120">A flag that indicates how these credentials will be used.</span></span> <span data-ttu-id="c3f67-121">Questo parametro può avere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="c3f67-121">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="c3f67-122">Valore</span><span class="sxs-lookup"><span data-stu-id="c3f67-122">Value</span></span>                                                                                                                                                                                                                                                                                    | <span data-ttu-id="c3f67-123">Significato</span><span class="sxs-lookup"><span data-stu-id="c3f67-123">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SECPKG_CRED_AUTOLOGON_RESTRICTED"></span><span id="secpkg_cred_autologon_restricted"></span><dl> <span data-ttu-id="c3f67-124"><dt>**SECPKG \_ 0x00000010 con \_ \_ accesso automatico cred**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="c3f67-124"><dt>**SECPKG\_CRED\_AUTOLOGON\_RESTRICTED**</dt> <dt>0x00000010</dt></span></span> </dl> | <span data-ttu-id="c3f67-125">Per la sicurezza non vengono utilizzate credenziali di accesso predefinite o credenziali di [Gestione credenziali](credential-manager.md).</span><span class="sxs-lookup"><span data-stu-id="c3f67-125">The security does not use default logon credentials or credentials from [Credential Manager](credential-manager.md).</span></span><br/> <span data-ttu-id="c3f67-126">**Windows server 2008, Windows Vista, Windows server 2003 e Windows XP:** Questo valore non è supportato.</span><span class="sxs-lookup"><span data-stu-id="c3f67-126">**Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** This value is not supported.</span></span><br/>                                                                                                                                                                                                                    |
| <span id="SECPKG_CRED_BOTH"></span><span id="secpkg_cred_both"></span><dl> <span data-ttu-id="c3f67-127"><dt>**SECPKG \_ cred \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c3f67-127"><dt>**SECPKG\_CRED\_BOTH**</dt></span></span> </dl>                                                                                                                  | <span data-ttu-id="c3f67-128">Convalidare le credenziali in ingresso o usare una credenziale locale per preparare un token in uscita.</span><span class="sxs-lookup"><span data-stu-id="c3f67-128">Validate an incoming credential or use a local credential to prepare an outgoing token.</span></span> <span data-ttu-id="c3f67-129">Questo flag Abilita entrambi gli altri flag.</span><span class="sxs-lookup"><span data-stu-id="c3f67-129">This flag enables both other flags.</span></span><br/>                                                                                                                                                                                                                                                                                                                                  |
| <span id="SECPKG_CRED_INBOUND"></span><span id="secpkg_cred_inbound"></span><dl> <span data-ttu-id="c3f67-130"><dt>**SECPKG \_ cred in \_ ingresso**</dt></span><span class="sxs-lookup"><span data-stu-id="c3f67-130"><dt>**SECPKG\_CRED\_INBOUND**</dt></span></span> </dl>                                                                                                         | <span data-ttu-id="c3f67-131">Convalidare le credenziali del server in ingresso.</span><span class="sxs-lookup"><span data-stu-id="c3f67-131">Validate an incoming server credential.</span></span> <span data-ttu-id="c3f67-132">Le credenziali in ingresso possono essere convalidate tramite un'autorità di autenticazione quando viene chiamato [**InitializeSecurityContext (Negotiate)**](initializesecuritycontext--negotiate.md) o [**AcceptSecurityContext (Negotiate)**](acceptsecuritycontext--negotiate.md) .</span><span class="sxs-lookup"><span data-stu-id="c3f67-132">Inbound credentials might be validated by using an authenticating authority when [**InitializeSecurityContext (Negotiate)**](initializesecuritycontext--negotiate.md) or [**AcceptSecurityContext (Negotiate)**](acceptsecuritycontext--negotiate.md) is called.</span></span> <span data-ttu-id="c3f67-133">Se tale autorità non è disponibile, la funzione avrà esito negativo e restituirà il secondo \_ e \_ Nessuna \_ autorità di autenticazione \_ .</span><span class="sxs-lookup"><span data-stu-id="c3f67-133">If such an authority is not available, the function will fail and return SEC\_E\_NO\_AUTHENTICATING\_AUTHORITY.</span></span> <span data-ttu-id="c3f67-134">La convalida è specifica del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="c3f67-134">Validation is package specific.</span></span><br/> |
| <span id="SECPKG_CRED_OUTBOUND"></span><span id="secpkg_cred_outbound"></span><dl> <span data-ttu-id="c3f67-135"><dt>**SECPKG \_ cred in \_ uscita**</dt></span><span class="sxs-lookup"><span data-stu-id="c3f67-135"><dt>**SECPKG\_CRED\_OUTBOUND**</dt></span></span> </dl>                                                                                                      | <span data-ttu-id="c3f67-136">Consentire a una credenziale client locale di preparare un token in uscita.</span><span class="sxs-lookup"><span data-stu-id="c3f67-136">Allow a local client credential to prepare an outgoing token.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                |
| <span id="SECPKG_CRED_PROCESS_POLICY_ONLY"></span><span id="secpkg_cred_process_policy_only"></span><dl> <span data-ttu-id="c3f67-137"><dt>**SECPKG \_ \_ \_ \_ Solo criteri di processo cred**</dt> <dt>0x00000020</dt></span><span class="sxs-lookup"><span data-stu-id="c3f67-137"><dt>**SECPKG\_CRED\_PROCESS\_POLICY\_ONLY**</dt> <dt>0x00000020</dt></span></span> </dl>   | <span data-ttu-id="c3f67-138">La funzione elabora i criteri del server e restituisce il **secondo \_ e \_ Nessuna \_ credenziale**, a indicare che l'applicazione deve richiedere le credenziali.</span><span class="sxs-lookup"><span data-stu-id="c3f67-138">The function processes server policy and returns **SEC\_E\_NO\_CREDENTIALS**, indicating that the application should prompt for credentials.</span></span><br/> <span data-ttu-id="c3f67-139">**Windows server 2008, Windows Vista, Windows server 2003 e Windows XP:** Questo valore non è supportato.</span><span class="sxs-lookup"><span data-stu-id="c3f67-139">**Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** This value is not supported.</span></span><br/>                                                                                                                                                                                             |



 

</dd> <dt>

<span data-ttu-id="c3f67-140">*pvLogonID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c3f67-140">*pvLogonID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3f67-141">Puntatore a un [*identificatore univoco locale*](../secgloss/l-gly.md) (LUID) che identifica l'utente.</span><span class="sxs-lookup"><span data-stu-id="c3f67-141">A pointer to a [*locally unique identifier*](../secgloss/l-gly.md) (LUID) that identifies the user.</span></span> <span data-ttu-id="c3f67-142">Questo parametro viene fornito per i processi di file System, ad esempio i redirector di rete.</span><span class="sxs-lookup"><span data-stu-id="c3f67-142">This parameter is provided for file-system processes such as network redirectors.</span></span> <span data-ttu-id="c3f67-143">Questo parametro può essere **NULL**.</span><span class="sxs-lookup"><span data-stu-id="c3f67-143">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c3f67-144">*pAuthData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c3f67-144">*pAuthData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3f67-145">Puntatore ai dati specifici del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="c3f67-145">A pointer to package-specific data.</span></span> <span data-ttu-id="c3f67-146">Questo parametro può essere **null**, a indicare che è necessario utilizzare le credenziali predefinite per il [*pacchetto di sicurezza*](../secgloss/s-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="c3f67-146">This parameter can be **NULL**, which indicates that the default credentials for that [*security package*](../secgloss/s-gly.md) must be used.</span></span> <span data-ttu-id="c3f67-147">Per usare le credenziali specificate, passare una struttura **\_ \_ \_ \_ opaca dell'identità di autenticazione WinNT PSEC** restituita da una chiamata precedente alla funzione [**SspiPromptForCredentials**](/windows/win32/api/sspi/nf-sspi-sspipromptforcredentialsa) .</span><span class="sxs-lookup"><span data-stu-id="c3f67-147">To use supplied credentials, pass a **PSEC\_WINNT\_AUTH\_IDENTITY\_OPAQUE** structure returned from a previous call to the [**SspiPromptForCredentials**](/windows/win32/api/sspi/nf-sspi-sspipromptforcredentialsa) function.</span></span>

<span data-ttu-id="c3f67-148">**Windows server 2008, Windows Vista, Windows server 2003 e Windows XP:** Il **tipo \_ \_ opaco di \_ identità \_ di autenticazione WinNT PSEC** e la funzione [**SspiPromptForCredentials**](/windows/win32/api/sspi/nf-sspi-sspipromptforcredentialsa) non sono supportati.</span><span class="sxs-lookup"><span data-stu-id="c3f67-148">**Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** The **PSEC\_WINNT\_AUTH\_IDENTITY\_OPAQUE** type and the [**SspiPromptForCredentials**](/windows/win32/api/sspi/nf-sspi-sspipromptforcredentialsa) function are not supported.</span></span> <span data-ttu-id="c3f67-149">Per usare le credenziali specificate, passare un puntatore a un' [**\_ identità di \_ autenticazione \_ WinNT di secondo**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) o a una struttura di [**\_ \_ \_ identità \_ di autorizzazione WinNT sec**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_ex2) , che include le credenziali.</span><span class="sxs-lookup"><span data-stu-id="c3f67-149">To use supplied credentials, pass a pointer to either a [**SEC\_WINNT\_AUTH\_IDENTITY**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) or [**SEC\_WINNT\_AUTH\_IDENTITY\_EX**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_ex2) structure that includes those credentials.</span></span>

<span data-ttu-id="c3f67-150">Il tempo di esecuzione RPC passa ciò che è stato fornito in [**RpcBindingSetAuthInfo**](/windows/win32/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfo).</span><span class="sxs-lookup"><span data-stu-id="c3f67-150">The RPC run time passes whatever was provided in [**RpcBindingSetAuthInfo**](/windows/win32/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfo).</span></span>

<span data-ttu-id="c3f67-151">Quando si utilizza il pacchetto Negotiate, le lunghezze dei caratteri massime per nome utente, password e dominio sono rispettivamente 256, 256 e 15.</span><span class="sxs-lookup"><span data-stu-id="c3f67-151">When using the Negotiate package, the maximum character lengths for user name, password, and domain are 256, 256, and 15, respectively.</span></span>

</dd> <dt>

<span data-ttu-id="c3f67-152">*pGetKeyFn* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c3f67-152">*pGetKeyFn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3f67-153">Questo parametro non viene utilizzato e deve essere impostato su **null**.</span><span class="sxs-lookup"><span data-stu-id="c3f67-153">This parameter is not used and should be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c3f67-154">*pvGetKeyArgument* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c3f67-154">*pvGetKeyArgument* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3f67-155">Questo parametro non viene utilizzato e deve essere impostato su **null**.</span><span class="sxs-lookup"><span data-stu-id="c3f67-155">This parameter is not used and should be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c3f67-156">*phCredential* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="c3f67-156">*phCredential* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c3f67-157">Puntatore a una struttura [CredHandle](sspi-handles.md) per la ricezione dell'handle delle credenziali.</span><span class="sxs-lookup"><span data-stu-id="c3f67-157">A pointer to a [CredHandle](sspi-handles.md) structure to receive the credential handle.</span></span>

</dd> <dt>

<span data-ttu-id="c3f67-158">*ptsExpiry* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="c3f67-158">*ptsExpiry* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c3f67-159">Puntatore a una struttura di [**timestamp**](timestamp.md) che riceve l'ora di scadenza delle credenziali restituite.</span><span class="sxs-lookup"><span data-stu-id="c3f67-159">A pointer to a [**TimeStamp**](timestamp.md) structure that receives the time at which the returned credentials expire.</span></span> <span data-ttu-id="c3f67-160">Il valore restituito in questa struttura di **timestamp** dipende dalla [*delega vincolata*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="c3f67-160">The value returned in this **TimeStamp** structure depends on the [*constrained delegation*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="c3f67-161">Il [*pacchetto di sicurezza*](../secgloss/s-gly.md) deve restituire questo valore nell'ora locale.</span><span class="sxs-lookup"><span data-stu-id="c3f67-161">The [*security package*](../secgloss/s-gly.md) must return this value in local time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3f67-162">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c3f67-162">Return value</span></span>

<span data-ttu-id="c3f67-163">Se la funzione ha esito positivo, la funzione restituisce SEC \_ E \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c3f67-163">If the function succeeds, the function returns SEC\_E\_OK.</span></span>

<span data-ttu-id="c3f67-164">Se la funzione ha esito negativo, restituisce uno dei codici di errore seguenti.</span><span class="sxs-lookup"><span data-stu-id="c3f67-164">If the function fails, it returns one of the following error codes.</span></span>



| <span data-ttu-id="c3f67-165">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="c3f67-165">Return code</span></span>                                                                                                 | <span data-ttu-id="c3f67-166">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c3f67-166">Description</span></span>                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c3f67-167"><dt>**SEC \_ E \_ memoria insufficiente \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c3f67-167"><dt>**SEC\_E\_INSUFFICIENT\_MEMORY**</dt></span></span> </dl> | <span data-ttu-id="c3f67-168">La memoria disponibile non è sufficiente per completare l'azione richiesta.</span><span class="sxs-lookup"><span data-stu-id="c3f67-168">There is not enough memory available to complete the requested action.</span></span><br/>                                                                  |
| <dl> <span data-ttu-id="c3f67-169"><dt>**\_ \_ errore interno sec \_ E**</dt></span><span class="sxs-lookup"><span data-stu-id="c3f67-169"><dt>**SEC\_E\_INTERNAL\_ERROR**</dt></span></span> </dl>      | <span data-ttu-id="c3f67-170">Si è verificato un errore che non è stato mappato a un codice di errore SSPI.</span><span class="sxs-lookup"><span data-stu-id="c3f67-170">An error occurred that did not map to an SSPI error code.</span></span><br/>                                                                               |
| <dl> <span data-ttu-id="c3f67-171"><dt>**SEC \_ E \_ Nessuna \_ credenziale**</dt></span><span class="sxs-lookup"><span data-stu-id="c3f67-171"><dt>**SEC\_E\_NO\_CREDENTIALS**</dt></span></span> </dl>      | <span data-ttu-id="c3f67-172">Nessuna credenziale disponibile nella [*delega vincolata*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="c3f67-172">No credentials are available in the [*constrained delegation*](../secgloss/s-gly.md).</span></span><br/> |
| <dl> <span data-ttu-id="c3f67-173"><dt>**SEC \_ E \_ non \_ proprietario**</dt></span><span class="sxs-lookup"><span data-stu-id="c3f67-173"><dt>**SEC\_E\_NOT\_OWNER**</dt></span></span> </dl>           | <span data-ttu-id="c3f67-174">Il chiamante della funzione non ha le credenziali necessarie.</span><span class="sxs-lookup"><span data-stu-id="c3f67-174">The caller of the function does not have the necessary credentials.</span></span><br/>                                                                     |
| <dl> <span data-ttu-id="c3f67-175"><dt>**SEC \_ E \_ SECPKG \_ non \_ trovati**</dt></span><span class="sxs-lookup"><span data-stu-id="c3f67-175"><dt>**SEC\_E\_SECPKG\_NOT\_FOUND**</dt></span></span> </dl>   | <span data-ttu-id="c3f67-176">Il [*pacchetto di sicurezza*](../secgloss/s-gly.md) richiesto non esiste.</span><span class="sxs-lookup"><span data-stu-id="c3f67-176">The requested [*security package*](../secgloss/s-gly.md) does not exist.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="c3f67-177"><dt>**SEC \_ E \_ \_ credenziali sconosciute**</dt></span><span class="sxs-lookup"><span data-stu-id="c3f67-177"><dt>**SEC\_E\_UNKNOWN\_CREDENTIALS**</dt></span></span> </dl> | <span data-ttu-id="c3f67-178">Le credenziali fornite al pacchetto non sono state riconosciute.</span><span class="sxs-lookup"><span data-stu-id="c3f67-178">The credentials supplied to the package were not recognized.</span></span><br/>                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="c3f67-179">Commenti</span><span class="sxs-lookup"><span data-stu-id="c3f67-179">Remarks</span></span>

<span data-ttu-id="c3f67-180">La funzione **AcquireCredentialsHandle (Negotiate)** restituisce un handle per le credenziali di un'entità, ad esempio un utente o un client, come usato da una [*delega vincolata*](../secgloss/s-gly.md)specifica.</span><span class="sxs-lookup"><span data-stu-id="c3f67-180">The **AcquireCredentialsHandle (Negotiate)** function returns a handle to the credentials of a principal, such as a user or client, as used by a specific [*constrained delegation*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="c3f67-181">Può trattarsi dell'handle per le credenziali preesistenti oppure la funzione può creare un nuovo set di credenziali e restituirlo.</span><span class="sxs-lookup"><span data-stu-id="c3f67-181">This can be the handle to preexisting credentials, or the function can create a new set of credentials and return it.</span></span> <span data-ttu-id="c3f67-182">Questo handle può essere usato nelle chiamate successive alle funzioni [**AcceptSecurityContext (Negotiate)**](acceptsecuritycontext--negotiate.md) e [**InitializeSecurityContext (Negotiate)**](initializesecuritycontext--negotiate.md) .</span><span class="sxs-lookup"><span data-stu-id="c3f67-182">This handle can be used in subsequent calls to the [**AcceptSecurityContext (Negotiate)**](acceptsecuritycontext--negotiate.md) and [**InitializeSecurityContext (Negotiate)**](initializesecuritycontext--negotiate.md) functions.</span></span>

<span data-ttu-id="c3f67-183">In generale, **AcquireCredentialsHandle (Negotiate)** non consente a un processo di ottenere un handle per le credenziali di altri utenti connessi allo stesso computer.</span><span class="sxs-lookup"><span data-stu-id="c3f67-183">In general, **AcquireCredentialsHandle (Negotiate)** does not allow a process to obtain a handle to the credentials of other users logged on to the same computer.</span></span> <span data-ttu-id="c3f67-184">Tuttavia, un chiamante con \_ \_ [*privilegi*](../secgloss/s-gly.md) per il nome TCB ha la possibilità di specificare l' [*identificatore di accesso*](../secgloss/l-gly.md) (LUID) di qualsiasi token di sessione di accesso esistente per ottenere un handle per le credenziali della sessione.</span><span class="sxs-lookup"><span data-stu-id="c3f67-184">However, a caller with SE\_TCB\_NAME [*privilege*](../secgloss/s-gly.md) has the option of specifying the [*logon identifier*](../secgloss/l-gly.md) (LUID) of any existing logon session token to get a handle to that session's credentials.</span></span> <span data-ttu-id="c3f67-185">Questa operazione viene in genere utilizzata dai moduli in modalità kernel che devono agire per conto di un utente connesso.</span><span class="sxs-lookup"><span data-stu-id="c3f67-185">Typically, this is used by kernel-mode modules that must act on behalf of a logged-on user.</span></span>

<span data-ttu-id="c3f67-186">Un pacchetto può chiamare la funzione in *pGetKeyFn* fornita dal trasporto di run-time RPC.</span><span class="sxs-lookup"><span data-stu-id="c3f67-186">A package might call the function in *pGetKeyFn* provided by the RPC run-time transport.</span></span> <span data-ttu-id="c3f67-187">Se il trasporto non supporta la nozione di callback per recuperare le credenziali, questo parametro deve essere **null**.</span><span class="sxs-lookup"><span data-stu-id="c3f67-187">If the transport does not support the notion of callback to retrieve credentials, this parameter must be **NULL**.</span></span>

<span data-ttu-id="c3f67-188">Per i chiamanti in modalità kernel, è necessario notare le differenze seguenti:</span><span class="sxs-lookup"><span data-stu-id="c3f67-188">For kernel mode callers, the following differences must be noted:</span></span>

-   <span data-ttu-id="c3f67-189">I due parametri di stringa devono essere stringhe [*Unicode*](../secgloss/u-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="c3f67-189">The two string parameters must be [*Unicode*](../secgloss/u-gly.md) strings.</span></span>
-   <span data-ttu-id="c3f67-190">I valori del buffer devono essere allocati nella memoria virtuale del processo, non dal pool.</span><span class="sxs-lookup"><span data-stu-id="c3f67-190">The buffer values must be allocated in process virtual memory, not from the pool.</span></span>

<span data-ttu-id="c3f67-191">Al termine dell'utilizzo delle credenziali restituite, liberare la memoria utilizzata dalle credenziali chiamando la funzione [**FreeCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-freecredentialshandle) .</span><span class="sxs-lookup"><span data-stu-id="c3f67-191">When you have finished using the returned credentials, free the memory used by the credentials by calling the [**FreeCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-freecredentialshandle) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3f67-192">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c3f67-192">Requirements</span></span>



| <span data-ttu-id="c3f67-193">Requisito</span><span class="sxs-lookup"><span data-stu-id="c3f67-193">Requirement</span></span> | <span data-ttu-id="c3f67-194">Valore</span><span class="sxs-lookup"><span data-stu-id="c3f67-194">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3f67-195">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c3f67-195">Minimum supported client</span></span><br/> | <span data-ttu-id="c3f67-196">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="c3f67-196">Windows XP \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="c3f67-197">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c3f67-197">Minimum supported server</span></span><br/> | <span data-ttu-id="c3f67-198">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c3f67-198">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="c3f67-199">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c3f67-199">Header</span></span><br/>                   | <dl> <span data-ttu-id="c3f67-200"><dt>SSPI. h (include Security. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c3f67-200"><dt>Sspi.h (include Security.h)</dt></span></span> </dl> |
| <span data-ttu-id="c3f67-201">Libreria</span><span class="sxs-lookup"><span data-stu-id="c3f67-201">Library</span></span><br/>                  | <dl> <span data-ttu-id="c3f67-202"><dt>Secur32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c3f67-202"><dt>Secur32.lib</dt></span></span> </dl>                 |
| <span data-ttu-id="c3f67-203">DLL</span><span class="sxs-lookup"><span data-stu-id="c3f67-203">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c3f67-204"><dt>Secur32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c3f67-204"><dt>Secur32.dll</dt></span></span> </dl>                 |
| <span data-ttu-id="c3f67-205">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="c3f67-205">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="c3f67-206">**AcquireCredentialsHandleW** (Unicode) e **AcquireCredentialsHandleA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="c3f67-206">**AcquireCredentialsHandleW** (Unicode) and **AcquireCredentialsHandleA** (ANSI)</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="c3f67-207">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c3f67-207">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3f67-208">Funzioni SSPI</span><span class="sxs-lookup"><span data-stu-id="c3f67-208">SSPI Functions</span></span>](authentication-functions.md#sspi-functions)
</dt> <dt>

[<span data-ttu-id="c3f67-209">**AcceptSecurityContext (negoziazione)**</span><span class="sxs-lookup"><span data-stu-id="c3f67-209">**AcceptSecurityContext (Negotiate)**</span></span>](acceptsecuritycontext--negotiate.md)
</dt> <dt>

[<span data-ttu-id="c3f67-210">**InitializeSecurityContext (negoziazione)**</span><span class="sxs-lookup"><span data-stu-id="c3f67-210">**InitializeSecurityContext (Negotiate)**</span></span>](initializesecuritycontext--negotiate.md)
</dt> <dt>

[<span data-ttu-id="c3f67-211">**FreeCredentialsHandle**</span><span class="sxs-lookup"><span data-stu-id="c3f67-211">**FreeCredentialsHandle**</span></span>](/windows/win32/api/sspi/nf-sspi-freecredentialshandle)
</dt> </dl>

 

 
