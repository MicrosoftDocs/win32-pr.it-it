---
title: Ricerca di oggetti
description: Julie Bankert deve trovare i numeri di telefono per tutti i program manager che lavorano nel reparto 101. A tale scopo, può creare uno script che usa ADO e ADSI.
ms.assetid: c6325068-4ae2-4348-9938-96402262cd43
ms.tgt_platform: multiple
keywords:
- ricerca di oggetti ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd41e87ad3396694b2f87158b15278c1dfbe28b044ad03ebbb09ddded705910a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119973504"
---
# <a name="searching-for-objects"></a>Ricerca di oggetti

Julie Bankert deve trovare i numeri di telefono per tutti i program manager che lavorano nel reparto 101. A tale scopo, può creare uno script che usa ADO e ADSI.

Quando si usa il provider ADO per eseguire una query, il set di risultati restituirà solo i primi 1000 oggetti. Per questo motivo, è importante usare una query di pagina per recuperare tutti gli oggetti nel set di risultati, purché il servizio directory non sia stato impostato per limitare il numero di elementi in un set di risultati. I set restituiti conterranno il numero di elementi specificati nelle dimensioni della pagina e i set di pagine continueranno a essere restituiti fino a quando non vengono restituiti tutti gli elementi nel set di risultati.


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



Per eseguire una ricerca ADSI in Visual Basic o in un ambiente di scripting, sono necessari tre componenti ADO: **Connection**, **Command** e **Recordset**. **L'oggetto Connection** consente di specificare il nome del provider, le credenziali alternative, se applicabile, e altri flag. **L'oggetto Command** consente di specificare le preferenze di ricerca e la stringa di query. È necessario associare **l'oggetto Connection** a un **oggetto Command** prima dell'esecuzione della query. Infine, **l'oggetto Recordset** viene usato per scorrere il set di risultati.

ADSI supporta due tipi di stringhe di query o dialetti. Nell'esempio di codice precedente viene utilizzato SQL dialetto. È anche possibile usare il dialetto LDAP. La stringa di query del dialetto LDAP è basata su [RFC 2254](https://www.ietf.org/rfc/rfc2254.txt) (una RFC è un documento Request For Comments, che è la base per lo sviluppo di standard LDAP). L'esempio precedente può essere convertito nell'esempio di codice seguente.


```VB
oCommand1.CommandText = "<LDAP://DC=fabrikam,DC=COM>;" & _
"(&(objectCategory=Person)" & _
"(objectClass=user)" & _
"(title=ProgramManager)" & _
"(department=101));" & _
"name,telephoneNumber;subTree"
```



Perché la parola "sottoalbero" è alla fine della stringa? Nel mondo della directory è possibile specificare l'ambito della ricerca. Le opzioni disponibili sono: "base", "onelevel" e "sottoalbero". "base" viene usato per leggere l'oggetto stesso; "onelevel" si riferisce agli elementi figlio immediati, in modo simile al **comando dir.** "sottoalbero" viene usato per cercare in profondità o in basso più livelli (simile a **dir /s).**

Con il SQL dialetto, è possibile specificare l'ambito nella proprietà del comando, ad esempio nell'esempio di codice seguente.


```VB
oCommand1.Properties("SearchScope") = ADS_SCOPE_ONELEVEL
```



Se l'ambito non è specificato, per impostazione predefinita usa una ricerca nel sottoalbero.

> [!Note]  
> Se si usa C++, è possibile usare [**l'interfaccia IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) da ADSI.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riorganizzazione](reorganization.md)
</dt> </dl>

 

 




