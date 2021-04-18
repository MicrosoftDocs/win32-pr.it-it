---
description: Recupera la password dell'account del servizio.
ms.assetid: B3D3842F-ACEB-4979-B336-BA3D0143044C
title: Funzione GetServiceAccountPassword (Secpkg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetServiceAccountPassword
api_type:
- HeaderDef
api_location:
- Secpkg.h
ms.openlocfilehash: 08719fb2b7e4a775df890f20cd640d059cb44475
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315352"
---
# <a name="getserviceaccountpassword-function"></a><span data-ttu-id="3c2d2-103">GetServiceAccountPassword (funzione)</span><span class="sxs-lookup"><span data-stu-id="3c2d2-103">GetServiceAccountPassword function</span></span>

<span data-ttu-id="3c2d2-104">Recupera la password dell'account di servizio, disponibile per i [*provider di supporto*](/windows/desktop/SecGloss/s-gly) per la sicurezza (SSP), ad esempio SSP Kerberos.</span><span class="sxs-lookup"><span data-stu-id="3c2d2-104">Retrieves the service account password, available to [*security support providers*](/windows/desktop/SecGloss/s-gly) (SSPs), such as Kerberos SSP.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c2d2-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3c2d2-105">Syntax</span></span>


```C++
NTSTATUS NTAPI GetServiceAccountPassword(
  _In_        PUNICODE_STRING AccountName,
  _In_opt_    PUNICODE_STRING DomainName,
  _In_        CRED_FETCH      CredFetch,
  _Inout_opt_ FILETIME        *FileTimeExpiry,
  _Out_       PUNICODE_STRING CurrentPassword,
  _Out_       PUNICODE_STRING PreviousPassword,
  _Out_opt_   FILETIME        *FileTimeCurrPwdValidForOutbound
);
```



## <a name="parameters"></a><span data-ttu-id="3c2d2-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3c2d2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c2d2-107">*AccountName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3c2d2-107">*AccountName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c2d2-108">Nome account con terminazione null dell'account del servizio gestito del gruppo (gMSA).</span><span class="sxs-lookup"><span data-stu-id="3c2d2-108">Null-terminated account name of the Group Managed Service Account (gMSA) account.</span></span> <span data-ttu-id="3c2d2-109">Il nome utente può essere uno dei seguenti formati:</span><span class="sxs-lookup"><span data-stu-id="3c2d2-109">The user name can be one of the following forms:</span></span>

-   <span data-ttu-id="3c2d2-110">Nome dell'account SAM del gMSA.</span><span class="sxs-lookup"><span data-stu-id="3c2d2-110">SAM account name of the gMSA.</span></span>
-   <span data-ttu-id="3c2d2-111">Nome utente in un nome di dominio completo (FQDN), ad esempio *NomeDominio \* **\\** _username_ o **www.** _dominio_* _. com \\_ \* _nome_.</span><span class="sxs-lookup"><span data-stu-id="3c2d2-111">User name in a fully qualified domain name (FQDN), such as *DomainName\***\\**_UserName_ or **www.**_domain_*_.com\\_\*_name_.</span></span> <span data-ttu-id="3c2d2-112">Il nome utente deve essere solo un nome SAM.</span><span class="sxs-lookup"><span data-stu-id="3c2d2-112">The user name must be a SAM name only.</span></span> <span data-ttu-id="3c2d2-113">Il nome di dominio può essere un nome DNS o un nome NetBIOS.</span><span class="sxs-lookup"><span data-stu-id="3c2d2-113">The domain name can be a DNS name or a NetBIOS name.</span></span>
-   <span data-ttu-id="3c2d2-114">Nome dell'entità utente (UPN) implicito per l'account gMSA, ad esempio *some \* **@** _Domain_*_. com_\*, dove, in base alla definizione di un UPN implicito, il *dominio \* \* *. com** è il nome DNS del dominio effettivo.</span><span class="sxs-lookup"><span data-stu-id="3c2d2-114">Implicit user principal name (UPN) for the gMSA account, for example, *SomeName\***@**_Domain_*_.com_\* where, according to the definition of an implicit UPN, the *Domain\*\*\*.com*\* is the actual domain DNS name.</span></span>

</dd> <dt>

<span data-ttu-id="3c2d2-115">*NomeDominio* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="3c2d2-115">*DomainName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3c2d2-116">Nome di dominio facoltativo con terminazione null.</span><span class="sxs-lookup"><span data-stu-id="3c2d2-116">Optional null-terminated domain name.</span></span> <span data-ttu-id="3c2d2-117">Questa operazione è valida solo se il parametro *AccountName* è un nome account SAM.</span><span class="sxs-lookup"><span data-stu-id="3c2d2-117">This is valid only if the *AccountName* parameter is a SAM account name.</span></span> <span data-ttu-id="3c2d2-118">Il nome di dominio può essere solo un nome NetBIOS o un nome di dominio completo (FQDN).</span><span class="sxs-lookup"><span data-stu-id="3c2d2-118">The domain name can only be a NetBIOS name or a fully qualified domain name (FQDN).</span></span>

</dd> <dt>

<span data-ttu-id="3c2d2-119">*CredFetch* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3c2d2-119">*CredFetch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c2d2-120">Valore dell'enumerazione [**cred \_ Fetch**](cred-fetch.md) che specifica come recuperare le credenziali.</span><span class="sxs-lookup"><span data-stu-id="3c2d2-120">A value of the [**CRED\_FETCH**](cred-fetch.md) enumeration that specifies how to retrieve the credential.</span></span>



| <span data-ttu-id="3c2d2-121">Valore</span><span class="sxs-lookup"><span data-stu-id="3c2d2-121">Value</span></span>                                                                                                                                                                                                    | <span data-ttu-id="3c2d2-122">Significato</span><span class="sxs-lookup"><span data-stu-id="3c2d2-122">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CredFetchDefault"></span><span id="credfetchdefault"></span><span id="CREDFETCHDEFAULT"></span><dl> <span data-ttu-id="3c2d2-123"><dt>**CredFetchDefault**</dt></span><span class="sxs-lookup"><span data-stu-id="3c2d2-123"><dt>**CredFetchDefault**</dt></span></span> </dl> | <span data-ttu-id="3c2d2-124">Il sistema operativo tenta prima di tutto di recuperare la password dalla cache locale se non è il momento di recuperare la password.</span><span class="sxs-lookup"><span data-stu-id="3c2d2-124">The operating system first attempts to retrieve the password from the local cache if it is not time to fetch the password.</span></span> <span data-ttu-id="3c2d2-125">Se è il momento di recuperare la password, il sistema operativo Contatta il controller di dominio; in caso contrario, restituisce le password memorizzate nella cache con un valore di stato success.</span><span class="sxs-lookup"><span data-stu-id="3c2d2-125">If it is time to fetch the password, then the operating system contacts the domain controller, otherwise, return any cached passwords with a status value of success.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="CredFetchDPAPI"></span><span id="credfetchdpapi"></span><span id="CREDFETCHDPAPI"></span><dl> <span data-ttu-id="3c2d2-126"><dt>**CredFetchDPAPI**</dt></span><span class="sxs-lookup"><span data-stu-id="3c2d2-126"><dt>**CredFetchDPAPI**</dt></span></span> </dl>         | <span data-ttu-id="3c2d2-127">Restituisce le credenziali DPAPI locali al chiamante.</span><span class="sxs-lookup"><span data-stu-id="3c2d2-127">Returns the local DPAPI credential to the caller.</span></span> <span data-ttu-id="3c2d2-128">Generalmente i provider di servizi condivisi non richiedono l'utilizzo di questo valore.</span><span class="sxs-lookup"><span data-stu-id="3c2d2-128">SSPs generally would not require use of this value.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="CredFetchForced"></span><span id="credfetchforced"></span><span id="CREDFETCHFORCED"></span><dl> <span data-ttu-id="3c2d2-129"><dt>**CredFetchForced**</dt></span><span class="sxs-lookup"><span data-stu-id="3c2d2-129"><dt>**CredFetchForced**</dt></span></span> </dl>     | <span data-ttu-id="3c2d2-130">Impone al sistema operativo di provare a leggere la password dal controller di dominio.</span><span class="sxs-lookup"><span data-stu-id="3c2d2-130">Forces the operating system to attempt to read the password from the domain controller.</span></span> <span data-ttu-id="3c2d2-131">Durante il tempo di rollover della password, è possibile che la password sia stata modificata nel controller di dominio e in altri host membro, ma l'host membro gMSA riconosce la password come ancora valida.</span><span class="sxs-lookup"><span data-stu-id="3c2d2-131">During the password rollover time, the password may have changed at the domain controller and other member hosts, but the gMSA member host recognizes the password as still valid.</span></span> <span data-ttu-id="3c2d2-132">Ciò può verificarsi a causa di problemi di sfasamento dell'orologio tra controller di dominio diversi.</span><span class="sxs-lookup"><span data-stu-id="3c2d2-132">This can happen due to clock skew issues between different domain controllers.</span></span> <span data-ttu-id="3c2d2-133">Quando si specifica questo valore, il sistema operativo determina se è possibile che si verifichi una modifica della password a causa dello sfasamento dell'orologio e, in caso affermativo, recupera la password.</span><span class="sxs-lookup"><span data-stu-id="3c2d2-133">When this value is specified, the operating system determines if there could be a possible password change due to clock skew and if so, retrieves the password.</span></span> <span data-ttu-id="3c2d2-134">In caso contrario, vengono restituite le credenziali memorizzate nella cache.</span><span class="sxs-lookup"><span data-stu-id="3c2d2-134">Otherwise, the cached credential is returned.</span></span> <span data-ttu-id="3c2d2-135">Se non sono presenti credenziali memorizzate nella cache, il sistema operativo tenta di ottenerne uno dal controller di dominio.</span><span class="sxs-lookup"><span data-stu-id="3c2d2-135">If there is no cached credential, then the operating system attempts to get one from the domain controller.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="3c2d2-136">*FileTimeExpiry* \[ in, out, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="3c2d2-136">*FileTimeExpiry* \[in, out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3c2d2-137">In caso di input, se questo valore è diverso da null e non è un **FILETIME** zero, *FileTimeExpiry* contiene l'ora di scadenza delle credenziali dell'account del servizio note al chiamante.</span><span class="sxs-lookup"><span data-stu-id="3c2d2-137">On input, if this value is nonnull and is not a zero **FILETIME**, *FileTimeExpiry* contains the expiry time of the service account credentials as known to the caller.</span></span> <span data-ttu-id="3c2d2-138">Se il parametro *FileTimeExpiry* è uguale a una delle credenziali correnti, la chiamata ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="3c2d2-138">If the *FileTimeExpiry* parameter is the same as one of the current credentials, this call fails.</span></span> <span data-ttu-id="3c2d2-139">Nell'output il parametro *FileTimeExpiry* contiene l'ora di scadenza della credenziale restituita.</span><span class="sxs-lookup"><span data-stu-id="3c2d2-139">On output, the *FileTimeExpiry* parameter contains the expiry time of the credential being returned.</span></span>

</dd> <dt>

<span data-ttu-id="3c2d2-140">*CurrentPassword* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="3c2d2-140">*CurrentPassword* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3c2d2-141">Password corrente di gMSA.</span><span class="sxs-lookup"><span data-stu-id="3c2d2-141">The current password of the gMSA.</span></span>

</dd> <dt>

<span data-ttu-id="3c2d2-142">*PreviousPassword* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="3c2d2-142">*PreviousPassword* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3c2d2-143">Password precedente di gMSA.</span><span class="sxs-lookup"><span data-stu-id="3c2d2-143">The previous password of the gMSA.</span></span>

</dd> <dt>

<span data-ttu-id="3c2d2-144">*FileTimeCurrPwdValidForOutbound* \[ out, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="3c2d2-144">*FileTimeCurrPwdValidForOutbound* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3c2d2-145">Indica l'ora dopo la quale la password corrente è valida per le richieste in uscita.</span><span class="sxs-lookup"><span data-stu-id="3c2d2-145">Denotes the time after which the current password is valid for outbound requests.</span></span> <span data-ttu-id="3c2d2-146">Il chiamante deve confrontare l'ora corrente con questo valore e usare la password corrente restituita solo se l'ora corrente è maggiore o uguale al valore restituito da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="3c2d2-146">The caller should compare the current time with this value and use the current password returned only if the current time is greater than or equal to the value returned by this parameter.</span></span> <span data-ttu-id="3c2d2-147">L'uso di questo parametro è progettato per i chiamanti che non hanno ritentato la logica in uscita, ad esempio, NTLM.</span><span class="sxs-lookup"><span data-stu-id="3c2d2-147">The use of this parameter is designed for callers that do not have retry in the outbound logic, for example, NTLM.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c2d2-148">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3c2d2-148">Return value</span></span>

<span data-ttu-id="3c2d2-149">Se la funzione ha esito positivo, il valore restituito è STATUS \_ Success.</span><span class="sxs-lookup"><span data-stu-id="3c2d2-149">If the function succeeds, the return value is STATUS\_SUCCESS.</span></span>

<span data-ttu-id="3c2d2-150">Se la funzione ha esito negativo, il valore restituito è un codice NTSTATUS.</span><span class="sxs-lookup"><span data-stu-id="3c2d2-150">If the function fails, the return value is an NTSTATUS code.</span></span> <span data-ttu-id="3c2d2-151">Per altre informazioni, vedere [valori restituiti della funzione di criteri LSA](management-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="3c2d2-151">For more information, see [LSA Policy Function Return Values](management-return-values.md).</span></span>

<span data-ttu-id="3c2d2-152">È possibile usare la funzione [**LsaNtStatusToWinError**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsantstatustowinerror) per convertire il codice NTSTATUS in un codice di errore di Windows.</span><span class="sxs-lookup"><span data-stu-id="3c2d2-152">You can use the [**LsaNtStatusToWinError**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsantstatustowinerror) function to convert the NTSTATUS code to a Windows error code.</span></span>

<span data-ttu-id="3c2d2-153">Al termine dell'uso dei buffer restituiti nei parametri *CurrentPassword* e *PreviousPassword* , è possibile liberarli chiamando la funzione [**FreeLsaHeap**](/windows/desktop/api/ntlsa/nc-ntlsa-lsa_free_lsa_heap) .</span><span class="sxs-lookup"><span data-stu-id="3c2d2-153">When you have finished using the buffers returned in the *CurrentPassword* and *PreviousPassword* parameters, free them by calling the [**FreeLsaHeap**](/windows/desktop/api/ntlsa/nc-ntlsa-lsa_free_lsa_heap) function.</span></span>

## <a name="remarks"></a><span data-ttu-id="3c2d2-154">Commenti</span><span class="sxs-lookup"><span data-stu-id="3c2d2-154">Remarks</span></span>

<span data-ttu-id="3c2d2-155">La funzione **GetServiceAccountPassword** può essere chiamata negli scenari seguenti:</span><span class="sxs-lookup"><span data-stu-id="3c2d2-155">The **GetServiceAccountPassword** function can be called in the following scenarios:</span></span>

-   <span data-ttu-id="3c2d2-156">Dalle funzioni di accesso di Security Support Provider (SSP), il provider di servizi condivisi deve rilevare che la password dell'account del servizio \_ \_ viene utilizzata per accedere all'entità e deve verificare che il chiamante disponga del privilegio TCB o di un servizio di rete.</span><span class="sxs-lookup"><span data-stu-id="3c2d2-156">From the logon functions of Security Support Providers (SSP), the SSP should detect that the SERVICE\_ACCOUNT\_PASSWORD is being used to log on to the entity and should check that the caller has TCB privilege or is a network service.</span></span> <span data-ttu-id="3c2d2-157">Il provider di servizi condivisi deve consentire al processo di accesso di procedere ottenendo le credenziali più recenti chiamando la funzione **GetServiceAccountPassword** con il valore **CredFetchDefault** nell'enumerazione di [**\_ recupero cred**](cred-fetch.md) .</span><span class="sxs-lookup"><span data-stu-id="3c2d2-157">Then the SSP should allow the log on process to proceed by getting the latest credential by calling the **GetServiceAccountPassword** function with the **CredFetchDefault** value in the [**CRED\_FETCH**](cred-fetch.md) enumeration.</span></span>

-   <span data-ttu-id="3c2d2-158">Da SSP nelle chiamate [**InitializeSecurityContext**](../SecAuthN/initializesecuritycontext--general.md) e [**AcceptSecurityContext**](../SecAuthN/acceptsecuritycontext--general.md) .</span><span class="sxs-lookup"><span data-stu-id="3c2d2-158">From SSPs in their [**InitializeSecurityContext**](../SecAuthN/initializesecuritycontext--general.md) and [**AcceptSecurityContext**](../SecAuthN/acceptsecuritycontext--general.md) calls.</span></span> <span data-ttu-id="3c2d2-159">Gli SSP devono rilevare che la \_ password dell'account del servizio \_ viene usata per queste chiamate. se la chiamata è per le credenziali non primarie, il provider di servizi condivisi deve verificare che il chiamante abbia il privilegio TCB o sia un servizio di rete.</span><span class="sxs-lookup"><span data-stu-id="3c2d2-159">SSPs should detect that the SERVICE\_ACCOUNT\_PASSWORD is being used for these calls, and if the call is for nonprimary credentials, then the SSP should ensure that the caller has either TCB privilege or is a network service.</span></span> <span data-ttu-id="3c2d2-160">Il provider di servizi condivisi deve quindi chiamare la funzione **GetServiceAccountPassword** con il valore **CredFetchDefault** nell'enumerazione [**cred \_ Fetch**](cred-fetch.md) e procedere con la chiamata.</span><span class="sxs-lookup"><span data-stu-id="3c2d2-160">Then the SSP should call the **GetServiceAccountPassword** function with the **CredFetchDefault** value in the [**CRED\_FETCH**](cred-fetch.md) enumeration and proceed with the call.</span></span> <span data-ttu-id="3c2d2-161">Se le chiamate a **InitializeSecurityContext** e **AcceptSecurityContext** hanno esito negativo, il provider di servizi condivisi deve usare *FileTimeExpiry* recuperato dalla chiamata precedente a **GetServiceAccountPassword** e usarlo come input per chiamare nuovamente **GetServiceAccountPassword** usando il valore **CredFetchForced** nell'enumerazione di **\_ recupero cred** .</span><span class="sxs-lookup"><span data-stu-id="3c2d2-161">If the **InitializeSecurityContext** and **AcceptSecurityContext** calls fail, then the SSP should use the *FileTimeExpiry* retrieved from the previous call to **GetServiceAccountPassword** and use it as input to calling **GetServiceAccountPassword** again using the **CredFetchForced** value in the **CRED\_FETCH** enumeration.</span></span> <span data-ttu-id="3c2d2-162">Se è disponibile una nuova credenziale gMSA, la seconda chiamata avrà esito positivo con le nuove credenziali e il provider di servizi condivisi dovrà riprovare con le nuove credenziali.</span><span class="sxs-lookup"><span data-stu-id="3c2d2-162">If a new gMSA credential is available, the second call will succeed with new credentials, and the SSP should then retry with the new credentials.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c2d2-163">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3c2d2-163">Requirements</span></span>



| <span data-ttu-id="3c2d2-164">Requisito</span><span class="sxs-lookup"><span data-stu-id="3c2d2-164">Requirement</span></span> | <span data-ttu-id="3c2d2-165">Valore</span><span class="sxs-lookup"><span data-stu-id="3c2d2-165">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="3c2d2-166">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3c2d2-166">Minimum supported client</span></span><br/> | <span data-ttu-id="3c2d2-167">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="3c2d2-167">Windows 8 \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="3c2d2-168">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3c2d2-168">Minimum supported server</span></span><br/> | <span data-ttu-id="3c2d2-169">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="3c2d2-169">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="3c2d2-170">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3c2d2-170">Header</span></span><br/>                   | <dl> <span data-ttu-id="3c2d2-171"><dt>Secpkg. h</dt></span><span class="sxs-lookup"><span data-stu-id="3c2d2-171"><dt>Secpkg.h</dt></span></span> </dl> |



 

