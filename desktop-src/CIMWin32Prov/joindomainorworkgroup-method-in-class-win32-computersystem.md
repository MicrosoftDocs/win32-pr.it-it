---
description: Aggiunge un computer a un dominio o a un gruppo di lavoro.
ms.assetid: b9421f04-9b56-4413-af5c-12dffeb6f0c8
ms.tgt_platform: multiple
title: Metodo JoinDomainOrWorkgroup della classe Win32_ComputerSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ComputerSystem.JoinDomainOrWorkgroup
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 927dd6b2664c92ff07e94407fdc59fdd917363dd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878170"
---
# <a name="joindomainorworkgroup-method-of-the-win32_computersystem-class"></a><span data-ttu-id="a9af0-103">Metodo JoinDomainOrWorkgroup della \_ classe ComputerSystem Win32</span><span class="sxs-lookup"><span data-stu-id="a9af0-103">JoinDomainOrWorkgroup method of the Win32\_ComputerSystem class</span></span>

<span data-ttu-id="a9af0-104">Il metodo **JoinDomainOrWorkGroup** aggiunge un computer a un dominio o a un gruppo di lavoro.</span><span class="sxs-lookup"><span data-stu-id="a9af0-104">The **JoinDomainOrWorkgroup** method joins a computer system to a domain or workgroup.</span></span>

<span data-ttu-id="a9af0-105">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="a9af0-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="a9af0-106">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="a9af0-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="a9af0-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a9af0-107">Syntax</span></span>


```mof
uint32 JoinDomainOrWorkgroup(
  [in] string Name,
  [in] string Password,
  [in] string UserName,
  [in] string AccountOU,
  [in] uint32 FJoinOptions = 
);
```



## <a name="parameters"></a><span data-ttu-id="a9af0-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="a9af0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a9af0-109">*Nome* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a9af0-109">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9af0-110">Specifica il dominio o il gruppo di lavoro da unire.</span><span class="sxs-lookup"><span data-stu-id="a9af0-110">Specifies the domain or workgroup to join.</span></span> <span data-ttu-id="a9af0-111">Non può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="a9af0-111">Cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="a9af0-112">*Password* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="a9af0-112">*Password* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9af0-113">Se il parametro *username* specifica un nome di account, il parametro *password* deve puntare alla password da usare per la connessione al controller di dominio.</span><span class="sxs-lookup"><span data-stu-id="a9af0-113">If the *UserName* parameter specifies an account name, the *Password* parameter must point to the password to use when connecting to the domain controller.</span></span> <span data-ttu-id="a9af0-114">In caso contrario, questo parametro deve essere **null**.</span><span class="sxs-lookup"><span data-stu-id="a9af0-114">Otherwise, this parameter must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="a9af0-115">*Nome utente* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a9af0-115">*UserName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9af0-116">Puntatore a una stringa di caratteri con terminazione **null** costante che specifica il nome dell'account da utilizzare per la connessione al controller di dominio.</span><span class="sxs-lookup"><span data-stu-id="a9af0-116">Pointer to a constant **null**-terminated character string that specifies the account name to use when connecting to the domain controller.</span></span> <span data-ttu-id="a9af0-117">È necessario specificare un nome NetBIOS di dominio e un account utente, ad esempio dominio \\ utente.</span><span class="sxs-lookup"><span data-stu-id="a9af0-117">Must specify a domain NetBIOS name and user account, for example, Domain\\user.</span></span> <span data-ttu-id="a9af0-118">Se questo parametro è **null**, vengono utilizzate le informazioni sul chiamante.</span><span class="sxs-lookup"><span data-stu-id="a9af0-118">If this parameter is **NULL**, the caller information is used.</span></span>

<span data-ttu-id="a9af0-119">È anche possibile usare il nome dell'entità utente (ALZAto) nel modulo user@domain .</span><span class="sxs-lookup"><span data-stu-id="a9af0-119">You can also use the user principal name (UPPED) in the form user@domain.</span></span>

</dd> <dt>

