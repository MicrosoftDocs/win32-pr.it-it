---
title: Controls. currentPositionString
description: La proprietà currentPositionString recupera la posizione corrente nell'elemento multimediale come stringa formattata come HH MM SS (ore, minuti e secondi).
ms.assetid: 2b360cdb-3cf8-4d3c-82c2-7eb621f82f4c
keywords:
- Media Player di Windows Controls. currentPositionString
topic_type:
- apiref
api_name:
- Controls.currentPositionString
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbf3472d71afc543c596485d10f0d7e59dde90a0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331760"
---
# <a name="controlscurrentpositionstring"></a><span data-ttu-id="1cc5a-104">Controls. currentPositionString</span><span class="sxs-lookup"><span data-stu-id="1cc5a-104">Controls.currentPositionString</span></span>

<span data-ttu-id="1cc5a-105">La proprietà **currentPositionString** recupera la posizione corrente nell'elemento multimediale come **stringa** formattata come HH: mm: SS (ore, minuti e secondi).</span><span class="sxs-lookup"><span data-stu-id="1cc5a-105">The **currentPositionString** property retrieves the current position in the media item as a **String** formatted as HH:MM:SS (hours, minutes, and seconds).</span></span>

``` syntax
player.controls.currentPositionString
      
```

## <a name="possible-values"></a><span data-ttu-id="1cc5a-106">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="1cc5a-106">Possible Values</span></span>

<span data-ttu-id="1cc5a-107">Questa proprietà è una **stringa** di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="1cc5a-107">This property is a read-only **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="1cc5a-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="1cc5a-108">Remarks</span></span>

<span data-ttu-id="1cc5a-109">Se la lunghezza dell'elemento multimediale è inferiore a un'ora, la parte HH: non è inclusa.</span><span class="sxs-lookup"><span data-stu-id="1cc5a-109">If the media item is less than an hour long, the HH: portion is not included.</span></span>

> [!Note]  
> <span data-ttu-id="1cc5a-110">È necessario includere il codice per arrestare il timer quando l'elemento multimediale viene arrestato o sospeso.</span><span class="sxs-lookup"><span data-stu-id="1cc5a-110">You should include code to stop the timer when the media item is stopped or paused.</span></span>

 

## <a name="examples"></a><span data-ttu-id="1cc5a-111">Esempio</span><span class="sxs-lookup"><span data-stu-id="1cc5a-111">Examples</span></span>

<span data-ttu-id="1cc5a-112">Nell'esempio JScript seguente viene avviato un timer HTML che visualizza la posizione corrente del file multimediale a intervalli di un secondo.</span><span class="sxs-lookup"><span data-stu-id="1cc5a-112">The following JScript example starts an HTML timer that displays the current position of the media file at one-second intervals.</span></span> <span data-ttu-id="1cc5a-113">È stato creato un elemento di testo HTML denominato testo per visualizzare la posizione corrente.</span><span class="sxs-lookup"><span data-stu-id="1cc5a-113">An HTML TEXT element named MyText was created to display the current position.</span></span> <span data-ttu-id="1cc5a-114">L'oggetto **Player** è stato creato con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="1cc5a-114">The **Player** object was created with ID = "Player".</span></span>


```JScript
var timer = window.setInterval("MyText.value = Player.controls.currentPositionString",1000);
```



## <a name="requirements"></a><span data-ttu-id="1cc5a-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1cc5a-115">Requirements</span></span>



| <span data-ttu-id="1cc5a-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="1cc5a-116">Requirement</span></span> | <span data-ttu-id="1cc5a-117">Valore</span><span class="sxs-lookup"><span data-stu-id="1cc5a-117">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1cc5a-118">Versione</span><span class="sxs-lookup"><span data-stu-id="1cc5a-118">Version</span></span><br/> | <span data-ttu-id="1cc5a-119">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="1cc5a-119">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="1cc5a-120">DLL</span><span class="sxs-lookup"><span data-stu-id="1cc5a-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="1cc5a-121"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1cc5a-121"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1cc5a-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1cc5a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1cc5a-123">**Oggetto Controls**</span><span class="sxs-lookup"><span data-stu-id="1cc5a-123">**Controls Object**</span></span>](controls-object.md)
</dt> </dl>

 

 





