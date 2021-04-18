---
title: PLAYERAPPLICATION. hasDisplay (attributo)
description: L'attributo hasDisplay recupera un valore che indica se il video può essere visualizzato tramite il controllo Media Player remoto di Windows.
ms.assetid: c6a735a4-29ae-401c-9381-d8aad2c456eb
keywords:
- Media Player Windows PLAYERAPPLICATION. hasDisplay
topic_type:
- apiref
api_name:
- PLAYERAPPLICATION.hasDisplay
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7579c724496ee2f36ce12adb01c2f13a0962e7dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327051"
---
# <a name="playerapplicationhasdisplay"></a><span data-ttu-id="06dca-104">PLAYERAPPLICATION.hasDisplay</span><span class="sxs-lookup"><span data-stu-id="06dca-104">PLAYERAPPLICATION.hasDisplay</span></span>

<span data-ttu-id="06dca-105">L'attributo **hasDisplay** recupera un valore che indica se il video può essere visualizzato tramite il controllo Media Player remoto di Windows.</span><span class="sxs-lookup"><span data-stu-id="06dca-105">The **hasDisplay** attribute retrieves a value indicating whether video can display through the remoted Windows Media Player control.</span></span>

``` syntax
        elementID.hasDisplay
```

## <a name="possible-values"></a><span data-ttu-id="06dca-106">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="06dca-106">Possible Values</span></span>

<span data-ttu-id="06dca-107">Questo attributo è un **valore booleano** di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="06dca-107">This attribute is a read-only **Boolean**.</span></span>



| <span data-ttu-id="06dca-108">Valore</span><span class="sxs-lookup"><span data-stu-id="06dca-108">Value</span></span> | <span data-ttu-id="06dca-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="06dca-109">Description</span></span>               |
|-------|---------------------------|
| <span data-ttu-id="06dca-110">True</span><span class="sxs-lookup"><span data-stu-id="06dca-110">True</span></span>  | <span data-ttu-id="06dca-111">Il video può essere visualizzato.</span><span class="sxs-lookup"><span data-stu-id="06dca-111">The video can display.</span></span>    |
| <span data-ttu-id="06dca-112">Falso</span><span class="sxs-lookup"><span data-stu-id="06dca-112">False</span></span> | <span data-ttu-id="06dca-113">Non è possibile visualizzare il video.</span><span class="sxs-lookup"><span data-stu-id="06dca-113">The video cannot display.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="06dca-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="06dca-114">Remarks</span></span>

<span data-ttu-id="06dca-115">Questo attributo viene utilizzato solo quando la comunicazione remota del controllo Media Player di Windows.</span><span class="sxs-lookup"><span data-stu-id="06dca-115">This attribute is used only when remoting the Windows Media Player control.</span></span>

<span data-ttu-id="06dca-116">È possibile eseguire contemporaneamente più controlli Media Player di Windows, ma i video possono essere visualizzati solo in una posizione alla volta, sia nella modalità completa del lettore che in uno dei controlli remoti.</span><span class="sxs-lookup"><span data-stu-id="06dca-116">Several Windows Media Player controls can be running remotely at the same time, but video can only display in one location at a time, either in the full mode of the Player or in one of the remoted controls.</span></span> <span data-ttu-id="06dca-117">Usare questa proprietà per determinare se il controllo corrente è quello tramite il quale è possibile visualizzare il video.</span><span class="sxs-lookup"><span data-stu-id="06dca-117">Use this property to determine whether the current control is the one through which video can be displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="06dca-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="06dca-118">Requirements</span></span>



| <span data-ttu-id="06dca-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="06dca-119">Requirement</span></span> | <span data-ttu-id="06dca-120">Valore</span><span class="sxs-lookup"><span data-stu-id="06dca-120">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="06dca-121">Versione</span><span class="sxs-lookup"><span data-stu-id="06dca-121">Version</span></span><br/> | <span data-ttu-id="06dca-122">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="06dca-122">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="06dca-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="06dca-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06dca-124">**Elemento PLAYERAPPLICATION**</span><span class="sxs-lookup"><span data-stu-id="06dca-124">**PLAYERAPPLICATION Element**</span></span>](playerapplication-element.md)
</dt> <dt>

[<span data-ttu-id="06dca-125">**Gestione remota del controllo di Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="06dca-125">**Remoting the Windows Media Player Control**</span></span>](remoting-the-windows-media-player-control.md)
</dt> </dl>

 

 





