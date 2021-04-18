---
description: È possibile generare un file di trasformazione utilizzando MsiDatabaseGenerateTransform o il metodo GenerateTransform dell'oggetto di database.
ms.assetid: c016fcba-0d54-4b99-bcdd-36967b2c9da0
title: Generazione di una trasformazione di personalizzazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f73609b7be60dbfe236d31ed5a865e86ff6e310
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314268"
---
# <a name="generating-a-customization-transform"></a>Generazione di una trasformazione di personalizzazione

È possibile generare un file di trasformazione utilizzando [**MsiDatabaseGenerateTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegeneratetransforma) o il [**Metodo GenerateTransform**](database-generatetransform.md) dell' [**oggetto di database**](database-object.md). Un esempio è fornito in Windows Installer SDK come WiGenXfm.vbs di utilità. Il frammento di codice seguente, Gen.vbs, illustra anche il metodo **GenerateTransform** ed è utilizzabile con Windows script host.


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



Per generare il file di trasformazione MNPtrans. MST dal database MNP2000.msi originale e dal database MNP2000t.msi modificato in [personalizzazione di un database originale](customizing-an-original-database.md), passare alla cartella contenente Gen.vbs, il database originale e il database del programma di installazione aggiornato e immettere la riga di comando seguente.

**Cscript.exe Gen.vbs MNP2000.msi MNP2000t.msi MNPtrans. MST**

[Continua](adding-summary-information-to-customization-transform.md)

 

 



