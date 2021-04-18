---
title: ClosedCaption.SAMIStyleCount
description: La proprietà SAMIStyleCount Recupera il numero di stili supportati dal file SAMI corrente.
ms.assetid: 57a85e5d-1598-4cb3-b47d-a6d8f22adfff
keywords:
- Media Player Windows ClosedCaption. SAMIStyleCount
topic_type:
- apiref
api_name:
- ClosedCaption.SAMIStyleCount
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ab48fc6660065da1635b58b67784f2ab0ff91b8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324835"
---
# <a name="closedcaptionsamistylecount"></a><span data-ttu-id="e9503-104">ClosedCaption.SAMIStyleCount</span><span class="sxs-lookup"><span data-stu-id="e9503-104">ClosedCaption.SAMIStyleCount</span></span>

<span data-ttu-id="e9503-105">La proprietà **SAMIStyleCount** Recupera il numero di stili supportati dal file Sami corrente.</span><span class="sxs-lookup"><span data-stu-id="e9503-105">The **SAMIStyleCount** property retrieves the number of styles supported by the current SAMI file.</span></span>

``` syntax
player.closedCaption.SAMIStyleCount
```

## <a name="possible-values"></a><span data-ttu-id="e9503-106">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="e9503-106">Possible Values</span></span>

<span data-ttu-id="e9503-107">Questa proprietà è un **numero** di sola lettura (**Long**).</span><span class="sxs-lookup"><span data-stu-id="e9503-107">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="e9503-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="e9503-108">Remarks</span></span>

<span data-ttu-id="e9503-109">Questo metodo non può essere usato fino a quando non viene aperto un file multimediale digitale (*Player*.**openState** è uguale a 13).</span><span class="sxs-lookup"><span data-stu-id="e9503-109">This method cannot be used until a digital media file is open (*Player*.**openState** is equal to 13).</span></span>

<span data-ttu-id="e9503-110">**Windows Media Player 10 Mobile:** Questa proprietà restituisce sempre 0.</span><span class="sxs-lookup"><span data-stu-id="e9503-110">**Windows Media Player 10 Mobile:** This property always returns 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9503-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e9503-111">Requirements</span></span>



| <span data-ttu-id="e9503-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="e9503-112">Requirement</span></span> | <span data-ttu-id="e9503-113">Valore</span><span class="sxs-lookup"><span data-stu-id="e9503-113">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e9503-114">Versione</span><span class="sxs-lookup"><span data-stu-id="e9503-114">Version</span></span><br/> | <span data-ttu-id="e9503-115">Windows Media Player 9 serie o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="e9503-115">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="e9503-116">DLL</span><span class="sxs-lookup"><span data-stu-id="e9503-116">DLL</span></span><br/>     | <dl> <span data-ttu-id="e9503-117"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e9503-117"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9503-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e9503-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9503-119">**Aggiunta di didascalie chiuse a file multimediali digitali**</span><span class="sxs-lookup"><span data-stu-id="e9503-119">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="e9503-120">**Oggetto ClosedCaption**</span><span class="sxs-lookup"><span data-stu-id="e9503-120">**ClosedCaption Object**</span></span>](closedcaption-object.md)
</dt> <dt>

[<span data-ttu-id="e9503-121">**ClosedCaption.getSAMIStyleName**</span><span class="sxs-lookup"><span data-stu-id="e9503-121">**ClosedCaption.getSAMIStyleName**</span></span>](closedcaption-getsamistylename.md)
</dt> <dt>

[<span data-ttu-id="e9503-122">**ClosedCaption.SAMIStyle**</span><span class="sxs-lookup"><span data-stu-id="e9503-122">**ClosedCaption.SAMIStyle**</span></span>](closedcaption-samistyle.md)
</dt> </dl>

 

 





