---
title: Error. clearErrorQueue, metodo
description: Il metodo clearErrorQueue Cancella gli errori dalla coda degli errori. | Error. clearErrorQueue, metodo
ms.assetid: 306f0700-88b1-4433-8abb-7d225e82060a
keywords:
- Metodo clearErrorQueue Windows Media Player
- Metodo clearErrorQueue Windows Media Player, classe Error
- Classe Error Media Player Windows, metodo clearErrorQueue
topic_type:
- apiref
api_name:
- Error.clearErrorQueue
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b756708b8f0643f86489c26dd921e87c408be8f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327293"
---
# <a name="errorclearerrorqueue-method"></a><span data-ttu-id="2fcec-107">Error. clearErrorQueue, metodo</span><span class="sxs-lookup"><span data-stu-id="2fcec-107">Error.clearErrorQueue method</span></span>

<span data-ttu-id="2fcec-108">Il metodo **clearErrorQueue** Cancella gli errori dalla coda degli errori.</span><span class="sxs-lookup"><span data-stu-id="2fcec-108">The **clearErrorQueue** method clears the errors from the error queue.</span></span>

## <a name="syntax"></a><span data-ttu-id="2fcec-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2fcec-109">Syntax</span></span>


```JScript
Error.clearErrorQueue()
```



## <a name="parameters"></a><span data-ttu-id="2fcec-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="2fcec-110">Parameters</span></span>

<span data-ttu-id="2fcec-111">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="2fcec-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2fcec-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2fcec-112">Return value</span></span>

<span data-ttu-id="2fcec-113">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="2fcec-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2fcec-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="2fcec-114">Remarks</span></span>

<span data-ttu-id="2fcec-115">Questo metodo è utile per cancellare la coda degli errori dopo l'elaborazione di una serie di errori.</span><span class="sxs-lookup"><span data-stu-id="2fcec-115">This method is useful to clear the error queue after a series of errors has been processed.</span></span>

<span data-ttu-id="2fcec-116">È necessario impostare *le impostazioni*. **enableErrorDialogs** su false se si sceglie di visualizzare i messaggi di errore personalizzati.</span><span class="sxs-lookup"><span data-stu-id="2fcec-116">You should set *Settings*.**enableErrorDialogs** to false if you choose to display custom error messages.</span></span>

## <a name="examples"></a><span data-ttu-id="2fcec-117">Esempio</span><span class="sxs-lookup"><span data-stu-id="2fcec-117">Examples</span></span>

<span data-ttu-id="2fcec-118">Nell'esempio JScript seguente viene utilizzato *Error*. **clearErrorQueue** in un gestore eventi per svuotare la coda degli errori dopo la visualizzazione di tutte le descrizioni degli errori.</span><span class="sxs-lookup"><span data-stu-id="2fcec-118">The following JScript example uses *Error*.**clearErrorQueue** in an event handler to empty the error queue after all error descriptions are displayed.</span></span> <span data-ttu-id="2fcec-119">L'oggetto **Player** è stato creato con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="2fcec-119">The **Player** object was created with ID = "Player".</span></span>


```JScript
<SCRIPT LANGUAGE = "JScript"  FOR = Player  EVENT = error()>

// Store the number of errors in the queue.
var max = Player.error.errorCount 

// Loop through the list of errors.
for (var i = 0; i < max; i++){
    // Get the error description for this item.
    var errDesc = Player.error.item(i).errorDescription;
    
    // Display the error message.
    alert(errDesc);
}

// Clear the error queue to prepare for the next group of errors.
Player.error.clearErrorQueue();

</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="2fcec-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2fcec-120">Requirements</span></span>



| <span data-ttu-id="2fcec-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="2fcec-121">Requirement</span></span> | <span data-ttu-id="2fcec-122">Valore</span><span class="sxs-lookup"><span data-stu-id="2fcec-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2fcec-123">Versione</span><span class="sxs-lookup"><span data-stu-id="2fcec-123">Version</span></span><br/> | <span data-ttu-id="2fcec-124">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="2fcec-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="2fcec-125">DLL</span><span class="sxs-lookup"><span data-stu-id="2fcec-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="2fcec-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2fcec-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2fcec-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2fcec-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2fcec-128">**Oggetto Error**</span><span class="sxs-lookup"><span data-stu-id="2fcec-128">**Error Object**</span></span>](error-object.md)
</dt> </dl>

 

 





