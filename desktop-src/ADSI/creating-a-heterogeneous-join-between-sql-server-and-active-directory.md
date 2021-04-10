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
# <a name="creating-a-heterogeneous-join-between-sql-server--active-directory"></a><span data-ttu-id="e0df3-103">Creazione di un join eterogeneo tra SQL Server & Active Directory</span><span class="sxs-lookup"><span data-stu-id="e0df3-103">Creating a Heterogeneous Join between SQL Server & Active Directory</span></span>

<span data-ttu-id="e0df3-104">Tutti i dipendenti di Fabrikam Corporation vengono esaminati ogni sei mesi.</span><span class="sxs-lookup"><span data-stu-id="e0df3-104">All employees at the Fabrikam corporation are reviewed every six months.</span></span> <span data-ttu-id="e0df3-105">Le classificazioni delle verifiche sono archiviate nel database delle risorse umane in SQL Server.</span><span class="sxs-lookup"><span data-stu-id="e0df3-105">Review ratings are stored in the Human Resource database in SQL Server.</span></span> <span data-ttu-id="e0df3-106">Per creare una vista dei dati, Joe worden, l'amministratore dell'organizzazione, deve prima creare una tabella di revisione delle prestazioni dei dipendenti.</span><span class="sxs-lookup"><span data-stu-id="e0df3-106">To create a view of this data, Joe Worden, the enterprise administrator, must first create an employee performance review table.</span></span>

<span data-ttu-id="e0df3-107">In SQL Query Analyzer, Joe creerà una tabella denominata EMP Review che conterrà \_ tre colonne per contenere il nome del dipendente, la data della revisione e la classificazione ricevuta dal dipendente.</span><span class="sxs-lookup"><span data-stu-id="e0df3-107">In the SQL Query Analyzer, Joe is going to create a table called EMP\_REVIEW that will contain three columns to hold the name of the employee, the date of the review, and the rating that the employee received.</span></span>


```sql
CREATE TABLE EMP_REVIEW
(
userName varChar(40),
reviewDate datetime,
rating decimal 
)
```



<span data-ttu-id="e0df3-108">Joe può quindi inserire alcuni record.</span><span class="sxs-lookup"><span data-stu-id="e0df3-108">Joe can then insert a few records.</span></span>


```sql
INSERT EMP_REVIEW VALUES('Julie Adam', '2/15/1999', 4 )
INSERT EMP_REVIEW VALUES('Julie Bankert', '7/15/1999', 5 )
INSERT EMP_REVIEW VALUES('Chris Gray', '2/15/1999', 3 )
INSERT EMP_REVIEW VALUES('Chris Gray', '7/15/1999', 4 )
```



<span data-ttu-id="e0df3-109">Ora Joe può unire gli oggetti Active Directory utente alla tabella SQL Server.</span><span class="sxs-lookup"><span data-stu-id="e0df3-109">Now Joe can join the Active Directory user objects to the SQL Server table.</span></span>

<span data-ttu-id="e0df3-110">In questo esempio, l'istruzione [Select](https://msdn.microsoft.com/library/Aa259187.aspx) contiene l'elenco dei dati che verranno ottenuti dal servizio directory e SQL Server.</span><span class="sxs-lookup"><span data-stu-id="e0df3-110">In this example, the [SELECT](https://msdn.microsoft.com/library/Aa259187.aspx) statement contains the list of data that will be obtained from the directory service and SQL Server.</span></span> <span data-ttu-id="e0df3-111">L'istruzione [from](https://msdn.microsoft.com/library/Aa258869.aspx) contiene il nome del server di directory collegato da cui verranno ottenute queste informazioni, in questo caso viewADUsers.</span><span class="sxs-lookup"><span data-stu-id="e0df3-111">The [FROM](https://msdn.microsoft.com/library/Aa258869.aspx) statement contains the name of the linked directory server where this information will be obtained from, in this case, viewADUsers.</span></span> <span data-ttu-id="e0df3-112">L'istruzione [where](https://msdn.microsoft.com/library/Aa260674.aspx) fornisce le condizioni di ricerca.</span><span class="sxs-lookup"><span data-stu-id="e0df3-112">The [WHERE](https://msdn.microsoft.com/library/Aa260674.aspx) statement provides the search conditions.</span></span> <span data-ttu-id="e0df3-113">In questo esempio, esegue una ricerca in base al nome nel servizio directory, che è impostato sul nome utente SQL immesso nell'attività precedente.</span><span class="sxs-lookup"><span data-stu-id="e0df3-113">In this example, it is searching by the name in the directory service, which is set to the SQL userName entered in the previous task.</span></span>


```sql
SELECT ADsPath, userName, title, ReviewDate, Rating 
FROM EMP_REVIEW, viewADUsers
WHERE userName = Name
```



<span data-ttu-id="e0df3-114">Il comando precedente ottiene il risultato da SQL Server e Active Directory.</span><span class="sxs-lookup"><span data-stu-id="e0df3-114">The previous command gets the result from both SQL Server and Active Directory.</span></span> <span data-ttu-id="e0df3-115">AdsPath e title sono da Active Directory, mentre userName, ReviewDate e rating sono della tabella SQL.</span><span class="sxs-lookup"><span data-stu-id="e0df3-115">AdsPath and title are from Active Directory, whereas userName, ReviewDate, and Rating are from the SQL table.</span></span> <span data-ttu-id="e0df3-116">Può anche creare un'altra visualizzazione per questo join.</span><span class="sxs-lookup"><span data-stu-id="e0df3-116">He can even create another view for this join.</span></span>


```sql
CREATE VIEW reviewReport
AS
SELECT ADsPath, userName, title, ReviewDate, Rating 
FROM EMP_REVIEW, viewADUsers
WHERE userName = Name
GO
SELECT * FROM reviewReport
```



 

 




