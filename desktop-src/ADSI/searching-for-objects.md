---
title: Ricerca di oggetti
description: Julie Bankert deve trovare i numeri di telefono per tutti i Program Manager che lavorano nel reparto 101. Per eseguire questa operazione, è possibile creare uno script che usa ADO e ADSI.
ms.assetid: c6325068-4ae2-4348-9938-96402262cd43
ms.tgt_platform: multiple
keywords:
- ricerca di oggetti ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb3c26f05b63524e3a657c0c460efb921978bd19
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/20/2020
ms.locfileid: "103858041"
---
# <a name="searching-for-objects"></a>Ricerca di oggetti

Julie Bankert deve trovare i numeri di telefono per tutti i Program Manager che lavorano nel reparto 101. Per eseguire questa operazione, è possibile creare uno script che usa ADO e ADSI.

Quando si utilizza il provider ADO per eseguire una query, il set di risultati restituirà solo i primi 1000 oggetti. Per questo motivo, è importante usare una query di paging per poter recuperare tutti gli oggetti nel set di risultati, purché il servizio directory non sia stato impostato per limitare il numero di elementi in un set di risultati. I set restituiti conterranno il numero di elementi specificati nelle dimensioni della pagina e i set di paging continueranno a essere restituiti finché non verranno restituiti tutti gli elementi del set di risultati.


```VB
' Create the connection and command object.
Set oConnection1 = CreateObject("ADODB.Connection")
Set oCommand1 = CreateObject("ADODB.Command")
' Open the connection.
oConnection1.Provider = "ADsDSOObject"  ' This is the ADSI OLE-DB provider name
oConnection1.Open "Active Directory Provider"
' Create a command object for this connection.
Set oCommand1.ActiveConnection = oConnection1

' Compose a search string.
oCommand1.CommandText = "select name,telephoneNumber " & _
"from 'LDAP://DC=Fabrikam,DC=com'" & _
"WHERE objectCategory='Person'" & _
"AND objectClass='user'" & _
"AND title='Program Manager'" & _
"AND department=101"

' Execute the query.
Set rs = oCommand1.Execute
'--------------------------------------
' Navigate the record set
'--------------------------------------
While Not rs.EOF
    Debug.Print rs.Fields("Name") & " , " & rs.Fields("telephoneNumber")
    rs.MoveNext
Wend
```



Per eseguire una ricerca ADSI in Visual Basic o in un ambiente di scripting, sono necessari tre componenti ADO, ovvero **connessione**, **comando** e **Recordset**. L'oggetto **Connection** consente di specificare il nome del provider, le credenziali alternative, se applicabile, e altri flag. L'oggetto **Command** consente di specificare le preferenze di ricerca e la stringa di query. È necessario associare l'oggetto **connessione** a un oggetto **comando** prima dell'esecuzione della query. Infine, viene utilizzato l'oggetto **Recordset** per scorrere il set di risultati.

ADSI supporta due tipi di stringhe di query o dialetti. Nell'esempio di codice precedente viene usato il sottolinguaggio SQL. È anche possibile usare il dialetto LDAP. La stringa di query del dialetto LDAP è basata su [rfc 2254](https://www.ietf.org/rfc/rfc2254.txt) (un documento RFC è una richiesta di commenti, che costituisce la base per lo sviluppo di standard LDAP). L'esempio precedente può essere convertito nell'esempio di codice seguente.


```VB
oCommand1.CommandText = "<LDAP://DC=fabrikam,DC=COM>;" & _
"(&(objectCategory=Person)" & _
"(objectClass=user)" & _
"(title=ProgramManager)" & _
"(department=101));" & _
"name,telephoneNumber;subTree"
```



Perché la parola "subtree" è alla fine della stringa? Nel mondo della directory è possibile specificare l'ambito di ricerca. Le scelte disponibili sono: "base", "unlivello" e "sottoalbero". "base" viene usato per leggere l'oggetto stesso; "unlivello" si riferisce agli elementi figlio immediati, in modo analogo al comando **dir** ; il "sottoalbero" viene usato per eseguire ricerche in più livelli (in modo analogo a **dir/s**).

Con il sottolinguaggio SQL, è possibile specificare l'ambito nella proprietà Command, ad esempio nell'esempio di codice seguente.


```VB
oCommand1.Properties("SearchScope") = ADS_SCOPE_ONELEVEL
```



Se l'ambito non è specificato, per impostazione predefinita viene usata la ricerca del sottoalbero.

> [!Note]  
> Se si usa C++, è possibile usare l'interfaccia [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) di ADSI.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riorganizzazione](reorganization.md)
</dt> </dl>

 

 




