---
title: Sottolinguaggio SQL
description: Il sottolinguaggio SQL, derivato dalla Structured Query Language, usa espressioni leggibili per definire istruzioni di query.
ms.assetid: c1032268-e0f5-4d74-ab72-864cdd36851d
ms.tgt_platform: multiple
keywords:
- Linguaggio ADSI SQL
- dialetto ADSI, sottolinguaggio SQL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b0936a54bc7bd0028717967ce779fe2f2048a33
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297648"
---
# <a name="sql-dialect"></a>Sottolinguaggio SQL

Il sottolinguaggio SQL, derivato dalla Structured Query Language, usa espressioni leggibili per definire istruzioni di query. Utilizzare un'istruzione di query SQL con le interfacce di ricerca ADSI seguenti:

-   Le interfacce [ADO (ActiveX Data Object)](searching-with-activex-data-objects-ado.md) , ovvero interfacce di automazione che utilizzano OLE DB.
-   [OLE DB](searching-with-ole-db.md), ovvero un set di interfacce C/C++ per l'esecuzione di query sui database.

Le istruzioni SQL richiedono la sintassi seguente.


```sql
SELECT [ALL] * | select-list FROM 'ADsPath' [WHERE search-condition] [ORDER BY sort-list]
```



Nella tabella seguente sono elencate le parole chiave dell'istruzione di query SQL.



| Parola chiave  | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SELECT   | Specifica un elenco delimitato da virgole di attributi da recuperare per ogni oggetto. Se si specifica \* , la query recupera solo il ADsPath di ogni oggetto.                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| FROM     | Specifica il ADsPath della base della ricerca. Ad esempio, il ADsPath del contenitore degli utenti in un dominio Active Directory potrebbe essere ' LDAP://CN = Users, DC = Fabrikam, DC = COM '. Tenere presente che il percorso è racchiuso tra virgolette singole (').                                                                                                                                                                                                                                                                                                                                                    |
| WHERE    | Parola chiave facoltativa che specifica il filtro per la query.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| ORDER BY | Parola chiave facoltativa che genera un ordinamento sul lato server se il server supporta il controllo di ordinamento LDAP. Active Directory supporta il controllo di ordinamento, ma può influisca sulle prestazioni del server, in particolare se il set di risultati è di grandi dimensioni. Sort-list è un elenco delimitato da virgole di attributi su cui eseguire l'ordinamento. Tenere presente che Active Directory supporta solo una singola chiave di ordinamento. È possibile usare le parole chiave ASC e DESC facoltative per specificare l'ordinamento crescente o decrescente. il valore predefinito è Ascending. La parola chiave ORDER BY esegue l'override di qualsiasi chiave di ordinamento specificata con la proprietà "Sort on" dell'oggetto comando ADO. |



 

> [!Note]  
> Nei casi in cui viene utilizzato un set di caratteri MultiByte, se la ricerca viene eseguita da ADO con il sottolinguaggio SQL, non è possibile utilizzare una barra rovesciata per eseguire il escape dei caratteri. Al contrario, è necessario usare le sequenze di escape elencate in [caratteri speciali](search-filter-syntax.md) . Ad esempio, per un'istruzione che usava la sintassi "samAccountName = \( test", che usa la barra rovesciata " \\ ", per eseguire l'escape della parentesi di apertura "(", invece, sostituire la barra rovesciata con il carattere speciale " \\ 28", come segue: "sAMAccountName = \\ 28Test".

 

Le istruzioni di query seguenti sono esempi di sottolinguaggio SQL in ADSI.

Per cercare tutti gli oggetti gruppo.


```sql
SELECT ADsPath, cn FROM 'LDAP://DC=Fabrikam,DC=COM' WHERE objectCategory='group'
```



Per cercare tutti gli utenti il cui cognome inizia con la lettera H.


```sql
SELECT ADsPath, cn FROM 'LDAP://OU=Sales,DC=Fabrikam,DC=COM' WHERE objectCategory='person' AND objectClass='user' AND sn = 'H*' ORDER BY sn
```



La grammatica formale per le query SQL è definita nell'esempio di codice seguente. Tutte le parole chiave non fanno distinzione tra maiuscole e minuscole.


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



I join interni di SQL non sono supportati dal provider Active Directory OLE DB, ma è possibile usare SQL per aggiungere dati SQL e Active Directory. Per ulteriori informazioni, vedere [creazione di un join eterogeneo tra SQL Server e Active Directory](creating-a-heterogeneous-join-between-sql-server-and-active-directory.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sintassi del filtro di ricerca](search-filter-syntax.md)
</dt> <dt>

[Dialetto LDAP](ldap-dialect.md)
</dt> <dt>

[Ricerca con l'interfaccia IDirectorySearch](searching-with-idirectorysearch.md)
</dt> <dt>

[Ricerca con ActiveX Data Objects](searching-with-activex-data-objects-ado.md)
</dt> <dt>

[Ricerca con OLE DB](searching-with-ole-db.md)
</dt> </dl>

 

 




