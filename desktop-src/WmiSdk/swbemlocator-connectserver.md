---
description: Si connette allo spazio dei nomi nel computer specificato nel parametro strServer.
ms.assetid: 31364c68-b031-4cf0-851f-b4e302f077e0
ms.tgt_platform: multiple
title: Metodo SWbemLocator.ConnectServer (Wbemdisp.h)
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
ms.openlocfilehash: f4153a5761d59c54cf8635202adcca0ddf72603022ebf8dbb5b160231c90e49e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119955211"
---
# <a name="swbemlocatorconnectserver-method"></a>Metodo SWbemLocator.ConnectServer

Il **metodo ConnectServer** dell'oggetto [**SWbemLocator**](swbemlocator.md) si connette allo spazio dei nomi nel computer specificato nel *parametro strServer.* Il computer di destinazione può essere locale o remoto, ma deve disporre di WMI installato. Per esempi e un confronto con il tipo di connessione del moniker, vedere [Creazione di uno script WMI](creating-a-wmi-script.md).

A partire da Windows Vista, **SWbemLocator.ConnectServer** può connettersi ai computer che eseguono IPv6 usando un indirizzo IPv6 nel *parametro strServer.* Per altre informazioni, vedere [Supporto IPv6 e IPv4 in WMI.](ipv6-and-ipv4-support-in-wmi.md)

Per una spiegazione di questa sintassi, vedere [Convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).

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

Nome computer a cui ci si connette. Se il computer remoto si trova in un dominio diverso rispetto all'account utente con cui si accede, usare il nome completo del computer. Se non si specifica questo parametro, per impostazione predefinita la chiamata viene chiamata al computer locale.

Esempio: `server1.network.fabrikam`

È anche possibile usare un indirizzo IP in questo parametro. Se l'indirizzo IP è in formato IPv6, il computer di destinazione deve eseguire IPv6. Un indirizzo in IPv4 è simile a `123.123.123.123`

Un indirizzo IP in formato IPv6 è simile a `2010:836B:4179::836B:4179`

Per altre informazioni su DNS e IPv4, vedere la sezione Osservazioni.

</dd> <dt>

*strNamespace* \[ in, facoltativo\]
</dt> <dd>

