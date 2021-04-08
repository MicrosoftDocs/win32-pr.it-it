---
title: Dialetto LDAP
description: Il dialetto LDAP è un formato per le istruzioni di query che usano la sintassi del filtro di ricerca LDAP.
ms.assetid: 29aca7e6-3ed5-4efd-8b03-6a2ee0571f1f
ms.tgt_platform: multiple
keywords:
- ADSI dialetto LDAP
- dialetti ADSI, dialetto LDAP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15f7d1f65a41655596d0a14cf6e2a3595916c2cc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855289"
---
# <a name="ldap-dialect"></a>Dialetto LDAP

Il dialetto LDAP è un formato per le istruzioni di query che usano la [sintassi del filtro di ricerca LDAP](search-filter-syntax.md). Usare un'istruzione di query LDAP con le interfacce di ricerca ADSI seguenti:

-   Le interfacce [ADO (ActiveX Data Object)](searching-with-activex-data-objects-ado.md) , ovvero interfacce di automazione che utilizzano OLE DB.
-   [OLE DB](searching-with-ole-db.md), ovvero un set di interfacce C/C++ per l'esecuzione di query sui database.
-   [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch), ovvero l'interfaccia C/C++ per Active Directory.

Una stringa di dialetto LDAP è costituita da quattro parti separate da punti e virgola (;).

-   Nome distinto di base. Ad esempio:

    ```VB
    <LDAP://DC=Fabrikam,DC=COM>
    ```

    

-   Filtri di ricerca LDAP. Per altre informazioni sui filtri di ricerca, vedere [sintassi del filtro di ricerca](search-filter-syntax.md).
-   Nome visualizzato LDAP degli attributi da recuperare. Più attributi sono separati da una virgola.
-   Specifica l'ambito della ricerca. I valori validi sono "base", "unlivello" e "sottoalbero". L'ambito specificato in una stringa di query LDAP sostituisce qualsiasi ambito di ricerca specificato con la proprietà "SearchScope" dell'oggetto comando ADO.

Di seguito è riportato un esempio di codice del dialetto LDAP in ADSI che cerca tutti gli oggetti nel sottoalbero.


```VB
"<LDAP://DC=Fabrikam,DC=com>;(objectClass=*);AdsPath, cn;subTree"
```



Non tutte le opzioni di ricerca (ad esempio, le dimensioni della pagina di ricerca) possono essere espresse nel dialetto LDAP, quindi è necessario impostare le opzioni prima che l'esecuzione effettiva della query venga avviata.

## <a name="example-code-for-performing-an-ldap-query"></a>Codice di esempio per l'esecuzione di una query LDAP

Nell'esempio di codice seguente viene illustrato come utilizzare una query LDAP


```VB
Dim con As New Connection, rs As New Recordset
Dim adVariant
Dim i 'Used for counter
Dim j 'Used for counter
Dim Com As New Command
Dim strDomain As String
Dim strPassword As String
 
' Open a Connection object.
con.Provider = "ADsDSOObject"
con.Properties("ADSI Flag") = 1
con.Properties("User ID") = strDomain + "\" + strUserID
con.Properties("Password") = strPassword

con.Open "Active Directory Provider"
 
' Create a command object on this connection.
Set Com.ActiveConnection = con
 
' Set the query string.
Com.CommandText = "<LDAP://MyServer/DC=MyDomain,DC=Fabrikam,DC=com>;
     (objectClass=*);ADsPath, objectclass;base"
 
' Set search preferences.
Com.Properties("Page Size") = 1000
Com.Properties("Timeout") = 30 'seconds
 
' Execute the query.
Set rs = Com.Execute
 
' Navigate the record set.
rs.MoveFirst
While Not rs.EOF
    For i = 0 To rs.Fields.Count - 1
        If rs.Fields(i).Type = adVariant And Not (IsNull(rs.Fields(i).Value)) Then
            Debug.Print rs.Fields(i).Name, " = "
            For j = LBound(rs.Fields(i).Value) To UBound(rs.Fields(i).Value)
                Debug.Print rs.Fields(i).Value(j), " # "
            Next j
        Else
            Debug.Print rs.Fields(i).Name, " = ", rs.Fields(i).Value
        End If
    Next i
    rs.MoveNext
Wend
 
rs.MoveLast
Debug.Print "No. of rows = ", rs.RecordCount
```



Per informazioni dettagliate sulla sintassi di query, vedere [sintassi del filtro di ricerca](search-filter-syntax.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sintassi del filtro di ricerca](search-filter-syntax.md)
</dt> <dt>

[Sottolinguaggio SQL](sql-dialect.md)
</dt> <dt>

[Ricerca con l'interfaccia IDirectorySearch](searching-with-idirectorysearch.md)
</dt> <dt>

[Ricerca con ActiveX Data Objects](searching-with-activex-data-objects-ado.md)
</dt> <dt>

[Ricerca con OLE DB](searching-with-ole-db.md)
</dt> </dl>

 

 




