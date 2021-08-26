---
description: Un'applicazione può usare la funzione MsiOpenDatabase per aprire un database di installazione nuovo o esistente (file .msi) o un pacchetto di patch (file msp). L'applicazione controlla il valore restituito di MsiOpenDatabase prima di usare l'handle del database.
ms.assetid: 54a8d571-ebc3-42d5-bc34-8f29b245b4d8
title: Esempio di database e patch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7de816e471bbc3df4ec2970202130dba79267a06cb872e74734de322cba2d68d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119997031"
---
# <a name="a-database-and-patch-example"></a>Esempio di database e patch

Un'applicazione può usare la [**funzione MsiOpenDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msiopendatabasea) per aprire un database di installazione nuovo o esistente (file .msi) o un pacchetto patch (file msp). L'applicazione controlla il valore restituito di **MsiOpenDatabase prima** di usare l'handle del database.

Negli esempi seguenti vengono usate le variabili di tipo **PMSIHANDLE** definite in msi.h. È consigliabile usare il tipo **PMSIHANDLE** perché il programma di installazione chiude gli oggetti **PMSIHANDLE** non appena es uscita dall'ambito, mentre l'applicazione deve chiudere gli oggetti **MSIHANDLE** chiamando [**MsiCloseHandle**](/windows/desktop/api/Msi/nf-msi-msiclosehandle). Per altre informazioni, vedere [la sezione Use PMSIHANDLE instead of HANDLE](windows-installer-best-practices.md) in Windows Installer Best [Practices](windows-installer-best-practices.md).

Nell'esempio seguente viene aperto un database, sample.msi, per la sola lettura. [**MsiOpenDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msiopendatabasea) ha esito positivo solo se sample.msi esistente nella directory c: \\ test. In caso di esito positivo, l'handle di database restituito può essere usato per eseguire query sui dati nel pacchetto di installazione usando [**MsiDatabaseOpenView**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseopenviewa) e [**MsiGetSummaryInformation.**](/windows/desktop/api/Msiquery/nf-msiquery-msigetsummaryinformationa)


```C++
PMSIHANDLE hDbReadOnly = 0;
UINT uiStatus1 = MsiOpenDatabase(TEXT("c:\\test\\sample.msi"), MSIDBOPEN_READONLY, &hDbReadOnly);
if (ERROR_SUCCESS != uiStatus1)
{
    // process error
    return uiStatus1;
}
```



Nell'esempio seguente viene aperto il database per la lettura e la scrittura. Se l'applicazione [**chiama MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit), tutte le modifiche apportate al database vengono salvate. Se l'applicazione non chiama **MsiDatabaseCommit**, non vengono apportate modifiche al database.


```C++
PMSIHANDLE hDbTransact = 0;
UINT uiStatus2 = MsiOpenDatabase(TEXT("c:\\test\\example.msi"), MSIDBOPEN_TRANSACT, &hDbTransact);
if (ERROR_SUCCESS != uiStatus2)
{
    // process error
    return uiStatus2;
}
```



Nell'esempio seguente viene creato un database esistente, text.msi e viene creato un nuovo database newtest.msi. Tutte le modifiche apportate possono essere salvate nel nuovo database chiamando [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit). Il database esistente specificato nel *parametro szDatabasePath* rimane invariato.


```C++
PMSIHANDLE hDbOutput = 0;
UINT uiStatus3 = MsiOpenDatabase(TEXT("c:\\test\\test.msi"), TEXT("c:\\test\\newtest.msi"), &hDbOutput);
if (ERROR_SUCCESS != uiStatus3)
{
    // process error
    return uiStatus3;
}
```



Nell'esempio seguente viene aperto un pacchetto Windows di patch del programma di installazione (file msp) per la sola lettura. L'handle di patch restituito può essere usato per determinare i file CAB e trasformare le risorse di archiviazione secondarie incluse nel pacchetto di patch tramite query sulle tabelle [ \_ Flussi](-streams-table.md) [ \_ e Storages.](-storages-table.md)

**Windows Installer 2.0:** Non supportato. A partire da Windows Installer 3.0, l'applicazione può eseguire una query sulla tabella [MsiPatchSequence](msipatchsequence-table.md) presente in un pacchetto di patch che usa le nuove informazioni di sequenziazione delle patch.


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



 

 



