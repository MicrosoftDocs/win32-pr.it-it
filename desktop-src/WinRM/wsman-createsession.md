---
title: Metodo WSMan. CreateSession (WSManDisp. h)
description: Crea un oggetto sessione che può quindi essere utilizzato per le operazioni di rete successive.
ms.assetid: 299d9a95-bd30-414c-996d-6633e8b7ce52
ms.tgt_platform: multiple
keywords:
- Gestione remota Windows del metodo CreateSession
- Metodo CreateSession Gestione remota Windows, oggetto WSMan
- Gestione remota Windows oggetto WSMan, metodo CreateSession
topic_type:
- apiref
api_name:
- WSMan.CreateSession
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 966fd1f43db7114d3a4c0cf4cddaa4428fcb41c6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518142"
---
# <a name="wsmancreatesession-method"></a><span data-ttu-id="4d63a-106">WSMan. CreateSession, metodo</span><span class="sxs-lookup"><span data-stu-id="4d63a-106">WSMan.CreateSession method</span></span>

<span data-ttu-id="4d63a-107">Crea un oggetto [**sessione**](session.md) che può quindi essere utilizzato per le operazioni di rete successive.</span><span class="sxs-lookup"><span data-stu-id="4d63a-107">Creates a [**Session**](session.md) object that can then be used for subsequent network operations.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d63a-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4d63a-108">Syntax</span></span>


```VB
WSMan.CreateSession( _
  [ ByVal connection ], _
  [ ByVal flags ], _
  [ ByVal connectionOptions ] _
)
```



## <a name="parameters"></a><span data-ttu-id="4d63a-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="4d63a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d63a-110">*connessione* \[ a in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="4d63a-110">*connection* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4d63a-111">Protocollo e servizio a cui connettersi, incluso IPv4 o IPv6.</span><span class="sxs-lookup"><span data-stu-id="4d63a-111">The protocol and service to connect to, including either IPv4 or IPv6.</span></span> <span data-ttu-id="4d63a-112">Il formato delle informazioni di connessione è il seguente: < ><  ><>*suffisso* di indirizzo di trasporto.</span><span class="sxs-lookup"><span data-stu-id="4d63a-112">The format of the connection information is as follows: <*Transport*><*Address*><*Suffix*>.</span></span> <span data-ttu-id="4d63a-113">Per esempi, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="4d63a-113">For examples, see Remarks.</span></span> <span data-ttu-id="4d63a-114">Se non viene fornita alcuna informazione di connessione, viene usato il computer locale.</span><span class="sxs-lookup"><span data-stu-id="4d63a-114">If no connection information is provided, the local computer is used.</span></span>

</dd> <dt>

<span data-ttu-id="4d63a-115">*flag* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="4d63a-115">*flags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4d63a-116">Flag di sessione che specificano il metodo di autenticazione, ad esempio [*Negotiate*](windows-remote-management-glossary.md) Authentication o [*Digest Authentication*](windows-remote-management-glossary.md), per la connessione a un computer remoto.</span><span class="sxs-lookup"><span data-stu-id="4d63a-116">The session flags that specify the authentication method, such as [*Negotiate authentication*](windows-remote-management-glossary.md) or [*Digest authentication*](windows-remote-management-glossary.md), for connecting to a remote computer.</span></span> <span data-ttu-id="4d63a-117">Questi flag specificano anche altre informazioni sulla connessione della sessione, ad esempio la codifica o la crittografia.</span><span class="sxs-lookup"><span data-stu-id="4d63a-117">These flags also specify other session connection information, such as encoding or encryption.</span></span> <span data-ttu-id="4d63a-118">Questo parametro deve contenere uno o più flag in **\_ \_ WSManSessionFlags** per una connessione remota.</span><span class="sxs-lookup"><span data-stu-id="4d63a-118">This parameter must contain one or more of the flags in **\_\_WSManSessionFlags** for a remote connection.</span></span> <span data-ttu-id="4d63a-119">Per altre informazioni, vedere [costanti di sessione](session-constants.md).</span><span class="sxs-lookup"><span data-stu-id="4d63a-119">For more information, see [Session Constants](session-constants.md).</span></span> <span data-ttu-id="4d63a-120">Non sono necessarie impostazioni di flag per una connessione a WinRM nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="4d63a-120">No flag settings are required for a connection to WinRM on the local computer.</span></span> <span data-ttu-id="4d63a-121">Il valore predefinito è **WSManFlagUseNegotiate**.</span><span class="sxs-lookup"><span data-stu-id="4d63a-121">The default is **WSManFlagUseNegotiate**.</span></span>

