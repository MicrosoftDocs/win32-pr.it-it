---
title: Proprietà AxWindowsMediaPlayer. stretchToFit
description: La proprietà stretchToFit Ottiene o imposta un valore che indica se il video visualizzato dal controllo Media Player di Windows viene ridimensionato automaticamente per adattarsi alla finestra video, quando la finestra video è più grande delle dimensioni dell'immagine video.
ms.assetid: 02e2bcba-4975-4ddd-996b-9bd40774ebc1
keywords:
- Finestra delle proprietà di stretchToFit Media Player
- Proprietà stretchToFit Windows Media Player, classe AxWindowsMediaPlayer
- Classe AxWindowsMediaPlayer Media Player Windows, proprietà stretchToFit
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.stretchToFit
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2dd6937ffa556817a80f0b21dfaed6d270c2e351
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330363"
---
# <a name="axwindowsmediaplayerstretchtofit-property"></a><span data-ttu-id="ccb74-106">Proprietà AxWindowsMediaPlayer. stretchToFit</span><span class="sxs-lookup"><span data-stu-id="ccb74-106">AxWindowsMediaPlayer.stretchToFit property</span></span>

<span data-ttu-id="ccb74-107">La proprietà stretchToFit Ottiene o imposta un valore che indica se il video visualizzato dal controllo Media Player di Windows viene ridimensionato automaticamente per adattarsi alla finestra video, quando la finestra video è più grande delle dimensioni dell'immagine video.</span><span class="sxs-lookup"><span data-stu-id="ccb74-107">The stretchToFit property gets or sets a value indicating whether video displayed by the Windows Media Player control automatically sizes to fit the video window, when the video window is larger than the dimensions of the video image.</span></span>

## <a name="syntax"></a><span data-ttu-id="ccb74-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ccb74-108">Syntax</span></span>


```CSharp
public System.Boolean stretchToFit {get; set;}
```


```VB

Public Property stretchToFit As System.Boolean
```





## <a name="property-value"></a><span data-ttu-id="ccb74-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="ccb74-109">Property value</span></span>

<span data-ttu-id="ccb74-110">Valore System. Boolean che indica se il video si estenderà per adattarsi alla finestra.</span><span class="sxs-lookup"><span data-stu-id="ccb74-110">The System.Boolean value that indicates whether the video will stretch to fit the window.</span></span> <span data-ttu-id="ccb74-111">Il valore predefinito è false.</span><span class="sxs-lookup"><span data-stu-id="ccb74-111">The default value is false.</span></span>

## <a name="remarks"></a><span data-ttu-id="ccb74-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="ccb74-112">Remarks</span></span>

<span data-ttu-id="ccb74-113">Quando **stretchToFit** è impostato su true, il controllo Media Player Windows mantiene le proporzioni originali del video.</span><span class="sxs-lookup"><span data-stu-id="ccb74-113">When **stretchToFit** is set to true, the Windows Media Player control maintains the original aspect ratio of the video.</span></span> <span data-ttu-id="ccb74-114">Se le proporzioni del video non corrispondono alle proporzioni della finestra video, le aree della maschera nera possono essere visualizzate nella parte superiore e inferiore, o a sinistra e a destra, dell'immagine del video.</span><span class="sxs-lookup"><span data-stu-id="ccb74-114">If the aspect ratio of the video does not match the aspect ratio of the video window, black mask areas may appear on either the top and the bottom, or left and right, of the video image.</span></span>

<span data-ttu-id="ccb74-115">Questa proprietà si applica al controllo Media Player Windows solo se è incorporata in una pagina Web.</span><span class="sxs-lookup"><span data-stu-id="ccb74-115">This property applies to the Windows Media Player control only when it is embedded in a webpage.</span></span>

## <a name="requirements"></a><span data-ttu-id="ccb74-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ccb74-116">Requirements</span></span>



| <span data-ttu-id="ccb74-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="ccb74-117">Requirement</span></span> | <span data-ttu-id="ccb74-118">Valore</span><span class="sxs-lookup"><span data-stu-id="ccb74-118">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ccb74-119">Versione</span><span class="sxs-lookup"><span data-stu-id="ccb74-119">Version</span></span><br/>   | <span data-ttu-id="ccb74-120">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="ccb74-120">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="ccb74-121">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ccb74-121">Namespace</span></span><br/> | <span data-ttu-id="ccb74-122">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="ccb74-122">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="ccb74-123">Assembly</span><span class="sxs-lookup"><span data-stu-id="ccb74-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="ccb74-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="ccb74-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ccb74-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ccb74-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ccb74-126">**Oggetto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="ccb74-126">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





