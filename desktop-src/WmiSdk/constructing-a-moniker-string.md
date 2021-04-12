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
# <a name="constructing-a-moniker-string"></a>Creazione di una stringa del moniker

Il formato della stringa del moniker è simile a quello di un percorso dell'oggetto WMI standard. Per ulteriori informazioni, vedere la pagina relativa [ai requisiti del percorso degli oggetti WMI](wmi-object-path-requirements.md).

Un moniker presenta le parti seguenti:

-   Il prefisso WinMgmts: (obbligatorio). Il prefisso indica a Windows script host (WSH) che il codice seguente utilizzerà gli [oggetti API di scripting](scripting-api-objects.md).
-   Un componente delle impostazioni di sicurezza (facoltativo)
-   Componente del percorso di un oggetto WMI (facoltativo)

Non è possibile specificare una password in una stringa del moniker WMI. Se è necessario modificare la password (parametro *strPassword* ) o il tipo di autenticazione (parametro *strAuthority* ) quando ci si connette a WMI, chiamare [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md). Tenere presente che è possibile specificare la password e l'autorità solo in connessioni ai computer remoti. Se si tenta di impostare questi dati in uno script in esecuzione nel computer locale, si verifica un errore. Per ulteriori informazioni sul momento in cui vengono utilizzate le impostazioni di sicurezza e i componenti del percorso dell'oggetto, vedere [WMI Security Settings](/previous-versions/tn-archive/ee156574(v=technet.10)).

Il moniker seguente specifica l'oggetto [**SWbemServices**](swbemservices.md) che rappresenta l'impostazione predefinita della radice dello spazio dei nomi \\ , con la rappresentazione su e il privilegio wbemPrivilegeDebug (SeDebugPrivilege) abilitato e il privilegio wbemPrivilegeSecurity (SeSecurityPrivilege) disabilitato.


```VB
"winmgmts:{impersonationLevel=impersonate," & "(debug,!security)}!root\default"
```



> [!Note]
>
> Tutti i valori letterali stringa non fanno distinzione tra maiuscole e minuscole.
>
> Il prefisso "!" per un privilegio indica che è necessario disabilitare il privilegio; l'omissione di questo prefisso implica l'abilitazione del privilegio.
>
> Il prefisso "!" viene utilizzato per il nome o lo spazio dei nomi del computer quando le impostazioni di sicurezza vengono specificate tra parentesi prima del nome del computer o dello spazio dei nomi.

 

Quando si specifica il percorso dell'oggetto, sono consentite le seguenti assegnazioni predefinite:

-   Il nome computer del computer può essere omesso dal percorso dell'oggetto, nel qual caso si presuppone il nome del computer locale.
-   Lo spazio dei nomi può essere omesso dal percorso dell'oggetto, nel qual caso si presuppone lo spazio dei nomi predefinito.

    Questo è determinato dal valore della chiave del registro di sistema **HKEY \_ Local \_ Machine** \\ **software** \\ **Microsoft** \\ **WBEM** \\ **Scripting** \\ **default namespace**, il valore predefinito è "root \\ CIMv2".

-   È possibile specificare anche una classe o un'istanza, nel qual caso l'oggetto restituito è un oggetto WMI anziché un oggetto Services.

> [!Note]  
> Se viene specificata una classe o un'istanza di, non è possibile omettere lo spazio dei nomi quando si specifica il nome del computer.

 

Per un riferimento alle costanti dei privilegi utilizzate sulla stringa del moniker WMI, vedere [costanti Privilege](privilege-constants.md)e i descrittori "scripting short name".

## <a name="valid-moniker-strings"></a>Stringhe del moniker valide

Negli esempi seguenti vengono illustrate stringhe del moniker valide.

Il moniker seguente identifica lo spazio dei nomi predefinito nel computer locale. Viene restituito un oggetto [**SWbemServices**](swbemservices.md) .


```VB
WinMgmts:
```



Il moniker seguente identifica lo spazio dei nomi predefinito nel server MyServer. Viene restituito un oggetto [**SWbemServices**](swbemservices.md) .


```VB
"WinMgmts://myServer"
```



Il moniker seguente identifica lo \\ spazio dei nomi CIMV2 radice nel computer server. Viene restituito un oggetto [**SWbemServices**](swbemservices.md) .


```VB
"WinMgmts://myServer/root/cimv2"
```



Il moniker seguente identifica lo \\ spazio dei nomi CIMV2 radice nel server locale. Viene restituito un oggetto [**SWbemServices**](swbemservices.md) .


```VB
"WinMgmts:root/cimv2"
```



Il moniker seguente identifica la classe [**Win32 \_ disco logico**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) nello \\ spazio dei nomi CIMV2 radice nel server MyServer. Viene restituito un oggetto [**SWbemObject**](swbemobject.md) .


