---
description: Il gruppo di file di tabelle contiene tutte le tabelle di Windows Installer correlate ai file.
ms.assetid: 8f56328e-ed58-41a1-94b6-266e9c117246
title: Gruppo di tabelle file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2667a1b9fe2bd9d2f8260523e2386bf7751dce8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309476"
---
# <a name="file-tables-group"></a><span data-ttu-id="d5e8f-103">Gruppo di tabelle file</span><span class="sxs-lookup"><span data-stu-id="d5e8f-103">File Tables Group</span></span>

![gruppo di tabelle file](images/filegrp.png)

<span data-ttu-id="d5e8f-105">Per ulteriori informazioni su questo diagramma, vedere la [legenda del diagramma delle relazioni tra entità](entity-relationship-diagram-legend.md).</span><span class="sxs-lookup"><span data-stu-id="d5e8f-105">For more information about this diagram, see the [entity relationship diagram legend](entity-relationship-diagram-legend.md).</span></span>

<span data-ttu-id="d5e8f-106">Uno sviluppatore di pacchetti del programma di installazione deve considerare il popolamento del gruppo di tabelle di file dopo aver suddiviso l'applicazione in [componenti e funzionalità](components-and-features.md) e dopo aver popolato il [gruppo tabelle principali](core-tables-group.md).</span><span class="sxs-lookup"><span data-stu-id="d5e8f-106">An installer package developer should consider populating the file table group of tables after breaking the application into [components and features](components-and-features.md) and after populating the [core tables group](core-tables-group.md).</span></span> <span data-ttu-id="d5e8f-107">Il gruppo di tabelle file contiene tutti i file appartenenti all'installazione e la maggior parte di questi file sono elencati nella [tabella file](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="d5e8f-107">The file table group contains all of the files belonging to the installation and most of these files are listed in the [File table](file-table.md).</span></span> <span data-ttu-id="d5e8f-108">La [tabella di directory](directory-table.md) non viene mostrata nella figura ma è strettamente correlata al gruppo di tabelle di file.</span><span class="sxs-lookup"><span data-stu-id="d5e8f-108">The [Directory table](directory-table.md) is not shown in the figure but is closely related to the file table group.</span></span> <span data-ttu-id="d5e8f-109">La tabella directory fornisce la struttura di directory dell'installazione.</span><span class="sxs-lookup"><span data-stu-id="d5e8f-109">The Directory table gives the directory structure of the installation.</span></span>

<span data-ttu-id="d5e8f-110">Il gruppo di file di tabelle contiene tutte le tabelle correlate ai file.</span><span class="sxs-lookup"><span data-stu-id="d5e8f-110">The file group of tables contains all of the tables that are related to files.</span></span>

-   <span data-ttu-id="d5e8f-111">La [tabella file](file-table.md) elenca i file appartenenti all'installazione.</span><span class="sxs-lookup"><span data-stu-id="d5e8f-111">The [File table](file-table.md) lists files belonging to the installation.</span></span> <span data-ttu-id="d5e8f-112">I file che non sono elencati nella tabella file includono i file su disco, elencati nella tabella media.</span><span class="sxs-lookup"><span data-stu-id="d5e8f-112">Files that are not listed in the File table include disk files, which are listed in Media table.</span></span> <span data-ttu-id="d5e8f-113">Poiché ogni file appartiene a un componente, la tabella dei file include una chiave esterna nella tabella dei componenti.</span><span class="sxs-lookup"><span data-stu-id="d5e8f-113">Because every file belongs to a component, the File table has an external key into the Component table.</span></span>
-   <span data-ttu-id="d5e8f-114">La [tabella RemoveFile](removefile-table.md) contiene un elenco di file che devono essere rimossi dall' [azione RemoveFiles](removefiles-action.md).</span><span class="sxs-lookup"><span data-stu-id="d5e8f-114">The [RemoveFile table](removefile-table.md) contains a list of files to be removed by the [RemoveFiles action](removefiles-action.md).</span></span>
-   <span data-ttu-id="d5e8f-115">La [tabella dei tipi](font-table.md) di carattere elenca i file dei tipi di carattere da registrare nel sistema.</span><span class="sxs-lookup"><span data-stu-id="d5e8f-115">The [Font table](font-table.md) lists font files to be registered with the system.</span></span>
-   <span data-ttu-id="d5e8f-116">La [tabella SelfReg](selfreg-table.md) elenca i file di modulo dell'installazione che sono autofirmati.</span><span class="sxs-lookup"><span data-stu-id="d5e8f-116">The [SelfReg table](selfreg-table.md) lists module files of the installation that are self-registered.</span></span>
-   <span data-ttu-id="d5e8f-117">La [tabella media](media-table.md) elenca i supporti di origine e i dischi appartenenti all'installazione.</span><span class="sxs-lookup"><span data-stu-id="d5e8f-117">The [Media table](media-table.md) lists the source media and disks belonging to the installation.</span></span>
-   <span data-ttu-id="d5e8f-118">La [tabella azione BindImage sul](bindimage-table.md) elenca i file associati alle DLL importate da file eseguibili.</span><span class="sxs-lookup"><span data-stu-id="d5e8f-118">The [BindImage table](bindimage-table.md) lists files that are bound to DLLs imported by executables.</span></span>
-   <span data-ttu-id="d5e8f-119">La [tabella MoveFile](movefile-table.md) specifica quali file vengono spostati durante l'installazione.</span><span class="sxs-lookup"><span data-stu-id="d5e8f-119">The [MoveFile table](movefile-table.md) specifies which files are moved during the installation.</span></span>
-   <span data-ttu-id="d5e8f-120">La [tabella DuplicateFile](duplicatefile-table.md) specifica quali file vengono duplicati durante l'installazione.</span><span class="sxs-lookup"><span data-stu-id="d5e8f-120">The [DuplicateFile table](duplicatefile-table.md) specifies which files are duplicated during the installation.</span></span>
-   <span data-ttu-id="d5e8f-121">La [tabella inifile](inifile-table.md) elenca i file ini e le informazioni che l'applicazione deve impostare nel file.</span><span class="sxs-lookup"><span data-stu-id="d5e8f-121">The [IniFile table](inifile-table.md) lists the .ini files and the information that the application needs to set in the file.</span></span>
-   <span data-ttu-id="d5e8f-122">La [tabella RemoveIniFile](removeinifile-table.md) contiene le informazioni che un'applicazione deve eliminare da un file ini.</span><span class="sxs-lookup"><span data-stu-id="d5e8f-122">The [RemoveIniFile table](removeinifile-table.md) contains the information an application needs to delete from a .ini file.</span></span>
-   <span data-ttu-id="d5e8f-123">La [tabella Environment](environment-table.md) viene utilizzata per impostare i valori delle variabili di ambiente.</span><span class="sxs-lookup"><span data-stu-id="d5e8f-123">The [Environment table](environment-table.md) is used to set the values of environment variables.</span></span>
-   <span data-ttu-id="d5e8f-124">Nella [tabella icone](icon-table.md) sono disponibili informazioni sull'icona che vengono copiate in un file come parte dell'annuncio del prodotto.</span><span class="sxs-lookup"><span data-stu-id="d5e8f-124">The [Icon table](icon-table.md) provides icon information which is copied to a file as a part of product advertisement.</span></span>
-   <span data-ttu-id="d5e8f-125">La [tabella FileSFPCatalog](filesfpcatalog-table.md) associa i file specificati ai file del catalogo di protezione dei file di sistema.</span><span class="sxs-lookup"><span data-stu-id="d5e8f-125">The [FileSFPCatalog table](filesfpcatalog-table.md) associates specified files with system file protection catalog files.</span></span>

    <span data-ttu-id="d5e8f-126">**Windows Vista, Windows Server 2003 e Windows XP:** Non supportato.</span><span class="sxs-lookup"><span data-stu-id="d5e8f-126">**Windows Vista, Windows Server 2003 and Windows XP:** Not supported.</span></span>

-   <span data-ttu-id="d5e8f-127">La [tabella SFPCatalog](sfpcatalog-table.md) contiene cataloghi di protezione dei file di sistema.</span><span class="sxs-lookup"><span data-stu-id="d5e8f-127">The [SFPCatalog table](sfpcatalog-table.md) contains system file protection catalogs.</span></span>

    <span data-ttu-id="d5e8f-128">**Windows Vista, Windows Server 2003 e Windows XP:** Non supportato.</span><span class="sxs-lookup"><span data-stu-id="d5e8f-128">**Windows Vista, Windows Server 2003 and Windows XP:** Not supported.</span></span>

-   <span data-ttu-id="d5e8f-129">La [tabella MsiFileHash](msifilehash-table.md) viene utilizzata per archiviare un hash a 128 bit di un file di origine fornito dal pacchetto Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="d5e8f-129">The [MsiFileHash table](msifilehash-table.md) is used to store a 128-bit hash of a source file provided by the Windows Installer package.</span></span>

 

 



