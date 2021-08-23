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
ms.openlocfilehash: 0c231d3c4d619775cca2ed9542733bff51219d92ff31d922f6d38ea7b1bcd2e4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119509981"
---
# <a name="ldap-dialect"></a>Dialetto LDAP

Il dialetto LDAP è un formato per le istruzioni di query che usano la [sintassi](search-filter-syntax.md)del filtro di ricerca LDAP . Usare un'istruzione di query LDAP con le interfacce di ricerca ADSI seguenti:

-   Le [ActiveX data object (ADO),](searching-with-activex-data-objects-ado.md) ovvero le interfacce di Automazione che usano OLE DB.
-   [OLE DB](searching-with-ole-db.md), che è un set di interfacce C/C++ per l'esecuzione di query su database.
-   [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch), ovvero l'interfaccia C/C++ per Active Directory.

Una stringa di dialetto LDAP è costituita da quattro parti separate da punti e virgola (;).

-   Nome distinto di base. Esempio:

    ```VB
    <LDAP://DC=Fabrikam,DC=COM>
    ```

    

-   Filtri di ricerca LDAP. Per altre informazioni sui filtri di ricerca, vedere [Sintassi del filtro di ricerca](search-filter-syntax.md).
-   Nome visualizzato LDAP degli attributi da recuperare. Più attributi sono separati da una virgola.
-   Specifica l'ambito della ricerca. I valori validi sono "base", "onelevel" e "subtree". L'ambito specificato in una stringa di query LDAP esegue l'override di qualsiasi ambito di ricerca specificato con la proprietà "SearchScope" dell'oggetto COMMAND ADO.

Di seguito è riportato un esempio di codice del dialetto LDAP in ADSI che cerca tutti gli oggetti nel sottoalbero.


```VB
"<LDAP://DC=Fabrikam,DC=com>;(objectClass=*);AdsPath, cn;subTree"
```



Non tutte le opzioni di ricerca ,ad esempio le dimensioni della pagina di ricerca, possono essere espresse nel dialetto LDAP, pertanto è necessario impostare le opzioni prima dell'avvio dell'esecuzione effettiva della query.

## <a name="example-code-for-performing-an-ldap-query"></a>Codice di esempio per l'esecuzione di una query LDAP

L'esempio di codice seguente illustra come usare una query LDAP


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



Per informazioni dettagliate sulla sintassi della query, vedere [Sintassi del filtro di ricerca](search-filter-syntax.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sintassi del filtro di ricerca](search-filter-syntax.md)
</dt> <dt>

[SQL dialetto](sql-dialect.md)
</dt> <dt>

[Ricerca con l'interfaccia IDirectorySearch](searching-with-idirectorysearch.md)
</dt> <dt>

[Ricerca con oggetti ActiveX dati](searching-with-activex-data-objects-ado.md)
</dt> <dt>

[Ricerca con OLE DB](searching-with-ole-db.md)
</dt> </dl>

 

 




