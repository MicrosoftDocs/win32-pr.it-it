---
title: IAgentCommandsEx SetGlobalVoiceCommandsEnabled
description: IAgentCommandsEx SetGlobalVoiceCommandsEnabled
ms.assetid: f456b1d3-60aa-4b90-90d0-6c695947fa8a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a87a576a36d3df4b3ddf0ca71f5709a712a3c9e1
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104117671"
---
# <a name="iagentcommandsexsetglobalvoicecommandsenabled"></a><span data-ttu-id="99319-103">IAgentCommandsEx::SetGlobalVoiceCommandsEnabled</span><span class="sxs-lookup"><span data-stu-id="99319-103">IAgentCommandsEx::SetGlobalVoiceCommandsEnabled</span></span>

<span data-ttu-id="99319-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="99319-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetGlobalVoiceCommandsEnabled(
 long bEnable  // Enabled setting for Agent's global voice commands
);
```

<span data-ttu-id="99319-105">Imposta la proprietà [**Enabled**](enabled-property.md) per la grammatica vocale dei comandi globali di Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="99319-105">Sets the [**Enabled**](enabled-property.md) property for the voice grammar of Microsoft Agent's global commands.</span></span>

-   <span data-ttu-id="99319-106">Restituisce \_ OK per indicare che l'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="99319-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="99319-107"><span id="bEnable"></span><span id="benable"></span><span id="BENABLE"></span>*bEnable*</span><span class="sxs-lookup"><span data-stu-id="99319-107"><span id="bEnable"></span><span id="benable"></span><span id="BENABLE"></span>*bEnable*</span></span>
</dt> <dd>

<span data-ttu-id="99319-108">Valore booleano che specifica se la grammatica vocale dei comandi globali dell'agente è abilitata.</span><span class="sxs-lookup"><span data-stu-id="99319-108">A Boolean value that sets whether the voice grammar of Agent's global commands is enabled.</span></span> <span data-ttu-id="99319-109">**True** Abilita la grammatica vocale; **False** lo Disabilita.</span><span class="sxs-lookup"><span data-stu-id="99319-109">**True** enables the voice grammar; **False** disables it.</span></span>

</dd> </dl>

<span data-ttu-id="99319-110">Microsoft Agent aggiunge automaticamente i parametri vocali (grammatica) per l'apertura e la chiusura della finestra dei comandi vocali e per visualizzare e nascondere il carattere.</span><span class="sxs-lookup"><span data-stu-id="99319-110">Microsoft Agent automatically adds voice parameters (grammar) for opening and closing the Voice Commands Window and for showing and hiding the character.</span></span> <span data-ttu-id="99319-111">Se impostato su **false**, Agent Disabilita tutti i parametri vocali per questi comandi, nonché i parametri vocali per la [**didascalia**](caption-property.md) degli oggetti [**comando**](/windows/desktop/lwef/the-command-object) di altri client.</span><span class="sxs-lookup"><span data-stu-id="99319-111">When set to **False**, Agent disables any voice parameters for these commands as well as the voice parameters for the [**Caption**](caption-property.md) of other client's [**Command**](/windows/desktop/lwef/the-command-object) objects.</span></span> <span data-ttu-id="99319-112">In questo modo è possibile eliminarli dalla grammatica attiva corrente del client.</span><span class="sxs-lookup"><span data-stu-id="99319-112">This enables you to eliminate these from your client's current active grammar.</span></span> <span data-ttu-id="99319-113">Tuttavia, poiché questo potrebbe bloccare l'accesso vocale ad altri client, reimpostare questa proprietà su **true** dopo l'elaborazione dell'input vocale dell'utente.</span><span class="sxs-lookup"><span data-stu-id="99319-113">However, because this potentially blocks voice access to other clients, reset this property to **True** after processing the user's voice input.</span></span>

<span data-ttu-id="99319-114">La disabilitazione della proprietà non influisce sul menu di scelta rapida del carattere.</span><span class="sxs-lookup"><span data-stu-id="99319-114">Disabling the property does not affect the character's pop-up menu.</span></span> <span data-ttu-id="99319-115">Verranno comunque visualizzati i comandi globali aggiunti dal server.</span><span class="sxs-lookup"><span data-stu-id="99319-115">The global commands added by the server will still appear.</span></span> <span data-ttu-id="99319-116">Non è possibile rimuoverli dal menu a comparsa.</span><span class="sxs-lookup"><span data-stu-id="99319-116">You cannot remove them from the pop-up menu.</span></span>

## <a name="see-also"></a><span data-ttu-id="99319-117">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="99319-117">See Also</span></span>

[<span data-ttu-id="99319-118">**IAgentCommandsEx::GetGlobalVoiceCommandsEnabled**</span><span class="sxs-lookup"><span data-stu-id="99319-118">**IAgentCommandsEx::GetGlobalVoiceCommandsEnabled**</span></span>](iagentcommandsex--getglobalvoicecommandsenabled.md)


 

 