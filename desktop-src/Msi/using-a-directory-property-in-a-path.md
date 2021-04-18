---
description: Le directory della tabella directory specificano il layout di un'installazione.
ms.assetid: 59f6ae09-d013-46d7-a1a7-0543f31ac487
title: Utilizzo di una proprietà di directory in un percorso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2789f6442072f3db6a96c0abb7db301038673f83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318975"
---
# <a name="using-a-directory-property-in-a-path"></a><span data-ttu-id="533f8-103">Utilizzo di una proprietà di directory in un percorso</span><span class="sxs-lookup"><span data-stu-id="533f8-103">Using a Directory Property in a Path</span></span>

<span data-ttu-id="533f8-104">Le directory della [tabella directory](directory-table.md) specificano il layout di un'installazione.</span><span class="sxs-lookup"><span data-stu-id="533f8-104">The directories in the [Directory table](directory-table.md) specify the layout of an installation.</span></span> <span data-ttu-id="533f8-105">Quando il Windows Installer risolve tali directory durante l' [azione CostFinalize secondo](costfinalize-action.md), le chiavi della tabella directory diventano [Proprietà](properties.md) impostate sui percorsi di directory.</span><span class="sxs-lookup"><span data-stu-id="533f8-105">When the Windows Installer resolves these directories during the [CostFinalize action](costfinalize-action.md), the keys in the Directory table become [properties](properties.md) set to directory paths.</span></span> <span data-ttu-id="533f8-106">Il programma di installazione imposta inoltre sempre un numero di [proprietà della cartella di sistema](property-reference.md) standard sui percorsi delle cartelle di sistema.</span><span class="sxs-lookup"><span data-stu-id="533f8-106">The installer also always sets a number of standard [System Folder Properties](property-reference.md) to system folder paths.</span></span>

<span data-ttu-id="533f8-107">I valori delle [proprietà della cartella di sistema](property-reference.md) sono sicuramente terminati in un separatore di directory.</span><span class="sxs-lookup"><span data-stu-id="533f8-107">The values of the [System Folder Properties](property-reference.md) are guaranteed to end in a directory separator.</span></span> <span data-ttu-id="533f8-108">I valori di tutte le altre proprietà immesse nella [tabella di directory](directory-table.md) possono essere terminati solo in un separatore di directory dopo che il programma di installazione ha eseguito l' [azione CostFinalize secondo](costfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="533f8-108">The values of all other properties entered in the [Directory table](directory-table.md) are only guaranteed to end in a directory separator after the installer has run the [CostFinalize action](costfinalize-action.md).</span></span> <span data-ttu-id="533f8-109">Prima che i costi siano completati, i valori delle proprietà immesse nella tabella di directory che non sono [proprietà della cartella di sistema](property-reference.md) potrebbero non finire in un separatore di directory.</span><span class="sxs-lookup"><span data-stu-id="533f8-109">Before costing has completed, the values of properties entered in the Directory table which are not [System Folder Properties](property-reference.md) may not end in a directory separator.</span></span> <span data-ttu-id="533f8-110">Pertanto, se l'installazione imposta le proprietà della directory utilizzando [azioni personalizzate](custom-actions.md) nel pacchetto, i valori nel riferimento potrebbero non terminare con un separatore di directory.</span><span class="sxs-lookup"><span data-stu-id="533f8-110">Therefore, if your installation sets directory properties using [custom actions](custom-actions.md) in the package, the values on reference might not end with a directory separator.</span></span>

<span data-ttu-id="533f8-111">Le proprietà della directory che terminano con un separatore di directory possono pertanto essere utilizzate in una stringa di percorso senza includere esplicitamente il separatore di directory.</span><span class="sxs-lookup"><span data-stu-id="533f8-111">Directory properties ending with a directory separator can therefore be used in a path string without explicitly including the directory separator.</span></span> <span data-ttu-id="533f8-112">Se, ad esempio, il valore di DirectoryProperty termina con un separatore di directory, la stringa seguente specifica correttamente il percorso del *file* nella *sottodirectory*</span><span class="sxs-lookup"><span data-stu-id="533f8-112">For example, if the value of DirectoryProperty ends with a directory separator, the following string correctly specifies the path to *file* in *subdirectory*</span></span>

``` syntax
[DirectoryProperty]subdirectory\file
```

<span data-ttu-id="533f8-113">e la stringa di percorso seguente non è corretta.</span><span class="sxs-lookup"><span data-stu-id="533f8-113">and the following path string is incorrect.</span></span>

``` syntax
[DirectoryProperty]\subdirectory\file
```

 

 



