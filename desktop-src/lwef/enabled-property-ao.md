---
title: Proprietà Enabled (oggetto AudioOutput)
description: Informazioni sulla proprietà dell'oggetto Enabled AudioOutput. Microsoft Agent è deprecato a livello di Windows 7.
ms.assetid: 6526f249-be13-4732-b79e-a9952489461f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b807b4cadcc9a0157b4efa400dd9d0e3cb5cf21a
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407344"
---
# <a name="enabled-property-audiooutput-object"></a><span data-ttu-id="eb254-104">Proprietà Enabled (oggetto AudioOutput)</span><span class="sxs-lookup"><span data-stu-id="eb254-104">Enabled Property (AudioOutput Object)</span></span>

<span data-ttu-id="eb254-105">\[Microsoft Agent è deprecato a livello di Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="eb254-105">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="eb254-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="eb254-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="eb254-107">Restituisce un valore booleano che indica se l'output audio (parlato) è abilitato.</span><span class="sxs-lookup"><span data-stu-id="eb254-107">Returns a Boolean indicating whether audio (spoken) output is enabled.</span></span>

</dd> <dt>

<span data-ttu-id="eb254-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="eb254-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="eb254-109">*agent\*\*\*. AudioOutput.Enabled*\*</span><span class="sxs-lookup"><span data-stu-id="eb254-109">*agent\*\*\*.AudioOutput.Enabled*\*</span></span>



| <span data-ttu-id="eb254-110">Valore</span><span class="sxs-lookup"><span data-stu-id="eb254-110">Value</span></span>     | <span data-ttu-id="eb254-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="eb254-111">Description</span></span>                               |
|-----------|-------------------------------------------|
| <span data-ttu-id="eb254-112">**True**</span><span class="sxs-lookup"><span data-stu-id="eb254-112">**True**</span></span>  | <span data-ttu-id="eb254-113">(Impostazione predefinita) L'output audio parlato è abilitato.</span><span class="sxs-lookup"><span data-stu-id="eb254-113">(Default) Spoken audio output is enabled.</span></span> |
| <span data-ttu-id="eb254-114">**False**</span><span class="sxs-lookup"><span data-stu-id="eb254-114">**False**</span></span> | <span data-ttu-id="eb254-115">L'output audio parlato è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="eb254-115">Spoken audio output is disabled.</span></span>          |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="eb254-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="eb254-116">Remarks</span></span>

<span data-ttu-id="eb254-117">Questa proprietà riflette l'opzione Riproduci output audio nella pagina Output della finestra delle proprietà agente (Opzioni carattere avanzate).</span><span class="sxs-lookup"><span data-stu-id="eb254-117">This property reflects the Play Audio Output option on the Output page of the Agent property sheet (Advanced Character Options).</span></span> <span data-ttu-id="eb254-118">Quando la [**proprietà Enabled**](enabled-property.md) restituisce **True,** il metodo [**Speak**](speak-method.md) produce output audio se è installato un motore TTS compatibile o si usano file audio per l'output parlato.</span><span class="sxs-lookup"><span data-stu-id="eb254-118">When the [**Enabled**](enabled-property.md) property returns **True**, the [**Speak**](speak-method.md) method produces audio output if a compatible TTS engine is installed or you use sound files for spoken output.</span></span> <span data-ttu-id="eb254-119">Quando restituisce **False,** significa che l'output vocale non è installato o è stato disabilitato dall'utente.</span><span class="sxs-lookup"><span data-stu-id="eb254-119">When it returns **False**, it means that speech output is not installed or has been disabled by the user.</span></span> <span data-ttu-id="eb254-120">L'impostazione della proprietà si applica a tutti i caratteri di Agent ed è di sola lettura. solo l'utente può impostare questo valore della proprietà.</span><span class="sxs-lookup"><span data-stu-id="eb254-120">The property setting applies to all Agent characters and is read-only; only the user can set this property value.</span></span>

## <a name="see-also"></a><span data-ttu-id="eb254-121">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="eb254-121">See Also</span></span>

[<span data-ttu-id="eb254-122">Evento AgentPropertyChange</span><span class="sxs-lookup"><span data-stu-id="eb254-122">AgentPropertyChange Event</span></span>](agentpropertychange-event.md)


 

 




