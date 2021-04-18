---
description: Utilizzare queste linee guida per creare un pacchetto di Windows Installer contenente più di 32767 file.
ms.assetid: 3145629f-cc0a-4216-8549-76bb61070772
title: Creazione di un pacchetto di grandi dimensioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aca09c427336e4ca8a17fd8ebdf803f52ebe6c26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311046"
---
# <a name="authoring-a-large-package"></a><span data-ttu-id="92698-103">Creazione di un pacchetto di grandi dimensioni</span><span class="sxs-lookup"><span data-stu-id="92698-103">Authoring a Large Package</span></span>

<span data-ttu-id="92698-104">Utilizzare queste linee guida per creare un pacchetto di Windows Installer contenente più di 32767 file.</span><span class="sxs-lookup"><span data-stu-id="92698-104">Use this guideline to author a Windows Installer package that contains more than 32767 files.</span></span>

<span data-ttu-id="92698-105">Se il pacchetto di Windows Installer contiene più di 32767 file, è necessario modificare lo schema del database per aumentare il limite delle colonne seguenti:</span><span class="sxs-lookup"><span data-stu-id="92698-105">If your Windows Installer package contains more than 32767 files, you must change the schema of the database to increase the limit of the following columns:</span></span>

-   <span data-ttu-id="92698-106">Colonna sequenza della tabella dei [file](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="92698-106">The Sequence column of the [File table](file-table.md).</span></span>
-   <span data-ttu-id="92698-107">Colonna LastSequence della tabella dei [supporti](media-table.md).</span><span class="sxs-lookup"><span data-stu-id="92698-107">The LastSequence column of the [Media table](media-table.md).</span></span>
-   <span data-ttu-id="92698-108">Colonna sequenza della tabella delle [patch](patch-table.md).</span><span class="sxs-lookup"><span data-stu-id="92698-108">The Sequence column of the [Patch table](patch-table.md).</span></span>

<span data-ttu-id="92698-109">Per altre informazioni, vedere [formato della definizione di colonna](column-definition-format.md).</span><span class="sxs-lookup"><span data-stu-id="92698-109">For more information, see [Column Definition Format](column-definition-format.md).</span></span>

<span data-ttu-id="92698-110">**Per aumentare il limite di una colonna del database**</span><span class="sxs-lookup"><span data-stu-id="92698-110">**To increase the limit of a database column**</span></span>

1.  <span data-ttu-id="92698-111">Esportare la tabella in un file con estensione IDT.</span><span class="sxs-lookup"><span data-stu-id="92698-111">Export the table to an .idt file.</span></span> <span data-ttu-id="92698-112">Per informazioni dettagliate, vedere [Msidb.exe](msidb-exe.md), [esportare file](export-files.md), [importazione ed esportazione](importing-and-exporting.md).</span><span class="sxs-lookup"><span data-stu-id="92698-112">For details, see [Msidb.exe](msidb-exe.md), [Export Files](export-files.md), and [Importing and Exporting](importing-and-exporting.md).</span></span>
2.  <span data-ttu-id="92698-113">Modificare il file con estensione IDT per modificare il tipo di colonna da i2 a I4 o da i2 a i4.</span><span class="sxs-lookup"><span data-stu-id="92698-113">Edit the .idt file to change the column type from i2 to i4, or from I2 to I4.</span></span>
3.  <span data-ttu-id="92698-114">Esportare la tabella di [ \_ convalida](-validation-table.md) in un file con estensione IDT.</span><span class="sxs-lookup"><span data-stu-id="92698-114">Export the [\_Validation](-validation-table.md) table to an .idt file.</span></span>
4.  <span data-ttu-id="92698-115">Modificare il file con estensione IDT per modificare i valori nella colonna MaxValue della tabella di [ \_ convalida](-validation-table.md) in modo da includere la larghezza delle colonne aumentata.</span><span class="sxs-lookup"><span data-stu-id="92698-115">Edit the .idt file to change the values in the MaxValue column of the [\_Validation](-validation-table.md) table to accommodate the increased column widths.</span></span>
5.  <span data-ttu-id="92698-116">Importare di nuovo i file con estensione IDT nel database.</span><span class="sxs-lookup"><span data-stu-id="92698-116">Import the .idt files back into the database.</span></span>

<span data-ttu-id="92698-117">Si noti che non è possibile creare trasformazioni e patch tra due pacchetti con tipi di colonne diversi.</span><span class="sxs-lookup"><span data-stu-id="92698-117">Note that transforms and patches cannot be created between two packages with different column types.</span></span>

 

 



