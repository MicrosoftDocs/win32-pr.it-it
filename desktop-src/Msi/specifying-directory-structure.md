---
description: Il programma di installazione mantiene le informazioni sulla struttura della directory di installazione nella tabella directory.
ms.assetid: 31390138-b1d0-4f0b-9304-6e7c69e6a736
title: Specifica della struttura di directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80a87880921799158559e28fed2c6dde97c9a331
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879553"
---
# <a name="specifying-directory-structure"></a><span data-ttu-id="38cb5-103">Specifica della struttura di directory</span><span class="sxs-lookup"><span data-stu-id="38cb5-103">Specifying Directory Structure</span></span>

<span data-ttu-id="38cb5-104">Il programma di installazione mantiene le informazioni sulla struttura della directory di installazione nella [tabella directory](directory-table.md).</span><span class="sxs-lookup"><span data-stu-id="38cb5-104">The installer keeps information about the installation directory structure in the [Directory Table](directory-table.md).</span></span> <span data-ttu-id="38cb5-105">Vedere il [gruppo tabelle principali](core-tables-group.md).</span><span class="sxs-lookup"><span data-stu-id="38cb5-105">See the [Core Tables Group](core-tables-group.md).</span></span> <span data-ttu-id="38cb5-106">In questa sezione è possibile aggiungere informazioni sulla struttura di directory per l'esempio del blocco note al database vuoto creato durante l' [importazione di un database vuoto](importing-a-blank-database.md).</span><span class="sxs-lookup"><span data-stu-id="38cb5-106">In this section you add directory structure information for the Notepad sample to the empty database you created in [Importing a Blank Database](importing-a-blank-database.md).</span></span> <span data-ttu-id="38cb5-107">Utilizzare l'editor di database Orca fornito con l'SDK o un altro editor per aprire la tabella di directory in MNP2000.msi.</span><span class="sxs-lookup"><span data-stu-id="38cb5-107">Use the database editor Orca that is provided with the SDK, or another editor, to open the Directory Table in MNP2000.msi.</span></span> <span data-ttu-id="38cb5-108">Utilizzare l'editor per immettere i dati seguenti nella tabella directory vuota.</span><span class="sxs-lookup"><span data-stu-id="38cb5-108">Use the editor to enter the following data into the blank Directory table.</span></span>

[<span data-ttu-id="38cb5-109">Tabella directory</span><span class="sxs-lookup"><span data-stu-id="38cb5-109">Directory Table</span></span>](directory-table.md)



