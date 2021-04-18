---
title: Proprietà AxWindowsMediaPlayer. cdromCollection
description: La proprietà cdromcollection ottiene un'interfaccia IWMPCdromCollection che consente di accedere a una raccolta di unità CD o DVD.
ms.assetid: 03f4e7d1-4376-4112-993e-943d29aca049
keywords:
- Finestra delle proprietà di cdromcollection Media Player
- Proprietà di cdromcollection Media Player di Windows, classe AxWindowsMediaPlayer
- Classe AxWindowsMediaPlayer Windows Media Player, proprietà cdromcollection
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.cdromCollection
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac4ba3bb5df95e9ee53e2a6c3aecbd1e9a355882
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106323923"
---
# <a name="axwindowsmediaplayercdromcollection-property"></a><span data-ttu-id="c61c9-106">Proprietà AxWindowsMediaPlayer. cdromCollection</span><span class="sxs-lookup"><span data-stu-id="c61c9-106">AxWindowsMediaPlayer.cdromCollection property</span></span>

<span data-ttu-id="c61c9-107">La proprietà cdromcollection ottiene un'interfaccia **IWMPCdromCollection** che consente di accedere a una raccolta di unità CD o DVD.</span><span class="sxs-lookup"><span data-stu-id="c61c9-107">The cdromCollection property gets an **IWMPCdromCollection** interface that provides access to a collection of CD or DVD drives.</span></span>

<span data-ttu-id="c61c9-108">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="c61c9-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c61c9-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c61c9-109">Syntax</span></span>


```CSharp
public IWMPCdromCollection cdromCollection {get;}
```


```VB

Public ReadOnly Property cdromCollection As IWMPCdromCollection
```





## <a name="property-value"></a><span data-ttu-id="c61c9-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="c61c9-110">Property value</span></span>

<span data-ttu-id="c61c9-111">Interfaccia WMPLib. IWMPCdromCollection.</span><span class="sxs-lookup"><span data-stu-id="c61c9-111">A WMPLib.IWMPCdromCollection interface.</span></span>

## <a name="remarks"></a><span data-ttu-id="c61c9-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="c61c9-112">Remarks</span></span>

<span data-ttu-id="c61c9-113">Per recuperare il valore di questa proprietà, è necessario l'accesso in lettura alla libreria.</span><span class="sxs-lookup"><span data-stu-id="c61c9-113">To retrieve the value of this property, read access to the library is required.</span></span> <span data-ttu-id="c61c9-114">Per altre informazioni, vedere [accesso alla libreria](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="c61c9-114">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c61c9-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c61c9-115">Requirements</span></span>



| <span data-ttu-id="c61c9-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="c61c9-116">Requirement</span></span> | <span data-ttu-id="c61c9-117">Valore</span><span class="sxs-lookup"><span data-stu-id="c61c9-117">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c61c9-118">Versione</span><span class="sxs-lookup"><span data-stu-id="c61c9-118">Version</span></span><br/>   | <span data-ttu-id="c61c9-119">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="c61c9-119">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="c61c9-120">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="c61c9-120">Namespace</span></span><br/> | <span data-ttu-id="c61c9-121">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="c61c9-121">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="c61c9-122">Assembly</span><span class="sxs-lookup"><span data-stu-id="c61c9-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="c61c9-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="c61c9-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c61c9-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c61c9-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c61c9-125">**Oggetto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="c61c9-125">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="c61c9-126">**Interfaccia IWMPCdromCollection (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="c61c9-126">**IWMPCdromCollection Interface (VB and C#)**</span></span>](iwmpcdromcollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="c61c9-127">**IWMPSettings2. mediaAccessRights (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="c61c9-127">**IWMPSettings2.mediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="c61c9-128">**IWMPSettings2. requestMediaAccessRights (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="c61c9-128">**IWMPSettings2.requestMediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





