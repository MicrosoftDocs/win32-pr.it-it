---
description: I cluster di caratteri sono sequenze di glifi che non possono essere suddivise tra le linee.
ms.assetid: ab852feb-9e26-429e-a02a-11fe0abdfafc
title: Uso di cluster di caratteri
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11357a929cf8fec2a7b0caa2bb6ae1ac403e3b91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760487"
---
# <a name="using-character-clusters"></a><span data-ttu-id="6f5ed-103">Uso di cluster di caratteri</span><span class="sxs-lookup"><span data-stu-id="6f5ed-103">Using Character Clusters</span></span>

<span data-ttu-id="6f5ed-104">I cluster di caratteri sono sequenze di glifi che non possono essere suddivise tra le linee.</span><span class="sxs-lookup"><span data-stu-id="6f5ed-104">Character clusters are glyph sequences that cannot be split between lines.</span></span> <span data-ttu-id="6f5ed-105">Alcuni linguaggi, ad esempio Thai e indiano, limitano il posizionamento del punto di inserimento ai punti tra i cluster.</span><span class="sxs-lookup"><span data-stu-id="6f5ed-105">Some languages, for example Thai and Indic, restrict caret placement to points between clusters.</span></span> <span data-ttu-id="6f5ed-106">Questa restrizione si applica al movimento del cursore avviato con azioni della tastiera o del mouse (hit testing).</span><span class="sxs-lookup"><span data-stu-id="6f5ed-106">This restriction applies to caret movement initiated with keyboard or mouse actions (hit testing).</span></span>

<span data-ttu-id="6f5ed-107">Uniscribe fornisce informazioni sul cluster sia negli attributi visivi contenuti in una struttura di [**script \_ VISATTR**](/windows/win32/api/usp10/ns-usp10-script_visattr) che negli attributi logici contenuti in una struttura [**\_ LOGATTR di script**](/windows/win32/api/usp10/ns-usp10-script_logattr) .</span><span class="sxs-lookup"><span data-stu-id="6f5ed-107">Uniscribe provides cluster information in both the visual attributes contained in a [**SCRIPT\_VISATTR**](/windows/win32/api/usp10/ns-usp10-script_visattr) structure, and the logical attributes contained in a [**SCRIPT\_LOGATTR**](/windows/win32/api/usp10/ns-usp10-script_logattr) structure.</span></span> <span data-ttu-id="6f5ed-108">Dopo che l'applicazione chiama [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape), le informazioni sul cluster vengono rappresentate sia dalle sequenze dello stesso valore nella **matrice \_ LOGATTR dello script** che dal membro **fClusterStart** nella matrice **\_ VISATTR di script** .</span><span class="sxs-lookup"><span data-stu-id="6f5ed-108">After the application calls [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape), the cluster information is represented both by sequences of the same value in the **SCRIPT\_LOGATTR** array, and by the **fClusterStart** member in the **SCRIPT\_VISATTR** array.</span></span>

<span data-ttu-id="6f5ed-109">[**ScriptBreak**](/windows/desktop/api/Usp10/nf-usp10-scriptbreak) recupera anche il membro **fCharStop** della struttura [**\_ LOGATTR dello script**](/windows/win32/api/usp10/ns-usp10-script_logattr) per identificare le posizioni del cluster.</span><span class="sxs-lookup"><span data-stu-id="6f5ed-109">[**ScriptBreak**](/windows/desktop/api/Usp10/nf-usp10-scriptbreak) also retrieves the **fCharStop** member of the [**SCRIPT\_LOGATTR**](/windows/win32/api/usp10/ns-usp10-script_logattr) structure to identify cluster positions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6f5ed-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6f5ed-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6f5ed-111">Uso di Uniscribe</span><span class="sxs-lookup"><span data-stu-id="6f5ed-111">Using Uniscribe</span></span>](using-uniscribe.md)
</dt> </dl>

 

 