Stringa che specifica lo spazio dei nomi a cui si accede. Ad esempio, per accedere allo spazio dei nomi predefinito \\ radice, usare root \\ default. Se non si specifica questo parametro, per impostazione predefinita viene utilizzato lo spazio dei nomi configurato come spazio dei nomi predefinito per lo scripting. Per altre informazioni, vedere [Creazione di un'applicazione WMI o di uno script](creating-a-wmi-application-or-script.md).

Esempio: \\ "CIMV2 radice"

</dd> <dt>

*strUser* \[ in, facoltativo\]
</dt> <dd>

Nome utente da usare per la connessione. La stringa può essere sotto forma di nome utente o nome utente di \\ dominio. Lasciare vuoto questo parametro per usare il contesto di sicurezza corrente. Il *parametro strUser* deve essere usato solo con connessioni a server WMI remoti. Se si tenta di specificare *strUser per* una connessione WMI locale, il tentativo di connessione ha esito negativo. Se è in uso l'autenticazione Kerberos, il nome utente e la password specificati in *strUser* e *strPassword* non possono essere intercettati in una rete. È possibile usare il formato UPN per specificare *strUser*.

Esempio: "NomeDominio \\ NomeUtente"

> [!Note]  
> Se viene specificato un dominio in *strAuthority*, il dominio non deve essere specificato qui. Se si specifica il dominio in entrambi i parametri, viene restituito un errore Parametro non valido.

 

</dd> <dt>

*strPassword* \[ in, facoltativo\]
</dt> <dd>

Stringa che specifica la password da usare durante il tentativo di connessione. Lasciare vuoto il parametro per usare il contesto di sicurezza corrente. Il *parametro strPassword* deve essere usato solo con connessioni a server WMI remoti. Se si tenta di specificare *strPassword per* una connessione WMI locale, il tentativo di connessione ha esito negativo. Se è in uso l'autenticazione Kerberos, il nome utente e la password specificati in *strUser* e *strPassword* non possono essere intercettati in rete.

</dd> <dt>

*strLocale* \[ in, facoltativo\]
</dt> <dd>

Stringa che specifica il codice di localizzazione. Se si vogliono usare le impostazioni locali correnti, lasciarlo vuoto. Se non è vuoto, questo parametro deve essere una stringa che indica le impostazioni locali desiderate in cui devono essere recuperate le informazioni. Per gli identificatori delle impostazioni locali Microsoft, il formato della stringa è "MS xxxx", dove xxxx è una stringa in formato esadecimale che indica \_ l'LCID. Ad esempio, l'inglese americano viene visualizzato come "MS \_ 409".

</dd> <dt>

*strAuthority* \[ in, facoltativo\]
</dt> <dd>

<dt>

""
</dt> <dd>

Questo parametro è facoltativo. Tuttavia, se viene specificato, è possibile usare solo Kerberos o NTLMDomain.

</dd> <dt>

Kerberos:
</dt> <dd>

Se il *parametro strAuthority* inizia con la stringa "Kerberos:", viene usata l'autenticazione Kerberos e questo parametro deve contenere un nome di entità Kerberos. Il nome dell'entità Kerberos viene specificato come Kerberos:*dominio*, ad esempio dove è il server a cui si sta `Kerberos:fabrikam` tentando di `fabrikam` connettersi.

Esempio: "Kerberos:DOMAIN"

</dd> <dt>

NTLMDomain:
</dt> <dd>

Per usare l'autenticazione NT Lan Manager (NTLM), è necessario specificarla come NTLMDomain:*dominio*, ad esempio dove è il `NTLMDomain:fabrikam` nome del `fabrikam` dominio.

Esempio: "NTLMDomain:DOMAIN"

</dd> </dl>

Se si lascia vuoto questo parametro, il sistema operativo negozia con COM per determinare se viene utilizzata l'autenticazione NTLM o Kerberos. Questo parametro deve essere usato solo con connessioni a server WMI remoti. Se si tenta di impostare l'autorità per una connessione WMI locale, il tentativo di connessione ha esito negativo.

> [!Note]  
> Se il dominio viene specificato in *strUser*, che è la posizione preferita, non deve essere specificato qui. Se si specifica il dominio in entrambi i parametri, viene restituito un errore Parametro non valido.

 

</dd> <dt>

*iSecurityFlags* \[ in, facoltativo\]
</dt> <dd>

Utilizzato per passare i valori dei flag **a ConnectServer**.

<dt>

0 (0x0)
</dt> <dd>

Il valore 0 per questo parametro fa sì che la chiamata a **ConnectServer** restituirà solo dopo che è stata stabilita la connessione al server. Ciò potrebbe causare l'arresto indefinito del programma se non è possibile stabilire la connessione.

</dd> <dt>

<span id="wbemConnectFlagUseMaxWait"></span><span id="wbemconnectflagusemaxwait"></span><span id="WBEMCONNECTFLAGUSEMAXWAIT"></span>

<span id="wbemConnectFlagUseMaxWait"></span><span id="wbemconnectflagusemaxwait"></span><span id="WBEMCONNECTFLAGUSEMAXWAIT"></span>wbemConnectFlagUseMaxWait**** (128 (0x80))


</dt> <dd>

La **chiamata ConnectServer** verrà restituita in 2 minuti o meno. Usare questo flag per impedire al programma di rispondere a tempo indeterminato se non è possibile stabilire la connessione.

</dd> </dl> </dd> <dt>

*objwbemNamedValueSet* \[ in, facoltativo\]
</dt> <dd>

In genere, questa operazione non è definita. In caso contrario, si tratta di un [**oggetto SWbemNamedValueSet**](swbemnamedvalueset.md) i cui elementi rappresentano le informazioni sul contesto che possono essere usate dal provider che sta servo della richiesta. Un provider che supporta o richiede tali informazioni deve documentare i nomi dei valori riconosciuti, il tipo di dati del valore, i valori consentiti e la semantica.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

In caso di esito positivo, WMI restituisce un oggetto [**SWbemServices**](swbemservices.md) associato allo spazio dei nomi specificato in *strNamespace* nel computer specificato in *strServer*.

## <a name="error-codes"></a>Codici di errore

Dopo il completamento del **metodo ConnectServer,** l'oggetto [Err](/previous-versions//sbf5ze0e(v=vs.85)) può contenere uno dei codici di errore nell'elenco seguente.

<dl> <dt>

**wbemErrAccessDenied** - 2147749891 (0x80041003)
</dt> <dd>

Nome utente e password correnti o specificati non validi o autorizzati a stabilire la connessione.

</dd> <dt>

**wbemErrFailed** - 2147749889 (0x80041001)
</dt> <dd>

Errore non specificato.

</dd> <dt>

**wbemErrInvalidNamespace** - 2147749902 (0x8004100E)
</dt> <dd>

Lo spazio dei nomi specificato non esiste nel server.

</dd> <dt>

**wbemErrInvalidParameter** - 2147749896 (0x80041008)
</dt> <dd>

È stato specificato un parametro non valido o non è stato possibile analizzare lo spazio dei nomi.

</dd> <dt>

**wbemErrOutOfMemory** - 2147749894 (0x80041006)
</dt> <dd>

Memoria insufficiente per completare l'operazione.

</dd> <dt>

**wbemErrTransportFailure** - 2147749909
</dt> <dd>

Si è verificato un errore di rete, impedendo il normale funzionamento.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il **metodo ConnectServer** viene spesso usato per la connessione a un account con credenziali di nome utente e password diverse in un computer remoto perché non è possibile specificare una password diversa in una stringa [del moniker.](constructing-a-moniker-string.md) Per altre informazioni, vedere [Connessione a WMI in un computer remoto](connecting-to-wmi-on-a-remote-computer.md).

L'uso di un indirizzo IPv4 per connettersi a un server remoto può comportare un comportamento imprevisto. La causa probabile è la non aggiornamento delle voci DNS nell'ambiente. In questi casi, verrà usata la voce PTR non obsoleta per il computer, con risultati imprevedibili. Per evitare questo comportamento, è possibile aggiungere un punto (".") all'indirizzo IP prima di chiamare ConnectServer. In questo modo la ricerca DNS inversa ha esito negativo, ma può consentire la riuscita della chiamata **ConnectServer** nel computer corretto.

## <a name="examples"></a>Esempio

L'esempio di codice VBScript seguente descrive come connettersi a un computer remoto per ottenere dati [**\_ Win32 IP4RouteTable.**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetable) Il nome di dominio specificato in *strDomain* viene usato in *strAuthority.*


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



Il frammento di codice di PowerShell seguente accede a un server remoto ed elenca le classi WMI disponibili.


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
| Intestazione<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemLocator<br/>                                                          |
| IID<br/>                      | IID \_ ISWbemLocator<br/>                                                           |



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

 

