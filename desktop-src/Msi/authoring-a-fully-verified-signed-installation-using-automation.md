---
description: L'esempio seguente illustra come popolare la tabella MsiDigitalCertificate e la tabella MsiDigitalSignature usando una subroutine Visual Basic, Applications Edition (VBA).
ms.assetid: 3a23a721-0672-4eac-bdf2-434282b92590
title: Creazione di un'installazione firmata completamente verificata tramite Automazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e27f1b0b90296ad92e471449213e86721482a545ff1932458b2ad6b21d47b665
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119559101"
---
# <a name="authoring-a-fully-verified-signed-installation-using-automation"></a>Creazione di un'installazione firmata completamente verificata tramite Automazione

L'esempio seguente illustra come popolare la tabella [MsiDigitalCertificate](msidigitalcertificate-table.md) e la tabella [MsiDigitalSignature](msidigitalsignature-table.md) usando una subroutine Visual Basic, Applications Edition (VBA). Per altre informazioni sulla protezione dei Windows installer, vedere Linee guida per [la creazione di installazioni protette.](guidelines-for-authoring-secure-installations.md)

Il [**metodo FileSignatureInfo restituisce**](installer-filesignatureinfo.md) un SAFEARRAY di byte. Per altre informazioni, vedere Il [**tipo di dati SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray). I dati di questa matrice devono essere convertiti in Unicode Visual Basic non è possibile scrivere byte direttamente in un file. Il [**metodo SetStream può**](record-setstream.md) quindi usare il file di dati convertiti per scrivere dati di flusso in un campo di record specificato di un oggetto [**Record**](record-object.md). Si noti che la conversione dei dati in byte in Unicode può potenzialmente modificare i dati e che i dati convertiti devono corrispondere ai dati originali per la verifica della firma corretta. L'autore del pacchetto deve assicurarsi che i dati originali e convertiti corrispondano.


```VB
Sub PopulateDigitalSignature()

    Dim Installer As Object
    Dim Database As Object
    Dim x() As Byte
    
    Const szSignedCabinet = "c:\test.cab"
    Const szCertFile = "c:\temp\test.cer"
    Const szDatabase = "c:\test.msi"
        
    Set Installer = CreateObject("WindowsInstaller.Installer")
    
    x = Installer.FileSignatureInfo(szSignedCabinet, 0, msiSignatureInfoCertificate)
    
    Dim fs, ts
    Dim s As String
    Set fs = CreateObject("Scripting.FileSystemObject")
    Set ts = fs.CreateTextFile(szCertFile, True)        'Create a file
    
    s = StrConv(x, vbUnicode)
    ts.Write s
    ts.Close
        
    Set Database = Installer.OpenDatabase(szDatabase, msiOpenDatabaseModeTransact)
    Set ViewCert = Database.OpenView("SELECT * FROM `MsiDigitalCertificate`")
    ViewCert.Execute 0
    Set ViewSig = Database.OpenView("SELECT * FROM `MsiDigitalSignature`")
    ViewSig.Execute 0
    
    Set RecordCert = Installer.CreateRecord(2)
    RecordCert.StringData(1) = "Test"
    RecordCert.SetStream 2, szCertFile
    ViewCert.Modify msiViewModifyInsert, RecordCert
    
    Set RecordSig = Installer.CreateRecord(4)
    RecordSig.StringData(1) = "Media"
    RecordSig.StringData(2) = "1"
    RecordSig.StringData(3) = "Test"
    ViewSig.Modify msiViewModifyInsert, RecordSig
    
    Database.Commit
      fs.DeleteFile(szCertFile)
End Sub
```



 

 
