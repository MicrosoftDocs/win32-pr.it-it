---
title: Evento KeyPress dell'oggetto AxWindowsMediaPlayer
description: L'evento KeyPress si verifica quando un tasto viene premuto e rilasciato. | Evento KeyPress dell'oggetto AxWindowsMediaPlayer
ms.assetid: 73ecd6f9-1b58-4e28-ad1b-2d930a235e1d
keywords:
- Evento KeyPress dell'oggetto AxWindowsMediaPlayer Windows Media Player
topic_type:
- apiref
api_name:
- KeyPress Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4a01e84b8f765d024c753d08211f3bb84e7f011
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331888"
---
# <a name="keypress-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="8138d-105">Evento KeyPress dell'oggetto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="8138d-105">KeyPress Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="8138d-106">L'evento KeyPress si verifica quando un tasto viene premuto e rilasciato.</span><span class="sxs-lookup"><span data-stu-id="8138d-106">The KeyPress event occurs when a key is pressed and released.</span></span>

``` syntax
[C#]
private void player_KeyPressEvent(
  object sender,
  _WMPOCXEvents_KeyPressEvent e
)

[Visual Basic]
Private Sub player_KeyPressEvent(  
  sender As Object,  
  e As _WMPOCXEvents_KeyPressEvent
) Handles player.KeyPressEvent
```

## <a name="event-data"></a><span data-ttu-id="8138d-107">Dati eventi</span><span class="sxs-lookup"><span data-stu-id="8138d-107">Event Data</span></span>

<span data-ttu-id="8138d-108">Il gestore associato a questo evento è di tipo **AxWMPLib. \_ \_KeyPressEventHandler WMPOCXEvents**.</span><span class="sxs-lookup"><span data-stu-id="8138d-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_KeyPressEventHandler**.</span></span> <span data-ttu-id="8138d-109">Questo gestore riceve un argomento di tipo **AxWMPLib. \_ WMPOCXEvents \_ KeyPressEvent**, che contiene la proprietà seguente correlata a questo evento.</span><span class="sxs-lookup"><span data-stu-id="8138d-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_KeyPressEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="8138d-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="8138d-110">Property</span></span>      | <span data-ttu-id="8138d-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8138d-111">Description</span></span>                                                                        |
|---------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8138d-112">**nKeyAscii**</span><span class="sxs-lookup"><span data-stu-id="8138d-112">**nKeyAscii**</span></span> | <span data-ttu-id="8138d-113">System. Int16Specifies codice ANSI numerico standard per il carattere.</span><span class="sxs-lookup"><span data-stu-id="8138d-113">System.Int16Specifies the standard numeric ANSI code for the character.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="8138d-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="8138d-114">Remarks</span></span>

<span data-ttu-id="8138d-115">Questo evento si verifica quando la sequenza di tasti restituisce un carattere di tastiera stampabile, il tasto CTRL combinato con un carattere dell'alfabeto standard o uno dei caratteri speciali e il tasto invio o BACKSPACE.</span><span class="sxs-lookup"><span data-stu-id="8138d-115">This event occurs when the keystroke results in any printable keyboard character, the CTRL key combined with a character from the standard alphabet or one of a few special characters, and the ENTER or BACKSPACE key.</span></span>

## <a name="requirements"></a><span data-ttu-id="8138d-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8138d-116">Requirements</span></span>



| <span data-ttu-id="8138d-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="8138d-117">Requirement</span></span> | <span data-ttu-id="8138d-118">Valore</span><span class="sxs-lookup"><span data-stu-id="8138d-118">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8138d-119">Versione</span><span class="sxs-lookup"><span data-stu-id="8138d-119">Version</span></span><br/>   | <span data-ttu-id="8138d-120">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="8138d-120">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="8138d-121">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="8138d-121">Namespace</span></span><br/> | <span data-ttu-id="8138d-122">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="8138d-122">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="8138d-123">Assembly</span><span class="sxs-lookup"><span data-stu-id="8138d-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="8138d-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="8138d-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8138d-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8138d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8138d-126">**Oggetto AxWindowsMediaPlayer (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="8138d-126">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





