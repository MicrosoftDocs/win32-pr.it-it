---
title: Proprietà AutoPopupMenu
description: Proprietà AutoPopupMenu
ms.assetid: 499092cb-0990-4edb-915c-12e3011de142
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25d4ebfc559c88c3750a338f30b5dee4aad66ec3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331532"
---
# <a name="autopopupmenu-property"></a><span data-ttu-id="6a57e-103">Proprietà AutoPopupMenu</span><span class="sxs-lookup"><span data-stu-id="6a57e-103">AutoPopupMenu Property</span></span>

<span data-ttu-id="6a57e-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="6a57e-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="6a57e-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="6a57e-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="6a57e-106">Restituisce o imposta un valore che indica se facendo clic con il pulsante destro del mouse sul carattere o sull'icona della barra delle applicazioni viene visualizzato automaticamente il menu popup del carattere</span><span class="sxs-lookup"><span data-stu-id="6a57e-106">Returns or sets whether right-clicking the character or its taskbar icon automatically displays the character's pop-up menu.</span></span>

</dd> <dt>

<span data-ttu-id="6a57e-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="6a57e-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="6a57e-108">\*agente. ***Caratteri \* \* \* \* ("*** CharacterID \* \* *"). AutoPopupMenu*( \*  \[  =  *booleano* )\]</span><span class="sxs-lookup"><span data-stu-id="6a57e-108">*agent.\*\*\*Characters\*\*\*\*("*\*\* CharacterID\***").AutoPopupMenu** \[ = *boolean*\]</span></span>



| <span data-ttu-id="6a57e-109">Parte</span><span class="sxs-lookup"><span data-stu-id="6a57e-109">Part</span></span>      | <span data-ttu-id="6a57e-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6a57e-110">Description</span></span>                                                                                                                                                                                                                                           |
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a57e-111">*boolean*</span><span class="sxs-lookup"><span data-stu-id="6a57e-111">*boolean*</span></span> | <span data-ttu-id="6a57e-112">Espressione booleana che specifica se il server Visualizza automaticamente il menu di scelta rapida del carattere facendo clic con il pulsante destro del mouse.</span><span class="sxs-lookup"><span data-stu-id="6a57e-112">A Boolean expression specifying whether the server automatically displays the character's pop-up menu on right-click.</span></span> <span data-ttu-id="6a57e-113">**True** (impostazione predefinita) consente di visualizzare il menu facendo clic con il pulsante destro del mouse.</span><span class="sxs-lookup"><span data-stu-id="6a57e-113">**True** (Default) Displays the menu on right-click.</span></span> <br/> <span data-ttu-id="6a57e-114">**False** Il menu non viene visualizzato facendo clic con il pulsante destro del mouse.</span><span class="sxs-lookup"><span data-stu-id="6a57e-114">**False** Does not display the menu on right-click.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6a57e-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="6a57e-115">Remarks</span></span>

<span data-ttu-id="6a57e-116">Impostando questa proprietà su **false**, è possibile creare un comportamento personalizzato per la gestione dei menu.</span><span class="sxs-lookup"><span data-stu-id="6a57e-116">By setting this property to **False**, you can create your own menu-handling behavior.</span></span> <span data-ttu-id="6a57e-117">Per visualizzare il menu dopo l'impostazione di questa proprietà su **false**, utilizzare il metodo [**ShowPopupMenu**](showpopupmenu-method.md) .</span><span class="sxs-lookup"><span data-stu-id="6a57e-117">To display the menu after setting this property to **False**, use the [**ShowPopupMenu**](showpopupmenu-method.md) method.</span></span>

<span data-ttu-id="6a57e-118">Questa proprietà si applica solo all'utilizzo del carattere da parte dell'applicazione client. l'impostazione non influisce sugli altri client del carattere o di altri caratteri dell'applicazione client.</span><span class="sxs-lookup"><span data-stu-id="6a57e-118">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

## <a name="see-also"></a><span data-ttu-id="6a57e-119">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="6a57e-119">See Also</span></span>

[<span data-ttu-id="6a57e-120">**Metodo ShowPopupMenu**</span><span class="sxs-lookup"><span data-stu-id="6a57e-120">**ShowPopupMenu method**</span></span>](showpopupmenu-method.md)


 

 





