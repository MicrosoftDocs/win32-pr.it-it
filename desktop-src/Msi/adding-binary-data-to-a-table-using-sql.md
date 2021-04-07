---
description: Non è possibile inserire dati binari in una tabella usando direttamente le query INSERT INTO o UPDATE SQL.
ms.assetid: cc055de8-eaba-48eb-a982-4d584ac7a881
title: Aggiunta di dati binari a una tabella tramite SQL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 491bfe57354b4faf9f7c385bc4e14c64ad366f1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881169"
---
# <a name="adding-binary-data-to-a-table-using-sql"></a><span data-ttu-id="8ab7c-103">Aggiunta di dati binari a una tabella tramite SQL</span><span class="sxs-lookup"><span data-stu-id="8ab7c-103">Adding Binary Data to a Table Using SQL</span></span>

<span data-ttu-id="8ab7c-104">Non è possibile inserire dati binari in una tabella usando direttamente le query INSERT INTO o UPDATE SQL.</span><span class="sxs-lookup"><span data-stu-id="8ab7c-104">Binary data cannot be inserted into a table directly using the INSERT INTO or UPDATE SQL queries.</span></span> <span data-ttu-id="8ab7c-105">Per aggiungere dati binari a una tabella, è innanzitutto necessario utilizzare il marcatore di parametro (?) nella query come segnaposto per il valore binario.</span><span class="sxs-lookup"><span data-stu-id="8ab7c-105">In order to add binary data to a table, you must first use the parameter marker (?) in the query as a placeholder for the binary value.</span></span> <span data-ttu-id="8ab7c-106">L'esecuzione della query deve includere un record contenente i dati binari in uno dei relativi campi.</span><span class="sxs-lookup"><span data-stu-id="8ab7c-106">The execution of the query should include a record that contains the binary data in one of its fields.</span></span>

<span data-ttu-id="8ab7c-107">Un marcatore è un riferimento di parametro a un valore fornito da un record inviato con la query.</span><span class="sxs-lookup"><span data-stu-id="8ab7c-107">A marker is a parameter reference to a value supplied by a record submitted with the query.</span></span> <span data-ttu-id="8ab7c-108">Viene rappresentato nell'istruzione SQL da un punto interrogativo (?).</span><span class="sxs-lookup"><span data-stu-id="8ab7c-108">It is represented in the SQL statement by a question mark (?).</span></span>

<span data-ttu-id="8ab7c-109">Il codice di esempio seguente aggiunge dati binari a una tabella.</span><span class="sxs-lookup"><span data-stu-id="8ab7c-109">The following sample code adds binary data to a table.</span></span>


```C++
#include <windows.h>
#include <Msiquery.h>
#include <tchar.h>
#pragma comment(lib, "msi.lib")


int main()  
{ 

PMSIHANDLE hDatabase = 0;
PMSIHANDLE hView = 0;
PMSIHANDLE hRec = 0;

if (ERROR_SUCCESS == MsiOpenDatabase(_T("c:\\temp\\testdb.msi"), MSIDBOPEN_TRANSACT, &hDatabase))
{
    //
    // Open view on Binary table so that we can add a new row, must use '?' to represent Binary data
    //

    if (ERROR_SUCCESS == MsiDatabaseOpenView(hDatabase, _T("INSERT INTO `Binary` (`Name`, `Data`) VALUES ('NewBlob', ?)"), &hView))
    {

        //
        // Create record with binary data in 1st field (must match up with '?' in query)
        //

        hRec = MsiCreateRecord(1);
        if (ERROR_SUCCESS == MsiRecordSetStream(hRec, 1, _T("c:\\temp\\data.bin")))
        {

            //
            // Execute view with record containing binary data value; commit database to save changes
            //

            if (ERROR_SUCCESS == MsiViewExecute(hView, hRec)
              && ERROR_SUCCESS == MsiViewClose(hView)
              && ERROR_SUCCESS == MsiDatabaseCommit(hDatabase))
            {
                //
                // New binary data successfully committed to the database
                //
            }
        }
    }
}

return 0;  
}
```



<span data-ttu-id="8ab7c-110">Lo script di esempio seguente aggiunge dati binari a una tabella.</span><span class="sxs-lookup"><span data-stu-id="8ab7c-110">The following sample script adds binary data to a table.</span></span>


```VB
Dim Installer
Dim Database
Dim View
Dim Record

Set Installer = CreateObject("WindowsInstaller.Installer")

Set Record = Installer.CreateRecord(1)
Record.SetStream 1, "c:\temp\data.bin"

Set Database = Installer.OpenDatabase("c:\temp\testdb.msi", msiOpenDatabaseModeTransact)
Set View = Database.OpenView("INSERT INTO `Binary` (`Name`, `Data`) VALUES ('NewBlob', ?)")
View.Execute Record
Database.Commit ' save changes
```



## <a name="related-topics"></a><span data-ttu-id="8ab7c-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8ab7c-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8ab7c-112">Utilizzo delle query</span><span class="sxs-lookup"><span data-stu-id="8ab7c-112">Working with Queries</span></span>](working-with-queries.md)
</dt> <dt>

[<span data-ttu-id="8ab7c-113">Sintassi SQL</span><span class="sxs-lookup"><span data-stu-id="8ab7c-113">SQL Syntax</span></span>](sql-syntax.md)
</dt> <dt>

[<span data-ttu-id="8ab7c-114">Esempi di query sul database con SQL e script</span><span class="sxs-lookup"><span data-stu-id="8ab7c-114">Examples of Database Queries Using SQL and Script</span></span>](examples-of-database-queries-using-sql-and-script.md)
</dt> </dl>

 

 



