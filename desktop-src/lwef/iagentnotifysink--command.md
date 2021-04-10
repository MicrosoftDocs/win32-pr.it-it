---
title: Comando IAgentNotifySink
description: Comando IAgentNotifySink
ms.assetid: d54fb2e8-27d6-47a4-8a1e-5419a94ea26d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9690d2914db9d284cd4ba4b826905d3169b83f2c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103963019"
---
# <a name="iagentnotifysinkcommand"></a><span data-ttu-id="6cbe3-103">Comando IAgentNotifySink::</span><span class="sxs-lookup"><span data-stu-id="6cbe3-103">IAgentNotifySink::Command</span></span>

<span data-ttu-id="6cbe3-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="6cbe3-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Command(
   long dwCommandID,         // Command ID of the best match
   IUnknown * punkUserInput  // address of IAgentUserInput object 
);                          
```

<span data-ttu-id="6cbe3-105">Notifica a un'applicazione client che un [**comando**](/windows/desktop/lwef/the-command-object) è stato selezionato dall'utente.</span><span class="sxs-lookup"><span data-stu-id="6cbe3-105">Notifies a client application that a [**Command**](/windows/desktop/lwef/the-command-object) was selected by the user.</span></span>

-   <span data-ttu-id="6cbe3-106">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="6cbe3-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="6cbe3-107"><span id="dwCommandID"></span><span id="dwcommandid"></span><span id="DWCOMMANDID"></span>*dwCommandID*</span><span class="sxs-lookup"><span data-stu-id="6cbe3-107"><span id="dwCommandID"></span><span id="dwcommandid"></span><span id="DWCOMMANDID"></span>*dwCommandID*</span></span>
</dt> <dd>

<span data-ttu-id="6cbe3-108">Identificatore dell'alternativa del comando di corrispondenza migliore.</span><span class="sxs-lookup"><span data-stu-id="6cbe3-108">Identifier of the best match command alternative.</span></span>

</dd> <dt>

<span data-ttu-id="6cbe3-109"><span id="punkUserInput"></span><span id="punkuserinput"></span><span id="PUNKUSERINPUT"></span>*punkUserInput*</span><span class="sxs-lookup"><span data-stu-id="6cbe3-109"><span id="punkUserInput"></span><span id="punkuserinput"></span><span id="PUNKUSERINPUT"></span>*punkUserInput*</span></span>
</dt> <dd>

<span data-ttu-id="6cbe3-110">Indirizzo dell'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) per l'oggetto [**IAgentUserInput**](iagentuserinput.md) .</span><span class="sxs-lookup"><span data-stu-id="6cbe3-110">Address of the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface for the [**IAgentUserInput**](iagentuserinput.md) object.</span></span>

</dd> </dl>

<span data-ttu-id="6cbe3-111">Utilizzare [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) per recuperare l'interfaccia [**IAgentUserInput**](iagentuserinput.md) .</span><span class="sxs-lookup"><span data-stu-id="6cbe3-111">Use [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) to retrieve the [**IAgentUserInput**](iagentuserinput.md) interface.</span></span>

<span data-ttu-id="6cbe3-112">Il server invia una notifica al client di input attivo quando l'utente sceglie un comando mediante voce o selezionando un comando dal menu a comparsa del carattere.</span><span class="sxs-lookup"><span data-stu-id="6cbe3-112">The server notifies the input-active client when the user chooses a command by voice or by selecting a command from the character's pop-up menu.</span></span> <span data-ttu-id="6cbe3-113">L'evento si verifica anche quando l'utente seleziona uno dei comandi del server.</span><span class="sxs-lookup"><span data-stu-id="6cbe3-113">The event occurs even when the user selects one of the server's commands.</span></span> <span data-ttu-id="6cbe3-114">In questo caso il server restituisce un ID di comando null, il Punteggio di confidenza e il testo vocale restituiti dal motore di sintesi vocale per tale voce.</span><span class="sxs-lookup"><span data-stu-id="6cbe3-114">In this case the server returns a null command ID, the confidence score, and the voice text returned by the speech engine for that entry.</span></span>

## <a name="see-also"></a><span data-ttu-id="6cbe3-115">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="6cbe3-115">See Also</span></span>

[<span data-ttu-id="6cbe3-116">**IAgentUserInput**</span><span class="sxs-lookup"><span data-stu-id="6cbe3-116">**IAgentUserInput**</span></span>](iagentuserinput.md)


 

 