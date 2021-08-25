---
title: Ricerca con ActiveX Data Objects (ADO)
description: Il ActiveX ADO (Data Object) è costituito da oggetti elencati nella tabella seguente.
ms.assetid: 27298f53-a652-49f2-a6e6-d92c7c6022af
ms.tgt_platform: multiple
keywords:
- ActiveX Oggetti dati ADSI , ricerca con ADO
- Ricerca con ACTIVEX Data Objects ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52eba3dd5bc9013500aa4def7a31104d1408d4818b78a35ff75f09f2454f4d21
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119770451"
---
# <a name="searching-with-activex-data-objects-ado"></a>Ricerca con ActiveX Data Objects (ADO)

Il ActiveX ADO (Data Object) è costituito da oggetti elencati nella tabella seguente.



| Oggetto         | Descrizione                                                                                                                        |
|----------------|------------------------------------------------------------------------------------------------------------------------------------|
| **Connection** | Una connessione aperta a un'OLE DB dati esistente, ad esempio ADSI.                                                                          |
| **Comando**    | Definisce un comando specifico da eseguire sull'origine dati.                                                                         |
| **Parametro**  | Raccolta facoltativa per tutti i parametri da fornire all'oggetto comando.                                                        |
| **Recordset**  | Set di record da una tabella, un oggetto comando o una SQL sintassi. È possibile creare un recordset senza alcun oggetto connessione sottostante. |
| **Campo**      | Singola colonna di dati in un recordset.                                                                                            |
| **Proprietà**   | Raccolta di valori forniti dal provider per ADO.                                                                           |
| **Error (Errore) (Error (Errore)e)**      | Contiene dati sugli errori di accesso ai dati. Aggiornato quando si verifica un errore in una singola operazione.                                      |



 

Per la comunicazione tra ADO e ADSI, devono essere presenti almeno due oggetti ADO: **Connection** e **RecordSet.** Questi oggetti ADO servono rispettivamente per autenticare gli utenti ed enumerare i risultati. In genere, si usa anche un oggetto **Command** per mantenere una connessione attiva, specificare i parametri di query, ad esempio le dimensioni della pagina e l'ambito di ricerca, ed eseguire una query. Per altre informazioni sulla sintassi del filtro di ricerca, vedere [Sintassi del filtro di ricerca.](search-filter-syntax.md)

**L'oggetto Connection** carica il provider OLE DB e convalida le credenziali utente. In Visual Basic chiamare la **funzione CreateObject** con "ADODB. Connection" per creare un'istanza di un **oggetto Connection** e quindi impostare la proprietà **Provider** dell'oggetto **Connection** su "ADsDSOObject". "ADODB. Connection" è il ProgID dell'oggetto **Connection** e "ADsDSOObject" è il nome del provider OLE DB in ADSI. Se non viene specificata alcuna credenziale, vengono utilizzate le credenziali dell'utente attualmente connesso.

Nell'esempio di codice seguente viene illustrato come creare un'istanza di un **oggetto Connection.**


```VB
Set con = CreateObject("ADODB.Connection")
con.Provider = "ADsDSOObject"
```



Nell'esempio di codice seguente viene illustrato come creare un'istanza di un **oggetto Connection.**


```VB
<%
Set con = Server.CreateObject("ADODB.Connection")
con.Provider = "ADsDSOObject"
%>
```



Nell'esempio di codice seguente viene illustrato come creare un'istanza di un **oggetto Connection.** Tenere presente che è necessario includere la libreria dei tipi ADO (msadoXX.dll) come uno dei riferimenti nel Visual Basic progetto.


```VB
Dim Con As New Connection
con.Provider = "ADsDSOObject"
```



Specificare i dati di autenticazione utente impostando le proprietà **dell'oggetto Connection.** Nella tabella seguente sono elencate le proprietà di autenticazione utente supportate da ADSI.



| Proprietà           | Descrizione                                                                                                                                                                                                                                                                                                                                    |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| "ID utente"          | Stringa che identifica l'utente il cui contesto di sicurezza viene utilizzato durante l'esecuzione della ricerca. Per altre informazioni sul formato della stringa del nome utente, vedere [**IADsOpenDSObject::OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject). Se non specificato, il valore predefinito è l'utente connesso o l'utente rappresentato dal processo chiamante. |
| "Password"         | Stringa che specifica la password dell'utente identificato da "ID utente".                                                                                                                                                                                                                                                                      |
| "Crittografa password" | Valore booleano che specifica se la password è crittografata. Il valore predefinito è **false**.                                                                                                                                                                                                                                                    |
| "Flag ADSI"        | Set di flag dell'enumerazione [**ADS \_ AUTHENTICATION \_ ENUM**](/windows/win32/api/iads/ne-iads-ads_authentication_enum) che specificano le opzioni di autenticazione dell'associazione. Il valore predefinito è zero.                                                                                                                                                                         |



 

