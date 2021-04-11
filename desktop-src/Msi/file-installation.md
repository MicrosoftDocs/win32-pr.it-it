---
description: 'Una volta completato il costo del file, il programma di installazione dispone di tutte le informazioni necessarie per elaborare le due azioni di manipolazione dei file: DuplicateFiles e MoveFiles.'
ms.assetid: 2e6d6eb3-1e71-46e6-a946-d9cc0b209325
title: Installazione file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 472c58db3dc2e9094a26d57f871359a38930877b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131786"
---
# <a name="file-installation"></a><span data-ttu-id="1a513-103">Installazione file</span><span class="sxs-lookup"><span data-stu-id="1a513-103">File Installation</span></span>

<span data-ttu-id="1a513-104">Una volta completato il [costo del file](file-costing.md) , il programma di installazione dispone di tutte le informazioni necessarie per elaborare le due azioni di manipolazione dei file: [DuplicateFiles](duplicatefiles-action.md) e [MoveFiles](movefiles-action.md).</span><span class="sxs-lookup"><span data-stu-id="1a513-104">Once [file costing](file-costing.md) has been completed, the installer has all the information required to process the two file manipulation actions: [DuplicateFiles](duplicatefiles-action.md) and [MoveFiles](movefiles-action.md).</span></span>

<span data-ttu-id="1a513-105">Usare l' [azione DuplicateFiles](duplicatefiles-action.md) per specificare i file che il programma di installazione deve duplicare nella [tabella DuplicateFile](duplicatefile-table.md).</span><span class="sxs-lookup"><span data-stu-id="1a513-105">Use the [DuplicateFiles action](duplicatefiles-action.md) to specify the files the installer is to duplicate in the [DuplicateFile table](duplicatefile-table.md).</span></span> <span data-ttu-id="1a513-106">Usare l' [azione MoveFiles](movefiles-action.md)per determinare i file da spostare eseguendo una query sulla [tabella MoveFile](movefile-table.md).</span><span class="sxs-lookup"><span data-stu-id="1a513-106">Use the [MoveFiles action](movefiles-action.md)to determine which files to move by querying the [MoveFile table](movefile-table.md).</span></span>

<span data-ttu-id="1a513-107">Si noti che il campo Options della [tabella MoveFile](movefile-table.md) specifica se il file originale deve essere eliminato dal percorso corrente.</span><span class="sxs-lookup"><span data-stu-id="1a513-107">Note that the Options field of the [MoveFile table](movefile-table.md) specifies whether or not the original file is to be deleted from its current location.</span></span> <span data-ttu-id="1a513-108">I file che vengono spostati o copiati dall'azione MoveFiles non vengono eliminati quando il prodotto viene disinstallato.</span><span class="sxs-lookup"><span data-stu-id="1a513-108">Files that are moved or copied by the MoveFiles action are not deleted when the product is uninstalled.</span></span>

<span data-ttu-id="1a513-109">L' [azione InstallFiles](installfiles-action.md) viene chiamata dopo che tutte le altre operazioni di manipolazione dei file sono state completate.</span><span class="sxs-lookup"><span data-stu-id="1a513-109">The [InstallFiles action](installfiles-action.md) is called once all other file manipulation operations have completed.</span></span> <span data-ttu-id="1a513-110">L'azione InstallFiles elabora la [tabella dei supporti](media-table.md), la [tabella dei file](file-table.md)e la tabella dei [componenti](component-table.md) per determinare quali file verranno copiati dall'origine alla destinazione.</span><span class="sxs-lookup"><span data-stu-id="1a513-110">The InstallFiles action processes the [Media table](media-table.md), the [File table](file-table.md), and the [Component table](component-table.md) to determine which files will be copied from the source to the destination.</span></span>

<span data-ttu-id="1a513-111">L' [azione InstallFiles](installfiles-action.md) crea la struttura di directory necessaria per installare tutti i file.</span><span class="sxs-lookup"><span data-stu-id="1a513-111">The [InstallFiles action](installfiles-action.md) creates the directory structure necessary to install all files.</span></span> <span data-ttu-id="1a513-112">Se è necessario installare una cartella vuota in modo esplicito, è possibile chiamare l' [azione CreateFolders](createfolders-action.md) per crearla.</span><span class="sxs-lookup"><span data-stu-id="1a513-112">If an explicitly empty folder is required to be installed, the [CreateFolders action](createfolders-action.md) may be called to create it.</span></span>

 

 



