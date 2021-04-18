---
description: Un file CAB è un singolo file, in genere con estensione cab, che archivia i file compressi in una libreria di file.
ms.assetid: df240302-b875-49bf-8e62-7a35204c35fb
title: File CAB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c7b54ae737785abc33edd46c9e53edc93fcd288
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311005"
---
# <a name="cabinet-files"></a><span data-ttu-id="b9ba1-103">File CAB</span><span class="sxs-lookup"><span data-stu-id="b9ba1-103">Cabinet Files</span></span>

<span data-ttu-id="b9ba1-104">Un file CAB è un singolo file, in genere con estensione cab, che archivia i file compressi in una libreria di file.</span><span class="sxs-lookup"><span data-stu-id="b9ba1-104">A cabinet is a single file, usually with a .cab extension, that stores compressed files in a file library.</span></span> <span data-ttu-id="b9ba1-105">Il formato CAB è un modo efficiente per creare un pacchetto di più file perché la compressione viene eseguita tra i limiti dei file, migliorando significativamente il rapporto di compressione.</span><span class="sxs-lookup"><span data-stu-id="b9ba1-105">The cabinet format is an efficient way to package multiple files because compression is performed across file boundaries, which significantly improves the compression ratio.</span></span>

<span data-ttu-id="b9ba1-106">Gli sviluppatori possono usare uno strumento per la creazione di file CAB, ad esempio Makecab.exe per creare file CAB da usare con i pacchetti del programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="b9ba1-106">Developers can use a cabinet file creation tool such as Makecab.exe to make cabinet files for use with installer packages.</span></span> <span data-ttu-id="b9ba1-107">L'utilità Makecab.exe è inclusa nei [componenti Windows SDK per Windows Installer sviluppatori](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="b9ba1-107">The Makecab.exe utility is included in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span>

<span data-ttu-id="b9ba1-108">Gli sviluppatori possono inoltre usare uno strumento di creazione di file CAB, ad esempio Cabarc.exe per creare file CAB da usare con i pacchetti del programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="b9ba1-108">Developers can also use a cabinet file creation tool such as Cabarc.exe to make cabinet files for use with installer packages.</span></span> <span data-ttu-id="b9ba1-109">Questo strumento scrive nella struttura del cabinet del diamante.</span><span class="sxs-lookup"><span data-stu-id="b9ba1-109">This tool writes to the Diamond cabinet structure.</span></span>

<span data-ttu-id="b9ba1-110">Le chiavi dei file archiviati all'interno di un file CAB devono corrispondere alle voci della colonna file della [tabella file](file-table.md) e la sequenza di file nel file CAB deve corrispondere alla sequenza di file specificata nella colonna sequenza.</span><span class="sxs-lookup"><span data-stu-id="b9ba1-110">The file keys of the files stored inside of a cabinet file must match the entries in the File column of the [File table](file-table.md) and the sequence of files in the cabinet must match the file sequence specified in the Sequence column.</span></span> <span data-ttu-id="b9ba1-111">Per altre informazioni, vedere [uso di cabinet e origini compresse](using-cabinets-and-compressed-sources.md).</span><span class="sxs-lookup"><span data-stu-id="b9ba1-111">For more information, see [Using Cabinets and Compressed Sources](using-cabinets-and-compressed-sources.md).</span></span>

<span data-ttu-id="b9ba1-112">I file di grandi dimensioni possono essere suddivisi tra due o più file CAB.</span><span class="sxs-lookup"><span data-stu-id="b9ba1-112">Large files can be split between two or more cabinet files.</span></span> <span data-ttu-id="b9ba1-113">Non possono essere presenti più di 15 file in un file CAB che si estende al file CAB successivo.</span><span class="sxs-lookup"><span data-stu-id="b9ba1-113">There can be no more than 15 files in any one cabinet file that spans to the next cabinet file.</span></span> <span data-ttu-id="b9ba1-114">Se, ad esempio, si dispone di tre file CAB, il primo file CAB può includere 15 file che si estendono al secondo file CAB e il secondo file CAB può includere 15 file che si estendono al terzo file CAB.</span><span class="sxs-lookup"><span data-stu-id="b9ba1-114">For example, if you have three cabinet files the first cabinet can have 15 files that span to the second cabinet file and the second cabinet file can have 15 files that span to the third cabinet file.</span></span>

<span data-ttu-id="b9ba1-115">Il programma di installazione estrae i file da un file CAB perché sono necessari per l'installazione e li installa nello stesso ordine in cui vengono archiviati nel file CAB.</span><span class="sxs-lookup"><span data-stu-id="b9ba1-115">The installer extracts files from a cabinet as they are needed by the installation and installs them in the same order as they are stored in the cabinet file.</span></span> <span data-ttu-id="b9ba1-116">I requisiti di spazio per l'installazione di un file archiviato in un file CAB non sono diversi da quelli per l'installazione di un file non compresso.</span><span class="sxs-lookup"><span data-stu-id="b9ba1-116">The space requirements for installing a file stored in a cabinet are no different than for installing an uncompressed file.</span></span>

<span data-ttu-id="b9ba1-117">Un file CAB può trovarsi all'interno o all'esterno del file con estensione msi.</span><span class="sxs-lookup"><span data-stu-id="b9ba1-117">A cabinet file can be located inside or outside of the .msi file.</span></span> <span data-ttu-id="b9ba1-118">A partire da Windows Installer 5,0 in esecuzione in Windows 7 o Windows Server 2008 R2 il programma di installazione salva tutti i cabinet incorporati nel file con estensione msi prima di memorizzare nella cache il pacchetto di installazione.</span><span class="sxs-lookup"><span data-stu-id="b9ba1-118">Beginning with Windows Installer 5.0 running on Windows 7 or Windows Server 2008 R2 the installer saves any cabinets that are embedded in the .msi file before caching the installation package.</span></span>

<span data-ttu-id="b9ba1-119">**[Windows Installer 4,5 o versioni precedenti](not-supported-in-windows-installer-4-5.md):** Per conservare spazio su disco, il programma di installazione rimuove sempre tutti i cabinet incorporati nel file con estensione msi prima di memorizzare nella cache il pacchetto di installazione nel computer dell'utente.</span><span class="sxs-lookup"><span data-stu-id="b9ba1-119">**[Windows Installer 4.5 or earlier](not-supported-in-windows-installer-4-5.md):** To conserve disk space, the installer always removes any cabinets that are embedded in the .msi file before caching the installation package on the user's computer.</span></span>

 

 



