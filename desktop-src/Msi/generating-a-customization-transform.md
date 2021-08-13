---
description: È possibile generare un file di trasformazione usando MsiDatabaseGenerateTransform o il metodo GenerateTransform dell'oggetto Database.
ms.assetid: c016fcba-0d54-4b99-bcdd-36967b2c9da0
title: Generazione di una trasformazione di personalizzazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b790917100cc06da97e09fd8aabf45b580e62008d23c9fc5065e6005112d8d4e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118635999"
---
# <a name="generating-a-customization-transform"></a>Generazione di una trasformazione di personalizzazione

È possibile generare un file di trasformazione usando [**MsiDatabaseGenerateTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegeneratetransforma) o il [**metodo GenerateTransform**](database-generatetransform.md) dell'oggetto [**Database**](database-object.md). Un esempio è disponibile in Windows Installer SDK come strumento di WiGenXfm.vbs. Il frammento di codice Gen.vbs illustra anche il metodo **GenerateTransform** ed è per l'uso con Windows host script.


```VB
'Gen.vbs. Argument(0) is the original database. Argument(1) is the
'    customized database. Argument(2) is the transform file.
 
Option Explicit

' Check arguments
If WScript.Arguments.Count < 2 Then
    WScript.Echo "Usage is gen.vbs [original database] [customized database] [transform file]"
    WScript.Quit(1)
End If

' Connect to Windows Installer object
On Error Resume Next
Dim installer : Set installer = Nothing
Set installer = Wscript.CreateObject("WindowsInstaller.Installer") 
' Open databases
Dim database1 : Set database1 = 
    installer.OpenDatabase(Wscript.Arguments(0), 0) 
Dim database2 : Set database2 = 
    installer.OpenDatabase(Wscript.Arguments(1), 0) 
' Generate transform
Dim transform : transform = Database2.GenerateTransform(Database1,
    Wscript.Arguments(2))
```



Per generare il file di trasformazione MNPtrans.mst dal database MNP2000.msi originale e dal database MNP2000t.msi modificato in [Personalizzazione](customizing-an-original-database.md)di un database originale, passare alla cartella contenente Gen.vbs, il database originale e il database del programma di installazione aggiornato e immettere la riga di comando seguente.

**Cscript.exe Gen.vbs MNP2000.msi MNP2000t.msi MNPtrans.mst**

[Continua](adding-summary-information-to-customization-transform.md)

 

 



