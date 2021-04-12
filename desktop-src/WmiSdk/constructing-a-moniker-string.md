---
description: Il formato della stringa del moniker è simile a quello di un percorso dell'oggetto WMI standard. Per ulteriori informazioni, vedere la pagina relativa ai requisiti del percorso degli oggetti WMI.
ms.assetid: 1aacc523-2a2f-43f5-96a3-aa0387cbae3e
ms.tgt_platform: multiple
title: Creazione di una stringa del moniker
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44e54e29b3c8f14890dc1cedd5907059308e8d22
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344936"
---
# <a name="constructing-a-moniker-string"></a><span data-ttu-id="35ad3-104">Creazione di una stringa del moniker</span><span class="sxs-lookup"><span data-stu-id="35ad3-104">Constructing a Moniker String</span></span>

<span data-ttu-id="35ad3-105">Il formato della stringa del moniker è simile a quello di un percorso dell'oggetto WMI standard.</span><span class="sxs-lookup"><span data-stu-id="35ad3-105">The moniker string format is similar to that of a standard WMI object path.</span></span> <span data-ttu-id="35ad3-106">Per ulteriori informazioni, vedere la pagina relativa [ai requisiti del percorso degli oggetti WMI](wmi-object-path-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="35ad3-106">For more information, see [WMI Object Path Requirements](wmi-object-path-requirements.md).</span></span>

<span data-ttu-id="35ad3-107">Un moniker presenta le parti seguenti:</span><span class="sxs-lookup"><span data-stu-id="35ad3-107">A moniker has the following parts:</span></span>

