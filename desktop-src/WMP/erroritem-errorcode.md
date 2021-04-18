---
title: ErrorItem. errorCode
description: La proprietà errorCode Recupera il codice di errore corrente.
ms.assetid: 1495ec34-0995-40c6-bfd0-f3695784e057
keywords:
- Media Player Windows ErrorItem. errorCode
topic_type:
- apiref
api_name:
- ErrorItem.errorCode
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c934b83b28e510f29b84a45b48bde700968c97b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324744"
---
# <a name="erroritemerrorcode"></a><span data-ttu-id="37781-104">ErrorItem. errorCode</span><span class="sxs-lookup"><span data-stu-id="37781-104">ErrorItem.errorCode</span></span>

<span data-ttu-id="37781-105">La proprietà **ErrorCode** Recupera il codice di errore corrente.</span><span class="sxs-lookup"><span data-stu-id="37781-105">The **errorCode** property retrieves the current error code.</span></span>

``` syntax
player.error.item(
        index
        ).errorCode
```

## <a name="possible-values"></a><span data-ttu-id="37781-106">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="37781-106">Possible Values</span></span>

<span data-ttu-id="37781-107">Questa proprietà è un **numero** di sola lettura (**Long**).</span><span class="sxs-lookup"><span data-stu-id="37781-107">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="37781-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="37781-108">Remarks</span></span>

<span data-ttu-id="37781-109">È necessario impostare *le impostazioni*. **enableErrorDialogs** su false se si sceglie di visualizzare i messaggi di errore personalizzati.</span><span class="sxs-lookup"><span data-stu-id="37781-109">You should set *Settings*.**enableErrorDialogs** to false if you choose to display custom error messages.</span></span>

## <a name="examples"></a><span data-ttu-id="37781-110">Esempio</span><span class="sxs-lookup"><span data-stu-id="37781-110">Examples</span></span>

<span data-ttu-id="37781-111">Nell'esempio JScript seguente viene usato *ErrorItem*. **ErrorCode** in un gestore eventi per visualizzare il codice di errore all'utente.</span><span class="sxs-lookup"><span data-stu-id="37781-111">The following JScript example uses *ErrorItem*.**errorCode** in an event handler to display the error code to the user.</span></span> <span data-ttu-id="37781-112">L'oggetto **Player** è stato creato con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="37781-112">The **Player** object was created with ID = "Player".</span></span>


```JScript
<SCRIPT LANGUAGE = "JScript"  FOR = Player  EVENT = error()>

// Get the error code for the first error item.
errNum = Player.error.item(0).errorCode;

// Display the error information.
var message = "Error number: " + errNum);
message += "<BR>";
message += "Use your BACK button to return ";
message += "to the previous page.";
document.write(message);

</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="37781-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="37781-113">Requirements</span></span>



| <span data-ttu-id="37781-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="37781-114">Requirement</span></span> | <span data-ttu-id="37781-115">Valore</span><span class="sxs-lookup"><span data-stu-id="37781-115">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="37781-116">Versione</span><span class="sxs-lookup"><span data-stu-id="37781-116">Version</span></span><br/> | <span data-ttu-id="37781-117">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="37781-117">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="37781-118">DLL</span><span class="sxs-lookup"><span data-stu-id="37781-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="37781-119"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="37781-119"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="37781-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="37781-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37781-121">**Oggetto ErrorItem**</span><span class="sxs-lookup"><span data-stu-id="37781-121">**ErrorItem Object**</span></span>](erroritem-object.md)
</dt> <dt>

[<span data-ttu-id="37781-122">**ErrorItem. errorDescription**</span><span class="sxs-lookup"><span data-stu-id="37781-122">**ErrorItem.errorDescription**</span></span>](erroritem-errordescription.md)
</dt> </dl>

 

 





