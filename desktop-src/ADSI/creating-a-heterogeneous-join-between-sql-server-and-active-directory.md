---
title: Creazione di un join eterogeneo tra SQL Server & Active Directory
description: Tutti i dipendenti di Fabrikam Corporation vengono esaminati ogni sei mesi.
ms.assetid: 16f605ae-7f6c-4429-a379-47686618b15d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8620706db56124b83c8cd8151c067a548d5a73d557fa6523ed82167647450b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117840291"
---
# <a name="creating-a-heterogeneous-join-between-sql-server--active-directory"></a>Creazione di un join eterogeneo tra SQL Server & Active Directory

Tutti i dipendenti di Fabrikam Corporation vengono esaminati ogni sei mesi. Le classificazioni di revisione vengono archiviate nel database delle risorse umane in SQL Server. Per creare una vista di questi dati, Joe Worden, amministratore dell'organizzazione, deve prima creare una tabella di verifica delle prestazioni dei dipendenti.

In SQL Query Analyzer, Joe creerà una tabella denominata EMP REVIEW che conterrà tre colonne per contenere il nome del dipendente, la data della revisione e la valutazione ricevuta \_ dal dipendente.


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



Joe può ora unire gli oggetti utente di Active Directory alla SQL Server tabella.

In questo esempio [l'istruzione SELECT](https://msdn.microsoft.com/library/Aa259187.aspx) contiene l'elenco di dati che verranno ottenuti dal servizio directory e SQL Server. [L'istruzione FROM](https://msdn.microsoft.com/library/Aa258869.aspx) contiene il nome del server di directory collegato da cui verranno ottenute queste informazioni, in questo caso viewADUsers. [L'istruzione WHERE](https://msdn.microsoft.com/library/Aa260674.aspx) fornisce le condizioni di ricerca. In questo esempio viene eseguita la ricerca in base al nome nel servizio directory, che è impostato sul SQL userName immesso nell'attività precedente.


```sql
SELECT ADsPath, userName, title, ReviewDate, Rating 
FROM EMP_REVIEW, viewADUsers
WHERE userName = Name
```



Il comando precedente ottiene il risultato sia da SQL Server che da Active Directory. AdsPath e title derivano da Active Directory, mentre userName, ReviewDate e Rating derivano dalla SQL tabella. Può anche creare un'altra visualizzazione per questo join.


```sql
CREATE VIEW reviewReport
AS
SELECT ADsPath, userName, title, ReviewDate, Rating 
FROM EMP_REVIEW, viewADUsers
WHERE userName = Name
GO
SELECT * FROM reviewReport
```



 

 




