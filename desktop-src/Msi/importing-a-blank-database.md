---
description: Per riprodurre l'esempio è necessario copiare o creare con uno strumento software, un file di database Windows Installer.
ms.assetid: e239bbe4-3290-40f0-9f28-0e8aa4ed23f8
title: Importazione di un database vuoto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b654b0de118013e8f211a9b06e896cc3f486faf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232442"
---
# <a name="importing-a-blank-database"></a><span data-ttu-id="2b06e-103">Importazione di un database vuoto</span><span class="sxs-lookup"><span data-stu-id="2b06e-103">Importing a Blank Database</span></span>

<span data-ttu-id="2b06e-104">Per riprodurre l'esempio è necessario copiare o creare con uno strumento software, un file di database Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="2b06e-104">To reproduce the sample you need to copy, or create with a software tool, a Windows Installer database file.</span></span> <span data-ttu-id="2b06e-105">Un database di installazione completamente vuoto, Schema.msi, viene fornito con i [componenti Windows SDK per Windows Installer sviluppatori](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="2b06e-105">A totally blank installation database, Schema.msi, is provided with the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="2b06e-106">L'SDK fornisce anche un database parzialmente vuoto, uisample.msi, che contiene le tabelle di sequenza suggerite e i dati necessari per una semplice interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="2b06e-106">The SDK also provides a partially blank database, uisample.msi, that contains the suggested sequence tables and data required for a simple user interface.</span></span> <span data-ttu-id="2b06e-107">Creare una copia di uisample.msi e spostarla nella stessa directory contenente la cartella del blocco note creata durante [la pianificazione dell'installazione](planning-the-installation.md).</span><span class="sxs-lookup"><span data-stu-id="2b06e-107">Make a copy of uisample.msi and move it into the same directory containing the Notepad folder you created in [Planning the Installation](planning-the-installation.md).</span></span> <span data-ttu-id="2b06e-108">Rinominare il file MNP2000.msi.</span><span class="sxs-lookup"><span data-stu-id="2b06e-108">Rename the file MNP2000.msi.</span></span> <span data-ttu-id="2b06e-109">Il file di database di installazione e i file di origine devono trovarsi nella radice della stessa directory.</span><span class="sxs-lookup"><span data-stu-id="2b06e-109">The installation database file and the source files must both be located at the root of the same directory.</span></span> <span data-ttu-id="2b06e-110">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="2b06e-110">For example:</span></span>

<span data-ttu-id="2b06e-111">C: \\MNP2000.msi di esempio \\</span><span class="sxs-lookup"><span data-stu-id="2b06e-111">C:\\Sample\\MNP2000.msi</span></span>

<span data-ttu-id="2b06e-112">C: \\ \\ blocco note di esempio</span><span class="sxs-lookup"><span data-stu-id="2b06e-112">C:\\Sample\\Notepad</span></span>\\

<span data-ttu-id="2b06e-113">Se non si usa Uisample.msi, è necessario ottenere un database vuoto, ad esempio Schema.msi, e immettere le informazioni per l'installazione usando uno strumento di modifica del database, ad esempio ORCA, fornito con l'SDK o un altro editor di database.</span><span class="sxs-lookup"><span data-stu-id="2b06e-113">If you do not use Uisample.msi, then you must obtain a blank database, such as Schema.msi, and enter information for the installation using a database editing tool such as Orca, which is provided with the SDK, or another database editor.</span></span>

[<span data-ttu-id="2b06e-114">Continua</span><span class="sxs-lookup"><span data-stu-id="2b06e-114">Continue</span></span>](specifying-directory-structure.md)

 

 



