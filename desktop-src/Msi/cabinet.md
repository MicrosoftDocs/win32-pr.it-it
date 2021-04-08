---
description: Il tipo di dati CAB deve essere utilizzato nella colonna CAB della tabella dei supporti.
ms.assetid: 149c74ea-4342-45dd-8da4-4dfa7f4317a0
title: CAB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4814473ef4d21d5445b5b5319278a5e25a7f5540
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881066"
---
# <a name="cabinet"></a><span data-ttu-id="c5230-103">CAB</span><span class="sxs-lookup"><span data-stu-id="c5230-103">Cabinet</span></span>

<span data-ttu-id="c5230-104">Il tipo di dati CAB deve essere utilizzato nella colonna CAB della [tabella dei supporti](media-table.md).</span><span class="sxs-lookup"><span data-stu-id="c5230-104">The Cabinet data type must be used in the Cabinet column of the [Media table](media-table.md).</span></span>

<span data-ttu-id="c5230-105">Se il nome del cabinet è preceduto dal simbolo di cancelletto, il file CAB viene archiviato come flusso di dati all'interno del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="c5230-105">If the cabinet name is preceded by the number sign, the cabinet is stored as a data stream inside the package.</span></span> <span data-ttu-id="c5230-106">La stringa di caratteri che segue \# è un [identificatore](identifier.md) per questo flusso di dati.</span><span class="sxs-lookup"><span data-stu-id="c5230-106">The character string which follows the \# is an [Identifier](identifier.md) for this data stream.</span></span> <span data-ttu-id="c5230-107">Si noti che se l'archivio è archiviato come flusso di dati, il nome di un file CAB fa distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="c5230-107">Note that if the cabinet is stored as a data stream, the name of a cabinet is case-sensitive.</span></span>

<span data-ttu-id="c5230-108">Se il nome del cabinet non è preceduto dal simbolo di cancelletto \# , il file CAB viene archiviato in un file separato che si trova nella radice dell'albero di origine specificato dalla [tabella di directory](directory-table.md).</span><span class="sxs-lookup"><span data-stu-id="c5230-108">If the cabinet name is not preceded by the number sign \#, the cabinet is stored in a separate file located at the root of the source tree specified by the [Directory Table](directory-table.md).</span></span> <span data-ttu-id="c5230-109">Il file CAB deve usare la sintassi del nome file breve costituito da un nome di otto caratteri, un punto e un'estensione di tre caratteri.</span><span class="sxs-lookup"><span data-stu-id="c5230-109">The cabinet file must use the short file name syntax consisting of an eight character name, a period, and a three character extension.</span></span> <span data-ttu-id="c5230-110">Il tipo di dati CAB non può utilizzare la \| sintassi Short LongName per i nomi di file.</span><span class="sxs-lookup"><span data-stu-id="c5230-110">The Cabinet data type cannot use the short\|longname syntax for file names.</span></span> <span data-ttu-id="c5230-111">Se il file CAB viene archiviato come file separato, il nome del file CAB non distingue tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="c5230-111">If the cabinet file is stored as a separate file, the name of the cabinet file is not case-sensitive.</span></span>

<span data-ttu-id="c5230-112">Per conservare spazio su disco, il programma di installazione rimuove tutti i cabinet incorporati nel file con estensione msi prima di memorizzare nella cache il pacchetto di installazione nel computer dell'utente.</span><span class="sxs-lookup"><span data-stu-id="c5230-112">To conserve disk space, the installer removes any cabinets embedded in the .msi file before caching the installation package on the user's computer.</span></span>

<span data-ttu-id="c5230-113">Vedere [inclusione di un file CAB in un'installazione](including-a-cabinet-file-in-an-installation.md).</span><span class="sxs-lookup"><span data-stu-id="c5230-113">See [Including a Cabinet File in an Installation](including-a-cabinet-file-in-an-installation.md).</span></span>

 

 



