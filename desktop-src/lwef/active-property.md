---
title: Proprietà attiva
description: Proprietà attiva
ms.assetid: 76ada073-782a-4355-b4e8-42dd84d0139b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 061fe5fea7d94586c9f9d5c12b3a3b11ffbd7c3f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221424"
---
# <a name="active-property"></a><span data-ttu-id="3c7ba-103">Proprietà attiva</span><span class="sxs-lookup"><span data-stu-id="3c7ba-103">Active Property</span></span>

<span data-ttu-id="3c7ba-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="3c7ba-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="3c7ba-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="3c7ba-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="3c7ba-106">Restituisce un valore che indica se l'applicazione è il client attivo del carattere e se il carattere è in primo piano.</span><span class="sxs-lookup"><span data-stu-id="3c7ba-106">Returns whether your application is the active client of the character and whether the character is topmost.</span></span>

</dd> <dt>

<span data-ttu-id="3c7ba-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="3c7ba-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="3c7ba-108">\*agente. ***Caratteri \* \* \* \* ("*** CharacterID \* \* *").* \*  \[  =  *Stato* attivo\]</span><span class="sxs-lookup"><span data-stu-id="3c7ba-108">*agent.\*\*\*Characters\*\*\*\*("*\*\* CharacterID\***").Active** \[ = *State*\]</span></span>



| <span data-ttu-id="3c7ba-109">Parte</span><span class="sxs-lookup"><span data-stu-id="3c7ba-109">Part</span></span>    | <span data-ttu-id="3c7ba-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3c7ba-110">Description</span></span>                                                                                                                                                                                                |
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c7ba-111">*state*</span><span class="sxs-lookup"><span data-stu-id="3c7ba-111">*state*</span></span> | <span data-ttu-id="3c7ba-112">Espressione Integer che specifica lo stato dell'applicazione client.</span><span class="sxs-lookup"><span data-stu-id="3c7ba-112">An integer expression specifying the state of your client application.</span></span> <span data-ttu-id="3c7ba-113">0 non è il client attivo.</span><span class="sxs-lookup"><span data-stu-id="3c7ba-113">0 Not the active client.</span></span><br/> <span data-ttu-id="3c7ba-114">1 il client attivo.</span><span class="sxs-lookup"><span data-stu-id="3c7ba-114">1 The active client.</span></span> <br/> <span data-ttu-id="3c7ba-115">2 il client attivo di input.</span><span class="sxs-lookup"><span data-stu-id="3c7ba-115">2 The input-active client.</span></span> <span data-ttu-id="3c7ba-116">(Il carattere in primo piano).</span><span class="sxs-lookup"><span data-stu-id="3c7ba-116">(The topmost character.)</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3c7ba-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="3c7ba-117">Remarks</span></span>

<span data-ttu-id="3c7ba-118">Quando più applicazioni client condividono lo stesso carattere, il client attivo del carattere riceve l'input del mouse, ad esempio gli eventi [**Click**](click-event.md) o [DragStart](dragstart-event.md) del controllo Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="3c7ba-118">When multiple client applications share the same character, the active client of the character receives mouse input (for example, Microsoft Agent control [**Click**](click-event.md) or [DragStart](dragstart-event.md) events).</span></span> <span data-ttu-id="3c7ba-119">Analogamente, quando vengono visualizzati più caratteri, il client attivo del carattere superiore (noto anche come client attivo di input) riceve gli eventi di comando.</span><span class="sxs-lookup"><span data-stu-id="3c7ba-119">Similarly, when multiple characters are displayed, the active client of the topmost character (also known as the input-active client) receives Command events.</span></span>

<span data-ttu-id="3c7ba-120">È possibile usare il metodo [**Activate**](activate-method.md)per impostare se l'applicazione è il client attivo del carattere o per rendere l'applicazione il client attivo di input (che rende anche il carattere in primo piano).</span><span class="sxs-lookup"><span data-stu-id="3c7ba-120">You can use the [**Activate**](activate-method.md)method to set whether your application is the active client of the character or to make your application the input active client (which also makes the character topmost).</span></span>

## <a name="see-also"></a><span data-ttu-id="3c7ba-121">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="3c7ba-121">See Also</span></span>

[<span data-ttu-id="3c7ba-122">Attivare il metodo \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="3c7ba-122">\*\*\*\*Activate\*\* method\*\*</span></span>](activate-method.md)


 

 