```VB
"WinMgmts:{impersonationLevel=impersonate}" _
    & "!//myServer/root/cimv2:Win32_LogicalDisk"
```



Il moniker seguente identifica la classe [**Win32 \_ disco logico**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) nello \\ spazio dei nomi CIMV2 radice nel server locale. Viene restituito un oggetto [**SWbemObject**](swbemobject.md) .


```VB
"WinMgmts:{impersonationLevel=impersonate}" & "!root/cimv2:Win32_LogicalDisk"
```



Il moniker seguente identifica la classe [**Win32 \_ disco logico**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) nello spazio dei nomi predefinito nel server locale. Viene restituito un oggetto [**SWbemObject**](swbemobject.md) .


```VB
"WinMgmts:{impersonationLevel=impersonate}" & "!Win32_LogicalDisk"
```



Il moniker seguente identifica l'istanza di [**\_ disco logico Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) corrispondente all'unità C: nello spazio dei nomi di scripting predefinito nel server locale. Viene restituito un oggetto [**SWbemObject**](swbemobject.md) . Lo spazio dei nomi predefinito per lo scripting è determinato dall'impostazione di configurazione dello spazio dei nomi predefinita, come specificato nel controllo WMI. Per ulteriori informazioni, vedere [impostazione della sicurezza dello spazio dei nomi con il controllo WMI](setting-namespace-security-with-the-wmi-control.md).


```VB
"WinMgmts::Win32_LogicalDisk='C:'"
```



Il moniker seguente identifica l'istanza di [**\_ disco logico Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) corrispondente all'unità C: nello \\ spazio dei nomi CIMV2 radice nel server MyServer. Viene restituito un oggetto [**SWbemObject**](swbemobject.md) .


```VB
"WinMgmts:{impersonationLevel=impersonate}" & "!//myServer/root/cimv2:Win32_LogicalDisk="C:""
```



Il moniker seguente identifica l'istanza di [**\_ disco logico Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) corrispondente all'unità C: nello \\ spazio dei nomi CIMV2 radice nel server locale. Viene restituito un oggetto [**SWbemObject**](swbemobject.md) .


```VB
"WinMgmts:{impersonationLevel=impersonate}" & "!root/cimv2:Win32_LogicalDisk="C:""
```



Il moniker seguente identifica l'istanza di [**\_ disco logico Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) corrispondente all'unità C: nello spazio dei nomi predefinito nel server locale. Viene restituito un oggetto [**SWbemObject**](swbemobject.md) .


```VB
"WinMgmts:{impersonationLevel=impersonate}" & "!Win32_LogicalDisk="C:""
```



Il moniker seguente imposta il livello di rappresentazione da rappresentare e imposta il privilegio di debug SE \_ .


```VB
"WinMgmts:{impersonationLevel=impersonate, (Debug)}"
```



Il moniker seguente imposta il livello di rappresentazione da rappresentare e imposta il privilegio di debug SE \_ . Revoca inoltre il \_ privilegio di arresto se.


```VB
"WinMgmts:{impersonate,(Debug,!Shutdown)}"
```



Il moniker seguente recupera le descrizioni localizzate in inglese americano per la classe **MyClass** dallo \\ spazio dei nomi WMI radice.


```VB
"WinMgmts:[locale=ms_409]!root/wmi:myclass"
```



Il moniker seguente richiede l'autenticazione Kerberos tramite il server di dominio principale \\ .


```VB
"Winmgmts:{impersonationLevel=delegate," _
    & "authority=kerberos:mydomain\server}" _
    & "!//myserver/root/default:__cimomidentification=@"
```



Il moniker seguente richiede l'autenticazione NTLM tramite il dominio di dominio.


```VB
"Winmgmts:{impersonationLevel=impersonate," & _
    "authority=ntlmdomain:mydomain} " & _
    "!//myserver/root/default:__cimomidentification=@
```



Nell'esempio di codice VBScript seguente viene illustrato come combinare la sicurezza e i parametri delle impostazioni locali in un moniker.


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
> Sebbene i moniker forniscano un accesso più diretto agli oggetti, in determinate circostanze, l'utilizzo ripetuto dei moniker può risultare meno efficiente del codice equivalente che si connette in modo esplicito a WMI. Se le prestazioni dell'applicazione sono considerate, provare a usare i meccanismi alternativi.
>
> Non è possibile utilizzare la funzione **GetObject** fornita da VBScript per aggiornare o impostare i dati durante l'esecuzione di script incorporati all'interno di una pagina HTML, in quanto Microsoft Internet Explorer nega l'utilizzo di questa chiamata per motivi di sicurezza.

 

 

 