<span data-ttu-id="4d63a-122">Per ulteriori informazioni, vedere [autenticazione per le connessioni remote](authentication-for-remote-connections.md) e il parametro *ConnectionOptions* .</span><span class="sxs-lookup"><span data-stu-id="4d63a-122">For more information, see [Authentication for Remote Connections](authentication-for-remote-connections.md) and the *connectionOptions* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="4d63a-123">*ConnectionOptions* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="4d63a-123">*connectionOptions* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4d63a-124">Puntatore a un oggetto [**ConnectionOptions**](connectionoptions.md) che contiene un nome utente e una password.</span><span class="sxs-lookup"><span data-stu-id="4d63a-124">A pointer to a [**ConnectionOptions**](connectionoptions.md) object that contains a user name and password.</span></span> <span data-ttu-id="4d63a-125">Il valore predefinito è **null**.</span><span class="sxs-lookup"><span data-stu-id="4d63a-125">The default is **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4d63a-126">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4d63a-126">Return value</span></span>

<span data-ttu-id="4d63a-127">Oggetto [**sessione**](session.md) che può quindi essere utilizzato per eseguire operazioni WinRM locali o remote.</span><span class="sxs-lookup"><span data-stu-id="4d63a-127">A [**Session**](session.md) object that can then be used to perform local or remote WinRM operations.</span></span>

## <a name="remarks"></a><span data-ttu-id="4d63a-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="4d63a-128">Remarks</span></span>

<span data-ttu-id="4d63a-129">Il metodo **CreateSession** Inizializza l'oggetto [**Session**](session.md) raccogliendo parametri, ad esempio flag, credenziali e una stringa di connessione per il parametro *Connection* .</span><span class="sxs-lookup"><span data-stu-id="4d63a-129">The **CreateSession** method initializes the [**Session**](session.md) object by gathering parameters, such as flags, credentials, and a connection string for the *connection* parameter.</span></span> <span data-ttu-id="4d63a-130">**CreateSession** non si connette effettivamente al computer locale o remoto.</span><span class="sxs-lookup"><span data-stu-id="4d63a-130">**CreateSession** does not actually connect to the local or remote computer.</span></span> <span data-ttu-id="4d63a-131">Se non è possibile stabilire la connessione, si verifica un errore durante la prima operazione di **sessione** , ad esempio [**Get**](session-get.md) o [**enumerate**](session-enumerate.md), dopo la chiamata a **CreateSession**.</span><span class="sxs-lookup"><span data-stu-id="4d63a-131">If the connection cannot be established, a failure occurs on the first **Session** operation, such as a [**Get**](session-get.md) or [**Enumerate**](session-enumerate.md), after the call to **CreateSession**.</span></span> <span data-ttu-id="4d63a-132">Questo comportamento è diverso da una connessione [*WMI*](windows-remote-management-glossary.md) a uno [*spazio dei nomi*](windows-remote-management-glossary.md) in un computer remoto.</span><span class="sxs-lookup"><span data-stu-id="4d63a-132">This behavior differs from a [*WMI*](windows-remote-management-glossary.md) connection to a [*namespace*](windows-remote-management-glossary.md) on a remote computer.</span></span> <span data-ttu-id="4d63a-133">Per ulteriori informazioni, vedere [gestione remota Windows e WMI](windows-remote-management-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="4d63a-133">For more information, see [Windows Remote Management and WMI](windows-remote-management-and-wmi.md).</span></span>

<span data-ttu-id="4d63a-134">L'esempio di codice VBScript seguente viene usato per chiamare questo metodo.</span><span class="sxs-lookup"><span data-stu-id="4d63a-134">The following VBScript code example is used to call this method.</span></span>


```VB
Set session = _
    wsman.CreateSession("<Transport><Address><Suffix>")
```



<span data-ttu-id="4d63a-135">Negli esempi seguenti vengono illustrati i diversi formati utilizzati per specificare le informazioni di connessione nel parametro *Connection* . quando si crea una sessione HTTPS, il campo <*Address*> deve corrispondere al nome del certificato del computer server, in caso contrario si verifica un errore:</span><span class="sxs-lookup"><span data-stu-id="4d63a-135">The following examples show the different formats used to specify connection information in the *connection* parameter (when creating an HTTPS session, the <*Address*> field must match the server computer certificate name, otherwise a failure occurs):</span></span>