Nell'esempio di codice seguente viene illustrato come impostare le proprietà prima di creare **l'oggetto** Command.


```VB
Set oConnect = CreateObject("ADODB.Connection")
oConnect.Provider = "ADsDSOObject"
oConnect.Properties("User ID") = stUser
oConnect.Properties("Password") = stPass
oConnect.Properties("Encrypt Password") = True
oConnect.Open "DS Query", stUser, stPass
```



Il secondo oggetto ADO è **l'oggetto Command.** Il ProgID **dell'oggetto Command** è "ADODB.Command". Questo oggetto consente di eseguire istruzioni di query e altri comandi ad ADSI usando la connessione attiva. **L'oggetto Command** usa la **proprietà ActiveConnection** per mantenere una connessione attiva. Gestisce anche la proprietà **CommandText** per contenere le istruzioni di query rilasciate da un utente. Le istruzioni di query sono espresse nel [sotto SQL o](sql-dialect.md) nel [dialetto LDAP.](ldap-dialect.md)

Negli esempi di codice seguenti viene illustrato come creare un **oggetto** Command.


```VB
Set command = CreateObject("ADODB.Command")
Set command.ActiveConnection = oConnect
command.CommandText = 
"SELECT AdsPath, cn FROM 'LDAP://DC=Fabrikam,DC=com' WHERE objectClass = '*'"
```



Nell'esempio di codice seguente includere la libreria dei tipi ADO (msadoXX.dll) come uno dei riferimenti.


```VB
Dim command As New Command
Set command.ActiveConnection = oConnect
command.CommandText = "<LDAP://DC=Fabrikam,DC=com>;(objectClass=*);AdsPath, cn; subTree"
```



Le opzioni di ricerca **per l'oggetto** Command vengono specificate impostando la **proprietà** Properties. Nella tabella seguente sono elencate le proprietà denominate accettabili per **Proprietà**.



