---
title: IAgentCommand sottotitoli
description: IAgentCommand sottotitoli
ms.assetid: f4fdd37a-28b4-4e00-885c-58addedec659
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88453f54ffa59b413f30d27c58aa6cd2dcc6e12e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104046665"
---
# <a name="iagentcommandsetcaption"></a><span data-ttu-id="e7f62-103">IAgentCommand:: Caption</span><span class="sxs-lookup"><span data-stu-id="e7f62-103">IAgentCommand::SetCaption</span></span>

<span data-ttu-id="e7f62-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e7f62-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetCaption(
   BSTR bszCaption  // Caption setting for Command
);
```

<span data-ttu-id="e7f62-105">Imposta il testo della [**didascalia**](caption-property.md) visualizzato per un [**comando**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="e7f62-105">Sets the [**Caption**](caption-property.md) text displayed for a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

-   <span data-ttu-id="e7f62-106">Restituisce \_ OK per indicare che l'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="e7f62-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="e7f62-107"><span id="bszCaption"></span><span id="bszcaption"></span><span id="BSZCAPTION"></span>*bszCaption*</span><span class="sxs-lookup"><span data-stu-id="e7f62-107"><span id="bszCaption"></span><span id="bszcaption"></span><span id="BSZCAPTION"></span>*bszCaption*</span></span>
</dt> <dd>

<span data-ttu-id="e7f62-108">BSTR che specifica il testo per la proprietà [**Caption**](caption-property.md) per un [**comando**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="e7f62-108">A BSTR that specifies the text for the [**Caption**](caption-property.md) property for a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

</dd> </dl>

<span data-ttu-id="e7f62-109">L'impostazione della proprietà [**Caption**](caption-property.md) per un [**comando**](/windows/desktop/lwef/the-command-object) ne definisce la modalità di visualizzazione nel menu popup del carattere quando la relativa proprietà [**Visible**](visible-property.md) è impostata su **true** e l'applicazione non è il client di input-Active.</span><span class="sxs-lookup"><span data-stu-id="e7f62-109">Setting the [**Caption**](caption-property.md) property for a [**Command**](/windows/desktop/lwef/the-command-object) defines how it will appear on the character's pop-up menu when its [**Visible**](visible-property.md) property is set to **True** and your application is not the input-active client.</span></span> <span data-ttu-id="e7f62-110">Per specificare un tasto di scelta (mnemonico) per la **didascalia**, includere un carattere e commerciale (&) prima di tale carattere.</span><span class="sxs-lookup"><span data-stu-id="e7f62-110">To specify an access key (unlined mnemonic) for your **Caption**, include an ampersand (&) character before that character.</span></span> <span data-ttu-id="e7f62-111">Per renderla selezionabile, la relativa proprietà [**Enabled**](enabled-property.md) deve essere impostata su **true**.</span><span class="sxs-lookup"><span data-stu-id="e7f62-111">To make it selectable, its [**Enabled**](enabled-property.md) property must be set to **True**.</span></span>

## <a name="see-also"></a><span data-ttu-id="e7f62-112">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="e7f62-112">See Also</span></span>

<span data-ttu-id="e7f62-113">[**IAgentCommand:: GetCaption**](iagentcommand--getcaption.md), [**IAgentCommand:: seenabled**](iagentcommand--setenabled.md), [**IAgentCommand:: sevisible**](iagentcommand--setvisible.md), [**IAgentCommand:: sevoice**](iagentcommand--setvoice.md), [**IAgentCommands:: Add**](iagentcommands--add.md), [**IAgentCommands:: Insert**](iagentcommands--insert.md)</span><span class="sxs-lookup"><span data-stu-id="e7f62-113">[**IAgentCommand::GetCaption**](iagentcommand--getcaption.md), [**IAgentCommand::SetEnabled**](iagentcommand--setenabled.md), [**IAgentCommand::SetVisible**](iagentcommand--setvisible.md), [**IAgentCommand::SetVoice**](iagentcommand--setvoice.md), [**IAgentCommands::Add**](iagentcommands--add.md), [**IAgentCommands::Insert**](iagentcommands--insert.md)</span></span>


 

 