---
description: ICE07 verifica che il pacchetto di installazione specifichi che i caratteri siano installati in FontsFolder. Se un tipo di carattere viene installato in una cartella diversa da FontsFolder, il programma di installazione crea un collegamento anziché installare effettivamente il tipo di carattere.
ms.assetid: aa51b077-fb7b-4e09-9de1-ef1905144a94
title: ICE07
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80a79bcb681a57bb09ff235b35a5287492a4f39c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314244"
---
# <a name="ice07"></a><span data-ttu-id="2f527-104">ICE07</span><span class="sxs-lookup"><span data-stu-id="2f527-104">ICE07</span></span>

<span data-ttu-id="2f527-105">ICE07 verifica che il pacchetto di installazione specifichi che i caratteri siano installati in FontsFolder.</span><span class="sxs-lookup"><span data-stu-id="2f527-105">ICE07 validates that installation package specifies that fonts be installed into the FontsFolder.</span></span> <span data-ttu-id="2f527-106">Se un tipo di carattere viene installato in una cartella diversa da FontsFolder, il programma di installazione crea un collegamento anziché installare effettivamente il tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="2f527-106">If a font is installed to a folder other than the FontsFolder the installer creates a shortcut rather than actually installing the font.</span></span>

<span data-ttu-id="2f527-107">L'azione personalizzata ICE07 esegue le operazioni seguenti per ogni tipo di carattere della [tabella dei tipi di carattere](font-table.md).</span><span class="sxs-lookup"><span data-stu-id="2f527-107">The ICE07 custom action does the following for each font in the [Font table](font-table.md).</span></span>

1.  <span data-ttu-id="2f527-108">Trova il file del tipo di carattere a cui appartiene ogni titolo del carattere usando la [tabella dei tipi di carattere](font-table.md).</span><span class="sxs-lookup"><span data-stu-id="2f527-108">Finds the font file to which each font title belongs using the [Font table](font-table.md).</span></span>
2.  <span data-ttu-id="2f527-109">Esegue una query sulla \_ colonna componente della [tabella file](file-table.md) per il componente che controlla ogni file.</span><span class="sxs-lookup"><span data-stu-id="2f527-109">Queries the Component\_ column of the [File table](file-table.md) for the component that controls each file.</span></span>
3.  <span data-ttu-id="2f527-110">Esegue una query sulla \_ colonna di directory della [tabella dei componenti](component-table.md) per ottenere una chiave nella tabella di directory.</span><span class="sxs-lookup"><span data-stu-id="2f527-110">Queries the Directory\_ column of the [Component table](component-table.md) to obtain a key into the Directory table.</span></span>
4.  <span data-ttu-id="2f527-111">Risolve la tabella di [directory](directory-table.md) per determinare il nome della cartella in cui il programma di installazione deve installare il file del tipo di carattere</span><span class="sxs-lookup"><span data-stu-id="2f527-111">Resolves the [Directory table](directory-table.md) to determine the name of the folder into which the installer is to install the font file</span></span>
5.  <span data-ttu-id="2f527-112">Invia un errore se il file del tipo di carattere viene installato in una cartella diversa da FontsFolder.</span><span class="sxs-lookup"><span data-stu-id="2f527-112">Posts an error if the font file is being installed into a folder other than the FontsFolder.</span></span>

## <a name="result"></a><span data-ttu-id="2f527-113">Risultato</span><span class="sxs-lookup"><span data-stu-id="2f527-113">Result</span></span>

<span data-ttu-id="2f527-114">ICE07 Invia un errore se rileva che il database specifica che un file del tipo di carattere deve essere installato in una cartella diversa da FontsFolder.</span><span class="sxs-lookup"><span data-stu-id="2f527-114">ICE07 posts an error if it finds that the database specifies that a font file be installed into a folder other than the FontsFolder.</span></span>

## <a name="example"></a><span data-ttu-id="2f527-115">Esempio</span><span class="sxs-lookup"><span data-stu-id="2f527-115">Example</span></span>

<span data-ttu-id="2f527-116">IC07 invia il messaggio di errore seguente per l'esempio illustrato.</span><span class="sxs-lookup"><span data-stu-id="2f527-116">IC07 would post the following error message for the example shown.</span></span>

``` syntax
'Tahoma' is a font and must be installed to the FontsFolder directory. Current Install Directory: 'Sandbar'.
```

[<span data-ttu-id="2f527-117">Tabella dei tipi di carattere</span><span class="sxs-lookup"><span data-stu-id="2f527-117">Font Table</span></span>](font-table.md)



