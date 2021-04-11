---
description: Acquisisce un handle per le credenziali preesistenti di un'entità di sicurezza che utilizza NTLM.
ms.assetid: 8a51ca50-0e05-4f1e-9dfc-c5d0118f65ed
title: Funzione AcquireCredentialsHandle (NTLM) (SSPI. h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 233bfd57c6e3a7471d7c26204157cd1451d7884f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232966"
---
# <a name="acquirecredentialshandle-ntlm-function"></a><span data-ttu-id="96d64-103">Funzione AcquireCredentialsHandle (NTLM)</span><span class="sxs-lookup"><span data-stu-id="96d64-103">AcquireCredentialsHandle (NTLM) function</span></span>

<span data-ttu-id="96d64-104">La funzione **AcquireCredentialsHandle (NTLM)** acquisisce un handle per le credenziali preesistenti di un' [*entità di sicurezza*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="96d64-104">The **AcquireCredentialsHandle (NTLM)** function acquires a handle to preexisting credentials of a [*security principal*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="96d64-105">Questo handle è richiesto dalle funzioni [**InitializeSecurityContext (NTLM)**](initializesecuritycontext--ntlm.md) e [**AcceptSecurityContext (NTLM)**](acceptsecuritycontext--ntlm.md) .</span><span class="sxs-lookup"><span data-stu-id="96d64-105">This handle is required by the [**InitializeSecurityContext (NTLM)**](initializesecuritycontext--ntlm.md) and [**AcceptSecurityContext (NTLM)**](acceptsecuritycontext--ntlm.md) functions.</span></span> <span data-ttu-id="96d64-106">Possono essere *credenziali* preesistenti, stabilite tramite un accesso di sistema non descritto in questo argomento, oppure il chiamante può fornire credenziali alternative.</span><span class="sxs-lookup"><span data-stu-id="96d64-106">These can be either preexisting *credentials*, which are established through a system logon that is not described here, or the caller can provide alternative credentials.</span></span>

> [!Note]  
> <span data-ttu-id="96d64-107">Non si tratta di un "accesso alla rete" e non implica la raccolta delle credenziali.</span><span class="sxs-lookup"><span data-stu-id="96d64-107">This is not a "log on to the network" and does not imply gathering of credentials.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="96d64-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="96d64-108">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="96d64-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="96d64-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96d64-110">*pszPrincipal* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="96d64-110">*pszPrincipal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96d64-111">Puntatore a una stringa con terminazione null che specifica il nome dell'entità le cui credenziali faranno riferimento all'handle.</span><span class="sxs-lookup"><span data-stu-id="96d64-111">A pointer to a null-terminated string that specifies the name of the principal whose credentials the handle will reference.</span></span>

> [!Note]  
> <span data-ttu-id="96d64-112">Se il processo che richiede l'handle non ha accesso alle credenziali, la funzione restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="96d64-112">If the process that requests the handle does not have access to the credentials, the function returns an error.</span></span> <span data-ttu-id="96d64-113">Una stringa null indica che il processo richiede un handle per le credenziali dell'utente con il [*contesto di sicurezza*](../secgloss/s-gly.md) in cui è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="96d64-113">A null string indicates that the process requires a handle to the credentials of the user under whose [*security context*](../secgloss/s-gly.md) it is executing.</span></span>

 

</dd> <dt>

<span data-ttu-id="96d64-114">*pszPackage* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="96d64-114">*pszPackage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96d64-115">Puntatore a una stringa con terminazione null che specifica il nome del [*pacchetto di sicurezza*](../secgloss/s-gly.md) con cui verranno utilizzate queste credenziali.</span><span class="sxs-lookup"><span data-stu-id="96d64-115">A pointer to a null-terminated string that specifies the name of the [*security package*](../secgloss/s-gly.md) with which these credentials will be used.</span></span> <span data-ttu-id="96d64-116">Nome del [*pacchetto di sicurezza*](../secgloss/s-gly.md) restituito nel membro del **nome** di una struttura [**SecPkgInfo**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) restituita dalla funzione [**EnumerateSecurityPackages**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) .</span><span class="sxs-lookup"><span data-stu-id="96d64-116">This is a [*security package*](../secgloss/s-gly.md) name returned in the **Name** member of a [**SecPkgInfo**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) structure returned by the [**EnumerateSecurityPackages**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) function.</span></span> <span data-ttu-id="96d64-117">Dopo aver stabilito un contesto, è possibile chiamare [**QueryContextAttributes (NTLM)**](querycontextattributes--ntlm.md) con *ULATTRIBUTE* impostato su SECPKG \_ attr \_ package \_ info per restituire informazioni sul [*pacchetto di sicurezza*](../secgloss/s-gly.md) in uso.</span><span class="sxs-lookup"><span data-stu-id="96d64-117">After a context is established, [**QueryContextAttributes (NTLM)**](querycontextattributes--ntlm.md) can be called with *ulAttribute* set to SECPKG\_ATTR\_PACKAGE\_INFO to return information on the [*security package*](../secgloss/s-gly.md) in use.</span></span>

</dd> <dt>

<span data-ttu-id="96d64-118">*fCredentialUse* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="96d64-118">*fCredentialUse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96d64-119">Flag che indica il modo in cui verranno utilizzate queste credenziali.</span><span class="sxs-lookup"><span data-stu-id="96d64-119">A flag that indicates how these credentials will be used.</span></span> <span data-ttu-id="96d64-120">Questo parametro può avere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="96d64-120">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="96d64-121">Valore</span><span class="sxs-lookup"><span data-stu-id="96d64-121">Value</span></span>                                                                                                                                                                               | <span data-ttu-id="96d64-122">Significato</span><span class="sxs-lookup"><span data-stu-id="96d64-122">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SECPKG_CRED_BOTH"></span><span id="secpkg_cred_both"></span><dl> <span data-ttu-id="96d64-123"><dt>**SECPKG \_ cred \_**</dt></span><span class="sxs-lookup"><span data-stu-id="96d64-123"><dt>**SECPKG\_CRED\_BOTH**</dt></span></span> </dl>             | <span data-ttu-id="96d64-124">Convalidare le credenziali in ingresso o usare una credenziale locale per preparare un token in uscita.</span><span class="sxs-lookup"><span data-stu-id="96d64-124">Validate an incoming credential or use a local credential to prepare an outgoing token.</span></span> <span data-ttu-id="96d64-125">Questo flag Abilita entrambi gli altri flag.</span><span class="sxs-lookup"><span data-stu-id="96d64-125">This flag enables both other flags.</span></span><br/>                                                                                                                                                                                                                                                                                                              |
| <span id="SECPKG_CRED_INBOUND"></span><span id="secpkg_cred_inbound"></span><dl> <span data-ttu-id="96d64-126"><dt>**SECPKG \_ cred in \_ ingresso**</dt></span><span class="sxs-lookup"><span data-stu-id="96d64-126"><dt>**SECPKG\_CRED\_INBOUND**</dt></span></span> </dl>    | <span data-ttu-id="96d64-127">Convalidare le credenziali del server in ingresso.</span><span class="sxs-lookup"><span data-stu-id="96d64-127">Validate an incoming server credential.</span></span> <span data-ttu-id="96d64-128">Le credenziali in ingresso possono essere convalidate tramite un'autorità di autenticazione quando viene chiamato [**InitializeSecurityContext (NTLM)**](initializesecuritycontext--ntlm.md) o [**AcceptSecurityContext (NTLM)**](acceptsecuritycontext--ntlm.md) .</span><span class="sxs-lookup"><span data-stu-id="96d64-128">Inbound credentials might be validated by using an authenticating authority when [**InitializeSecurityContext (NTLM)**](initializesecuritycontext--ntlm.md) or [**AcceptSecurityContext (NTLM)**](acceptsecuritycontext--ntlm.md) is called.</span></span> <span data-ttu-id="96d64-129">Se tale autorità non è disponibile, la funzione avrà esito negativo e restituirà il secondo \_ e \_ Nessuna \_ autorità di autenticazione \_ .</span><span class="sxs-lookup"><span data-stu-id="96d64-129">If such an authority is not available, the function will fail and return SEC\_E\_NO\_AUTHENTICATING\_AUTHORITY.</span></span> <span data-ttu-id="96d64-130">La convalida è specifica del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="96d64-130">Validation is package specific.</span></span><br/> |
| <span id="SECPKG_CRED_OUTBOUND"></span><span id="secpkg_cred_outbound"></span><dl> <span data-ttu-id="96d64-131"><dt>**SECPKG \_ cred in \_ uscita**</dt></span><span class="sxs-lookup"><span data-stu-id="96d64-131"><dt>**SECPKG\_CRED\_OUTBOUND**</dt></span></span> </dl> | <span data-ttu-id="96d64-132">Consentire a una credenziale client locale di preparare un token in uscita.</span><span class="sxs-lookup"><span data-stu-id="96d64-132">Allow a local client credential to prepare an outgoing token.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                            |



 

</dd> <dt>

<span data-ttu-id="96d64-133">*pvLogonID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="96d64-133">*pvLogonID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96d64-134">Puntatore a un [*identificatore univoco locale*](../secgloss/l-gly.md) (LUID) che identifica l'utente.</span><span class="sxs-lookup"><span data-stu-id="96d64-134">A pointer to a [*locally unique identifier*](../secgloss/l-gly.md) (LUID) that identifies the user.</span></span> <span data-ttu-id="96d64-135">Questo parametro viene fornito per i processi di file System, ad esempio i redirector di rete.</span><span class="sxs-lookup"><span data-stu-id="96d64-135">This parameter is provided for file-system processes such as network redirectors.</span></span> <span data-ttu-id="96d64-136">Questo parametro può essere **NULL**.</span><span class="sxs-lookup"><span data-stu-id="96d64-136">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="96d64-137">*pAuthData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="96d64-137">*pAuthData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96d64-138">Puntatore ai dati specifici del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="96d64-138">A pointer to package-specific data.</span></span> <span data-ttu-id="96d64-139">Questo parametro può essere **null**, a indicare che è necessario utilizzare le credenziali predefinite per il [*pacchetto di sicurezza*](../secgloss/s-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="96d64-139">This parameter can be **NULL**, which indicates that the default credentials for that [*security package*](../secgloss/s-gly.md) must be used.</span></span> <span data-ttu-id="96d64-140">Per usare le credenziali specificate, passare una struttura di [**\_ \_ \_ identità di autenticazione WinNT in secondi**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) che includa le credenziali in questo parametro.</span><span class="sxs-lookup"><span data-stu-id="96d64-140">To use supplied credentials, pass a [**SEC\_WINNT\_AUTH\_IDENTITY**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) structure that includes those credentials in this parameter.</span></span> <span data-ttu-id="96d64-141">Il tempo di esecuzione RPC passa ciò che è stato fornito in [**RpcBindingSetAuthInfo**](/windows/win32/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfo).</span><span class="sxs-lookup"><span data-stu-id="96d64-141">The RPC run time passes whatever was provided in [**RpcBindingSetAuthInfo**](/windows/win32/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfo).</span></span>

<span data-ttu-id="96d64-142">Quando si utilizza il pacchetto NTLM, le lunghezze dei caratteri massime per nome utente, password e dominio sono rispettivamente 256, 256 e 15.</span><span class="sxs-lookup"><span data-stu-id="96d64-142">When using the NTLM package, the maximum character lengths for user name, password, and domain are 256, 256, and 15, respectively.</span></span>

</dd> <dt>

<span data-ttu-id="96d64-143">*pGetKeyFn* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="96d64-143">*pGetKeyFn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96d64-144">Questo parametro non viene utilizzato e deve essere impostato su **null**.</span><span class="sxs-lookup"><span data-stu-id="96d64-144">This parameter is not used and should be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="96d64-145">*pvGetKeyArgument* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="96d64-145">*pvGetKeyArgument* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96d64-146">Questo parametro non viene utilizzato e deve essere impostato su **null**.</span><span class="sxs-lookup"><span data-stu-id="96d64-146">This parameter is not used and should be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="96d64-147">*phCredential* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="96d64-147">*phCredential* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="96d64-148">Puntatore a una struttura [CredHandle](sspi-handles.md) per la ricezione dell'handle delle credenziali.</span><span class="sxs-lookup"><span data-stu-id="96d64-148">A pointer to a [CredHandle](sspi-handles.md) structure to receive the credential handle.</span></span>

</dd> <dt>

<span data-ttu-id="96d64-149">*ptsExpiry* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="96d64-149">*ptsExpiry* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="96d64-150">Puntatore a una struttura di [**timestamp**](timestamp.md) che riceve l'ora di scadenza delle credenziali restituite.</span><span class="sxs-lookup"><span data-stu-id="96d64-150">A pointer to a [**TimeStamp**](timestamp.md) structure that receives the time at which the returned credentials expire.</span></span> <span data-ttu-id="96d64-151">Il valore restituito in questa struttura di **timestamp** dipende dalla [*delega vincolata*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="96d64-151">The value returned in this **TimeStamp** structure depends on the [*constrained delegation*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="96d64-152">Il [*pacchetto di sicurezza*](../secgloss/s-gly.md) deve restituire questo valore nell'ora locale.</span><span class="sxs-lookup"><span data-stu-id="96d64-152">The [*security package*](../secgloss/s-gly.md) must return this value in local time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96d64-153">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="96d64-153">Return value</span></span>

<span data-ttu-id="96d64-154">Se la funzione ha esito positivo, la funzione restituisce SEC \_ E \_ OK.</span><span class="sxs-lookup"><span data-stu-id="96d64-154">If the function succeeds, the function returns SEC\_E\_OK.</span></span>

<span data-ttu-id="96d64-155">Se la funzione ha esito negativo, restituisce uno dei codici di errore seguenti.</span><span class="sxs-lookup"><span data-stu-id="96d64-155">If the function fails, it returns one of the following error codes.</span></span>



| <span data-ttu-id="96d64-156">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="96d64-156">Return code</span></span>                                                                                                 | <span data-ttu-id="96d64-157">Descrizione</span><span class="sxs-lookup"><span data-stu-id="96d64-157">Description</span></span>                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="96d64-158"><dt>**SEC \_ E \_ memoria insufficiente \_**</dt></span><span class="sxs-lookup"><span data-stu-id="96d64-158"><dt>**SEC\_E\_INSUFFICIENT\_MEMORY**</dt></span></span> </dl> | <span data-ttu-id="96d64-159">La memoria disponibile non è sufficiente per completare l'azione richiesta.</span><span class="sxs-lookup"><span data-stu-id="96d64-159">There is not enough memory available to complete the requested action.</span></span><br/>                                                                  |
| <dl> <span data-ttu-id="96d64-160"><dt>**\_ \_ errore interno sec \_ E**</dt></span><span class="sxs-lookup"><span data-stu-id="96d64-160"><dt>**SEC\_E\_INTERNAL\_ERROR**</dt></span></span> </dl>      | <span data-ttu-id="96d64-161">Si è verificato un errore che non è stato mappato a un codice di errore SSPI.</span><span class="sxs-lookup"><span data-stu-id="96d64-161">An error occurred that did not map to an SSPI error code.</span></span><br/>                                                                               |
| <dl> <span data-ttu-id="96d64-162"><dt>**SEC \_ E \_ Nessuna \_ credenziale**</dt></span><span class="sxs-lookup"><span data-stu-id="96d64-162"><dt>**SEC\_E\_NO\_CREDENTIALS**</dt></span></span> </dl>      | <span data-ttu-id="96d64-163">Nessuna credenziale disponibile nella [*delega vincolata*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="96d64-163">No credentials are available in the [*constrained delegation*](../secgloss/s-gly.md).</span></span><br/> |
| <dl> <span data-ttu-id="96d64-164"><dt>**SEC \_ E \_ non \_ proprietario**</dt></span><span class="sxs-lookup"><span data-stu-id="96d64-164"><dt>**SEC\_E\_NOT\_OWNER**</dt></span></span> </dl>           | <span data-ttu-id="96d64-165">Il chiamante della funzione non ha le credenziali necessarie.</span><span class="sxs-lookup"><span data-stu-id="96d64-165">The caller of the function does not have the necessary credentials.</span></span><br/>                                                                     |
| <dl> <span data-ttu-id="96d64-166"><dt>**SEC \_ E \_ SECPKG \_ non \_ trovati**</dt></span><span class="sxs-lookup"><span data-stu-id="96d64-166"><dt>**SEC\_E\_SECPKG\_NOT\_FOUND**</dt></span></span> </dl>   | <span data-ttu-id="96d64-167">Il [*pacchetto di sicurezza*](../secgloss/s-gly.md) richiesto non esiste.</span><span class="sxs-lookup"><span data-stu-id="96d64-167">The requested [*security package*](../secgloss/s-gly.md) does not exist.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="96d64-168"><dt>**SEC \_ E \_ \_ credenziali sconosciute**</dt></span><span class="sxs-lookup"><span data-stu-id="96d64-168"><dt>**SEC\_E\_UNKNOWN\_CREDENTIALS**</dt></span></span> </dl> | <span data-ttu-id="96d64-169">Le credenziali fornite al pacchetto non sono state riconosciute.</span><span class="sxs-lookup"><span data-stu-id="96d64-169">The credentials supplied to the package were not recognized.</span></span><br/>                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="96d64-170">Commenti</span><span class="sxs-lookup"><span data-stu-id="96d64-170">Remarks</span></span>

<span data-ttu-id="96d64-171">La funzione **AcquireCredentialsHandle (NTLM)** restituisce un handle per le credenziali di un'entità, ad esempio un utente o un client, come usato da una [*delega vincolata*](../secgloss/s-gly.md)specifica.</span><span class="sxs-lookup"><span data-stu-id="96d64-171">The **AcquireCredentialsHandle (NTLM)** function returns a handle to the credentials of a principal, such as a user or client, as used by a specific [*constrained delegation*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="96d64-172">Può trattarsi dell'handle per le credenziali preesistenti oppure la funzione può creare un nuovo set di credenziali e restituirlo.</span><span class="sxs-lookup"><span data-stu-id="96d64-172">This can be the handle to preexisting credentials, or the function can create a new set of credentials and return it.</span></span> <span data-ttu-id="96d64-173">Questo handle può essere utilizzato nelle chiamate successive alle funzioni [**AcceptSecurityContext (NTLM)**](acceptsecuritycontext--ntlm.md) e [**InitializeSecurityContext (NTLM)**](initializesecuritycontext--ntlm.md) .</span><span class="sxs-lookup"><span data-stu-id="96d64-173">This handle can be used in subsequent calls to the [**AcceptSecurityContext (NTLM)**](acceptsecuritycontext--ntlm.md) and [**InitializeSecurityContext (NTLM)**](initializesecuritycontext--ntlm.md) functions.</span></span>

<span data-ttu-id="96d64-174">In generale, **AcquireCredentialsHandle (NTLM)** non consente a un processo di ottenere un handle per le credenziali di altri utenti connessi allo stesso computer.</span><span class="sxs-lookup"><span data-stu-id="96d64-174">In general, **AcquireCredentialsHandle (NTLM)** does not allow a process to obtain a handle to the credentials of other users logged on to the same computer.</span></span> <span data-ttu-id="96d64-175">Tuttavia, un chiamante con \_ \_ [*privilegi*](../secgloss/s-gly.md) per il nome TCB ha la possibilità di specificare l' [*identificatore di accesso*](../secgloss/l-gly.md) (LUID) di qualsiasi token di sessione di accesso esistente per ottenere un handle per le credenziali della sessione.</span><span class="sxs-lookup"><span data-stu-id="96d64-175">However, a caller with SE\_TCB\_NAME [*privilege*](../secgloss/s-gly.md) has the option of specifying the [*logon identifier*](../secgloss/l-gly.md) (LUID) of any existing logon session token to get a handle to that session's credentials.</span></span> <span data-ttu-id="96d64-176">Questa operazione viene in genere utilizzata dai moduli in modalità kernel che devono agire per conto di un utente connesso.</span><span class="sxs-lookup"><span data-stu-id="96d64-176">Typically, this is used by kernel-mode modules that must act on behalf of a logged-on user.</span></span>

<span data-ttu-id="96d64-177">Un pacchetto può chiamare la funzione in *pGetKeyFn* fornita dal trasporto di run-time RPC.</span><span class="sxs-lookup"><span data-stu-id="96d64-177">A package might call the function in *pGetKeyFn* provided by the RPC run-time transport.</span></span> <span data-ttu-id="96d64-178">Se il trasporto non supporta la nozione di callback per recuperare le credenziali, questo parametro deve essere **null**.</span><span class="sxs-lookup"><span data-stu-id="96d64-178">If the transport does not support the notion of callback to retrieve credentials, this parameter must be **NULL**.</span></span>

<span data-ttu-id="96d64-179">Per i chiamanti in modalità kernel, è necessario notare le differenze seguenti:</span><span class="sxs-lookup"><span data-stu-id="96d64-179">For kernel mode callers, the following differences must be noted:</span></span>

-   <span data-ttu-id="96d64-180">I due parametri di stringa devono essere stringhe [*Unicode*](../secgloss/u-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="96d64-180">The two string parameters must be [*Unicode*](../secgloss/u-gly.md) strings.</span></span>
-   <span data-ttu-id="96d64-181">I valori del buffer devono essere allocati nella memoria virtuale del processo, non dal pool.</span><span class="sxs-lookup"><span data-stu-id="96d64-181">The buffer values must be allocated in process virtual memory, not from the pool.</span></span>

<span data-ttu-id="96d64-182">Al termine dell'utilizzo delle credenziali restituite, liberare la memoria utilizzata dalle credenziali chiamando la funzione [**FreeCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-freecredentialshandle) .</span><span class="sxs-lookup"><span data-stu-id="96d64-182">When you have finished using the returned credentials, free the memory used by the credentials by calling the [**FreeCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-freecredentialshandle) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="96d64-183">Requisiti</span><span class="sxs-lookup"><span data-stu-id="96d64-183">Requirements</span></span>



| <span data-ttu-id="96d64-184">Requisito</span><span class="sxs-lookup"><span data-stu-id="96d64-184">Requirement</span></span> | <span data-ttu-id="96d64-185">Valore</span><span class="sxs-lookup"><span data-stu-id="96d64-185">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="96d64-186">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="96d64-186">Minimum supported client</span></span><br/> | <span data-ttu-id="96d64-187">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="96d64-187">Windows XP \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="96d64-188">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="96d64-188">Minimum supported server</span></span><br/> | <span data-ttu-id="96d64-189">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="96d64-189">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="96d64-190">Intestazione</span><span class="sxs-lookup"><span data-stu-id="96d64-190">Header</span></span><br/>                   | <dl> <span data-ttu-id="96d64-191"><dt>SSPI. h (include Security. h)</dt></span><span class="sxs-lookup"><span data-stu-id="96d64-191"><dt>Sspi.h (include Security.h)</dt></span></span> </dl> |
| <span data-ttu-id="96d64-192">Libreria</span><span class="sxs-lookup"><span data-stu-id="96d64-192">Library</span></span><br/>                  | <dl> <span data-ttu-id="96d64-193"><dt>Secur32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="96d64-193"><dt>Secur32.lib</dt></span></span> </dl>                 |
| <span data-ttu-id="96d64-194">DLL</span><span class="sxs-lookup"><span data-stu-id="96d64-194">DLL</span></span><br/>                      | <dl> <span data-ttu-id="96d64-195"><dt>Secur32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="96d64-195"><dt>Secur32.dll</dt></span></span> </dl>                 |
| <span data-ttu-id="96d64-196">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="96d64-196">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="96d64-197">**AcquireCredentialsHandleW** (Unicode) e **AcquireCredentialsHandleA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="96d64-197">**AcquireCredentialsHandleW** (Unicode) and **AcquireCredentialsHandleA** (ANSI)</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="96d64-198">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="96d64-198">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96d64-199">Funzioni SSPI</span><span class="sxs-lookup"><span data-stu-id="96d64-199">SSPI Functions</span></span>](authentication-functions.md#sspi-functions)
</dt> <dt>

[<span data-ttu-id="96d64-200">**AcceptSecurityContext (NTLM)**</span><span class="sxs-lookup"><span data-stu-id="96d64-200">**AcceptSecurityContext (NTLM)**</span></span>](acceptsecuritycontext--ntlm.md)
</dt> <dt>

[<span data-ttu-id="96d64-201">**InitializeSecurityContext (NTLM)**</span><span class="sxs-lookup"><span data-stu-id="96d64-201">**InitializeSecurityContext (NTLM)**</span></span>](initializesecuritycontext--ntlm.md)
</dt> <dt>

[<span data-ttu-id="96d64-202">**FreeCredentialsHandle**</span><span class="sxs-lookup"><span data-stu-id="96d64-202">**FreeCredentialsHandle**</span></span>](/windows/win32/api/sspi/nf-sspi-freecredentialshandle)
</dt> </dl>

 

 
