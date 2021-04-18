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
# <a name="swbemlocatorconnectserver-method"></a>SWbemLocator. ConnectServer, metodo

Il metodo **ConnectServer** dell'oggetto [**SWbemLocator**](swbemlocator.md) si connette allo spazio dei nomi nel computer specificato nel parametro *strServer* . Il computer di destinazione può essere locale o remoto, ma deve essere installato WMI. Per esempi e un confronto con il tipo di connessione del moniker, vedere [creazione di uno script WMI](creating-a-wmi-script.md).

A partire da Windows Vista, **SWbemLocator. ConnectServer** è in grado di connettersi ai computer che eseguono IPv6 utilizzando un indirizzo IPv6 nel parametro *strServer* . Per ulteriori informazioni, vedere [supporto di IPv6 e IPv4 in WMI](ipv6-and-ipv4-support-in-wmi.md).

Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintassi


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



## <a name="parameters"></a>Parametri

<dl> <dt>

*strServer* \[ in, facoltativo\]
</dt> <dd>

Nome del computer a cui ci si connette. Se il computer remoto si trova in un dominio diverso rispetto all'account utente con cui si esegue l'accesso, utilizzare il nome completo del computer. Se non si specifica questo parametro, la chiamata viene eseguita per impostazione predefinita sul computer locale.

Esempio: `server1.network.fabrikam`

È anche possibile usare un indirizzo IP in questo parametro. Se l'indirizzo IP è in formato IPv6, il computer di destinazione deve eseguire IPv6. Un indirizzo in IPv4 appare come `123.123.123.123`

Un indirizzo IP in formato IPv6 ha un aspetto simile al `2010:836B:4179::836B:4179`

Per ulteriori informazioni su DNS e IPv4, vedere la sezione Osservazioni.

</dd> <dt>

*strNameSpace* \[ in, facoltativo\]
</dt> <dd>

