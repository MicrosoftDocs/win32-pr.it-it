---
description: Il metodo ShowCursor rende visibile il cursore quando l'oggetto MSWebDVD è in modalità schermo intero.
ms.assetid: 3a611cc8-7979-473d-bd0f-f4ca43701c63
title: Metodo ShowCursor
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 917c1d0d2724259fc19baf72ab6b3844cddc3419
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103876642"
---
# <a name="showcursor-method"></a><span data-ttu-id="771a6-103">Metodo ShowCursor</span><span class="sxs-lookup"><span data-stu-id="771a6-103">ShowCursor Method</span></span>

> [!Note]  
> <span data-ttu-id="771a6-104">Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="771a6-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="771a6-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="771a6-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="771a6-106">Il `ShowCursor` metodo rende il cursore visibile quando l'oggetto **mswebdvd** è in modalità schermo intero.</span><span class="sxs-lookup"><span data-stu-id="771a6-106">The `ShowCursor` method makes the cursor visible when the **MSWebDVD** object is in full-screen mode.</span></span>

``` syntax
MSWebDVD.ShowCursor(bShow)
```

## <a name="parameters"></a><span data-ttu-id="771a6-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="771a6-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="771a6-108"><span id="bShow"></span><span id="bshow"></span><span id="BSHOW"></span>*bShow*</span><span class="sxs-lookup"><span data-stu-id="771a6-108"><span id="bShow"></span><span id="bshow"></span><span id="BSHOW"></span>*bShow*</span></span>
</dt> <dd>

<span data-ttu-id="771a6-109">Specifica se mostrare il cursore come valore booleano.</span><span class="sxs-lookup"><span data-stu-id="771a6-109">Specifies whether to show the cursor as a Boolean.</span></span>



| <span data-ttu-id="771a6-110">Valore</span><span class="sxs-lookup"><span data-stu-id="771a6-110">Value</span></span> | <span data-ttu-id="771a6-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="771a6-111">Description</span></span>            |
|-------|------------------------|
| <span data-ttu-id="771a6-112">true</span><span class="sxs-lookup"><span data-stu-id="771a6-112">true</span></span>  | <span data-ttu-id="771a6-113">Mostra il cursore</span><span class="sxs-lookup"><span data-stu-id="771a6-113">Show the cursor</span></span>        |
| <span data-ttu-id="771a6-114">false</span><span class="sxs-lookup"><span data-stu-id="771a6-114">false</span></span> | <span data-ttu-id="771a6-115">Non visualizzare il cursore</span><span class="sxs-lookup"><span data-stu-id="771a6-115">Do not show the cursor</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="771a6-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="771a6-116">Return Value</span></span>

<span data-ttu-id="771a6-117">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="771a6-117">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="771a6-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="771a6-118">Remarks</span></span>

<span data-ttu-id="771a6-119">Quando la visualizzazione DVD passa alla modalità schermo intero, il cursore scompare tra 3 e 5 secondi.</span><span class="sxs-lookup"><span data-stu-id="771a6-119">When the DVD display goes into full-screen mode, the cursor disappears within 3 to 5 seconds.</span></span> <span data-ttu-id="771a6-120">Utilizzare questo metodo per rendere nuovamente visibile il cursore se i pulsanti di controllo dell'applicazione sono visibili in modalità schermo intero.</span><span class="sxs-lookup"><span data-stu-id="771a6-120">Use this method to make the cursor visible again if your application's control buttons are visible in full-screen mode.</span></span>

 

 



