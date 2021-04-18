---
description: È possibile archiviare la trasformazione personalizzazione in una risorsa di archiviazione del pacchetto di Windows Installer per garantire che la trasformazione sia sempre disponibile quando è disponibile il pacchetto di installazione.
ms.assetid: d4c022d2-a8c4-4b4e-8a6c-b14e1bc6effe
title: Incorporamento di trasformazioni di personalizzazione come sottoarchivio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfd275d36b37b2e29ae166a2a464a62495d2ca9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313349"
---
# <a name="embedding-customization-transforms-as-substorage"></a>Incorporamento di trasformazioni di personalizzazione come sottoarchivio

È possibile archiviare la trasformazione personalizzazione in una risorsa di archiviazione del pacchetto di Windows Installer per garantire che la trasformazione sia sempre disponibile quando è disponibile il pacchetto di installazione. Vedere [trasformazioni incorporate](embedded-transforms.md). Un esempio è fornito in Windows Installer SDK come WiSubStg.vbs di utilità. Il frammento di codice seguente, Emb.vbs, illustra anche l'uso della [tabella Storages](-storages-table.md) per aggiungere una trasformazione incorporata e deve essere usata con Windows script host.


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



Per aggiungere una risorsa di archiviazione denominata MNPtrans1 a MNP2000.msi e contenente la trasformazione creata in [aggiunta di informazioni di riepilogo alla trasformazione personalizzazione](adding-summary-information-to-customization-transform.md), passare alla cartella contenente Emb.vbs, il database originale e il file di trasformazione, quindi immettere la riga di comando seguente.

**Cscript.exe Emb.vbs MNP2000.msi MNPtrans. MST MNPtrans1**

Questa operazione completa l'esempio di trasformazione della personalizzazione. Dopo aver incorporato la trasformazione in MNPtrans. MST, la trasformazione è sempre disponibile con il pacchetto di installazione. Non è necessario che il file MNPtrans. MST si trovi nell'origine per applicare la trasformazione.

Rimuovere MNPtrans. MST dalla cartella che contiene il pacchetto di installazione di esempio. Fare clic sull'icona MNP2000.msi per avviare un'installazione o utilizzare la riga di comando seguente.

**msiexec/i MNP2000.msi**

Si noti che in questo modo viene installato il prodotto senza le personalizzazioni. Per eseguire l'installazione con le personalizzazioni, immettere la riga di comando seguente. Usare i due punti per indicare che il valore della proprietà [**TRANSforms**](transforms.md) si riferisce a una trasformazione incorporata.

msiexec/i MNP2000.msi Transforms =: MNPtrans1

Si noti che la funzionalità di controllo non viene visualizzata nell'albero di selezione delle funzionalità e che i componenti della funzionalità Gate non sono installati anche se nell'interfaccia utente è selezionato un tipo di installazione completo.

## <a name="next-example"></a>Esempio successivo

[Un piccolo esempio di patch di aggiornamento](a-small-update-patching-example.md)

 

 



