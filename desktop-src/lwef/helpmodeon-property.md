---
title: Proprietà HelpModeOn
description: Proprietà HelpModeOn
ms.assetid: 4a9b5fd3-12e2-489b-8ce0-9b66b01f517a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43662469c6461e92186a92daddb505b851f8740a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710924"
---
# <a name="helpmodeon-property"></a><span data-ttu-id="6a095-103">Proprietà HelpModeOn</span><span class="sxs-lookup"><span data-stu-id="6a095-103">HelpModeOn Property</span></span>

<span data-ttu-id="6a095-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="6a095-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="6a095-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="6a095-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="6a095-106">Restituisce o imposta un valore che indica se la modalità della Guida sensibile al contesto è impostata su on per il carattere.</span><span class="sxs-lookup"><span data-stu-id="6a095-106">Returns or sets whether context-sensitive Help mode is on for the character.</span></span>

</dd> <dt>

<span data-ttu-id="6a095-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="6a095-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="6a095-108">\*agente. ***Caratteri ("*** CharacterID \* \* *"). HelpModeOn*( \*  \[  =  *booleano* )\]</span><span class="sxs-lookup"><span data-stu-id="6a095-108">*agent.\*\*\*Characters("*\*\* CharacterID\***").HelpModeOn** \[ = *boolean*\]</span></span>



| <span data-ttu-id="6a095-109">Parte</span><span class="sxs-lookup"><span data-stu-id="6a095-109">Part</span></span>      | <span data-ttu-id="6a095-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6a095-110">Description</span></span>                                                                                                                                                       |
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a095-111">*boolean*</span><span class="sxs-lookup"><span data-stu-id="6a095-111">*boolean*</span></span> | <span data-ttu-id="6a095-112">Espressione booleana che specifica se la modalità della Guida sensibile al contesto è on.</span><span class="sxs-lookup"><span data-stu-id="6a095-112">A Boolean expression specifying whether context-sensitive Help mode is on.</span></span> <span data-ttu-id="6a095-113">Valore **true** La modalità della guida è on.</span><span class="sxs-lookup"><span data-stu-id="6a095-113">**True** Help mode is on.</span></span> <br/> <span data-ttu-id="6a095-114">**False** (impostazione predefinita) la modalità della guida è disattivata.</span><span class="sxs-lookup"><span data-stu-id="6a095-114">**False** (Default) Help mode is off.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6a095-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="6a095-115">Remarks</span></span>

<span data-ttu-id="6a095-116">Quando si imposta questa proprietà su **true**, il puntatore del mouse assume la forma dell'immagine della Guida sensibile al contesto quando viene spostato sul carattere o sul menu di scelta rapida per il carattere.</span><span class="sxs-lookup"><span data-stu-id="6a095-116">When you set this property to **True**, the mouse pointer changes to the context-sensitive Help image when moved over the character or over the pop-up menu for the character.</span></span> <span data-ttu-id="6a095-117">Quando l'utente fa clic o trascina il carattere o fa clic su un elemento nel menu popup del carattere, il server attiva l'evento [**HelpComplete**](helpcomplete-event.md) e chiude la modalità della guida.</span><span class="sxs-lookup"><span data-stu-id="6a095-117">When the user clicks or drags the character or clicks an item in the character's pop-up menu, the server triggers the [**HelpComplete**](helpcomplete-event.md) event and exits Help mode.</span></span>

<span data-ttu-id="6a095-118">In modalità guida, il server non invia gli eventi [**Click**](click-event.md), [**DragStart**](dragstart-event.md), [**DragComplete**](dragcomplete-event.md)e [**Command**](command-event.md) , a meno che non si imposti la proprietà [**AutoPopupMenu**](autopopupmenu-property.md) su **true**.</span><span class="sxs-lookup"><span data-stu-id="6a095-118">In Help mode, the server does not send the [**Click**](click-event.md), [**DragStart**](dragstart-event.md), [**DragComplete**](dragcomplete-event.md), and [**Command**](command-event.md) events, unless you set the [**AutoPopupMenu**](autopopupmenu-property.md) property to **True**.</span></span> <span data-ttu-id="6a095-119">In tal caso, il server invierà l'evento **Click** (non esce dalla modalità guida), ma solo per il pulsante destro del mouse per consentire la visualizzazione del menu a comparsa.</span><span class="sxs-lookup"><span data-stu-id="6a095-119">In that case, the server will send the **Click** event (does not exit Help mode), but only for the right mouse button to enable you to display the pop-up menu.</span></span>

<span data-ttu-id="6a095-120">Questa proprietà si applica solo all'utilizzo del carattere da parte dell'applicazione client. l'impostazione non influisce sugli altri client del carattere o di altri caratteri dell'applicazione client.</span><span class="sxs-lookup"><span data-stu-id="6a095-120">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

## <a name="see-also"></a><span data-ttu-id="6a095-121">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="6a095-121">See Also</span></span>

[<span data-ttu-id="6a095-122">**Evento HelpComplete**</span><span class="sxs-lookup"><span data-stu-id="6a095-122">**HelpComplete event**</span></span>](helpcomplete-event.md)


 

 





