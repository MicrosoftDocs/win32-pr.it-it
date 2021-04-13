---
title: IAgentCommandsEx GetGlobalVoiceCommandsEnabled
description: IAgentCommandsEx GetGlobalVoiceCommandsEnabled
ms.assetid: 9c8fa978-a02b-4dfc-8cf7-e066c5b75122
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea7275bfe28190e06782cb2564dbf4868dd2c096
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104398946"
---
# <a name="iagentcommandsexgetglobalvoicecommandsenabled"></a><span data-ttu-id="a3b85-103">IAgentCommandsEx::GetGlobalVoiceCommandsEnabled</span><span class="sxs-lookup"><span data-stu-id="a3b85-103">IAgentCommandsEx::GetGlobalVoiceCommandsEnabled</span></span>

<span data-ttu-id="a3b85-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a3b85-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetGlobalVoiceCommandsEnabled(
   long * pbEnabled  // address of the global voice command setting
);
```

<span data-ttu-id="a3b85-105">Recupera un valore che indica se la grammatica vocale per i comandi globali dell'agente è abilitata.</span><span class="sxs-lookup"><span data-stu-id="a3b85-105">Retrieves whether the voice grammar for Agent's global commands is enabled.</span></span>

-   <span data-ttu-id="a3b85-106">Restituisce \_ OK per indicare che l'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="a3b85-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="a3b85-107"><span id="pbEnabled"></span><span id="pbenabled"></span><span id="PBENABLED"></span>*pbEnabled*</span><span class="sxs-lookup"><span data-stu-id="a3b85-107"><span id="pbEnabled"></span><span id="pbenabled"></span><span id="PBENABLED"></span>*pbEnabled*</span></span>
</dt> <dd>

<span data-ttu-id="a3b85-108">Indirizzo che riceve **true** se la grammatica vocale per i comandi globali dell'agente è abilitata, **false** se è disabilitata.</span><span class="sxs-lookup"><span data-stu-id="a3b85-108">The address that receives **True** if the voice grammar for Agent's global commands is enabled, **False** if disabled.</span></span>

</dd> </dl>

<span data-ttu-id="a3b85-109">Microsoft Agent aggiunge automaticamente i parametri vocali (grammatica) per l'apertura e la chiusura della finestra dei comandi vocali e per visualizzare e nascondere il carattere.</span><span class="sxs-lookup"><span data-stu-id="a3b85-109">Microsoft Agent automatically adds voice parameters (grammar) for opening and closing the Voice Commands Window and for showing and hiding the character.</span></span> <span data-ttu-id="a3b85-110">Quando questo metodo restituisce **false**, tutti i parametri vocali per questi comandi e i parametri vocali per la [**didascalia**](caption-property.md) degli oggetti [**comando**](/windows/desktop/lwef/the-command-object) di altri client non sono inclusi nella grammatica.</span><span class="sxs-lookup"><span data-stu-id="a3b85-110">When this method returns **False**, any voice parameters for these commands as well as the voice parameters for the [**Caption**](caption-property.md) of other clients' [**Command**](/windows/desktop/lwef/the-command-object) objects are not included in the grammar.</span></span> <span data-ttu-id="a3b85-111">In questo modo è possibile eliminarli dalla grammatica attiva corrente del client.</span><span class="sxs-lookup"><span data-stu-id="a3b85-111">This enables you to eliminate these from your client's current active grammar.</span></span> <span data-ttu-id="a3b85-112">Questa impostazione non riflette tuttavia l'inclusione di questi comandi nel menu di scelta rapida del carattere.</span><span class="sxs-lookup"><span data-stu-id="a3b85-112">However, this setting does not reflect the inclusion of these commands in the character's pop-up menu.</span></span>

## <a name="see-also"></a><span data-ttu-id="a3b85-113">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="a3b85-113">See Also</span></span>

[<span data-ttu-id="a3b85-114">**IAgentCommandsEx::SetGlobalVoiceCommandsEnabled**</span><span class="sxs-lookup"><span data-stu-id="a3b85-114">**IAgentCommandsEx::SetGlobalVoiceCommandsEnabled**</span></span>](iagentcommandsex--setglobalvoicecommandsenabled.md)


 

 