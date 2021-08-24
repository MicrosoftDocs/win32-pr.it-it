---
description: 'È possibile usare i metodi seguenti per determinare la versione Windows Installer:'
ms.assetid: 6b39bb19-4360-4d0e-a797-980912a91275
title: Determinazione della versione Windows installer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e13907790585356fa4a5bc8376fe87f30793e0e3af71e1b0c113f30cf04b8f9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764221"
---
# <a name="determining-the-windows-installer-version"></a>Determinazione della versione Windows installer

È possibile usare i metodi seguenti per determinare la versione Windows Installer:

-   Chiamare la [**funzione MsiGetFileVersion**](/windows/desktop/api/Msi/nf-msi-msigetfileversiona) con il *parametro szFilePath* impostato sul percorso del file Msi.dll.

    È possibile chiamare la [**funzione SHGetKnownFolderPath**](/windows/win32/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) con la costante **SYSTEM CSIDL \_** per ottenere il percorso Msi.dll. A partire Windows Vista, le applicazioni devono usare la [**funzione SHGetFolderPath**](/windows/win32/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) e **REFKNOWNFOLDERID** "System." Le applicazioni esistenti che usano **la funzione SHGetFolderPath** e il **tipo CSIDL** continueranno a funzionare.

-   Il valore della proprietà [**Installer.Version**](installer-version.md) dell'oggetto [**Installer**](installer-object.md) è equivalente alle stringhe a quattro campi elencate nell'argomento Released [Versions of Windows Installer](released-versions-of-windows-installer.md) .
-   Le applicazioni possono ottenere la Windows installer usando [**DllGetVersion.**](/windows/win32/api/shlwapi/nc-shlwapi-dllgetversionproc)
-   Il programma di installazione imposta [**la proprietà VersionMsi**](versionmsi.md) sulla versione Windows programma di installazione che viene eseguita durante l'installazione.

Per altre informazioni, vedere [Versioni rilasciate di Windows Installer.](released-versions-of-windows-installer.md)

 

 
