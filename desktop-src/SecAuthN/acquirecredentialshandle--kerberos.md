---
description: Acquisisce un handle per le credenziali preesistenti di un'entità di sicurezza che utilizza Kerberos.
ms.assetid: 2612bbe9-856b-4a81-bffb-6c761035883d
title: Funzione AcquireCredentialsHandle (Kerberos) (SSPI. h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 05a4dd885712e89b812896684f73d60df610e41d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316241"
---
# <a name="acquirecredentialshandle-kerberos-function"></a><span data-ttu-id="35e2a-103">Funzione AcquireCredentialsHandle (Kerberos)</span><span class="sxs-lookup"><span data-stu-id="35e2a-103">AcquireCredentialsHandle (Kerberos) function</span></span>

<span data-ttu-id="35e2a-104">La funzione **AcquireCredentialsHandle (Kerberos)** acquisisce un handle per le credenziali preesistenti di un' [*entità di sicurezza*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="35e2a-104">The **AcquireCredentialsHandle (Kerberos)** function acquires a handle to preexisting credentials of a [*security principal*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="35e2a-105">Questo handle è richiesto dalle funzioni [**InitializeSecurityContext (Kerberos)**](initializesecuritycontext--kerberos.md) e [**AcceptSecurityContext (Kerberos)**](acceptsecuritycontext--kerberos.md) .</span><span class="sxs-lookup"><span data-stu-id="35e2a-105">This handle is required by the [**InitializeSecurityContext (Kerberos)**](initializesecuritycontext--kerberos.md) and [**AcceptSecurityContext (Kerberos)**](acceptsecuritycontext--kerberos.md) functions.</span></span> <span data-ttu-id="35e2a-106">Possono essere *credenziali* preesistenti, stabilite tramite un accesso di sistema non descritto in questo argomento, oppure il chiamante può fornire credenziali alternative.</span><span class="sxs-lookup"><span data-stu-id="35e2a-106">These can be either preexisting *credentials*, which are established through a system logon that is not described here, or the caller can provide alternative credentials.</span></span>

> [!Note]  
> <span data-ttu-id="35e2a-107">Non si tratta di un "accesso alla rete" e non implica la raccolta delle credenziali.</span><span class="sxs-lookup"><span data-stu-id="35e2a-107">This is not a "log on to the network" and does not imply gathering of credentials.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="35e2a-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="35e2a-108">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="35e2a-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="35e2a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35e2a-110">*pszPrincipal* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="35e2a-110">*pszPrincipal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35e2a-111">Puntatore a una stringa con terminazione null che specifica il nome dell'entità le cui credenziali faranno riferimento all'handle.</span><span class="sxs-lookup"><span data-stu-id="35e2a-111">A pointer to a null-terminated string that specifies the name of the principal whose credentials the handle will reference.</span></span>

> [!Note]  
> <span data-ttu-id="35e2a-112">Se il processo che richiede l'handle non ha accesso alle credenziali, la funzione restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="35e2a-112">If the process that requests the handle does not have access to the credentials, the function returns an error.</span></span> <span data-ttu-id="35e2a-113">Una stringa null indica che il processo richiede un handle per le credenziali dell'utente con il [*contesto di sicurezza*](../secgloss/s-gly.md) in cui è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="35e2a-113">A null string indicates that the process requires a handle to the credentials of the user under whose [*security context*](../secgloss/s-gly.md) it is executing.</span></span>

 

</dd> <dt>

<span data-ttu-id="35e2a-114">*pszPackage* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="35e2a-114">*pszPackage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35e2a-115">Puntatore a una stringa con terminazione null che specifica il nome del [*pacchetto di sicurezza*](../secgloss/s-gly.md) con cui verranno utilizzate queste credenziali.</span><span class="sxs-lookup"><span data-stu-id="35e2a-115">A pointer to a null-terminated string that specifies the name of the [*security package*](../secgloss/s-gly.md) with which these credentials will be used.</span></span> <span data-ttu-id="35e2a-116">Nome del [*pacchetto di sicurezza*](../secgloss/s-gly.md) restituito nel membro del **nome** di una struttura [**SecPkgInfo**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) restituita dalla funzione [**EnumerateSecurityPackages**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) .</span><span class="sxs-lookup"><span data-stu-id="35e2a-116">This is a [*security package*](../secgloss/s-gly.md) name returned in the **Name** member of a [**SecPkgInfo**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) structure returned by the [**EnumerateSecurityPackages**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) function.</span></span> <span data-ttu-id="35e2a-117">Dopo aver stabilito un contesto, è possibile chiamare [**QueryContextAttributes (Kerberos)**](querycontextattributes--kerberos.md) con *ULATTRIBUTE* impostato su SECPKG \_ attr \_ package \_ info per restituire informazioni sul [*pacchetto di sicurezza*](../secgloss/s-gly.md) in uso.</span><span class="sxs-lookup"><span data-stu-id="35e2a-117">After a context is established, [**QueryContextAttributes (Kerberos)**](querycontextattributes--kerberos.md) can be called with *ulAttribute* set to SECPKG\_ATTR\_PACKAGE\_INFO to return information on the [*security package*](../secgloss/s-gly.md) in use.</span></span>

</dd> <dt>

<span data-ttu-id="35e2a-118">*fCredentialUse* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="35e2a-118">*fCredentialUse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35e2a-119">Flag che indica il modo in cui verranno utilizzate queste credenziali.</span><span class="sxs-lookup"><span data-stu-id="35e2a-119">A flag that indicates how these credentials will be used.</span></span> <span data-ttu-id="35e2a-120">Questo parametro può avere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="35e2a-120">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="35e2a-121">Valore</span><span class="sxs-lookup"><span data-stu-id="35e2a-121">Value</span></span>                                                                                                                                                                               | <span data-ttu-id="35e2a-122">Significato</span><span class="sxs-lookup"><span data-stu-id="35e2a-122">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SECPKG_CRED_BOTH"></span><span id="secpkg_cred_both"></span><dl> <span data-ttu-id="35e2a-123"><dt>**SECPKG \_ cred \_**</dt></span><span class="sxs-lookup"><span data-stu-id="35e2a-123"><dt>**SECPKG\_CRED\_BOTH**</dt></span></span> </dl>             | <span data-ttu-id="35e2a-124">Convalidare le credenziali in ingresso o usare una credenziale locale per preparare un token in uscita.</span><span class="sxs-lookup"><span data-stu-id="35e2a-124">Validate an incoming credential or use a local credential to prepare an outgoing token.</span></span> <span data-ttu-id="35e2a-125">Questo flag Abilita entrambi gli altri flag.</span><span class="sxs-lookup"><span data-stu-id="35e2a-125">This flag enables both other flags.</span></span><br/>                                                                                                                                                                                                                                                                                                                              |
| <span id="SECPKG_CRED_INBOUND"></span><span id="secpkg_cred_inbound"></span><dl> <span data-ttu-id="35e2a-126"><dt>**SECPKG \_ cred in \_ ingresso**</dt></span><span class="sxs-lookup"><span data-stu-id="35e2a-126"><dt>**SECPKG\_CRED\_INBOUND**</dt></span></span> </dl>    | <span data-ttu-id="35e2a-127">Convalidare le credenziali del server in ingresso.</span><span class="sxs-lookup"><span data-stu-id="35e2a-127">Validate an incoming server credential.</span></span> <span data-ttu-id="35e2a-128">Le credenziali in ingresso possono essere convalidate tramite un'autorità di autenticazione quando viene chiamato [**InitializeSecurityContext (Kerberos)**](initializesecuritycontext--kerberos.md) o [**AcceptSecurityContext (Kerberos)**](acceptsecuritycontext--kerberos.md) .</span><span class="sxs-lookup"><span data-stu-id="35e2a-128">Inbound credentials might be validated by using an authenticating authority when [**InitializeSecurityContext (Kerberos)**](initializesecuritycontext--kerberos.md) or [**AcceptSecurityContext (Kerberos)**](acceptsecuritycontext--kerberos.md) is called.</span></span> <span data-ttu-id="35e2a-129">Se tale autorità non è disponibile, la funzione avrà esito negativo e restituirà il secondo \_ e \_ Nessuna \_ autorità di autenticazione \_ .</span><span class="sxs-lookup"><span data-stu-id="35e2a-129">If such an authority is not available, the function will fail and return SEC\_E\_NO\_AUTHENTICATING\_AUTHORITY.</span></span> <span data-ttu-id="35e2a-130">La convalida è specifica del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="35e2a-130">Validation is package specific.</span></span><br/> |
| <span id="SECPKG_CRED_OUTBOUND"></span><span id="secpkg_cred_outbound"></span><dl> <span data-ttu-id="35e2a-131"><dt>**SECPKG \_ cred in \_ uscita**</dt></span><span class="sxs-lookup"><span data-stu-id="35e2a-131"><dt>**SECPKG\_CRED\_OUTBOUND**</dt></span></span> </dl> | <span data-ttu-id="35e2a-132">Consentire a una credenziale client locale di preparare un token in uscita.</span><span class="sxs-lookup"><span data-stu-id="35e2a-132">Allow a local client credential to prepare an outgoing token.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                            |



 

</dd> <dt>

<span data-ttu-id="35e2a-133">*pvLogonID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="35e2a-133">*pvLogonID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35e2a-134">Puntatore a un [*identificatore univoco locale*](../secgloss/l-gly.md) (LUID) che identifica l'utente.</span><span class="sxs-lookup"><span data-stu-id="35e2a-134">A pointer to a [*locally unique identifier*](../secgloss/l-gly.md) (LUID) that identifies the user.</span></span> <span data-ttu-id="35e2a-135">Questo parametro viene fornito per i processi di file System, ad esempio i redirector di rete.</span><span class="sxs-lookup"><span data-stu-id="35e2a-135">This parameter is provided for file-system processes such as network redirectors.</span></span> <span data-ttu-id="35e2a-136">Questo parametro può essere **NULL**.</span><span class="sxs-lookup"><span data-stu-id="35e2a-136">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="35e2a-137">*pAuthData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="35e2a-137">*pAuthData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35e2a-138">Puntatore ai dati specifici del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="35e2a-138">A pointer to package-specific data.</span></span> <span data-ttu-id="35e2a-139">Questo parametro può essere **null**, a indicare che è necessario utilizzare le credenziali predefinite per il [*pacchetto di sicurezza*](../secgloss/s-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="35e2a-139">This parameter can be **NULL**, which indicates that the default credentials for that [*security package*](../secgloss/s-gly.md) must be used.</span></span> <span data-ttu-id="35e2a-140">Per usare le credenziali specificate, passare una struttura di [**\_ \_ \_ identità di autenticazione WinNT in secondi**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) che includa le credenziali in questo parametro.</span><span class="sxs-lookup"><span data-stu-id="35e2a-140">To use supplied credentials, pass a [**SEC\_WINNT\_AUTH\_IDENTITY**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) structure that includes those credentials in this parameter.</span></span> <span data-ttu-id="35e2a-141">Il tempo di esecuzione RPC passa ciò che è stato fornito in [**RpcBindingSetAuthInfo**](/windows/win32/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfo).</span><span class="sxs-lookup"><span data-stu-id="35e2a-141">The RPC run time passes whatever was provided in [**RpcBindingSetAuthInfo**](/windows/win32/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfo).</span></span>

</dd> <dt>

<span data-ttu-id="35e2a-142">*pGetKeyFn* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="35e2a-142">*pGetKeyFn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35e2a-143">Questo parametro non viene utilizzato e deve essere impostato su **null**.</span><span class="sxs-lookup"><span data-stu-id="35e2a-143">This parameter is not used and should be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="35e2a-144">*pvGetKeyArgument* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="35e2a-144">*pvGetKeyArgument* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35e2a-145">Questo parametro non viene utilizzato e deve essere impostato su **null**.</span><span class="sxs-lookup"><span data-stu-id="35e2a-145">This parameter is not used and should be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="35e2a-146">*phCredential* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="35e2a-146">*phCredential* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="35e2a-147">Puntatore a una struttura [CredHandle](sspi-handles.md) per la ricezione dell'handle delle credenziali.</span><span class="sxs-lookup"><span data-stu-id="35e2a-147">A pointer to a [CredHandle](sspi-handles.md) structure to receive the credential handle.</span></span>

</dd> <dt>

<span data-ttu-id="35e2a-148">*ptsExpiry* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="35e2a-148">*ptsExpiry* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="35e2a-149">Puntatore a una struttura di [**timestamp**](timestamp.md) che riceve l'ora di scadenza delle credenziali restituite.</span><span class="sxs-lookup"><span data-stu-id="35e2a-149">A pointer to a [**TimeStamp**](timestamp.md) structure that receives the time at which the returned credentials expire.</span></span> <span data-ttu-id="35e2a-150">Il valore restituito in questa struttura di **timestamp** dipende dalla [*delega vincolata*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="35e2a-150">The value returned in this **TimeStamp** structure depends on the [*constrained delegation*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="35e2a-151">Il [*pacchetto di sicurezza*](../secgloss/s-gly.md) deve restituire questo valore nell'ora locale.</span><span class="sxs-lookup"><span data-stu-id="35e2a-151">The [*security package*](../secgloss/s-gly.md) must return this value in local time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35e2a-152">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="35e2a-152">Return value</span></span>

<span data-ttu-id="35e2a-153">Se la funzione ha esito positivo, la funzione restituisce SEC \_ E \_ OK.</span><span class="sxs-lookup"><span data-stu-id="35e2a-153">If the function succeeds, the function returns SEC\_E\_OK.</span></span>

<span data-ttu-id="35e2a-154">Se la funzione ha esito negativo, restituisce uno dei codici di errore seguenti.</span><span class="sxs-lookup"><span data-stu-id="35e2a-154">If the function fails, it returns one of the following error codes.</span></span>



| <span data-ttu-id="35e2a-155">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="35e2a-155">Return code</span></span>                                                                                                 | <span data-ttu-id="35e2a-156">Descrizione</span><span class="sxs-lookup"><span data-stu-id="35e2a-156">Description</span></span>                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="35e2a-157"><dt>**SEC \_ E \_ memoria insufficiente \_**</dt></span><span class="sxs-lookup"><span data-stu-id="35e2a-157"><dt>**SEC\_E\_INSUFFICIENT\_MEMORY**</dt></span></span> </dl> | <span data-ttu-id="35e2a-158">La memoria disponibile non è sufficiente per completare l'azione richiesta.</span><span class="sxs-lookup"><span data-stu-id="35e2a-158">There is not enough memory available to complete the requested action.</span></span><br/>                                                                  |
| <dl> <span data-ttu-id="35e2a-159"><dt>**\_ \_ errore interno sec \_ E**</dt></span><span class="sxs-lookup"><span data-stu-id="35e2a-159"><dt>**SEC\_E\_INTERNAL\_ERROR**</dt></span></span> </dl>      | <span data-ttu-id="35e2a-160">Si è verificato un errore che non è stato mappato a un codice di errore SSPI.</span><span class="sxs-lookup"><span data-stu-id="35e2a-160">An error occurred that did not map to an SSPI error code.</span></span><br/>                                                                               |
| <dl> <span data-ttu-id="35e2a-161"><dt>**SEC \_ E \_ Nessuna \_ credenziale**</dt></span><span class="sxs-lookup"><span data-stu-id="35e2a-161"><dt>**SEC\_E\_NO\_CREDENTIALS**</dt></span></span> </dl>      | <span data-ttu-id="35e2a-162">Nessuna credenziale disponibile nella [*delega vincolata*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="35e2a-162">No credentials are available in the [*constrained delegation*](../secgloss/s-gly.md).</span></span><br/> |
| <dl> <span data-ttu-id="35e2a-163"><dt>**SEC \_ E \_ non \_ proprietario**</dt></span><span class="sxs-lookup"><span data-stu-id="35e2a-163"><dt>**SEC\_E\_NOT\_OWNER**</dt></span></span> </dl>           | <span data-ttu-id="35e2a-164">Il chiamante della funzione non ha le credenziali necessarie.</span><span class="sxs-lookup"><span data-stu-id="35e2a-164">The caller of the function does not have the necessary credentials.</span></span><br/>                                                                     |
| <dl> <span data-ttu-id="35e2a-165"><dt>**SEC \_ E \_ SECPKG \_ non \_ trovati**</dt></span><span class="sxs-lookup"><span data-stu-id="35e2a-165"><dt>**SEC\_E\_SECPKG\_NOT\_FOUND**</dt></span></span> </dl>   | <span data-ttu-id="35e2a-166">Il [*pacchetto di sicurezza*](../secgloss/s-gly.md) richiesto non esiste.</span><span class="sxs-lookup"><span data-stu-id="35e2a-166">The requested [*security package*](../secgloss/s-gly.md) does not exist.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="35e2a-167"><dt>**SEC \_ E \_ \_ credenziali sconosciute**</dt></span><span class="sxs-lookup"><span data-stu-id="35e2a-167"><dt>**SEC\_E\_UNKNOWN\_CREDENTIALS**</dt></span></span> </dl> | <span data-ttu-id="35e2a-168">Le credenziali fornite al pacchetto non sono state riconosciute.</span><span class="sxs-lookup"><span data-stu-id="35e2a-168">The credentials supplied to the package were not recognized.</span></span><br/>                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="35e2a-169">Commenti</span><span class="sxs-lookup"><span data-stu-id="35e2a-169">Remarks</span></span>

<span data-ttu-id="35e2a-170">La funzione **AcquireCredentialsHandle (Kerberos)** restituisce un handle per le credenziali di un'entità, ad esempio un utente o un client, come usato da una [*delega vincolata*](../secgloss/s-gly.md)specifica.</span><span class="sxs-lookup"><span data-stu-id="35e2a-170">The **AcquireCredentialsHandle (Kerberos)** function returns a handle to the credentials of a principal, such as a user or client, as used by a specific [*constrained delegation*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="35e2a-171">Può trattarsi dell'handle per le credenziali preesistenti oppure la funzione può creare un nuovo set di credenziali e restituirlo.</span><span class="sxs-lookup"><span data-stu-id="35e2a-171">This can be the handle to preexisting credentials, or the function can create a new set of credentials and return it.</span></span> <span data-ttu-id="35e2a-172">Questo handle può essere utilizzato nelle chiamate successive alle funzioni [**AcceptSecurityContext (Kerberos)**](acceptsecuritycontext--kerberos.md) e [**InitializeSecurityContext (Kerberos)**](initializesecuritycontext--kerberos.md) .</span><span class="sxs-lookup"><span data-stu-id="35e2a-172">This handle can be used in subsequent calls to the [**AcceptSecurityContext (Kerberos)**](acceptsecuritycontext--kerberos.md) and [**InitializeSecurityContext (Kerberos)**](initializesecuritycontext--kerberos.md) functions.</span></span>

<span data-ttu-id="35e2a-173">In generale, **AcquireCredentialsHandle (Kerberos)** non consente a un processo di ottenere un handle per le credenziali di altri utenti connessi allo stesso computer.</span><span class="sxs-lookup"><span data-stu-id="35e2a-173">In general, **AcquireCredentialsHandle (Kerberos)** does not allow a process to obtain a handle to the credentials of other users logged on to the same computer.</span></span> <span data-ttu-id="35e2a-174">Tuttavia, un chiamante con \_ \_ [*privilegi*](../secgloss/s-gly.md) per il nome TCB ha la possibilità di specificare l' [*identificatore di accesso*](../secgloss/l-gly.md) (LUID) di qualsiasi token di sessione di accesso esistente per ottenere un handle per le credenziali della sessione.</span><span class="sxs-lookup"><span data-stu-id="35e2a-174">However, a caller with SE\_TCB\_NAME [*privilege*](../secgloss/s-gly.md) has the option of specifying the [*logon identifier*](../secgloss/l-gly.md) (LUID) of any existing logon session token to get a handle to that session's credentials.</span></span> <span data-ttu-id="35e2a-175">Questa operazione viene in genere utilizzata dai moduli in modalità kernel che devono agire per conto di un utente connesso.</span><span class="sxs-lookup"><span data-stu-id="35e2a-175">Typically, this is used by kernel-mode modules that must act on behalf of a logged-on user.</span></span>

<span data-ttu-id="35e2a-176">Un pacchetto può chiamare la funzione in *pGetKeyFn* fornita dal trasporto di run-time RPC.</span><span class="sxs-lookup"><span data-stu-id="35e2a-176">A package might call the function in *pGetKeyFn* provided by the RPC run-time transport.</span></span> <span data-ttu-id="35e2a-177">Se il trasporto non supporta la nozione di callback per recuperare le credenziali, questo parametro deve essere **null**.</span><span class="sxs-lookup"><span data-stu-id="35e2a-177">If the transport does not support the notion of callback to retrieve credentials, this parameter must be **NULL**.</span></span>

<span data-ttu-id="35e2a-178">Per i chiamanti in modalità kernel, è necessario notare le differenze seguenti:</span><span class="sxs-lookup"><span data-stu-id="35e2a-178">For kernel mode callers, the following differences must be noted:</span></span>

-   <span data-ttu-id="35e2a-179">I due parametri di stringa devono essere stringhe [*Unicode*](../secgloss/u-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="35e2a-179">The two string parameters must be [*Unicode*](../secgloss/u-gly.md) strings.</span></span>
-   <span data-ttu-id="35e2a-180">I valori del buffer devono essere allocati nella memoria virtuale del processo, non dal pool.</span><span class="sxs-lookup"><span data-stu-id="35e2a-180">The buffer values must be allocated in process virtual memory, not from the pool.</span></span>

<span data-ttu-id="35e2a-181">Al termine dell'utilizzo delle credenziali restituite, liberare la memoria utilizzata dalle credenziali chiamando la funzione [**FreeCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-freecredentialshandle) .</span><span class="sxs-lookup"><span data-stu-id="35e2a-181">When you have finished using the returned credentials, free the memory used by the credentials by calling the [**FreeCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-freecredentialshandle) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="35e2a-182">Requisiti</span><span class="sxs-lookup"><span data-stu-id="35e2a-182">Requirements</span></span>



| <span data-ttu-id="35e2a-183">Requisito</span><span class="sxs-lookup"><span data-stu-id="35e2a-183">Requirement</span></span> | <span data-ttu-id="35e2a-184">Valore</span><span class="sxs-lookup"><span data-stu-id="35e2a-184">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35e2a-185">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="35e2a-185">Minimum supported client</span></span><br/> | <span data-ttu-id="35e2a-186">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="35e2a-186">Windows XP \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="35e2a-187">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="35e2a-187">Minimum supported server</span></span><br/> | <span data-ttu-id="35e2a-188">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="35e2a-188">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="35e2a-189">Intestazione</span><span class="sxs-lookup"><span data-stu-id="35e2a-189">Header</span></span><br/>                   | <dl> <span data-ttu-id="35e2a-190"><dt>SSPI. h (include Security. h)</dt></span><span class="sxs-lookup"><span data-stu-id="35e2a-190"><dt>Sspi.h (include Security.h)</dt></span></span> </dl> |
| <span data-ttu-id="35e2a-191">Libreria</span><span class="sxs-lookup"><span data-stu-id="35e2a-191">Library</span></span><br/>                  | <dl> <span data-ttu-id="35e2a-192"><dt>Secur32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="35e2a-192"><dt>Secur32.lib</dt></span></span> </dl>                 |
| <span data-ttu-id="35e2a-193">DLL</span><span class="sxs-lookup"><span data-stu-id="35e2a-193">DLL</span></span><br/>                      | <dl> <span data-ttu-id="35e2a-194"><dt>Secur32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="35e2a-194"><dt>Secur32.dll</dt></span></span> </dl>                 |
| <span data-ttu-id="35e2a-195">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="35e2a-195">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="35e2a-196">**AcquireCredentialsHandleW** (Unicode) e **AcquireCredentialsHandleA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="35e2a-196">**AcquireCredentialsHandleW** (Unicode) and **AcquireCredentialsHandleA** (ANSI)</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="35e2a-197">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="35e2a-197">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35e2a-198">Funzioni SSPI</span><span class="sxs-lookup"><span data-stu-id="35e2a-198">SSPI Functions</span></span>](authentication-functions.md#sspi-functions)
</dt> <dt>

[<span data-ttu-id="35e2a-199">**AcceptSecurityContext (Kerberos)**</span><span class="sxs-lookup"><span data-stu-id="35e2a-199">**AcceptSecurityContext (Kerberos)**</span></span>](acceptsecuritycontext--kerberos.md)
</dt> <dt>

[<span data-ttu-id="35e2a-200">**InitializeSecurityContext (Kerberos)**</span><span class="sxs-lookup"><span data-stu-id="35e2a-200">**InitializeSecurityContext (Kerberos)**</span></span>](initializesecuritycontext--kerberos.md)
</dt> <dt>

[<span data-ttu-id="35e2a-201">**FreeCredentialsHandle**</span><span class="sxs-lookup"><span data-stu-id="35e2a-201">**FreeCredentialsHandle**</span></span>](/windows/win32/api/sspi/nf-sspi-freecredentialshandle)
</dt> </dl>

 

 
