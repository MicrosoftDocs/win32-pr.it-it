---
title: IAgentCommands sottotitoli
description: IAgentCommands sottotitoli
ms.assetid: 042f7366-0071-40a5-a47c-81c02cdbe3a9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a8c472bfbfd82235e21c28e24e7e0ce03223ff8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104398885"
---
# <a name="iagentcommandssetcaption"></a><span data-ttu-id="172a6-103">IAgentCommands:: Caption</span><span class="sxs-lookup"><span data-stu-id="172a6-103">IAgentCommands::SetCaption</span></span>

<span data-ttu-id="172a6-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="172a6-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetCaption(
   BSTR bszCaption  // Caption setting for Commands collection
);
```

<span data-ttu-id="172a6-105">Imposta il testo della [**didascalia**](caption-property.md) visualizzato per una raccolta di [**comandi**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="172a6-105">Sets the [**Caption**](caption-property.md) text displayed for a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

-   <span data-ttu-id="172a6-106">Restituisce \_ OK per indicare che l'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="172a6-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="172a6-107"><span id="bszCaption"></span><span id="bszcaption"></span><span id="BSZCAPTION"></span>*bszCaption*</span><span class="sxs-lookup"><span data-stu-id="172a6-107"><span id="bszCaption"></span><span id="bszcaption"></span><span id="BSZCAPTION"></span>*bszCaption*</span></span>
</dt> <dd>

<span data-ttu-id="172a6-108">BSTR che specifica il valore per la proprietà [**Caption**](caption-property.md) per una raccolta di [**comandi**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="172a6-108">A BSTR that specifies the value for the [**Caption**](caption-property.md) property for a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

</dd> </dl>

<span data-ttu-id="172a6-109">Impostando la proprietà [**Caption**](caption-property.md) per una raccolta di [**comandi**](/windows/desktop/lwef/the-commands-collection-object) , viene definita la modalità di visualizzazione nel menu popup del carattere quando la relativa proprietà [**Visible**](visible-property.md) è impostata su **true** e l'applicazione non è il client di input-Active.</span><span class="sxs-lookup"><span data-stu-id="172a6-109">Setting the [**Caption**](caption-property.md) property for a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection defines how it will appear on the character's pop-up menu when its [**Visible**](visible-property.md) property is set to **True** and your application is not the input-active client.</span></span> <span data-ttu-id="172a6-110">Per specificare un tasto di scelta (mnemonico) per la **didascalia**, includere un carattere e commerciale (&) prima di tale carattere.</span><span class="sxs-lookup"><span data-stu-id="172a6-110">To specify an access key (unlined mnemonic) for your **Caption**, include an ampersand (&) character before that character.</span></span>

<span data-ttu-id="172a6-111">Se si definiscono i comandi per una raccolta di [**comandi**](/windows/desktop/lwef/the-commands-collection-object) per cui è impostata la [**didascalia**](caption-property.md) , in genere si definisce anche una **didascalia** per la raccolta di **comandi** .</span><span class="sxs-lookup"><span data-stu-id="172a6-111">If you define commands for a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection that has its [**Caption**](caption-property.md) set, you typically also define a **Caption** for its **Commands** collection.</span></span>

## <a name="see-also"></a><span data-ttu-id="172a6-112">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="172a6-112">See Also</span></span>

<span data-ttu-id="172a6-113">[**IAgentCommands:: GetCaption**](iagentcommands--getcaption.md), [**IAgentCommands:: sevisible**](iagentcommands--setvisible.md), [**IAgentCommands:: sevoice**](iagentcommands--setvoice.md)</span><span class="sxs-lookup"><span data-stu-id="172a6-113">[**IAgentCommands::GetCaption**](iagentcommands--getcaption.md), [**IAgentCommands::SetVisible**](iagentcommands--setvisible.md), [**IAgentCommands::SetVoice**](iagentcommands--setvoice.md)</span></span>


 

 