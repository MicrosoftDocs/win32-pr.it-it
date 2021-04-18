---
description: ICE18 verifica che tutte le directory vuote utilizzate come percorso della chiave per un componente siano elencate nella tabella CreateFolder.
ms.assetid: de31b893-831b-4a6d-809a-c4a3056b8a66
title: ICE18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a60a3032a285604197e4c0bfda4225d519b0b744
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308192"
---
# <a name="ice18"></a><span data-ttu-id="f0b6f-103">ICE18</span><span class="sxs-lookup"><span data-stu-id="f0b6f-103">ICE18</span></span>

<span data-ttu-id="f0b6f-104">ICE18 verifica che tutte le directory vuote utilizzate come percorso della chiave per un componente siano elencate nella [tabella CreateFolder](createfolder-table.md).</span><span class="sxs-lookup"><span data-stu-id="f0b6f-104">ICE18 validates that any empty directories used as a key path for a component are listed in the [CreateFolder table](createfolder-table.md).</span></span>

<span data-ttu-id="f0b6f-105">Se la colonna del percorso di chiave della [tabella dei componenti](component-table.md) è null, significa che la directory elencata nella colonna directory \_ è il percorso della chiave per tale componente.</span><span class="sxs-lookup"><span data-stu-id="f0b6f-105">If the KeyPath column of the [Component table](component-table.md) is Null, this means that directory listed in the Directory\_ column is the key path for that component.</span></span> <span data-ttu-id="f0b6f-106">Poiché le cartelle create dal programma di installazione vengono eliminate quando diventano vuote, la cartella deve essere elencata nella [tabella CreateFolder](createfolder-table.md) per impedire che il programma di installazione tenti di installare ogni volta.</span><span class="sxs-lookup"><span data-stu-id="f0b6f-106">Because folders created by the installer are deleted when they become empty, this folder must be listed in the [CreateFolder table](createfolder-table.md) to prevent the installer from attempting to install every time.</span></span>

<span data-ttu-id="f0b6f-107">Non rendere la directory SystemFolder il percorso della chiave di un componente.</span><span class="sxs-lookup"><span data-stu-id="f0b6f-107">Do not make the SystemFolder directory the key path of a component.</span></span> <span data-ttu-id="f0b6f-108">Poiché questa cartella è presente in ogni sistema operativo, il programma di installazione rileva sempre il percorso della chiave, indipendentemente dal fatto che il componente sia presente o meno.</span><span class="sxs-lookup"><span data-stu-id="f0b6f-108">Because this folder is present on every operating system, the installer always detects the key path whether or not the component is present.</span></span> <span data-ttu-id="f0b6f-109">In questo caso, il percorso della chiave deve essere un file, una voce del registro di sistema o un'origine dati ODBC.</span><span class="sxs-lookup"><span data-stu-id="f0b6f-109">In this case, the key path should be a file, registry entry, or ODBC data source.</span></span>

<span data-ttu-id="f0b6f-110">Quando si esegue un ICE18 di convalida, verifica innanzitutto se sono soddisfatte le condizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="f0b6f-110">When performing a validation ICE18 first checks whether the following are all true:</span></span>

-   <span data-ttu-id="f0b6f-111">La colonna di percorso della [tabella dei componenti](component-table.md) contiene un valore null.</span><span class="sxs-lookup"><span data-stu-id="f0b6f-111">The KeyPath column of the [Component table](component-table.md) contains a Null value.</span></span>
-   <span data-ttu-id="f0b6f-112">Non sono presenti file elencati per il componente nella [tabella file](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="f0b6f-112">That there are no files listed for the component in the [File table](file-table.md).</span></span>
-   <span data-ttu-id="f0b6f-113">Che non siano presenti file per il componente elencati nella [tabella RemoveFile](removefile-table.md) e che il valore in DirProperty corrisponda alla \_ colonna directory della [tabella Component](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="f0b6f-113">That there are no files for the component listed in the [RemoveFile table](removefile-table.md) and that the value in the DirProperty is the same as the Directory\_ column of the [Component table](component-table.md).</span></span>
-   <span data-ttu-id="f0b6f-114">Che non siano presenti file per il componente elencati nella [tabella DuplicateFile](duplicatefile-table.md) e che il valore in DestFolder corrisponda alla \_ colonna directory della [tabella Component](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="f0b6f-114">That there are no files for the component listed in the [DuplicateFile table](duplicatefile-table.md) and that the value in the DestFolder is the same as the Directory\_ column of the [Component table](component-table.md).</span></span>
-   <span data-ttu-id="f0b6f-115">Che non siano presenti file per il componente elencati nella [tabella MoveFile](movefile-table.md) e che il valore in DestFolder corrisponda alla \_ colonna directory della [tabella Component](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="f0b6f-115">That there are no files for the component listed in the [MoveFile table](movefile-table.md) and that the value in the DestFolder is the same as the Directory\_ column of the [Component table](component-table.md).</span></span>

<span data-ttu-id="f0b6f-116">Se si verificano tutte le condizioni, ICE18 convalida quanto segue:</span><span class="sxs-lookup"><span data-stu-id="f0b6f-116">If these are all true then ICE18 validates the following:</span></span>

-   <span data-ttu-id="f0b6f-117">Il valore della \_ colonna Component della [tabella CreateFolder](createfolder-table.md) è uguale a quello della colonna Component della [tabella Component](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="f0b6f-117">That the Component\_ column of the [CreateFolder table](createfolder-table.md) has the same value as the Component column of the [Component table](component-table.md).</span></span>
-   <span data-ttu-id="f0b6f-118">Il valore della \_ colonna directory della tabella CreateFolder è uguale a quello della colonna directory \_ della [tabella Component](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="f0b6f-118">That the Directory\_ column of the CreateFolder table has the same value as the Directory\_ column of the [Component table](component-table.md).</span></span>

## <a name="result"></a><span data-ttu-id="f0b6f-119">Risultato</span><span class="sxs-lookup"><span data-stu-id="f0b6f-119">Result</span></span>

<span data-ttu-id="f0b6f-120">ICE18 Invia un messaggio di errore se il pacchetto di installazione specifica una directory come percorso della chiave per il componente che non è elencato nella [tabella CreateFolder](createfolder-table.md).</span><span class="sxs-lookup"><span data-stu-id="f0b6f-120">ICE18 posts an error message if the installation package specifies a directory as the key path for component that is not listed in the [CreateFolder table](createfolder-table.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f0b6f-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f0b6f-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f0b6f-122">Riferimento ghiaccio</span><span class="sxs-lookup"><span data-stu-id="f0b6f-122">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



