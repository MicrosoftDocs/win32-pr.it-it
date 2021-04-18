---
title: Proprietà AxWindowsMediaPlayer. openState
description: La proprietà openState ottiene un valore di enumerazione che indica lo stato dell'origine del contenuto.
ms.assetid: 7a76814a-649f-4516-a92a-5f536fb1b147
keywords:
- Finestra delle proprietà di openState Media Player
- Proprietà openState Windows Media Player, classe AxWindowsMediaPlayer
- Classe AxWindowsMediaPlayer Media Player Windows, proprietà openState
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.openState
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 919bf906ce67793c4cd26f32892eae8acf441295
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325867"
---
# <a name="axwindowsmediaplayeropenstate-property"></a><span data-ttu-id="81892-106">Proprietà AxWindowsMediaPlayer. openState</span><span class="sxs-lookup"><span data-stu-id="81892-106">AxWindowsMediaPlayer.openState property</span></span>

<span data-ttu-id="81892-107">La proprietà openState ottiene un valore di enumerazione che indica lo stato dell'origine del contenuto.</span><span class="sxs-lookup"><span data-stu-id="81892-107">The openState property gets an enumeration value indicating the state of the content source.</span></span>

<span data-ttu-id="81892-108">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="81892-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="81892-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="81892-109">Syntax</span></span>


```CSharp
public WMPOpenState openState {get;}
```


```VB

Public ReadOnly Property openState As WMPOpenState
```





## <a name="property-value"></a><span data-ttu-id="81892-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="81892-110">Property value</span></span>

<span data-ttu-id="81892-111">Valore di enumerazione WMPLib. WMPOpenState.</span><span class="sxs-lookup"><span data-stu-id="81892-111">The WMPLib.WMPOpenState enumeration value.</span></span>

## <a name="remarks"></a><span data-ttu-id="81892-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="81892-112">Remarks</span></span>

<span data-ttu-id="81892-113">Non è garantito che gli Stati di Windows Media Player vengano eseguiti in un ordine particolare.</span><span class="sxs-lookup"><span data-stu-id="81892-113">Windows Media Player states are not guaranteed to occur in any particular order.</span></span> <span data-ttu-id="81892-114">Inoltre, non tutti gli Stati si verificano necessariamente durante una sequenza di eventi.</span><span class="sxs-lookup"><span data-stu-id="81892-114">Furthermore, not every state necessarily occurs during a sequence of events.</span></span> <span data-ttu-id="81892-115">Non è necessario scrivere codice che si basa sull'ordine di stato.</span><span class="sxs-lookup"><span data-stu-id="81892-115">You should not write code that relies upon state order.</span></span>

## <a name="requirements"></a><span data-ttu-id="81892-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="81892-116">Requirements</span></span>



| <span data-ttu-id="81892-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="81892-117">Requirement</span></span> | <span data-ttu-id="81892-118">Valore</span><span class="sxs-lookup"><span data-stu-id="81892-118">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81892-119">Versione</span><span class="sxs-lookup"><span data-stu-id="81892-119">Version</span></span><br/>   | <span data-ttu-id="81892-120">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="81892-120">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="81892-121">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="81892-121">Namespace</span></span><br/> | <span data-ttu-id="81892-122">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="81892-122">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="81892-123">Assembly</span><span class="sxs-lookup"><span data-stu-id="81892-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="81892-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="81892-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81892-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="81892-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81892-126">**Oggetto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="81892-126">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="81892-127">**Evento AxWindowsMediaPlayer. OpenStateChange**</span><span class="sxs-lookup"><span data-stu-id="81892-127">**AxWindowsMediaPlayer.OpenStateChange Event**</span></span>](axwmplib-axwindowsmediaplayer-openstatechange.md)
</dt> <dt>

[<span data-ttu-id="81892-128">**WMPLib. WMPOpenState**</span><span class="sxs-lookup"><span data-stu-id="81892-128">**WMPLib.WMPOpenState**</span></span>](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpopenstate)
</dt> </dl>

 

 





