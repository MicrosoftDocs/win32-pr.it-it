---
title: Proprietà di avvio automatico IWMPSettings
description: La proprietà AutoStart Ottiene o imposta un valore che indica se l'elemento multimediale corrente inizia la riproduzione automatica.
ms.assetid: 01a1cb78-9951-478a-8ea3-1ae06164beab
keywords:
- Finestra delle proprietà di avvio automatico Media Player
- Proprietà di avvio automatico Media Player Windows, interfaccia IWMPSettings
- Interfaccia IWMPSettings Windows Media Player, proprietà AutoStart
topic_type:
- apiref
api_name:
- IWMPSettings.autoStart
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aaf6c1fb43107df11462737286e26fa7801360d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330448"
---
# <a name="iwmpsettingsautostart-property"></a><span data-ttu-id="dc4b3-106">Proprietà IWMPSettings:: autostart</span><span class="sxs-lookup"><span data-stu-id="dc4b3-106">IWMPSettings::autoStart property</span></span>

<span data-ttu-id="dc4b3-107">La proprietà **autostart** Ottiene o imposta un valore che indica se l'elemento multimediale corrente inizia la riproduzione automatica.</span><span class="sxs-lookup"><span data-stu-id="dc4b3-107">The **autoStart** property gets or sets a value indicating whether the current media item begins playing automatically.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc4b3-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dc4b3-108">Syntax</span></span>


```CSharp
public System.Boolean autoStart {get; set;}
```


```VB

Public Property autoStart As System.Boolean
```





## <a name="property-value"></a><span data-ttu-id="dc4b3-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="dc4b3-109">Property value</span></span>

<span data-ttu-id="dc4b3-110">Valore **System. Boolean** che indica se l'elemento multimediale corrente inizia la riproduzione automatica.</span><span class="sxs-lookup"><span data-stu-id="dc4b3-110">A **System.Boolean** value that indicates whether the current media item begins playing automatically.</span></span> <span data-ttu-id="dc4b3-111">Il valore predefinito è **True**.</span><span class="sxs-lookup"><span data-stu-id="dc4b3-111">The default is **true**.</span></span>

## <a name="remarks"></a><span data-ttu-id="dc4b3-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="dc4b3-112">Remarks</span></span>

<span data-ttu-id="dc4b3-113">Se **autostart** è impostato su **true**, l'elemento multimediale inizierà a riprodurre quando viene impostato **AxWindowsMediaPlayer. URL**, **AxWindowsMediaPlayer. currentPlaylist** o **AxWindowsMediaPlayer. currentMedia** .</span><span class="sxs-lookup"><span data-stu-id="dc4b3-113">If **autoStart** is set to **true**, the media item will begin playing when **AxWindowsMediaPlayer.URL**, **AxWindowsMediaPlayer.currentPlaylist**, or **AxWindowsMediaPlayer.currentMedia** is set.</span></span> <span data-ttu-id="dc4b3-114">In caso contrario, l'elemento multimediale non inizierà a riprodurre fino a quando non viene chiamato il metodo **IWMPControls. Play** .</span><span class="sxs-lookup"><span data-stu-id="dc4b3-114">Otherwise, the media item will not start playing until the **IWMPControls.play** method is called.</span></span>

<span data-ttu-id="dc4b3-115">Se non si imposta **avvio automatico** su **true** immediatamente prima di specificare un elemento multimediale, è consigliabile non fare affidamento su questa impostazione come sostituto per l'utilizzo del metodo **IWMPControls. Play** .</span><span class="sxs-lookup"><span data-stu-id="dc4b3-115">Unless you set **autoStart** to **true** immediately before specifying a media item, you should not rely on this setting as a substitute for using the **IWMPControls.play** method.</span></span>

## <a name="requirements"></a><span data-ttu-id="dc4b3-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dc4b3-116">Requirements</span></span>



| <span data-ttu-id="dc4b3-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="dc4b3-117">Requirement</span></span> | <span data-ttu-id="dc4b3-118">Valore</span><span class="sxs-lookup"><span data-stu-id="dc4b3-118">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc4b3-119">Versione</span><span class="sxs-lookup"><span data-stu-id="dc4b3-119">Version</span></span><br/>   | <span data-ttu-id="dc4b3-120">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="dc4b3-120">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="dc4b3-121">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="dc4b3-121">Namespace</span></span><br/> | <span data-ttu-id="dc4b3-122">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="dc4b3-122">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="dc4b3-123">Assembly</span><span class="sxs-lookup"><span data-stu-id="dc4b3-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="dc4b3-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="dc4b3-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc4b3-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dc4b3-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc4b3-126">**AxWindowsMediaPlayer. currentMedia (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="dc4b3-126">**AxWindowsMediaPlayer.currentMedia (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="dc4b3-127">**AxWindowsMediaPlayer. currentPlaylist (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="dc4b3-127">**AxWindowsMediaPlayer.currentPlaylist (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-currentplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="dc4b3-128">**AxWindowsMediaPlayer. URL (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="dc4b3-128">**AxWindowsMediaPlayer.URL (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="dc4b3-129">**IWMPControls. Play (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="dc4b3-129">**IWMPControls.play (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-play--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="dc4b3-130">**Interfaccia IWMPSettings (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="dc4b3-130">**IWMPSettings Interface (VB and C#)**</span></span>](iwmpsettings--vb-and-c.md)
</dt> </dl>

 

 





