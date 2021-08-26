---
description: Elenco delle proprietà del Windows installer che rendono i valori scritti nella chiave del Registro di sistema Uninstall.
ms.assetid: f831cc62-4b19-4285-8bb1-6080567ac985
title: Windows Proprietà del programma di installazione per la chiave di disinstallazione del Registro di sistema
ms.topic: article
ms.date: 05/31/2018
ms.custom: contperf-fy21q3
ms.openlocfilehash: b898cd2a83a05783141ddf1fb4a7cbebb783bbcd7640526c5b653afa434d2175
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810320"
---
# <a name="windows-installer-properties-for-the-uninstall-registry-key"></a>Windows Proprietà del programma di installazione per la chiave di disinstallazione del Registro di sistema

Le proprietà del programma di installazione seguenti forniscono i valori scritti nella chiave del Registro di sistema:

**HKEY \_ Local \_ MACHINE** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Uninstall**

I valori vengono archiviati in una sottochiave identificata dal GUID del codice prodotto dell'applicazione.



| Valore               | Windows Proprietà Installer                                                                                                                                                                                                                                                                                                                                           |
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DisplayName         | [**ProductName**](productname.md) - proprietà                                                                                                                                                                                                                                                                                                                          |
| DisplayVersion      | Derivato dalla [**proprietà ProductVersion**](productversion.md)                                                                                                                                                                                                                                                                                                       |
| Publisher           | [**Proprietà Manufacturer**](manufacturer.md)                                                                                                                                                                                                                                                                                                                        |
| VersionMinor        | Derivato dalla [**proprietà ProductVersion**](productversion.md)                                                                                                                                                                                                                                                                                                       |
| VersionMajor        | Derivato dalla [**proprietà ProductVersion**](productversion.md)                                                                                                                                                                                                                                                                                                       |
| Versione             | Derivato dalla [**proprietà ProductVersion**](productversion.md)                                                                                                                                                                                                                                                                                                       |
| HelpLink            | [**Proprietà ARPHELPLINK**](arphelplink.md)                                                                                                                                                                                                                                                                                                                          |
| HelpTelephone       | [**ARPHELPTELEPHONE**](arphelptelephone.md) - proprietà                                                                                                                                                                                                                                                                                                                |
| InstallDate         | Data e ora dell'ultima ricezione del servizio da parte del prodotto. Il valore di questa proprietà viene sostituito ogni volta che viene applicata o rimossa una patch dal prodotto o viene usata l'opzione della riga di comando [/v](command-line-options.md) per ripristinare il prodotto. Se il prodotto non ha ricevuto riparazioni o patch, questa proprietà contiene l'ora in cui il prodotto è stato installato nel computer. |
| InstallLocation     | [**ARPINSTALLLOCATION -**](arpinstalllocation.md) proprietà                                                                                                                                                                                                                                                                                                            |
| InstallSource       | [**SourceDir -**](sourcedir.md) proprietà                                                                                                                                                                                                                                                                                                                              |
| URLInfoAbout        | [**ARPURLINFOABOUT -**](arpurlinfoabout.md) proprietà                                                                                                                                                                                                                                                                                                                  |
| URLUpdateInfo       | [**ARPURLUPDATEINFO**](arpurlupdateinfo.md) - proprietà                                                                                                                                                                                                                                                                                                                |
| AuthorizedCDFPrefix | [**ARPAUTHORIZEDCDFPREFIX -**](arpauthorizedcdfprefix.md) proprietà                                                                                                                                                                                                                                                                                                    |
| Commenti            | [**Proprietà ARPCOMMENTS**](arpcomments.md) <br/> Commenti forniti al pannello **di controllo** Installazione applicazioni.<br/>                                                                                                                                                                                                                                |
| Contatto             | [**Proprietà ARPCONTACT**](arpcontact.md) <br/> Contattare il pannello **di controllo Installazione** applicazioni.<br/>                                                                                                                                                                                                                                   |
| EstimatedSize       | Determinato e impostato dal programma di Windows di installazione.                                                                                                                                                                                                                                                                                                                         |
| Linguaggio            | [**ProductLanguage -**](productlanguage.md) proprietà                                                                                                                                                                                                                                                                                                                  |
| ModifyPath          | Determinato e impostato dal programma di Windows di installazione.                                                                                                                                                                                                                                                                                                                         |
| File Leggimi              | [**Proprietà ARPREADME**](arpreadme.md) <br/> File Leggimi fornito nel pannello **di controllo Installazione** applicazioni.<br/>                                                                                                                                                                                                                                      |
| UninstallString     | Determinato e impostato dal programma Windows programma di installazione.                                                                                                                                                                                                                                                                                                                             |
| SettingsIdentifier  | [**MsiARPSETTINGSIDENTIFIER -**](msiarpsettingsidentifier.md) proprietà                                                                                                                                                                                                                                                                                                |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sulle proprietà](about-properties.md)
</dt> <dt>

[Configurazione di Installazione applicazioni con il programma di Windows installazione](configuring-add-remove-programs-with-windows-installer.md)
</dt> <dt>

[Informazioni di riferimento sulla proprietà](property-reference.md)
</dt> <dt>

[Utilizzo delle proprietà](using-properties.md)
</dt> </dl>

 

 




