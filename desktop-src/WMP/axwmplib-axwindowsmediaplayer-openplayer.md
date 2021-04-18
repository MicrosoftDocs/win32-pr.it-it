---
title: AxWindowsMediaPlayer. openPlayer, metodo
description: Il metodo openPlayer apre Windows Media Player usando l'URL specificato. | AxWindowsMediaPlayer. openPlayer, metodo
ms.assetid: 9a9d8200-f427-42ff-b49f-d973cf86014f
keywords:
- Metodo openPlayer Windows Media Player
- Metodo openPlayer Windows Media Player, classe AxWindowsMediaPlayer
- Classe AxWindowsMediaPlayer Windows Media Player, metodo openPlayer
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.openPlayer
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58416a1f20969b0bd223f653f44b5633f19cb096
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325873"
---
# <a name="axwindowsmediaplayeropenplayer-method"></a><span data-ttu-id="b1e8c-107">AxWindowsMediaPlayer. openPlayer, metodo</span><span class="sxs-lookup"><span data-stu-id="b1e8c-107">AxWindowsMediaPlayer.openPlayer method</span></span>

<span data-ttu-id="b1e8c-108">Il metodo **openPlayer** apre Windows Media Player usando l'URL specificato.</span><span class="sxs-lookup"><span data-stu-id="b1e8c-108">The **openPlayer** method opens Windows Media Player using the specified URL.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1e8c-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b1e8c-109">Syntax</span></span>


```CSharp
public void openPlayer(
  System.String bstrURL
);
```


```VB

Public Sub openPlayer( _
  ByVal bstrURL As System.String _
)
```





## <a name="parameters"></a><span data-ttu-id="b1e8c-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="b1e8c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1e8c-111">*bstrURL*</span><span class="sxs-lookup"><span data-stu-id="b1e8c-111">*bstrURL*</span></span> 
</dt> <dd>

<span data-ttu-id="b1e8c-112">**System. String** che rappresenta l'URL dell'elemento multimediale da riprodurre.</span><span class="sxs-lookup"><span data-stu-id="b1e8c-112">The **System.String** that is the URL of the media item to play.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1e8c-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b1e8c-113">Return value</span></span>

<span data-ttu-id="b1e8c-114">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="b1e8c-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b1e8c-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="b1e8c-115">Remarks</span></span>

<span data-ttu-id="b1e8c-116">Questo metodo avvia Media Player Windows con l'URL specificato impostato come elemento multimediale corrente.</span><span class="sxs-lookup"><span data-stu-id="b1e8c-116">This method launches Windows Media Player with the specified URL set as the current media item.</span></span> <span data-ttu-id="b1e8c-117">Se il lettore è stato chiuso in precedenza in modalità Skin, verrà aperto utilizzando l'ultima interfaccia selezionata dall'utente.</span><span class="sxs-lookup"><span data-stu-id="b1e8c-117">If the Player was previously closed in skin mode it will open using the skin last chosen by the user.</span></span> <span data-ttu-id="b1e8c-118">In caso contrario, il lettore verrà aperto in modalità completa.</span><span class="sxs-lookup"><span data-stu-id="b1e8c-118">Otherwise, the Player opens in full mode.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1e8c-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b1e8c-119">Requirements</span></span>



| <span data-ttu-id="b1e8c-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="b1e8c-120">Requirement</span></span> | <span data-ttu-id="b1e8c-121">Valore</span><span class="sxs-lookup"><span data-stu-id="b1e8c-121">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1e8c-122">Versione</span><span class="sxs-lookup"><span data-stu-id="b1e8c-122">Version</span></span><br/>   | <span data-ttu-id="b1e8c-123">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="b1e8c-123">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="b1e8c-124">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b1e8c-124">Namespace</span></span><br/> | <span data-ttu-id="b1e8c-125">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="b1e8c-125">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="b1e8c-126">Assembly</span><span class="sxs-lookup"><span data-stu-id="b1e8c-126">Assembly</span></span><br/>  | <dl> <span data-ttu-id="b1e8c-127"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="b1e8c-127"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1e8c-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b1e8c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1e8c-129">**Oggetto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="b1e8c-129">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





