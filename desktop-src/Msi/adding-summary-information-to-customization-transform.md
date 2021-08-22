---
description: Per applicare la trasformazione di personalizzazione durante un'installazione del prodotto, è necessario aggiungere un flusso di informazioni di riepilogo al file di trasformazione MNPtrans.mst generato in Generazione di una trasformazione di personalizzazione.
ms.assetid: 586f6c43-7449-4d06-9201-9b4b4919871e
title: Aggiunta di informazioni di riepilogo alla trasformazione personalizzazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4ea4c9aa505d425bfd06fe5cac1f45666e794624618db14100ee5f517dd3048
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118639471"
---
# <a name="adding-summary-information-to-customization-transform"></a>Aggiunta di informazioni di riepilogo alla trasformazione personalizzazione

Per applicare la trasformazione di personalizzazione durante un'installazione del prodotto, è necessario aggiungere un flusso di informazioni di riepilogo al file di trasformazione MNPtrans.mst generato in Generazione di una trasformazione [di personalizzazione](generating-a-customization-transform.md). [](summary-information-stream.md)

È possibile generare informazioni di riepilogo per una trasformazione [**usando MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa) o [**il metodo CreateTransformSummaryInfo**](database-createtransformsummaryinfo.md). Il frammento Sum.vbs seguente illustra il [**metodo CreateTransformSummaryInfo**](database-createtransformsummaryinfo.md) ed è da usare con Windows Host script. Si noti che questo esempio non esegue alcuna convalida e non elimina alcuna condizione di errore.


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



Per creare e aggiungere informazioni di riepilogo al file di trasformazione MNPtrans.mst creato [in](generating-a-customization-transform.md)Generazione di una trasformazione di personalizzazione, passare alla cartella contenente Gen.vbs, il database originale, il database aggiornato e la trasformazione e immettere la riga di comando seguente.

**Cscript.exe Sum.vbs MNP2000.msi MNP2000t.msi MNPtrans.mst**

Fare clic MNP2000.msi'icona di avvio per avviare un'installazione o usare la riga di comando seguente.

**msiexec /i MNP2000.msi**

In questo modo il prodotto viene installato senza le personalizzazioni. Per eseguire l'installazione con la personalizzazione, immettere la riga di comando seguente. Si noti che il valore della [**proprietà TRANSFORMS**](transforms.md) fa riferimento al file di trasformazione che si trova nell'origine.

**msiexec /i MNP2000.msi TRANSFORMS=MNPtrans.mst**

La funzionalità Gate non viene visualizzata nell'albero di selezione delle funzionalità e i componenti della funzionalità Gate non vengono installati anche se nell'interfaccia utente è selezionato Un tipo completo di installazione.

[Continua](embedding-customization-transforms-as-substorage.md)

 

 



