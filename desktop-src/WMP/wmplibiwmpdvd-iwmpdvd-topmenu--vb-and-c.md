---
title: Metodo IWMPDVD tomenu
description: Il metodo di menu di scelta rapida interrompe la riproduzione e visualizza il menu principale (o radice) per il titolo corrente.
ms.assetid: d6eb6311-167d-4cc1-b445-4e3d3e111e43
keywords:
- Windows Media Player metodo di menu di scelta rapida
- Metodo di menu di scelta rapida Windows Media Player, interfaccia IWMPDVD
- Interfaccia IWMPDVD Media Player Windows, metodo tomenu
topic_type:
- apiref
api_name:
- IWMPDVD.topMenu
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d59bf126a026626cc7f1ba87ea9d0eb94bd1a91
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332446"
---
# <a name="iwmpdvdtopmenu-method"></a><span data-ttu-id="f8772-106">Metodo IWMPDVD:: tomenu</span><span class="sxs-lookup"><span data-stu-id="f8772-106">IWMPDVD::topMenu method</span></span>

<span data-ttu-id="f8772-107">Il metodo di **menu di scelta rapida** interrompe la riproduzione e visualizza il menu principale (o radice) per il titolo corrente.</span><span class="sxs-lookup"><span data-stu-id="f8772-107">The **topMenu** method stops playback and displays the top (or root) menu for the current title.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8772-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f8772-108">Syntax</span></span>


```CSharp
public void topMenu();
```


```VB

Public Sub topMenu()
Implements IWMPDVD.topMenu
```





## <a name="parameters"></a><span data-ttu-id="f8772-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="f8772-109">Parameters</span></span>

<span data-ttu-id="f8772-110">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="f8772-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f8772-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f8772-111">Return value</span></span>

<span data-ttu-id="f8772-112">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="f8772-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f8772-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="f8772-113">Remarks</span></span>

<span data-ttu-id="f8772-114">Ogni DVD viene creato in modo diverso.</span><span class="sxs-lookup"><span data-stu-id="f8772-114">Every DVD is authored differently.</span></span> <span data-ttu-id="f8772-115">Il DVD deve contenere un menu per il funzionamento di questo metodo.</span><span class="sxs-lookup"><span data-stu-id="f8772-115">The DVD must contain a menu for this method to work.</span></span> <span data-ttu-id="f8772-116">Alcuni DVD vengono creati in modo che i metodi **tomenu** e **IWMPDVD. titleMenu** aprano lo stesso menu.</span><span class="sxs-lookup"><span data-stu-id="f8772-116">Some DVDs are authored so that the **topMenu** and **IWMPDVD.titleMenu** methods open the same menu.</span></span> <span data-ttu-id="f8772-117">Il metodo di **menu di scelta rapida** richiama in genere il menu principale (o radice), ma può richiamare il menu del titolo se non è disponibile alcun menu radice.</span><span class="sxs-lookup"><span data-stu-id="f8772-117">The **topMenu** method usually invokes the top (or root) menu, but it may invoke the title menu if there is no root menu available.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8772-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f8772-118">Requirements</span></span>



| <span data-ttu-id="f8772-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="f8772-119">Requirement</span></span> | <span data-ttu-id="f8772-120">Valore</span><span class="sxs-lookup"><span data-stu-id="f8772-120">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8772-121">Versione</span><span class="sxs-lookup"><span data-stu-id="f8772-121">Version</span></span><br/>   | <span data-ttu-id="f8772-122">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="f8772-122">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="f8772-123">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f8772-123">Namespace</span></span><br/> | <span data-ttu-id="f8772-124">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="f8772-124">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="f8772-125">Assembly</span><span class="sxs-lookup"><span data-stu-id="f8772-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="f8772-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="f8772-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8772-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f8772-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8772-128">**Interfaccia IWMPDVD (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="f8772-128">**IWMPDVD Interface (VB and C#)**</span></span>](iwmpdvd--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="f8772-129">**IWMPDVD. titleMenu (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="f8772-129">**IWMPDVD.titleMenu (VB and C#)**</span></span>](wmplibiwmpdvd-iwmpdvd-titlemenu--vb-and-c.md)
</dt> </dl>

 

 





