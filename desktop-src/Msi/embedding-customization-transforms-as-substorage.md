---
description: È possibile archiviare la trasformazione di personalizzazione in un archivio del pacchetto Windows Installer per garantire che la trasformazione sia sempre disponibile quando il pacchetto di installazione è disponibile.
ms.assetid: d4c022d2-a8c4-4b4e-8a6c-b14e1bc6effe
title: Incorporamento di trasformazioni di personalizzazione come archiviazione secondaria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 175c2bd1e52a58d6c73e1e46f8b95501b016bc0e4e1069b86c9c53f47859f20c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118947002"
---
# <a name="embedding-customization-transforms-as-substorage"></a>Incorporamento di trasformazioni di personalizzazione come archiviazione secondaria

È possibile archiviare la trasformazione di personalizzazione in un archivio del pacchetto Windows Installer per garantire che la trasformazione sia sempre disponibile quando il pacchetto di installazione è disponibile. Vedere [Trasformazioni incorporate](embedded-transforms.md). Un esempio è disponibile nell'SDK Windows Installer come utilità WiSubStg.vbs. Il frammento di Emb.vbs seguente illustra anche l'uso della tabella [Storages](-storages-table.md) per aggiungere una trasformazione incorporata e viene utilizzato con Windows Script Host.


```VB
'Emb.vbs. Argument(0) is the original database. Argument(1) is the
'    path to the transform file. Argument(2) is the name of the storage.
'
Option Explicit

' Check arguments
If WScript.Arguments.Count < 2 Then
 WScript.Echo "Usage is emb.vbs [original database] [transform] [storage name]"
 WScript.Quit(1)
End If

' Connect to Windows Installer object
On Error Resume Next
Dim installer : Set installer = Nothing
Set installer = Wscript.CreateObject("WindowsInstaller.Installer")
 
' Evaluate command-line arguments and set open and update modes
Dim databasePath: databasePath = Wscript.Arguments(0)
Dim importPath  : importPath = Wscript.Arguments(1)
Dim storageName : storageName = Wscript.Arguments(2)
 
' Open database and create a view on the _Storages table
Dim sqlQuery : sqlQuery = "SELECT `Name`,`Data` FROM _Storages"
Dim database : Set database = installer.OpenDatabase(databasePath, 1)
Dim view     : Set view = database.OpenView(sqlQuery)
 
'Create and Insert the row.
Dim record   : Set record = installer.CreateRecord(2)
record.StringData(1) = storageName
view.Execute record
 
'Insert storage - copy data into stream
record.SetStream 2, importPath
view.Modify 3, record
database.Commit
Set view = Nothing
Set database = Nothing
```



Per aggiungere un'archiviazione denominata MNPtrans1 a MNP2000.msi e contenente la trasformazione creata [in](adding-summary-information-to-customization-transform.md)Aggiunta di informazioni di riepilogo alla trasformazione personalizzazione , passare alla cartella contenente Emb.vbs, il database originale e il file di trasformazione, quindi immettere la riga di comando seguente.

**Cscript.exe Emb.vbs MNP2000.msi MNPtrans.mst MNPtrans1**

Questa operazione completa l'esempio di trasformazione di personalizzazione. Dopo l'incorporamento della trasformazione in MNPtrans.mst, la trasformazione è sempre disponibile con il pacchetto di installazione. Non è necessario che il file MNPtrans.mst si trovi nell'origine per applicare la trasformazione.

Rimuovere MNPtrans.mst dalla cartella contenente il pacchetto di installazione di esempio. Fare clic MNP2000.msi'icona di avvio per avviare un'installazione o usare la riga di comando seguente.

**msiexec /i MNP2000.msi**

Si noti che il prodotto viene installato senza le personalizzazioni. Per eseguire l'installazione con le personalizzazioni, immettere la riga di comando seguente. Usare i due punti per indicare che il valore della [**proprietà TRANSFORMS**](transforms.md) fa riferimento a una trasformazione incorporata.

msiexec /i MNP2000.msi TRANSFORMS=:MNPtrans1

Si noti che la funzionalità Gate non viene visualizzata nell'albero di selezione delle funzionalità e che i componenti della funzionalità Gate non vengono installati anche se nell'interfaccia utente è selezionato Un tipo di installazione completo.

## <a name="next-example"></a>Esempio successivo

[Esempio di applicazione di patch per gli aggiornamenti di piccole dimensioni](a-small-update-patching-example.md)

 

 



