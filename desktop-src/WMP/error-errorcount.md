---
title: Errore. errorCount
description: La proprietà errorCount Recupera il numero di errori nella coda degli errori.
ms.assetid: 64d9bb0a-fcc4-401b-a7bd-529e1a517f3b
keywords:
- Errore. errorCount Windows Media Player
topic_type:
- apiref
api_name:
- Error.errorCount
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94848023d2cd331545f97d3bea6d92f2fcd4b49c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324578"
---
# <a name="errorerrorcount"></a><span data-ttu-id="d8983-104">Errore. errorCount</span><span class="sxs-lookup"><span data-stu-id="d8983-104">Error.errorCount</span></span>

<span data-ttu-id="d8983-105">La proprietà **ErrorCount** Recupera il numero di errori nella coda degli errori.</span><span class="sxs-lookup"><span data-stu-id="d8983-105">The **errorCount** property retrieves the number of errors in the error queue.</span></span>

``` syntax
player.error.errorCount
      
```

## <a name="possible-values"></a><span data-ttu-id="d8983-106">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="d8983-106">Possible Values</span></span>

<span data-ttu-id="d8983-107">Questa proprietà è un **numero** di sola lettura (**Long**).</span><span class="sxs-lookup"><span data-stu-id="d8983-107">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="d8983-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="d8983-108">Remarks</span></span>

<span data-ttu-id="d8983-109">È necessario impostare *le impostazioni*. **enableErrorDialogs** su false se si sceglie di visualizzare i messaggi di errore personalizzati.</span><span class="sxs-lookup"><span data-stu-id="d8983-109">You should set *Settings*.**enableErrorDialogs** to false if you choose to display custom error messages.</span></span>

## <a name="examples"></a><span data-ttu-id="d8983-110">Esempio</span><span class="sxs-lookup"><span data-stu-id="d8983-110">Examples</span></span>

<span data-ttu-id="d8983-111">Nell'esempio JScript seguente viene utilizzato *Error*. **ErrorCount** in un gestore eventi per avvertire l'utente dell'errore più recente nella coda degli errori.</span><span class="sxs-lookup"><span data-stu-id="d8983-111">The following JScript example uses *Error*.**errorCount** in an event handler to alert the user about the most recent error in the error queue.</span></span> <span data-ttu-id="d8983-112">L'oggetto **Player** è stato creato con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="d8983-112">The **Player** object was created with ID = "Player".</span></span>


```JScript
<SCRIPT LANGUAGE = "JScript"  FOR = Player  EVENT = error()>

// Store the number of errors in the queue.
var max = Player.error.errorCount;

// Get the description of the last error. Error items start at zero,
// so the item index will always be one less than the error count.
var errDesc = Player.error.item(max-1).errorDescription;

// Display the error description.
alert(errDesc);

</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="d8983-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d8983-113">Requirements</span></span>



| <span data-ttu-id="d8983-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="d8983-114">Requirement</span></span> | <span data-ttu-id="d8983-115">Valore</span><span class="sxs-lookup"><span data-stu-id="d8983-115">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d8983-116">Versione</span><span class="sxs-lookup"><span data-stu-id="d8983-116">Version</span></span><br/> | <span data-ttu-id="d8983-117">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="d8983-117">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="d8983-118">DLL</span><span class="sxs-lookup"><span data-stu-id="d8983-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="d8983-119"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d8983-119"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8983-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d8983-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8983-121">**Oggetto Error**</span><span class="sxs-lookup"><span data-stu-id="d8983-121">**Error Object**</span></span>](error-object.md)
</dt> </dl>

 

 





