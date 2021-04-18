---
description: La sezione install di un file INF definisce i passaggi della procedura di installazione.
ms.assetid: 24d40dc6-ac09-4cf8-9229-f81da2925576
title: Esempio di sezione di installazione INF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39c8162dbf06b87faf8a1ce432c361a28befca0d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315325"
---
# <a name="inf-install-section-example"></a><span data-ttu-id="185bc-103">Esempio di sezione di installazione INF</span><span class="sxs-lookup"><span data-stu-id="185bc-103">INF Install Section Example</span></span>

<span data-ttu-id="185bc-104">La sezione **Install** di un file inf definisce i passaggi della procedura di installazione.</span><span class="sxs-lookup"><span data-stu-id="185bc-104">The **Install** section of an INF File defines the steps of the installation procedure.</span></span> <span data-ttu-id="185bc-105">Ogni riga di una sezione di **installazione** è costituita da due parti.</span><span class="sxs-lookup"><span data-stu-id="185bc-105">Each line of an **Install** section has two parts.</span></span> <span data-ttu-id="185bc-106">A sinistra del segno di uguale (=) è la chiave.</span><span class="sxs-lookup"><span data-stu-id="185bc-106">On the left of the equals sign (=) is the key.</span></span> <span data-ttu-id="185bc-107">Sul lato destro è disponibile un elenco di uno o più titoli di sezione.</span><span class="sxs-lookup"><span data-stu-id="185bc-107">On the right hand side, is a list of one or more section titles.</span></span> <span data-ttu-id="185bc-108">La chiave specifica il tipo di sezioni elencate a destra.</span><span class="sxs-lookup"><span data-stu-id="185bc-108">The key specifies the type of the sections that are listed on the right.</span></span> <span data-ttu-id="185bc-109">Per una descrizione del formato di questa sezione, vedere le sezioni e le direttive dei file INF del Microsoft Windows 2000 Driver Development Kit.</span><span class="sxs-lookup"><span data-stu-id="185bc-109">For a description of this section's format see the "INF File Sections and Directives" of the Microsoft Windows 2000 Driver Development Kit.</span></span>

<span data-ttu-id="185bc-110">Di seguito è riportato un esempio di una sezione di **installazione** .</span><span class="sxs-lookup"><span data-stu-id="185bc-110">The following is an example of an **Install** section.</span></span>

``` syntax
[MyInstallSection]
Copyfiles=DataFiles, ProgramFiles
Delfiles=OldFiles
UpdateInis=NewIniInfo
AddReg=NewRegistryInfo, MoreNewRegistryInfo
DelReg=OldRegistryInfo, MoreOldRegistryInfo
```

<span data-ttu-id="185bc-111">In questo esempio la chiave **CopyFiles** è impostata sui valori "DataFiles" e "ProgramFiles".</span><span class="sxs-lookup"><span data-stu-id="185bc-111">In this example the **CopyFiles** key is set to the values "DataFiles" and "ProgramFiles".</span></span> <span data-ttu-id="185bc-112">Vengono specificate due sezioni **copia file** nel file inf che contengono i nomi dei file di origine utilizzati per la copia delle operazioni.</span><span class="sxs-lookup"><span data-stu-id="185bc-112">This specifies two **Copy Files** sections in the INF file that contain the names of the source files used by copying operations.</span></span> <span data-ttu-id="185bc-113">La destinazione per i file copiati verrebbe specificata in una sezione **DestinationDirs** nel file inf.</span><span class="sxs-lookup"><span data-stu-id="185bc-113">The destination for the copied files would be specified in a **DestinationDirs** section in the INF file.</span></span>

<span data-ttu-id="185bc-114">Alla chiave **delfiles** viene assegnato il valore "OldFiles".</span><span class="sxs-lookup"><span data-stu-id="185bc-114">The **Delfiles** key is given the value "OldFiles".</span></span> <span data-ttu-id="185bc-115">Viene specificata una sezione **Delete Files** che contiene informazioni rilevanti per le operazioni di eliminazione di file.</span><span class="sxs-lookup"><span data-stu-id="185bc-115">This specifies a **Delete Files** section that contains information relevant to file deletion operations.</span></span>

<span data-ttu-id="185bc-116">La chiave **UpdateInis** specifica le sezioni del **file ini di aggiornamento** contenenti informazioni sull'aggiornamento delle voci nel file ini.</span><span class="sxs-lookup"><span data-stu-id="185bc-116">The **UpdateInis** key specifies **Update INI File** sections that contain information about updating entries in the INI file.</span></span>

<span data-ttu-id="185bc-117">Le chiavi **AddReg** e **DelReg** specificano le sezioni **Add Registry** ed **Delete** Registry contenenti informazioni sull'aggiunta o l'eliminazione di informazioni del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="185bc-117">The **AddReg** and **DelReg** keys specify **Add Registry** and **Delete Registry** sections that contain information about adding or deleting registry information.</span></span>

 

 



