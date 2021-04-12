---
title: TabbedToUnknownElement
description: TabbedToUnknownElement
ms.assetid: B0447B19-E281-4D30-8ED8-FC0EE13571C8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 612476d81779c882eeca807a9c3b82c41594f218
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395678"
---
# <a name="tabbedtounknownelement"></a><span data-ttu-id="a9c94-103">TabbedToUnknownElement</span><span class="sxs-lookup"><span data-stu-id="a9c94-103">TabbedToUnknownElement</span></span>

## <a name="text"></a><span data-ttu-id="a9c94-104">Testo</span><span class="sxs-lookup"><span data-stu-id="a9c94-104">Text</span></span>

<span data-ttu-id="a9c94-105">La tabulazione è stata spostata in un elemento al di fuori dell'HWND di destinazione.</span><span class="sxs-lookup"><span data-stu-id="a9c94-105">Tabbing has gone to an element outside the target hwnd.</span></span>

## <a name="type"></a><span data-ttu-id="a9c94-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="a9c94-106">Type</span></span>

<span data-ttu-id="a9c94-107">Errore</span><span class="sxs-lookup"><span data-stu-id="a9c94-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="a9c94-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a9c94-108">Description</span></span>

<span data-ttu-id="a9c94-109">Se si utilizza la navigazione da tastiera standard (TAB o MAIUSC + TAB), lo stato attivo viene spostato all'esterno dell'HWND della destinazione di verifica.</span><span class="sxs-lookup"><span data-stu-id="a9c94-109">Using standard keyboard navigation (Tab or Shift+Tab) causes focus to shift outside the HWND of the verification target.</span></span>

<span data-ttu-id="a9c94-110">AccChecker sposta l'albero degli elementi nell'HWND di primo livello per la destinazione di verifica scelta prima di eseguire qualsiasi attività di verifica.</span><span class="sxs-lookup"><span data-stu-id="a9c94-110">AccChecker moves up the element tree to the top-level HWND for the chosen verification target before running any verification tasks.</span></span> <span data-ttu-id="a9c94-111">In questo modo si riduce il numero di errori non corretti generati se un HWND scelto per la verifica fa parte di un'area client più complessa.</span><span class="sxs-lookup"><span data-stu-id="a9c94-111">This reduces the number of spurious errors generated if an HWND chosen for verification is part of a more complex client area.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="a9c94-112">Possibili cause</span><span class="sxs-lookup"><span data-stu-id="a9c94-112">Possible causes</span></span>

-   <span data-ttu-id="a9c94-113">La destinazione di verifica non richiede un'implementazione di tabulazione per fornire funzionalità complete.</span><span class="sxs-lookup"><span data-stu-id="a9c94-113">The verification target doesn't require a tabbing implementation to provide full functionality.</span></span>
-   <span data-ttu-id="a9c94-114">Interazione dell'utente durante la verifica, ad esempio lo spostare lo stato attivo su un HWND non di destinazione, interferisce con il processo di verifica.</span><span class="sxs-lookup"><span data-stu-id="a9c94-114">User interaction during verification, such as moving focus to a non-target HWND, interfered with the verification process.</span></span>

 

 




