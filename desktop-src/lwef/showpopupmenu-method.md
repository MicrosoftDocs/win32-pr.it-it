---
title: Metodo ShowPopupMenu
description: Metodo ShowPopupMenu
ms.assetid: 7f964d53-2594-41b1-9450-1ba7e9f85882
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0325a552cc3c1f91a64c1240964f1d0c329292c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297847"
---
# <a name="showpopupmenu-method"></a><span data-ttu-id="0c9ff-103">Metodo ShowPopupMenu</span><span class="sxs-lookup"><span data-stu-id="0c9ff-103">ShowPopupMenu Method</span></span>

<span data-ttu-id="0c9ff-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="0c9ff-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="0c9ff-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="0c9ff-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="0c9ff-106">Consente di visualizzare il menu di scelta rapida del carattere nella posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="0c9ff-106">Displays the character's pop-up menu at the specified location.</span></span>

</dd> <dt>

<span data-ttu-id="0c9ff-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="0c9ff-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="0c9ff-108">*agente. ***Caratteri ("*** CharacterID ***"). ShowPopupMenu*** x, y*</span><span class="sxs-lookup"><span data-stu-id="0c9ff-108">*agent.\*\*\*Characters("*\*\* CharacterID ***").ShowPopupMenu*** x, y\*</span></span>



| <span data-ttu-id="0c9ff-109">Parte</span><span class="sxs-lookup"><span data-stu-id="0c9ff-109">Part</span></span> | <span data-ttu-id="0c9ff-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0c9ff-110">Description</span></span>                                                                                                                                          |
|------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c9ff-111">*x*</span><span class="sxs-lookup"><span data-stu-id="0c9ff-111">*x*</span></span>  | <span data-ttu-id="0c9ff-112">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="0c9ff-112">Required.</span></span> <span data-ttu-id="0c9ff-113">Valore intero che indica la coordinata orizzontale (*x*) dello schermo per visualizzare il menu.</span><span class="sxs-lookup"><span data-stu-id="0c9ff-113">An integer value that indicates the horizontal (*x*) screen coordinate to display the menu.</span></span> <span data-ttu-id="0c9ff-114">È necessario specificare queste coordinate in pixel.</span><span class="sxs-lookup"><span data-stu-id="0c9ff-114">These coordinates must be specified in pixels.</span></span> |
| <span data-ttu-id="0c9ff-115">*y*</span><span class="sxs-lookup"><span data-stu-id="0c9ff-115">*y*</span></span>  | <span data-ttu-id="0c9ff-116">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="0c9ff-116">Required.</span></span> <span data-ttu-id="0c9ff-117">Valore intero che indica la coordinata verticale (*y*) dello schermo per visualizzare il menu.</span><span class="sxs-lookup"><span data-stu-id="0c9ff-117">An integer value that indicates the vertical (*y*) screen coordinate to display the menu.</span></span> <span data-ttu-id="0c9ff-118">È necessario specificare queste coordinate in pixel.</span><span class="sxs-lookup"><span data-stu-id="0c9ff-118">These coordinates must be specified in pixels.</span></span>   |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0c9ff-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="0c9ff-119">Remarks</span></span>

<span data-ttu-id="0c9ff-120">Agent Visualizza automaticamente il menu di scelta rapida del carattere quando l'utente fa clic con il pulsante destro del mouse sul carattere.</span><span class="sxs-lookup"><span data-stu-id="0c9ff-120">Agent automatically displays the character's pop-up menu when the user right-clicks the character.</span></span> <span data-ttu-id="0c9ff-121">Se si imposta [**AutoPopupMenu**](autopopupmenu-property.md) su **false**, è possibile usare questo metodo per visualizzare il menu.</span><span class="sxs-lookup"><span data-stu-id="0c9ff-121">If you set [**AutoPopupMenu**](autopopupmenu-property.md) to **False**, you can use this method to display the menu.</span></span>

<span data-ttu-id="0c9ff-122">Il menu rimane visualizzato fino a quando l'utente non seleziona un comando o Visualizza un altro menu.</span><span class="sxs-lookup"><span data-stu-id="0c9ff-122">The menu remains displayed until the user selects a command or displays another menu.</span></span> <span data-ttu-id="0c9ff-123">È possibile visualizzare un solo menu popup alla volta; Pertanto, le chiamate a questo metodo cancelleranno (rimuovere) il menu precedente.</span><span class="sxs-lookup"><span data-stu-id="0c9ff-123">Only one pop-up menu can be displayed at a time; therefore, calls to this method will cancel (remove) the former menu.</span></span>

<span data-ttu-id="0c9ff-124">Questo metodo deve essere chiamato solo quando l'applicazione client è il client attivo del carattere; in caso contrario, avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="0c9ff-124">This method should be called only when your client application is the active client of the character; otherwise it fails.</span></span> <span data-ttu-id="0c9ff-125">Per determinare l'esito positivo di questo metodo, è possibile chiamarlo come funzione e restituirà un valore booleano che indica se il metodo ha avuto esito positivo.</span><span class="sxs-lookup"><span data-stu-id="0c9ff-125">To determine the success of this method you can call it as a function and it will return a Boolean value indicating whether the method succeeded.</span></span>


```
   If Genie.ShowPopupMenu (10,10) = True Then
      ' The menu will be displayed

   Else 
      ' The menu will not be displayed

   End If
```



## <a name="see-also"></a><span data-ttu-id="0c9ff-126">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="0c9ff-126">See Also</span></span>

[<span data-ttu-id="0c9ff-127">**Proprietà AutoPopupMenu**</span><span class="sxs-lookup"><span data-stu-id="0c9ff-127">**AutoPopupMenu property**</span></span>](autopopupmenu-property.md)


 

 




