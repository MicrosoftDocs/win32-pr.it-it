---
title: Evento AgentPropertyChange
description: Evento AgentPropertyChange
ms.assetid: 56607e9c-99eb-42c1-987a-0f2bc3f82d75
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bd643797e766543877497330a995d492f982d8a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044496"
---
# <a name="agentpropertychange-event"></a><span data-ttu-id="5e00e-103">Evento AgentPropertyChange</span><span class="sxs-lookup"><span data-stu-id="5e00e-103">AgentPropertyChange Event</span></span>

<span data-ttu-id="5e00e-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="5e00e-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="5e00e-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="5e00e-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="5e00e-106">Si verifica quando l'utente modifica una proprietà nella finestra Opzioni carattere avanzate.</span><span class="sxs-lookup"><span data-stu-id="5e00e-106">Occurs when the user changes a property in the Advanced Character Options window.</span></span>

</dd> <dt>

<span data-ttu-id="5e00e-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="5e00e-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="5e00e-108">Agente **secondario** *. \* \* \* AgentPropertyChange*\*</span><span class="sxs-lookup"><span data-stu-id="5e00e-108">**Sub** *agent.\*\*\*AgentPropertyChange*\*</span></span>

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="5e00e-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="5e00e-109">Remarks</span></span>

<span data-ttu-id="5e00e-110">Questo evento indica quando l'utente ha modificato e applicato qualsiasi proprietà inclusa nella finestra delle opzioni dei caratteri avanzati.</span><span class="sxs-lookup"><span data-stu-id="5e00e-110">This event indicates when the user has changed and applied any property included in the Advanced Character Option window.</span></span>

<span data-ttu-id="5e00e-111">Nel codice per la gestione di questo evento, è possibile eseguire una query per le impostazioni specifiche delle proprietà degli oggetti [AudioOutput](the-audiooutput-object.md) o [SpeechInput](the-speechinput-object.md) .</span><span class="sxs-lookup"><span data-stu-id="5e00e-111">In your code for this handling this event, you can query for the specific property settings of [AudioOutput](the-audiooutput-object.md) or [SpeechInput](the-speechinput-object.md) objects.</span></span>

### <a name="see-also"></a><span data-ttu-id="5e00e-112">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="5e00e-112">See Also</span></span>

[<span data-ttu-id="5e00e-113">**Evento DefaultCharacterChange**</span><span class="sxs-lookup"><span data-stu-id="5e00e-113">**DefaultCharacterChange event**</span></span>](defaultcharacterchange-event.md)


 

 




