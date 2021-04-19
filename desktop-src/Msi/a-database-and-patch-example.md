---
description: Un'applicazione può utilizzare la funzione MsiOpenDatabase per aprire un database di installazione nuovo o esistente (file con estensione msi) o un pacchetto di patch (file con estensione msp). L'applicazione verifica il valore restituito di MsiOpenDatabase prima di usare l'handle di database.
ms.assetid: 54a8d571-ebc3-42d5-bc34-8f29b245b4d8
title: Esempio di database e patch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07ff5925fc409352b4c9ed8c1762ba1ad17b261f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311105"
---
# <a name="a-database-and-patch-example"></a>Esempio di database e patch

Un'applicazione può utilizzare la funzione [**MsiOpenDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msiopendatabasea) per aprire un database di installazione nuovo o esistente (file con estensione msi) o un pacchetto di patch (file con estensione msp). L'applicazione verifica il valore restituito di **MsiOpenDatabase** prima di usare l'handle di database.

Negli esempi seguenti vengono usate le variabili di tipo **PMSIHANDLE** definite in MSI. h. È consigliabile usare il tipo **PMSIHANDLE** perché il programma di installazione chiude gli oggetti **PMSIHANDLE** mentre escono dall'ambito, mentre l'applicazione deve chiudere gli oggetti **MSIHANDLE** chiamando [**MsiCloseHandle**](/windows/desktop/api/Msi/nf-msi-msiclosehandle). Per ulteriori informazioni, vedere la sezione [utilizzare PMSIHANDLE anziché handle](windows-installer-best-practices.md) nell' [Windows Installer procedure consigliate](windows-installer-best-practices.md).

Nell'esempio seguente viene aperto un database, sample.msi, solo per la lettura. [**MsiOpenDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msiopendatabasea) ha esito positivo solo se sample.msi esiste nella directory c: \\ test. Al termine dell'operazione, è possibile usare l'handle di database restituito per eseguire query sui dati nel pacchetto di installazione usando [**MsiDatabaseOpenView**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseopenviewa) e [**MsiGetSummaryInformation**](/windows/desktop/api/Msiquery/nf-msiquery-msigetsummaryinformationa).


```C++
PMSIHANDLE hDbReadOnly = 0;
UINT uiStatus1 = MsiOpenDatabase(TEXT("c:\\test\\sample.msi"), MSIDBOPEN_READONLY, &hDbReadOnly);
if (ERROR_SUCCESS != uiStatus1)
{
    // process error
    return uiStatus1;
}
```



Nell'esempio seguente viene aperto il database per la lettura e la scrittura. Se l'applicazione chiama [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit), vengono salvate tutte le modifiche apportate al database. Se l'applicazione non chiama **MsiDatabaseCommit**, non viene apportata alcuna modifica al database.


```C++
PMSIHANDLE hDbTransact = 0;
UINT uiStatus2 = MsiOpenDatabase(TEXT("c:\\test\\example.msi"), MSIDBOPEN_TRANSACT, &hDbTransact);
if (ERROR_SUCCESS != uiStatus2)
{
    // process error
    return uiStatus2;
}
```



Nell'esempio seguente viene preso un database esistente, text.msi e viene creato un nuovo database, newtest.msi. Tutte le modifiche apportate possono essere salvate nel nuovo database chiamando [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit). Il database esistente specificato nel parametro *szDatabasePath* è invariato.


```C++
PMSIHANDLE hDbOutput = 0;
UINT uiStatus3 = MsiOpenDatabase(TEXT("c:\\test\\test.msi"), TEXT("c:\\test\\newtest.msi"), &hDbOutput);
if (ERROR_SUCCESS != uiStatus3)
{
    // process error
    return uiStatus3;
}
```



Nell'esempio seguente viene aperto un pacchetto di patch Windows Installer (file con estensione msp) per la sola lettura. L'handle di patch restituito può essere usato per determinare gli armadi e trasformare le sottoarchiviazioni incluse nel pacchetto di patch dalle query sulle tabelle [ \_ Streams](-streams-table.md) e [ \_ Storages](-storages-table.md) .

**Windows Installer 2,0:** Non supportato. A partire da Windows Installer 3,0, l'applicazione può eseguire una query sulla [tabella MsiPatchSequence](msipatchsequence-table.md) presente in un pacchetto di patch che usa le nuove informazioni di sequenziazione delle patch.


```C++
PMSIHANDLE hDbPatch = 0;
LPCTSTR szPersistMode = MSIDBOPEN_READONLY + MSIDBOPEN_PATCHFILE;
UINT uiStatus4 = MsiOpenDatabase(TEXT("c:\\test\\sample.msp"), szPersistMode, &hDbPatch);
if (ERROR_SUCCESS != uiStatus4)
{
    // process error
    return uiStatus4;
}
```



 

 



