---
description: I dati binari non possono essere inseriti direttamente in una tabella usando l'istruzione INSERT INTO o UPDATE SQL query.
ms.assetid: cc055de8-eaba-48eb-a982-4d584ac7a881
title: Aggiunta di dati binari a una tabella tramite SQL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 005b7de98fa62ae6e79378831802b8a5a9c95b1d0f3d33dd353fd5403ad600ca
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996951"
---
# <a name="adding-binary-data-to-a-table-using-sql"></a>Aggiunta di dati binari a una tabella tramite SQL

I dati binari non possono essere inseriti direttamente in una tabella usando l'istruzione INSERT INTO o UPDATE SQL query. Per aggiungere dati binari a una tabella, è prima necessario usare il marcatore di parametro (?) nella query come segnaposto per il valore binario. L'esecuzione della query deve includere un record che contiene i dati binari in uno dei relativi campi.

Un marcatore è un riferimento di parametro a un valore fornito da un record inviato con la query. È rappresentato nell'istruzione SQL da un punto interrogativo (?).

Il codice di esempio seguente aggiunge dati binari a una tabella.


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



Lo script di esempio seguente aggiunge dati binari a una tabella.


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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Utilizzo delle query](working-with-queries.md)
</dt> <dt>

[SQL Sintassi](sql-syntax.md)
</dt> <dt>

[Esempi di query di database con SQL e script](examples-of-database-queries-using-sql-and-script.md)
</dt> </dl>

 

 



