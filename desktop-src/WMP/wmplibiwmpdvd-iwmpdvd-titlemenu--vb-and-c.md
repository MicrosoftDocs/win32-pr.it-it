---
title: Metodo IWMPDVD titleMenu
description: Il metodo titleMenu interrompe la riproduzione e visualizza il menu del titolo.
ms.assetid: 28714644-12c4-46eb-95fc-70091624f6dd
keywords:
- Metodo titleMenu Windows Media Player
- Metodo titleMenu Windows Media Player, interfaccia IWMPDVD
- Interfaccia IWMPDVD Windows Media Player, metodo titleMenu
topic_type:
- apiref
api_name:
- IWMPDVD.titleMenu
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0889a3f65ccefe4e09bb5ff47a66867681dcc801
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332447"
---
# <a name="iwmpdvdtitlemenu-method"></a><span data-ttu-id="365b6-106">Metodo IWMPDVD:: titleMenu</span><span class="sxs-lookup"><span data-stu-id="365b6-106">IWMPDVD::titleMenu method</span></span>

<span data-ttu-id="365b6-107">Il metodo **titleMenu** interrompe la riproduzione e visualizza il menu del titolo.</span><span class="sxs-lookup"><span data-stu-id="365b6-107">The **titleMenu** method stops playback and displays the title menu.</span></span>

## <a name="syntax"></a><span data-ttu-id="365b6-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="365b6-108">Syntax</span></span>


```CSharp
public void titleMenu();
```


```VB

Public Sub titleMenu()
Implements IWMPDVD.titleMenu
```





## <a name="parameters"></a><span data-ttu-id="365b6-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="365b6-109">Parameters</span></span>

<span data-ttu-id="365b6-110">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="365b6-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="365b6-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="365b6-111">Return value</span></span>

<span data-ttu-id="365b6-112">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="365b6-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="365b6-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="365b6-113">Remarks</span></span>

<span data-ttu-id="365b6-114">Ogni DVD viene creato in modo diverso.</span><span class="sxs-lookup"><span data-stu-id="365b6-114">Every DVD is authored differently.</span></span> <span data-ttu-id="365b6-115">Il DVD deve contenere un menu per il funzionamento di questo metodo.</span><span class="sxs-lookup"><span data-stu-id="365b6-115">The DVD must contain a menu for this method to work.</span></span> <span data-ttu-id="365b6-116">Alcuni DVD vengono creati in modo che i metodi **IWMPDVD. tomenu** e **titleMenu** aprano lo stesso menu.</span><span class="sxs-lookup"><span data-stu-id="365b6-116">Some DVDs are authored so that the **IWMPDVD.topMenu** and **titleMenu** methods open the same menu.</span></span> <span data-ttu-id="365b6-117">Il metodo **titleMenu** richiama in genere il menu del titolo, ma può richiamare il menu superiore se non è disponibile alcun menu titolo.</span><span class="sxs-lookup"><span data-stu-id="365b6-117">The **titleMenu** method usually invokes the title menu, but it may invoke the top menu if there is no title menu available.</span></span>

## <a name="requirements"></a><span data-ttu-id="365b6-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="365b6-118">Requirements</span></span>



| <span data-ttu-id="365b6-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="365b6-119">Requirement</span></span> | <span data-ttu-id="365b6-120">Valore</span><span class="sxs-lookup"><span data-stu-id="365b6-120">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="365b6-121">Versione</span><span class="sxs-lookup"><span data-stu-id="365b6-121">Version</span></span><br/>   | <span data-ttu-id="365b6-122">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="365b6-122">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="365b6-123">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="365b6-123">Namespace</span></span><br/> | <span data-ttu-id="365b6-124">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="365b6-124">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="365b6-125">Assembly</span><span class="sxs-lookup"><span data-stu-id="365b6-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="365b6-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="365b6-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="365b6-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="365b6-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="365b6-128">**Interfaccia IWMPDVD (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="365b6-128">**IWMPDVD Interface (VB and C#)**</span></span>](iwmpdvd--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="365b6-129">**IWMPDVD. tomenu (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="365b6-129">**IWMPDVD.topMenu (VB and C#)**</span></span>](wmplibiwmpdvd-iwmpdvd-topmenu--vb-and-c.md)
</dt> </dl>

 

 





