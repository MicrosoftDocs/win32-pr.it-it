---
description: ICE36 verifica che ogni icona nella tabella delle icone sia elencata almeno una volta nella proprietà ARPPRODUCTICON o nelle tabelle di classe, ProgId o collegamento.
ms.assetid: d502c0a9-17e5-467a-8b02-8b254e77b96b
title: ICE36
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7f24eebc1b591edde418c59b6765d7ee91a00dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104057808"
---
# <a name="ice36"></a><span data-ttu-id="99c95-103">ICE36</span><span class="sxs-lookup"><span data-stu-id="99c95-103">ICE36</span></span>

<span data-ttu-id="99c95-104">ICE36 verifica che ogni icona nella tabella delle icone sia elencata almeno una volta nella proprietà [**arpproducticon**](arpproducticon.md) o nelle tabelle di [classe](class-table.md), [ProgID](progid-table.md)o [collegamento](shortcut-table.md) .</span><span class="sxs-lookup"><span data-stu-id="99c95-104">ICE36 validates that every icon in the Icon table is listed at least once in the [**ARPPRODUCTICON**](arpproducticon.md) property or the [Class](class-table.md), [ProgId](progid-table.md), or [Shortcut](shortcut-table.md) tables.</span></span>

<span data-ttu-id="99c95-105">Durante l'annuncio, il programma di installazione installa tutte le icone elencate nella [tabella](icon-table.md) delle icone nel computer dell'utente.</span><span class="sxs-lookup"><span data-stu-id="99c95-105">During advertisement, the installer installs all the icons listed in the [Icon table](icon-table.md) on the user's computer.</span></span> <span data-ttu-id="99c95-106">La presenza di icone inutilizzate nella tabella delle icone non impedisce l'esecuzione dell'installazione. Tuttavia, aumenta inutilmente le dimensioni del file con estensione msi e il tempo e lo spazio necessari per annunciare una funzionalità.</span><span class="sxs-lookup"><span data-stu-id="99c95-106">Having unused icons in the Icon table does not prevent the installation from running, however it does unnecessarily increase the size of the .msi file and the time and space required to advertise a feature.</span></span>

<span data-ttu-id="99c95-107">Se non viene fatto riferimento a un'icona nella proprietà o nella tabella e non è disponibile alcuna interfaccia utente per creare un riferimento in fase di esecuzione, è necessario rimuovere l'icona per ottenere prestazioni migliori.</span><span class="sxs-lookup"><span data-stu-id="99c95-107">If an icon is not referenced in the property or table and there is no UI provided to create a reference at run time, you should remove the icon to achieve better performance.</span></span>

## <a name="result"></a><span data-ttu-id="99c95-108">Risultato</span><span class="sxs-lookup"><span data-stu-id="99c95-108">Result</span></span>

<span data-ttu-id="99c95-109">ICE36 Invia un messaggio se è presente un'icona nella tabella delle icone a cui non viene fatto riferimento nelle tabelle [class](class-table.md), [ProgID](progid-table.md)o [Shortcut](shortcut-table.md) e se non è disponibile alcuna interfaccia utente per creare un riferimento di questo tipo in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="99c95-109">ICE36 posts a message if there is a icon in the Icon table that is not referenced in the [Class](class-table.md), [ProgId](progid-table.md), or [Shortcut](shortcut-table.md) tables and if there is no UI provided to create such a reference at run time.</span></span>

## <a name="example"></a><span data-ttu-id="99c95-110">Esempio</span><span class="sxs-lookup"><span data-stu-id="99c95-110">Example</span></span>

<span data-ttu-id="99c95-111">ICE36 segnala l'errore seguente per l'esempio illustrato.</span><span class="sxs-lookup"><span data-stu-id="99c95-111">ICE36 reports the following error for the example shown.</span></span>

``` syntax
Icon Bloat. Icon Icon4 is not used in the Class, Shortcut, or ProgID table. This adversely affects performance.
```

<span data-ttu-id="99c95-112">[Tabella icone](icon-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="99c95-112">[Icon Table](icon-table.md) (partial)</span></span>



| <span data-ttu-id="99c95-113">Nome</span><span class="sxs-lookup"><span data-stu-id="99c95-113">Name</span></span>  | <span data-ttu-id="99c95-114">Data</span><span class="sxs-lookup"><span data-stu-id="99c95-114">Data</span></span>     |
|-------|----------|
| <span data-ttu-id="99c95-115">Icon1</span><span class="sxs-lookup"><span data-stu-id="99c95-115">Icon1</span></span> | <span data-ttu-id="99c95-116">Control1</span><span class="sxs-lookup"><span data-stu-id="99c95-116">Control1</span></span> |
| <span data-ttu-id="99c95-117">Icon2</span><span class="sxs-lookup"><span data-stu-id="99c95-117">Icon2</span></span> | <span data-ttu-id="99c95-118">Controllo2</span><span class="sxs-lookup"><span data-stu-id="99c95-118">Control2</span></span> |
| <span data-ttu-id="99c95-119">Icon3</span><span class="sxs-lookup"><span data-stu-id="99c95-119">Icon3</span></span> | <span data-ttu-id="99c95-120">Control3</span><span class="sxs-lookup"><span data-stu-id="99c95-120">Control3</span></span> |
| <span data-ttu-id="99c95-121">Icon4</span><span class="sxs-lookup"><span data-stu-id="99c95-121">Icon4</span></span> | <span data-ttu-id="99c95-122">Control4</span><span class="sxs-lookup"><span data-stu-id="99c95-122">Control4</span></span> |



 

<span data-ttu-id="99c95-123">[Tabella ProgId](progid-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="99c95-123">[ProgID Table](progid-table.md) (partial)</span></span>



| <span data-ttu-id="99c95-124">ProgID</span><span class="sxs-lookup"><span data-stu-id="99c95-124">ProgID</span></span>    |
|-----------|
| <span data-ttu-id="99c95-125">Property1</span><span class="sxs-lookup"><span data-stu-id="99c95-125">Property1</span></span> |



 

<span data-ttu-id="99c95-126">[Tabella classi](class-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="99c95-126">[Class Table](class-table.md) (partial)</span></span>



| <span data-ttu-id="99c95-127">CLSID</span><span class="sxs-lookup"><span data-stu-id="99c95-127">CLSID</span></span>                                  |
|----------------------------------------|
| <span data-ttu-id="99c95-128">{3E469ABA-3644-11d2-8892-00A0C981B015}</span><span class="sxs-lookup"><span data-stu-id="99c95-128">{3E469ABA-3644-11d2-8892-00A0C981B015}</span></span> |



 

<span data-ttu-id="99c95-129">[Tabella collegamenti](shortcut-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="99c95-129">[Shortcut Table](shortcut-table.md) (partial)</span></span>



| <span data-ttu-id="99c95-130">Tasto di scelta rapida</span><span class="sxs-lookup"><span data-stu-id="99c95-130">Shortcut</span></span>  | <span data-ttu-id="99c95-131">Icona\_</span><span class="sxs-lookup"><span data-stu-id="99c95-131">Icon\_</span></span> |
|-----------|--------|
| <span data-ttu-id="99c95-132">Shortcut1</span><span class="sxs-lookup"><span data-stu-id="99c95-132">Shortcut1</span></span> | <span data-ttu-id="99c95-133">Icon2</span><span class="sxs-lookup"><span data-stu-id="99c95-133">Icon2</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="99c95-134">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="99c95-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="99c95-135">Riferimento ghiaccio</span><span class="sxs-lookup"><span data-stu-id="99c95-135">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



