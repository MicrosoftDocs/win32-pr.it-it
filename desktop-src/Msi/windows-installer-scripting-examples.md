---
description: La Windows SDK components for Windows Installer Developers contiene file VBScript che illustrano come viene usata l'interfaccia di automazione Windows Installer per modificare i pacchetti Windows Installer.
ms.assetid: 93747a8d-32e0-4f31-a5cf-f95fb26b97df
title: Windows Esempi di scripting del programma di installazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3addf648460418daad783b6c5dbcc71078f9904c4a0bba1324f025896692cd37
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065771"
---
# <a name="windows-installer-scripting-examples"></a>Windows Esempi di scripting del programma di installazione

La [Windows SDK components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md) contiene file VBScript che illustrano come viene usata l'interfaccia di automazione Windows Installer per modificare i pacchetti Windows Installer.

Gli esempi di script identificati in questo argomento non sono supportati da Microsoft Corporation e vengono forniti solo come riferimento potenzialmente utile. L'esecuzione di questi esempi richiede Windows Host script. Per altre informazioni sull'host Windows script, vedere la sezione Windows [Script Host](/previous-versions//9bbdkx3k(v=vs.85)) di Microsoft Windows Software Development Kit (SDK).



| File di script di esempio | Descrizione                                                                                                 |
|--------------------|-------------------------------------------------------------------------------------------------------------|
| WiLstPrd.vbs       | [Elencare prodotti, proprietà, funzionalità e componenti](list-products-properties-features-and-components.md) |
| WiImport.vbs       | [Importare file](import-files.md)                                                                            |
| WiExport.vbs       | [Esportare file](export-files.md)                                                                            |
| WiSubStg.vbs       | [Gestire le sottocartelle](manage-substorages.md)                                                                |
| WiStream.vbs       | [Gestire le Flussi](manage-binary-streams.md)                                                          |
| WiMerge.vbs        | [Unire due database](merge-two-databases.md)                                                              |
| WiGenXfm.vbs       | [Generare una trasformazione](generate-a-transform.md)                                                            |
| WiUseXfm.vbs       | [Applicare una trasformazione](apply-a-transform.md)                                                                  |
| WiLstXfm.vbs       | [Visualizzare una trasformazione](view-a-transform.md) (solo CSCRIPT)                                                     |
| WiDiffDb.vbs       | [Visualizzare le differenze tra due database](view-differences-between-two-databases.md) (solo CSCRIPT)         |
| WiLstScr.vbs       | [Visualizza script del programma di](view-installer-script.md) installazione (solo CSCRIPT)                                           |
| WiSumInf.vbs       | [Gestire le informazioni di riepilogo](manage-summary-information.md)                                                |
| WiPolicy.vbs       | [Gestione delle impostazioni dei criteri](manage-policy-settings.md)                                                        |
| WiLangId.vbs       | [Gestire la lingua e la tabella codici](manage-language-and-codepage.md)                                            |
| WiToAnsi.vbs       | [Copiare un file Unicode in un file Ansi](copy-a-unicode-file-to-an-ansi-file.md)                              |
| WiFilVer.vbs       | [Gestire le dimensioni e le versioni dei file](manage-file-sizes-and-versions.md)                                        |
| WiMakCab.vbs       | [Generare file CAB](generate-file-cabinet.md)                                                          |
| WiRunSQL.vbs       | [Eseguire SQL istruzioni](execute-sql-statements.md)                                                        |
| WiTextIn.vbs       | [Copiare un file ANSI in un campo di database](copy-ansi-file-into-a-database-field.md)                            |
| WiCompon.vbs       | [Elencare i componenti](list-components.md)                                                                      |
| WiFeatur.vbs       | [Elencare le funzionalità](list-features.md)                                                                          |
| WiDialog.vbs       | [Anteprima Interfaccia utente](preview-user-interface.md)                                                        |



 

Tutti questi script visualizzano una schermata della Guida che descrive gli argomenti della riga di comando. Per visualizzare la schermata della Guida in Windows fare doppio clic sul file. Per visualizzare la schermata della Guida da una riga di comando, immettere ? come primo argomento oppure immettere un numero di argomenti inferiore a quello richiesto. Gli script restituiscono il valore 0 per l'esito positivo, 1 se viene richiamata la Guida e 2 in caso di errore.

Questi esempi richiedono l Windows'host script per l'esecuzione. Windows L'host script è in realtà due host:

-   CScript.exe è la versione che consente di eseguire script dal prompt dei comandi e fornisce opzioni della riga di comando per l'impostazione delle proprietà dello script.
-   WScript.exe è la versione dell'host Windows script che consente di eseguire script da Windows. Per altre informazioni, vedere la sezione [Windows Script Host](/previous-versions//9bbdkx3k(v=vs.85)) in Windows SDK.

LMakecab.exe utilità è inclusa negli esempi di applicazione di patch in [Windows SDK components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).

Per informazioni su WMI, vedere [Using Windows Installer with WMI](using-windows-installer-with-wmi.md).

 

 
