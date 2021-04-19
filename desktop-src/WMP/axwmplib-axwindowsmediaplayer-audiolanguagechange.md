---
title: Evento AudioLanguageChange dell'oggetto AxWindowsMediaPlayer
description: L'evento AudioLanguageChange si verifica quando cambia la lingua audio corrente. | Evento AudioLanguageChange dell'oggetto AxWindowsMediaPlayer
ms.assetid: 35e4ff82-fc59-4d28-b7fc-1527fb46b960
keywords:
- Evento AudioLanguageChange dell'oggetto AxWindowsMediaPlayer Media Player Windows
topic_type:
- apiref
api_name:
- AudioLanguageChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 354a34f30df237827e3d369721963ec2c1797e71
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106323930"
---
# <a name="audiolanguagechange-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="ac93e-105">Evento AudioLanguageChange dell'oggetto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="ac93e-105">AudioLanguageChange Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="ac93e-106">L'evento AudioLanguageChange si verifica quando cambia la lingua audio corrente.</span><span class="sxs-lookup"><span data-stu-id="ac93e-106">The AudioLanguageChange event occurs when the current audio language changes.</span></span>

``` syntax
[C#]
private void player_AudioLanguageChange(
  object sender,
  _WMPOCXEvents_AudioLanguageChangeEvent e
)

[Visual Basic]
Private Sub player_AudioLanguageChange(
  sender As Object,
  e As _WMPOCXEvents_AudioLanguageChangeEvent
) Handles player.AudioLanguageChange
```

## <a name="event-data"></a><span data-ttu-id="ac93e-107">Dati eventi</span><span class="sxs-lookup"><span data-stu-id="ac93e-107">Event Data</span></span>

<span data-ttu-id="ac93e-108">Il gestore associato a questo evento è di tipo **AxWMPLib. \_ \_AudioLanguageChangeEventHandler WMPOCXEvents**.</span><span class="sxs-lookup"><span data-stu-id="ac93e-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_AudioLanguageChangeEventHandler**.</span></span> <span data-ttu-id="ac93e-109">Questo gestore riceve un argomento di tipo **AxWMPLib. \_ WMPOCXEvents \_ AudioLanguageChangeEvent**, che contiene la proprietà seguente correlata a questo evento.</span><span class="sxs-lookup"><span data-stu-id="ac93e-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_AudioLanguageChangeEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="ac93e-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ac93e-110">Property</span></span>   | <span data-ttu-id="ac93e-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ac93e-111">Description</span></span>                                                                                    |
|------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac93e-112">**langID**</span><span class="sxs-lookup"><span data-stu-id="ac93e-112">**langID**</span></span> | <span data-ttu-id="ac93e-113">**System. Int32** Identifica in modo univoco un dialetto di lingua particolare, denominato impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="ac93e-113">**System.Int32** Uniquely identifies a particular language dialect, called a locale.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ac93e-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="ac93e-114">Remarks</span></span>

<span data-ttu-id="ac93e-115">Un identificatore delle impostazioni locali (LCID) identifica in modo univoco un dialetto di lingua particolare, denominato impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="ac93e-115">A locale identifier (LCID) uniquely identifies a particular language dialect, called a locale.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac93e-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ac93e-116">Requirements</span></span>



| <span data-ttu-id="ac93e-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="ac93e-117">Requirement</span></span> | <span data-ttu-id="ac93e-118">Valore</span><span class="sxs-lookup"><span data-stu-id="ac93e-118">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac93e-119">Versione</span><span class="sxs-lookup"><span data-stu-id="ac93e-119">Version</span></span><br/>   | <span data-ttu-id="ac93e-120">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="ac93e-120">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="ac93e-121">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ac93e-121">Namespace</span></span><br/> | <span data-ttu-id="ac93e-122">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="ac93e-122">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="ac93e-123">Assembly</span><span class="sxs-lookup"><span data-stu-id="ac93e-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="ac93e-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="ac93e-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac93e-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ac93e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac93e-126">**Oggetto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="ac93e-126">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="ac93e-127">**IWMPControls3. currentAudioLanguage (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="ac93e-127">**IWMPControls3.currentAudioLanguage (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguage--vb-and-c.md)
</dt> </dl>

 

 





