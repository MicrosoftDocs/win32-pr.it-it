---
description: La sezione SourceDisksNames di un file INF identifica i dischi che contengono i file di origine da installare.
ms.assetid: af4bc466-f0a3-4f83-adb7-6bfc276f7764
title: Esempio di sezioni INF SourceDisksNames e SourceDisksFiles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f991727a8a2ca9cce2bd2d7161dfbf27b62ce74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315323"
---
# <a name="inf-sourcedisksnames-and-sourcedisksfiles-sections-example"></a><span data-ttu-id="e9919-103">Esempio di sezioni INF SourceDisksNames e SourceDisksFiles</span><span class="sxs-lookup"><span data-stu-id="e9919-103">INF SourceDisksNames and SourceDisksFiles Sections Example</span></span>

<span data-ttu-id="e9919-104">La sezione **SourceDisksNames** di un file inf identifica i dischi che contengono i file di origine da installare.</span><span class="sxs-lookup"><span data-stu-id="e9919-104">The **SourceDisksNames** section of an INF file identifies the disks that contain the source files being installed.</span></span> <span data-ttu-id="e9919-105">La sezione **SourceDisksFiles** identifica i file di origine e i dischi di origine che li contengono.</span><span class="sxs-lookup"><span data-stu-id="e9919-105">The **SourceDisksFiles** section identifies the source files and the source disks that contain them.</span></span> <span data-ttu-id="e9919-106">Si noti che le piattaforme MIPS, Alpha e PPC non sono supportate da Windows 2000 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="e9919-106">Note that MIPS, Alpha, and PPC platforms are not supported by Windows 2000 or Windows XP.</span></span>

<span data-ttu-id="e9919-107">A partire da Windows XP, una sezione **SourceDisksNames** può specificare un tag e un file CAB.</span><span class="sxs-lookup"><span data-stu-id="e9919-107">Beginning with Windows XP, a **SourceDisksNames** section may specify a tag as well as cabinet file.</span></span> <span data-ttu-id="e9919-108">Ad esempio, la sezione **SourceDisksNames** seguente può essere utilizzata con supporti rimovibili o fissi.</span><span class="sxs-lookup"><span data-stu-id="e9919-108">For example, the following **SourceDisksNames** section may be used with removable or fixed media.</span></span> <span data-ttu-id="e9919-109">Se si usa un supporto rimovibile, nella sezione di esempio viene verificata la presenza del supporto controllando prima di tutto la presenza del tag.</span><span class="sxs-lookup"><span data-stu-id="e9919-109">If using removable media, the example section verifies the presence of the media by first checking for the presence of the tag.</span></span> <span data-ttu-id="e9919-110">Se si usa un supporto fisso, nella sezione di esempio viene verificata la presenza del supporto controllando prima di tutto la presenza del cabinet.</span><span class="sxs-lookup"><span data-stu-id="e9919-110">If using fixed media, the example section verifies the presence of the media by first checking for the presence of the cabinet.</span></span> <span data-ttu-id="e9919-111">Dopo aver verificato la presenza di un file CAB, il sistema tenta di copiare i file all'esterno dell'archivio e di richiedere eventuali file che non sono stati copiati.</span><span class="sxs-lookup"><span data-stu-id="e9919-111">After verifying the presence of a cabinet, the system attempts to copy files out of the cabinet and prompts for any files it was unable to copy.</span></span>

``` syntax
[SourceDisksNames]
1="Dajava" , "Dajava.cab",,, 0x10,"Dajava.tag"
```

<span data-ttu-id="e9919-112">Per ulteriori informazioni su **SourceDisksNames** o **SourceDisksFiles**, vedere le sezioni "linee guida generali per file inf" e "sezioni e DIRETTIVe dei file inf" del Microsoft Windows 2000 Driver Development Kit.</span><span class="sxs-lookup"><span data-stu-id="e9919-112">For more information about **SourceDisksNames** or **SourceDisksFiles**, see the "General Guidelines for INF File" and "INF File Sections and Directives" sections of the Microsoft Windows 2000 Driver Development Kit.</span></span>

 

 



