---
description: ICE59 verifica che i collegamenti annunciati appartengano ai componenti installati dalla funzionalità di destinazione del collegamento.
ms.assetid: 9cd19137-792d-4fde-92d2-7d96942448d6
title: ICE59
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5631b723a158bb371fff3211654a70d694b6cb5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310978"
---
# <a name="ice59"></a><span data-ttu-id="24745-103">ICE59</span><span class="sxs-lookup"><span data-stu-id="24745-103">ICE59</span></span>

<span data-ttu-id="24745-104">ICE59 verifica che i collegamenti annunciati appartengano ai componenti installati dalla funzionalità di destinazione del collegamento.</span><span class="sxs-lookup"><span data-stu-id="24745-104">ICE59 checks that advertised shortcuts belong to components that are installed by the target feature of the shortcut.</span></span>

<span data-ttu-id="24745-105">Gli errori segnalati da ICE59 in genere comportano il comportamento seguente:</span><span class="sxs-lookup"><span data-stu-id="24745-105">Errors reported by ICE59 generally lead to the following behavior:</span></span>

1.  <span data-ttu-id="24745-106">Il collegamento annunciato avvierà il Windows Installer per installare la funzionalità elencata nella colonna destinazione.</span><span class="sxs-lookup"><span data-stu-id="24745-106">The advertised shortcut will launch the Windows Installer to install the feature listed in the Target column.</span></span>
2.  <span data-ttu-id="24745-107">Tuttavia, poiché la [tabella FeatureComponents](featurecomponents-table.md) non esegue il mapping della funzionalità di destinazione al componente contenente il collegamento, il file di base del componente (attivato dal collegamento) non è installato.</span><span class="sxs-lookup"><span data-stu-id="24745-107">But because the [FeatureComponents table](featurecomponents-table.md) does not map the target feature to the component containing the shortcut, the keyfile of the component (which is activated by the shortcut) is not installed.</span></span>
3.  <span data-ttu-id="24745-108">Pertanto, il collegamento viene rotto e non eseguirà alcuna operazione.</span><span class="sxs-lookup"><span data-stu-id="24745-108">Therefore the shortcut is broken and will not do anything.</span></span>

## <a name="result"></a><span data-ttu-id="24745-109">Risultato</span><span class="sxs-lookup"><span data-stu-id="24745-109">Result</span></span>

<span data-ttu-id="24745-110">ICE59 Invia un errore se un collegamento annunciato non appartiene ai componenti installati dalla funzionalità di destinazione del collegamento.</span><span class="sxs-lookup"><span data-stu-id="24745-110">ICE59 posts an error if an advertised shortcut does not belong to the components that are installed by the target feature of the shortcut.</span></span>

## <a name="example"></a><span data-ttu-id="24745-111">Esempio</span><span class="sxs-lookup"><span data-stu-id="24745-111">Example</span></span>

<span data-ttu-id="24745-112">ICE59 segnala l'errore seguente per l'esempio illustrato:</span><span class="sxs-lookup"><span data-stu-id="24745-112">ICE59 reports the following error for the example shown:</span></span>

``` syntax
The shortcut ShortcutB activates component ComponentB and advertises feature FeatureA, but there is no mapping between FeatureA and ComponentB in the FeatureComponents table.
```

<span data-ttu-id="24745-113">In questo caso, ShortcutB annuncia FeatureA e, quando attivato, avvia il file di chiave di ComponentB.</span><span class="sxs-lookup"><span data-stu-id="24745-113">In this case, ShortcutB advertises FeatureA, and when activated, starts the key file of ComponentB.</span></span> <span data-ttu-id="24745-114">Tuttavia, ComponentB non viene mai installato da FeatureA, quindi anche dopo che la fase di installazione su richiesta è stata completata, la destinazione del collegamento non esiste.</span><span class="sxs-lookup"><span data-stu-id="24745-114">Yet ComponentB is never installed by FeatureA, so even after the installation-on-demand phase completes, the target of the shortcut does not exist.</span></span>

<span data-ttu-id="24745-115">Per correggere l'errore, aggiungere una riga alla [tabella FeatureComponents](featurecomponents-table.md) che associa FeatureA e ComponentB.</span><span class="sxs-lookup"><span data-stu-id="24745-115">To fix this error, add a row to the [FeatureComponents table](featurecomponents-table.md) that associates FeatureA and ComponentB.</span></span>

