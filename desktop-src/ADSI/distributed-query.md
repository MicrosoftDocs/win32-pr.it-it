---
title: Query distribuite
description: Poiché ADSI è un OLE DB, può partecipare a Distributed Query introdotta in Microsoft SQL Server 7.0.
ms.assetid: 0a93ec2e-397a-47f7-b00c-f0f9aaa06de6
ms.tgt_platform: multiple
keywords:
- query ADSI , query distribuite
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b46ab174565d8a02ae9058792aa36ef7c3379453e0ba0f861cddf150abf662c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118428702"
---
# <a name="distributed-query"></a>Query distribuite

Poiché ADSI è un OLE DB, può partecipare a Distributed Query introdotta in Microsoft SQL Server 7.0. Di seguito sono riportati i possibili scenari:

-   Unione di oggetti Active Directory con SQL Server dati.
-   Aggiornamento SQL dati da oggetti di Active Directory.
-   Creazione di join a tre o quattro elementi con altri OLE DB provider. Ad esempio, Index Server, SQL Server e Active Directory.

Il provider OLE DB supporta due dialetti di comando, LDAP e SQL, per accedere al servizio directory e restituire i risultati in un formato tabulare su cui è possibile eseguire query SQL Server query distribuite.

**Per avviare l'SQL Query Analyzer**

