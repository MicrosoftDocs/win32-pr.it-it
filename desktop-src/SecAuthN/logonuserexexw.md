---
description: La funzione LogonUserExExW tenta di registrare un utente nel computer locale.
ms.assetid: d90db4c6-a711-4519-8b91-5069cee07738
title: Funzione LogonUserExExW (Winbasep. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LogonUserExExW
api_type:
- DllExport
api_location:
- Advapi32.dll
ms.openlocfilehash: 35ec65e7899f45a5222ae12b08992e77ea67f306
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058037"
---
# <a name="logonuserexexw-function"></a><span data-ttu-id="2d00e-103">LogonUserExExW (funzione)</span><span class="sxs-lookup"><span data-stu-id="2d00e-103">LogonUserExExW function</span></span>

<span data-ttu-id="2d00e-104">La funzione **LogonUserExExW** tenta di registrare un utente nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="2d00e-104">The **LogonUserExExW** function attempts to log a user on to the local computer.</span></span> <span data-ttu-id="2d00e-105">Il computer locale è il computer da cui è stato chiamato **LogonUserExExW** .</span><span class="sxs-lookup"><span data-stu-id="2d00e-105">The local computer is the computer from which **LogonUserExExW** was called.</span></span> <span data-ttu-id="2d00e-106">Non è possibile usare **LogonUserExExW** per accedere a un computer remoto.</span><span class="sxs-lookup"><span data-stu-id="2d00e-106">You cannot use **LogonUserExExW** to log on to a remote computer.</span></span> <span data-ttu-id="2d00e-107">Specificare l'utente utilizzando un nome utente e un dominio e [*autenticare*](../secgloss/a-gly.md) l'utente utilizzando una password in testo non crittografato.</span><span class="sxs-lookup"><span data-stu-id="2d00e-107">Specify the user by using a user name and domain and [*authenticate*](../secgloss/a-gly.md) the user by using a plaintext password.</span></span> <span data-ttu-id="2d00e-108">Se la funzione ha esito positivo, riceve un handle per un token che rappresenta l'utente connesso.</span><span class="sxs-lookup"><span data-stu-id="2d00e-108">If the function succeeds, it receives a handle to a token that represents the logged-on user.</span></span> <span data-ttu-id="2d00e-109">È quindi possibile usare questo handle di token per rappresentare l'utente specificato o, nella maggior parte dei casi, per creare un [*processo*](../secgloss/p-gly.md) che viene eseguito nel contesto dell'utente specificato.</span><span class="sxs-lookup"><span data-stu-id="2d00e-109">You can then use this token handle to impersonate the specified user or, in most cases, to create a [*process*](../secgloss/p-gly.md) that runs in the context of the specified user.</span></span>

<span data-ttu-id="2d00e-110">Questa funzione è simile alla funzione [**LogonUserEx**](/windows/desktop/api/Winbase/nf-winbase-logonuserexa) , ma accetta il parametro aggiuntivo, *pTokenGroups*, che è un set di uno o più [*identificatori di sicurezza*](../secgloss/s-gly.md) (SID) aggiunti al token restituito al chiamante quando l'accesso ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="2d00e-110">This function is similar to the [**LogonUserEx**](/windows/desktop/api/Winbase/nf-winbase-logonuserexa) function, except that it takes the additional parameter, *pTokenGroups*, which is a set of one or more [*security identifiers*](../secgloss/s-gly.md) (SIDs) that are added to the token returned to the caller when the logon is successful.</span></span>

<span data-ttu-id="2d00e-111">Questa funzione non è dichiarata in un'intestazione pubblica e non dispone di librerie di importazione associate.</span><span class="sxs-lookup"><span data-stu-id="2d00e-111">This function is not declared in a public header and has no associated import library.</span></span> <span data-ttu-id="2d00e-112">È necessario utilizzare le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per collegare dinamicamente a Advapi32.dll.</span><span class="sxs-lookup"><span data-stu-id="2d00e-112">You must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Advapi32.dll.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d00e-113">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2d00e-113">Syntax</span></span>


```C++
BOOL WINAPI LogonUserExExW(
  _In_      LPTSTR        lpszUsername,
  _In_opt_  LPTSTR        lpszDomain,
  _In_opt_  LPTSTR        lpszPassword,
  _In_      DWORD         dwLogonType,
  _In_      DWORD         dwLogonProvider,
  _In_opt_  PTOKEN_GROUPS pTokenGroups,
  _Out_opt_ PHANDLE       phToken,
  _Out_opt_ PSID          *ppLogonSid,
  _Out_opt_ PVOID         *ppProfileBuffer,
  _Out_opt_ LPDWORD       pdwProfileLength,
  _Out_opt_ PQUOTA_LIMITS pQuotaLimits
);
```



## <a name="parameters"></a><span data-ttu-id="2d00e-114">Parametri</span><span class="sxs-lookup"><span data-stu-id="2d00e-114">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d00e-115">*lpszUsername* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2d00e-115">*lpszUsername* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d00e-116">Puntatore a una stringa con terminazione null che specifica il nome dell'utente.</span><span class="sxs-lookup"><span data-stu-id="2d00e-116">A pointer to a null-terminated string that specifies the name of the user.</span></span> <span data-ttu-id="2d00e-117">Si tratta del nome dell'account utente a cui accedere.</span><span class="sxs-lookup"><span data-stu-id="2d00e-117">This is the name of the user account to log on to.</span></span> <span data-ttu-id="2d00e-118">Se si usa il formato del [*nome dell'entità utente*](../secgloss/u-gly.md) (UPN), il parametro *LpszDomain* deve essere **null**.</span><span class="sxs-lookup"><span data-stu-id="2d00e-118">If you use the [*user principal name*](../secgloss/u-gly.md) (UPN) format, the *lpszDomain* parameter must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="2d00e-119">*lpszDomain* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="2d00e-119">*lpszDomain* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2d00e-120">Puntatore a una stringa con terminazione null che specifica il nome del dominio o del server il cui database di account contiene l'account *lpszUsername* .</span><span class="sxs-lookup"><span data-stu-id="2d00e-120">A pointer to a null-terminated string that specifies the name of the domain or server whose account database contains the *lpszUsername* account.</span></span> <span data-ttu-id="2d00e-121">Se questo parametro è **null**, il nome utente deve essere specificato in formato UPN.</span><span class="sxs-lookup"><span data-stu-id="2d00e-121">If this parameter is **NULL**, the user name must be specified in UPN format.</span></span> <span data-ttu-id="2d00e-122">Se questo parametro è ".", la funzione convalida l'account utilizzando solo il database di account locale.</span><span class="sxs-lookup"><span data-stu-id="2d00e-122">If this parameter is ".", the function validates the account by using only the local account database.</span></span>

</dd> <dt>

<span data-ttu-id="2d00e-123">*lpszPassword* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="2d00e-123">*lpszPassword* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2d00e-124">Puntatore a una stringa con terminazione null che specifica la password in testo non crittografato per l'account utente specificato da *lpszUsername*.</span><span class="sxs-lookup"><span data-stu-id="2d00e-124">A pointer to a null-terminated string that specifies the plaintext password for the user account specified by *lpszUsername*.</span></span> <span data-ttu-id="2d00e-125">Al termine dell'utilizzo della password, cancellare la password dalla memoria chiamando la funzione [**SecureZeroMemory**](/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="2d00e-125">When you have finished using the password, clear the password from memory by calling the [**SecureZeroMemory**](/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) function.</span></span> <span data-ttu-id="2d00e-126">Per ulteriori informazioni sulla protezione delle password, vedere [gestione delle password](../secbp/handling-passwords.md).</span><span class="sxs-lookup"><span data-stu-id="2d00e-126">For more information about protecting passwords, see [Handling Passwords](../secbp/handling-passwords.md).</span></span>

</dd> <dt>

<span data-ttu-id="2d00e-127">*dwLogonType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2d00e-127">*dwLogonType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d00e-128">Tipo di operazione di accesso da eseguire.</span><span class="sxs-lookup"><span data-stu-id="2d00e-128">The type of logon operation to perform.</span></span> <span data-ttu-id="2d00e-129">Questo parametro può avere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="2d00e-129">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="2d00e-130">Valore</span><span class="sxs-lookup"><span data-stu-id="2d00e-130">Value</span></span>                                                                                                                                                                                                                                                                        | <span data-ttu-id="2d00e-131">Significato</span><span class="sxs-lookup"><span data-stu-id="2d00e-131">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LOGON32_LOGON_INTERACTIVE"></span><span id="logon32_logon_interactive"></span><dl> <span data-ttu-id="2d00e-132"><dt>**LOGON32 \_ ACCESSO \_ interattivo**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="2d00e-132"><dt>**LOGON32\_LOGON\_INTERACTIVE**</dt> <dt>2</dt></span></span> </dl>                    | <span data-ttu-id="2d00e-133">Questo tipo di accesso è destinato agli utenti che utilizzano in modo interattivo il computer, ad esempio un utente connesso da un server [*Terminal*](../secgloss/t-gly.md) , una shell remota o un processo simile.</span><span class="sxs-lookup"><span data-stu-id="2d00e-133">This logon type is intended for users who will be interactively using the computer, such as a user being logged on by a [*terminal*](../secgloss/t-gly.md) server, remote shell, or similar process.</span></span> <span data-ttu-id="2d00e-134">Questo tipo di accesso comporta le spese aggiuntive per la memorizzazione nella cache delle informazioni di accesso per le operazioni disconnesse. Pertanto, non è appropriato per alcune applicazioni client/server, ad esempio un server di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="2d00e-134">This logon type has the additional expense of caching logon information for disconnected operations; therefore, it is inappropriate for some client/server applications, such as a mail server.</span></span><br/>                                  |
| <span id="LOGON32_LOGON_NETWORK"></span><span id="logon32_logon_network"></span><dl> <span data-ttu-id="2d00e-135"><dt>**LOGON32 \_ \_Rete di accesso**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="2d00e-135"><dt>**LOGON32\_LOGON\_NETWORK**</dt> <dt>3</dt></span></span> </dl>                                | <span data-ttu-id="2d00e-136">Questo tipo di accesso è destinato ai server ad alte prestazioni per l'autenticazione di password in testo non crittografato.</span><span class="sxs-lookup"><span data-stu-id="2d00e-136">This logon type is intended for high performance servers to authenticate plaintext passwords.</span></span> <span data-ttu-id="2d00e-137">La funzione **LogonUserExExW** non memorizza nella cache le credenziali per questo tipo di accesso.</span><span class="sxs-lookup"><span data-stu-id="2d00e-137">The **LogonUserExExW** function does not cache credentials for this logon type.</span></span><br/>                                                                                                                                                                                                                                                                                                 |
| <span id="LOGON32_LOGON_BATCH"></span><span id="logon32_logon_batch"></span><dl> <span data-ttu-id="2d00e-138"><dt>**LOGON32 \_ \_Batch di accesso**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="2d00e-138"><dt>**LOGON32\_LOGON\_BATCH**</dt> <dt>4</dt></span></span> </dl>                                      | <span data-ttu-id="2d00e-139">Questo tipo di accesso è destinato ai server batch, in cui i processi possono essere eseguiti per conto di un utente senza l'intervento diretto.</span><span class="sxs-lookup"><span data-stu-id="2d00e-139">This logon type is intended for batch servers, where processes may be executing on behalf of a user without their direct intervention.</span></span> <span data-ttu-id="2d00e-140">Questo tipo è anche per i server con prestazioni più elevate che elaborano molti tentativi di autenticazione in testo non crittografato alla volta, ad esempio posta elettronica o server Web.</span><span class="sxs-lookup"><span data-stu-id="2d00e-140">This type is also for higher performance servers that process many plaintext authentication attempts at a time, such as mail or web servers.</span></span> <span data-ttu-id="2d00e-141">La funzione **LogonUserExExW** non memorizza nella cache le credenziali per questo tipo di accesso.</span><span class="sxs-lookup"><span data-stu-id="2d00e-141">The **LogonUserExExW** function does not cache credentials for this logon type.</span></span><br/>                                                                                                           |
| <span id="LOGON32_LOGON_SERVICE"></span><span id="logon32_logon_service"></span><dl> <span data-ttu-id="2d00e-142"><dt>**LOGON32 \_ \_Servizio di accesso**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="2d00e-142"><dt>**LOGON32\_LOGON\_SERVICE**</dt> <dt>5</dt></span></span> </dl>                                | <span data-ttu-id="2d00e-143">Indica un accesso del tipo di servizio.</span><span class="sxs-lookup"><span data-stu-id="2d00e-143">Indicates a service-type logon.</span></span> <span data-ttu-id="2d00e-144">Per l'account specificato deve essere abilitato il privilegio servizio.</span><span class="sxs-lookup"><span data-stu-id="2d00e-144">The account provided must have the service privilege enabled.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="LOGON32_LOGON_UNLOCK"></span><span id="logon32_logon_unlock"></span><dl> <span data-ttu-id="2d00e-145"><dt>**LOGON32 \_ \_Sblocco di accesso**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="2d00e-145"><dt>**LOGON32\_LOGON\_UNLOCK**</dt> <dt>7</dt></span></span> </dl>                                   | <span data-ttu-id="2d00e-146">Questo tipo di accesso è per le dll [*Gina*](../secgloss/g-gly.md) che accedono agli utenti che utilizzeranno il computer in modo interattivo.</span><span class="sxs-lookup"><span data-stu-id="2d00e-146">This logon type is for [*GINA*](../secgloss/g-gly.md) DLLs that log on users who will be interactively using the computer.</span></span> <span data-ttu-id="2d00e-147">Questo tipo di accesso può generare un record di controllo univoco che indica quando la workstation è stata sbloccata.</span><span class="sxs-lookup"><span data-stu-id="2d00e-147">This logon type can generate a unique audit record that shows when the workstation was unlocked.</span></span><br/>                                                                                                                                                                                                                   |
| <span id="LOGON32_LOGON_NETWORK_CLEARTEXT"></span><span id="logon32_logon_network_cleartext"></span><dl> <span data-ttu-id="2d00e-148"><dt>**LOGON32 \_ Rete di accesso non \_ \_ crittografata**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="2d00e-148"><dt>**LOGON32\_LOGON\_NETWORK\_CLEARTEXT**</dt> <dt>8</dt></span></span> </dl> | <span data-ttu-id="2d00e-149">Questo tipo di accesso conserva il nome e la password nel [*pacchetto di autenticazione*](../secgloss/a-gly.md), che consente al server di stabilire connessioni ad altri server di rete durante la rappresentazione del client.</span><span class="sxs-lookup"><span data-stu-id="2d00e-149">This logon type preserves the name and password in the [*authentication package*](../secgloss/a-gly.md), which allows the server to make connections to other network servers while impersonating the client.</span></span> <span data-ttu-id="2d00e-150">Un server può accettare le credenziali in testo non crittografato da un client, chiamare **LogonUserExExW**, verificare che l'utente possa accedere al sistema attraverso la rete e continuare a comunicare con altri server.</span><span class="sxs-lookup"><span data-stu-id="2d00e-150">A server can accept plaintext credentials from a client, call **LogonUserExExW**, verify that the user can access the system across the network, and still communicate with other servers.</span></span> <br/> |
| <span id="LOGON32_LOGON_NEW_CREDENTIALS"></span><span id="logon32_logon_new_credentials"></span><dl> <span data-ttu-id="2d00e-151"><dt>**LOGON32 \_ \_Nuove \_ credenziali di accesso**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="2d00e-151"><dt>**LOGON32\_LOGON\_NEW\_CREDENTIALS**</dt> <dt>9</dt></span></span> </dl>       | <span data-ttu-id="2d00e-152">Questo tipo di accesso consente al chiamante di clonare il token corrente e di specificare nuove credenziali per le connessioni in uscita.</span><span class="sxs-lookup"><span data-stu-id="2d00e-152">This logon type allows the caller to clone its current token and specify new credentials for outbound connections.</span></span> <span data-ttu-id="2d00e-153">La nuova sessione di accesso ha lo stesso identificatore locale ma usa credenziali diverse per altre connessioni di rete.</span><span class="sxs-lookup"><span data-stu-id="2d00e-153">The new logon session has the same local identifier but uses different credentials for other network connections.</span></span><br/> <span data-ttu-id="2d00e-154">Questo tipo di accesso è supportato solo dal provider di accesso **\_ \_ WINNT50 del provider LOGON32** .</span><span class="sxs-lookup"><span data-stu-id="2d00e-154">This logon type is supported only by the **LOGON32\_PROVIDER\_WINNT50** logon provider.</span></span><br/>                                                                                                                                       |



 

</dd> <dt>

<span data-ttu-id="2d00e-155">*dwLogonProvider* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2d00e-155">*dwLogonProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d00e-156">Provider di accesso.</span><span class="sxs-lookup"><span data-stu-id="2d00e-156">The logon provider.</span></span> <span data-ttu-id="2d00e-157">Questo parametro può avere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="2d00e-157">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="2d00e-158">Valore</span><span class="sxs-lookup"><span data-stu-id="2d00e-158">Value</span></span>                                                                                                                                                                                           | <span data-ttu-id="2d00e-159">Significato</span><span class="sxs-lookup"><span data-stu-id="2d00e-159">Meaning</span></span>                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LOGON32_PROVIDER_DEFAULT"></span><span id="logon32_provider_default"></span><dl> <span data-ttu-id="2d00e-160"><dt>**\_Impostazione predefinita del provider LOGON32 \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2d00e-160"><dt>**LOGON32\_PROVIDER\_DEFAULT**</dt></span></span> </dl> | <span data-ttu-id="2d00e-161">Utilizzare il provider di accesso standard per il sistema.</span><span class="sxs-lookup"><span data-stu-id="2d00e-161">Use the standard logon provider for the system.</span></span> <span data-ttu-id="2d00e-162">Il [*provider di sicurezza*](../secgloss/s-gly.md) predefinito è NTLM.</span><span class="sxs-lookup"><span data-stu-id="2d00e-162">The default [*security provider*](../secgloss/s-gly.md) is NTLM.</span></span><br/> |
| <span id="LOGON32_PROVIDER_WINNT50"></span><span id="logon32_provider_winnt50"></span><dl> <span data-ttu-id="2d00e-163"><dt>**\_Provider LOGON32 \_ WINNT50**</dt></span><span class="sxs-lookup"><span data-stu-id="2d00e-163"><dt>**LOGON32\_PROVIDER\_WINNT50**</dt></span></span> </dl> | <span data-ttu-id="2d00e-164">Utilizzare il provider di accesso Negotiate.</span><span class="sxs-lookup"><span data-stu-id="2d00e-164">Use the negotiate logon provider.</span></span> <br/>                                                                                                                                                         |
| <span id="LOGON32_PROVIDER_WINNT40"></span><span id="logon32_provider_winnt40"></span><dl> <span data-ttu-id="2d00e-165"><dt>**\_Provider LOGON32 \_ WINNT40**</dt></span><span class="sxs-lookup"><span data-stu-id="2d00e-165"><dt>**LOGON32\_PROVIDER\_WINNT40**</dt></span></span> </dl> | <span data-ttu-id="2d00e-166">Utilizzare il provider di accesso NTLM.</span><span class="sxs-lookup"><span data-stu-id="2d00e-166">Use the NTLM logon provider.</span></span><br/>                                                                                                                                                               |



 

</dd> <dt>

<span data-ttu-id="2d00e-167">*pTokenGroups* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="2d00e-167">*pTokenGroups* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2d00e-168">Puntatore a una struttura [**di \_ gruppi di token**](/windows/win32/api/winnt/ns-winnt-token_groups) che specifica un elenco di SID di gruppo che vengono aggiunti al token che questa funzione riceve al completamento dell'accesso.</span><span class="sxs-lookup"><span data-stu-id="2d00e-168">A pointer to a [**TOKEN\_GROUPS**](/windows/win32/api/winnt/ns-winnt-token_groups) structure that specifies a list of group SIDs that are added to the token that this function receives upon successful logon.</span></span> <span data-ttu-id="2d00e-169">Eventuali SID aggiunti al token hanno effetto anche sull'espansione del gruppo.</span><span class="sxs-lookup"><span data-stu-id="2d00e-169">Any SIDs added to the token also effect group expansion.</span></span> <span data-ttu-id="2d00e-170">Se, ad esempio, i SID aggiunti sono membri dei gruppi locali, anche tali gruppi vengono aggiunti al token di accesso ricevuto.</span><span class="sxs-lookup"><span data-stu-id="2d00e-170">For example, if the added SIDs are members of local groups, those groups are also added to the received access token.</span></span>

<span data-ttu-id="2d00e-171">Se questo parametro non è **null**, il chiamante di questa funzione deve avere il privilegio di **\_ \_ privilegio se TCB** concesso e abilitato.</span><span class="sxs-lookup"><span data-stu-id="2d00e-171">If this parameter is not **NULL**, the caller of this function must have the **SE\_TCB\_PRIVILEGE** privilege granted and enabled.</span></span>

</dd> <dt>

<span data-ttu-id="2d00e-172">*phToken* \[ out, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="2d00e-172">*phToken* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2d00e-173">Puntatore a una variabile dell'handle che riceve un handle per un token che rappresenta l'utente specificato.</span><span class="sxs-lookup"><span data-stu-id="2d00e-173">A pointer to a handle variable that receives a handle to a token that represents the specified user.</span></span>

<span data-ttu-id="2d00e-174">È possibile usare l'handle restituito nelle chiamate alla funzione [**ImpersonateLoggedOnUser**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateloggedonuser) .</span><span class="sxs-lookup"><span data-stu-id="2d00e-174">You can use the returned handle in calls to the [**ImpersonateLoggedOnUser**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateloggedonuser) function.</span></span>

<span data-ttu-id="2d00e-175">Nella maggior parte dei casi, l'handle restituito è un [*token primario*](../secgloss/p-gly.md) che è possibile usare nelle chiamate alla funzione [**CreateProcessAsUser ha**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) .</span><span class="sxs-lookup"><span data-stu-id="2d00e-175">In most cases, the returned handle is a [*primary token*](../secgloss/p-gly.md) that you can use in calls to the [**CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) function.</span></span> <span data-ttu-id="2d00e-176">Tuttavia, se si specifica il \_ \_ flag di rete di accesso LOGON32, **LogonUserExExW** restituisce un [*token di rappresentazione*](../secgloss/i-gly.md) che non è possibile utilizzare in **CreateProcessAsUser ha** a meno che non si chiami [**DuplicateTokenEx**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-duplicatetokenex) per convertire il token di rappresentazione in un token primario.</span><span class="sxs-lookup"><span data-stu-id="2d00e-176">However, if you specify the LOGON32\_LOGON\_NETWORK flag, **LogonUserExExW** returns an [*impersonation token*](../secgloss/i-gly.md) that you cannot use in **CreateProcessAsUser** unless you call [**DuplicateTokenEx**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-duplicatetokenex) to convert the impersonation token to a primary token.</span></span>

<span data-ttu-id="2d00e-177">Quando questo handle non è più necessario, chiuderlo chiamando la funzione [**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle) .</span><span class="sxs-lookup"><span data-stu-id="2d00e-177">When you no longer need this handle, close it by calling the [**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle) function.</span></span>

</dd> <dt>

<span data-ttu-id="2d00e-178">*ppLogonSid* \[ out, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="2d00e-178">*ppLogonSid* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2d00e-179">Puntatore a un puntatore a un SID che riceve il SID dell'utente connesso.</span><span class="sxs-lookup"><span data-stu-id="2d00e-179">A pointer to a pointer to a SID that receives the SID of the user logged on.</span></span>

<span data-ttu-id="2d00e-180">Al termine dell'utilizzo del SID, liberarlo chiamando la funzione [**LocalFree**](/windows/win32/api/winbase/nf-winbase-localfree) .</span><span class="sxs-lookup"><span data-stu-id="2d00e-180">When you have finished using the SID, free it by calling the [**LocalFree**](/windows/win32/api/winbase/nf-winbase-localfree) function.</span></span>

</dd> <dt>

<span data-ttu-id="2d00e-181">*ppProfileBuffer* \[ out, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="2d00e-181">*ppProfileBuffer* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2d00e-182">Puntatore a un puntatore che riceve l'indirizzo di un buffer che contiene il profilo dell'utente connesso.</span><span class="sxs-lookup"><span data-stu-id="2d00e-182">A pointer to a pointer that receives the address of a buffer that contains the logged on user's profile.</span></span>

</dd> <dt>

<span data-ttu-id="2d00e-183">*pdwProfileLength* \[ out, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="2d00e-183">*pdwProfileLength* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2d00e-184">Puntatore a un **valore DWORD** che riceve la lunghezza del buffer del profilo.</span><span class="sxs-lookup"><span data-stu-id="2d00e-184">A pointer to a **DWORD** that receives the length of the profile buffer.</span></span>

</dd> <dt>

<span data-ttu-id="2d00e-185">*pQuotaLimits* \[ out, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="2d00e-185">*pQuotaLimits* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2d00e-186">Puntatore a una struttura [**di \_ limiti di quota**](/windows/desktop/api/Winnt/ns-winnt-quota_limits) che riceve informazioni sulle quote per l'utente che ha eseguito l'accesso.</span><span class="sxs-lookup"><span data-stu-id="2d00e-186">A pointer to a [**QUOTA\_LIMITS**](/windows/desktop/api/Winnt/ns-winnt-quota_limits) structure that receives information about the quotas for the logged on user.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d00e-187">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2d00e-187">Return value</span></span>

<span data-ttu-id="2d00e-188">Se la funzione ha esito positivo, la funzione restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="2d00e-188">If the function succeeds, the function returns nonzero.</span></span>

<span data-ttu-id="2d00e-189">Se la funzione ha esito negativo, viene restituito zero.</span><span class="sxs-lookup"><span data-stu-id="2d00e-189">If the function fails, it returns zero.</span></span> <span data-ttu-id="2d00e-190">Per informazioni dettagliate sull'errore, chiamare [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="2d00e-190">To get extended error information, call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="2d00e-191">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="2d00e-191">Remarks</span></span>

<span data-ttu-id="2d00e-192">Il tipo di accesso alla **\_ \_ rete di accesso LOGON32** è più veloce, ma presenta le limitazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="2d00e-192">The **LOGON32\_LOGON\_NETWORK** logon type is fastest, but it has the following limitations:</span></span>

-   <span data-ttu-id="2d00e-193">La funzione restituisce un [*token di rappresentazione*](../secgloss/i-gly.md), non un token primario.</span><span class="sxs-lookup"><span data-stu-id="2d00e-193">The function returns an [*impersonation token*](../secgloss/i-gly.md), not a primary token.</span></span> <span data-ttu-id="2d00e-194">Non è possibile usare questo token direttamente nella funzione [**CreateProcessAsUser ha**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) .</span><span class="sxs-lookup"><span data-stu-id="2d00e-194">You cannot use this token directly in the [**CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) function.</span></span> <span data-ttu-id="2d00e-195">Tuttavia, è possibile chiamare la funzione [**DuplicateTokenEx**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-duplicatetokenex) per convertire il token in un token primario e quindi usarlo in **CreateProcessAsUser ha**.</span><span class="sxs-lookup"><span data-stu-id="2d00e-195">However, you can call the [**DuplicateTokenEx**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-duplicatetokenex) function to convert the token to a primary token, and then use it in **CreateProcessAsUser**.</span></span>
-   <span data-ttu-id="2d00e-196">Se si converte il token in un token primario e lo si usa in [**CreateProcessAsUser ha**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) per avviare un processo, il nuovo processo non può accedere ad altre risorse di rete, ad esempio server remoti o stampanti, tramite il redirector.</span><span class="sxs-lookup"><span data-stu-id="2d00e-196">If you convert the token to a primary token and use it in [**CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) to start a process, the new process cannot access other network resources, such as remote servers or printers, through the redirector.</span></span> <span data-ttu-id="2d00e-197">Un'eccezione è che se la risorsa di rete non è controllata dall'accesso, il nuovo processo sarà in grado di accedervi.</span><span class="sxs-lookup"><span data-stu-id="2d00e-197">An exception is that if the network resource is not access controlled, then the new process will be able to access it.</span></span>

<span data-ttu-id="2d00e-198">L'account specificato da *lpszUsername* deve disporre dei diritti di account necessari.</span><span class="sxs-lookup"><span data-stu-id="2d00e-198">The account specified by *lpszUsername* must have the necessary account rights.</span></span> <span data-ttu-id="2d00e-199">Ad esempio, per accedere a un utente con il **flag \_ \_ interattivo accesso LOGON32** , l'utente o un gruppo a cui appartiene l'utente deve disporre dell'account **\_ \_ \_ nome di accesso interattivo se** .</span><span class="sxs-lookup"><span data-stu-id="2d00e-199">For example, to log on a user with the **LOGON32\_LOGON\_INTERACTIVE** flag, the user (or a group to which the user belongs) must have the **SE\_INTERACTIVE\_LOGON\_NAME** account right.</span></span> <span data-ttu-id="2d00e-200">Per un elenco dei diritti dell'account che interessano le varie operazioni di accesso, vedere [diritti di accesso agli oggetti account](../secmgmt/account-object-access-rights.md).</span><span class="sxs-lookup"><span data-stu-id="2d00e-200">For a list of the account rights that affect the various logon operations, see [Account Object Access Rights](../secmgmt/account-object-access-rights.md).</span></span>

<span data-ttu-id="2d00e-201">Un utente viene considerato connesso se esiste almeno un token.</span><span class="sxs-lookup"><span data-stu-id="2d00e-201">A user is considered logged on if at least one token exists.</span></span> <span data-ttu-id="2d00e-202">Se si chiama [**CreateProcessAsUser ha**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) e si chiude il token, l'utente viene comunque connesso fino al termine del processo e di tutti i processi figlio.</span><span class="sxs-lookup"><span data-stu-id="2d00e-202">If you call [**CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) and then close the token, the user is still logged on until the process (and all child processes) have ended.</span></span>

<span data-ttu-id="2d00e-203">Se viene specificato il parametro facoltativo *pTokenGroups* , LSA non aggiungerà automaticamente il SID locale o il SID di accesso.</span><span class="sxs-lookup"><span data-stu-id="2d00e-203">If the optional *pTokenGroups* parameter is supplied, LSA will not add either the local SID or the logon SID automatically.</span></span>

## <a name="requirements"></a><span data-ttu-id="2d00e-204">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2d00e-204">Requirements</span></span>



| <span data-ttu-id="2d00e-205">Requisito</span><span class="sxs-lookup"><span data-stu-id="2d00e-205">Requirement</span></span> | <span data-ttu-id="2d00e-206">Valore</span><span class="sxs-lookup"><span data-stu-id="2d00e-206">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d00e-207">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2d00e-207">Minimum supported client</span></span><br/> | <span data-ttu-id="2d00e-208">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2d00e-208">Windows Vista \[desktop apps only\]</span></span><br/>                                                                        |
| <span data-ttu-id="2d00e-209">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2d00e-209">Minimum supported server</span></span><br/> | <span data-ttu-id="2d00e-210">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2d00e-210">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                  |
| <span data-ttu-id="2d00e-211">Versione</span><span class="sxs-lookup"><span data-stu-id="2d00e-211">Version</span></span><br/>                  | <span data-ttu-id="2d00e-212">LogonUserExExW è disponibile anche in Windows Server 2003 o Windows XPwith la versione di distribuzione generale.</span><span class="sxs-lookup"><span data-stu-id="2d00e-212">LogonUserExExW is also available onWindows Server 2003 or Windows XPwith the General Distribution Release.</span></span><br/> |
| <span data-ttu-id="2d00e-213">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2d00e-213">Header</span></span><br/>                   | <dl> <span data-ttu-id="2d00e-214"><dt>Winbasep. h</dt></span><span class="sxs-lookup"><span data-stu-id="2d00e-214"><dt>Winbasep.h</dt></span></span> </dl>                                 |
| <span data-ttu-id="2d00e-215">DLL</span><span class="sxs-lookup"><span data-stu-id="2d00e-215">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2d00e-216"><dt>Advapi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2d00e-216"><dt>Advapi32.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="2d00e-217">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2d00e-217">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d00e-218">Controllo di accesso client/server</span><span class="sxs-lookup"><span data-stu-id="2d00e-218">Client/Server Access Control</span></span>](../secauthz/client-server-access-control.md)
</dt> <dt>

[<span data-ttu-id="2d00e-219">Funzioni di controllo di accesso client/server</span><span class="sxs-lookup"><span data-stu-id="2d00e-219">Client/Server Access Control Functions</span></span>](../secauthz/authorization-functions.md)
</dt> <dt>

[<span data-ttu-id="2d00e-220">**CloseHandle**</span><span class="sxs-lookup"><span data-stu-id="2d00e-220">**CloseHandle**</span></span>](/windows/win32/api/handleapi/nf-handleapi-closehandle)
</dt> <dt>

[<span data-ttu-id="2d00e-221">**CreateProcessAsUser ha**</span><span class="sxs-lookup"><span data-stu-id="2d00e-221">**CreateProcessAsUser**</span></span>](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera)
</dt> <dt>

[<span data-ttu-id="2d00e-222">**DuplicateTokenEx**</span><span class="sxs-lookup"><span data-stu-id="2d00e-222">**DuplicateTokenEx**</span></span>](/windows/win32/api/securitybaseapi/nf-securitybaseapi-duplicatetokenex)
</dt> <dt>

[<span data-ttu-id="2d00e-223">**ImpersonateLoggedOnUser**</span><span class="sxs-lookup"><span data-stu-id="2d00e-223">**ImpersonateLoggedOnUser**</span></span>](/windows/win32/api/securitybaseapi/nf-securitybaseapi-impersonateloggedonuser)
</dt> <dt>

[<span data-ttu-id="2d00e-224">**LogonUserEx**</span><span class="sxs-lookup"><span data-stu-id="2d00e-224">**LogonUserEx**</span></span>](/windows/desktop/api/Winbase/nf-winbase-logonuserexa)
</dt> <dt>

[<span data-ttu-id="2d00e-225">**limiti di QUOTA \_**</span><span class="sxs-lookup"><span data-stu-id="2d00e-225">**QUOTA\_LIMITS**</span></span>](/windows/desktop/api/Winnt/ns-winnt-quota_limits)
</dt> </dl>

 

 