<span data-ttu-id="24745-116">[Tabella collegamenti](shortcut-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="24745-116">[Shortcut Table](shortcut-table.md) (partial)</span></span>



| <span data-ttu-id="24745-117">Tasto di scelta rapida</span><span class="sxs-lookup"><span data-stu-id="24745-117">Shortcut</span></span>  | <span data-ttu-id="24745-118">Destinazione</span><span class="sxs-lookup"><span data-stu-id="24745-118">Target</span></span>   | <span data-ttu-id="24745-119">Componente\_</span><span class="sxs-lookup"><span data-stu-id="24745-119">Component\_</span></span> |
|-----------|----------|-------------|
| <span data-ttu-id="24745-120">ShortcutB</span><span class="sxs-lookup"><span data-stu-id="24745-120">ShortcutB</span></span> | <span data-ttu-id="24745-121">FunzionalitàA</span><span class="sxs-lookup"><span data-stu-id="24745-121">FeatureA</span></span> | <span data-ttu-id="24745-122">ComponentB</span><span class="sxs-lookup"><span data-stu-id="24745-122">ComponentB</span></span>  |



 

[<span data-ttu-id="24745-123">Tabella FeatureComponents</span><span class="sxs-lookup"><span data-stu-id="24745-123">FeatureComponents Table</span></span>](featurecomponents-table.md)



| <span data-ttu-id="24745-124">Funzionalità\_</span><span class="sxs-lookup"><span data-stu-id="24745-124">Feature\_</span></span> | <span data-ttu-id="24745-125">Componente\_</span><span class="sxs-lookup"><span data-stu-id="24745-125">Component\_</span></span> |
|-----------|-------------|
| <span data-ttu-id="24745-126">FunzionalitàA</span><span class="sxs-lookup"><span data-stu-id="24745-126">FeatureA</span></span>  | <span data-ttu-id="24745-127">ComponentA</span><span class="sxs-lookup"><span data-stu-id="24745-127">ComponentA</span></span>  |



 

<span data-ttu-id="24745-128">[Tabella delle funzionalità](feature-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="24745-128">[Feature Table](feature-table.md) (partial)</span></span>



| <span data-ttu-id="24745-129">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="24745-129">Feature</span></span>  | <span data-ttu-id="24745-130">Level</span><span class="sxs-lookup"><span data-stu-id="24745-130">Level</span></span> |
|----------|-------|
| <span data-ttu-id="24745-131">FunzionalitàA</span><span class="sxs-lookup"><span data-stu-id="24745-131">FeatureA</span></span> | <span data-ttu-id="24745-132">10</span><span class="sxs-lookup"><span data-stu-id="24745-132">10</span></span>    |



 

<span data-ttu-id="24745-133">[Tabella componenti](component-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="24745-133">[Component Table](component-table.md) (partial)</span></span>



| <span data-ttu-id="24745-134">Componente</span><span class="sxs-lookup"><span data-stu-id="24745-134">Component</span></span>  | <span data-ttu-id="24745-135">KeyPath</span><span class="sxs-lookup"><span data-stu-id="24745-135">KeyPath</span></span> |
|------------|---------|
| <span data-ttu-id="24745-136">ComponentA</span><span class="sxs-lookup"><span data-stu-id="24745-136">ComponentA</span></span> | <span data-ttu-id="24745-137">FileA</span><span class="sxs-lookup"><span data-stu-id="24745-137">FileA</span></span>   |
| <span data-ttu-id="24745-138">ComponentB</span><span class="sxs-lookup"><span data-stu-id="24745-138">ComponentB</span></span> | <span data-ttu-id="24745-139">FileB</span><span class="sxs-lookup"><span data-stu-id="24745-139">FileB</span></span>   |



 

<span data-ttu-id="24745-140">[Tabella file](file-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="24745-140">[File Table](file-table.md) (partial)</span></span>



| <span data-ttu-id="24745-141">File</span><span class="sxs-lookup"><span data-stu-id="24745-141">File</span></span>  | <span data-ttu-id="24745-142">Componente\_</span><span class="sxs-lookup"><span data-stu-id="24745-142">Component\_</span></span> | <span data-ttu-id="24745-143">Sequenza</span><span class="sxs-lookup"><span data-stu-id="24745-143">Sequence</span></span> |
|-------|-------------|----------|
| <span data-ttu-id="24745-144">FileA</span><span class="sxs-lookup"><span data-stu-id="24745-144">FileA</span></span> | <span data-ttu-id="24745-145">ComponentA</span><span class="sxs-lookup"><span data-stu-id="24745-145">ComponentA</span></span>  | <span data-ttu-id="24745-146">1</span><span class="sxs-lookup"><span data-stu-id="24745-146">1</span></span>        |
| <span data-ttu-id="24745-147">FileB</span><span class="sxs-lookup"><span data-stu-id="24745-147">FileB</span></span> | <span data-ttu-id="24745-148">ComponentB</span><span class="sxs-lookup"><span data-stu-id="24745-148">ComponentB</span></span>  | <span data-ttu-id="24745-149">2</span><span class="sxs-lookup"><span data-stu-id="24745-149">2</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="24745-150">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="24745-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="24745-151">Riferimento ghiaccio</span><span class="sxs-lookup"><span data-stu-id="24745-151">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



