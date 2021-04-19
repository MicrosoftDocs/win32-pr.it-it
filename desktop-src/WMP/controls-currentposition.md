---
title: Controls. currentPosition
description: La proprietà currentPosition specifica o recupera la posizione corrente nell'elemento multimediale in secondi dall'inizio.
ms.assetid: 374ad144-3f74-4d1b-bec5-1cd0f03777b7
keywords:
- Media Player di Windows Controls. currentPosition
topic_type:
- apiref
api_name:
- Controls.currentPosition
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12c690c102bb95c1a58785f18d727ffdae2a82c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331762"
---
# <a name="controlscurrentposition"></a><span data-ttu-id="747f7-104">Controls. currentPosition</span><span class="sxs-lookup"><span data-stu-id="747f7-104">Controls.currentPosition</span></span>

<span data-ttu-id="747f7-105">La proprietà **currentPosition** specifica o recupera la posizione corrente nell'elemento multimediale in secondi dall'inizio.</span><span class="sxs-lookup"><span data-stu-id="747f7-105">The **currentPosition** property specifies or retrieves the current position in the media item in seconds from the beginning.</span></span>

``` syntax
player.controls.currentPosition
      
```

## <a name="possible-values"></a><span data-ttu-id="747f7-106">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="747f7-106">Possible Values</span></span>

<span data-ttu-id="747f7-107">Questa proprietà è un **numero** di lettura/scrittura (**Double**).</span><span class="sxs-lookup"><span data-stu-id="747f7-107">This property is a read/write **Number** (**double**).</span></span>

## <a name="examples"></a><span data-ttu-id="747f7-108">Esempio</span><span class="sxs-lookup"><span data-stu-id="747f7-108">Examples</span></span>

<span data-ttu-id="747f7-109">Nell'esempio seguente viene usato **currentPosition** per cercare una posizione fornita dall'utente.</span><span class="sxs-lookup"><span data-stu-id="747f7-109">The following example uses **currentPosition** to seek to a position provided by the user.</span></span> <span data-ttu-id="747f7-110">Viene creato un elemento BUTTON HTML per eseguire il codice JScript.</span><span class="sxs-lookup"><span data-stu-id="747f7-110">An HTML BUTTON element is created to execute the JScript code.</span></span> <span data-ttu-id="747f7-111">È stato creato un elemento input di testo HTML, denominato seposition, per accettare un valore, in secondi, dall'utente.</span><span class="sxs-lookup"><span data-stu-id="747f7-111">An HTML TEXT input element, named setPosition, was created to accept a value, in seconds, from the user.</span></span> <span data-ttu-id="747f7-112">L'oggetto **Player** è stato creato con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="747f7-112">The **Player** object was created with ID = "Player".</span></span>


```JScript
<INPUT TYPE = "BUTTON"  ID = "Set"  NAME = "Set"  VALUE = "Set Position"

    /* Check to be sure the TEXT element contains a valid value. */
    if (!isNaN(setPosition.value) && (setPosition.value != '))

    /* Set the current position when the user clicks the button. */
    onClick = "Player.controls.currentPosition = setPosition.value;
">
```



## <a name="requirements"></a><span data-ttu-id="747f7-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="747f7-113">Requirements</span></span>



| <span data-ttu-id="747f7-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="747f7-114">Requirement</span></span> | <span data-ttu-id="747f7-115">Valore</span><span class="sxs-lookup"><span data-stu-id="747f7-115">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="747f7-116">Versione</span><span class="sxs-lookup"><span data-stu-id="747f7-116">Version</span></span><br/> | <span data-ttu-id="747f7-117">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="747f7-117">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="747f7-118">DLL</span><span class="sxs-lookup"><span data-stu-id="747f7-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="747f7-119"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="747f7-119"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="747f7-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="747f7-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="747f7-121">**Oggetto Controls**</span><span class="sxs-lookup"><span data-stu-id="747f7-121">**Controls Object**</span></span>](controls-object.md)
</dt> </dl>

 

 





