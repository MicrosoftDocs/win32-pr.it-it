---
title: Proprietà ListeningTip
description: Proprietà ListeningTip
ms.assetid: 02a678bb-5eb6-495f-b339-35170a44b15e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 402fd970bf902f034fd6ffb713029e3a27095c8e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298791"
---
# <a name="listeningtip-property"></a><span data-ttu-id="82055-103">Proprietà ListeningTip</span><span class="sxs-lookup"><span data-stu-id="82055-103">ListeningTip Property</span></span>

<span data-ttu-id="82055-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="82055-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="82055-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="82055-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="82055-106">Restituisce un valore booleano che indica l'impostazione dell'utente corrente per il suggerimento di ascolto.</span><span class="sxs-lookup"><span data-stu-id="82055-106">Returns a Boolean indicating the current user setting for the Listening Tip.</span></span>

</dd> <dt>

<span data-ttu-id="82055-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="82055-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Syntax**</span></span> 
</dt> <dd>

<span data-ttu-id="82055-108">*agente \* \* *. SpeechInput.ListeningTip**</span><span class="sxs-lookup"><span data-stu-id="82055-108">*agent\*\*\*.SpeechInput.ListeningTip*\*</span></span>



| <span data-ttu-id="82055-109">Valore</span><span class="sxs-lookup"><span data-stu-id="82055-109">Value</span></span>     | <span data-ttu-id="82055-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="82055-110">Description</span></span>                    |
|-----------|--------------------------------|
| <span data-ttu-id="82055-111">**True**</span><span class="sxs-lookup"><span data-stu-id="82055-111">**True**</span></span>  | <span data-ttu-id="82055-112">Il suggerimento di ascolto è abilitato.</span><span class="sxs-lookup"><span data-stu-id="82055-112">The Listening Tip is enabled.</span></span>  |
| <span data-ttu-id="82055-113">**False**</span><span class="sxs-lookup"><span data-stu-id="82055-113">**False**</span></span> | <span data-ttu-id="82055-114">Il suggerimento di ascolto è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="82055-114">The Listening Tip is disabled.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="82055-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="82055-115">Remarks</span></span>

<span data-ttu-id="82055-116">La proprietà **ListeningTip** indica se l'opzione Visualizza suggerimento in ascolto nella finestra delle proprietà di Microsoft Agent (opzioni avanzate per i caratteri) è abilitata.</span><span class="sxs-lookup"><span data-stu-id="82055-116">The **ListeningTip** property indicates whether the Display Listening Tip option in the Microsoft Agent property sheet (Advanced Character Options) is enabled.</span></span> <span data-ttu-id="82055-117">Quando **ListeningTip** restituisce **true** e l'input vocale è abilitato, il server Visualizza la finestra di suggerimento quando l'utente preme il tasto di attesa.</span><span class="sxs-lookup"><span data-stu-id="82055-117">When **ListeningTip** returns **True** and speech input is enabled, the server displays the tip window when the user presses the Listening key.</span></span>

## <a name="see-also"></a><span data-ttu-id="82055-118">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="82055-118">See Also</span></span>

[<span data-ttu-id="82055-119">**Evento AgentPropertyChange**</span><span class="sxs-lookup"><span data-stu-id="82055-119">**AgentPropertyChange event**</span></span>](agentpropertychange-event.md)


 

 




