---
title: Query distribuite
description: Poiché ADSI è un provider di OLE DB, può partecipare alla query distribuita introdotta in Microsoft SQL Server 7,0.
ms.assetid: 0a93ec2e-397a-47f7-b00c-f0f9aaa06de6
ms.tgt_platform: multiple
keywords:
- query ADSI, query distribuite
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8675f0a5ba9faa6ece78783eb4f61f17aafabc8
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/20/2020
ms.locfileid: "106299453"
---
# <a name="distributed-query"></a>Query distribuite

Poiché ADSI è un provider di OLE DB, può partecipare alla query distribuita introdotta in Microsoft SQL Server 7,0. Gli scenari possibili sono i seguenti:

-   Unione di Active Directory oggetti con dati SQL Server.
-   Aggiornamento dei dati SQL da oggetti Active Directory.
-   Creazione di join a tre vie o a quattro vie con altri provider di OLE DB. Ad esempio, index server, SQL Server e Active Directory.

Il provider OLE DB supporta due dialetti dei comandi, LDAP e SQL, per accedere al servizio directory e restituire i risultati in un formato tabulare su cui è possibile eseguire query con SQL Server query distribuite.

**Per avviare SQL Query Analyzer**

1.  Per prima cosa, aprire [SQL Query Analyzer](https://msdn.microsoft.com/library/Aa216983.aspx) nel SQL Server collegato al servizio directory (vedere Creazione di un server collegato).
2.  Eseguire **SQL Query Analyzer** (avvia \| programmi \| Microsoft SQL Server 7,0)
3.  Accedere al computer SQL Server.
4.  Immettere la query SQL nel riquadro Editor della finestra query.
5.  Eseguire la query premendo F5.

Le sezioni seguenti forniscono maggiori dettagli:

-   [Creazione di un server collegato](#creating-a-linked-server)
-   [Creazione di un account di accesso con autenticazione SQL Server](#creating-a-sql-server-authenticated-login)
-   [Esecuzione di query sul servizio directory](#querying-the-directory-service)

## <a name="creating-a-linked-server"></a>Creazione di un server collegato

Per configurare un join distribuito in un servizio directory di Windows Server 2000, creare un server collegato. A tale scopo, configurare il mapping ADSI utilizzando la stored procedure di sistema [SP \_ addlinkedserver](https://msdn.microsoft.com/library/Aa259589.aspx) . Questa procedura collega un nome a un nome di provider OLE DB.

Nell'esempio seguente si noti che esistono diversi argomenti utilizzati con la stored procedure di sistema [SP \_ addlinkedserver](https://msdn.microsoft.com/library/Aa259589.aspx) :

-   "ADSI" è l'argomento del **Server** e sarà il nome del server collegato.
-   "Active Directory Services 2,5" è l'argomento **srvproduct** , ovvero il nome dell'origine dati OLE DB che si sta aggiungendo come server collegato.
-   "ADSDSOObject" è l'argomento del **\_ nome del provider** .
-   "adsdatasource" è l'argomento dell' **\_ origine dati** , ovvero il nome dell'origine dati interpretato dal provider OLE DB.

Il comando [Exec](https://msdn.microsoft.com/library/Aa258848.aspx) viene utilizzato per eseguire stored procedure di sistema.


```sql
EXEC sp_addlinkedserver 'ADSI', 'Active Directory Services 2.5', 
'ADSDSOObject', 'adsdatasource'
GO
```



Per gli account di accesso con autenticazione di Windows, il mapping automatico è sufficiente per accedere alla directory con SQL Server delega di sicurezza. Poiché per impostazione predefinita il mapping automatico viene creato per i server collegati creati tramite [SP \_ addlinkedserver](https://msdn.microsoft.com/library/Aa259589.aspx), non è necessario alcun altro mapping degli account di accesso.

Per gli account di accesso con autenticazione SQL Server, è possibile configurare account di accesso e password appropriati per la connessione al servizio directory tramite la stored procedure di sistema [SP \_ addlinkedsrvlogin](https://msdn.microsoft.com/library/Aa259581.aspx) .

> [!Note]  
> Se possibile, usare l'autenticazione di Windows.

 

## <a name="creating-a-sql-server-authenticated-login"></a>Creazione di un account di accesso con autenticazione SQL Server

Se si preferisce usare un account di accesso con autenticazione SQL Server anziché l'autenticazione di Windows, aggiungere un account di accesso al server collegato. vedere la sezione precedente. A tale scopo, usare la stored procedure di sistema [SP \_ addlinkedsrvlogin](https://msdn.microsoft.com/library/Aa259581.aspx) .

Nell'esempio seguente sono presenti diversi argomenti usati con la stored procedure di sistema [SP \_ addlinkedsrvlogin](https://msdn.microsoft.com/library/Aa259581.aspx) :

-   "ADSI" è l'argomento **rmtsvrname** , ovvero il nome del server collegato creato nell'esempio precedente.
-   " \\ Amministratore Fabrikam" è l'argomento **locallogin** , che è l'account di accesso nel server locale e può essere il SQL Server account di accesso o un utente di Windows NT.
-   "CN = Administrator, OU = Sales, DC = activeds, DC = Fabrikam, DC = com" è l'argomento **rmtuser** , che corrisponde al nome utente usato per la connessione perché **useself** è **false**.
-   "Secret \* \* 2000" è **rmtpassword**, che è la password associata a **rmtuser**

Il comando [Exec](https://msdn.microsoft.com/library/Aa258848.aspx) viene utilizzato per eseguire stored procedure di sistema.


```sql
EXEC sp_addlinkedsrvlogin 'ADSI', false, 'Fabrikam\Administrator', 
'CN=Administrator,OU=Sales,DC=activeds,DC=Fabrikam,DC=com', 'secret**2000'
```



## <a name="querying-the-directory-service"></a>Esecuzione di query sul servizio directory

Dopo aver creato un server collegato, usare un'istruzione [OPENQUERY](https://msdn.microsoft.com/library/Aa276848.aspx) per inviare una query al servizio directory. La query SQL seguente crea una tabella virtuale in cui conservare i risultati della query utilizzando l'istruzione [Create View](https://msdn.microsoft.com/library/Aa258253.aspx) . La vista creata è denominata "viewADContacts".

La prima istruzione [Select](https://msdn.microsoft.com/library/Aa259187.aspx) definisce le informazioni su cui viene eseguita una query dal servizio directory e ne esegue il mapping a una colonna della tabella. Le informazioni racchiuse tra parentesi quadre indicano i dati inseriti nella tabella virtuale. Le informazioni non tra parentesi quadre indicano i dati recuperati dal servizio directory. Si noti che è necessario fare riferimento alle informazioni recuperate dal servizio directory tramite il relativo nome visualizzato LDAP.

L'istruzione successiva è l'istruzione [OPENQUERY](https://msdn.microsoft.com/library/Aa276848.aspx) . Questa istruzione ha due argomenti: ADSI, ovvero il nome del server collegato creato e un'istruzione di query. L'istruzione di query contiene gli elementi seguenti:

-   L'istruzione [Select](https://msdn.microsoft.com/library/Aa259187.aspx) contiene l'elenco dei dati che verranno ottenuti dal servizio directory. È necessario usare il nome visualizzato LDAP per indicare i dati che si stanno cercando.
-   L'istruzione [from](https://msdn.microsoft.com/library/Aa258869.aspx) contiene il nome del server di directory collegato da cui verranno ottenute queste informazioni.
-   L'istruzione [where](https://msdn.microsoft.com/library/Aa260674.aspx) fornisce le condizioni di ricerca. In questo esempio è in corso la ricerca di contatti.

L'istruzione [Select](https://msdn.microsoft.com/library/Aa259187.aspx) finale viene utilizzata per prelevare i risultati dalla visualizzazione da visualizzare.


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



 

 




