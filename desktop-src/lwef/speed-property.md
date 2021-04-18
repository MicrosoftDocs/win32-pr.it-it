---
title: Proprietà Speed
description: Proprietà Speed
ms.assetid: 43d0480b-d3a5-4992-a2a5-80eba37221e4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24738ac17d7efac45f2aefe7e4beb5ec018915a0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298061"
---
# <a name="speed-property"></a><span data-ttu-id="9a24f-103">Proprietà Speed</span><span class="sxs-lookup"><span data-stu-id="9a24f-103">Speed Property</span></span>

<span data-ttu-id="9a24f-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="9a24f-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="9a24f-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="9a24f-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="9a24f-106">Restituisce un valore long integer che specifica la velocità corrente dell'output vocale del carattere.</span><span class="sxs-lookup"><span data-stu-id="9a24f-106">Returns a Long integer that specifies the current speed of the character's speech output.</span></span>

</dd> <dt>

<span data-ttu-id="9a24f-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="9a24f-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="9a24f-108">*agente ***. Caratteri ("*** CharacterID \* \* *"). Velocità**</span><span class="sxs-lookup"><span data-stu-id="9a24f-108">*agent ***.Characters ("*** CharacterID\*\*\*").Speed*\*</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9a24f-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="9a24f-109">Remarks</span></span>

<span data-ttu-id="9a24f-110">Questa proprietà restituisce l'impostazione della velocità di output in lettura corrente per il carattere.</span><span class="sxs-lookup"><span data-stu-id="9a24f-110">This property returns the current speaking output speed setting for the character.</span></span> <span data-ttu-id="9a24f-111">Per i caratteri che usano l'output TTS, la proprietà restituisce l'impostazione di output TTS effettivo per il carattere.</span><span class="sxs-lookup"><span data-stu-id="9a24f-111">For characters using TTS output, the property returns the actual TTS output setting for the character.</span></span> <span data-ttu-id="9a24f-112">Se TTS non è abilitato o il carattere non supporta l'output TTS, l'impostazione riflette l'impostazione utente per la velocità di output.</span><span class="sxs-lookup"><span data-stu-id="9a24f-112">If TTS is not enabled or the character does not support TTS output, the setting reflects the user setting for output speed.</span></span>

<span data-ttu-id="9a24f-113">Anche se l'applicazione non è in grado di scrivere questo valore, è possibile includere tag **SPD** (Speed) nel testo di output che accelererà temporaneamente l'output per una determinata espressione.</span><span class="sxs-lookup"><span data-stu-id="9a24f-113">Although your application cannot write this value, you can include **Spd** (speed) tags in your output text that will temporarily speed up the output for a particular utterance.</span></span> <span data-ttu-id="9a24f-114">Tuttavia, l'uso del tag **SPD** per modificare l'output parlato del carattere non influisce sull'impostazione della proprietà **Speed** .</span><span class="sxs-lookup"><span data-stu-id="9a24f-114">However, using the **Spd** tag to change the character's spoken output does not affect the **Speed** property setting.</span></span> <span data-ttu-id="9a24f-115">Per altre informazioni, vedere [tag di output vocale](microsoft-agent-speech-output-tags.md).</span><span class="sxs-lookup"><span data-stu-id="9a24f-115">For further information, see [Speech Output Tags](microsoft-agent-speech-output-tags.md).</span></span>

 

 




