---
title: Nome IAgentCharacter
description: Nome IAgentCharacter
ms.assetid: 4944f910-60e9-446b-82e9-2794f445789a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec058e338adfa8c998bf26a1223ae71f0c7de3d4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298975"
---
# <a name="iagentcharactersetname"></a><span data-ttu-id="7ba95-103">IAgentCharacter:: nome</span><span class="sxs-lookup"><span data-stu-id="7ba95-103">IAgentCharacter::SetName</span></span>

<span data-ttu-id="7ba95-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="7ba95-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetName(
   BSTR bszName   // character name
);
```

<span data-ttu-id="7ba95-105">Imposta il nome del carattere.</span><span class="sxs-lookup"><span data-stu-id="7ba95-105">Sets the name of the character.</span></span>

-   <span data-ttu-id="7ba95-106">Restituisce \_ OK per indicare che l'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="7ba95-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="7ba95-107"><span id="bszName"></span><span id="bszname"></span><span id="BSZNAME"></span>*bszName*</span><span class="sxs-lookup"><span data-stu-id="7ba95-107"><span id="bszName"></span><span id="bszname"></span><span id="BSZNAME"></span>*bszName*</span></span>
</dt> <dd>

<span data-ttu-id="7ba95-108">BSTR che imposta il nome del carattere.</span><span class="sxs-lookup"><span data-stu-id="7ba95-108">A BSTR that sets the character's name.</span></span> <span data-ttu-id="7ba95-109">Il nome predefinito di un carattere viene definito quando viene compilato con l'editor dei caratteri di Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="7ba95-109">A character's default name is defined when it is compiled with the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="7ba95-110">È possibile modificarlo utilizzando **IAgentCharacter:: Sename**; Tuttavia, modifica il nome del carattere per tutti i client correnti del carattere.</span><span class="sxs-lookup"><span data-stu-id="7ba95-110">You can change it using **IAgentCharacter::SetName**; however, this changes the character name for all current clients of the character.</span></span> <span data-ttu-id="7ba95-111">Questa proprietà non è permanente (archiviata in modo permanente).</span><span class="sxs-lookup"><span data-stu-id="7ba95-111">This property is not persistent (stored permanently).</span></span> <span data-ttu-id="7ba95-112">Il nome del carattere viene ripristinato con il nome predefinito ogni volta che il carattere viene caricato per la prima volta da un client.</span><span class="sxs-lookup"><span data-stu-id="7ba95-112">The character's name reverts to its default name whenever the character is first loaded by a client.</span></span>

<span data-ttu-id="7ba95-113">Il nome del carattere può inoltre dipendere dall'ID della lingua.</span><span class="sxs-lookup"><span data-stu-id="7ba95-113">The character's name may also depend on its language ID.</span></span> <span data-ttu-id="7ba95-114">I caratteri possono essere compilati con nomi diversi per le diverse lingue.</span><span class="sxs-lookup"><span data-stu-id="7ba95-114">Characters can be compiled with different names for different languages.</span></span>

<span data-ttu-id="7ba95-115">Il server utilizza l'impostazione del nome del carattere in parti dell'interfaccia dell'agente Microsoft, ad esempio il titolo della finestra comandi vocali quando il carattere è input-attivo e nel menu a comparsa della barra delle applicazioni di Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="7ba95-115">The server uses the character's name setting in parts of the Microsoft Agent's interface, such as the Voice Commands Window title when the character is input-active and in the Microsoft Agent taskbar pop-up menu.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="7ba95-116">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="7ba95-116">See Also</span></span>

[<span data-ttu-id="7ba95-117">**IAgentCharacter:: GetName**</span><span class="sxs-lookup"><span data-stu-id="7ba95-117">**IAgentCharacter::GetName**</span></span>](iagentcharacter--getname.md)


 

 




