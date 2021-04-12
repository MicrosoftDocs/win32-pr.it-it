---
title: Direttive per il preprocessore (menu e altre risorse)
description: È possibile usare le direttive descritte nella tabella seguente in base alle esigenze nello script della risorsa. Indicano a RC di eseguire azioni o di assegnare valori ai nomi.
ms.assetid: 162f946e-54d8-4e23-9aa7-8e91eda4ee68
keywords:
- compilatore di risorse, direttive per il preprocessore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43e8c32f1d32dab784d5d947fdf64b7018451a5a
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104340242"
---
# <a name="preprocessor-directives-menus-and-other-resources"></a><span data-ttu-id="6945f-105">Direttive per il preprocessore (menu e altre risorse)</span><span class="sxs-lookup"><span data-stu-id="6945f-105">Preprocessor Directives (Menus and Other Resources)</span></span>

<span data-ttu-id="6945f-106">È possibile usare le direttive descritte nella tabella seguente in base alle esigenze nello script della risorsa.</span><span class="sxs-lookup"><span data-stu-id="6945f-106">You can use the directives described in the following table as needed in your resource script.</span></span> <span data-ttu-id="6945f-107">Indicano a RC di eseguire azioni o di assegnare valori ai nomi.</span><span class="sxs-lookup"><span data-stu-id="6945f-107">They instruct RC to perform actions or to assign values to names.</span></span>



| <span data-ttu-id="6945f-108">Direttiva</span><span class="sxs-lookup"><span data-stu-id="6945f-108">Directive</span></span>                     | <span data-ttu-id="6945f-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6945f-109">Description</span></span>                                                           |
|-------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="6945f-110">**\#definire**</span><span class="sxs-lookup"><span data-stu-id="6945f-110">**\#define**</span></span>](-define.md)   | <span data-ttu-id="6945f-111">Definisce un nome specificato assegnando a esso un valore specificato.</span><span class="sxs-lookup"><span data-stu-id="6945f-111">Defines a specified name by assigning it a given value.</span></span>               |
| [<span data-ttu-id="6945f-112">**\#elif**</span><span class="sxs-lookup"><span data-stu-id="6945f-112">**\#elif**</span></span>](-elif.md)       | <span data-ttu-id="6945f-113">Contrassegna una clausola facoltativa di un blocco di compilazione condizionale.</span><span class="sxs-lookup"><span data-stu-id="6945f-113">Marks an optional clause of a conditional-compilation block.</span></span>          |
| [<span data-ttu-id="6945f-114">**\#else**</span><span class="sxs-lookup"><span data-stu-id="6945f-114">**\#else**</span></span>](-else.md)       | <span data-ttu-id="6945f-115">Contrassegna l'ultima clausola facoltativa di un blocco di compilazione condizionale.</span><span class="sxs-lookup"><span data-stu-id="6945f-115">Marks the last optional clause of a conditional-compilation block.</span></span>    |
| [<span data-ttu-id="6945f-116">**\#endif**</span><span class="sxs-lookup"><span data-stu-id="6945f-116">**\#endif**</span></span>](-endif.md)     | <span data-ttu-id="6945f-117">Contrassegna la fine di un blocco di compilazione condizionale.</span><span class="sxs-lookup"><span data-stu-id="6945f-117">Marks the end of a conditional-compilation block.</span></span>                     |
| [<span data-ttu-id="6945f-118">**\#if**</span><span class="sxs-lookup"><span data-stu-id="6945f-118">**\#if**</span></span>](-if.md)           | <span data-ttu-id="6945f-119">Compila in modo condizionale lo script se un'espressione specificata è true.</span><span class="sxs-lookup"><span data-stu-id="6945f-119">Conditionally compiles the script if a specified expression is true.</span></span>  |
| [<span data-ttu-id="6945f-120">**\#ifdef**</span><span class="sxs-lookup"><span data-stu-id="6945f-120">**\#ifdef**</span></span>](-ifdef.md)     | <span data-ttu-id="6945f-121">Compila in modo condizionale lo script se è stato definito un nome specificato.</span><span class="sxs-lookup"><span data-stu-id="6945f-121">Conditionally compiles the script if a specified name is defined.</span></span>     |
| [<span data-ttu-id="6945f-122">**\#ifndef**</span><span class="sxs-lookup"><span data-stu-id="6945f-122">**\#ifndef**</span></span>](-ifndef.md)   | <span data-ttu-id="6945f-123">Compila in modo condizionale lo script se non è definito un nome specificato.</span><span class="sxs-lookup"><span data-stu-id="6945f-123">Conditionally compiles the script if a specified name is not defined.</span></span> |
| [<span data-ttu-id="6945f-124">**\#includere**</span><span class="sxs-lookup"><span data-stu-id="6945f-124">**\#include**</span></span>](-include.md) | <span data-ttu-id="6945f-125">Copia il contenuto di un file nel file di definizione delle risorse.</span><span class="sxs-lookup"><span data-stu-id="6945f-125">Copies the contents of a file into the resource-definition file.</span></span>      |
| [<span data-ttu-id="6945f-126">**\#undef**</span><span class="sxs-lookup"><span data-stu-id="6945f-126">**\#undef**</span></span>](-undef.md)     | <span data-ttu-id="6945f-127">Rimuove la definizione del nome specificato.</span><span class="sxs-lookup"><span data-stu-id="6945f-127">Removes the definition of the specified name.</span></span>                         |



 

<span data-ttu-id="6945f-128">Per definire i simboli per gli identificatori di risorsa, usare la direttiva **\# define** per definirli in un file di intestazione.</span><span class="sxs-lookup"><span data-stu-id="6945f-128">To define symbols for your resource identifiers, use the **\#define** directive to define them in a header file.</span></span> <span data-ttu-id="6945f-129">Includere questa intestazione sia nello script di risorsa che nel codice sorgente dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="6945f-129">Include this header both in the resource script and your application source code.</span></span> <span data-ttu-id="6945f-130">Analogamente, è possibile definire i valori per gli attributi e gli stili delle risorse includendo Windows. h nello script della risorsa.</span><span class="sxs-lookup"><span data-stu-id="6945f-130">Similarly, you define the values for resource attributes and styles by including Windows.h in the resource script.</span></span>

<span data-ttu-id="6945f-131">RC considera i file con le estensioni. c e. h in modo speciale.</span><span class="sxs-lookup"><span data-stu-id="6945f-131">RC treats files with the .c and .h extensions in a special manner.</span></span> <span data-ttu-id="6945f-132">Si presuppone che un file con una di queste estensioni non contenga risorse.</span><span class="sxs-lookup"><span data-stu-id="6945f-132">It assumes that a file with one of these extensions does not contain resources.</span></span> <span data-ttu-id="6945f-133">Se un file ha l'estensione di file. c o. h, RC ignora tutte le righe nel file tranne le direttive del preprocessore.</span><span class="sxs-lookup"><span data-stu-id="6945f-133">If a file has the .c or .h file name extension, RC ignores all lines in the file except the preprocessor directives.</span></span> <span data-ttu-id="6945f-134">Pertanto, per includere un file che contiene risorse in un altro script di risorsa, assegnare al file un'estensione diversa da. c o. h.</span><span class="sxs-lookup"><span data-stu-id="6945f-134">Therefore, to include a file that contains resources in another resource script, give the file to be included an extension other than .c or .h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6945f-135">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6945f-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6945f-136">Pragma (direttive)</span><span class="sxs-lookup"><span data-stu-id="6945f-136">Pragma Directives</span></span>](pragma-directives.md)
</dt> </dl>

 

 




