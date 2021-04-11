---
title: Proprietà Enabled (oggetto AudioOutput)
description: Proprietà Enabled
ms.assetid: 6526f249-be13-4732-b79e-a9952489461f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5dff9153a1aa7a6bf5346d46f43f80bf48809c9
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104047762"
---
# <a name="enabled-property-audiooutput-object"></a><span data-ttu-id="6b8d6-103">Proprietà Enabled (oggetto AudioOutput)</span><span class="sxs-lookup"><span data-stu-id="6b8d6-103">Enabled Property (AudioOutput Object)</span></span>

<span data-ttu-id="6b8d6-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="6b8d6-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="6b8d6-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="6b8d6-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="6b8d6-106">Restituisce un valore booleano che indica se l'output audio (parlato) è abilitato.</span><span class="sxs-lookup"><span data-stu-id="6b8d6-106">Returns a Boolean indicating whether audio (spoken) output is enabled.</span></span>

</dd> <dt>

<span data-ttu-id="6b8d6-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="6b8d6-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="6b8d6-108">*agente \* \* *. AudioOutput. Enabled**</span><span class="sxs-lookup"><span data-stu-id="6b8d6-108">*agent\*\*\*.AudioOutput.Enabled*\*</span></span>



| <span data-ttu-id="6b8d6-109">Valore</span><span class="sxs-lookup"><span data-stu-id="6b8d6-109">Value</span></span>     | <span data-ttu-id="6b8d6-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6b8d6-110">Description</span></span>                               |
|-----------|-------------------------------------------|
| <span data-ttu-id="6b8d6-111">**True**</span><span class="sxs-lookup"><span data-stu-id="6b8d6-111">**True**</span></span>  | <span data-ttu-id="6b8d6-112">Predefinita L'output audio parlato è abilitato.</span><span class="sxs-lookup"><span data-stu-id="6b8d6-112">(Default) Spoken audio output is enabled.</span></span> |
| <span data-ttu-id="6b8d6-113">**False**</span><span class="sxs-lookup"><span data-stu-id="6b8d6-113">**False**</span></span> | <span data-ttu-id="6b8d6-114">L'output audio parlato è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="6b8d6-114">Spoken audio output is disabled.</span></span>          |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6b8d6-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="6b8d6-115">Remarks</span></span>

<span data-ttu-id="6b8d6-116">Questa proprietà riflette l'opzione Riproduci output audio nella pagina output della finestra delle proprietà dell'agente (Opzioni carattere avanzate).</span><span class="sxs-lookup"><span data-stu-id="6b8d6-116">This property reflects the Play Audio Output option on the Output page of the Agent property sheet (Advanced Character Options).</span></span> <span data-ttu-id="6b8d6-117">Quando la proprietà [**Enabled**](enabled-property.md) restituisce **true**, il metodo [**Speak**](speak-method.md) produce l'output audio se è installato un motore TTS compatibile o si usano file audio per l'output parlato.</span><span class="sxs-lookup"><span data-stu-id="6b8d6-117">When the [**Enabled**](enabled-property.md) property returns **True**, the [**Speak**](speak-method.md) method produces audio output if a compatible TTS engine is installed or you use sound files for spoken output.</span></span> <span data-ttu-id="6b8d6-118">Quando restituisce **false**, significa che l'output vocale non è installato o è stato disabilitato dall'utente.</span><span class="sxs-lookup"><span data-stu-id="6b8d6-118">When it returns **False**, it means that speech output is not installed or has been disabled by the user.</span></span> <span data-ttu-id="6b8d6-119">L'impostazione della proprietà si applica a tutti i caratteri degli agenti ed è di sola lettura. il valore della proprietà può essere impostato solo dall'utente.</span><span class="sxs-lookup"><span data-stu-id="6b8d6-119">The property setting applies to all Agent characters and is read-only; only the user can set this property value.</span></span>

## <a name="see-also"></a><span data-ttu-id="6b8d6-120">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="6b8d6-120">See Also</span></span>

[<span data-ttu-id="6b8d6-121">Evento AgentPropertyChange</span><span class="sxs-lookup"><span data-stu-id="6b8d6-121">AgentPropertyChange Event</span></span>](agentpropertychange-event.md)


 

 