Stringa che specifica lo spazio dei nomi a cui si accede. Per accedere allo \\ spazio dei nomi predefinito radice, ad esempio, usare il \\ valore predefinito radice. Se non si specifica questo parametro, per impostazione predefinita viene utilizzato lo spazio dei nomi configurato come spazio dei nomi predefinito per lo scripting. Per ulteriori informazioni, vedere [creazione di un'applicazione o di uno script WMI](creating-a-wmi-application-or-script.md).

Esempio: "root \\ cimv2"

</dd> <dt>

*strUser* \[ in, facoltativo\]
</dt> <dd>

Nome utente da utilizzare per la connessione. Il formato della stringa può essere un nome utente o un nome utente di dominio \\ . Lasciare vuoto questo parametro per usare il contesto di sicurezza corrente. Il parametro *strUser* deve essere utilizzato solo con connessioni a server WMI remoti. Se si tenta di specificare *strUser* per una connessione WMI locale, il tentativo di connessione non riesce. Se l'autenticazione Kerberos è in uso, non è possibile intercettare il nome utente e la password specificati in *strUser* e *strPassword* in una rete. È possibile usare il formato UPN per specificare il *strUser*.

Esempio: "DomainName \\ username"

> [!Note]  
> Se un dominio viene specificato in *strAuthority*, non è necessario specificare il dominio in questo punto. Se si specifica il dominio in entrambi i parametri, si verifica un errore di parametro non valido.

 

</dd> <dt>

*strPassword* \[ in, facoltativo\]
</dt> <dd>

Stringa che specifica la password da utilizzare durante il tentativo di connessione. Lasciare vuoto il parametro per usare il contesto di sicurezza corrente. Il parametro *strPassword* deve essere utilizzato solo con connessioni a server WMI remoti. Se si tenta di specificare *strPassword* per una connessione WMI locale, il tentativo di connessione non riesce. Se è in uso l'autenticazione Kerberos, il nome utente e la password specificati in *strUser* e *strPassword* non possono essere intercettati sulla rete.

</dd> <dt>

*strLocale* \[ in, facoltativo\]
</dt> <dd>

Stringa che specifica il codice di localizzazione. Se si desidera utilizzare le impostazioni locali correnti, lasciarlo vuoto. Se non è vuoto, questo parametro deve essere una stringa che indica le impostazioni locali desiderate in cui devono essere recuperate le informazioni. Per gli identificatori delle impostazioni locali Microsoft, il formato della stringa è "MS \_ xxxx", dove xxxx è una stringa nel formato esadecimale che indica il valore LCID. Ad esempio, l'inglese americano verrebbe visualizzato come "MS \_ 409".

</dd> <dt>

*strAuthority* \[ in, facoltativo\]
</dt> <dd>

<dt>

""
</dt> <dd>

Questo parametro è facoltativo. Tuttavia, se è specificato, è possibile usare solo Kerberos o NTLMDomain.

</dd> <dt>

Kerberos
</dt> <dd>

Se il parametro *strAuthority* inizia con la stringa "Kerberos:", viene utilizzata l'autenticazione Kerberos e questo parametro deve contenere un nome entità Kerberos. Il nome dell'entità Kerberos viene specificato come Kerberos:*dominio*, ad esempio `Kerberos:fabrikam` dove `fabrikam` è il server a cui si sta tentando di connettersi.

Esempio: "Kerberos: DOMAIN"

</dd> <dt>

NTLMDomain
</dt> <dd>

Per utilizzare l'autenticazione NT LAN Manager (NTLM), è necessario specificarla come NTLMDomain:*Domain*, ad esempio `NTLMDomain:fabrikam` Where `fabrikam` è il nome del dominio.

Esempio: "NTLMDomain: DOMAIN"

</dd> </dl>

Se si lascia vuoto questo parametro, il sistema operativo negozia con COM per determinare se viene utilizzata l'autenticazione NTLM o Kerberos. Questo parametro deve essere utilizzato solo con connessioni a server WMI remoti. Se si tenta di impostare l'autorità per una connessione WMI locale, il tentativo di connessione non riesce.

> [!Note]  
> Se il dominio è specificato in *strUser*, che è il percorso preferito, questo non deve essere specificato in questo punto. Se si specifica il dominio in entrambi i parametri, si verifica un errore di parametro non valido.

 

</dd> <dt>

*iSecurityFlags* \[ in, facoltativo\]
</dt> <dd>

Utilizzato per passare i valori del flag a **ConnectServer**.

<dt>

0 (0x0)
</dt> <dd>

Il valore 0 per questo parametro determina la restituzione della chiamata a **ConnectServer** solo dopo che è stata stabilita la connessione al server. Questo potrebbe causare un arresto illimitato del programma se non è possibile stabilire la connessione.

</dd> <dt>

<span id="wbemConnectFlagUseMaxWait"></span><span id="wbemconnectflagusemaxwait"></span><span id="WBEMCONNECTFLAGUSEMAXWAIT"></span>

<span id="wbemConnectFlagUseMaxWait"></span><span id="wbemconnectflagusemaxwait"></span><span id="WBEMCONNECTFLAGUSEMAXWAIT"></span>wbemConnectFlagUseMaxWait * * * * (128 (0x80))


</dt> <dd>

La chiamata di **ConnectServer** è garantita la restituzione in 2 minuti o meno. Utilizzare questo flag per impedire che il programma cessi di rispondere a tempo indefinito se non è possibile stabilire la connessione.

</dd> </dl> </dd> <dt>

*objwbemNamedValueSet* \[ in, facoltativo\]
</dt> <dd>

In genere, non è definito. In caso contrario, si tratta di un oggetto [**SWbemNamedValueSet**](swbemnamedvalueset.md) i cui elementi rappresentano le informazioni sul contesto che possono essere utilizzate dal provider che sta servendo la richiesta. Un provider che supporta o richiede tali informazioni deve documentare i nomi dei valori riconosciuti, il tipo di dati del valore, i valori consentiti e la semantica.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

In caso di esito positivo, WMI restituisce un oggetto [**SWbemServices**](swbemservices.md) associato allo spazio dei nomi specificato in *strNameSpace* nel computer specificato in *strServer*.

## <a name="error-codes"></a>Codici di errore

Dopo il completamento del metodo **ConnectServer** , l'oggetto [Err](/previous-versions//sbf5ze0e(v=vs.85)) può contenere uno dei codici di errore elencati di seguito.

<dl> <dt>

**wbemErrAccessDenied** -2147749891 (0x80041003)
</dt> <dd>

Il nome utente o la password corrente o specificata non sono validi o sono autorizzati a eseguire la connessione.

</dd> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Errore non specificato.

</dd> <dt>

**wbemErrInvalidNamespace** -2147749902 (0x8004100E)
</dt> <dd>

Lo spazio dei nomi specificato non esiste nel server.

</dd> <dt>

**wbemErrInvalidParameter** -2147749896 (0x80041008)
</dt> <dd>

È stato specificato un parametro non valido o non è stato possibile analizzare lo spazio dei nomi.

</dd> <dt>

**wbemErrOutOfMemory** -2147749894 (0x80041006)
</dt> <dd>

Memoria insufficiente per completare l'operazione.

</dd> <dt>

**wbemErrTransportFailure** -2147749909
</dt> <dd>

Si è verificato un errore di rete che impedisce il normale funzionamento.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il metodo **ConnectServer** viene spesso usato per la connessione a un account con credenziali di nome utente e password diverse in un computer remoto perché non è possibile specificare una password diversa in una stringa del [moniker](constructing-a-moniker-string.md) . Per ulteriori informazioni, vedere [connessione a WMI in un computer remoto](connecting-to-wmi-on-a-remote-computer.md).

L'utilizzo di un indirizzo IPv4 per connettersi a un server remoto può causare un comportamento imprevisto. La causa probabile sono le voci DNS non aggiornate nell'ambiente in uso. In questi casi, verrà usata la voce PTR non aggiornata per il computer, con risultati imprevedibili. Per evitare questo comportamento, è possibile aggiungere un punto (".") all'indirizzo IP prima di chiamare ConnectServer. In questo modo, la ricerca DNS inversa avrà esito negativo, ma potrebbe consentire la riuscita della chiamata **ConnectServer** nel computer corretto.

## <a name="examples"></a>Esempio

Nell'esempio di codice VBScript seguente viene descritto come connettersi a un computer remoto per ottenere i dati [**\_ IP4RouteTable Win32**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetable) . Il nome di dominio specificato in *strDomain* viene usato in *strAuthority*.


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



Il seguente frammento di codice di PowerShell accede a un server remoto ed elenca le classi WMI disponibili.


```PowerShell
$NameSpace = 'root\ccm'
$ComputerName = 'sccm.company.com'
$WbemLocator = New-Object -ComObject "WbemScripting.SWbemLocator"
$WbemServices = $WbemLocator.ConnectServer($ComputerName, $Namespace)
$WbemClasses = $WbemServices.SubclassesOf()
$WbemClasses
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMLOCATOR CLSID<br/>                                                          |
| IID<br/>                      | \_ISWBEMLOCATOR IID<br/>                                                           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SWbemLocator**](swbemlocator.md)
</dt> <dt>

[**SWbemServices**](swbemservices.md)
</dt> <dt>

[Connessione a WMI in un computer remoto](connecting-to-wmi-on-a-remote-computer.md)
</dt> <dt>

[Creazione di uno script WMI](creating-a-wmi-script.md)
</dt> </dl>

 

