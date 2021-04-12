---
description: Il tipo di dati filename è una stringa di testo contenente un nome file o una cartella.
ms.assetid: af59e1b8-0699-4031-895f-415752611e21
title: Nome file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fc049fa0808efc180afbd715e311a124bfdada9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528189"
---
# <a name="filename"></a><span data-ttu-id="0ee82-103">Nome file</span><span class="sxs-lookup"><span data-stu-id="0ee82-103">Filename</span></span>

<span data-ttu-id="0ee82-104">Il tipo di dati filename è una stringa di testo contenente un nome file o una cartella.</span><span class="sxs-lookup"><span data-stu-id="0ee82-104">The Filename data type is a text string containing a file name or folder.</span></span> <span data-ttu-id="0ee82-105">Per impostazione predefinita, si presuppone che il nome file usi la sintassi del nome file breve. ovvero un nome di otto caratteri, un punto (.) e un'estensione di 3 caratteri.</span><span class="sxs-lookup"><span data-stu-id="0ee82-105">By default, the file name is assumed to use short file name syntax; that is, eight-character name, period (.), and 3-character extension.</span></span> <span data-ttu-id="0ee82-106">È necessario specificare sempre un nome di file breve perché è possibile impostare la proprietà [**SHORTFILENAMES**](shortfilenames.md) o il volume di destinazione per l'installazione può supportare solo nomi di file brevi.</span><span class="sxs-lookup"><span data-stu-id="0ee82-106">A short file name must always be provided because the [**SHORTFILENAMES**](shortfilenames.md) property may be set or the target volume for the installation may only support short file names.</span></span>

<span data-ttu-id="0ee82-107">Per includere un nome di file lungo con il nome del file breve, separarlo dal nome del file breve con una barra verticale ( \| ).</span><span class="sxs-lookup"><span data-stu-id="0ee82-107">To include a long file name with the short file name, separate it from the short file name with a vertical bar (\|).</span></span>

<span data-ttu-id="0ee82-108">Ad esempio, le due stringhe seguenti sono valide:</span><span class="sxs-lookup"><span data-stu-id="0ee82-108">For example, the following two strings are valid:</span></span>

-   <span data-ttu-id="0ee82-109">status.txt</span><span class="sxs-lookup"><span data-stu-id="0ee82-109">status.txt</span></span>
-   <span data-ttu-id="0ee82-110">Project ~1.txt\| progetto Status.txt</span><span class="sxs-lookup"><span data-stu-id="0ee82-110">projec~1.txt\|Project Status.txt</span></span>

<span data-ttu-id="0ee82-111">I nomi di file brevi e lunghi non devono contenere i caratteri seguenti:</span><span class="sxs-lookup"><span data-stu-id="0ee82-111">Short and long file names must not contain the following characters:</span></span>

-   <span data-ttu-id="0ee82-112">barra (/) o ( \\ )</span><span class="sxs-lookup"><span data-stu-id="0ee82-112">slash (/) or (\\)</span></span>
-   <span data-ttu-id="0ee82-113">punto interrogativo (?)</span><span class="sxs-lookup"><span data-stu-id="0ee82-113">question mark (?)</span></span>
-   <span data-ttu-id="0ee82-114">barra verticale ( \| )</span><span class="sxs-lookup"><span data-stu-id="0ee82-114">vertical bar (\|)</span></span>
-   <span data-ttu-id="0ee82-115">parentesi uncinata chiusa (>)</span><span class="sxs-lookup"><span data-stu-id="0ee82-115">right angle bracket (>)</span></span>
-   <span data-ttu-id="0ee82-116">parentesi uncinata aperta (<)</span><span class="sxs-lookup"><span data-stu-id="0ee82-116">left angle bracket (<)</span></span>
-   <span data-ttu-id="0ee82-117">due punti (:)</span><span class="sxs-lookup"><span data-stu-id="0ee82-117">colon (:)</span></span>
-   <span data-ttu-id="0ee82-118">asterisco ( \* )</span><span class="sxs-lookup"><span data-stu-id="0ee82-118">asterisk (\*)</span></span>
-   <span data-ttu-id="0ee82-119">virgolette doppie (")</span><span class="sxs-lookup"><span data-stu-id="0ee82-119">quotation mark (")</span></span>

<span data-ttu-id="0ee82-120">Inoltre, i nomi di file brevi non devono contenere i caratteri seguenti:</span><span class="sxs-lookup"><span data-stu-id="0ee82-120">In addition, short file names must not contain the following characters:</span></span>

-   <span data-ttu-id="0ee82-121">segno di addizione (+)</span><span class="sxs-lookup"><span data-stu-id="0ee82-121">plus sign (+)</span></span>
-   <span data-ttu-id="0ee82-122">virgola (,)</span><span class="sxs-lookup"><span data-stu-id="0ee82-122">comma (,)</span></span>
-   <span data-ttu-id="0ee82-123">punto e virgola (;)</span><span class="sxs-lookup"><span data-stu-id="0ee82-123">semicolon (;)</span></span>
-   <span data-ttu-id="0ee82-124">segno di uguale (=)</span><span class="sxs-lookup"><span data-stu-id="0ee82-124">equals sign (=)</span></span>
-   <span data-ttu-id="0ee82-125">parentesi quadra aperta ( \[ )</span><span class="sxs-lookup"><span data-stu-id="0ee82-125">left square bracket (\[)</span></span>
-   <span data-ttu-id="0ee82-126">parentesi quadra chiusa ( \] )</span><span class="sxs-lookup"><span data-stu-id="0ee82-126">right square bracket (\])</span></span>

<span data-ttu-id="0ee82-127">Non è consentito alcuno spazio prima del separatore della barra verticale ( \| ) per il nome file breve o la sintassi del nome file lungo.</span><span class="sxs-lookup"><span data-stu-id="0ee82-127">No space is allowed preceding the vertical bar (\|) separator for the short file name/long file name syntax.</span></span> <span data-ttu-id="0ee82-128">I nomi di file brevi non possono includere uno spazio, sebbene sia possibile un nome di file lungo.</span><span class="sxs-lookup"><span data-stu-id="0ee82-128">Short file names may not include a space, although a long file name may.</span></span> <span data-ttu-id="0ee82-129">Uno spazio può esistere dopo il separatore solo se il nome di file lungo del nome del file inizia con lo spazio.</span><span class="sxs-lookup"><span data-stu-id="0ee82-129">A space can exist after the separator only if the long file name of the file name begins with the space.</span></span> <span data-ttu-id="0ee82-130">Non è consentita alcuna sintassi per percorsi completi.</span><span class="sxs-lookup"><span data-stu-id="0ee82-130">No full-path syntax is allowed.</span></span>

> [!Note]  
> <span data-ttu-id="0ee82-131">Il formato della colonna FileName della tabella [MsiEmbeddedUI](msiembeddedui-table.md) è simile al tipo di dati Format filename, tranne per il fatto che il separatore della barra verticale ( \| ) per il nome file breve o il nome di file lungo non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="0ee82-131">The format of the FileName column of the [MsiEmbeddedUI](msiembeddedui-table.md) table is like the format Filename data type except that the vertical bar (\|) separator for the short file name/long file name syntax is not available.</span></span>

 

 

 



