---
description: 'Per determinare la versione Windows Installer, è possibile utilizzare i metodi seguenti:'
ms.assetid: 6b39bb19-4360-4d0e-a797-980912a91275
title: Determinazione della versione di Windows Installer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a48434fe415084a93158fb3445a36906d8b8993
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314287"
---
# <a name="determining-the-windows-installer-version"></a>Determinazione della versione di Windows Installer

Per determinare la versione Windows Installer, è possibile utilizzare i metodi seguenti:

-   Chiamare la funzione [**MsiGetFileVersion**](/windows/desktop/api/Msi/nf-msi-msigetfileversiona) con il parametro *szFilePath* impostato sul percorso del file Msi.dll.

    È possibile chiamare la funzione [**SHGetKnownFolderPath**](/windows/win32/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) con la costante di **\_ sistema CSIDL** per ottenere il percorso Msi.dll. A partire da Windows Vista, le applicazioni devono utilizzare la funzione [**SHGetFolderPath**](/windows/win32/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) e **REFKNOWNFOLDERID** "System". Le applicazioni esistenti che usano la funzione **SHGetFolderPath** e il tipo **CSIDL** continueranno a funzionare.

-   Il valore della proprietà [**Installer. Version**](installer-version.md) dell' [**oggetto Installer**](installer-object.md) è equivalente alle stringhe di quattro campi elencate nelle [versioni rilasciate di Windows Installer](released-versions-of-windows-installer.md) argomento.
-   Le applicazioni possono ottenere la versione Windows Installer usando [**DllGetVersion**](/windows/win32/api/shlwapi/nc-shlwapi-dllgetversionproc).
-   Il programma di installazione imposta la proprietà [**VersionMsi**](versionmsi.md) sulla versione di Windows Installer eseguita durante l'installazione.

Per ulteriori informazioni, vedere [versioni rilasciate di Windows Installer](released-versions-of-windows-installer.md).

 

 