-   <span data-ttu-id="35ad3-108">Il prefisso WinMgmts: (obbligatorio).</span><span class="sxs-lookup"><span data-stu-id="35ad3-108">The prefix WinMgmts: (mandatory).</span></span> <span data-ttu-id="35ad3-109">Il prefisso indica a Windows script host (WSH) che il codice seguente utilizzerà gli [oggetti API di scripting](scripting-api-objects.md).</span><span class="sxs-lookup"><span data-stu-id="35ad3-109">The prefix instructs the Windows Script Host (WSH) that the following code will be using the [Scripting API objects](scripting-api-objects.md).</span></span>
-   <span data-ttu-id="35ad3-110">Un componente delle impostazioni di sicurezza (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="35ad3-110">A security settings component (optional)</span></span>
-   <span data-ttu-id="35ad3-111">Componente del percorso di un oggetto WMI (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="35ad3-111">A WMI object path component (optional)</span></span>

<span data-ttu-id="35ad3-112">Non è possibile specificare una password in una stringa del moniker WMI.</span><span class="sxs-lookup"><span data-stu-id="35ad3-112">You cannot specify a password in a WMI moniker string.</span></span> <span data-ttu-id="35ad3-113">Se è necessario modificare la password (parametro *strPassword* ) o il tipo di autenticazione (parametro *strAuthority* ) quando ci si connette a WMI, chiamare [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md).</span><span class="sxs-lookup"><span data-stu-id="35ad3-113">If you must change the password (*strPassword* parameter) or the type of authentication (*strAuthority* parameter) when connecting to WMI, then call [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md).</span></span> <span data-ttu-id="35ad3-114">Tenere presente che è possibile specificare la password e l'autorità solo in connessioni ai computer remoti.</span><span class="sxs-lookup"><span data-stu-id="35ad3-114">Be aware that you can only specify the password and authority in connections to remote computers.</span></span> <span data-ttu-id="35ad3-115">Se si tenta di impostare questi dati in uno script in esecuzione nel computer locale, si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="35ad3-115">Attempting to set these in a script that is running on the local computer results in a error.</span></span> <span data-ttu-id="35ad3-116">Per ulteriori informazioni sul momento in cui vengono utilizzate le impostazioni di sicurezza e i componenti del percorso dell'oggetto, vedere [WMI Security Settings](/previous-versions/tn-archive/ee156574(v=technet.10)).</span><span class="sxs-lookup"><span data-stu-id="35ad3-116">For more information about when the security settings and object path components are used, see [WMI Security Settings](/previous-versions/tn-archive/ee156574(v=technet.10)).</span></span>

<span data-ttu-id="35ad3-117">Il moniker seguente specifica l'oggetto [**SWbemServices**](swbemservices.md) che rappresenta l'impostazione predefinita della radice dello spazio dei nomi \\ , con la rappresentazione su e il privilegio wbemPrivilegeDebug (SeDebugPrivilege) abilitato e il privilegio wbemPrivilegeSecurity (SeSecurityPrivilege) disabilitato.</span><span class="sxs-lookup"><span data-stu-id="35ad3-117">The following moniker specifies the [**SWbemServices**](swbemservices.md) object that represents the namespace root\\default, with impersonation on and the wbemPrivilegeDebug (SeDebugPrivilege) privilege enabled, and the wbemPrivilegeSecurity (SeSecurityPrivilege) privilege disabled.</span></span>


```VB
"winmgmts:{impersonationLevel=impersonate," & "(debug,!security)}!root\default"
```



> [!Note]
>
> <span data-ttu-id="35ad3-118">Tutti i valori letterali stringa non fanno distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="35ad3-118">All string literals are case-insensitive.</span></span>
>
> <span data-ttu-id="35ad3-119">Il prefisso "!" per un privilegio indica che è necessario disabilitare il privilegio; l'omissione di questo prefisso implica l'abilitazione del privilegio.</span><span class="sxs-lookup"><span data-stu-id="35ad3-119">The "!" prefix on a privilege indicates that the privilege is to be disabled; the omission of this prefix implies that the privilege is to be enabled.</span></span>
>
> <span data-ttu-id="35ad3-120">Il prefisso "!" viene utilizzato per il nome o lo spazio dei nomi del computer quando le impostazioni di sicurezza vengono specificate tra parentesi prima del nome del computer o dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="35ad3-120">The "!" prefix is used on the computer name or namespace when security settings are specified in brackets before the computer name or namespace.</span></span>

 

<span data-ttu-id="35ad3-121">Quando si specifica il percorso dell'oggetto, sono consentite le seguenti assegnazioni predefinite:</span><span class="sxs-lookup"><span data-stu-id="35ad3-121">The following default assignments are allowed when specifying the object path:</span></span>

-   <span data-ttu-id="35ad3-122">Il nome computer del computer può essere omesso dal percorso dell'oggetto, nel qual caso si presuppone il nome del computer locale.</span><span class="sxs-lookup"><span data-stu-id="35ad3-122">The computer machine name can be omitted from the object path, in which case the local machine name is assumed.</span></span>
-   <span data-ttu-id="35ad3-123">Lo spazio dei nomi può essere omesso dal percorso dell'oggetto, nel qual caso si presuppone lo spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="35ad3-123">The namespace can be omitted from the object path, in which case the default namespace is assumed.</span></span>

    <span data-ttu-id="35ad3-124">Questo è determinato dal valore della chiave del registro di sistema **HKEY \_ Local \_ Machine** \\ **software** \\ **Microsoft** \\ **WBEM** \\ **Scripting** \\ **default namespace**, il valore predefinito è "root \\ CIMv2".</span><span class="sxs-lookup"><span data-stu-id="35ad3-124">This is determined by the value of the registry key **HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**WBEM**\\**Scripting**\\**Default Namespace**, the default value is "Root\\CIMv2".</span></span>

-   <span data-ttu-id="35ad3-125">È possibile specificare anche una classe o un'istanza, nel qual caso l'oggetto restituito è un oggetto WMI anziché un oggetto Services.</span><span class="sxs-lookup"><span data-stu-id="35ad3-125">A class or instance can also be specified, in which case the returned object is a WMI object rather than a services object.</span></span>

> [!Note]  
> <span data-ttu-id="35ad3-126">Se viene specificata una classe o un'istanza di, non è possibile omettere lo spazio dei nomi quando si specifica il nome del computer.</span><span class="sxs-lookup"><span data-stu-id="35ad3-126">If a class or instance is specified, you cannot omit the namespace when specifying the computer machine name.</span></span>

 

<span data-ttu-id="35ad3-127">Per un riferimento alle costanti dei privilegi utilizzate sulla stringa del moniker WMI, vedere [costanti Privilege](privilege-constants.md)e i descrittori "scripting short name".</span><span class="sxs-lookup"><span data-stu-id="35ad3-127">For a reference of the Privilege Constants used on WMI moniker string, see [Privilege Constants](privilege-constants.md), and the "Scripting short name" descriptors.</span></span>

## <a name="valid-moniker-strings"></a><span data-ttu-id="35ad3-128">Stringhe del moniker valide</span><span class="sxs-lookup"><span data-stu-id="35ad3-128">Valid Moniker Strings</span></span>

<span data-ttu-id="35ad3-129">Negli esempi seguenti vengono illustrate stringhe del moniker valide.</span><span class="sxs-lookup"><span data-stu-id="35ad3-129">The following examples show valid moniker strings.</span></span>

<span data-ttu-id="35ad3-130">Il moniker seguente identifica lo spazio dei nomi predefinito nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="35ad3-130">The following moniker identifies the default namespace on the local computer.</span></span> <span data-ttu-id="35ad3-131">Viene restituito un oggetto [**SWbemServices**](swbemservices.md) .</span><span class="sxs-lookup"><span data-stu-id="35ad3-131">An [**SWbemServices**](swbemservices.md) object is returned.</span></span>


```VB
WinMgmts:
```



<span data-ttu-id="35ad3-132">Il moniker seguente identifica lo spazio dei nomi predefinito nel server MyServer.</span><span class="sxs-lookup"><span data-stu-id="35ad3-132">The following moniker identifies the default namespace on the computer myServer.</span></span> <span data-ttu-id="35ad3-133">Viene restituito un oggetto [**SWbemServices**](swbemservices.md) .</span><span class="sxs-lookup"><span data-stu-id="35ad3-133">An [**SWbemServices**](swbemservices.md) object is returned.</span></span>


```VB
"WinMgmts://myServer"
```



<span data-ttu-id="35ad3-134">Il moniker seguente identifica lo \\ spazio dei nomi CIMV2 radice nel computer server.</span><span class="sxs-lookup"><span data-stu-id="35ad3-134">The following moniker identifies the root\\cimv2 namespace on the myServer computer.</span></span> <span data-ttu-id="35ad3-135">Viene restituito un oggetto [**SWbemServices**](swbemservices.md) .</span><span class="sxs-lookup"><span data-stu-id="35ad3-135">An [**SWbemServices**](swbemservices.md) object is returned.</span></span>


```VB
"WinMgmts://myServer/root/cimv2"
```



<span data-ttu-id="35ad3-136">Il moniker seguente identifica lo \\ spazio dei nomi CIMV2 radice nel server locale.</span><span class="sxs-lookup"><span data-stu-id="35ad3-136">The following moniker identifies the root\\cimv2 namespace on the local server.</span></span> <span data-ttu-id="35ad3-137">Viene restituito un oggetto [**SWbemServices**](swbemservices.md) .</span><span class="sxs-lookup"><span data-stu-id="35ad3-137">An [**SWbemServices**](swbemservices.md) object is returned.</span></span>


```VB
"WinMgmts:root/cimv2"
```



<span data-ttu-id="35ad3-138">Il moniker seguente identifica la classe [**Win32 \_ disco logico**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) nello \\ spazio dei nomi CIMV2 radice nel server MyServer.</span><span class="sxs-lookup"><span data-stu-id="35ad3-138">The following moniker identifies the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class in the root\\cimv2 namespace on the myServer server.</span></span> <span data-ttu-id="35ad3-139">Viene restituito un oggetto [**SWbemObject**](swbemobject.md) .</span><span class="sxs-lookup"><span data-stu-id="35ad3-139">An [**SWbemObject**](swbemobject.md) object is returned.</span></span>


```VB
"WinMgmts:{impersonationLevel=impersonate}" _
    & "!//myServer/root/cimv2:Win32_LogicalDisk"
```



<span data-ttu-id="35ad3-140">Il moniker seguente identifica la classe [**Win32 \_ disco logico**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) nello \\ spazio dei nomi CIMV2 radice nel server locale.</span><span class="sxs-lookup"><span data-stu-id="35ad3-140">The following moniker identifies the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class in the root\\cimv2 namespace on the local server.</span></span> <span data-ttu-id="35ad3-141">Viene restituito un oggetto [**SWbemObject**](swbemobject.md) .</span><span class="sxs-lookup"><span data-stu-id="35ad3-141">An [**SWbemObject**](swbemobject.md) object is returned.</span></span>


```VB
"WinMgmts:{impersonationLevel=impersonate}" & "!root/cimv2:Win32_LogicalDisk"
```



<span data-ttu-id="35ad3-142">Il moniker seguente identifica la classe [**Win32 \_ disco logico**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) nello spazio dei nomi predefinito nel server locale.</span><span class="sxs-lookup"><span data-stu-id="35ad3-142">The following moniker identifies the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class in the default namespace on the local server.</span></span> <span data-ttu-id="35ad3-143">Viene restituito un oggetto [**SWbemObject**](swbemobject.md) .</span><span class="sxs-lookup"><span data-stu-id="35ad3-143">An [**SWbemObject**](swbemobject.md) object is returned.</span></span>


```VB
"WinMgmts:{impersonationLevel=impersonate}" & "!Win32_LogicalDisk"
```



<span data-ttu-id="35ad3-144">Il moniker seguente identifica l'istanza di [**\_ disco logico Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) corrispondente all'unità C: nello spazio dei nomi di scripting predefinito nel server locale.</span><span class="sxs-lookup"><span data-stu-id="35ad3-144">The following moniker identifies the instance of [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) corresponding to drive C: in the default scripting namespace on the local server.</span></span> <span data-ttu-id="35ad3-145">Viene restituito un oggetto [**SWbemObject**](swbemobject.md) .</span><span class="sxs-lookup"><span data-stu-id="35ad3-145">An [**SWbemObject**](swbemobject.md) object is returned.</span></span> <span data-ttu-id="35ad3-146">Lo spazio dei nomi predefinito per lo scripting è determinato dall'impostazione di configurazione dello spazio dei nomi predefinita, come specificato nel controllo WMI.</span><span class="sxs-lookup"><span data-stu-id="35ad3-146">The default namespace for scripting is determined by the default namespace configuration setting as specified in the WMI Control.</span></span> <span data-ttu-id="35ad3-147">Per ulteriori informazioni, vedere [impostazione della sicurezza dello spazio dei nomi con il controllo WMI](setting-namespace-security-with-the-wmi-control.md).</span><span class="sxs-lookup"><span data-stu-id="35ad3-147">For more information, see [Setting Namespace Security with the WMI Control](setting-namespace-security-with-the-wmi-control.md).</span></span>


```VB
"WinMgmts::Win32_LogicalDisk='C:'"
```



<span data-ttu-id="35ad3-148">Il moniker seguente identifica l'istanza di [**\_ disco logico Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) corrispondente all'unità C: nello \\ spazio dei nomi CIMV2 radice nel server MyServer.</span><span class="sxs-lookup"><span data-stu-id="35ad3-148">The following moniker identifies the instance of [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) corresponding to drive C: in the root\\cimv2 namespace on the myServer server.</span></span> <span data-ttu-id="35ad3-149">Viene restituito un oggetto [**SWbemObject**](swbemobject.md) .</span><span class="sxs-lookup"><span data-stu-id="35ad3-149">An [**SWbemObject**](swbemobject.md) object is returned.</span></span>


```VB
"WinMgmts:{impersonationLevel=impersonate}" & "!//myServer/root/cimv2:Win32_LogicalDisk="C:""
```



<span data-ttu-id="35ad3-150">Il moniker seguente identifica l'istanza di [**\_ disco logico Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) corrispondente all'unità C: nello \\ spazio dei nomi CIMV2 radice nel server locale.</span><span class="sxs-lookup"><span data-stu-id="35ad3-150">The following moniker identifies the instance of [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) corresponding to drive C: in the root\\cimv2 namespace on the local server.</span></span> <span data-ttu-id="35ad3-151">Viene restituito un oggetto [**SWbemObject**](swbemobject.md) .</span><span class="sxs-lookup"><span data-stu-id="35ad3-151">An [**SWbemObject**](swbemobject.md) object is returned.</span></span>


```VB
"WinMgmts:{impersonationLevel=impersonate}" & "!root/cimv2:Win32_LogicalDisk="C:""
```



<span data-ttu-id="35ad3-152">Il moniker seguente identifica l'istanza di [**\_ disco logico Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) corrispondente all'unità C: nello spazio dei nomi predefinito nel server locale.</span><span class="sxs-lookup"><span data-stu-id="35ad3-152">The following moniker identifies the instance of [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) corresponding to drive C: in the default namespace on the local server.</span></span> <span data-ttu-id="35ad3-153">Viene restituito un oggetto [**SWbemObject**](swbemobject.md) .</span><span class="sxs-lookup"><span data-stu-id="35ad3-153">An [**SWbemObject**](swbemobject.md) object is returned.</span></span>


```VB
"WinMgmts:{impersonationLevel=impersonate}" & "!Win32_LogicalDisk="C:""
```



<span data-ttu-id="35ad3-154">Il moniker seguente imposta il livello di rappresentazione da rappresentare e imposta il privilegio di debug SE \_ .</span><span class="sxs-lookup"><span data-stu-id="35ad3-154">The following moniker sets the impersonation level to impersonate and sets the SE\_DEBUG privilege.</span></span>


```VB
"WinMgmts:{impersonationLevel=impersonate, (Debug)}"
```



<span data-ttu-id="35ad3-155">Il moniker seguente imposta il livello di rappresentazione da rappresentare e imposta il privilegio di debug SE \_ .</span><span class="sxs-lookup"><span data-stu-id="35ad3-155">The following moniker sets the impersonation level to impersonate and sets the SE\_DEBUG privilege.</span></span> <span data-ttu-id="35ad3-156">Revoca inoltre il \_ privilegio di arresto se.</span><span class="sxs-lookup"><span data-stu-id="35ad3-156">It also revokes the SE\_SHUTDOWN privilege.</span></span>


```VB
"WinMgmts:{impersonate,(Debug,!Shutdown)}"
```



<span data-ttu-id="35ad3-157">Il moniker seguente recupera le descrizioni localizzate in inglese americano per la classe **MyClass** dallo \\ spazio dei nomi WMI radice.</span><span class="sxs-lookup"><span data-stu-id="35ad3-157">The following moniker retrieves American English localized descriptions for the **myclass** class from the root\\wmi namespace.</span></span>


```VB
"WinMgmts:[locale=ms_409]!root/wmi:myclass"
```



<span data-ttu-id="35ad3-158">Il moniker seguente richiede l'autenticazione Kerberos tramite il server di dominio principale \\ .</span><span class="sxs-lookup"><span data-stu-id="35ad3-158">The following moniker requests Kerberos authentication using the principal mydomain\\server.</span></span>


```VB
"Winmgmts:{impersonationLevel=delegate," _
    & "authority=kerberos:mydomain\server}" _
    & "!//myserver/root/default:__cimomidentification=@"
```



<span data-ttu-id="35ad3-159">Il moniker seguente richiede l'autenticazione NTLM tramite il dominio di dominio.</span><span class="sxs-lookup"><span data-stu-id="35ad3-159">The following moniker requests NTLM authentication using the mydomain domain.</span></span>


```VB
"Winmgmts:{impersonationLevel=impersonate," & _
    "authority=ntlmdomain:mydomain} " & _
    "!//myserver/root/default:__cimomidentification=@
```



<span data-ttu-id="35ad3-160">Nell'esempio di codice VBScript seguente viene illustrato come combinare la sicurezza e i parametri delle impostazioni locali in un moniker.</span><span class="sxs-lookup"><span data-stu-id="35ad3-160">The following VBScript code example shows how to combine security and locale parameters in a moniker.</span></span>


```VB
'*****************************************************************
'   Name    :  Moniker.vbs
'
'   Purpose :  This example shows how to set various 
'              parameters in a moniker. 
'****************************************************************

Set myobj = GetObject("WINMGMTS:" _
            & "{impersonationLevel=impersonate," _
            & "authenticationLevel=pktPrivacy," _
            & "authority=ntlmdomain:mydomain," _
            & "(Debug,!Shutdown)}" _
            & "[locale=ms_409]" _
            & "!\\User1\ROOT\CIMV2:Win32_LogicalDisk=""C:""")

wscript.echo "File system = " & myobj.filesystem
```



> [!Note]
>
> Sebbene i moniker forniscano un accesso più diretto agli oggetti, in determinate circostanze, l'utilizzo ripetuto dei moniker può risultare meno efficiente del codice equivalente che si connette in modo esplicito a WMI. <span data-ttu-id="35ad3-162">Se le prestazioni dell'applicazione sono considerate, provare a usare i meccanismi alternativi.</span><span class="sxs-lookup"><span data-stu-id="35ad3-162">If application performance is a consideration, consider using the alternative mechanisms.</span></span>
>
> <span data-ttu-id="35ad3-163">Non è possibile utilizzare la funzione **GetObject** fornita da VBScript per aggiornare o impostare i dati durante l'esecuzione di script incorporati all'interno di una pagina HTML, in quanto Microsoft Internet Explorer nega l'utilizzo di questa chiamata per motivi di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="35ad3-163">It is not possible to use the **GetObject** function provided by VBScript to update or set data when running scripts embedded within an HTML page, as Microsoft Internet Explorer denies the use of this call for security reasons.</span></span>

 

 

 
