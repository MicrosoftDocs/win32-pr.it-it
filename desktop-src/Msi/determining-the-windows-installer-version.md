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
# <a name="determining-the-windows-installer-version"></a><span data-ttu-id="44ebf-103">Determinazione della versione di Windows Installer</span><span class="sxs-lookup"><span data-stu-id="44ebf-103">Determining the Windows Installer Version</span></span>

<span data-ttu-id="44ebf-104">Per determinare la versione Windows Installer, è possibile utilizzare i metodi seguenti:</span><span class="sxs-lookup"><span data-stu-id="44ebf-104">You can use the following methods to determine the Windows Installer version:</span></span>

-   <span data-ttu-id="44ebf-105">Chiamare la funzione [**MsiGetFileVersion**](/windows/desktop/api/Msi/nf-msi-msigetfileversiona) con il parametro *szFilePath* impostato sul percorso del file Msi.dll.</span><span class="sxs-lookup"><span data-stu-id="44ebf-105">Call the [**MsiGetFileVersion**](/windows/desktop/api/Msi/nf-msi-msigetfileversiona) function with the *szFilePath* parameter set to the path to the file Msi.dll.</span></span>

    <span data-ttu-id="44ebf-106">È possibile chiamare la funzione [**SHGetKnownFolderPath**](/windows/win32/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) con la costante di **\_ sistema CSIDL** per ottenere il percorso Msi.dll.</span><span class="sxs-lookup"><span data-stu-id="44ebf-106">You can call the [**SHGetKnownFolderPath**](/windows/win32/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) function with the **CSIDL\_SYSTEM** constant to get the path to Msi.dll.</span></span> <span data-ttu-id="44ebf-107">A partire da Windows Vista, le applicazioni devono utilizzare la funzione [**SHGetFolderPath**](/windows/win32/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) e **REFKNOWNFOLDERID** "System".</span><span class="sxs-lookup"><span data-stu-id="44ebf-107">Beginning with Windows Vista, applications should use the [**SHGetFolderPath**](/windows/win32/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) function and the **REFKNOWNFOLDERID** "System."</span></span> <span data-ttu-id="44ebf-108">Le applicazioni esistenti che usano la funzione **SHGetFolderPath** e il tipo **CSIDL** continueranno a funzionare.</span><span class="sxs-lookup"><span data-stu-id="44ebf-108">Existing applications that use the **SHGetFolderPath** function and the **CSIDL** type will continue to work.</span></span>

-   <span data-ttu-id="44ebf-109">Il valore della proprietà [**Installer. Version**](installer-version.md) dell' [**oggetto Installer**](installer-object.md) è equivalente alle stringhe di quattro campi elencate nelle [versioni rilasciate di Windows Installer](released-versions-of-windows-installer.md) argomento.</span><span class="sxs-lookup"><span data-stu-id="44ebf-109">The value of the [**Installer.Version**](installer-version.md) property of the [**Installer Object**](installer-object.md) is equivalent to the four-field strings listed in the [Released Versions of Windows Installer](released-versions-of-windows-installer.md) topic.</span></span>
-   <span data-ttu-id="44ebf-110">Le applicazioni possono ottenere la versione Windows Installer usando [**DllGetVersion**](/windows/win32/api/shlwapi/nc-shlwapi-dllgetversionproc).</span><span class="sxs-lookup"><span data-stu-id="44ebf-110">Applications can get the Windows Installer version by using [**DllGetVersion**](/windows/win32/api/shlwapi/nc-shlwapi-dllgetversionproc).</span></span>
-   <span data-ttu-id="44ebf-111">Il programma di installazione imposta la proprietà [**VersionMsi**](versionmsi.md) sulla versione di Windows Installer eseguita durante l'installazione.</span><span class="sxs-lookup"><span data-stu-id="44ebf-111">The installer sets the [**VersionMsi**](versionmsi.md) property to the version of Windows Installer that is run during the installation.</span></span>

<span data-ttu-id="44ebf-112">Per ulteriori informazioni, vedere [versioni rilasciate di Windows Installer](released-versions-of-windows-installer.md).</span><span class="sxs-lookup"><span data-stu-id="44ebf-112">For more information, see [Released Versions of Windows Installer](released-versions-of-windows-installer.md).</span></span>

 

 
