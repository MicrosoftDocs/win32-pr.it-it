---
title: Pitch (proprietà)
description: Pitch (proprietà)
ms.assetid: 98b2ada3-93c6-4fa1-bf12-353eb229c30c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 998ee4bcf77878062425086d67066040f5d58421
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396890"
---
# <a name="pitch-property"></a><span data-ttu-id="095f1-103">Pitch (proprietà)</span><span class="sxs-lookup"><span data-stu-id="095f1-103">Pitch Property</span></span>

<span data-ttu-id="095f1-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="095f1-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="095f1-105"><span id="Description_"></span><span id="description_"></span><span id="DESCRIPTION_"></span>**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="095f1-105"><span id="Description_"></span><span id="description_"></span><span id="DESCRIPTION_"></span>**Description**</span></span> 
</dt> <dd>

<span data-ttu-id="095f1-106">Restituisce un valore long integer per l'impostazione del pitch di output vocale del carattere specificato (TTS).</span><span class="sxs-lookup"><span data-stu-id="095f1-106">Returns a Long integer for the specified character's speech output (TTS) pitch setting.</span></span>

</dd> <dt>

<span data-ttu-id="095f1-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="095f1-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="095f1-108">*agente ***. Caratteri ("*** CharacterID \* \* *"). Passo**</span><span class="sxs-lookup"><span data-stu-id="095f1-108">*agent ***.Characters ("*** CharacterID\*\*\*").Pitch*\*</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="095f1-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="095f1-109">Remarks</span></span>

<span data-ttu-id="095f1-110">Questa proprietà si applica solo ai caratteri configurati per l'output TTS.</span><span class="sxs-lookup"><span data-stu-id="095f1-110">This property applies only to characters configured for TTS output.</span></span> <span data-ttu-id="095f1-111">Se il carattere non supporta l'output TTS, questa proprietà restituisce zero (0).</span><span class="sxs-lookup"><span data-stu-id="095f1-111">If the character does not support TTS output, this property returns zero (0).</span></span>

<span data-ttu-id="095f1-112">Anche se l'applicazione non è in grado di scrivere questo valore, è possibile includere tag **Pit** (pitch) nel testo di output che aumenterà temporaneamente il pitch per una determinata espressione.</span><span class="sxs-lookup"><span data-stu-id="095f1-112">Although your application cannot write this value, you can include **Pit** (pitch) tags in your output text that will temporarily increase the pitch for a particular utterance.</span></span> <span data-ttu-id="095f1-113">Tuttavia, se si usa il tag **Pit** per modificare il pitch, l'impostazione della proprietà **pitch** non cambierà.</span><span class="sxs-lookup"><span data-stu-id="095f1-113">However, using the **Pit** tag to change the pitch will not change the **Pitch** property setting.</span></span> <span data-ttu-id="095f1-114">Per altre informazioni, vedere [tag di output vocale](pit-tag.md).</span><span class="sxs-lookup"><span data-stu-id="095f1-114">For further information, see [Speech Output Tags](pit-tag.md).</span></span>

 

 




