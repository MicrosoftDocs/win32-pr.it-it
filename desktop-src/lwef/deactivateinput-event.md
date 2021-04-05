---
title: Evento DeactivateInput
description: Evento DeactivateInput
ms.assetid: 59747932-82be-45d5-8465-73798904e8a7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b2fe1ff13b599fe5fbcf2dac22e548a0432f415
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955592"
---
# <a name="deactivateinput-event"></a><span data-ttu-id="87b41-103">Evento DeactivateInput</span><span class="sxs-lookup"><span data-stu-id="87b41-103">DeactivateInput Event</span></span>

<span data-ttu-id="87b41-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="87b41-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="87b41-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="87b41-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="87b41-106">Si verifica quando un client diventa non attivo in input.</span><span class="sxs-lookup"><span data-stu-id="87b41-106">Occurs when a client becomes non-input-active.</span></span>

</dd> <dt>

<span data-ttu-id="87b41-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="87b41-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="87b41-108">Agente **secondario** \*\* \* \* \_ DeactivateInput\* \*  **(ByVal** *CharacterID \* \* *)**</span><span class="sxs-lookup"><span data-stu-id="87b41-108">**Sub** *agent\*\*\*\_DeactivateInput*\* **(ByVal** *CharacterID\*\*\*)*\*</span></span>



| <span data-ttu-id="87b41-109">Parte</span><span class="sxs-lookup"><span data-stu-id="87b41-109">Part</span></span>          | <span data-ttu-id="87b41-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="87b41-110">Description</span></span>                                                                    |
|---------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="87b41-111">*CharacterID*</span><span class="sxs-lookup"><span data-stu-id="87b41-111">*CharacterID*</span></span> | <span data-ttu-id="87b41-112">Restituisce l'ID del carattere che rende il client non attivo.</span><span class="sxs-lookup"><span data-stu-id="87b41-112">Returns the ID of the character that makes the client become non-input-active.</span></span> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="87b41-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="87b41-113">Remarks</span></span>

<span data-ttu-id="87b41-114">Un client non input-attivo non riceve più gli eventi del mouse o della voce dal server, a meno che non diventi di nuovo input-Active.</span><span class="sxs-lookup"><span data-stu-id="87b41-114">A non-input-active client no longer receives mouse or speech events from the server (unless it becomes input-active again).</span></span> <span data-ttu-id="87b41-115">Il server invia questo evento solo al client che diventa non attivo.</span><span class="sxs-lookup"><span data-stu-id="87b41-115">The server sends this event only to the client that becomes non-input-active.</span></span>

<span data-ttu-id="87b41-116">Questo evento si verifica quando l'applicazione client è di input-attivo e l'utente sceglie la didascalia di un altro client nel menu di scelta rapida di un carattere o nella finestra comandi vocali oppure si chiama il metodo [**Activate**](activate-method.md) e si imposta il parametro **state** su 0.</span><span class="sxs-lookup"><span data-stu-id="87b41-116">This event occurs when your client application is input-active and the user chooses the caption of another client in a character's pop-up menu or the Voice Commands Window or you call the [**Activate**](activate-method.md) method and set the **State** parameter to 0.</span></span> <span data-ttu-id="87b41-117">Può inoltre verificarsi quando l'utente seleziona il nome di un altro carattere facendo clic o parlando.</span><span class="sxs-lookup"><span data-stu-id="87b41-117">It may also occur when the user selects the name of another character by clicking or speaking.</span></span> <span data-ttu-id="87b41-118">Questo evento viene visualizzato anche quando il carattere è nascosto o un altro carattere diventa visibile.</span><span class="sxs-lookup"><span data-stu-id="87b41-118">You also get this event when your character is hidden or another character becomes visible.</span></span>

### <a name="see-also"></a><span data-ttu-id="87b41-119">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="87b41-119">See Also</span></span>

[<span data-ttu-id="87b41-120">**Evento ActivateInput**</span><span class="sxs-lookup"><span data-stu-id="87b41-120">**ActivateInput event**</span></span>](activateinput-event.md)


 

 




