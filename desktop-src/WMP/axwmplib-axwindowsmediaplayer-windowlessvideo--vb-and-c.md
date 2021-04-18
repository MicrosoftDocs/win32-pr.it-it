---
title: Proprietà AxWindowsMediaPlayer. windowlessVideo
description: La proprietà windowlessVideo Ottiene o imposta un valore che indica se il controllo Windows Media Player esegue il rendering del video in modalità senza finestra.
ms.assetid: 70386aae-cd30-405d-90dd-9b3fa63dad17
keywords:
- Finestra delle proprietà di windowlessVideo Media Player
- Proprietà windowlessVideo Windows Media Player, classe AxWindowsMediaPlayer
- Classe AxWindowsMediaPlayer Media Player Windows, proprietà windowlessVideo
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.windowlessVideo
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d22ecc0f39b03201809877fe8ebc667d62e16d0b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333771"
---
# <a name="axwindowsmediaplayerwindowlessvideo-property"></a><span data-ttu-id="1eed4-106">Proprietà AxWindowsMediaPlayer. windowlessVideo</span><span class="sxs-lookup"><span data-stu-id="1eed4-106">AxWindowsMediaPlayer.windowlessVideo property</span></span>

<span data-ttu-id="1eed4-107">La proprietà windowlessVideo Ottiene o imposta un valore che indica se il controllo Windows Media Player esegue il rendering del video in modalità senza finestra.</span><span class="sxs-lookup"><span data-stu-id="1eed4-107">The windowlessVideo property gets or sets a value indicating whether the Windows Media Player control renders video in windowless mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="1eed4-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1eed4-108">Syntax</span></span>


```CSharp
public System.Boolean windowlessVideo {get; set;}
```


```VB

Public Property windowlessVideo As System.Boolean
```





## <a name="property-value"></a><span data-ttu-id="1eed4-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="1eed4-109">Property value</span></span>

<span data-ttu-id="1eed4-110">Valore System. Boolean che indica se il controllo Windows Media Player esegue il rendering del video in modalità senza finestra.</span><span class="sxs-lookup"><span data-stu-id="1eed4-110">A System.Boolean value indicating whether the Windows Media Player control renders video in windowless mode.</span></span> <span data-ttu-id="1eed4-111">Il valore predefinito è false.</span><span class="sxs-lookup"><span data-stu-id="1eed4-111">The default value is false.</span></span>

## <a name="remarks"></a><span data-ttu-id="1eed4-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="1eed4-112">Remarks</span></span>

<span data-ttu-id="1eed4-113">Per impostazione predefinita, un controllo di Windows Media Player incorporato esegue il rendering dei video nella propria finestra all'interno dell'area client.</span><span class="sxs-lookup"><span data-stu-id="1eed4-113">By default, an embedded Windows Media Player control renders video in its own window within the client area.</span></span> <span data-ttu-id="1eed4-114">Quando **windowlessVideo** è impostato su true, l'oggetto Windows Media Player esegue il rendering del video direttamente nell'area client, in modo che sia possibile applicare effetti speciali o sovrapporre il video con il testo.</span><span class="sxs-lookup"><span data-stu-id="1eed4-114">When **windowlessVideo** is set to true, the Windows Media Player object renders video directly in the client area, so you can apply special effects or layer the video with text.</span></span>

<span data-ttu-id="1eed4-115">In Windows Vista, il rendering di video in modalità senza finestra può compromettere le prestazioni.</span><span class="sxs-lookup"><span data-stu-id="1eed4-115">In Windows Vista, rendering video in windowless mode can degrade performance.</span></span>

<span data-ttu-id="1eed4-116">Il recupero di un valore per questa proprietà non è supportato per Netscape Navigator.</span><span class="sxs-lookup"><span data-stu-id="1eed4-116">Getting a value for this property is not supported for Netscape Navigator.</span></span> <span data-ttu-id="1eed4-117">L'impostazione di un valore per questa proprietà in Netscape Navigator può produrre risultati imprevisti.</span><span class="sxs-lookup"><span data-stu-id="1eed4-117">Setting a value for this property in Netscape Navigator may yield unexpected results.</span></span>

## <a name="requirements"></a><span data-ttu-id="1eed4-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1eed4-118">Requirements</span></span>



| <span data-ttu-id="1eed4-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="1eed4-119">Requirement</span></span> | <span data-ttu-id="1eed4-120">Valore</span><span class="sxs-lookup"><span data-stu-id="1eed4-120">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1eed4-121">Versione</span><span class="sxs-lookup"><span data-stu-id="1eed4-121">Version</span></span><br/>   | <span data-ttu-id="1eed4-122">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="1eed4-122">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="1eed4-123">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="1eed4-123">Namespace</span></span><br/> | <span data-ttu-id="1eed4-124">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="1eed4-124">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="1eed4-125">Assembly</span><span class="sxs-lookup"><span data-stu-id="1eed4-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="1eed4-126"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="1eed4-126"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1eed4-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1eed4-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1eed4-128">**Oggetto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="1eed4-128">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





