---
description: ICE67 verifica che la destinazione di un collegamento non annunciato appartenga allo stesso componente del collegamento stesso o che gli attributi del componente di destinazione garantiscano che non modifichi i percorsi di installazione.
ms.assetid: 3fc462e7-4c11-4167-a157-6c1e0791901d
title: ICE67
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ca140a2d7eace9b693e82763f6bf5824346b51e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968236"
---
# <a name="ice67"></a><span data-ttu-id="02eeb-103">ICE67</span><span class="sxs-lookup"><span data-stu-id="02eeb-103">ICE67</span></span>

<span data-ttu-id="02eeb-104">ICE67 verifica che la destinazione di un collegamento non annunciato appartenga allo stesso componente del collegamento stesso o che gli attributi del componente di destinazione garantiscano che non modifichi i percorsi di installazione.</span><span class="sxs-lookup"><span data-stu-id="02eeb-104">ICE67 checks that the target of a non-advertised shortcut belongs to the same component as the shortcut itself, or that the attributes of the target component ensure that it does not change installation locations.</span></span>

<span data-ttu-id="02eeb-105">Se si verifica un errore durante la correzione di un avviso o di un errore segnalato da ICE67, il collegamento non può essere valido se lo stato del componente di destinazione è diverso da quello di origine.</span><span class="sxs-lookup"><span data-stu-id="02eeb-105">Failure to fix a warning or error reported by ICE67 can cause the shortcut to be invalid if the target component changes state and the source component does not.</span></span> <span data-ttu-id="02eeb-106">Ad esempio, quando il componente del file di destinazione è impostato per l'esecuzione dall'origine, una reinstallazione che modifica il componente in locale genera il componente contenente il collegamento che non viene reinstallato.</span><span class="sxs-lookup"><span data-stu-id="02eeb-106">For example, when the target file's component is set to run from source, a reinstallation that changes the component to local results in the component containing the shortcut not being reinstalled.</span></span> <span data-ttu-id="02eeb-107">Quindi il collegamento punta a una posizione non valida.</span><span class="sxs-lookup"><span data-stu-id="02eeb-107">Thus the shortcut points to an invalid location.</span></span>

<span data-ttu-id="02eeb-108">Si noti che in alcuni casi l'uso di un componente diverso per il collegamento è inevitabile.</span><span class="sxs-lookup"><span data-stu-id="02eeb-108">Note that in some cases, using a different component for the shortcut is unavoidable.</span></span> <span data-ttu-id="02eeb-109">Se, ad esempio, il collegamento viene creato nel profilo utente e il file viene installato in una directory non del profilo, potrebbe non essere possibile utilizzare lo stesso componente per entrambe le parti di dati.</span><span class="sxs-lookup"><span data-stu-id="02eeb-109">For example, if the shortcut is created in the user profile and the file is installed to a non-profile directory, you may not be able to use the same component for both pieces of data.</span></span> <span data-ttu-id="02eeb-110">Ciò comporta errori negli scenari multiutente, ad esempio quelli descritti in [ICE57](ice57.md).</span><span class="sxs-lookup"><span data-stu-id="02eeb-110">(This results in failures in multi-user scenarios – such as those described in [ICE57](ice57.md)).</span></span> <span data-ttu-id="02eeb-111">In questo caso, è possibile usare i tasti di scelta rapida annunciati per ottenere il comportamento desiderato. in alternativa, è sufficiente assicurarsi che il componente di destinazione non sia in grado di passare da Run-from-source a local.</span><span class="sxs-lookup"><span data-stu-id="02eeb-111">In this case, you may be able to use advertised shortcuts to achieve the behavior you want, or you can simply ensure that the target component cannot change from run-from-source to local.</span></span>

## <a name="result"></a><span data-ttu-id="02eeb-112">Risultato</span><span class="sxs-lookup"><span data-stu-id="02eeb-112">Result</span></span>

<span data-ttu-id="02eeb-113">ICE67 restituisce un errore o un avviso se la destinazione di un collegamento non annunciato non appartiene allo stesso componente del collegamento stesso o se gli attributi del componente di destinazione non assicurano che i percorsi di installazione non vengano modificati.</span><span class="sxs-lookup"><span data-stu-id="02eeb-113">ICE67 returns an error or a warning if the target of a non-advertised shortcut does not belong to the same component as the shortcut itself, or if the attributes of the target component do not ensure that the installation locations will not change.</span></span>

## <a name="example"></a><span data-ttu-id="02eeb-114">Esempio</span><span class="sxs-lookup"><span data-stu-id="02eeb-114">Example</span></span>

<span data-ttu-id="02eeb-115">ICE67 segnala i seguenti avvisi ed errori per l'esempio illustrato.</span><span class="sxs-lookup"><span data-stu-id="02eeb-115">ICE67 reports the following warning and errors for the example shown.</span></span>