1.  Aprire prima di tutto [SQL Query Analyzer](https://msdn.microsoft.com/library/Aa216983.aspx) nel SQL Server collegato al servizio directory (vedere Creazione di un server collegato).
2.  Eseguire **l'SQL Query Analyzer** (Avviare \| programmi Microsoft SQL Server \| 7.0)
3.  Accedere al computer SQL Server locale.
4.  Immettere la SQL query nel riquadro Editor della finestra della query.
5.  Eseguire la query premendo F5.

Le sezioni seguenti forniscono informazioni più dettagliate:

-   [Creazione di un server collegato](#creating-a-linked-server)
-   [Creazione di un SQL Server di accesso autenticato](#creating-a-sql-server-authenticated-login)
-   [Esecuzione di query sul servizio directory](#querying-the-directory-service)

## <a name="creating-a-linked-server"></a>Creazione di un server collegato

Per configurare un join distribuito in un Windows directory di 2000 Server, creare un server collegato. A tale scopo, configurare il mapping ADSI usando la stored procedure di sistema [ \_ sp addlinkedserver.](https://msdn.microsoft.com/library/Aa259589.aspx) Questa procedura collega un nome a un OLE DB provider.

Nell'esempio seguente vengono usati diversi argomenti con la stored procedure di sistema [ \_ sp addlinkedserver](https://msdn.microsoft.com/library/Aa259589.aspx) :

-   "ADSI" è l'argomento **del server** e sarà il nome del server collegato.
-   "Active Directory Services 2.5" è l'argomento **srvproduct,** ovvero il nome dell'origine dati OLE DB da aggiungere come server collegato.
-   "ADSDSOObject" è **l'argomento del nome \_ del provider.**
-   "adsdatasource" è l'argomento **\_ dell'origine** dati, ovvero il nome dell'origine dati interpretato dal provider OLE DB dati.

Il [comando EXEC](https://msdn.microsoft.com/library/Aa258848.aspx) viene usato per eseguire stored procedure di sistema.


```sql
EXEC sp_addlinkedserver 'ADSI', 'Active Directory Services 2.5', 
'ADSDSOObject', 'adsdatasource'
GO
```



Per Windows di accesso autenticati, il mapping automatico è sufficiente per accedere alla directory con SQL Server di sicurezza. Poiché il mapping automatico viene creato per impostazione predefinita per i server collegati creati tramite [sp \_ addlinkedserver](https://msdn.microsoft.com/library/Aa259589.aspx), non sono necessari altri mapping degli account di accesso.

Per SQL Server gli account di accesso autenticati, è possibile configurare account di accesso e password adatti per la connessione al servizio directory usando la stored procedure di sistema [sp \_ addlinkedsrvlogin.](https://msdn.microsoft.com/library/Aa259581.aspx)

> [!Note]  
> Se possibile, usare l'autenticazione di Windows.

 

## <a name="creating-a-sql-server-authenticated-login"></a>Creazione di un SQL Server di accesso autenticato

Se si preferisce usare un account di accesso autenticato SQL Server anziché l'autenticazione Windows, aggiungere un account di accesso al server collegato (vedere la sezione precedente). A tale scopo, usare la stored procedure di sistema [ \_ sp addlinkedsrvlogin.](https://msdn.microsoft.com/library/Aa259581.aspx)

Nell'esempio seguente vengono usati diversi argomenti con la stored procedure di sistema [ \_ sp addlinkedsrvlogin:](https://msdn.microsoft.com/library/Aa259581.aspx)

-   "ADSI" è **l'argomento rmtsvrname,** ovvero il nome del server collegato creato nell'esempio precedente.
-   "Fabrikam \\ Administrator" è l'argomento **locallogin,** ovvero l'account di accesso nel server locale e può essere l'account di accesso SQL Server o un Windows NT utente.
-   "CN=Administrator,OU=Sales,DC=activeds,DC=Fabrikam,DC=com" è l'argomento **rmtuser,** ovvero il nome utente che si usa per connettersi perché **useself** è **false.**
-   "secret \* \* 2000" è **rmtpassword**, ovvero la password associata a **rmtuser**

Il [comando EXEC](https://msdn.microsoft.com/library/Aa258848.aspx) viene usato per eseguire stored procedure di sistema.


```sql
EXEC sp_addlinkedsrvlogin 'ADSI', false, 'Fabrikam\Administrator', 
'CN=Administrator,OU=Sales,DC=activeds,DC=Fabrikam,DC=com', 'secret**2000'
```



## <a name="querying-the-directory-service"></a>Esecuzione di query sul servizio directory

Dopo aver creato un server collegato, usare [un'istruzione OPENQUERY](https://msdn.microsoft.com/library/Aa276848.aspx) per inviare una query al servizio directory. La query SQL seguente crea una tabella virtuale per contenere i risultati della query usando [l'istruzione CREATE](https://msdn.microsoft.com/library/Aa258253.aspx) VIEW. La vista creata è denominata "viewADContacts".

La prima [istruzione SELECT](https://msdn.microsoft.com/library/Aa259187.aspx) definisce le informazioni su cui viene eseguita la query dal servizio directory ed esegue il mapping a una colonna della tabella. Le informazioni racchiuse tra parentesi indicano i dati inseriti nella tabella virtuale. Le informazioni non racchiuse tra parentesi indicano i dati recuperati dal servizio directory. Si noti che le informazioni recuperate dal servizio directory devono essere referenziate dal relativo nome visualizzato LDAP.

L'istruzione successiva è [l'istruzione OPENQUERY.](https://msdn.microsoft.com/library/Aa276848.aspx) Questa istruzione ha due argomenti: ADSI, ovvero il nome del server collegato creato, e un'istruzione di query. L'istruzione di query contiene gli elementi seguenti:

-   [L'istruzione SELECT](https://msdn.microsoft.com/library/Aa259187.aspx) contiene l'elenco di dati che verranno ottenuti dal servizio directory. È necessario usare il nome visualizzato LDAP per indicare i dati da cercare.
-   [L'istruzione FROM](https://msdn.microsoft.com/library/Aa258869.aspx) contiene il nome del server di directory collegato da cui verranno ottenute queste informazioni.
-   [L'istruzione WHERE](https://msdn.microsoft.com/library/Aa260674.aspx) fornisce le condizioni di ricerca. In questo esempio viene eseguita la ricerca di contatti.

[L'istruzione SELECT](https://msdn.microsoft.com/library/Aa259187.aspx) finale viene usata per raccogliere i risultati dalla visualizzazione da visualizzare.


```sql
CREATE VIEW viewADContacts
AS
SELECT  [Name], sn [Last Name], street [Street], l [City], st [State]
FROM OPENQUERY( ADSI, 
     'SELECT name, sn, street, l, st
      FROM 'LDAP:// OU=Sales,DC=activeds,DC=Fabrikam,DC=Com'
      WHERE objectCategory='Person' AND 
      objectClass = 'contact'')
GO
SELECT * FROM viewADContacts
```



 

 




