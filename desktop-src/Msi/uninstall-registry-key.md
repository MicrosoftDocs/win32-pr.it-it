---
description: Elenco delle proprietà di Windows Installer che assegnano valori scritti sotto la chiave Disinstalla del registro di sistema.
ms.assetid: f831cc62-4b19-4285-8bb1-6080567ac985
title: Windows Installer proprietà della chiave Disinstalla registro di sistema
ms.topic: article
ms.date: 05/31/2018
ms.custom: contperf-fy21q3
ms.openlocfilehash: 90174cabed7a1d9ff0ca21b532c459a1026787a6
ms.sourcegitcommit: 4af3e9ec3142ba499d20ed8b174c2b219c5eacd2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/30/2021
ms.locfileid: "106334295"
---
# <a name="windows-installer-properties-for-the-uninstall-registry-key"></a>Windows Installer proprietà della chiave Disinstalla registro di sistema

Le seguenti proprietà del programma di installazione forniscono i valori scritti sotto la chiave del registro di sistema:

**HKEY \_ \_Computer locale** \\ **software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Uninstall**

I valori vengono archiviati in una sottochiave identificata dal GUID del codice prodotto dell'applicazione.



| Valore               | Proprietà Windows Installer                                                                                                                                                                                                                                                                                                                                           |
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DisplayName         | Proprietà [**ProductName**](productname.md)                                                                                                                                                                                                                                                                                                                          |
| DisplayVersion      | Derivato dalla proprietà [**ProductVersion**](productversion.md)                                                                                                                                                                                                                                                                                                       |
| Publisher           | Proprietà [**produttore**](manufacturer.md)                                                                                                                                                                                                                                                                                                                        |
| VersionMinor        | Derivato dalla proprietà [**ProductVersion**](productversion.md)                                                                                                                                                                                                                                                                                                       |
| VersionMajor        | Derivato dalla proprietà [**ProductVersion**](productversion.md)                                                                                                                                                                                                                                                                                                       |
| Versione             | Derivato dalla proprietà [**ProductVersion**](productversion.md)                                                                                                                                                                                                                                                                                                       |
| HelpLink            | Proprietà [**ARPHELPLINK**](arphelplink.md)                                                                                                                                                                                                                                                                                                                          |
| HelpTelephone       | Proprietà [**ARPHELPTELEPHONE**](arphelptelephone.md)                                                                                                                                                                                                                                                                                                                |
| InstallDate         | L'ultima volta in cui il prodotto ha ricevuto il servizio. Il valore di questa proprietà viene sostituito ogni volta che una patch viene applicata o rimossa dal prodotto oppure viene utilizzata l' [opzione della riga di comando](command-line-options.md) /v per ripristinare il prodotto. Se il prodotto non ha ricevuto alcuna riparazione o patch, questa proprietà contiene l'ora in cui questo prodotto è stato installato nel computer. |
| InstallLocation     | Proprietà [**ARPINSTALLLOCATION**](arpinstalllocation.md)                                                                                                                                                                                                                                                                                                            |
| InstallSource       | Proprietà [**SourceDir**](sourcedir.md)                                                                                                                                                                                                                                                                                                                              |
| URLInfoAbout        | Proprietà [**ARPURLINFOABOUT**](arpurlinfoabout.md)                                                                                                                                                                                                                                                                                                                  |
| URLUpdateInfo       | Proprietà [**ARPURLUPDATEINFO**](arpurlupdateinfo.md)                                                                                                                                                                                                                                                                                                                |
| AuthorizedCDFPrefix | Proprietà [**ARPAUTHORIZEDCDFPREFIX**](arpauthorizedcdfprefix.md)                                                                                                                                                                                                                                                                                                    |
| Commenti            | Proprietà [**ARPCOMMENTS**](arpcomments.md) <br/> Commenti forniti al pannello di controllo **Installazione applicazioni** .<br/>                                                                                                                                                                                                                                |
| Contatto             | Proprietà [**ARPCONTACT**](arpcontact.md) <br/> Contatto fornito al pannello di controllo **Installazione applicazioni** .<br/>                                                                                                                                                                                                                                   |
| EstimatedSize       | Determinato e impostato dal Windows Installer.                                                                                                                                                                                                                                                                                                                         |
| Linguaggio            | Proprietà [**ProductLanguage**](productlanguage.md)                                                                                                                                                                                                                                                                                                                  |
| ModifyPath          | Determinato e impostato dal Windows Installer.                                                                                                                                                                                                                                                                                                                         |
| File Leggimi              | Proprietà [**ARPREADME**](arpreadme.md) <br/> File Leggimi fornito nel pannello di controllo **Installazione applicazioni** .<br/>                                                                                                                                                                                                                                      |
| UninstallString     | Determinato e impostato dal Windows Installer.                                                                                                                                                                                                                                                                                                                             |
| SettingsIdentifier  | Proprietà [**MSIARPSETTINGSIDENTIFIER**](msiarpsettingsidentifier.md)                                                                                                                                                                                                                                                                                                |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sulle proprietà](about-properties.md)
</dt> <dt>

[Configurazione di installazione applicazioni con Windows Installer](configuring-add-remove-programs-with-windows-installer.md)
</dt> <dt>

[Riferimento alla proprietà](property-reference.md)
</dt> <dt>

[Utilizzo delle proprietà](using-properties.md)
</dt> </dl>

 

 




