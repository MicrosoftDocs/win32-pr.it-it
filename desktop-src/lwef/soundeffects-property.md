---
title: Proprietà SoundEffects
description: Proprietà SoundEffects
ms.assetid: 39e48e5f-b24e-48ce-b5a3-85467ac252e9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fca45d373d39d479c62149a131f2a6678e5ecdf5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298107"
---
# <a name="soundeffects-property"></a><span data-ttu-id="b83d0-103">Proprietà SoundEffects</span><span class="sxs-lookup"><span data-stu-id="b83d0-103">SoundEffects Property</span></span>

<span data-ttu-id="b83d0-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="b83d0-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="b83d0-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="b83d0-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="b83d0-106">Restituisce un valore booleano che indica se gli effetti audio (. WAV) i file configurati come parte delle azioni di un carattere vengono riprodotti.</span><span class="sxs-lookup"><span data-stu-id="b83d0-106">Returns a Boolean indicating whether sound effects (.WAV) files configured as part of a character's actions will play.</span></span>

</dd> <dt>

<span data-ttu-id="b83d0-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="b83d0-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="b83d0-108">*agente \* \* *. AudioOutput.SoundEffects**</span><span class="sxs-lookup"><span data-stu-id="b83d0-108">*agent\*\*\*.AudioOutput.SoundEffects*\*</span></span>



| <span data-ttu-id="b83d0-109">Valore</span><span class="sxs-lookup"><span data-stu-id="b83d0-109">Value</span></span>     | <span data-ttu-id="b83d0-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b83d0-110">Description</span></span>                          |
|-----------|--------------------------------------|
| <span data-ttu-id="b83d0-111">**True**</span><span class="sxs-lookup"><span data-stu-id="b83d0-111">**True**</span></span>  | <span data-ttu-id="b83d0-112">Gli effetti audio del carattere sono abilitati.</span><span class="sxs-lookup"><span data-stu-id="b83d0-112">Character sound effects are enabled.</span></span> |
| <span data-ttu-id="b83d0-113">**False**</span><span class="sxs-lookup"><span data-stu-id="b83d0-113">**False**</span></span> | <span data-ttu-id="b83d0-114">L'effetto audio carattere è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="b83d0-114">Character sound effect are disabled.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b83d0-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="b83d0-115">Remarks</span></span>

<span data-ttu-id="b83d0-116">Questa proprietà riflette l'opzione Play Character Sound Effects nella pagina output della finestra delle proprietà dell'agente (Opzioni carattere avanzate).</span><span class="sxs-lookup"><span data-stu-id="b83d0-116">This property reflects the Play Character Sound Effects option on the Output page of the Agent property sheet (Advanced Character Options).</span></span> <span data-ttu-id="b83d0-117">Quando la proprietà **SoundEffects** restituisce **true**, verranno riprodotti gli effetti audio inclusi nella definizione di un carattere.</span><span class="sxs-lookup"><span data-stu-id="b83d0-117">When the **SoundEffects** property returns **True**, sound effects included in a character's definition will be played.</span></span> <span data-ttu-id="b83d0-118">Se è **false**, gli effetti audio non verranno riprodotti.</span><span class="sxs-lookup"><span data-stu-id="b83d0-118">When **False**, the sound effects will not be played.</span></span> <span data-ttu-id="b83d0-119">L'impostazione della proprietà ha effetto su tutti i caratteri ed è di sola lettura. il valore della proprietà può essere impostato solo dall'utente.</span><span class="sxs-lookup"><span data-stu-id="b83d0-119">The property setting affects all characters and is read-only; only the user can set this property value.</span></span>

## <a name="see-also"></a><span data-ttu-id="b83d0-120">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="b83d0-120">See Also</span></span>

[<span data-ttu-id="b83d0-121">**Evento AgentPropertyChange**</span><span class="sxs-lookup"><span data-stu-id="b83d0-121">**AgentPropertyChange event**</span></span>](agentpropertychange-event.md)


 

 




