---
description: Come determinare se una directory specificata è una cartella montata.
ms.assetid: b4a2c3d7-8805-41de-b316-592e77076570
title: Determinare se una directory è una cartella montata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ca7492a3114ff0c9c9ce0685c6d3e2b94724457
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884341"
---
# <a name="determining-whether-a-directory-is-a-mounted-folder"></a><span data-ttu-id="8a8a5-103">Determinare se una directory è una cartella montata</span><span class="sxs-lookup"><span data-stu-id="8a8a5-103">Determining Whether a Directory Is a Mounted Folder</span></span>

<span data-ttu-id="8a8a5-104">È utile determinare se una directory è una cartella montata quando, ad esempio, si usa un'applicazione di backup o di ricerca limitata a un volume.</span><span class="sxs-lookup"><span data-stu-id="8a8a5-104">It is useful to determine whether a directory is a mounted folder when, for example, you are using a backup or search application that is limited to one volume.</span></span> <span data-ttu-id="8a8a5-105">Un'applicazione di questo tipo può raggiungere informazioni su più volumi se si usano funzioni come [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) per creare cartelle montate per gli altri volumi del volume a cui l'applicazione è limitata.</span><span class="sxs-lookup"><span data-stu-id="8a8a5-105">Such an application can reach information on multiple volumes if you use functions such as [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) to create mounted folders for the other volumes on the volume that the application is limited to.</span></span> <span data-ttu-id="8a8a5-106">Per ulteriori informazioni, vedere [creazione di cartelle montate](mounting-and-dismounting-a-volume.md).</span><span class="sxs-lookup"><span data-stu-id="8a8a5-106">For more information, see [Creating Mounted Folders](mounting-and-dismounting-a-volume.md).</span></span>

<span data-ttu-id="8a8a5-107">Per determinare se una directory specificata è una cartella montata, chiamare prima la funzione [**GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa) ed esaminare il flag di **\_ \_ reparse \_ Point dell'attributo file** nel valore restituito per verificare se alla directory è associato un reparse point.</span><span class="sxs-lookup"><span data-stu-id="8a8a5-107">To determine if a specified directory is a mounted folder, first call the [**GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa) function and inspect the **FILE\_ATTRIBUTE\_REPARSE\_POINT** flag in the return value to see if the directory has an associated reparse point.</span></span> <span data-ttu-id="8a8a5-108">In caso contrario, usare le funzioni [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea) e [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea) per ottenere il tag reparse nel membro **dwReserved0** della struttura di [**\_ \_ dati Find di Win32**](/windows/desktop/api/MinWinBase/ns-minwinbase-win32_find_dataa) .</span><span class="sxs-lookup"><span data-stu-id="8a8a5-108">If it does, use the [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea) and [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea) functions to obtain the reparse tag in the **dwReserved0** member of the [**WIN32\_FIND\_DATA**](/windows/desktop/api/MinWinBase/ns-minwinbase-win32_find_dataa) structure.</span></span> <span data-ttu-id="8a8a5-109">Per determinare se il reparse point è una cartella montata (e non un'altra forma di punto di analisi), verificare se il valore del tag è uguale **al \_ \_ \_ \_ punto di montaggio del tag** di i/o del valore.</span><span class="sxs-lookup"><span data-stu-id="8a8a5-109">To determine if the reparse point is a mounted folder (and not some other form of reparse point), test whether the tag value equals the value **IO\_REPARSE\_TAG\_MOUNT\_POINT**.</span></span> <span data-ttu-id="8a8a5-110">Per ulteriori informazioni, vedere [reparse point](reparse-points.md).</span><span class="sxs-lookup"><span data-stu-id="8a8a5-110">For more information, see [Reparse Points](reparse-points.md).</span></span>

<span data-ttu-id="8a8a5-111">Per ottenere il volume di destinazione di una cartella montata, usare la funzione [**GetVolumeNameForVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumenameforvolumemountpointw) .</span><span class="sxs-lookup"><span data-stu-id="8a8a5-111">To obtain the target volume of a mounted folder, use the [**GetVolumeNameForVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumenameforvolumemountpointw) function.</span></span>

<span data-ttu-id="8a8a5-112">In modo analogo, è possibile determinare se un reparse point è un collegamento simbolico verificando se il valore del tag è l'i/o di **\_ reparse \_ tag \_** simbolico.</span><span class="sxs-lookup"><span data-stu-id="8a8a5-112">In a similar manner, you can determine if a reparse point is a symbolic link by testing whether the tag value is **IO\_REPARSE\_TAG\_SYMLINK**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8a8a5-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8a8a5-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8a8a5-114">**Costanti di attributi file**</span><span class="sxs-lookup"><span data-stu-id="8a8a5-114">**File Attribute Constants**</span></span>](file-attribute-constants.md)
</dt> </dl>

 

 



