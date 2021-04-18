---
title: Evento DomainChange dell'oggetto AxWindowsMediaPlayer
description: L'evento DomainChange si verifica quando viene modificato il dominio DVD. | Evento DomainChange dell'oggetto AxWindowsMediaPlayer
ms.assetid: a080082e-1ba4-4080-b39c-b84292ecacb0
keywords:
- Evento DomainChange dell'oggetto AxWindowsMediaPlayer Media Player Windows
topic_type:
- apiref
api_name:
- DomainChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 342ac559f75c3bb7d65b442bfbdced5e5ed3f690
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331400"
---
# <a name="domainchange-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="677ed-105">Evento DomainChange dell'oggetto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="677ed-105">DomainChange Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="677ed-106">L'evento DomainChange si verifica quando viene modificato il dominio DVD.</span><span class="sxs-lookup"><span data-stu-id="677ed-106">The DomainChange event occurs when the DVD domain changes.</span></span>

``` syntax
[C#]
private void player_DomainChange(
  object sender,
  _WMPOCXEvents_DomainChangeEvent e
)

[Visual Basic]
Private Sub player_DomainChange(  
  sender As Object,
  e As _WMPOCXEvents_DomainChangeEvent
) Handles player.DomainChange
```

## <a name="event-data"></a><span data-ttu-id="677ed-107">Dati eventi</span><span class="sxs-lookup"><span data-stu-id="677ed-107">Event Data</span></span>

<span data-ttu-id="677ed-108">Il gestore associato a questo evento è di tipo **AxWMPLib. \_ \_DomainChangeEventHandler WMPOCXEvents**.</span><span class="sxs-lookup"><span data-stu-id="677ed-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_DomainChangeEventHandler**.</span></span> <span data-ttu-id="677ed-109">Questo gestore riceve un argomento di tipo **AxWMPLib. \_ WMPOCXEvents \_ DomainChangeEvent**, che contiene la proprietà seguente correlata a questo evento.</span><span class="sxs-lookup"><span data-stu-id="677ed-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_DomainChangeEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="677ed-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="677ed-110">Property</span></span>  | <span data-ttu-id="677ed-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="677ed-111">Description</span></span>                                                                                     |
|-----------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="677ed-112">strDomain</span><span class="sxs-lookup"><span data-stu-id="677ed-112">strDomain</span></span> | <span data-ttu-id="677ed-113">System. StringIndicates il nuovo dominio.</span><span class="sxs-lookup"><span data-stu-id="677ed-113">System.StringIndicates the new domain.</span></span> <span data-ttu-id="677ed-114">Per i valori possibili, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="677ed-114">For possible values, see the Remarks section.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="677ed-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="677ed-115">Remarks</span></span>

<span data-ttu-id="677ed-116">Nella tabella seguente vengono illustrati i valori possibili per la proprietà strDomain.</span><span class="sxs-lookup"><span data-stu-id="677ed-116">The following table shows the possible values for the strDomain property.</span></span>



| <span data-ttu-id="677ed-117">string</span><span class="sxs-lookup"><span data-stu-id="677ed-117">String</span></span>            | <span data-ttu-id="677ed-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="677ed-118">Description</span></span>                                                          |
|-------------------|----------------------------------------------------------------------|
| <span data-ttu-id="677ed-119">firstPlay</span><span class="sxs-lookup"><span data-stu-id="677ed-119">firstPlay</span></span>         | <span data-ttu-id="677ed-120">Esecuzione dell'inizializzazione predefinita di un disco DVD.</span><span class="sxs-lookup"><span data-stu-id="677ed-120">Performing default initialization of a DVD disc.</span></span>                     |
| <span data-ttu-id="677ed-121">videoManagerMenu</span><span class="sxs-lookup"><span data-stu-id="677ed-121">videoManagerMenu</span></span>  | <span data-ttu-id="677ed-122">Visualizzazione dei menu per l'intero disco. Noto anche come menu radice o menu di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="677ed-122">Displaying menus for whole disc. Also known as Root Menu or topMenu.</span></span> |
| <span data-ttu-id="677ed-123">videoTitleSetMenu</span><span class="sxs-lookup"><span data-stu-id="677ed-123">videoTitleSetMenu</span></span> | <span data-ttu-id="677ed-124">Visualizzazione dei menu per il set di titoli corrente.</span><span class="sxs-lookup"><span data-stu-id="677ed-124">Displaying menus for current title set.</span></span> <span data-ttu-id="677ed-125">Noto anche come titleMenu.</span><span class="sxs-lookup"><span data-stu-id="677ed-125">Also known as titleMenu.</span></span>     |
| <span data-ttu-id="677ed-126">title</span><span class="sxs-lookup"><span data-stu-id="677ed-126">title</span></span>             | <span data-ttu-id="677ed-127">Visualizzazione del titolo corrente.</span><span class="sxs-lookup"><span data-stu-id="677ed-127">Displaying the current title.</span></span>                                        |
| <span data-ttu-id="677ed-128">stop</span><span class="sxs-lookup"><span data-stu-id="677ed-128">stop</span></span>              | <span data-ttu-id="677ed-129">Il navigatore DVD si trova nel dominio di arresto DVD.</span><span class="sxs-lookup"><span data-stu-id="677ed-129">The DVD Navigator is in the DVD Stop domain.</span></span>                         |



 

## <a name="requirements"></a><span data-ttu-id="677ed-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="677ed-130">Requirements</span></span>



| <span data-ttu-id="677ed-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="677ed-131">Requirement</span></span> | <span data-ttu-id="677ed-132">Valore</span><span class="sxs-lookup"><span data-stu-id="677ed-132">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="677ed-133">Versione</span><span class="sxs-lookup"><span data-stu-id="677ed-133">Version</span></span><br/>   | <span data-ttu-id="677ed-134">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="677ed-134">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="677ed-135">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="677ed-135">Namespace</span></span><br/> | <span data-ttu-id="677ed-136">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="677ed-136">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="677ed-137">Assembly</span><span class="sxs-lookup"><span data-stu-id="677ed-137">Assembly</span></span><br/>  | <dl> <span data-ttu-id="677ed-138"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="677ed-138"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="677ed-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="677ed-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="677ed-140">**Oggetto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="677ed-140">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="677ed-141">**Interfaccia IWMPDVD (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="677ed-141">**IWMPDVD Interface (VB and C#)**</span></span>](iwmpdvd--vb-and-c.md)
</dt> </dl>

 

 





