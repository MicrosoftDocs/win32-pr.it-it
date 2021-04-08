---
description: ICE02 verifica che determinati riferimenti tra le tabelle del componente, del file e del registro di sistema siano reciproci. Questi riferimenti devono essere reciproci affinché il programma di installazione determini correttamente lo stato di installazione dei componenti.
ms.assetid: 864404f1-439d-49a2-973d-4e6e1618863e
title: ICE02
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1975203825d079d5eeb1ec5e4183767dd68625bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750135"
---
# <a name="ice02"></a><span data-ttu-id="904c8-104">ICE02</span><span class="sxs-lookup"><span data-stu-id="904c8-104">ICE02</span></span>

<span data-ttu-id="904c8-105">ICE02 verifica che determinati riferimenti tra le tabelle del [componente](component-table.md), del [file](file-table.md)e [del registro di sistema](registry-table.md) siano reciproci.</span><span class="sxs-lookup"><span data-stu-id="904c8-105">ICE02 validates that certain references between the [Component](component-table.md), [File](file-table.md), and [Registry](registry-table.md) tables are reciprocal.</span></span> <span data-ttu-id="904c8-106">Questi riferimenti devono essere reciproci affinché il programma di installazione determini correttamente lo stato di installazione dei componenti.</span><span class="sxs-lookup"><span data-stu-id="904c8-106">These references must to be reciprocal for the installer to correctly determine the installation state of components.</span></span>

<span data-ttu-id="904c8-107">Il programma di installazione utilizza la colonna di percorso della tabella dei componenti per rilevare la presenza del componente elencato nella colonna componente.</span><span class="sxs-lookup"><span data-stu-id="904c8-107">The installer uses the KeyPath column of the Component table to detect the presence of the component listed in the Component column.</span></span> <span data-ttu-id="904c8-108">La colonna di chiave percorso contiene una chiave nel registro di sistema o nelle tabelle di file.</span><span class="sxs-lookup"><span data-stu-id="904c8-108">The KeyPath column contains a key into the Registry or File tables.</span></span> <span data-ttu-id="904c8-109">In entrambe le tabelle è presente una \_ colonna Component che contiene una chiave nella tabella Component che punta al componente che controlla la voce del registro di sistema o il file.</span><span class="sxs-lookup"><span data-stu-id="904c8-109">Both of these tables have a Component\_ column that contains a key back into the Component table pointing to the component that controls the registry entry or file.</span></span> <span data-ttu-id="904c8-110">Questi riferimenti devono essere reciproci.</span><span class="sxs-lookup"><span data-stu-id="904c8-110">These references must be reciprocal.</span></span>

## <a name="result"></a><span data-ttu-id="904c8-111">Risultato</span><span class="sxs-lookup"><span data-stu-id="904c8-111">Result</span></span>

<span data-ttu-id="904c8-112">ICE02 Invia un messaggio di errore se trova un riferimento che deve essere reciproco e non lo è.</span><span class="sxs-lookup"><span data-stu-id="904c8-112">ICE02 posts an error message if it finds a reference that should be reciprocal and is not.</span></span>

## <a name="example"></a><span data-ttu-id="904c8-113">Esempio</span><span class="sxs-lookup"><span data-stu-id="904c8-113">Example</span></span>

<span data-ttu-id="904c8-114">ICE02 invierà il messaggio di errore seguente per un file con estensione msi contenente le voci di database indicate.</span><span class="sxs-lookup"><span data-stu-id="904c8-114">ICE02 would post the following error message for a .msi file containing the database entries shown.</span></span>

``` syntax
File: 'Red_File' cannot be the key file for Component: 'Blue'. The file belongs to Component: 'Red'
```

<span data-ttu-id="904c8-115">[Tabella componenti](component-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="904c8-115">[Component Table](component-table.md) (partial)</span></span>



| <span data-ttu-id="904c8-116">Componente</span><span class="sxs-lookup"><span data-stu-id="904c8-116">Component</span></span> | <span data-ttu-id="904c8-117">KeyPath</span><span class="sxs-lookup"><span data-stu-id="904c8-117">KeyPath</span></span>   |
|-----------|-----------|
| <span data-ttu-id="904c8-118">Red</span><span class="sxs-lookup"><span data-stu-id="904c8-118">Red</span></span>       | <span data-ttu-id="904c8-119">\_File rosso</span><span class="sxs-lookup"><span data-stu-id="904c8-119">Red\_File</span></span> |
| <span data-ttu-id="904c8-120">Blu</span><span class="sxs-lookup"><span data-stu-id="904c8-120">Blue</span></span>      | <span data-ttu-id="904c8-121">\_File rosso</span><span class="sxs-lookup"><span data-stu-id="904c8-121">Red\_File</span></span> |



 

<span data-ttu-id="904c8-122">[Tabella file](file-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="904c8-122">[File Table](file-table.md) (partial)</span></span>



| <span data-ttu-id="904c8-123">Colonna file</span><span class="sxs-lookup"><span data-stu-id="904c8-123">File Column</span></span> | <span data-ttu-id="904c8-124">Componente\_</span><span class="sxs-lookup"><span data-stu-id="904c8-124">Component\_</span></span> |
|-------------|-------------|
| <span data-ttu-id="904c8-125">\_File rosso</span><span class="sxs-lookup"><span data-stu-id="904c8-125">Red\_File</span></span>   | <span data-ttu-id="904c8-126">Red</span><span class="sxs-lookup"><span data-stu-id="904c8-126">Red</span></span>         |
| <span data-ttu-id="904c8-127">\_File blu</span><span class="sxs-lookup"><span data-stu-id="904c8-127">Blue\_File</span></span>  | <span data-ttu-id="904c8-128">Blu</span><span class="sxs-lookup"><span data-stu-id="904c8-128">Blue</span></span>        |



 

<span data-ttu-id="904c8-129">Il componente blu fa riferimento \_ al file rosso, ma \_ il file rosso non è controllato dal blu del componente e pertanto non può essere il file del percorso di base.</span><span class="sxs-lookup"><span data-stu-id="904c8-129">Component Blue references Red\_File, but Red\_File is not controlled by Component Blue and therefore cannot be the KeyPath file.</span></span> <span data-ttu-id="904c8-130">Se è stato chiamato il programma di installazione per ottenere lo stato di installazione di Blue, non verrà verificato correttamente se \_ è stato installato il file rosso.</span><span class="sxs-lookup"><span data-stu-id="904c8-130">If the installer were called to get the installation state of Blue it would incorrectly check whether Red\_File was installed.</span></span> <span data-ttu-id="904c8-131">Se si modifica il campo del percorso della tabella per il blu nella tabella dei componenti nel \_ file blu, viene risolto l'errore.</span><span class="sxs-lookup"><span data-stu-id="904c8-131">Changing the KeyPath field for Blue in the Component Table to Blue\_File fixes the error.</span></span>

## <a name="related-topics"></a><span data-ttu-id="904c8-132">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="904c8-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="904c8-133">Riferimento ghiaccio</span><span class="sxs-lookup"><span data-stu-id="904c8-133">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



