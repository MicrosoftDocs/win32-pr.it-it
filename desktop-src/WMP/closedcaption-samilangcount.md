---
title: ClosedCaption.SAMILangCount
description: La proprietà SAMILangCount Recupera il numero di lingue supportate dal file SAMI corrente.
ms.assetid: ad2e776a-b430-46ee-9705-18d279e8715e
keywords:
- Media Player Windows ClosedCaption. SAMILangCount
topic_type:
- apiref
api_name:
- ClosedCaption.SAMILangCount
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57d202ecc8bc18261ac4569f2251201e15911f91
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326729"
---
# <a name="closedcaptionsamilangcount"></a><span data-ttu-id="6c485-104">ClosedCaption.SAMILangCount</span><span class="sxs-lookup"><span data-stu-id="6c485-104">ClosedCaption.SAMILangCount</span></span>

<span data-ttu-id="6c485-105">La proprietà **SAMILangCount** Recupera il numero di lingue supportate dal file Sami corrente.</span><span class="sxs-lookup"><span data-stu-id="6c485-105">The **SAMILangCount** property retrieves the number of languages supported by the current SAMI file.</span></span>

``` syntax
player.closedCaption.SAMILangCount
```

## <a name="possible-values"></a><span data-ttu-id="6c485-106">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="6c485-106">Possible Values</span></span>

<span data-ttu-id="6c485-107">Questa proprietà è un **numero** di sola lettura (**Long**).</span><span class="sxs-lookup"><span data-stu-id="6c485-107">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="6c485-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="6c485-108">Remarks</span></span>

<span data-ttu-id="6c485-109">Questo metodo non può essere usato fino a quando non viene aperto un file multimediale digitale (*Player*.**openState** è uguale a 13).</span><span class="sxs-lookup"><span data-stu-id="6c485-109">This method cannot be used until a digital media file is open (*Player*.**openState** is equal to 13).</span></span>

<span data-ttu-id="6c485-110">**Windows Media Player 10 Mobile:** Questa proprietà restituisce sempre 0.</span><span class="sxs-lookup"><span data-stu-id="6c485-110">**Windows Media Player 10 Mobile:** This property always returns 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c485-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6c485-111">Requirements</span></span>



| <span data-ttu-id="6c485-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c485-112">Requirement</span></span> | <span data-ttu-id="6c485-113">Valore</span><span class="sxs-lookup"><span data-stu-id="6c485-113">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6c485-114">Versione</span><span class="sxs-lookup"><span data-stu-id="6c485-114">Version</span></span><br/> | <span data-ttu-id="6c485-115">Windows Media Player 9 serie o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="6c485-115">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="6c485-116">DLL</span><span class="sxs-lookup"><span data-stu-id="6c485-116">DLL</span></span><br/>     | <dl> <span data-ttu-id="6c485-117"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6c485-117"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c485-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6c485-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c485-119">**Aggiunta di didascalie chiuse a file multimediali digitali**</span><span class="sxs-lookup"><span data-stu-id="6c485-119">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="6c485-120">**Oggetto ClosedCaption**</span><span class="sxs-lookup"><span data-stu-id="6c485-120">**ClosedCaption Object**</span></span>](closedcaption-object.md)
</dt> <dt>

[<span data-ttu-id="6c485-121">**ClosedCaption.getSAMILangName**</span><span class="sxs-lookup"><span data-stu-id="6c485-121">**ClosedCaption.getSAMILangName**</span></span>](closedcaption-getsamilangname.md)
</dt> <dt>

[<span data-ttu-id="6c485-122">**ClosedCaption.SAMILang**</span><span class="sxs-lookup"><span data-stu-id="6c485-122">**ClosedCaption.SAMILang**</span></span>](closedcaption-samilang.md)
</dt> </dl>

 

 





