---
title: Proprietà defaultAudioLanguage di IWMPSettings2
description: La proprietà defaultAudioLanguage Ottiene l'identificatore delle impostazioni locali (LCID) della lingua audio predefinita specificata in Windows Media Player.
ms.assetid: 4b7c9639-9d9f-4ed7-bb70-12cc608dd57a
keywords:
- Finestra delle proprietà di defaultAudioLanguage Media Player
- Proprietà di defaultAudioLanguage Media Player Windows, interfaccia IWMPSettings2
- Interfaccia IWMPSettings2 Windows Media Player, proprietà defaultAudioLanguage
topic_type:
- apiref
api_name:
- IWMPSettings2.defaultAudioLanguage
- IWMPSettings2.get_defaultAudioLanguage
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc7ac9120437005d9f32388e4d639d2d5893675e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327478"
---
# <a name="iwmpsettings2defaultaudiolanguage-property"></a><span data-ttu-id="5b865-106">IWMPSettings2::d proprietà efaultAudioLanguage</span><span class="sxs-lookup"><span data-stu-id="5b865-106">IWMPSettings2::defaultAudioLanguage property</span></span>

<span data-ttu-id="5b865-107">La proprietà **defaultAudioLanguage** Ottiene l'identificatore delle impostazioni locali (LCID) della lingua audio predefinita specificata in Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="5b865-107">The **defaultAudioLanguage** property gets the locale identifier (LCID) of the default audio language specified in Windows Media Player.</span></span>

<span data-ttu-id="5b865-108">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="5b865-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b865-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5b865-109">Syntax</span></span>


```CSharp
public System.Int32 defaultAudioLanguage {get;}
```


```VB

Public ReadOnly Property defaultAudioLanguage As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="5b865-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="5b865-110">Property value</span></span>

<span data-ttu-id="5b865-111">**System. Int32** che rappresenta l'identificatore LCID.</span><span class="sxs-lookup"><span data-stu-id="5b865-111">A **System.Int32** that is the LCID.</span></span>

## <a name="remarks"></a><span data-ttu-id="5b865-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="5b865-112">Remarks</span></span>

<span data-ttu-id="5b865-113">Un LCID identifica in modo univoco un dialetto di lingua particolare, denominato impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="5b865-113">An LCID uniquely identifies a particular language dialect, called a locale.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b865-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5b865-114">Requirements</span></span>



| <span data-ttu-id="5b865-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b865-115">Requirement</span></span> | <span data-ttu-id="5b865-116">Valore</span><span class="sxs-lookup"><span data-stu-id="5b865-116">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b865-117">Versione</span><span class="sxs-lookup"><span data-stu-id="5b865-117">Version</span></span><br/>   | <span data-ttu-id="5b865-118">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="5b865-118">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="5b865-119">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="5b865-119">Namespace</span></span><br/> | <span data-ttu-id="5b865-120">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="5b865-120">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="5b865-121">Assembly</span><span class="sxs-lookup"><span data-stu-id="5b865-121">Assembly</span></span><br/>  | <dl> <span data-ttu-id="5b865-122"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="5b865-122"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b865-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5b865-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b865-124">**IWMPControls3. currentAudioLanguage (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="5b865-124">**IWMPControls3.currentAudioLanguage (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguage--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="5b865-125">**Interfaccia IWMPSettings (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="5b865-125">**IWMPSettings Interface (VB and C#)**</span></span>](iwmpsettings--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="5b865-126">**Interfaccia IWMPSettings2 (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="5b865-126">**IWMPSettings2 Interface (VB and C#)**</span></span>](iwmpsettings2--vb-and-c.md)
</dt> </dl>

 

 





