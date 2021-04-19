---
title: Evento Player. Error
description: L'evento di errore si verifica in presenza di una condizione di errore.
ms.assetid: 1e418a56-ae81-4ff0-b721-3390be08970d
keywords:
- Media Player di eventi di errore di Windows
- Evento di errore Windows Media Player, classe Player
- Classe Player Windows Media Player, evento Error
topic_type:
- apiref
api_name:
- Player.Error
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a99411773994ad012155eea5a203ed341d50b460
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329301"
---
# <a name="playererror-event"></a><span data-ttu-id="70d90-106">Evento Player. Error</span><span class="sxs-lookup"><span data-stu-id="70d90-106">Player.Error event</span></span>

<span data-ttu-id="70d90-107">L'evento di **errore** si verifica in presenza di una condizione di errore.</span><span class="sxs-lookup"><span data-stu-id="70d90-107">The **Error** event occurs when there is an error condition.</span></span>

## <a name="syntax"></a><span data-ttu-id="70d90-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="70d90-108">Syntax</span></span>


```JScript
Player.Error()
```



## <a name="parameters"></a><span data-ttu-id="70d90-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="70d90-109">Parameters</span></span>

<span data-ttu-id="70d90-110">Questo evento non contiene parametri.</span><span class="sxs-lookup"><span data-stu-id="70d90-110">This event has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="70d90-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="70d90-111">Return value</span></span>

<span data-ttu-id="70d90-112">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="70d90-112">This event does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="70d90-113">Esempio</span><span class="sxs-lookup"><span data-stu-id="70d90-113">Examples</span></span>

<span data-ttu-id="70d90-114">Nell'esempio JScript seguente viene creato un gestore eventi per visualizzare il testo della descrizione per il primo errore nella coda degli errori.</span><span class="sxs-lookup"><span data-stu-id="70d90-114">The following JScript example creates an event handler to display the description text for the first error in the error queue.</span></span> <span data-ttu-id="70d90-115">L'oggetto **Player** è stato creato con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="70d90-115">The **Player** object was created with ID = "Player".</span></span>


```JScript
<SCRIPT LANGUAGE = "JScript"  FOR = Player  EVENT = error()>

// Get the description of the first error. 
var errDesc = Player.error.item(0).errorDescription;

// Display the error description.
alert(errDesc);

</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="70d90-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="70d90-116">Requirements</span></span>



| <span data-ttu-id="70d90-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="70d90-117">Requirement</span></span> | <span data-ttu-id="70d90-118">Valore</span><span class="sxs-lookup"><span data-stu-id="70d90-118">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="70d90-119">Versione</span><span class="sxs-lookup"><span data-stu-id="70d90-119">Version</span></span><br/> | <span data-ttu-id="70d90-120">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="70d90-120">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="70d90-121">DLL</span><span class="sxs-lookup"><span data-stu-id="70d90-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="70d90-122"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="70d90-122"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="70d90-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="70d90-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70d90-124">**ErrorItem. errorDescription**</span><span class="sxs-lookup"><span data-stu-id="70d90-124">**ErrorItem.errorDescription**</span></span>](erroritem-errordescription.md)
</dt> <dt>

[<span data-ttu-id="70d90-125">**Errore. elemento**</span><span class="sxs-lookup"><span data-stu-id="70d90-125">**Error.item**</span></span>](error-item.md)
</dt> <dt>

[<span data-ttu-id="70d90-126">**Oggetto Player**</span><span class="sxs-lookup"><span data-stu-id="70d90-126">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





