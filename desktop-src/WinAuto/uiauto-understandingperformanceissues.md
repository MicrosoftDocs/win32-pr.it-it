---
title: Informazioni sui problemi di prestazioni
description: In questo argomento vengono descritti i problemi di prestazioni associati all'utilizzo dei pattern di controllo Text e TextRange.
ms.assetid: D78BFFA8-E303-441D-9D32-AD22E1B1A249
keywords:
- client, informazioni sui problemi di prestazioni
- client, controlli basati su testo
- client, intervalli di testo
- client, pattern di controllo Text
- client, pattern di controllo TextRange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61d8d9b9b6c5cb0ef3ed34c6960e5aeafa623068
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "104339723"
---
# <a name="understanding-performance-issues"></a><span data-ttu-id="410f0-108">Informazioni sui problemi di prestazioni</span><span class="sxs-lookup"><span data-stu-id="410f0-108">Understanding Performance Issues</span></span>

<span data-ttu-id="410f0-109">In questo argomento vengono descritti i problemi di prestazioni associati all'utilizzo dei pattern di controllo [Text e TextRange](uiauto-implementingtextandtextrange.md) .</span><span class="sxs-lookup"><span data-stu-id="410f0-109">This topic describes performance issues associated with using the [Text and TextRange](uiauto-implementingtextandtextrange.md) control patterns.</span></span>


<span data-ttu-id="410f0-110">Le interfacce [**IUIAutomationTextPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextpattern) e [**IUIAutomationTextRange**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange) si basano sulle chiamate tra processi, ma non forniscono un meccanismo di memorizzazione nella cache per migliorare le prestazioni durante il recupero o l'elaborazione di contenuto testuale.</span><span class="sxs-lookup"><span data-stu-id="410f0-110">The [**IUIAutomationTextPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextpattern) and [**IUIAutomationTextRange**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange) interfaces rely on cross-process calls—they do not provide a caching mechanism to improve performance when retrieving or processing textual content.</span></span>

<span data-ttu-id="410f0-111">Un'applicazione client può migliorare le prestazioni usando il metodo [**IUIAutomationTextRange:: GetText**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext) per recuperare blocchi di testo di dimensioni moderate.</span><span class="sxs-lookup"><span data-stu-id="410f0-111">A client application can improve performance by using the [**IUIAutomationTextRange::GetText**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-gettext) method to retrieve moderately sized blocks of text.</span></span> <span data-ttu-id="410f0-112">Ad esempio, l'utilizzo di **gettext** per recuperare singoli caratteri comporterà un riscontro delle prestazioni tra processi per ogni carattere, mentre se non si specifica una lunghezza massima durante la chiamata di **gettext** , viene raggiunto un hit tra processi, ma può avere una latenza elevata a seconda delle dimensioni dell'intervallo di testo.</span><span class="sxs-lookup"><span data-stu-id="410f0-112">For example, using **GetText** to retrieve single characters will incur a cross-process performance hit for each character, whereas not specifying a maximum length when calling **GetText** will incur one cross-process hit, but can have high latency depending on the size of the text range.</span></span>

## <a name="related-topics"></a><span data-ttu-id="410f0-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="410f0-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="410f0-114">Pattern di controllo Text e TextRange</span><span class="sxs-lookup"><span data-stu-id="410f0-114">Text and TextRange Control Patterns</span></span>](uiauto-implementingtextandtextrange.md)
</dt> <dt>

[<span data-ttu-id="410f0-115">Supporto di automazione interfaccia utente per contenuto testuale</span><span class="sxs-lookup"><span data-stu-id="410f0-115">UI Automation Support for Textual Content</span></span>](uiauto-ui-automation-textpattern-overview.md)
</dt> <dt>

[<span data-ttu-id="410f0-116">Utilizzo di controlli basati su testo</span><span class="sxs-lookup"><span data-stu-id="410f0-116">Working with Text-based Controls</span></span>](uiauto-workingwithtextbasedcontrols.md)
</dt> </dl>

 

 




