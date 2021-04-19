---
title: ClosedCaption.captioningID
description: La proprietà captioningID specifica o Recupera il nome dell'elemento che visualizza la didascalia.
ms.assetid: 99d4aae3-485f-4c86-9130-101b1ca968e9
keywords:
- Media Player Windows ClosedCaption. captioningID
topic_type:
- apiref
api_name:
- ClosedCaption.captioningID
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: faadae626dd5ac0314c4140e3f9d82ab645ef9b2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106323908"
---
# <a name="closedcaptioncaptioningid"></a><span data-ttu-id="1c3de-104">ClosedCaption.captioningID</span><span class="sxs-lookup"><span data-stu-id="1c3de-104">ClosedCaption.captioningID</span></span>

<span data-ttu-id="1c3de-105">La proprietà **captioningID** specifica o Recupera il nome dell'elemento che visualizza la didascalia.</span><span class="sxs-lookup"><span data-stu-id="1c3de-105">The **captioningID** property specifies or retrieves the name of the element displaying the captioning.</span></span>

``` syntax
player.closedCaption.captioningID
```

## <a name="possible-values"></a><span data-ttu-id="1c3de-106">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="1c3de-106">Possible Values</span></span>

<span data-ttu-id="1c3de-107">Questa proprietà è una **stringa** di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="1c3de-107">This property is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="1c3de-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="1c3de-108">Remarks</span></span>

<span data-ttu-id="1c3de-109">Il nome dell'elemento specificato può essere qualsiasi elemento HTML nella pagina Web, purché supporti l'attributo innerHTML.</span><span class="sxs-lookup"><span data-stu-id="1c3de-109">The element name specified can be any HTML element in the webpage as long as it supports the innerHTML attribute.</span></span> <span data-ttu-id="1c3de-110">Se la pagina Web contiene più frame, il nome dell'elemento può fare riferimento solo a un elemento nello stesso frame del controllo lettore.</span><span class="sxs-lookup"><span data-stu-id="1c3de-110">If the webpage contains multiple frames, the element name can only refer to an element in the same frame as the Player control.</span></span>

<span data-ttu-id="1c3de-111">**Windows Media Player 10 Mobile:** Questa proprietà è di sola lettura e restituisce sempre una stringa vuota.</span><span class="sxs-lookup"><span data-stu-id="1c3de-111">**Windows Media Player 10 Mobile:** This property is read only, and always returns an empty string.</span></span>

## <a name="examples"></a><span data-ttu-id="1c3de-112">Esempio</span><span class="sxs-lookup"><span data-stu-id="1c3de-112">Examples</span></span>

<span data-ttu-id="1c3de-113">Nell'esempio Microsoft JScript seguente viene usato *ClosedCaption*. **captioningID** per scegliere l'area di una pagina Web utilizzata per visualizzare le didascalie.</span><span class="sxs-lookup"><span data-stu-id="1c3de-113">The following Microsoft JScript example uses *ClosedCaption*.**captioningID** to choose the area of a webpage used to display captions.</span></span> <span data-ttu-id="1c3de-114">Sono stati creati due elementi DIV HTML con ID = CC1 e ID = CC2, rispettivamente.</span><span class="sxs-lookup"><span data-stu-id="1c3de-114">Two HTML DIV elements were created, with ID = CC1 and ID = CC2, respectively.</span></span> <span data-ttu-id="1c3de-115">L'oggetto **Player** è stato creato con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="1c3de-115">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create two HTML BUTTON elements to allow the user to choose a display region. -->
<INPUT TYPE = "BUTTON"  NAME = "SET1"  VALUE = "Move Caption to CC1"
       OnClick = "
           /* Clear the caption text from the other DIV */
           CC2.innerHTML = 'This is the CC2 DIV';

           /* Show the captions in the DIV named CC1. */ 
           Player.ClosedCaption.captioningID = 'CC1';
          ">

<INPUT TYPE = "BUTTON" NAME = "SET2" VALUE = "Move Caption to CC2"
       OnClick = "
           /* Clear the caption text from the other DIV */
           CC1.innerHTML = 'This is the CC1 DIV';

           /* Show the captions in the DIV named CC2. */
           Player.ClosedCaption.captioningID = 'CC2';
          ">

```



## <a name="requirements"></a><span data-ttu-id="1c3de-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1c3de-116">Requirements</span></span>



| <span data-ttu-id="1c3de-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="1c3de-117">Requirement</span></span> | <span data-ttu-id="1c3de-118">Valore</span><span class="sxs-lookup"><span data-stu-id="1c3de-118">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1c3de-119">Versione</span><span class="sxs-lookup"><span data-stu-id="1c3de-119">Version</span></span><br/> | <span data-ttu-id="1c3de-120">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="1c3de-120">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="1c3de-121">DLL</span><span class="sxs-lookup"><span data-stu-id="1c3de-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="1c3de-122"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1c3de-122"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c3de-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1c3de-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c3de-124">**Aggiunta di didascalie chiuse a file multimediali digitali**</span><span class="sxs-lookup"><span data-stu-id="1c3de-124">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="1c3de-125">**Oggetto ClosedCaption**</span><span class="sxs-lookup"><span data-stu-id="1c3de-125">**ClosedCaption Object**</span></span>](closedcaption-object.md)
</dt> </dl>

 

 