| <span data-ttu-id="38cb5-110">Directory</span><span class="sxs-lookup"><span data-stu-id="38cb5-110">Directory</span></span>                                        | <span data-ttu-id="38cb5-111">\_Padre directory</span><span class="sxs-lookup"><span data-stu-id="38cb5-111">Directory\_Parent</span></span>                                | <span data-ttu-id="38cb5-112">DefaultDir</span><span class="sxs-lookup"><span data-stu-id="38cb5-112">DefaultDir</span></span>        |
|--------------------------------------------------|--------------------------------------------------|-------------------|
| [<span data-ttu-id="38cb5-113">**TARGETDIR**</span><span class="sxs-lookup"><span data-stu-id="38cb5-113">**TARGETDIR**</span></span>](targetdir.md)                   |                                                  | <span data-ttu-id="38cb5-114">SourceDir</span><span class="sxs-lookup"><span data-stu-id="38cb5-114">SourceDir</span></span>         |
| [<span data-ttu-id="38cb5-115">**ProgramFilesFolder**</span><span class="sxs-lookup"><span data-stu-id="38cb5-115">**ProgramFilesFolder**</span></span>](programfilesfolder.md) | [<span data-ttu-id="38cb5-116">**TARGETDIR**</span><span class="sxs-lookup"><span data-stu-id="38cb5-116">**TARGETDIR**</span></span>](targetdir.md)                   | <span data-ttu-id="38cb5-117">.</span><span class="sxs-lookup"><span data-stu-id="38cb5-117">.</span></span>                 |
| <span data-ttu-id="38cb5-118">ARTSDIR</span><span class="sxs-lookup"><span data-stu-id="38cb5-118">ARTSDIR</span></span>                                          | <span data-ttu-id="38cb5-119">NOTEPADDIR</span><span class="sxs-lookup"><span data-stu-id="38cb5-119">NOTEPADDIR</span></span>                                       | <span data-ttu-id="38cb5-120">Arts: eventi</span><span class="sxs-lookup"><span data-stu-id="38cb5-120">Arts:Events</span></span>       |
| <span data-ttu-id="38cb5-121">HOLDIR</span><span class="sxs-lookup"><span data-stu-id="38cb5-121">HOLDIR</span></span>                                           | <span data-ttu-id="38cb5-122">MONDIno</span><span class="sxs-lookup"><span data-stu-id="38cb5-122">MONDIR</span></span>                                           | <span data-ttu-id="38cb5-123">.: Festività</span><span class="sxs-lookup"><span data-stu-id="38cb5-123">.:Holidays</span></span>        |
| <span data-ttu-id="38cb5-124">MENUDIR</span><span class="sxs-lookup"><span data-stu-id="38cb5-124">MENUDIR</span></span>                                          | <span data-ttu-id="38cb5-125">NOTEPADDIR</span><span class="sxs-lookup"><span data-stu-id="38cb5-125">NOTEPADDIR</span></span>                                       | <span data-ttu-id="38cb5-126">Menu</span><span class="sxs-lookup"><span data-stu-id="38cb5-126">Menu</span></span>              |
| <span data-ttu-id="38cb5-127">MONDIno</span><span class="sxs-lookup"><span data-stu-id="38cb5-127">MONDIR</span></span>                                           | <span data-ttu-id="38cb5-128">NOTEPADDIR</span><span class="sxs-lookup"><span data-stu-id="38cb5-128">NOTEPADDIR</span></span>                                       | <span data-ttu-id="38cb5-129">Cancello</span><span class="sxs-lookup"><span data-stu-id="38cb5-129">Gate</span></span>              |
| <span data-ttu-id="38cb5-130">NOTEPADDIR</span><span class="sxs-lookup"><span data-stu-id="38cb5-130">NOTEPADDIR</span></span>                                       | [<span data-ttu-id="38cb5-131">**ProgramFilesFolder**</span><span class="sxs-lookup"><span data-stu-id="38cb5-131">**ProgramFilesFolder**</span></span>](programfilesfolder.md) | <span data-ttu-id="38cb5-132">Red \_ Park: blocco note</span><span class="sxs-lookup"><span data-stu-id="38cb5-132">Red\_Park:Notepad</span></span> |
| <span data-ttu-id="38cb5-133">SPORTDIR</span><span class="sxs-lookup"><span data-stu-id="38cb5-133">SPORTDIR</span></span>                                         | <span data-ttu-id="38cb5-134">NOTEPADDIR</span><span class="sxs-lookup"><span data-stu-id="38cb5-134">NOTEPADDIR</span></span>                                       | <span data-ttu-id="38cb5-135">Sport: eventi</span><span class="sxs-lookup"><span data-stu-id="38cb5-135">Sports:Events</span></span>     |



 

<span data-ttu-id="38cb5-136">L'immissione di questi dati nella tabella directory specifica le strutture di directory di origine e di destinazione.</span><span class="sxs-lookup"><span data-stu-id="38cb5-136">Entering this data into the Directory table specifies the source and target directory structures.</span></span> <span data-ttu-id="38cb5-137">Vedere la [tabella directory](directory-table.md) e [usare gli argomenti della tabella directory](using-the-directory-table.md) .</span><span class="sxs-lookup"><span data-stu-id="38cb5-137">See the [Directory Table](directory-table.md) and [Using the Directory Table](using-the-directory-table.md) topics.</span></span> <span data-ttu-id="38cb5-138">Si noti che la proprietà [**targetdir**](targetdir.md) deve corrispondere al nome di una radice nella tabella di directory di ogni installazione.</span><span class="sxs-lookup"><span data-stu-id="38cb5-138">Note that the [**TARGETDIR**](targetdir.md) property must be the name of one root in the Directory table of every installation.</span></span>

[<span data-ttu-id="38cb5-139">Continua</span><span class="sxs-lookup"><span data-stu-id="38cb5-139">Continue</span></span>](specifying-components.md)

 

 



