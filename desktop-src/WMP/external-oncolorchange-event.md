---
title: Evento External. OnColorChange
description: Si noti che in questo argomento viene descritta la funzionalità progettata per l'utilizzo da punti vendita online. | Evento External. OnColorChange
ms.assetid: f2cd44b1-c813-479b-b847-96ddb9572697
keywords:
- Media Player di Windows dell'evento External. OnColorChange
topic_type:
- apiref
api_name:
- External.OnColorChange Event
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 029c8bb860443ed026737c7413be2bed8862c6d2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328886"
---
# <a name="externaloncolorchange-event"></a><span data-ttu-id="a8a85-105">Evento External. OnColorChange</span><span class="sxs-lookup"><span data-stu-id="a8a85-105">External.OnColorChange Event</span></span>

> [!Note]  
> <span data-ttu-id="a8a85-106">Questo argomento descrive la funzionalità progettata per l'uso da punti vendita online.</span><span class="sxs-lookup"><span data-stu-id="a8a85-106">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="a8a85-107">L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato.</span><span class="sxs-lookup"><span data-stu-id="a8a85-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="a8a85-108">L'evento **OnColorChange** si verifica quando cambia il colore dell'interfaccia utente di Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="a8a85-108">The **OnColorChange** event occurs when the color of the Windows Media Player user interface changes.</span></span>

``` syntax
window.external.OnColorChange = FunctionName
```

## <a name="possible-values"></a><span data-ttu-id="a8a85-109">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="a8a85-109">Possible Values</span></span>

<span data-ttu-id="a8a85-110">Si tratta di una proprietà di sola scrittura che specifica il nome della funzione nello script che Windows Media Player chiama quando si verifica l'evento.</span><span class="sxs-lookup"><span data-stu-id="a8a85-110">This is a write-only property that specifies the name of the function in script that Windows Media Player calls when the event occurs.</span></span>

## <a name="parameters"></a><span data-ttu-id="a8a85-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="a8a85-111">Parameters</span></span>

<span data-ttu-id="a8a85-112">La funzione che gestisce questo evento non accetta parametri.</span><span class="sxs-lookup"><span data-stu-id="a8a85-112">The function that handles this event takes no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="a8a85-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="a8a85-113">Remarks</span></span>

<span data-ttu-id="a8a85-114">Gli utenti possono modificare il colore dell'interfaccia utente di Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="a8a85-114">Users can change the color of the Windows Media Player user interface.</span></span> <span data-ttu-id="a8a85-115">È possibile usare questo evento per personalizzare l'aspetto della pagina Web ospitata in modo che corrisponda al lettore.</span><span class="sxs-lookup"><span data-stu-id="a8a85-115">You can use this event to customize the appearance of your hosted webpage to match the Player.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8a85-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a8a85-116">Requirements</span></span>



| <span data-ttu-id="a8a85-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8a85-117">Requirement</span></span> | <span data-ttu-id="a8a85-118">Valore</span><span class="sxs-lookup"><span data-stu-id="a8a85-118">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a8a85-119">Versione</span><span class="sxs-lookup"><span data-stu-id="a8a85-119">Version</span></span><br/> | <span data-ttu-id="a8a85-120">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="a8a85-120">Windows Media Player 9 Series or later</span></span><br/>                                  |
| <span data-ttu-id="a8a85-121">DLL</span><span class="sxs-lookup"><span data-stu-id="a8a85-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="a8a85-122"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a8a85-122"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8a85-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a8a85-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8a85-124">**Oggetto esterno per i negozi di tipo 2 online**</span><span class="sxs-lookup"><span data-stu-id="a8a85-124">**External Object for Type 2 Online Stores**</span></span>](external-object-for-type-2-online-stores.md)
</dt> </dl>

 

 





