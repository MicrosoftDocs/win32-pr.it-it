---
description: Nell'esempio seguente viene illustrato come popolare la tabella MsiDigitalCertificate e la tabella MsiDigitalSignature utilizzando una subroutine Visual Basic, Applications Edition (VBA).
ms.assetid: 3a23a721-0672-4eac-bdf2-434282b92590
title: Creazione di un'installazione firmata completamente verificata tramite l'automazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e99267feffac71401f36635c08fa7f9f6598a0c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967270"
---
# <a name="authoring-a-fully-verified-signed-installation-using-automation"></a>Creazione di un'installazione firmata completamente verificata tramite l'automazione

Nell'esempio seguente viene illustrato come popolare la [tabella MsiDigitalCertificate](msidigitalcertificate-table.md) e la [tabella MsiDigitalSignature](msidigitalsignature-table.md) utilizzando una subroutine Visual Basic, Applications Edition (VBA). Per ulteriori informazioni sulla protezione dei pacchetti di Windows Installer, vedere [linee guida per la creazione di installazioni protette](guidelines-for-authoring-secure-installations.md).

Il [**Metodo FileSignatureInfo**](installer-filesignatureinfo.md) restituisce un SAFEARRAY di byte. Per ulteriori informazioni, vedere il [**tipo di dati SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray). I dati di questa matrice devono essere convertiti in Unicode perché Visual Basic non dispone di un modo per scrivere i byte direttamente in un file. Il [**Metodo sestream**](record-setstream.md) può quindi utilizzare il file di dati convertiti per scrivere i dati di flusso in un campo record specificato di un [**oggetto record**](record-object.md). Si noti che la conversione dei dati in byte in formato Unicode può potenzialmente modificare i dati e che i dati convertiti devono corrispondere ai dati originali per la corretta verifica della firma. L'autore del pacchetto deve garantire che i dati originali e convertiti corrispondano.


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



 

 
