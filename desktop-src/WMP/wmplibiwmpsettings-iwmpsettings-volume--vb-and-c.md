---
title: Proprietà volume IWMPSettings
description: La proprietà volume Ottiene o imposta il volume di riproduzione corrente.
ms.assetid: cff4fe70-9ca2-4419-bfc3-d622e8c72756
keywords:
- Proprietà volume Media Player Windows
- Proprietà volume Media Player Windows, interfaccia IWMPSettings
- Interfaccia IWMPSettings Windows Media Player, proprietà volume
topic_type:
- apiref
api_name:
- IWMPSettings.volume
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b21e50c9d3c52b7ce117d6c2ab681e592571c0f4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325962"
---
# <a name="iwmpsettingsvolume-property"></a><span data-ttu-id="b6c12-106">Proprietà IWMPSettings:: volume</span><span class="sxs-lookup"><span data-stu-id="b6c12-106">IWMPSettings::volume property</span></span>

<span data-ttu-id="b6c12-107">La proprietà **volume** Ottiene o imposta il volume di riproduzione corrente.</span><span class="sxs-lookup"><span data-stu-id="b6c12-107">The **volume** property gets or sets the current playback volume.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6c12-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b6c12-108">Syntax</span></span>


```CSharp
public System.Int32 volume {get; set;}
```


```VB

Public Property volume As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="b6c12-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="b6c12-109">Property value</span></span>

<span data-ttu-id="b6c12-110">**System. Int32** che rappresenta il livello del volume, compreso tra 0 e 100.</span><span class="sxs-lookup"><span data-stu-id="b6c12-110">A **System.Int32** that is the volume level, ranging from 0 to 100.</span></span>

## <a name="remarks"></a><span data-ttu-id="b6c12-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="b6c12-111">Remarks</span></span>

<span data-ttu-id="b6c12-112">Un valore pari a zero non specifica alcun volume (disattivato).</span><span class="sxs-lookup"><span data-stu-id="b6c12-112">A value of zero specifies no volume (muted).</span></span> <span data-ttu-id="b6c12-113">Il valore 100 specifica il volume completo.</span><span class="sxs-lookup"><span data-stu-id="b6c12-113">A value of 100 specifies full volume.</span></span> <span data-ttu-id="b6c12-114">Se per questa proprietà non viene specificato alcun valore, per impostazione predefinita viene impostata l'ultima impostazione del volume stabilita per Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="b6c12-114">If no value is specified for this property, it defaults to the last volume setting established for Windows Media Player.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6c12-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b6c12-115">Requirements</span></span>



| <span data-ttu-id="b6c12-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="b6c12-116">Requirement</span></span> | <span data-ttu-id="b6c12-117">Valore</span><span class="sxs-lookup"><span data-stu-id="b6c12-117">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6c12-118">Versione</span><span class="sxs-lookup"><span data-stu-id="b6c12-118">Version</span></span><br/>   | <span data-ttu-id="b6c12-119">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="b6c12-119">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="b6c12-120">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b6c12-120">Namespace</span></span><br/> | <span data-ttu-id="b6c12-121">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="b6c12-121">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="b6c12-122">Assembly</span><span class="sxs-lookup"><span data-stu-id="b6c12-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="b6c12-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="b6c12-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6c12-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b6c12-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6c12-125">**Interfaccia IWMPSettings (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="b6c12-125">**IWMPSettings Interface (VB and C#)**</span></span>](iwmpsettings--vb-and-c.md)
</dt> </dl>

 

 





