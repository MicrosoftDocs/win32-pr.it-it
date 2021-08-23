---
title: SQL Dialetto
description: Il SQL dialetto, derivato dal Structured Query Language, usa espressioni leggibili per definire le istruzioni di query.
ms.assetid: c1032268-e0f5-4d74-ab72-864cdd36851d
ms.tgt_platform: multiple
keywords:
- SQL Dialetto ADSI
- dialetto ADSI , SQL dialetto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7483a5e3785f410e6c2fd875122ba24618a82b70d1ed6dc9a85105ae4e8dcfa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119262051"
---
# <a name="sql-dialect"></a>SQL Dialetto

Il SQL dialetto, derivato dal Structured Query Language, usa espressioni leggibili per definire le istruzioni di query. Usare un SQL di query con le interfacce di ricerca ADSI seguenti:

-   Le [ActiveX ADO (Data Object),](searching-with-activex-data-objects-ado.md) ovvero interfacce di automazione che usano OLE DB.
-   [OLE DB](searching-with-ole-db.md), ovvero un set di interfacce C/C++ per l'esecuzione di query su database.

SQL istruzioni richiedono la sintassi seguente.


```sql
SELECT [ALL] * | select-list FROM 'ADsPath' [WHERE search-condition] [ORDER BY sort-list]
```



Nella tabella seguente sono elencate le SQL delle istruzioni di query.



| Parola chiave  | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SELECT   | Specifica un elenco delimitato da virgole di attributi da recuperare per ogni oggetto. Se si specifica \* , la query recupera solo l'ADsPath di ogni oggetto.                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| FROM     | Specifica il valore ADsPath della base della ricerca. Ad esempio, il percorso ADsPath del contenitore Users in un dominio di Active Directory potrebbe essere "LDAP://CN=Users,DC=Fabrikam,DC=COM". Tenere presente che il percorso è racchiuso tra una coppia di virgolette singole (').                                                                                                                                                                                                                                                                                                                                                    |
| WHERE    | Parola chiave facoltativa che specifica il filtro di query.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| ORDER BY | Parola chiave facoltativa che genera un ordinamento lato server se il server supporta il controllo di ordinamento LDAP. Active Directory supporta il controllo di ordinamento, ma può influire sulle prestazioni del server, in particolare se il set di risultati è di grandi dimensioni. L'elenco di ordinamento è un elenco delimitato da virgole di attributi in base ai quali eseguire l'ordinamento. Tenere presente che Active Directory supporta solo una singola chiave di ordinamento. È possibile usare le parole chiave facoltative ASC e DESC per specificare l'ordinamento crescente o decrescente. il valore predefinito è crescente. La parola chiave ORDER BY esegue l'override di qualsiasi chiave di ordinamento specificata con la proprietà "Sort on" dell'oggetto ADO Command. |



 

> [!Note]  
> Nei casi in cui viene usato un set di caratteri multibyte, se la ricerca viene eseguita da ADO con il dialetto SQL, non è possibile usare una barra rovesciata per i caratteri di escape. È invece necessario usare le sequenze di escape [elencate](search-filter-syntax.md) in Caratteri speciali. Ad esempio, per un'istruzione che usa la sintassi "samAccountName= Test", che usa la barra rovesciata, " ", per eseguire l'escape della parentesi aperta, "(", sostituire invece la barra rovesciata con il carattere speciale " 28", come indicato di \( \\ \\ seguito: "samAccountName= \\ 28Test".

 

Le istruzioni di query seguenti sono esempi di SQL dialetto in ADSI.

Per cercare tutti gli oggetti gruppo.


```sql
SELECT ADsPath, cn FROM 'LDAP://DC=Fabrikam,DC=COM' WHERE objectCategory='group'
```



Per cercare tutti gli utenti il cui cognome inizia con la lettera H.


```sql
SELECT ADsPath, cn FROM 'LDAP://OU=Sales,DC=Fabrikam,DC=COM' WHERE objectCategory='person' AND objectClass='user' AND sn = 'H*' ORDER BY sn
```



La grammatica formale per SQL query è definita nell'esempio di codice seguente. Per tutte le parole chiave non viene fatto distinzione tra maiuscole e minuscole.


```sql
statement ::= select-statement
select-statement ::= SELECT [ALL] select-list FROM table-identifier [WHERE search-condition] [ORDER BY sort-list]
select-list ::= * | select-sublist [, select-sublist]... 
select-sublist ::= column-identifier
column-identifier ::= user-defined-name 
table-identifier ::= string-literal
search-condition ::= boolean-term [OR search-condition]
sort-list ::= column-identifier [ASC | DESC] [,column-identifier [ASC | DESC]]... 
boolean-term ::= boolean-factor [AND boolean-term]
boolean-factor ::= [NOT] boolean-primary
boolean-primary ::= comparison-predicate | (search-condition)
comparison-predicate ::= column-identifier comparison-operator literal
comparison-operator ::= < | > | <= | >= | = | <>
user-defined-name ::= letter [letter | digit]...
literal ::= string-literal | numeric-literal | boolean-literal 
string-literal ::= '{character}...' (Any sequence of characters delimited by quotes)
numeric-literal ::= digits [fraction] [exponent]
digits ::= digit [digit]...
fraction ::= . digits 
exponent ::= E digits
boolean-literal ::= TRUE | FALSE | YES | NO | ON | OFF
```



SQL inner join non sono supportati dal provider di Active Directory OLE DB, ma è possibile usare SQL per aggiungere SQL dati di Active Directory. Per altre informazioni, vedere [Creazione di un join eterogeneo](creating-a-heterogeneous-join-between-sql-server-and-active-directory.md)tra SQL Server e Active Directory.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sintassi del filtro di ricerca](search-filter-syntax.md)
</dt> <dt>

[Dialetto LDAP](ldap-dialect.md)
</dt> <dt>

[Ricerca con l'interfaccia IDirectorySearch](searching-with-idirectorysearch.md)
</dt> <dt>

[Ricerca con oggetti ActiveX dati](searching-with-activex-data-objects-ado.md)
</dt> <dt>

[Ricerca con OLE DB](searching-with-ole-db.md)
</dt> </dl>

 

 




