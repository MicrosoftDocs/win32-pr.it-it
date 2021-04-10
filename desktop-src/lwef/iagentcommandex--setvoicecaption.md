---
title: IAgentCommandEx SetVoiceCaption
description: IAgentCommandEx SetVoiceCaption
ms.assetid: 672fdc13-25d3-4ced-b295-2b687767c17f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 358514dd33fc97a98f9b63107eabc98e0387bab8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104046578"
---
# <a name="iagentcommandexsetvoicecaption"></a><span data-ttu-id="f8738-103">IAgentCommandEx::SetVoiceCaption</span><span class="sxs-lookup"><span data-stu-id="f8738-103">IAgentCommandEx::SetVoiceCaption</span></span>

<span data-ttu-id="f8738-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f8738-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetVoiceCaption(
   BSTR bszVoiceCaption  // voice caption text
);
```

<span data-ttu-id="f8738-105">Imposta il testo [**VoiceCaption**](voicecaption-property.md) visualizzato per un [**comando**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="f8738-105">Sets the [**VoiceCaption**](voicecaption-property.md) text displayed for a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

-   <span data-ttu-id="f8738-106">Restituisce \_ OK per indicare che l'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="f8738-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="f8738-107"><span id="bszVoiceCaption"></span><span id="bszvoicecaption"></span><span id="BSZVOICECAPTION"></span>*bszVoiceCaption*</span><span class="sxs-lookup"><span data-stu-id="f8738-107"><span id="bszVoiceCaption"></span><span id="bszvoicecaption"></span><span id="BSZVOICECAPTION"></span>*bszVoiceCaption*</span></span>
</dt> <dd>

<span data-ttu-id="f8738-108">BSTR che specifica il testo per la proprietà [**VoiceCaption**](voicecaption-property.md) per un [**comando**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="f8738-108">A BSTR that specifies the text for the [**VoiceCaption**](voicecaption-property.md) property for a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

</dd> </dl>

<span data-ttu-id="f8738-109">Se si definisce un oggetto [**Command**](/windows/desktop/lwef/the-command-object) in una raccolta di [**comandi**](/windows/desktop/lwef/the-commands-collection-object) e si imposta la relativa proprietà [**Voice**](voice-property.md) , in genere viene impostata anche la relativa proprietà [**VoiceCaption**](voicecaption-property.md) .</span><span class="sxs-lookup"><span data-stu-id="f8738-109">If you define a [**Command**](/windows/desktop/lwef/the-command-object) object in a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection and set its [**Voice**](voice-property.md) property, you will typically also set its [**VoiceCaption**](voicecaption-property.md) property.</span></span> <span data-ttu-id="f8738-110">Questo testo verrà visualizzato nella finestra comandi vocali quando l'applicazione client è di input attiva.</span><span class="sxs-lookup"><span data-stu-id="f8738-110">This text will appear in the Voice Commands Window when your client application is input active.</span></span> <span data-ttu-id="f8738-111">Se questa proprietà non è impostata, l'impostazione per la proprietà [**Caption**](caption-property.md) determina il testo visualizzato.</span><span class="sxs-lookup"><span data-stu-id="f8738-111">If this property is not set, the setting for the [**Caption**](caption-property.md) property determines the text displayed.</span></span> <span data-ttu-id="f8738-112">Quando non è impostata né la proprietà o **VoiceCaption** , il comando non viene visualizzato nella finestra dei comandi vocali.</span><span class="sxs-lookup"><span data-stu-id="f8738-112">When neither the **VoiceCaption** or property is set, the command does not appear in the Voice Commands Window.</span></span>

[<span data-ttu-id="f8738-113">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="f8738-113">**Caption**</span></span>](caption-property.md)

## <a name="see-also"></a><span data-ttu-id="f8738-114">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="f8738-114">See Also</span></span>

<span data-ttu-id="f8738-115">[**IAgentCommand:: GetCaption**](iagentcommand--getcaption.md), [**IAgentCommand:: seenabled**](iagentcommand--setenabled.md), [**IAgentCommand:: sevisible**](iagentcommand--setvisible.md), [**IAgentCommand:: sevoice**](iagentcommand--setvoice.md), [**IAgentCommandsEx:: AddEx**](iagentcommandsex--addex.md), [**IAgentCommandsEx:: InsertEx**](iagentcommandsex--insertex.md), [**IAgentCommands:: Add**](iagentcommands--add.md), [**IAgentCommands:: Insert**](iagentcommands--insert.md)</span><span class="sxs-lookup"><span data-stu-id="f8738-115">[**IAgentCommand::GetCaption**](iagentcommand--getcaption.md), [**IAgentCommand::SetEnabled**](iagentcommand--setenabled.md), [**IAgentCommand::SetVisible**](iagentcommand--setvisible.md), [**IAgentCommand::SetVoice**](iagentcommand--setvoice.md), [**IAgentCommandsEx::AddEx**](iagentcommandsex--addex.md), [**IAgentCommandsEx::InsertEx**](iagentcommandsex--insertex.md), [**IAgentCommands::Add**](iagentcommands--add.md), [**IAgentCommands::Insert**](iagentcommands--insert.md)</span></span>


 

 