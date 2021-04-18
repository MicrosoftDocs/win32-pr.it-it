---
title: Proprietà AxWindowsMediaPlayer. mediacollection
description: La proprietà mediacollection ottiene un'interfaccia IWMPMediaCollection che fornisce un modo per organizzare una raccolta di elementi multimediali di grandi dimensioni.
ms.assetid: ec37e1da-a843-4b89-88fc-ec9255baa98a
keywords:
- Proprietà di mediacollection Media Player Windows
- Proprietà mediacollection Media Player Windows, classe AxWindowsMediaPlayer
- Classe AxWindowsMediaPlayer Windows Media Player, proprietà mediacollection
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.mediaCollection
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6501dd5dda8e60b8ba1a5f2667f6b581cbdfd90
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331879"
---
# <a name="axwindowsmediaplayermediacollection-property"></a><span data-ttu-id="8e20e-106">Proprietà AxWindowsMediaPlayer. mediacollection</span><span class="sxs-lookup"><span data-stu-id="8e20e-106">AxWindowsMediaPlayer.mediaCollection property</span></span>

<span data-ttu-id="8e20e-107">La proprietà mediacollection ottiene un'interfaccia **IWMPMediaCollection** che fornisce un modo per organizzare una raccolta di elementi multimediali di grandi dimensioni.</span><span class="sxs-lookup"><span data-stu-id="8e20e-107">The mediaCollection property gets an **IWMPMediaCollection** interface that provides a way to organize a large collection of media items.</span></span>

<span data-ttu-id="8e20e-108">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="8e20e-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e20e-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8e20e-109">Syntax</span></span>


```CSharp
public IWMPMediaCollection mediaCollection {get;}
```


```VB

Public ReadOnly Property mediaCollection As IWMPMediaCollection
```





## <a name="property-value"></a><span data-ttu-id="8e20e-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="8e20e-110">Property value</span></span>

<span data-ttu-id="8e20e-111">Interfaccia WMPLib. IWMPMediaCollection per una raccolta di elementi multimediali.</span><span class="sxs-lookup"><span data-stu-id="8e20e-111">The WMPLib.IWMPMediaCollection interface to a collection of media items.</span></span>

## <a name="remarks"></a><span data-ttu-id="8e20e-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="8e20e-112">Remarks</span></span>

<span data-ttu-id="8e20e-113">Per recuperare il valore di questa proprietà, è necessario l'accesso in lettura alla libreria.</span><span class="sxs-lookup"><span data-stu-id="8e20e-113">To retrieve the value of this property, read access to the library is required.</span></span> <span data-ttu-id="8e20e-114">Per altre informazioni, vedere [accesso alla libreria](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="8e20e-114">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8e20e-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8e20e-115">Requirements</span></span>



| <span data-ttu-id="8e20e-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="8e20e-116">Requirement</span></span> | <span data-ttu-id="8e20e-117">Valore</span><span class="sxs-lookup"><span data-stu-id="8e20e-117">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e20e-118">Versione</span><span class="sxs-lookup"><span data-stu-id="8e20e-118">Version</span></span><br/>   | <span data-ttu-id="8e20e-119">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="8e20e-119">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="8e20e-120">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="8e20e-120">Namespace</span></span><br/> | <span data-ttu-id="8e20e-121">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="8e20e-121">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="8e20e-122">Assembly</span><span class="sxs-lookup"><span data-stu-id="8e20e-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="8e20e-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="8e20e-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e20e-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8e20e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e20e-125">**Oggetto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="8e20e-125">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="8e20e-126">**Interfaccia IWMPMediaCollection (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="8e20e-126">**IWMPMediaCollection Interface (VB and C#)**</span></span>](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="8e20e-127">**IWMPSettings2. mediaAccessRights (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="8e20e-127">**IWMPSettings2.mediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="8e20e-128">**IWMPSettings2. requestMediaAccessRights (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="8e20e-128">**IWMPSettings2.requestMediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





