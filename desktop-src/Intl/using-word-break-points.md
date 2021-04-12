---
description: Quando l'applicazione sta gestendo parole intere, le posizioni valide per il punto di inserimento sono contrassegnate dal valore del membro fWordStop della \_ struttura LOGATTR dello script. Questo valore viene recuperato effettuando una chiamata a ScriptBreak.
ms.assetid: c9bbfb51-727a-45ff-8450-774bc106f9f7
title: Uso di punti di interruzioni di Word
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b9cf68d5c90b6e93a6e6f15706ec357c7a33b23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104234188"
---
# <a name="using-word-break-points"></a><span data-ttu-id="b082a-104">Uso di punti di interruzioni di Word</span><span class="sxs-lookup"><span data-stu-id="b082a-104">Using Word Break Points</span></span>

<span data-ttu-id="b082a-105">Quando l'applicazione sta gestendo parole intere, le posizioni valide per il punto di inserimento sono contrassegnate dal valore del membro **fWordStop** della [**struttura \_ LOGATTR dello script**](/windows/win32/api/usp10/ns-usp10-script_logattr) .</span><span class="sxs-lookup"><span data-stu-id="b082a-105">When the application is dealing with whole words, valid positions for the caret are marked by the value of the **fWordStop** member of the [**SCRIPT\_LOGATTR**](/windows/win32/api/usp10/ns-usp10-script_logattr) structure.</span></span> <span data-ttu-id="b082a-106">Questo valore viene recuperato effettuando una chiamata a [**ScriptBreak**](/windows/desktop/api/Usp10/nf-usp10-scriptbreak).</span><span class="sxs-lookup"><span data-stu-id="b082a-106">This value is retrieved by making a call to [**ScriptBreak**](/windows/desktop/api/Usp10/nf-usp10-scriptbreak).</span></span>

<span data-ttu-id="b082a-107">Le posizioni valide per suddividere le righe tra le parole sono contrassegnate dal valore **fSoftBreak** recuperato da [**ScriptBreak**](/windows/desktop/api/Usp10/nf-usp10-scriptbreak).</span><span class="sxs-lookup"><span data-stu-id="b082a-107">Valid positions for breaking lines between words are marked by the **fSoftBreak** value retrieved by [**ScriptBreak**](/windows/desktop/api/Usp10/nf-usp10-scriptbreak).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b082a-108">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b082a-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b082a-109">Uso di Uniscribe</span><span class="sxs-lookup"><span data-stu-id="b082a-109">Using Uniscribe</span></span>](using-uniscribe.md)
</dt> </dl>

 

 



