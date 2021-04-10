---
title: Evento dimensioni
description: Evento dimensioni
ms.assetid: 06089f84-8e75-475f-a492-536c83fa6730
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d9a896d2dcbf8b925c0ca13fa429f6dfd95bc21
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855982"
---
# <a name="size-event"></a><span data-ttu-id="ac04e-103">Evento dimensioni</span><span class="sxs-lookup"><span data-stu-id="ac04e-103">Size Event</span></span>

<span data-ttu-id="ac04e-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="ac04e-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="ac04e-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="ac04e-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="ac04e-106">Si verifica quando le dimensioni di un carattere cambiano.</span><span class="sxs-lookup"><span data-stu-id="ac04e-106">Occurs when a character's size changes.</span></span>

</dd> <dt>

<span data-ttu-id="ac04e-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="ac04e-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="ac04e-108">Dimensioni agente **secondario**  \_ **(ByVal** *CharacterID*, **ByVal** *Width*, **ByVal** *Height*)</span><span class="sxs-lookup"><span data-stu-id="ac04e-108">**Sub** *agent*\_**Size (ByVal** *CharacterID*, **ByVal** *Width*, **ByVal** *Height*)</span></span>



| <span data-ttu-id="ac04e-109">Parte</span><span class="sxs-lookup"><span data-stu-id="ac04e-109">Part</span></span>          | <span data-ttu-id="ac04e-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ac04e-110">Description</span></span>                                                         |
|---------------|---------------------------------------------------------------------|
| <span data-ttu-id="ac04e-111">*CharacterID*</span><span class="sxs-lookup"><span data-stu-id="ac04e-111">*CharacterID*</span></span> | <span data-ttu-id="ac04e-112">Restituisce l'ID del carattere spostato.</span><span class="sxs-lookup"><span data-stu-id="ac04e-112">Returns the ID of the character that moved.</span></span>                         |
| <span data-ttu-id="ac04e-113">*Larghezza*</span><span class="sxs-lookup"><span data-stu-id="ac04e-113">*Width*</span></span>       | <span data-ttu-id="ac04e-114">Restituisce la nuova larghezza (in pixel) del fotogramma carattere come numero intero.</span><span class="sxs-lookup"><span data-stu-id="ac04e-114">Returns the character frame's new width (in pixels) as an integer.</span></span>  |
| <span data-ttu-id="ac04e-115">*Altezza*</span><span class="sxs-lookup"><span data-stu-id="ac04e-115">*Height*</span></span>      | <span data-ttu-id="ac04e-116">Restituisce la nuova altezza (in pixel) del fotogramma di caratteri come valore integer.</span><span class="sxs-lookup"><span data-stu-id="ac04e-116">Returns the character frame's new height (in pixels) as an integer.</span></span> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="ac04e-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="ac04e-117">Remarks</span></span>

<span data-ttu-id="ac04e-118">Questo evento si verifica quando un'applicazione modifica la dimensione di un carattere.</span><span class="sxs-lookup"><span data-stu-id="ac04e-118">This event occurs when an application changes the size of a character.</span></span> <span data-ttu-id="ac04e-119">Questo evento viene inviato solo ai client del carattere, ovvero le applicazioni che hanno caricato il carattere.</span><span class="sxs-lookup"><span data-stu-id="ac04e-119">This event is sent only to the clients of the character (applications that have loaded the character).</span></span>

### <a name="see-also"></a><span data-ttu-id="ac04e-120">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="ac04e-120">See Also</span></span>

[<span data-ttu-id="ac04e-121">**Sposta evento**</span><span class="sxs-lookup"><span data-stu-id="ac04e-121">**Move event**</span></span>](move-event.md)


 

 




