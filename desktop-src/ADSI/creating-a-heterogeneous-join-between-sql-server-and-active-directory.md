---
title: Creazione di un join eterogeneo tra SQL Server & Active Directory
description: Tutti i dipendenti di Fabrikam Corporation vengono esaminati ogni sei mesi.
ms.assetid: 16f605ae-7f6c-4429-a379-47686618b15d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93e4e6b7f3bfd9c853d9ff262365d49c1f3a8d5c
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/20/2020
ms.locfileid: "103956211"
---
# <a name="creating-a-heterogeneous-join-between-sql-server--active-directory"></a>Creazione di un join eterogeneo tra SQL Server & Active Directory

Tutti i dipendenti di Fabrikam Corporation vengono esaminati ogni sei mesi. Le classificazioni delle verifiche sono archiviate nel database delle risorse umane in SQL Server. Per creare una vista dei dati, Joe worden, l'amministratore dell'organizzazione, deve prima creare una tabella di revisione delle prestazioni dei dipendenti.

In SQL Query Analyzer, Joe creerà una tabella denominata EMP Review che conterrà \_ tre colonne per contenere il nome del dipendente, la data della revisione e la classificazione ricevuta dal dipendente.


```sql
CREATE TABLE EMP_REVIEW
(
userName varChar(40),
reviewDate datetime,
rating decimal 
)
```



Joe può quindi inserire alcuni record.


```sql
INSERT EMP_REVIEW VALUES('Julie Adam', '2/15/1999', 4 )
INSERT EMP_REVIEW VALUES('Julie Bankert', '7/15/1999', 5 )
INSERT EMP_REVIEW VALUES('Chris Gray', '2/15/1999', 3 )
INSERT EMP_REVIEW VALUES('Chris Gray', '7/15/1999', 4 )
```



Ora Joe può unire gli oggetti Active Directory utente alla tabella SQL Server.

In questo esempio, l'istruzione [Select](https://msdn.microsoft.com/library/Aa259187.aspx) contiene l'elenco dei dati che verranno ottenuti dal servizio directory e SQL Server. L'istruzione [from](https://msdn.microsoft.com/library/Aa258869.aspx) contiene il nome del server di directory collegato da cui verranno ottenute queste informazioni, in questo caso viewADUsers. L'istruzione [where](https://msdn.microsoft.com/library/Aa260674.aspx) fornisce le condizioni di ricerca. In questo esempio, esegue una ricerca in base al nome nel servizio directory, che è impostato sul nome utente SQL immesso nell'attività precedente.


```sql
SELECT ADsPath, userName, title, ReviewDate, Rating 
FROM EMP_REVIEW, viewADUsers
WHERE userName = Name
```



Il comando precedente ottiene il risultato da SQL Server e Active Directory. AdsPath e title sono da Active Directory, mentre userName, ReviewDate e rating sono della tabella SQL. Può anche creare un'altra visualizzazione per questo join.


```sql
CREATE VIEW reviewReport
AS
SELECT ADsPath, userName, title, ReviewDate, Rating 
FROM EMP_REVIEW, viewADUsers
WHERE userName = Name
GO
SELECT * FROM reviewReport
```



 

 




