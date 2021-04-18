---
description: Si connette allo spazio dei nomi nel computer specificato nel parametro strServer.
ms.assetid: 31364c68-b031-4cf0-851f-b4e302f077e0
ms.tgt_platform: multiple
title: Metodo SWbemLocator. ConnectServer (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemLocator.ConnectServer
- ISWbemLocator.ConnectServer
- ISWbemLocator.ConnectServer
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 31c2e6de8cf1504543727cad056a3616a51182d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318175"
---
# <a name="swbemlocatorconnectserver-method"></a><span data-ttu-id="fe2a6-103">SWbemLocator. ConnectServer, metodo</span><span class="sxs-lookup"><span data-stu-id="fe2a6-103">SWbemLocator.ConnectServer method</span></span>

<span data-ttu-id="fe2a6-104">Il metodo **ConnectServer** dell'oggetto [**SWbemLocator**](swbemlocator.md) si connette allo spazio dei nomi nel computer specificato nel parametro *strServer* .</span><span class="sxs-lookup"><span data-stu-id="fe2a6-104">The **ConnectServer** method of the [**SWbemLocator**](swbemlocator.md) object connects to the namespace on the computer that is specified in the *strServer* parameter.</span></span> <span data-ttu-id="fe2a6-105">Il computer di destinazione può essere locale o remoto, ma deve essere installato WMI.</span><span class="sxs-lookup"><span data-stu-id="fe2a6-105">The target computer can be either local or remote, but it must have WMI installed.</span></span> <span data-ttu-id="fe2a6-106">Per esempi e un confronto con il tipo di connessione del moniker, vedere [creazione di uno script WMI](creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="fe2a6-106">For examples and a comparison with the moniker type of connection, see [Creating a WMI Script](creating-a-wmi-script.md).</span></span>

<span data-ttu-id="fe2a6-107">A partire da Windows Vista, **SWbemLocator. ConnectServer** è in grado di connettersi ai computer che eseguono IPv6 utilizzando un indirizzo IPv6 nel parametro *strServer* .</span><span class="sxs-lookup"><span data-stu-id="fe2a6-107">Starting with Windows Vista, **SWbemLocator.ConnectServer** can connect with computers running IPv6 using an IPv6 address in the *strServer* parameter.</span></span> <span data-ttu-id="fe2a6-108">Per ulteriori informazioni, vedere [supporto di IPv6 e IPv4 in WMI](ipv6-and-ipv4-support-in-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="fe2a6-108">For more information, see [IPv6 and IPv4 Support in WMI](ipv6-and-ipv4-support-in-wmi.md).</span></span>

<span data-ttu-id="fe2a6-109">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="fe2a6-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="fe2a6-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fe2a6-110">Syntax</span></span>


```VB
objwbemServices = .ConnectServer( _
  [ ByVal strServer ], _
  [ ByVal strNamespace ], _
  [ ByVal strUser ], _
  [ ByVal strPassword ], _
  [ ByVal strLocale ], _
  [ ByVal strAuthority ], _
  [ ByVal iSecurityFlags ], _
  [ ByVal objwbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="fe2a6-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="fe2a6-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe2a6-112">*strServer* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="fe2a6-112">*strServer* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="fe2a6-113">Nome del computer a cui ci si connette.</span><span class="sxs-lookup"><span data-stu-id="fe2a6-113">Computer name to which you are connecting.</span></span> <span data-ttu-id="fe2a6-114">Se il computer remoto si trova in un dominio diverso rispetto all'account utente con cui si esegue l'accesso, utilizzare il nome completo del computer.</span><span class="sxs-lookup"><span data-stu-id="fe2a6-114">If the remote computer is in a different domain than the user account under which you log in, then use the fully qualified computer name.</span></span> <span data-ttu-id="fe2a6-115">Se non si specifica questo parametro, la chiamata viene eseguita per impostazione predefinita sul computer locale.</span><span class="sxs-lookup"><span data-stu-id="fe2a6-115">If you do not provide this parameter, the call defaults to the local computer.</span></span>

<span data-ttu-id="fe2a6-116">Esempio: `server1.network.fabrikam`</span><span class="sxs-lookup"><span data-stu-id="fe2a6-116">Example: `server1.network.fabrikam`</span></span>

<span data-ttu-id="fe2a6-117">È anche possibile usare un indirizzo IP in questo parametro.</span><span class="sxs-lookup"><span data-stu-id="fe2a6-117">You also can use an IP address in this parameter.</span></span> <span data-ttu-id="fe2a6-118">Se l'indirizzo IP è in formato IPv6, il computer di destinazione deve eseguire IPv6.</span><span class="sxs-lookup"><span data-stu-id="fe2a6-118">If the IP address is in IPv6 format, the target computer must be running IPv6.</span></span> <span data-ttu-id="fe2a6-119">Un indirizzo in IPv4 appare come `123.123.123.123`</span><span class="sxs-lookup"><span data-stu-id="fe2a6-119">An address in IPv4 looks like `123.123.123.123`</span></span>

<span data-ttu-id="fe2a6-120">Un indirizzo IP in formato IPv6 ha un aspetto simile al `2010:836B:4179::836B:4179`</span><span class="sxs-lookup"><span data-stu-id="fe2a6-120">An IP address in IPv6 format looks like `2010:836B:4179::836B:4179`</span></span>

<span data-ttu-id="fe2a6-121">Per ulteriori informazioni su DNS e IPv4, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="fe2a6-121">For more information on DNS and IPv4, see the Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="fe2a6-122">*strNameSpace* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="fe2a6-122">*strNamespace* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="fe2a6-123">Stringa che specifica lo spazio dei nomi a cui si accede.</span><span class="sxs-lookup"><span data-stu-id="fe2a6-123">String that specifies the namespace to which you log on.</span></span> <span data-ttu-id="fe2a6-124">Per accedere allo \\ spazio dei nomi predefinito radice, ad esempio, usare il \\ valore predefinito radice.</span><span class="sxs-lookup"><span data-stu-id="fe2a6-124">For example, to log on to the root\\default namespace, use root\\default.</span></span> <span data-ttu-id="fe2a6-125">Se non si specifica questo parametro, per impostazione predefinita viene utilizzato lo spazio dei nomi configurato come spazio dei nomi predefinito per lo scripting.</span><span class="sxs-lookup"><span data-stu-id="fe2a6-125">If you do not specify this parameter, it defaults to the namespace that is configured as the default namespace for scripting.</span></span> <span data-ttu-id="fe2a6-126">Per ulteriori informazioni, vedere [creazione di un'applicazione o di uno script WMI](creating-a-wmi-application-or-script.md).</span><span class="sxs-lookup"><span data-stu-id="fe2a6-126">For more information, see [Creating a WMI Application or Script](creating-a-wmi-application-or-script.md).</span></span>

<span data-ttu-id="fe2a6-127">Esempio: "root \\ cimv2"</span><span class="sxs-lookup"><span data-stu-id="fe2a6-127">Example: "root\\CIMV2"</span></span>

</dd> <dt>

<span data-ttu-id="fe2a6-128">*strUser* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="fe2a6-128">*strUser* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="fe2a6-129">Nome utente da utilizzare per la connessione.</span><span class="sxs-lookup"><span data-stu-id="fe2a6-129">User name to use to connect.</span></span> <span data-ttu-id="fe2a6-130">Il formato della stringa può essere un nome utente o un nome utente di dominio \\ .</span><span class="sxs-lookup"><span data-stu-id="fe2a6-130">The string can be in the form of either a user name or a Domain\\Username.</span></span> <span data-ttu-id="fe2a6-131">Lasciare vuoto questo parametro per usare il contesto di sicurezza corrente.</span><span class="sxs-lookup"><span data-stu-id="fe2a6-131">Leave this parameter blank to use the current security context.</span></span> <span data-ttu-id="fe2a6-132">Il parametro *strUser* deve essere utilizzato solo con connessioni a server WMI remoti.</span><span class="sxs-lookup"><span data-stu-id="fe2a6-132">The *strUser* parameter should only be used with connections to remote WMI servers.</span></span> <span data-ttu-id="fe2a6-133">Se si tenta di specificare *strUser* per una connessione WMI locale, il tentativo di connessione non riesce.</span><span class="sxs-lookup"><span data-stu-id="fe2a6-133">If you attempt to specify *strUser* for a local WMI connection, the connection attempt fails.</span></span> <span data-ttu-id="fe2a6-134">Se l'autenticazione Kerberos è in uso, non è possibile intercettare il nome utente e la password specificati in *strUser* e *strPassword* in una rete.</span><span class="sxs-lookup"><span data-stu-id="fe2a6-134">If Kerberos authentication is in use, then the username and password that is specified in *strUser* and *strPassword* cannot be intercepted on a network.</span></span> <span data-ttu-id="fe2a6-135">È possibile usare il formato UPN per specificare il *strUser*.</span><span class="sxs-lookup"><span data-stu-id="fe2a6-135">You can use the UPN format to specify the *strUser*.</span></span>

<span data-ttu-id="fe2a6-136">Esempio: "DomainName \\ username"</span><span class="sxs-lookup"><span data-stu-id="fe2a6-136">Example: "DomainName\\UserName"</span></span>

> [!Note]  
> <span data-ttu-id="fe2a6-137">Se un dominio viene specificato in *strAuthority*, non è necessario specificare il dominio in questo punto.</span><span class="sxs-lookup"><span data-stu-id="fe2a6-137">If a domain is specified in *strAuthority*, then the domain must not be specified here.</span></span> <span data-ttu-id="fe2a6-138">Se si specifica il dominio in entrambi i parametri, si verifica un errore di parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="fe2a6-138">Specifying the domain in both parameters results in an Invalid Parameter error.</span></span>

 

</dd> <dt>

<span data-ttu-id="fe2a6-139">*strPassword* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="fe2a6-139">*strPassword* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="fe2a6-140">Stringa che specifica la password da utilizzare durante il tentativo di connessione.</span><span class="sxs-lookup"><span data-stu-id="fe2a6-140">String that specifies the password to use when attempting to connect.</span></span> <span data-ttu-id="fe2a6-141">Lasciare vuoto il parametro per usare il contesto di sicurezza corrente.</span><span class="sxs-lookup"><span data-stu-id="fe2a6-141">Leave the parameter blank to use the current security context.</span></span> <span data-ttu-id="fe2a6-142">Il parametro *strPassword* deve essere utilizzato solo con connessioni a server WMI remoti.</span><span class="sxs-lookup"><span data-stu-id="fe2a6-142">The *strPassword* parameter should only be used with connections to remote WMI servers.</span></span> <span data-ttu-id="fe2a6-143">Se si tenta di specificare *strPassword* per una connessione WMI locale, il tentativo di connessione non riesce.</span><span class="sxs-lookup"><span data-stu-id="fe2a6-143">If you attempt to specify *strPassword* for a local WMI connection, the connection attempt fails.</span></span> <span data-ttu-id="fe2a6-144">Se è in uso l'autenticazione Kerberos, il nome utente e la password specificati in *strUser* e *strPassword* non possono essere intercettati sulla rete.</span><span class="sxs-lookup"><span data-stu-id="fe2a6-144">If Kerberos authentication is in use then the username and password that is specified in *strUser* and *strPassword* cannot be intercepted on the network.</span></span>

</dd> <dt>

<span data-ttu-id="fe2a6-145">*strLocale* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="fe2a6-145">*strLocale* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="fe2a6-146">Stringa che specifica il codice di localizzazione.</span><span class="sxs-lookup"><span data-stu-id="fe2a6-146">String that specifies the localization code.</span></span> <span data-ttu-id="fe2a6-147">Se si desidera utilizzare le impostazioni locali correnti, lasciarlo vuoto.</span><span class="sxs-lookup"><span data-stu-id="fe2a6-147">If you want to use the current locale, leave it blank.</span></span> <span data-ttu-id="fe2a6-148">Se non è vuoto, questo parametro deve essere una stringa che indica le impostazioni locali desiderate in cui devono essere recuperate le informazioni.</span><span class="sxs-lookup"><span data-stu-id="fe2a6-148">If not blank, this parameter must be a string that indicates the desired locale where information must be retrieved.</span></span> <span data-ttu-id="fe2a6-149">Per gli identificatori delle impostazioni locali Microsoft, il formato della stringa è "MS \_ xxxx", dove xxxx è una stringa nel formato esadecimale che indica il valore LCID.</span><span class="sxs-lookup"><span data-stu-id="fe2a6-149">For Microsoft locale identifiers, the format of the string is "MS\_xxxx", where xxxx is a string in the hexadecimal form that indicates the LCID.</span></span> <span data-ttu-id="fe2a6-150">Ad esempio, l'inglese americano verrebbe visualizzato come "MS \_ 409".</span><span class="sxs-lookup"><span data-stu-id="fe2a6-150">For example, American English would appear as "MS\_409".</span></span>

</dd> <dt>

<span data-ttu-id="fe2a6-151">*strAuthority* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="fe2a6-151">*strAuthority* \[in, optional\]</span></span>
</dt> <dd>

<dt>

<span data-ttu-id="fe2a6-152">""</span><span class="sxs-lookup"><span data-stu-id="fe2a6-152">""</span></span>
</dt> <dd>

<span data-ttu-id="fe2a6-153">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="fe2a6-153">This parameter is optional.</span></span> <span data-ttu-id="fe2a6-154">Tuttavia, se è specificato, è possibile usare solo Kerberos o NTLMDomain.</span><span class="sxs-lookup"><span data-stu-id="fe2a6-154">However, if it is specified, only Kerberos or NTLMDomain can be used.</span></span>

</dd> <dt>

<span data-ttu-id="fe2a6-155">Kerberos</span><span class="sxs-lookup"><span data-stu-id="fe2a6-155">Kerberos:</span></span>
</dt> <dd>

<span data-ttu-id="fe2a6-156">Se il parametro *strAuthority* inizia con la stringa "Kerberos:", viene utilizzata l'autenticazione Kerberos e questo parametro deve contenere un nome entità Kerberos.</span><span class="sxs-lookup"><span data-stu-id="fe2a6-156">If the *strAuthority* parameter begins with the string "Kerberos:", then Kerberos authentication is used and this parameter should contain a Kerberos principal name.</span></span> <span data-ttu-id="fe2a6-157">Il nome dell'entità Kerberos viene specificato come Kerberos:*dominio*, ad esempio `Kerberos:fabrikam` dove `fabrikam` è il server a cui si sta tentando di connettersi.</span><span class="sxs-lookup"><span data-stu-id="fe2a6-157">The Kerberos principal name is specified as Kerberos:*domain*, such as `Kerberos:fabrikam` where `fabrikam` is the server to which you are attempting to connect.</span></span>

<span data-ttu-id="fe2a6-158">Esempio: "Kerberos: DOMAIN"</span><span class="sxs-lookup"><span data-stu-id="fe2a6-158">Example: "Kerberos:DOMAIN"</span></span>

</dd> <dt>

<span data-ttu-id="fe2a6-159">NTLMDomain</span><span class="sxs-lookup"><span data-stu-id="fe2a6-159">NTLMDomain:</span></span>
</dt> <dd>

<span data-ttu-id="fe2a6-160">Per utilizzare l'autenticazione NT LAN Manager (NTLM), è necessario specificarla come NTLMDomain:*Domain*, ad esempio `NTLMDomain:fabrikam` Where `fabrikam` è il nome del dominio.</span><span class="sxs-lookup"><span data-stu-id="fe2a6-160">To use NT Lan Manager (NTLM) authentication, you must specify it as NTLMDomain:*domain*, such as `NTLMDomain:fabrikam` where `fabrikam` is the name of the domain.</span></span>

<span data-ttu-id="fe2a6-161">Esempio: "NTLMDomain: DOMAIN"</span><span class="sxs-lookup"><span data-stu-id="fe2a6-161">Example: "NTLMDomain:DOMAIN"</span></span>

</dd> </dl>

<span data-ttu-id="fe2a6-162">Se si lascia vuoto questo parametro, il sistema operativo negozia con COM per determinare se viene utilizzata l'autenticazione NTLM o Kerberos.</span><span class="sxs-lookup"><span data-stu-id="fe2a6-162">If you leave this parameter blank, the operating system negotiates with COM to determine whether NTLM or Kerberos authentication is used.</span></span> <span data-ttu-id="fe2a6-163">Questo parametro deve essere utilizzato solo con connessioni a server WMI remoti.</span><span class="sxs-lookup"><span data-stu-id="fe2a6-163">This parameter should only be used with connections to remote WMI servers.</span></span> <span data-ttu-id="fe2a6-164">Se si tenta di impostare l'autorità per una connessione WMI locale, il tentativo di connessione non riesce.</span><span class="sxs-lookup"><span data-stu-id="fe2a6-164">If you attempt to set the authority for a local WMI connection, the connection attempt fails.</span></span>

> [!Note]  
> <span data-ttu-id="fe2a6-165">Se il dominio è specificato in *strUser*, che è il percorso preferito, questo non deve essere specificato in questo punto.</span><span class="sxs-lookup"><span data-stu-id="fe2a6-165">If the domain is specified in *strUser*, which is the preferred location, then it must not be specified here.</span></span> <span data-ttu-id="fe2a6-166">Se si specifica il dominio in entrambi i parametri, si verifica un errore di parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="fe2a6-166">Specifying the domain in both parameters results in an Invalid Parameter error.</span></span>

 

</dd> <dt>

<span data-ttu-id="fe2a6-167">*iSecurityFlags* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="fe2a6-167">*iSecurityFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="fe2a6-168">Utilizzato per passare i valori del flag a **ConnectServer**.</span><span class="sxs-lookup"><span data-stu-id="fe2a6-168">Used to pass flag values to **ConnectServer**.</span></span>

<dt>

<span data-ttu-id="fe2a6-169">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="fe2a6-169">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="fe2a6-170">Il valore 0 per questo parametro determina la restituzione della chiamata a **ConnectServer** solo dopo che è stata stabilita la connessione al server.</span><span class="sxs-lookup"><span data-stu-id="fe2a6-170">A value of 0 for this parameter causes the call to **ConnectServer** to return only after the connection to the server is established.</span></span> <span data-ttu-id="fe2a6-171">Questo potrebbe causare un arresto illimitato del programma se non è possibile stabilire la connessione.</span><span class="sxs-lookup"><span data-stu-id="fe2a6-171">This could cause your program to stop responding indefinitely if the connection cannot be established.</span></span>

</dd> <dt>

<span id="wbemConnectFlagUseMaxWait"></span><span id="wbemconnectflagusemaxwait"></span><span id="WBEMCONNECTFLAGUSEMAXWAIT"></span>

<span data-ttu-id="fe2a6-172"><span id="wbemConnectFlagUseMaxWait"></span><span id="wbemconnectflagusemaxwait"></span><span id="WBEMCONNECTFLAGUSEMAXWAIT"></span>wbemConnectFlagUseMaxWait \* \* \* \* (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="fe2a6-172"><span id="wbemConnectFlagUseMaxWait"></span><span id="wbemconnectflagusemaxwait"></span><span id="WBEMCONNECTFLAGUSEMAXWAIT"></span>\*\*\*\*wbemConnectFlagUseMaxWait\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="fe2a6-173">La chiamata di **ConnectServer** è garantita la restituzione in 2 minuti o meno.</span><span class="sxs-lookup"><span data-stu-id="fe2a6-173">The **ConnectServer** call is guaranteed to return in 2 minutes or less.</span></span> <span data-ttu-id="fe2a6-174">Utilizzare questo flag per impedire che il programma cessi di rispondere a tempo indefinito se non è possibile stabilire la connessione.</span><span class="sxs-lookup"><span data-stu-id="fe2a6-174">Use this flag to prevent your program from ceasing to respond indefinitely if the connection cannot be established.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="fe2a6-175">*objwbemNamedValueSet* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="fe2a6-175">*objwbemNamedValueSet* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="fe2a6-176">In genere, non è definito.</span><span class="sxs-lookup"><span data-stu-id="fe2a6-176">Typically, this is undefined.</span></span> <span data-ttu-id="fe2a6-177">In caso contrario, si tratta di un oggetto [**SWbemNamedValueSet**](swbemnamedvalueset.md) i cui elementi rappresentano le informazioni sul contesto che possono essere utilizzate dal provider che sta servendo la richiesta.</span><span class="sxs-lookup"><span data-stu-id="fe2a6-177">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="fe2a6-178">Un provider che supporta o richiede tali informazioni deve documentare i nomi dei valori riconosciuti, il tipo di dati del valore, i valori consentiti e la semantica.</span><span class="sxs-lookup"><span data-stu-id="fe2a6-178">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe2a6-179">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fe2a6-179">Return value</span></span>

<span data-ttu-id="fe2a6-180">In caso di esito positivo, WMI restituisce un oggetto [**SWbemServices**](swbemservices.md) associato allo spazio dei nomi specificato in *strNameSpace* nel computer specificato in *strServer*.</span><span class="sxs-lookup"><span data-stu-id="fe2a6-180">If successful, WMI returns an [**SWbemServices**](swbemservices.md) object that is bound to the namespace that is specified in *strNamespace* on the computer that is specified in *strServer*.</span></span>

## <a name="error-codes"></a><span data-ttu-id="fe2a6-181">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="fe2a6-181">Error codes</span></span>

<span data-ttu-id="fe2a6-182">Dopo il completamento del metodo **ConnectServer** , l'oggetto [Err](/previous-versions//sbf5ze0e(v=vs.85)) può contenere uno dei codici di errore elencati di seguito.</span><span class="sxs-lookup"><span data-stu-id="fe2a6-182">After the completion of the **ConnectServer** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="fe2a6-183">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="fe2a6-183">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="fe2a6-184">Il nome utente o la password corrente o specificata non sono validi o sono autorizzati a eseguire la connessione.</span><span class="sxs-lookup"><span data-stu-id="fe2a6-184">The current or specified user name and password were not valid or authorized to make the connection.</span></span>

</dd> <dt>

<span data-ttu-id="fe2a6-185">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="fe2a6-185">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="fe2a6-186">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="fe2a6-186">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="fe2a6-187">**wbemErrInvalidNamespace** -2147749902 (0x8004100E)</span><span class="sxs-lookup"><span data-stu-id="fe2a6-187">**wbemErrInvalidNamespace** - 2147749902 (0x8004100E)</span></span>
</dt> <dd>

<span data-ttu-id="fe2a6-188">Lo spazio dei nomi specificato non esiste nel server.</span><span class="sxs-lookup"><span data-stu-id="fe2a6-188">The specified namespace did not exist on the server.</span></span>

</dd> <dt>

<span data-ttu-id="fe2a6-189">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="fe2a6-189">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="fe2a6-190">È stato specificato un parametro non valido o non è stato possibile analizzare lo spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="fe2a6-190">An invalid parameter was specified, or the namespace could not be parsed.</span></span>

</dd> <dt>

<span data-ttu-id="fe2a6-191">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="fe2a6-191">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="fe2a6-192">Memoria insufficiente per completare l'operazione.</span><span class="sxs-lookup"><span data-stu-id="fe2a6-192">Not enough memory to complete the operation.</span></span>

</dd> <dt>

<span data-ttu-id="fe2a6-193">**wbemErrTransportFailure** -2147749909</span><span class="sxs-lookup"><span data-stu-id="fe2a6-193">**wbemErrTransportFailure** - 2147749909</span></span>
</dt> <dd>

<span data-ttu-id="fe2a6-194">Si è verificato un errore di rete che impedisce il normale funzionamento.</span><span class="sxs-lookup"><span data-stu-id="fe2a6-194">A networking error occurred, preventing normal operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fe2a6-195">Commenti</span><span class="sxs-lookup"><span data-stu-id="fe2a6-195">Remarks</span></span>

<span data-ttu-id="fe2a6-196">Il metodo **ConnectServer** viene spesso usato per la connessione a un account con credenziali di nome utente e password diverse in un computer remoto perché non è possibile specificare una password diversa in una stringa del [moniker](constructing-a-moniker-string.md) .</span><span class="sxs-lookup"><span data-stu-id="fe2a6-196">The **ConnectServer** method is often used when connecting to an account with a different username and password credentials on a remote computer because you cannot specify a different password in a [moniker](constructing-a-moniker-string.md) string.</span></span> <span data-ttu-id="fe2a6-197">Per ulteriori informazioni, vedere [connessione a WMI in un computer remoto](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="fe2a6-197">For more information, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>

<span data-ttu-id="fe2a6-198">L'utilizzo di un indirizzo IPv4 per connettersi a un server remoto può causare un comportamento imprevisto.</span><span class="sxs-lookup"><span data-stu-id="fe2a6-198">Using an IPv4 address to connect to a remote server may result in unexpected behavior.</span></span> <span data-ttu-id="fe2a6-199">La causa probabile sono le voci DNS non aggiornate nell'ambiente in uso.</span><span class="sxs-lookup"><span data-stu-id="fe2a6-199">The likely cause is stale DNS entries in your environment.</span></span> <span data-ttu-id="fe2a6-200">In questi casi, verrà usata la voce PTR non aggiornata per il computer, con risultati imprevedibili.</span><span class="sxs-lookup"><span data-stu-id="fe2a6-200">In these circumstances, the stale PTR entry for the machine will be used, with unpredictable results.</span></span> <span data-ttu-id="fe2a6-201">Per evitare questo comportamento, è possibile aggiungere un punto (".") all'indirizzo IP prima di chiamare ConnectServer.</span><span class="sxs-lookup"><span data-stu-id="fe2a6-201">To avoid this behavior, you can append a period (".") to the IP address before calling ConnectServer.</span></span> <span data-ttu-id="fe2a6-202">In questo modo, la ricerca DNS inversa avrà esito negativo, ma potrebbe consentire la riuscita della chiamata **ConnectServer** nel computer corretto.</span><span class="sxs-lookup"><span data-stu-id="fe2a6-202">This causes the reverse DNS lookup to fail, but may allow the **ConnectServer** call to succeed on the correct machine.</span></span>

## <a name="examples"></a><span data-ttu-id="fe2a6-203">Esempio</span><span class="sxs-lookup"><span data-stu-id="fe2a6-203">Examples</span></span>

<span data-ttu-id="fe2a6-204">Nell'esempio di codice VBScript seguente viene descritto come connettersi a un computer remoto per ottenere i dati [**\_ IP4RouteTable Win32**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetable) .</span><span class="sxs-lookup"><span data-stu-id="fe2a6-204">The following VBScript code example describes how to connect to a remote computer to obtain [**Win32\_IP4RouteTable**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetable) data.</span></span> <span data-ttu-id="fe2a6-205">Il nome di dominio specificato in *strDomain* viene usato in *strAuthority*.</span><span class="sxs-lookup"><span data-stu-id="fe2a6-205">The domain name that is specified in *strDomain* is used in *strAuthority*.</span></span>


```VB
Const intMin = 3600
strComputer = "RemoteComputer" 
strDomain = "DomainName"  
Wscript.StdOut.Write "Please enter your user name:"
strUser = Wscript.StdIn.ReadLine 
Set objPassword = CreateObject("ScriptPW.Password")
Wscript.StdOut.Write "Please enter your password:"
strPassword = objPassword.GetPassword()
Wscript.Echo

Set objSWbemLocator = CreateObject("WbemScripting.SWbemLocator") 
Set objWMIService = objSWbemLocator.ConnectServer(strComputer, _ 
                                                  "root\CIMV2", _ 
                                                  strUser, _ 
                                                  strPassword, _ 
                                                  "MS_409", _ 
                                                  "NTLMDomain:" + strDomain) 
Set colItems = objWMIService.ExecQuery("SELECT * FROM Win32_IP4RouteTable",,48) 
For Each objItem in colItems
    WScript.Echo "Age in Minutes: " & int(objItem.Age/intMin) & VBNewLine _
               & "Description:    " & objItem.Description & VBNewLine _
               & "Destination:    " & objItem.Destination & VBNewLine _
               & "InterfaceIndex: " & objItem.InterfaceIndex & VBNewLine _
               & "Mask:           " & objItem.Mask & VBNewLine _
               & "Metric1:        " & objItem.Metric1 & VBNewLine _
               & "Metric2:        " & objItem.Metric2 & VBNewLine _
               & "Metric3:        " & objItem.Metric3 & VBNewLine _
               & "Metric4:        " & objItem.Metric4 & VBNewLine _
               & "Metric5:        " & objItem.Metric5 & VBNewLine _
               & "Name:           " & objItem.Name & VBNewLine _
               & "NextHop:        " & objItem.NextHop & VBNewLine _
               & "Protocol:       " & objItem.Protocol & VBNewLine _
               & "Type: " & objItem.Type
    WScript.Echo
   </example>
Next
```



<span data-ttu-id="fe2a6-206">Il seguente frammento di codice di PowerShell accede a un server remoto ed elenca le classi WMI disponibili.</span><span class="sxs-lookup"><span data-stu-id="fe2a6-206">The following PowerShell snippet access a remote server and lists the available WMI classes.</span></span>


```PowerShell
$NameSpace = 'root\ccm'
$ComputerName = 'sccm.company.com'
$WbemLocator = New-Object -ComObject "WbemScripting.SWbemLocator"
$WbemServices = $WbemLocator.ConnectServer($ComputerName, $Namespace)
$WbemClasses = $WbemServices.SubclassesOf()
$WbemClasses
```



## <a name="requirements"></a><span data-ttu-id="fe2a6-207">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fe2a6-207">Requirements</span></span>



| <span data-ttu-id="fe2a6-208">Requisito</span><span class="sxs-lookup"><span data-stu-id="fe2a6-208">Requirement</span></span> | <span data-ttu-id="fe2a6-209">Valore</span><span class="sxs-lookup"><span data-stu-id="fe2a6-209">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fe2a6-210">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fe2a6-210">Minimum supported client</span></span><br/> | <span data-ttu-id="fe2a6-211">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fe2a6-211">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="fe2a6-212">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fe2a6-212">Minimum supported server</span></span><br/> | <span data-ttu-id="fe2a6-213">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fe2a6-213">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="fe2a6-214">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fe2a6-214">Header</span></span><br/>                   | <dl> <span data-ttu-id="fe2a6-215"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="fe2a6-215"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="fe2a6-216">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="fe2a6-216">Type library</span></span><br/>             | <dl> <span data-ttu-id="fe2a6-217"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="fe2a6-217"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="fe2a6-218">DLL</span><span class="sxs-lookup"><span data-stu-id="fe2a6-218">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fe2a6-219"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fe2a6-219"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="fe2a6-220">CLSID</span><span class="sxs-lookup"><span data-stu-id="fe2a6-220">CLSID</span></span><br/>                    | <span data-ttu-id="fe2a6-221">\_SWBEMLOCATOR CLSID</span><span class="sxs-lookup"><span data-stu-id="fe2a6-221">CLSID\_SWbemLocator</span></span><br/>                                                          |
| <span data-ttu-id="fe2a6-222">IID</span><span class="sxs-lookup"><span data-stu-id="fe2a6-222">IID</span></span><br/>                      | <span data-ttu-id="fe2a6-223">\_ISWBEMLOCATOR IID</span><span class="sxs-lookup"><span data-stu-id="fe2a6-223">IID\_ISWbemLocator</span></span><br/>                                                           |



## <a name="see-also"></a><span data-ttu-id="fe2a6-224">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fe2a6-224">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe2a6-225">**SWbemLocator**</span><span class="sxs-lookup"><span data-stu-id="fe2a6-225">**SWbemLocator**</span></span>](swbemlocator.md)
</dt> <dt>

[<span data-ttu-id="fe2a6-226">**SWbemServices**</span><span class="sxs-lookup"><span data-stu-id="fe2a6-226">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="fe2a6-227">Connessione a WMI in un computer remoto</span><span class="sxs-lookup"><span data-stu-id="fe2a6-227">Connecting to WMI on a Remote Computer</span></span>](connecting-to-wmi-on-a-remote-computer.md)
</dt> <dt>

[<span data-ttu-id="fe2a6-228">Creazione di uno script WMI</span><span class="sxs-lookup"><span data-stu-id="fe2a6-228">Creating a WMI Script</span></span>](creating-a-wmi-script.md)
</dt> </dl>

 

