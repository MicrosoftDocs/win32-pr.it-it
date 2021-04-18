---
description: Prima di poter aggiungere o rimuovere operazioni di file dall'elenco spazio su disco, è necessario crearlo utilizzando la funzione SetupCreateDiskSpaceList.
ms.assetid: 287fd84a-dc8c-4a5c-b998-db5f2fbee5f1
title: Uso dell'elenco Disk-Space
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a19f100fd5190472f5f6bfebaf74affe1a789cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310742"
---
# <a name="using-the-disk-space-list"></a><span data-ttu-id="977cd-103">Uso dell'elenco Disk-Space</span><span class="sxs-lookup"><span data-stu-id="977cd-103">Using the Disk-Space List</span></span>

<span data-ttu-id="977cd-104">Prima di poter aggiungere o rimuovere operazioni di file dall'elenco spazio su disco, è necessario crearlo utilizzando la funzione [**SetupCreateDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupcreatediskspacelista) .</span><span class="sxs-lookup"><span data-stu-id="977cd-104">Before you can add or remove file operations from the disk-space list, you must create it by using the [**SetupCreateDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupcreatediskspacelista) function.</span></span>

<span data-ttu-id="977cd-105">Dopo aver creato un elenco di spazio su disco, è possibile aggiungere singole operazioni di copia o eliminazione di file all'elenco usando [**SetupAddToDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupaddtodiskspacelista).</span><span class="sxs-lookup"><span data-stu-id="977cd-105">After you create a disk-space list you can add individual file copy or delete operations to the list by using [**SetupAddToDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupaddtodiskspacelista).</span></span> <span data-ttu-id="977cd-106">Per aggiungere tutte le operazioni di copia o eliminazione di file in un'intera sezione INF, usare la funzione [**SetupAddSectionToDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupaddsectiontodiskspacelista) o [**SetupAddInstallSectionToDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupaddinstallsectiontodiskspacelista) .</span><span class="sxs-lookup"><span data-stu-id="977cd-106">To add all the file copy or delete operations in an entire INF section, use either the [**SetupAddSectionToDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupaddsectiontodiskspacelista) or [**SetupAddInstallSectionToDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupaddinstallsectiontodiskspacelista) function.</span></span>

<span data-ttu-id="977cd-107">Dopo aver aggiunto tutte le operazioni di installazione nell'elenco spazio su disco, è possibile eseguire una query per verificare la quantità di spazio su disco necessaria per l'installazione specificata tramite la funzione [**SetupQuerySpaceRequiredOnDrive**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryspacerequiredondrivea) .</span><span class="sxs-lookup"><span data-stu-id="977cd-107">After you add all the installation operations to the disk-space list, you can query it to find out how much disk space is required for the specified installation by using the [**SetupQuerySpaceRequiredOnDrive**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryspacerequiredondrivea) function.</span></span>

<span data-ttu-id="977cd-108">La funzione [**SetupQueryDrivesInDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupquerydrivesindiskspacelista) restituisce le specifiche di unità per ogni unità di destinazione a cui si fa riferimento nelle operazioni sui file nell'elenco spazio su disco.</span><span class="sxs-lookup"><span data-stu-id="977cd-108">The [**SetupQueryDrivesInDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupquerydrivesindiskspacelista) function returns the drive specifications for each target drive referenced in the file operations on the disk-space list.</span></span> <span data-ttu-id="977cd-109">È possibile usare queste informazioni per confrontare a livello di codice lo spazio disponibile in queste unità con lo spazio necessario per l'installazione.</span><span class="sxs-lookup"><span data-stu-id="977cd-109">You can use this information to programmatically compare the available space on these drives with the space required by the installation.</span></span>

<span data-ttu-id="977cd-110">Per rimuovere un'operazione su file dall'elenco spazio su disco, usare la funzione [**SetupRemoveFromDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupremovefromdiskspacelista) .</span><span class="sxs-lookup"><span data-stu-id="977cd-110">To remove a file operation from the disk-space list, use the [**SetupRemoveFromDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupremovefromdiskspacelista) function.</span></span> <span data-ttu-id="977cd-111">Per rimuovere tutte le operazioni di copia o eliminazione di file da un'intera sezione INF, usare la funzione [**SetupRemoveSectionFromDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupremovesectionfromdiskspacelista) o [**SetupRemoveInstallSectionFromDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupremoveinstallsectionfromdiskspacelista) .</span><span class="sxs-lookup"><span data-stu-id="977cd-111">To remove all file copy or delete operations from an entire INF section, use the [**SetupRemoveSectionFromDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupremovesectionfromdiskspacelista) or [**SetupRemoveInstallSectionFromDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupremoveinstallsectionfromdiskspacelista) function.</span></span>

<span data-ttu-id="977cd-112">Una volta che l'elenco spazio su disco non è più necessario, è possibile rilasciare le risorse allocate chiamando la funzione [**SetupDestroyDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupdestroydiskspacelist) .</span><span class="sxs-lookup"><span data-stu-id="977cd-112">After the disk-space list is no longer required, you can release the resources allocated to it by calling the [**SetupDestroyDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupdestroydiskspacelist) function.</span></span>

 

 



