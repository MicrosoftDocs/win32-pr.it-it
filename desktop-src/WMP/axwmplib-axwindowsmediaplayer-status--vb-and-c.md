---
title: Proprietà AxWindowsMediaPlayer. status
description: La proprietà Status ottiene un valore che indica lo stato di Windows Media Player.
ms.assetid: fefed54d-1fae-4599-8efc-eb2efdbd8ebd
keywords:
- Finestra Proprietà stato Media Player
- Proprietà di stato Windows Media Player, classe AxWindowsMediaPlayer
- Classe AxWindowsMediaPlayer Media Player Windows, proprietà Status
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.status
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ea7e8c36ad05e2f9a4573d8e2433d705f354239
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328303"
---
# <a name="axwindowsmediaplayerstatus-property"></a><span data-ttu-id="1bdb6-106">Proprietà AxWindowsMediaPlayer. status</span><span class="sxs-lookup"><span data-stu-id="1bdb6-106">AxWindowsMediaPlayer.status property</span></span>

<span data-ttu-id="1bdb6-107">La proprietà Status ottiene un valore che indica lo stato di Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="1bdb6-107">The status property gets a value indicating the status of Windows Media Player.</span></span>

<span data-ttu-id="1bdb6-108">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="1bdb6-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="1bdb6-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1bdb6-109">Syntax</span></span>


```CSharp
public System.String status {get;}
```


```VB

Public ReadOnly Property status As System.String
```





## <a name="property-value"></a><span data-ttu-id="1bdb6-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="1bdb6-110">Property value</span></span>

<span data-ttu-id="1bdb6-111">System. String che rappresenta lo stato.</span><span class="sxs-lookup"><span data-stu-id="1bdb6-111">The System.String that is the status.</span></span>

## <a name="remarks"></a><span data-ttu-id="1bdb6-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="1bdb6-112">Remarks</span></span>

<span data-ttu-id="1bdb6-113">I valori contenuti in questa proprietà sono soggetti a modifiche in qualsiasi momento e devono essere utilizzati solo a scopo di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="1bdb6-113">The values contained in this property are subject to change at any time, and should be used for display purposes only.</span></span>

<span data-ttu-id="1bdb6-114">AxWindowsMediaPlayer. L'evento **StatusChange** viene generato ogni volta che questa proprietà cambia valore.</span><span class="sxs-lookup"><span data-stu-id="1bdb6-114">The AxWindowsMediaPlayer.**StatusChange** event is fired whenever this property changes value.</span></span>

## <a name="requirements"></a><span data-ttu-id="1bdb6-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1bdb6-115">Requirements</span></span>



| <span data-ttu-id="1bdb6-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="1bdb6-116">Requirement</span></span> | <span data-ttu-id="1bdb6-117">Valore</span><span class="sxs-lookup"><span data-stu-id="1bdb6-117">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1bdb6-118">Versione</span><span class="sxs-lookup"><span data-stu-id="1bdb6-118">Version</span></span><br/>   | <span data-ttu-id="1bdb6-119">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="1bdb6-119">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="1bdb6-120">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="1bdb6-120">Namespace</span></span><br/> | <span data-ttu-id="1bdb6-121">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="1bdb6-121">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="1bdb6-122">Assembly</span><span class="sxs-lookup"><span data-stu-id="1bdb6-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="1bdb6-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="1bdb6-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1bdb6-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1bdb6-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1bdb6-125">**Oggetto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="1bdb6-125">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="1bdb6-126">**Evento AxWindowsMediaPlayer. StatusChange (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="1bdb6-126">**AxWindowsMediaPlayer.StatusChange Event (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-statuschange.md)
</dt> </dl>

 

 





