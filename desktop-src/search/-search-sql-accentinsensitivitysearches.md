---
description: Per impostazione predefinita, il motore di ricerca di Windows e il catalogo non sono sensibili ai segni diacritici, che sono contrassegni accentati aggiunti alle lettere per modificare il significato o la pronuncia di una parola.
ms.assetid: 71007bd4-5232-469c-982b-ff0d24bd0c1f
title: Distinzione tra segni diacritici nelle ricerche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46fb68676418fc109fa24ed2d55fb9602b7ad41d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306138"
---
# <a name="diacritic-sensitivity-in-searches"></a><span data-ttu-id="dedb4-103">Distinzione tra segni diacritici nelle ricerche</span><span class="sxs-lookup"><span data-stu-id="dedb4-103">Diacritic Sensitivity in Searches</span></span>

<span data-ttu-id="dedb4-104">Per impostazione predefinita, il motore di ricerca di Windows e il catalogo non sono sensibili ai segni diacritici, che sono contrassegni accentati aggiunti alle lettere per modificare il significato o la pronuncia di una parola.</span><span class="sxs-lookup"><span data-stu-id="dedb4-104">By default, the Windows Search engine and catalog are insensitive to diacritics, which are accent marks added to letters to alter a word's meaning or pronunciation.</span></span> <span data-ttu-id="dedb4-105">Windows Search consente tuttavia di modificare questa impostazione per il catalogo usando [gestione catalogo](-search-3x-wds-mngidx-catalog-manager.md) per impostare la sensibilità dei segni diacritici.</span><span class="sxs-lookup"><span data-stu-id="dedb4-105">However, Windows Search enables you to change this for your catalog using the [Catalog Manager](-search-3x-wds-mngidx-catalog-manager.md) to set diacritic sensitivity.</span></span> <span data-ttu-id="dedb4-106">Con la sensibilità dei segni diacritici impostata su **false**, ad esempio, il catalogo considera "Resume" e "curriculum" come se fossero la stessa parola.</span><span class="sxs-lookup"><span data-stu-id="dedb4-106">For example, with diacritic sensitivity set to **FALSE**, the catalog would treat "resume" and "resumé" as if they were the same word.</span></span>

<span data-ttu-id="dedb4-107">A livello di query, i termini di query con segni diacritici nelle clausole FREETEXT e CONTAINs vengono passati al motore e vengono quindi normalizzati (come in fase di indicizzazione) per la corrispondenza.</span><span class="sxs-lookup"><span data-stu-id="dedb4-107">At the query layer, query terms with diacritics in FREETEXT and CONTAINS clauses are passed through to the engine and are then normalized (as they would be at index time) for matching.</span></span> <span data-ttu-id="dedb4-108">La corrispondenza con il catalogo è sempre sensibile ai segni diacritici.</span><span class="sxs-lookup"><span data-stu-id="dedb4-108">Matching against the catalog is always diacritic sensitive.</span></span>

> [!Note]  
> <span data-ttu-id="dedb4-109">Questo non avviene per gli intervalli di caratteri 0x2e81-F8FF e 0x1100-0x11ff.</span><span class="sxs-lookup"><span data-stu-id="dedb4-109">This is not the case for the character ranges 0x2e81-f8ff and 0x1100-0x11ff.</span></span>

 

 

 



