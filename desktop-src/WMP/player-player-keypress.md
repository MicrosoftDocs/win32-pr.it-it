---
title: Evento Player. KeyPress
description: L'evento KeyPress si verifica quando un tasto viene premuto e rilasciato. | Evento Player. KeyPress
ms.assetid: fc51dfd3-7968-464a-a4e2-669ffcb52a59
keywords:
- Media Player di eventi KeyPress Windows
- Evento KeyPress Media Player Windows, classe Player
- Classe Player Windows Media Player, evento KeyPress
topic_type:
- apiref
api_name:
- Player.KeyPress
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c78b72dd703c13019c71b23af53790aa974927f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326311"
---
# <a name="playerkeypress-event"></a><span data-ttu-id="43c64-107">Evento Player. KeyPress</span><span class="sxs-lookup"><span data-stu-id="43c64-107">Player.KeyPress event</span></span>

<span data-ttu-id="43c64-108">L'evento **KeyPress** si verifica quando un tasto viene premuto e rilasciato.</span><span class="sxs-lookup"><span data-stu-id="43c64-108">The **KeyPress** event occurs when a key is pressed and released.</span></span>

## <a name="syntax"></a><span data-ttu-id="43c64-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="43c64-109">Syntax</span></span>


```JScript
Player.KeyPress(
  nKeyAscii
)
```



## <a name="parameters"></a><span data-ttu-id="43c64-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="43c64-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43c64-111">*nKeyAscii*</span><span class="sxs-lookup"><span data-stu-id="43c64-111">*nKeyAscii*</span></span> 
</dt> <dd>

<span data-ttu-id="43c64-112">**Number** (**int**) che specifica il codice ANSI numerico standard per il carattere.</span><span class="sxs-lookup"><span data-stu-id="43c64-112">**Number** (**int**) specifying the standard numeric ANSI code for the character.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43c64-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="43c64-113">Return value</span></span>

<span data-ttu-id="43c64-114">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="43c64-114">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="43c64-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="43c64-115">Remarks</span></span>

<span data-ttu-id="43c64-116">Questo evento si verifica quando la sequenza di tasti restituisce un carattere di tastiera stampabile, il tasto CTRL combinato con un carattere dell'alfabeto standard o uno dei caratteri speciali e il tasto invio o BACKSPACE.</span><span class="sxs-lookup"><span data-stu-id="43c64-116">This event occurs when the keystroke results in any printable keyboard character, the CTRL key combined with a character from the standard alphabet or one of a few special characters, and the ENTER or BACKSPACE key.</span></span>

<span data-ttu-id="43c64-117">Il valore dei parametri evento viene specificato da Windows Media Player ed è possibile accedervi o passarli a un metodo in un file JScript importato usando il nome del parametro specificato.</span><span class="sxs-lookup"><span data-stu-id="43c64-117">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="43c64-118">Questo nome di parametro deve essere digitato esattamente come illustrato, incluse le maiuscole.</span><span class="sxs-lookup"><span data-stu-id="43c64-118">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="43c64-119">**Windows Media Player 10 Mobile:** Questo evento non è supportato.</span><span class="sxs-lookup"><span data-stu-id="43c64-119">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="43c64-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="43c64-120">Requirements</span></span>



| <span data-ttu-id="43c64-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="43c64-121">Requirement</span></span> | <span data-ttu-id="43c64-122">Valore</span><span class="sxs-lookup"><span data-stu-id="43c64-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="43c64-123">Versione</span><span class="sxs-lookup"><span data-stu-id="43c64-123">Version</span></span><br/> | <span data-ttu-id="43c64-124">Windows Media Player 9 serie o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="43c64-124">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="43c64-125">DLL</span><span class="sxs-lookup"><span data-stu-id="43c64-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="43c64-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="43c64-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43c64-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="43c64-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43c64-128">**Oggetto Player**</span><span class="sxs-lookup"><span data-stu-id="43c64-128">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





