---
description: La tabella seguente illustra i diversi metodi che possono essere usati dall'applicazione per gestire il punto di inserimento, la giustificazione e i cluster.
ms.assetid: 950a24b4-62ab-4eaf-ac15-87434d3c28c0
title: Utilizzo delle relazioni tra le posizioni del punto di inserimento, i punti di giustificazione e i cluster
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d051d008a8ae991b2858be598713fe9ad1adc0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307271"
---
# <a name="working-with-relationships-among-caret-positions-justification-points-and-clusters"></a><span data-ttu-id="7ac68-103">Utilizzo delle relazioni tra le posizioni del punto di inserimento, i punti di giustificazione e i cluster</span><span class="sxs-lookup"><span data-stu-id="7ac68-103">Working with Relationships Among Caret Positions, Justification Points, and Clusters</span></span>

<span data-ttu-id="7ac68-104">La tabella seguente illustra i diversi metodi che possono essere usati dall'applicazione per gestire il punto di inserimento, la giustificazione e i cluster.</span><span class="sxs-lookup"><span data-stu-id="7ac68-104">The following table shows the various methods that the application can use to handle the caret, justification, and clusters.</span></span>



| <span data-ttu-id="7ac68-105">Attività</span><span class="sxs-lookup"><span data-stu-id="7ac68-105">Task</span></span>                             | <span data-ttu-id="7ac68-106">Supporto di Uniscribe</span><span class="sxs-lookup"><span data-stu-id="7ac68-106">Uniscribe support</span></span>                                                                                                                                                                                                                                                              |
|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ac68-107">Spostamento del punto di inserimento per cluster di caratteri</span><span class="sxs-lookup"><span data-stu-id="7ac68-107">Caret move by character cluster</span></span>  | <span data-ttu-id="7ac68-108">Il parametro *pwLogClust* del membro [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) functionThe **fClusterStart** della struttura di [**script \_ VISATTR**](/windows/win32/api/usp10/ns-usp10-script_visattr)</span><span class="sxs-lookup"><span data-stu-id="7ac68-108">The *pwLogClust* parameter of the [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) functionThe **fClusterStart** member of the [**SCRIPT\_VISATTR**](/windows/win32/api/usp10/ns-usp10-script_visattr) structure</span></span><br/> <span data-ttu-id="7ac68-109">Membro **fCharStop** della struttura [**\_ LOGATTR dello script**](/windows/win32/api/usp10/ns-usp10-script_logattr)</span><span class="sxs-lookup"><span data-stu-id="7ac68-109">The **fCharStop** member of the [**SCRIPT\_LOGATTR**](/windows/win32/api/usp10/ns-usp10-script_logattr) structure</span></span><br/> |
| <span data-ttu-id="7ac68-110">Interruzioni di riga tra caratteri</span><span class="sxs-lookup"><span data-stu-id="7ac68-110">Line breaking between characters</span></span> | <span data-ttu-id="7ac68-111">Il parametro *pwLogClust* del membro [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) functionThe **fClusterStart** della struttura di [**script \_ VISATTR**](/windows/win32/api/usp10/ns-usp10-script_visattr)</span><span class="sxs-lookup"><span data-stu-id="7ac68-111">The *pwLogClust* parameter of the [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) functionThe **fClusterStart** member of the [**SCRIPT\_VISATTR**](/windows/win32/api/usp10/ns-usp10-script_visattr) structure</span></span><br/> <span data-ttu-id="7ac68-112">Membro **fCharStop** della struttura [**\_ LOGATTR dello script**](/windows/win32/api/usp10/ns-usp10-script_logattr)</span><span class="sxs-lookup"><span data-stu-id="7ac68-112">The **fCharStop** member of the [**SCRIPT\_LOGATTR**](/windows/win32/api/usp10/ns-usp10-script_logattr) structure</span></span><br/> |
| <span data-ttu-id="7ac68-113">Spostamento del cursore per parola</span><span class="sxs-lookup"><span data-stu-id="7ac68-113">Caret move by word</span></span>               | <span data-ttu-id="7ac68-114">Membro **fWordStop** della struttura [**\_ LOGATTR dello script**](/windows/win32/api/usp10/ns-usp10-script_logattr)</span><span class="sxs-lookup"><span data-stu-id="7ac68-114">The **fWordStop** member of the [**SCRIPT\_LOGATTR**](/windows/win32/api/usp10/ns-usp10-script_logattr) structure</span></span>                                                                                                                                                                                            |
| <span data-ttu-id="7ac68-115">Interruzioni di riga tra le parole</span><span class="sxs-lookup"><span data-stu-id="7ac68-115">Line breaking between words</span></span>      | <span data-ttu-id="7ac68-116">Membro **fWordStop** della struttura [**\_ LOGATTR dello script**](/windows/win32/api/usp10/ns-usp10-script_logattr)</span><span class="sxs-lookup"><span data-stu-id="7ac68-116">The **fWordStop** member of the [**SCRIPT\_LOGATTR**](/windows/win32/api/usp10/ns-usp10-script_logattr) structure</span></span>                                                                                                                                                                                            |
| <span data-ttu-id="7ac68-117">Giustificazione</span><span class="sxs-lookup"><span data-stu-id="7ac68-117">Justification</span></span>                    | <span data-ttu-id="7ac68-118">Membro **uJustification** della struttura [**\_ VISATTR dello script**](/windows/win32/api/usp10/ns-usp10-script_visattr)</span><span class="sxs-lookup"><span data-stu-id="7ac68-118">The **uJustification** member of the [**SCRIPT\_VISATTR**](/windows/win32/api/usp10/ns-usp10-script_visattr) structure</span></span>                                                                                                                                                                                       |



 

## <a name="related-topics"></a><span data-ttu-id="7ac68-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7ac68-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7ac68-120">Uso di Uniscribe</span><span class="sxs-lookup"><span data-stu-id="7ac68-120">Using Uniscribe</span></span>](using-uniscribe.md)
</dt> </dl>

 

 




