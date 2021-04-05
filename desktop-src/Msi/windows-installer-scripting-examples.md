---
description: I componenti di Windows SDK per Windows Installer sviluppatori contengono file VBScript che mostrano come viene usata l'interfaccia di automazione del Windows Installer per modificare i pacchetti Windows Installer.
ms.assetid: 93747a8d-32e0-4f31-a5cf-f95fb26b97df
title: Esempi di script di Windows Installer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47c2ad75411201cdbf74ef3aa035906d7e58aa7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967731"
---
# <a name="windows-installer-scripting-examples"></a>Esempi di script di Windows Installer

I [componenti di Windows SDK per Windows Installer sviluppatori](platform-sdk-components-for-windows-installer-developers.md) contengono file VBScript che mostrano come viene usata l'interfaccia di automazione del Windows Installer per modificare i pacchetti Windows Installer.

Gli esempi di script identificati in questo argomento non sono supportati da Microsoft Corporation e sono forniti solo come riferimento potenzialmente utile. Per eseguire questi esempi, è necessario Windows script host. Per ulteriori informazioni su Windows script host, vedere la sezione [Windows script host](/previous-versions//9bbdkx3k(v=vs.85)) di Microsoft Windows Software Development Kit (SDK).



| File script di esempio | Descrizione                                                                                                 |
|--------------------|-------------------------------------------------------------------------------------------------------------|
| WiLstPrd.vbs       | [Elencare prodotti, proprietà, funzionalità e componenti](list-products-properties-features-and-components.md) |
| WiImport.vbs       | [Importa file](import-files.md)                                                                            |
| WiExport.vbs       | [Esporta file](export-files.md)                                                                            |
| WiSubStg.vbs       | [Gestisci sottoarchivi](manage-substorages.md)                                                                |
| WiStream.vbs       | [Gestisci flussi binari](manage-binary-streams.md)                                                          |
| WiMerge.vbs        | [Unire due database](merge-two-databases.md)                                                              |
| WiGenXfm.vbs       | [Genera una trasformazione](generate-a-transform.md)                                                            |
| WiUseXfm.vbs       | [Applicare una trasformazione](apply-a-transform.md)                                                                  |
| WiLstXfm.vbs       | [Visualizzazione di una trasformazione](view-a-transform.md) (solo cscript)                                                     |
| WiDiffDb.vbs       | [Visualizzare le differenze tra due database](view-differences-between-two-databases.md) (solo cscript)         |
| WiLstScr.vbs       | [Visualizza script del programma di installazione](view-installer-script.md) (solo cscript)                                           |
| WiSumInf.vbs       | [Gestione delle informazioni di riepilogo](manage-summary-information.md)                                                |
| WiPolicy.vbs       | [Gestione delle impostazioni dei criteri](manage-policy-settings.md)                                                        |
| WiLangId.vbs       | [Gestisci lingua e tabella codici](manage-language-and-codepage.md)                                            |
| WiToAnsi.vbs       | [Copiare un file Unicode in un file ANSI](copy-a-unicode-file-to-an-ansi-file.md)                              |
| WiFilVer.vbs       | [Gestire le dimensioni e le versioni dei file](manage-file-sizes-and-versions.md)                                        |
| WiMakCab.vbs       | [Genera file CAB](generate-file-cabinet.md)                                                          |
| WiRunSQL.vbs       | [Istruzioni EXECUTE SQL](execute-sql-statements.md)                                                        |
| WiTextIn.vbs       | [Copia il file ANSI in un campo di database](copy-ansi-file-into-a-database-field.md)                            |
| WiCompon.vbs       | [Elenca componenti](list-components.md)                                                                      |
| WiFeatur.vbs       | [Elencare le funzionalità](list-features.md)                                                                          |
| WiDialog.vbs       | [Interfaccia utente di anteprima](preview-user-interface.md)                                                        |



 

Tutti questi script visualizzano una schermata della guida che descrive gli argomenti della riga di comando. Per visualizzare la schermata della Guida in Windows, fare doppio clic sul file. Per visualizzare la schermata della guida da una riga di comando, immettere una? come primo argomento oppure immettere un numero di argomenti inferiore al necessario. Gli script restituiscono il valore 0 per l'esito positivo, 1 se la guida viene richiamata e 2 se in caso di errore.

Per questi esempi è necessario che Windows script host sia in esecuzione. Windows script host è in realtà costituito da due host:

-   CScript.exe è la versione che consente di eseguire gli script dal prompt dei comandi e fornisce opzioni della riga di comando per l'impostazione delle proprietà dello script.
-   WScript.exe è la versione di Windows script host che consente di eseguire script da Windows. Per ulteriori informazioni, vedere la sezione [Windows script host](/previous-versions//9bbdkx3k(v=vs.85)) nell'Windows SDK.

L'utilità Makecab.exe è inclusa negli esempi di applicazione di patch nei [componenti Windows SDK per Windows Installer sviluppatori](platform-sdk-components-for-windows-installer-developers.md).

Per informazioni su WMI, vedere [utilizzo di Windows Installer con WMI](using-windows-installer-with-wmi.md).

 

 