-   <span data-ttu-id="4d63a-136">"https://service"</span><span class="sxs-lookup"><span data-stu-id="4d63a-136">"https://service"</span></span>

    <span data-ttu-id="4d63a-137">Usa HTTPS per connettersi al percorso predefinito del servizio Web.</span><span class="sxs-lookup"><span data-stu-id="4d63a-137">Uses HTTPS to connect to the default web service location.</span></span>

-   <span data-ttu-id="4d63a-138">"https://service.corp.com/websvcs/wsman"</span><span class="sxs-lookup"><span data-stu-id="4d63a-138">"https://service.corp.com/websvcs/wsman"</span></span>

    <span data-ttu-id="4d63a-139">Usa HTTPS per connettersi alla posizione specifica del servizio Web.</span><span class="sxs-lookup"><span data-stu-id="4d63a-139">Uses HTTPS to connect to the specific web service location.</span></span>

-   <span data-ttu-id="4d63a-140">"https:// \[ E3D7:0000:0000:0000:51F4:9BC8: C0A8:6420 \] "</span><span class="sxs-lookup"><span data-stu-id="4d63a-140">"https://\[E3D7:0000:0000:0000:51F4:9BC8:C0A8:6420\]"</span></span>

    <span data-ttu-id="4d63a-141">Usa HTTPS e IPv6 con la porta predefinita.</span><span class="sxs-lookup"><span data-stu-id="4d63a-141">Uses HTTPS and IPv6 with the default port.</span></span>

-   <span data-ttu-id="4d63a-142">"https:// \[ E3D7:0000:0000:0000:51F4:9BC8: C0A8:6420 \] : 9999/WSMan"</span><span class="sxs-lookup"><span data-stu-id="4d63a-142">"https://\[E3D7:0000:0000:0000:51F4:9BC8:C0A8:6420\]:9999/wsman"</span></span>

    <span data-ttu-id="4d63a-143">Usa HTTPS e IPv6 con la porta specificata.</span><span class="sxs-lookup"><span data-stu-id="4d63a-143">Uses HTTPS and IPv6 with the given port.</span></span>

## <a name="examples"></a><span data-ttu-id="4d63a-144">Esempio</span><span class="sxs-lookup"><span data-stu-id="4d63a-144">Examples</span></span>

<span data-ttu-id="4d63a-145">Nell'esempio di codice VBScript seguente viene creata una sessione nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="4d63a-145">The following VBScript code example creates a session on the local computer.</span></span>


```VB
 Set NewSession = Wsman.CreateSession   
   
```



<span data-ttu-id="4d63a-146">Nell'esempio di codice VBScript seguente viene creata una sessione in un computer remoto identificato da un indirizzo IP.</span><span class="sxs-lookup"><span data-stu-id="4d63a-146">The following VBScript code example creates a session on a remote computer that is identified by an IP address.</span></span> <span data-ttu-id="4d63a-147">Lo script fornisce un nome utente e una password per un account.</span><span class="sxs-lookup"><span data-stu-id="4d63a-147">The script supplies a user name and password for an account.</span></span> <span data-ttu-id="4d63a-148">I flag **WSManFlagCredUserNamePassword** e **WSManFlagUseBasic** vengono combinati per indicare che l'account è un account locale nel computer remoto.</span><span class="sxs-lookup"><span data-stu-id="4d63a-148">The flags **WSManFlagCredUserNamePassword** and **WSManFlagUseBasic** are combined to indicate that the account is a local account on the remote computer.</span></span> <span data-ttu-id="4d63a-149">Se la creazione della sessione ha esito negativo, lo script viene terminato.</span><span class="sxs-lookup"><span data-stu-id="4d63a-149">If the creation of the session fails, the script terminates.</span></span> <span data-ttu-id="4d63a-150">Lo script usa i metodi che restituiscono la costante, ad esempio [**WSMan. SessionFlagUseBasic**](wsman-sessionflagusebasic.md).</span><span class="sxs-lookup"><span data-stu-id="4d63a-150">The script uses the methods that return the constant, such as [**WSMan.SessionFlagUseBasic**](wsman-sessionflagusebasic.md).</span></span>