``` syntax
The shortcut 'Shortcut1' is a non-advertised shortcut with a file target. The shortcut and target are installed by different components, and the target component can run locally or from source.
```

<span data-ttu-id="02eeb-116">Shortcut1 viene installato da Component2, ma il relativo file di destinazione, file1, viene installato da Component1.</span><span class="sxs-lookup"><span data-stu-id="02eeb-116">Shortcut1 is installed by Component2, but its target file, File1, is installed by component1.</span></span> <span data-ttu-id="02eeb-117">Il componente di destinazione è contrassegnato come facoltativo, ovvero può essere locale o di origine.</span><span class="sxs-lookup"><span data-stu-id="02eeb-117">The target component is marked optional (meaning that it can be local or run-from-source).</span></span> <span data-ttu-id="02eeb-118">Una possibile situazione che potrebbe causare un problema è il caso in cui Component1 modifiche da Run-from-source a local.</span><span class="sxs-lookup"><span data-stu-id="02eeb-118">One possible situation that would cause a problem is if Component1 changes from run-from-source to local.</span></span> <span data-ttu-id="02eeb-119">In questo modo Shortcut1 potrebbe puntare a una posizione non valida.</span><span class="sxs-lookup"><span data-stu-id="02eeb-119">This would cause Shortcut1 to point to an invalid location.</span></span>

<span data-ttu-id="02eeb-120">Per correggere il problema, installare il collegamento come parte di Component1 oppure contrassegnare Component1 come LocalOnly o SourceOnly.</span><span class="sxs-lookup"><span data-stu-id="02eeb-120">To fix this warning, Install the shortcut as part of Component1, or mark Component1 as LocalOnly or SourceOnly.</span></span>

<span data-ttu-id="02eeb-121">[Tabella file](file-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="02eeb-121">[File Table](file-table.md) (partial)</span></span>



| <span data-ttu-id="02eeb-122">File</span><span class="sxs-lookup"><span data-stu-id="02eeb-122">File</span></span>  | <span data-ttu-id="02eeb-123">Componente\_</span><span class="sxs-lookup"><span data-stu-id="02eeb-123">Component\_</span></span> |
|-------|-------------|
| <span data-ttu-id="02eeb-124">File1</span><span class="sxs-lookup"><span data-stu-id="02eeb-124">File1</span></span> | <span data-ttu-id="02eeb-125">Component1</span><span class="sxs-lookup"><span data-stu-id="02eeb-125">Component1</span></span>  |



 

<span data-ttu-id="02eeb-126">[Tabella collegamenti](shortcut-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="02eeb-126">[Shortcut Table](shortcut-table.md) (partial)</span></span>



| <span data-ttu-id="02eeb-127">Tasto di scelta rapida</span><span class="sxs-lookup"><span data-stu-id="02eeb-127">Shortcut</span></span>  | <span data-ttu-id="02eeb-128">Componente\_</span><span class="sxs-lookup"><span data-stu-id="02eeb-128">Component\_</span></span> | <span data-ttu-id="02eeb-129">Destinazione</span><span class="sxs-lookup"><span data-stu-id="02eeb-129">Target</span></span>      |
|-----------|-------------|-------------|
| <span data-ttu-id="02eeb-130">Shortcut1</span><span class="sxs-lookup"><span data-stu-id="02eeb-130">Shortcut1</span></span> | <span data-ttu-id="02eeb-131">Component2</span><span class="sxs-lookup"><span data-stu-id="02eeb-131">Component2</span></span>  | <span data-ttu-id="02eeb-132">\[\#File1\]</span><span class="sxs-lookup"><span data-stu-id="02eeb-132">\[\#File1\]</span></span> |



 

<span data-ttu-id="02eeb-133">[Tabella componenti](component-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="02eeb-133">[Component Table](component-table.md) (partial)</span></span>



| <span data-ttu-id="02eeb-134">Componente</span><span class="sxs-lookup"><span data-stu-id="02eeb-134">Component</span></span>  | <span data-ttu-id="02eeb-135">Attributi</span><span class="sxs-lookup"><span data-stu-id="02eeb-135">Attributes</span></span> |
|------------|------------|
| <span data-ttu-id="02eeb-136">Component1</span><span class="sxs-lookup"><span data-stu-id="02eeb-136">Component1</span></span> | <span data-ttu-id="02eeb-137">2</span><span class="sxs-lookup"><span data-stu-id="02eeb-137">2</span></span>          |



 

## <a name="related-topics"></a><span data-ttu-id="02eeb-138">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="02eeb-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="02eeb-139">Riferimento ghiaccio</span><span class="sxs-lookup"><span data-stu-id="02eeb-139">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



