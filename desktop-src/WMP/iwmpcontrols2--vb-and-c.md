---
title: Interfaccia IWMPControls2 (VB e C) (Wmp.h)
description: Fornisce un metodo che integra l'interfaccia IWMPControls.
ms.assetid: 6a181911-9ab1-4cab-a6a2-9e1465f44029
keywords:
- Interfaccia IWMPControls2 (VB e C) Windows Media Player
- Interfaccia IWMPControls2 (VB e C) Windows Media Player, descritta
topic_type:
- apiref
api_name:
- IWMPControls2 (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b955ee2a8b18f1629427dfe45da802759901ab00
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328212"
---
# <a name="iwmpcontrols2-vb-and-c-interface"></a><span data-ttu-id="769db-105">Interfaccia IWMPControls2 (VB e C#)</span><span class="sxs-lookup"><span data-stu-id="769db-105">IWMPControls2 (VB and C#) interface</span></span>

<span data-ttu-id="769db-106">Fornisce un metodo che integra l'interfaccia [**IWMPControls**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols) .</span><span class="sxs-lookup"><span data-stu-id="769db-106">Provides a method that supplements the [**IWMPControls**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols) interface.</span></span>

## <a name="members"></a><span data-ttu-id="769db-107">Membri</span><span class="sxs-lookup"><span data-stu-id="769db-107">Members</span></span>

<span data-ttu-id="769db-108">L'interfaccia **IWMPControls2 (VB e C#)** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="769db-108">The **IWMPControls2 (VB and C#)** interface has these types of members:</span></span>

-   [<span data-ttu-id="769db-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="769db-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="769db-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="769db-110">Methods</span></span>

<span data-ttu-id="769db-111">L'interfaccia **IWMPControls2 (VB e C#)** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="769db-111">The **IWMPControls2 (VB and C#)** interface has these methods.</span></span>



| <span data-ttu-id="769db-112">Metodo</span><span class="sxs-lookup"><span data-stu-id="769db-112">Method</span></span>                                                           | <span data-ttu-id="769db-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="769db-113">Description</span></span>                                                                                                 |
|:-----------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="769db-114">**passo**</span><span class="sxs-lookup"><span data-stu-id="769db-114">**step**</span></span>](wmplibiwmpcontrols2-iwmpcontrols2-step--vb-and-c.md) | <span data-ttu-id="769db-115">Sposta l'elemento multimediale del video corrente nel frame successivo o nel frame precedente e blocca la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="769db-115">Moves the current video media item to the next frame or the previous frame and freezes playback.</span></span><br/> |



 

<span data-ttu-id="769db-116">Nell'esempio di codice seguente viene illustrato come accedere a un'interfaccia [**IWMPControls2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols2) .</span><span class="sxs-lookup"><span data-stu-id="769db-116">The following example code shows how to access an [**IWMPControls2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols2) interface.</span></span> <span data-ttu-id="769db-117">Il codice di esempio esegue il cast del valore [**IWMPControls**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols) che la proprietà [**AxWindowsMediaPlayer. Ctlcontrols**](axwmplib-axwindowsmediaplayer-ctlcontrols--vb-and-c.md) restituisce a un valore **IWMPControls2** .</span><span class="sxs-lookup"><span data-stu-id="769db-117">The example code casts the [**IWMPControls**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols) value that the [**AxWindowsMediaPlayer.Ctlcontrols**](axwmplib-axwindowsmediaplayer-ctlcontrols--vb-and-c.md) property returns to a **IWMPControls2** value.</span></span>

<span data-ttu-id="769db-118">Per **C#**:</span><span class="sxs-lookup"><span data-stu-id="769db-118">For **C#**:</span></span>


```CSharp
IWMPControls2 Ctlcontrols2 = (IWMPControls2)AxWindowsMediaPlayer.Ctlcontrols;
```



<span data-ttu-id="769db-119">Per **VB**:</span><span class="sxs-lookup"><span data-stu-id="769db-119">For **VB**:</span></span>


```VB
Dim Ctlcontrols As WMPLib.IWMPControls = Me.AxWindowsMediaPlayer1.Ctlcontrols
Dim Ctlcontrols2 As WMPLib.IWMPControls2 = DirectCast(Ctlcontrols, WMPLib.IWMPControls2)
```



## <a name="requirements"></a><span data-ttu-id="769db-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="769db-120">Requirements</span></span>



| <span data-ttu-id="769db-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="769db-121">Requirement</span></span> | <span data-ttu-id="769db-122">Valore</span><span class="sxs-lookup"><span data-stu-id="769db-122">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="769db-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="769db-123">Header</span></span><br/> | <dl> <span data-ttu-id="769db-124"><dt>WMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="769db-124"><dt>Wmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="769db-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="769db-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="769db-126">**IWMPControls**</span><span class="sxs-lookup"><span data-stu-id="769db-126">**IWMPControls**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols)
</dt> <dt>

[<span data-ttu-id="769db-127">**Interfacce per Visual Basic .NET e C #**</span><span class="sxs-lookup"><span data-stu-id="769db-127">**Interfaces for Visual Basic .NET and C#**</span></span>](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[<span data-ttu-id="769db-128">**Interfaccia IWMPControls (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="769db-128">**IWMPControls Interface (VB and C#)**</span></span>](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="769db-129">**Interfaccia IWMPControls3 (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="769db-129">**IWMPControls3 Interface (VB and C#)**</span></span>](iwmpcontrols3--vb-and-c.md)
</dt> </dl>

 

 





