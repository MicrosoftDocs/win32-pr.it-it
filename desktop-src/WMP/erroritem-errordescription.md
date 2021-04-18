---
title: ErrorItem. errorDescription
description: La proprietà errorDescription recupera una descrizione dell'errore.
ms.assetid: 7fd16c3d-1460-41b5-81ca-2636d7a1d0d1
keywords:
- Media Player Windows ErrorItem. errorDescription
topic_type:
- apiref
api_name:
- ErrorItem.errorDescription
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0de19bb67a5846a82e87d091f95a18cd12c5c2b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324740"
---
# <a name="erroritemerrordescription"></a><span data-ttu-id="ff321-104">ErrorItem. errorDescription</span><span class="sxs-lookup"><span data-stu-id="ff321-104">ErrorItem.errorDescription</span></span>

<span data-ttu-id="ff321-105">La proprietà **errorDescription** recupera una descrizione dell'errore.</span><span class="sxs-lookup"><span data-stu-id="ff321-105">The **errorDescription** property retrieves a description of the error.</span></span>

``` syntax
player.error.item(
        index
        ).errorDescription
```

## <a name="possible-values"></a><span data-ttu-id="ff321-106">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="ff321-106">Possible Values</span></span>

<span data-ttu-id="ff321-107">Questa proprietà è una **stringa** di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="ff321-107">This property is a read-only **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="ff321-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="ff321-108">Remarks</span></span>

<span data-ttu-id="ff321-109">È necessario impostare *le impostazioni*. **enableErrorDialogs** su false se si sceglie di visualizzare i messaggi di errore personalizzati.</span><span class="sxs-lookup"><span data-stu-id="ff321-109">You should set *Settings*.**enableErrorDialogs** to false if you choose to display custom error messages.</span></span>

## <a name="examples"></a><span data-ttu-id="ff321-110">Esempio</span><span class="sxs-lookup"><span data-stu-id="ff321-110">Examples</span></span>

<span data-ttu-id="ff321-111">Nell'esempio JScript seguente viene usato *ErrorItem*. **errorDescription** in un gestore eventi per visualizzare il messaggio di errore all'utente.</span><span class="sxs-lookup"><span data-stu-id="ff321-111">The following JScript example uses *ErrorItem*.**errorDescription** in an event handler to display the error message to the user.</span></span> <span data-ttu-id="ff321-112">L'oggetto **Player** è stato creato con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="ff321-112">The **Player** object was created with ID = "Player".</span></span>


```JScript
<SCRIPT LANGUAGE = "JScript"  FOR = Player  EVENT = error()>

// Get the error description for the first error item.
errDesc = Player.error.item(0).errorDescription;

// Display the error code.
var message = "Error: " + errDesc";
message += "<BR>";
message += "Use your BACK button to return ";
message += "to the previous page.";
document.write(message);

</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="ff321-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ff321-113">Requirements</span></span>



| <span data-ttu-id="ff321-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="ff321-114">Requirement</span></span> | <span data-ttu-id="ff321-115">Valore</span><span class="sxs-lookup"><span data-stu-id="ff321-115">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ff321-116">Versione</span><span class="sxs-lookup"><span data-stu-id="ff321-116">Version</span></span><br/> | <span data-ttu-id="ff321-117">Windows Media Player versione 7,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="ff321-117">Windows Media Player version 7.0 or later</span></span><br/>                               |
| <span data-ttu-id="ff321-118">DLL</span><span class="sxs-lookup"><span data-stu-id="ff321-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="ff321-119"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ff321-119"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ff321-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ff321-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff321-121">**Oggetto ErrorItem**</span><span class="sxs-lookup"><span data-stu-id="ff321-121">**ErrorItem Object**</span></span>](erroritem-object.md)
</dt> </dl>

 

 