| <span data-ttu-id="2f527-118">file\_</span><span class="sxs-lookup"><span data-stu-id="2f527-118">File\_</span></span> | <span data-ttu-id="2f527-119">FontTitle</span><span class="sxs-lookup"><span data-stu-id="2f527-119">FontTitle</span></span> |
|--------|-----------|
| <span data-ttu-id="2f527-120">Myrtle</span><span class="sxs-lookup"><span data-stu-id="2f527-120">Myrtle</span></span> | <span data-ttu-id="2f527-121">Tahoma</span><span class="sxs-lookup"><span data-stu-id="2f527-121">Tahoma</span></span>    |



 

<span data-ttu-id="2f527-122">[Tabella file](file-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="2f527-122">[File Table](file-table.md) (partial)</span></span>



| <span data-ttu-id="2f527-123">File</span><span class="sxs-lookup"><span data-stu-id="2f527-123">File</span></span>   | <span data-ttu-id="2f527-124">Componente\_</span><span class="sxs-lookup"><span data-stu-id="2f527-124">Component\_</span></span>   |
|--------|---------------|
| <span data-ttu-id="2f527-125">Myrtle</span><span class="sxs-lookup"><span data-stu-id="2f527-125">Myrtle</span></span> | <span data-ttu-id="2f527-126">Myrtle \_ Beach</span><span class="sxs-lookup"><span data-stu-id="2f527-126">Myrtle\_Beach</span></span> |



 

<span data-ttu-id="2f527-127">[Tabella componenti](component-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="2f527-127">[Component Table](component-table.md) (partial)</span></span>



| <span data-ttu-id="2f527-128">Componente</span><span class="sxs-lookup"><span data-stu-id="2f527-128">Component</span></span>     | <span data-ttu-id="2f527-129">Directory\_</span><span class="sxs-lookup"><span data-stu-id="2f527-129">Directory\_</span></span> |
|---------------|-------------|
| <span data-ttu-id="2f527-130">Myrtle \_ Beach</span><span class="sxs-lookup"><span data-stu-id="2f527-130">Myrtle\_Beach</span></span> | <span data-ttu-id="2f527-131">SandBar</span><span class="sxs-lookup"><span data-stu-id="2f527-131">SandBar</span></span>     |



 

<span data-ttu-id="2f527-132">In questo esempio, il tipo di carattere Tahoma esegue il mapping al file del tipo di carattere Myrtle.</span><span class="sxs-lookup"><span data-stu-id="2f527-132">In this example, the font Tahoma maps to the font file Myrtle.</span></span> <span data-ttu-id="2f527-133">Il file Myrtle appartiene al componente Myrtle \_ Beach.</span><span class="sxs-lookup"><span data-stu-id="2f527-133">The file Myrtle belongs to the component Myrtle\_Beach.</span></span> <span data-ttu-id="2f527-134">La risoluzione della tabella di directory mostra che tutti i file appartenenti a Myrtle \_ Beach devono essere installati nella cartella di sabbia.</span><span class="sxs-lookup"><span data-stu-id="2f527-134">Resolution of the Directory table shows that all the files belonging to Myrtle\_Beach are to be installed in the Sandbar folder.</span></span> <span data-ttu-id="2f527-135">Poiché non è FontsFolder, ICE07 pubblica un messaggio di errore.</span><span class="sxs-lookup"><span data-stu-id="2f527-135">Because this is not the FontsFolder, ICE07 posts an error message.</span></span>

<span data-ttu-id="2f527-136">Si noti che se il componente Myrtle \_ Beach appartiene realmente alla cartella del banco di sabbia e non al FontsFolder, il tipo di carattere Tahoma potrebbe non appartenere a Myrtle \_ Beach.</span><span class="sxs-lookup"><span data-stu-id="2f527-136">Note that if the component Myrtle\_Beach really belongs in the Sandbar folder, and not the FontsFolder, then the font Tahoma may not belong in Myrtle\_Beach.</span></span> <span data-ttu-id="2f527-137">Una possibile correzione per l'errore consiste nell'includere Tahoma in un altro componente che viene installato nella directory FontsFolder.</span><span class="sxs-lookup"><span data-stu-id="2f527-137">A possible fix for the error would be to include Tahoma in another component that does get installed in the FontsFolder directory.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2f527-138">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2f527-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2f527-139">Riferimento ghiaccio</span><span class="sxs-lookup"><span data-stu-id="2f527-139">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