<span data-ttu-id="4d63a-151">Per eseguire questo script, tenere presente che è necessario configurare le impostazioni di configurazione predefinite per client e server per consentire il traffico non crittografato e l'autenticazione di base (**AllowUnencrypted** impostato su **true** e Basic impostato su **true**).</span><span class="sxs-lookup"><span data-stu-id="4d63a-151">To run this script, be aware that you must configure the default configuration settings for both client and server to allow unencrypted traffic and Basic authentication (**AllowUnencrypted** set to **True** and Basic set to **True**).</span></span> <span data-ttu-id="4d63a-152">Per ulteriori informazioni, vedere [installazione e configurazione per gestione remota Windows](installation-and-configuration-for-windows-remote-management.md).</span><span class="sxs-lookup"><span data-stu-id="4d63a-152">For more information, see [Installation and Configuration for Windows Remote Management](installation-and-configuration-for-windows-remote-management.md).</span></span>


```VB
iFlags = WSMan.SessionFlagUseBasic Or WSMan.SessionFlagCredUsernamePassword
Set Options = Wsman.CreateConnectionOptions
Options.Username = "MyUserName"
Options.Password = "MyPassword"
Set NewSession = WSMan.CreateSession("127.0.51.1", iFlags, _
    Options) 
```



<span data-ttu-id="4d63a-153">Nell'esempio di codice VBScript seguente, l'account è un account di dominio e viene utilizzata l'autenticazione Negotiate.</span><span class="sxs-lookup"><span data-stu-id="4d63a-153">In the following VBScript code example, the account is a domain account and Negotiate authentication is used.</span></span> <span data-ttu-id="4d63a-154">Con l'autenticazione Negotiate, è necessario specificare il nome utente come `computername\username` o `ipaddress\username` .</span><span class="sxs-lookup"><span data-stu-id="4d63a-154">With Negotiate authentication, you must specify the user name as `computername\username` or `ipaddress\username`.</span></span>


```VB
iFlags = WSMan.SessionFlagUseNegotiate Or WSMan.SessionFlagCredUsernamePassword
Set Options = Wsman.CreateConnectionOptions
Options.Username = "MyComputer\MyUserName"
Options.Password = "MyPassword"
Set NewSession = WSMan.CreateSession("127.0.51.1", iFlags, _
    Options) 
```



## <a name="requirements"></a><span data-ttu-id="4d63a-155">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4d63a-155">Requirements</span></span>



| <span data-ttu-id="4d63a-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="4d63a-156">Requirement</span></span> | <span data-ttu-id="4d63a-157">Valore</span><span class="sxs-lookup"><span data-stu-id="4d63a-157">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d63a-158">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4d63a-158">Minimum supported client</span></span><br/> | <span data-ttu-id="4d63a-159">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4d63a-159">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="4d63a-160">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4d63a-160">Minimum supported server</span></span><br/> | <span data-ttu-id="4d63a-161">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4d63a-161">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="4d63a-162">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4d63a-162">Header</span></span><br/>                   | <dl> <span data-ttu-id="4d63a-163"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="4d63a-163"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="4d63a-164">IDL</span><span class="sxs-lookup"><span data-stu-id="4d63a-164">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4d63a-165"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4d63a-165"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="4d63a-166">Libreria</span><span class="sxs-lookup"><span data-stu-id="4d63a-166">Library</span></span><br/>                  | <dl> <span data-ttu-id="4d63a-167"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="4d63a-167"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="4d63a-168">DLL</span><span class="sxs-lookup"><span data-stu-id="4d63a-168">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4d63a-169"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4d63a-169"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4d63a-170">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4d63a-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d63a-171">**WSMan**</span><span class="sxs-lookup"><span data-stu-id="4d63a-171">**WSMan**</span></span>](wsman.md)
</dt> <dt>

[<span data-ttu-id="4d63a-172">**ConnectionOptions**</span><span class="sxs-lookup"><span data-stu-id="4d63a-172">**ConnectionOptions**</span></span>](connectionoptions.md)
</dt> <dt>

[<span data-ttu-id="4d63a-173">**Sessione**</span><span class="sxs-lookup"><span data-stu-id="4d63a-173">**Session**</span></span>](session.md)
</dt> <dt>

[<span data-ttu-id="4d63a-174">Autenticazione per le connessioni remote</span><span class="sxs-lookup"><span data-stu-id="4d63a-174">Authentication for Remote Connections</span></span>](authentication-for-remote-connections.md)
</dt> <dt>

[<span data-ttu-id="4d63a-175">Installazione e configurazione per Gestione remota Windows</span><span class="sxs-lookup"><span data-stu-id="4d63a-175">Installation and Configuration for Windows Remote Management</span></span>](installation-and-configuration-for-windows-remote-management.md)
</dt> </dl>

 

 