<span data-ttu-id="a9af0-120">*AccountOU* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a9af0-120">*AccountOU* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9af0-121">Specifica il puntatore a una stringa di caratteri con terminazione **null** costante contenente il nome in formato [RFC 1779](https://www.ietf.org/rfc/rfc1779.txt) dell'unità organizzativa (OU) per l'account computer.</span><span class="sxs-lookup"><span data-stu-id="a9af0-121">Specifies the pointer to a constant **null**-terminated character string that contains the [RFC 1779](https://www.ietf.org/rfc/rfc1779.txt) format name of the organizational unit (OU) for the computer account.</span></span> <span data-ttu-id="a9af0-122">Se si specifica questo parametro, la stringa deve contenere un percorso completo; in caso contrario, l' *accento* deve essere **null**.</span><span class="sxs-lookup"><span data-stu-id="a9af0-122">If you specify this parameter, the string must contain a full path, otherwise *Accent* must be **NULL**.</span></span>

<span data-ttu-id="a9af0-123">Esempio: "OU = texttesto; DC = dominio; DC = dominio; DC = com "</span><span class="sxs-lookup"><span data-stu-id="a9af0-123">Example: "OU=testOU; DC=domain; DC=Domain; DC=com"</span></span>

</dd> <dt>

<span data-ttu-id="a9af0-124">*FJoinOptions* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a9af0-124">*FJoinOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9af0-125">Set di flag di bit che definiscono le opzioni di join.</span><span class="sxs-lookup"><span data-stu-id="a9af0-125">Set of bit flags that define the join options.</span></span>

<dt>



 <span data-ttu-id="a9af0-126"> (0)</span><span class="sxs-lookup"><span data-stu-id="a9af0-126">(0)</span></span>


</dt> <dd>

<span data-ttu-id="a9af0-127">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="a9af0-127">Default.</span></span> <span data-ttu-id="a9af0-128">Nessuna opzione di join.</span><span class="sxs-lookup"><span data-stu-id="a9af0-128">No join options.</span></span>

</dd> <dt>

<span id="NETSETUP_JOIN_DOMAIN"></span><span id="netsetup_join_domain"></span>

<span data-ttu-id="a9af0-129"><span id="NETSETUP_JOIN_DOMAIN"></span><span id="netsetup_join_domain"></span>**Netsetup \_ Aggiunta a un \_ dominio** (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="a9af0-129"><span id="NETSETUP_JOIN_DOMAIN"></span><span id="netsetup_join_domain"></span>**NETSETUP\_JOIN\_DOMAIN** (0x00000001)</span></span>


</dt> <dd>

<span data-ttu-id="a9af0-130">Aggiunge il computer a un dominio.</span><span class="sxs-lookup"><span data-stu-id="a9af0-130">Joins the computer to a domain.</span></span> <span data-ttu-id="a9af0-131">Se questo valore non è specificato, aggiunge il computer a un gruppo di lavoro.</span><span class="sxs-lookup"><span data-stu-id="a9af0-131">If this value is not specified, joins the computer to a workgroup.</span></span>

</dd> <dt>

<span id="NETSETUP_ACCT_CREATE"></span><span id="netsetup_acct_create"></span>

<span data-ttu-id="a9af0-132"><span id="NETSETUP_ACCT_CREATE"></span><span id="netsetup_acct_create"></span>**Netsetup \_ \_Creazione Acct** (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="a9af0-132"><span id="NETSETUP_ACCT_CREATE"></span><span id="netsetup_acct_create"></span>**NETSETUP\_ACCT\_CREATE** (0x00000002)</span></span>


</dt> <dd>

<span data-ttu-id="a9af0-133">Crea l'account nel dominio.</span><span class="sxs-lookup"><span data-stu-id="a9af0-133">Creates the account on the domain.</span></span>

</dd> <dt>

<span id="NETSETUP_WIN9X_UPGRADE"></span><span id="netsetup_win9x_upgrade"></span>

<span data-ttu-id="a9af0-134"><span id="NETSETUP_WIN9X_UPGRADE"></span><span id="netsetup_win9x_upgrade"></span>**Netsetup \_ \_Aggiornamento di Win9x** (0x00000010)</span><span class="sxs-lookup"><span data-stu-id="a9af0-134"><span id="NETSETUP_WIN9X_UPGRADE"></span><span id="netsetup_win9x_upgrade"></span>**NETSETUP\_WIN9X\_UPGRADE** (0x00000010)</span></span>


</dt> <dd>

<span data-ttu-id="a9af0-135">L'operazione di join si verifica come parte di un aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="a9af0-135">The join operation is occurring as part of an upgrade.</span></span>

</dd> <dt>

<span id="NETSETUP_DOMAIN_JOIN_IF_JOINED"></span><span id="netsetup_domain_join_if_joined"></span>

<span data-ttu-id="a9af0-136"><span id="NETSETUP_DOMAIN_JOIN_IF_JOINED"></span><span id="netsetup_domain_join_if_joined"></span>**Netsetup \_ \_Aggiunta a un dominio \_ se \_ aggiunto** (0x00000020)</span><span class="sxs-lookup"><span data-stu-id="a9af0-136"><span id="NETSETUP_DOMAIN_JOIN_IF_JOINED"></span><span id="netsetup_domain_join_if_joined"></span>**NETSETUP\_DOMAIN\_JOIN\_IF\_JOINED** (0x00000020)</span></span>


</dt> <dd>

<span data-ttu-id="a9af0-137">Consente un join a un nuovo dominio anche se il computer è già aggiunto a un dominio.</span><span class="sxs-lookup"><span data-stu-id="a9af0-137">Allows a join to a new domain even if the computer is already joined to a domain.</span></span>

</dd> <dt>

<span id="NETSETUP_JOIN_UNSECURE"></span><span id="netsetup_join_unsecure"></span>

<span data-ttu-id="a9af0-138"><span id="NETSETUP_JOIN_UNSECURE"></span><span id="netsetup_join_unsecure"></span>**Netsetup \_ JOIN non \_ sicuro** (0x00000040)</span><span class="sxs-lookup"><span data-stu-id="a9af0-138"><span id="NETSETUP_JOIN_UNSECURE"></span><span id="netsetup_join_unsecure"></span>**NETSETUP\_JOIN\_UNSECURE** (0x00000040)</span></span>


</dt> <dd>

<span data-ttu-id="a9af0-139">esegue un join non sicuro.</span><span class="sxs-lookup"><span data-stu-id="a9af0-139">Performs an unsecured join.</span></span>

<span data-ttu-id="a9af0-140">Questa opzione richiede l'aggiunta di un dominio a un account creato in precedenza senza eseguire l'autenticazione con le credenziali utente di dominio.</span><span class="sxs-lookup"><span data-stu-id="a9af0-140">This option requests a domain join to a pre-created account without authenticating with domain user credentials.</span></span> <span data-ttu-id="a9af0-141">Questa opzione può essere usata in combinazione con l'opzione **Netsetup \_ Machine \_ pwd \_ passata** .</span><span class="sxs-lookup"><span data-stu-id="a9af0-141">This option can be used in conjunction with **NETSETUP\_MACHINE\_PWD\_PASSED** option.</span></span> <span data-ttu-id="a9af0-142">In questo caso, *password* è la password dell'account computer creato in precedenza.</span><span class="sxs-lookup"><span data-stu-id="a9af0-142">In this case, *Password* is the password of the pre-created machine account.</span></span>

<span data-ttu-id="a9af0-143">Prima di Windows Vista con SP1 e Windows Server 2008, un join non sicuro non è stato autenticato nel controller di dominio.</span><span class="sxs-lookup"><span data-stu-id="a9af0-143">Prior to Windows Vista with SP1 and Windows Server 2008, an unsecure join did not authenticate to the domain controller.</span></span> <span data-ttu-id="a9af0-144">Tutte le comunicazioni sono state eseguite utilizzando una sessione null (non autenticata).</span><span class="sxs-lookup"><span data-stu-id="a9af0-144">All communication was performed using a null (unauthenticated) session.</span></span> <span data-ttu-id="a9af0-145">A partire da Windows Vista con SP1 e Windows Server 2008, il nome e la password dell'account del computer vengono utilizzati per l'autenticazione nel controller di dominio.</span><span class="sxs-lookup"><span data-stu-id="a9af0-145">Starting with Windows Vista with SP1 and Windows Server 2008, the machine account name and password are used to authenticate to the domain controller.</span></span>

</dd> <dt>

<span id="NETSETUP_MACHINE_PWD_PASSED"></span><span id="netsetup_machine_pwd_passed"></span>

<span data-ttu-id="a9af0-146"><span id="NETSETUP_MACHINE_PWD_PASSED"></span><span id="netsetup_machine_pwd_passed"></span>**Netsetup \_ \_Pwd computer \_ superato** (0x00000080)</span><span class="sxs-lookup"><span data-stu-id="a9af0-146"><span id="NETSETUP_MACHINE_PWD_PASSED"></span><span id="netsetup_machine_pwd_passed"></span>**NETSETUP\_MACHINE\_PWD\_PASSED** (0x00000080)</span></span>


</dt> <dd>

<span data-ttu-id="a9af0-147">Indica che il parametro *password* specifica una password dell'account del computer locale anziché una password utente.</span><span class="sxs-lookup"><span data-stu-id="a9af0-147">Indicates that the *Password* parameter specifies a local machine account password rather than a user password.</span></span> <span data-ttu-id="a9af0-148">Questo flag è valido solo per i join non protetti, che è necessario indicare impostando anche il flag di \_ aggiunta Netsetup join non \_ sicuro.</span><span class="sxs-lookup"><span data-stu-id="a9af0-148">This flag is valid only for unsecured joins, which you must indicate by also setting the NETSETUP\_JOIN\_UNSECURE flag.</span></span>

<span data-ttu-id="a9af0-149">Se si imposta questo flag, dopo che l'operazione di join ha avuto esito positivo, la password del computer verrà impostata sul valore di *password*, se tale valore è una password del computer valida.</span><span class="sxs-lookup"><span data-stu-id="a9af0-149">If you set this flag, then after the join operation succeeds, the machine password will be set to the value of *Password*, if that value is a valid machine password.</span></span>

</dd> <dt>

<span id="NETSETUP_DEFER_SPN_SET"></span><span id="netsetup_defer_spn_set"></span>

<span data-ttu-id="a9af0-150"><span id="NETSETUP_DEFER_SPN_SET"></span><span id="netsetup_defer_spn_set"></span>**Netsetup \_ RINVIA \_ \_ set SPN** (0x00000100)</span><span class="sxs-lookup"><span data-stu-id="a9af0-150"><span id="NETSETUP_DEFER_SPN_SET"></span><span id="netsetup_defer_spn_set"></span>**NETSETUP\_DEFER\_SPN\_SET** (0x00000100)</span></span>


</dt> <dd>

<span data-ttu-id="a9af0-151">Indica che il nome dell'entità servizio (SPN) e le proprietà DnsHostName dell'oggetto computer non devono essere aggiornati in questo momento.</span><span class="sxs-lookup"><span data-stu-id="a9af0-151">Indicates that the service principal name (SPN) and the DnsHostName properties on the computer object should not be updated at this time.</span></span>

<span data-ttu-id="a9af0-152">In genere, queste proprietà vengono aggiornate durante l'operazione di join.</span><span class="sxs-lookup"><span data-stu-id="a9af0-152">Typically, these properties are updated during the join operation.</span></span> <span data-ttu-id="a9af0-153">Al contrario, queste proprietà devono essere aggiornate durante una chiamata successiva al metodo [**Rename**](rename-method-in-class-win32-computersystem.md) .</span><span class="sxs-lookup"><span data-stu-id="a9af0-153">Instead, these properties should be updated during a subsequent call to the [**Rename**](rename-method-in-class-win32-computersystem.md) method.</span></span> <span data-ttu-id="a9af0-154">Queste proprietà vengono sempre aggiornate durante l'operazione di ridenominazione.</span><span class="sxs-lookup"><span data-stu-id="a9af0-154">These properties are always updated during the rename operation.</span></span>

</dd> <dt>

<span id="NETSETUP_JOIN_DC_ACCOUNT"></span><span id="netsetup_join_dc_account"></span>

<span data-ttu-id="a9af0-155"><span id="NETSETUP_JOIN_DC_ACCOUNT"></span><span id="netsetup_join_dc_account"></span>**Netsetup \_ Unisci \_ \_ account controller** di dominio (0x00000200)</span><span class="sxs-lookup"><span data-stu-id="a9af0-155"><span id="NETSETUP_JOIN_DC_ACCOUNT"></span><span id="netsetup_join_dc_account"></span>**NETSETUP\_JOIN\_DC\_ACCOUNT** (0x00000200)</span></span>


</dt> <dd>

<span data-ttu-id="a9af0-156">Consentire l'aggiunta a un dominio se l'account esistente è un controller di dominio.</span><span class="sxs-lookup"><span data-stu-id="a9af0-156">Allow the domain join if existing account is a domain controller.</span></span>

> [!Note]  
> <span data-ttu-id="a9af0-157">Questo flag è supportato in Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="a9af0-157">This flag is supported on Windows Vista and later.</span></span>

 

</dd> <dt>

<span id="NETSETUP_AMBIGUOUS_DC"></span><span id="netsetup_ambiguous_dc"></span>

<span data-ttu-id="a9af0-158"><span id="NETSETUP_AMBIGUOUS_DC"></span><span id="netsetup_ambiguous_dc"></span>**Netsetup \_ \_DC ambiguo** (0x00001000)</span><span class="sxs-lookup"><span data-stu-id="a9af0-158"><span id="NETSETUP_AMBIGUOUS_DC"></span><span id="netsetup_ambiguous_dc"></span>**NETSETUP\_AMBIGUOUS\_DC** (0x00001000)</span></span>


</dt> <dd>

<span data-ttu-id="a9af0-159">Quando si aggiunge il dominio, non provare a impostare il controller di dominio preferito nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="a9af0-159">When joining the domain don't try to set the preferred domain controller in the registry.</span></span>

> [!Note]  
> <span data-ttu-id="a9af0-160">Questo flag è supportato in Windows 7, Windows Server 2008 R2 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="a9af0-160">This flag is supported on Windows 7, Windows Server 2008 R2, and later.</span></span>

 

</dd> <dt>

<span id="NETSETUP_NO_NETLOGON_CACHE"></span><span id="netsetup_no_netlogon_cache"></span>

<span data-ttu-id="a9af0-161"><span id="NETSETUP_NO_NETLOGON_CACHE"></span><span id="netsetup_no_netlogon_cache"></span>**Netsetup \_ Nessuna \_ \_ cache di Netlogon** (0x00002000)</span><span class="sxs-lookup"><span data-stu-id="a9af0-161"><span id="NETSETUP_NO_NETLOGON_CACHE"></span><span id="netsetup_no_netlogon_cache"></span>**NETSETUP\_NO\_NETLOGON\_CACHE** (0x00002000)</span></span>


</dt> <dd>

<span data-ttu-id="a9af0-162">Quando si aggiunge il dominio, non creare la cache di Netlogon.</span><span class="sxs-lookup"><span data-stu-id="a9af0-162">When joining the domain don't create the Netlogon cache.</span></span>

> [!Note]  
> <span data-ttu-id="a9af0-163">Questo flag è supportato in Windows 7, Windows Server 2008 R2 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="a9af0-163">This flag is supported on Windows 7, Windows Server 2008 R2, and later.</span></span>

 

</dd> <dt>

<span id="NETSETUP_DONT_CONTROL_SERVICES"></span><span id="netsetup_dont_control_services"></span>

<span data-ttu-id="a9af0-164"><span id="NETSETUP_DONT_CONTROL_SERVICES"></span><span id="netsetup_dont_control_services"></span>**Netsetup \_ \_ \_ Servizi di controllo dont** (0x00004000)</span><span class="sxs-lookup"><span data-stu-id="a9af0-164"><span id="NETSETUP_DONT_CONTROL_SERVICES"></span><span id="netsetup_dont_control_services"></span>**NETSETUP\_DONT\_CONTROL\_SERVICES** (0x00004000)</span></span>


</dt> <dd>

<span data-ttu-id="a9af0-165">Quando si aggiunge il dominio, non forzare l'avvio del servizio Netlogon.</span><span class="sxs-lookup"><span data-stu-id="a9af0-165">When joining the domain don't force Netlogon service to start.</span></span>

> [!Note]  
> <span data-ttu-id="a9af0-166">Questo flag è supportato in Windows 7, Windows Server 2008 R2 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="a9af0-166">This flag is supported on Windows 7, Windows Server 2008 R2, and later.</span></span>

 

</dd> <dt>

<span id="NETSETUP_SET_MACHINE_NAME"></span><span id="netsetup_set_machine_name"></span>

<span data-ttu-id="a9af0-167"><span id="NETSETUP_SET_MACHINE_NAME"></span><span id="netsetup_set_machine_name"></span>**Netsetup \_ IMPOSTA \_ il \_ nome del computer** (0x00008000)</span><span class="sxs-lookup"><span data-stu-id="a9af0-167"><span id="NETSETUP_SET_MACHINE_NAME"></span><span id="netsetup_set_machine_name"></span>**NETSETUP\_SET\_MACHINE\_NAME** (0x00008000)</span></span>


</dt> <dd>

<span data-ttu-id="a9af0-168">Quando si aggiunge il dominio solo per il join offline, impostare il nome host del computer di destinazione e il nome NetBIOS.</span><span class="sxs-lookup"><span data-stu-id="a9af0-168">When joining the domain for offline join only, set target machine hostname and NetBIOS name.</span></span>

> [!Note]  
> <span data-ttu-id="a9af0-169">Questo flag è supportato in Windows 7, Windows Server 2008 R2 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="a9af0-169">This flag is supported on Windows 7, Windows Server 2008 R2, and later.</span></span>

 

</dd> <dt>

<span id="NETSETUP_FORCE_SPN_SET"></span><span id="netsetup_force_spn_set"></span>

<span data-ttu-id="a9af0-170"><span id="NETSETUP_FORCE_SPN_SET"></span><span id="netsetup_force_spn_set"></span>**Netsetup \_ FORCE \_ \_ set SPN** (0x00010000)</span><span class="sxs-lookup"><span data-stu-id="a9af0-170"><span id="NETSETUP_FORCE_SPN_SET"></span><span id="netsetup_force_spn_set"></span>**NETSETUP\_FORCE\_SPN\_SET** (0x00010000)</span></span>


</dt> <dd>

<span data-ttu-id="a9af0-171">Quando si aggiunge il dominio, eseguire l'override di altre impostazioni durante l'aggiunta a un dominio e impostare il nome dell'entità servizio (SPN).</span><span class="sxs-lookup"><span data-stu-id="a9af0-171">When joining the domain, override other settings during domain join and set the service principal name (SPN).</span></span>

> [!Note]  
> <span data-ttu-id="a9af0-172">Questo flag è supportato in Windows 7, Windows Server 2008 R2 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="a9af0-172">This flag is supported on Windows 7, Windows Server 2008 R2, and later.</span></span>

 

</dd> <dt>

<span id="NETSETUP_NO_ACCT_REUSE"></span><span id="netsetup_no_acct_reuse"></span>

<span data-ttu-id="a9af0-173"><span id="NETSETUP_NO_ACCT_REUSE"></span><span id="netsetup_no_acct_reuse"></span>**Netsetup \_ Nessun \_ \_ riuso Acct** (0x00020000)</span><span class="sxs-lookup"><span data-stu-id="a9af0-173"><span id="NETSETUP_NO_ACCT_REUSE"></span><span id="netsetup_no_acct_reuse"></span>**NETSETUP\_NO\_ACCT\_REUSE** (0x00020000)</span></span>


</dt> <dd>

<span data-ttu-id="a9af0-174">Quando si aggiunge il dominio, non riutilizzare un account esistente.</span><span class="sxs-lookup"><span data-stu-id="a9af0-174">When joining the domain, do not reuse an existing account.</span></span>

> [!Note]  
> <span data-ttu-id="a9af0-175">Questo flag è supportato in Windows 7, Windows Server 2008 R2 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="a9af0-175">This flag is supported on Windows 7, Windows Server 2008 R2, and later.</span></span>

 

</dd> <dt>

<span id="NETSETUP_IGNORE_UNSUPPORTED_FLAGS"></span><span id="netsetup_ignore_unsupported_flags"></span>

<span data-ttu-id="a9af0-176"><span id="NETSETUP_IGNORE_UNSUPPORTED_FLAGS"></span><span id="netsetup_ignore_unsupported_flags"></span>**Netsetup \_ Ignora \_ \_ flag non supportati** (0x10000000)</span><span class="sxs-lookup"><span data-stu-id="a9af0-176"><span id="NETSETUP_IGNORE_UNSUPPORTED_FLAGS"></span><span id="netsetup_ignore_unsupported_flags"></span>**NETSETUP\_IGNORE\_UNSUPPORTED\_FLAGS** (0x10000000)</span></span>


</dt> <dd>

<span data-ttu-id="a9af0-177">Se questo bit è impostato, i flag non riconosciuti verranno ignorati dalla funzione **JoinDomainOrWorkGroup** e [**NetJoinDomain**](/windows/desktop/api/lmjoin/nf-lmjoin-netjoindomain) si comporterà come se i flag non fossero impostati.</span><span class="sxs-lookup"><span data-stu-id="a9af0-177">If this bit is set, unrecognized flags will be ignored by the **JoinDomainOrWorkgroup** function and [**NetJoinDomain**](/windows/desktop/api/lmjoin/nf-lmjoin-netjoindomain) will behave as if the flags were not set.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a9af0-178">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a9af0-178">Return value</span></span>

<span data-ttu-id="a9af0-179">Restituisce un [codice di errore di sistema](/windows/desktop/Debug/system-error-codes), che può includere uno dei seguenti valori numerici.</span><span class="sxs-lookup"><span data-stu-id="a9af0-179">Returns a [system error code](/windows/desktop/Debug/system-error-codes), which may include one of the following numeric values.</span></span> <span data-ttu-id="a9af0-180">Qualsiasi altro numero indica un errore.</span><span class="sxs-lookup"><span data-stu-id="a9af0-180">Any other number indicates an error.</span></span> <span data-ttu-id="a9af0-181">Per ulteriori codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="a9af0-181">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span>

<dl> <dt>

<span data-ttu-id="a9af0-182">**Success**</span><span class="sxs-lookup"><span data-stu-id="a9af0-182">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="a9af0-183">0</span><span class="sxs-lookup"><span data-stu-id="a9af0-183">0</span></span>

</dd> <dt>

<span data-ttu-id="a9af0-184">**5**</span><span class="sxs-lookup"><span data-stu-id="a9af0-184">**5**</span></span>
</dt> <dd>

<span data-ttu-id="a9af0-185">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="a9af0-185">Access is denied.</span></span>

</dd> <dt>

<span data-ttu-id="a9af0-186">**87**</span><span class="sxs-lookup"><span data-stu-id="a9af0-186">**87**</span></span>
</dt> <dd>

<span data-ttu-id="a9af0-187">Parametro non corretto.</span><span class="sxs-lookup"><span data-stu-id="a9af0-187">The parameter is incorrect.</span></span>

</dd> <dt>

<span data-ttu-id="a9af0-188">**110**</span><span class="sxs-lookup"><span data-stu-id="a9af0-188">**110**</span></span>
</dt> <dd>

<span data-ttu-id="a9af0-189">il sistema non è in grado di aprire l'oggetto specificato.</span><span class="sxs-lookup"><span data-stu-id="a9af0-189">he system cannot open the specified object.</span></span>

</dd> <dt>

<span data-ttu-id="a9af0-190">**1323**</span><span class="sxs-lookup"><span data-stu-id="a9af0-190">**1323**</span></span>
</dt> <dd>

<span data-ttu-id="a9af0-191">Non è possibile aggiornare la password.</span><span class="sxs-lookup"><span data-stu-id="a9af0-191">Unable to update the password.</span></span>

</dd> <dt>

<span data-ttu-id="a9af0-192">**1326**</span><span class="sxs-lookup"><span data-stu-id="a9af0-192">**1326**</span></span>
</dt> <dd>

<span data-ttu-id="a9af0-193">Errore di accesso: nome utente sconosciuto o password errata.</span><span class="sxs-lookup"><span data-stu-id="a9af0-193">Logon failure: unknown username or bad password.</span></span>

</dd> <dt>

<span data-ttu-id="a9af0-194">**1355**</span><span class="sxs-lookup"><span data-stu-id="a9af0-194">**1355**</span></span>
</dt> <dd>

<span data-ttu-id="a9af0-195">Il dominio specificato non esiste o non è possibile contattarlo.</span><span class="sxs-lookup"><span data-stu-id="a9af0-195">The specified domain either does not exist or could not be contacted.</span></span>

</dd> <dt>

<span data-ttu-id="a9af0-196">**2224**</span><span class="sxs-lookup"><span data-stu-id="a9af0-196">**2224**</span></span>
</dt> <dd>

<span data-ttu-id="a9af0-197">L'account esiste già.</span><span class="sxs-lookup"><span data-stu-id="a9af0-197">The account already exists.</span></span>

</dd> <dt>

<span data-ttu-id="a9af0-198">**2691**</span><span class="sxs-lookup"><span data-stu-id="a9af0-198">**2691**</span></span>
</dt> <dd>

<span data-ttu-id="a9af0-199">Il computer è già aggiunto al dominio.</span><span class="sxs-lookup"><span data-stu-id="a9af0-199">The machine is already joined to the domain.</span></span>

</dd> <dt>

<span data-ttu-id="a9af0-200">**2692**</span><span class="sxs-lookup"><span data-stu-id="a9af0-200">**2692**</span></span>
</dt> <dd>

<span data-ttu-id="a9af0-201">Il computer non è attualmente aggiunto a un dominio.</span><span class="sxs-lookup"><span data-stu-id="a9af0-201">The machine is not currently joined to a domain.</span></span>

</dd> <dt>

<span data-ttu-id="a9af0-202">**\_ \_ connessione crittografata WBEM E \_ \_ necessaria**</span><span class="sxs-lookup"><span data-stu-id="a9af0-202">**WBEM\_E\_ENCRYPTED\_CONNECTION\_REQUIRED**</span></span>
</dt> <dd>

<span data-ttu-id="a9af0-203">0x80041087</span><span class="sxs-lookup"><span data-stu-id="a9af0-203">0x80041087</span></span>

<span data-ttu-id="a9af0-204">La *password* e il *nome utente* vengono specificati, ma il livello di autenticazione non è la **\_ \_ \_ \_ \_ privacy PKT a livello** di autenticazione di RPC C.</span><span class="sxs-lookup"><span data-stu-id="a9af0-204">*Password* and *UserName* are specified but the authentication level is not **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="a9af0-205">Per Visual Basic, viene restituito **wbemErrEncryptedConnectionRequired** .</span><span class="sxs-lookup"><span data-stu-id="a9af0-205">For Visual Basic, **wbemErrEncryptedConnectionRequired** is returned.</span></span>

</dd> <dt>

<span data-ttu-id="a9af0-206">**Altri**</span><span class="sxs-lookup"><span data-stu-id="a9af0-206">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="a9af0-207">1 4294967295</span><span class="sxs-lookup"><span data-stu-id="a9af0-207">1 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a9af0-208">Commenti</span><span class="sxs-lookup"><span data-stu-id="a9af0-208">Remarks</span></span>

<span data-ttu-id="a9af0-209">Quando si trasferisce un computer da un dominio a un gruppo di lavoro, è necessario rimuovere il computer dal dominio (con una chiamata a [**UnjoinDomainOrWorkgroup**](unjoindomainorworkgroup-method-in-class-win32-computersystem.md)) prima di chiamare questo metodo per aggiungere un gruppo di lavoro (con una chiamata a **JoinDomainOrWorkGroup**).</span><span class="sxs-lookup"><span data-stu-id="a9af0-209">When moving a computer from a domain to a workgroup, you must remove the computer from the domain (with a call to [**UnjoinDomainOrWorkgroup**](unjoindomainorworkgroup-method-in-class-win32-computersystem.md)) before calling this method to join a workgroup (with a call to **JoinDomainOrWorkgroup**).</span></span> <span data-ttu-id="a9af0-210">Dopo aver chiamato questo metodo, riavviare il computer interessato per applicare le modifiche.</span><span class="sxs-lookup"><span data-stu-id="a9af0-210">After calling this method, restart the affected computer to apply the changes.</span></span>

<span data-ttu-id="a9af0-211">Il *nome utente* e la *password* possono essere lasciati **null**.</span><span class="sxs-lookup"><span data-stu-id="a9af0-211">*UserName* and *Password* can be left **null**.</span></span> <span data-ttu-id="a9af0-212">Tuttavia, l'autenticazione della connessione a WMI deve essere 6 in script o **WbemAuthenticationLevelPktPrivacy** in Visual Basic e in altri linguaggi che possono usare la libreria [wbemdisp.dll](/windows/desktop/WmiSdk/using-the-wmi-scripting-type-library) .</span><span class="sxs-lookup"><span data-stu-id="a9af0-212">However, the authentication of the connection to WMI must be 6 in script or **WbemAuthenticationLevelPktPrivacy** in Visual Basic and other languages that can use the [wbemdisp.dll](/windows/desktop/WmiSdk/using-the-wmi-scripting-type-library) library.</span></span> <span data-ttu-id="a9af0-213">Per ulteriori informazioni, vedere [impostazione del livello di sicurezza del processo predefinito tramite VBScript](/windows/desktop/WmiSdk/setting-the-default-process-security-level-using-vbscript).</span><span class="sxs-lookup"><span data-stu-id="a9af0-213">For more information, see [Setting the Default Process Security Level Using VBScript](/windows/desktop/WmiSdk/setting-the-default-process-security-level-using-vbscript).</span></span>

<span data-ttu-id="a9af0-214">In C++, impostare l'autenticazione a **livello di autenticazione RPC \_ C \_ \_ \_ PKT \_ privacy** in [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity), per l'intero processo o in [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket)per una connessione al proxy [**IWbemServices**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices) .</span><span class="sxs-lookup"><span data-stu-id="a9af0-214">In C++, set the authentication at **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY** either in [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity), for the entire process, or in [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket), for a connection to the [**IWbemServices**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices) proxy.</span></span> <span data-ttu-id="a9af0-215">Per ulteriori informazioni, vedere [impostazione dell'autenticazione mediante C++](/windows/desktop/WmiSdk/setting-authentication-using-c-) e [impostazione della sicurezza su IWbemServices e altri proxy](/windows/desktop/WmiSdk/setting-the-security-on-iwbemservices-and-other-proxies).</span><span class="sxs-lookup"><span data-stu-id="a9af0-215">For more information, see [Setting Authentication Using C++](/windows/desktop/WmiSdk/setting-authentication-using-c-) and [Setting the Security on IWbemServices and Other Proxies](/windows/desktop/WmiSdk/setting-the-security-on-iwbemservices-and-other-proxies).</span></span>

## <a name="examples"></a><span data-ttu-id="a9af0-216">Esempio</span><span class="sxs-lookup"><span data-stu-id="a9af0-216">Examples</span></span>

<span data-ttu-id="a9af0-217">L'esempio [aggiungere un computer a un dominio di](https://Gallery.TechNet.Microsoft.Com/Join-a-computer-to-a-domain-6e19d905) PowerShell aggiunge un computer a un dominio.</span><span class="sxs-lookup"><span data-stu-id="a9af0-217">The [Join a computer to a domain](https://Gallery.TechNet.Microsoft.Com/Join-a-computer-to-a-domain-6e19d905) PowerShell example joins a computer to a domain.</span></span>

<span data-ttu-id="a9af0-218">Nell'esempio di codice VBScript seguente viene creato un join di un computer a un dominio e viene creato l'account del computer in Active Directory.</span><span class="sxs-lookup"><span data-stu-id="a9af0-218">The following VBScript code example joins a computer to a domain and creates the computer's account in Active Directory.</span></span>


```VB
Const JOIN_DOMAIN             = 1
Const ACCT_CREATE             = 2
Const ACCT_DELETE             = 4
Const WIN9X_UPGRADE           = 16
Const DOMAIN_JOIN_IF_JOINED   = 32
Const JOIN_UNSECURE           = 64
Const MACHINE_PASSWORD_PASSED = 128
Const DEFERRED_SPN_SET        = 256
Const INSTALL_INVOCATION      = 262144
strDomain   = "FABRIKAM"
strPassword = "ls4k5ywA"
strUser     = "shenalan"
Set objNetwork = CreateObject("WScript.Network")
strComputer = objNetwork.ComputerName
Set objComputer = GetObject("winmgmts:{impersonationLevel=Impersonate}!\\" & strComputer & _
                            "\root\cimv2:Win32_ComputerSystem.Name='" & strComputer & "'")
ReturnValue = objComputer.JoinDomainOrWorkGroup(strDomain, _
                                                strPassword, _
                                                strDomain & "\" & strUser, _
                                                NULL, _
                                                JOIN_DOMAIN + ACCT_CREATE)
```



## <a name="requirements"></a><span data-ttu-id="a9af0-219">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a9af0-219">Requirements</span></span>



| <span data-ttu-id="a9af0-220">Requisito</span><span class="sxs-lookup"><span data-stu-id="a9af0-220">Requirement</span></span> | <span data-ttu-id="a9af0-221">Valore</span><span class="sxs-lookup"><span data-stu-id="a9af0-221">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a9af0-222">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a9af0-222">Minimum supported client</span></span><br/> | <span data-ttu-id="a9af0-223">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a9af0-223">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a9af0-224">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a9af0-224">Minimum supported server</span></span><br/> | <span data-ttu-id="a9af0-225">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a9af0-225">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a9af0-226">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="a9af0-226">Namespace</span></span><br/>                | <span data-ttu-id="a9af0-227">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="a9af0-227">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a9af0-228">MOF</span><span class="sxs-lookup"><span data-stu-id="a9af0-228">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a9af0-229"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a9af0-229"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a9af0-230">DLL</span><span class="sxs-lookup"><span data-stu-id="a9af0-230">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a9af0-231"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a9af0-231"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9af0-232">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a9af0-232">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9af0-233">**\_ComputerSystem Win32**</span><span class="sxs-lookup"><span data-stu-id="a9af0-233">**Win32\_ComputerSystem**</span></span>](win32-computersystem.md)
</dt> <dt>

[<span data-ttu-id="a9af0-234">**Metodo UnjoinDomainOrWorkgroup**</span><span class="sxs-lookup"><span data-stu-id="a9af0-234">**UnjoinDomainOrWorkgroup method**</span></span>](unjoindomainorworkgroup-method-in-class-win32-computersystem.md)
</dt> </dl>

 

