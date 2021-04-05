---
description: La tabella azione BindImage sul contiene informazioni su ogni file eseguibile o DLL che deve essere associato alle DLL importate.
ms.assetid: 68bf064c-dd85-4796-8e08-6af307f94ad8
title: Tabella azione BindImage sul
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f47b97efc8886d7748d0426a49ed76567810939c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967254"
---
# <a name="bindimage-table"></a><span data-ttu-id="045d5-103">Tabella azione BindImage sul</span><span class="sxs-lookup"><span data-stu-id="045d5-103">BindImage Table</span></span>

<span data-ttu-id="045d5-104">La tabella azione BindImage sul contiene informazioni su ogni file eseguibile o DLL che deve essere associato alle DLL importate.</span><span class="sxs-lookup"><span data-stu-id="045d5-104">The BindImage table contains information about each executable or DLL that needs to be bound to the DLLs imported by it.</span></span>

<span data-ttu-id="045d5-105">La tabella azione BindImage sul include le colonne seguenti.</span><span class="sxs-lookup"><span data-stu-id="045d5-105">The BindImage table has the following columns.</span></span>



| <span data-ttu-id="045d5-106">Colonna</span><span class="sxs-lookup"><span data-stu-id="045d5-106">Column</span></span> | <span data-ttu-id="045d5-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="045d5-107">Type</span></span>                         | <span data-ttu-id="045d5-108">Chiave</span><span class="sxs-lookup"><span data-stu-id="045d5-108">Key</span></span> | <span data-ttu-id="045d5-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="045d5-109">Nullable</span></span> |
|--------|------------------------------|-----|----------|
| <span data-ttu-id="045d5-110">file\_</span><span class="sxs-lookup"><span data-stu-id="045d5-110">File\_</span></span> | [<span data-ttu-id="045d5-111">Identificatore</span><span class="sxs-lookup"><span data-stu-id="045d5-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="045d5-112">S</span><span class="sxs-lookup"><span data-stu-id="045d5-112">Y</span></span>   | <span data-ttu-id="045d5-113">N</span><span class="sxs-lookup"><span data-stu-id="045d5-113">N</span></span>        |
| <span data-ttu-id="045d5-114">Percorso</span><span class="sxs-lookup"><span data-stu-id="045d5-114">Path</span></span>   | [<span data-ttu-id="045d5-115">Percorsi</span><span class="sxs-lookup"><span data-stu-id="045d5-115">Paths</span></span>](paths.md)           | <span data-ttu-id="045d5-116">N</span><span class="sxs-lookup"><span data-stu-id="045d5-116">N</span></span>   | <span data-ttu-id="045d5-117">S</span><span class="sxs-lookup"><span data-stu-id="045d5-117">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="045d5-118">Colonne</span><span class="sxs-lookup"><span data-stu-id="045d5-118">Columns</span></span>

<dl> <dt>

<span data-ttu-id="045d5-119"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>File\_</span><span class="sxs-lookup"><span data-stu-id="045d5-119"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>File\_</span></span>
</dt> <dd>

<span data-ttu-id="045d5-120">Chiave esterna per la colonna uno della [tabella dei file](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="045d5-120">An external key to column one of the [File table](file-table.md).</span></span> <span data-ttu-id="045d5-121">Deve trattarsi di un file eseguibile o di un file DLL.</span><span class="sxs-lookup"><span data-stu-id="045d5-121">This must be an executable file or a DLL file.</span></span>

</dd> <dt>

<span data-ttu-id="045d5-122"><span id="Path"></span><span id="path"></span><span id="PATH"></span>Percorso</span><span class="sxs-lookup"><span data-stu-id="045d5-122"><span id="Path"></span><span id="path"></span><span id="PATH"></span>Path</span></span>
</dt> <dd>

<span data-ttu-id="045d5-123">Elenco di percorsi, separati da punti e virgola, che rappresentano i percorsi in cui eseguire la ricerca per trovare le dll importate.</span><span class="sxs-lookup"><span data-stu-id="045d5-123">A list of paths, separated by semicolons, that represent the paths to be searched to find the imported DLLs.</span></span> <span data-ttu-id="045d5-124">L'elenco è in genere un elenco di proprietà, con ogni proprietà racchiusa tra parentesi quadre ( \[ \] ).</span><span class="sxs-lookup"><span data-stu-id="045d5-124">The list is usually a list of properties, with each property enclosed inside square brackets (\[ \]) .</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="045d5-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="045d5-125">Remarks</span></span>

<span data-ttu-id="045d5-126">Il programma di installazione calcola l'indirizzo virtuale di ogni funzione importata da tutte le dll e l'indirizzo virtuale calcolato viene quindi salvato nella tabella degli indirizzi di importazione (IAT) dell'immagine di importazione.</span><span class="sxs-lookup"><span data-stu-id="045d5-126">The installer computes the virtual address of each function that is imported from all DLLs, and the computed virtual address is then saved in the importing image's Import Address Table (IAT).</span></span>

<span data-ttu-id="045d5-127">Questa tabella viene definita quando viene eseguita l' [azione azione BindImage sul](bindimage-action.md) .</span><span class="sxs-lookup"><span data-stu-id="045d5-127">This table is referred to when the [BindImage action](bindimage-action.md) is executed.</span></span>

## <a name="validation"></a><span data-ttu-id="045d5-128">Convalida</span><span class="sxs-lookup"><span data-stu-id="045d5-128">Validation</span></span>

<dl>

[<span data-ttu-id="045d5-129">ICE03</span><span class="sxs-lookup"><span data-stu-id="045d5-129">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="045d5-130">ICE06</span><span class="sxs-lookup"><span data-stu-id="045d5-130">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="045d5-131">ICE32</span><span class="sxs-lookup"><span data-stu-id="045d5-131">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="045d5-132">ICE46</span><span class="sxs-lookup"><span data-stu-id="045d5-132">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="045d5-133">ICE76</span><span class="sxs-lookup"><span data-stu-id="045d5-133">ICE76</span></span>](ice76.md)  
</dl>

 

 