| Proprietà denominata      | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| "Asynchronous"      | Valore booleano che specifica se la ricerca è sincrona o asincrona. Il valore predefinito è False (sincrono). Una ricerca sincrona si blocca fino a quando il server non restituisce l'intero risultato o, per una ricerca di pagine, l'intera pagina. Una ricerca asincrona si blocca fino a quando non è disponibile una riga dei risultati della ricerca o fino al termine del tempo specificato dalla proprietà "Timeout".                           |
| "Memorizzare nella cache i risultati"     | Valore booleano che specifica se il risultato deve essere memorizzato nella cache sul lato client. Il valore predefinito è **true.** ADSI memorizza nella cache il set di risultati. La disattivazione di questa opzione può essere utile per set di risultati di grandi dimensioni.                                                                                                                                                                                                    |
| "Segnalazioni di inseguimento"   | Valore [**dell'enumerazione ADS \_ REFERRAL \_ REFERRALS \_ che**](/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum) specifica in che modo la ricerca cerca i riferimenti. Il valore predefinito è **ADS \_ \_ REFERRALS \_ NEVER**. Per altre informazioni su questa proprietà, vedere [Segnalazioni.](/windows/desktop/AD/referrals)<br/>                                                                                                                                           |
| "Solo nomi di colonna" | Valore booleano che indica che la ricerca deve recuperare solo il nome degli attributi a cui sono stati assegnati valori. Il valore predefinito è **false**.                                                                                                                                                                                                                                                       |
| "Deref Aliases"     | Valore booleano che specifica se gli alias degli oggetti trovati vengono risolti. Il valore predefinito è **false**.                                                                                                                                                                                                                                                                                                        |
| "Dimensioni pagina"         | Valore intero che attiva il paging e specifica il numero massimo di oggetti da restituire in un set di risultati. Il valore predefinito è nessuna dimensione di pagina. Per altre informazioni, vedere [Recupero di set di risultati di grandi dimensioni.](retrieving-large-results-sets.md)                                                                                                                                                                       |
| "SearchScope"       | Valore [**dell'enumerazione ADS \_ SCOPEENUM**](/windows/win32/api/iads/ne-iads-ads_scopeenum) che specifica l'ambito di ricerca. Il valore predefinito è **ADS \_ SCOPE \_ SUBTREE.**                                                                                                                                                                                                                                                                  |
| "Limite dimensioni"        | Valore intero che specifica il limite di dimensioni per la ricerca. Per Active Directory, il limite delle dimensioni specifica il numero massimo di oggetti restituiti. Il server interrompe la ricerca quando viene raggiunto il limite di dimensioni e restituisce i risultati accumulati. Il valore predefinito è nessun limite.                                                                                                                                  |
| "Ordina in base a"           | Stringa che specifica un elenco delimitato da virgole di attributi da utilizzare come chiavi di ordinamento. Questa proprietà funziona solo per i server di directory che supportano il controllo LDAP per l'ordinamento lato server. Active Directory supporta il controllo di ordinamento, ma può influire sulle prestazioni del server, in particolare se il set di risultati è di grandi dimensioni. Tenere presente che Active Directory supporta solo una singola chiave di ordinamento. Il valore predefinito non è alcun ordinamento. |
| "Limite di tempo"        | Valore intero che specifica il limite di tempo, in secondi, per la ricerca. Quando viene raggiunto il limite di tempo, il server interrompe la ricerca e restituisce i risultati accumulati. Il valore predefinito non è alcun limite di tempo.                                                                                                                                                                                                      |
| "Timeout"           | Valore intero che specifica il valore di timeout sul lato client, espresso in secondi. Questo valore indica il tempo di attesa dei risultati dal server da parte del client prima di arrestare la ricerca. Il valore predefinito non è alcun timeout.                                                                                                                                                                                                  |



 

Nell'esempio di codice seguente viene illustrato come impostare le opzioni di ricerca.


```VB
Const ADS_SCOPE_ONELEVEL = 1
Const ADS_CHASE_REFERRALS_EXTERNAL = &H40

Dim Com As New Command
 
Com.Properties("Page Size") = 999
Com.Properties("Timeout") = 30     ' Seconds
Com.Properties("searchscope") = ADS_SCOPE_ONELEVEL
Com.Properties("Chase referrals") = ADS_CHASE_REFERRALS_EXTERNAL
Com.Properties("Cache Results") = False     ' Do not cache the result set.
```



Il terzo oggetto ADO è **RecordSet**. Questo oggetto viene ottenuto quando si richiama il **metodo Execute** su un **oggetto** Command. La funzione principale **dell'oggetto RecordSet** è enumerare il set di risultati e ottenere i dati. Il set di risultati può contenere valori per gli attributi con valori singoli o multipli. Ottenere un attributo a valore singolo è semplice, come ottenere il valore della colonna nel database relazionale, ad esempio:


```VB
Fields('name').Value
```



Il recupero di un attributo con più valori, tuttavia, è più complesso. In questo caso, **Field.Value** è una matrice ed è necessario controllare il limite inferiore e superiore della matrice, come illustrato nell'esempio di codice seguente.


```VB
Set rs = Com.Execute
 
For i = 0 To rs.Fields.Count - 1
    Debug.Print rs.Fields(i).Name, rs.Fields(i).Type
Next i
 
'--------------------------
' Navigate the record set.
'--------------------------
rs.MoveFirst
lstResult.Clear      ' Clear the user interface.
While Not rs.EOF
For i = 0 To rs.Fields.Count - 1
    ' For Multi Value attribute
    If rs.Fields(i).Type = adVariant And Not (IsNull(rs.Fields(i).Value)) Then
        Debug.Print rs.Fields(i).Name, " = "
        For j = LBound(rs.Fields(i).Value) To UBound(rs.Fields(i).Value)
            Debug.Print rs.Fields(i).Value(j), " # "
            lstResult.AddItem rs.Fields(i).Value(j)
        Next j
    Else
        ' For Single Value attribute.
         Debug.Print rs.Fields(i).Name, " = ", rs.Fields(i).Value
         lstResult.AddItem rs.Fields(i).Value
    End If
Next i
rs.MoveNext
Wend
```



L'esempio di codice seguente disabilita gli account utente in un server LDAP.


```VB
Dim X as IADs
Dim con As New Connection, rs As New Recordset
Dim MyUser As IADsUser
 
con.Provider = "ADsDSOObject"
con.Open "Active Directory Provider", "CN=Test,CN=Users,DC=Fabrikam,DC=COM,O=INTERNET", "Password"
Set rs = con.Execute("<LDAP://MyMachine/DC=MyDomain,DC=Fabrikam,DC=com>;(objectClass=User);ADsPath;onelevel")
 
While Not rs.EOF
    ' Bind to the object to make changes 
    ' to it because ADO is currently read-only.
    MyUser = GetObject(rs.Fields(0).Value)
    MyUser.AccountDisabled = True
    MyUser.SetInfo
    rs.MoveNext
Wend
```



Per altre informazioni sul modello a oggetti ADO, vedere [Microsoft ActiveX Data Objects](/sql/ado/microsoft-activex-data-objects-ado?view=sql-server-ver15).

 

