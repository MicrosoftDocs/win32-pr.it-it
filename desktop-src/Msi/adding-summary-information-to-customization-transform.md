---
description: Per applicare la trasformazione personalizzazione durante un'installazione del prodotto, è necessario aggiungere un flusso di informazioni di riepilogo al file di trasformazione MNPtrans. MST generato durante la generazione di una trasformazione di personalizzazione.
ms.assetid: 586f6c43-7449-4d06-9201-9b4b4919871e
title: Aggiunta di informazioni di riepilogo alla trasformazione personalizzazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64957fcf8f29ab8793517015c7018292ba9a6e69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311076"
---
# <a name="adding-summary-information-to-customization-transform"></a>Aggiunta di informazioni di riepilogo alla trasformazione personalizzazione

Per applicare la trasformazione personalizzazione durante un'installazione del prodotto, è necessario aggiungere un [flusso di informazioni di riepilogo](summary-information-stream.md) al file di trasformazione MNPtrans. MST generato durante la generazione di [una trasformazione di personalizzazione](generating-a-customization-transform.md).

È possibile generare informazioni di riepilogo per una trasformazione utilizzando [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa) o il [**Metodo CreateTransformSummaryInfo**](database-createtransformsummaryinfo.md). Il frammento di codice seguente, Sum.vbs, illustra il [**Metodo CreateTransformSummaryInfo**](database-createtransformsummaryinfo.md) ed è utilizzabile con Windows script host. Si noti che in questo esempio non viene eseguita alcuna convalida e non vengono evitate condizioni di errore.


```VB
'Sum.vbs. Argument(0) is the original database. Argument(1) is the
'    customized database. Argument(2) is the transform file.
 
Option Explicit

' Check arguments
If WScript.Arguments.Count < 2 Then
    WScript.Echo "Usage is sum.vbs [original database] [customized database] [transform]"
    WScript.Quit(1)
End If

' Connect to Windows Installer object
On Error Resume Next
Dim installer : Set installer = Nothing
Set installer = Wscript.CreateObject("WindowsInstaller.Installer") 
 
' Open databases and transform 
Dim database1 : Set database1 =
    installer.OpenDatabase(Wscript.Arguments(0), 0) 
Dim database2 : Set database2 =
    installer.OpenDatabase(Wscript.Arguments(1), 0) 
Dim transform : transform = Wscript.Arguments(2)
 
' Create and add Summary Information
Dim transinfo : transinfo =
    Database2.CreateTransformSummaryInfo(Database1, transform,0,0)
```



Per creare e aggiungere informazioni di riepilogo al file di trasformazione MNPtrans. MST creato durante la [generazione di una trasformazione di personalizzazione](generating-a-customization-transform.md), passare alla cartella contenente Gen.vbs, il database originale, il database aggiornato e la trasformazione, quindi immettere la riga di comando seguente.

**Cscript.exe Sum.vbs MNP2000.msi MNP2000t.msi MNPtrans. MST**

Fare clic sull'icona MNP2000.msi per avviare un'installazione o utilizzare la riga di comando seguente.

**msiexec/i MNP2000.msi**

Il prodotto verrà installato senza le personalizzazioni. Per eseguire l'installazione con la personalizzazione, immettere la riga di comando seguente. Si noti che il valore della proprietà [**TRANSforms**](transforms.md) si riferisce al file di trasformazione situato nell'origine.

**msiexec/i MNP2000.msi Transforms = MNPtrans. MST**

La funzionalità di controllo non viene visualizzata nell'albero di selezione delle funzionalità e i componenti della funzionalità di controllo non vengono installati anche se nell'interfaccia utente è selezionato un tipo completo di installazione.

[Continua](embedding-customization-transforms-as-substorage.md)

 

 



