---
title: Stili della descrizione comando (CommCtrl. h)
description: Questa sezione elenca gli stili di controllo usati con i controlli ToolTip.
ms.assetid: a6aeac71-6a69-4903-af78-0bfe1f83e632
topic_type:
- apiref
api_name:
- TTS_ALWAYSTIP
- TTS_BALLOON
- TTS_CLOSE
- TTS_NOANIMATE
- TTS_NOFADE
- TTS_NOPREFIX
- TTS_USEVISUALSTYLE
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff8b89aed88caddceae815414b9f2b4d93a550c5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326842"
---
# <a name="tooltip-styles"></a><span data-ttu-id="a406f-103">Stili descrizione comando</span><span class="sxs-lookup"><span data-stu-id="a406f-103">Tooltip Styles</span></span>

<span data-ttu-id="a406f-104">Questa sezione elenca gli stili di controllo usati con i controlli ToolTip.</span><span class="sxs-lookup"><span data-stu-id="a406f-104">This section lists the control styles used with tooltip controls.</span></span>



| <span data-ttu-id="a406f-105">Costante</span><span class="sxs-lookup"><span data-stu-id="a406f-105">Constant</span></span>                                                                                                                                                                     | <span data-ttu-id="a406f-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a406f-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                                       |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TTS_ALWAYSTIP"></span><span id="tts_alwaystip"></span><dl> <span data-ttu-id="a406f-107"><dt>**\_ALWAYSTIP TTS**</dt></span><span class="sxs-lookup"><span data-stu-id="a406f-107"><dt>**TTS\_ALWAYSTIP**</dt></span></span> </dl>                | <span data-ttu-id="a406f-108">Indica che il controllo ToolTip viene visualizzato quando il cursore si trova in uno strumento, anche se la finestra proprietaria del controllo ToolTip è inattiva.</span><span class="sxs-lookup"><span data-stu-id="a406f-108">Indicates that the tooltip control appears when the cursor is on a tool, even if the tooltip control's owner window is inactive.</span></span> <span data-ttu-id="a406f-109">Senza questo stile, la descrizione comando viene visualizzata solo quando la finestra proprietaria dello strumento è attiva.</span><span class="sxs-lookup"><span data-stu-id="a406f-109">Without this style, the tooltip appears only when the tool's owner window is active.</span></span><br/>                                                                                                                                  |
| <span id="TTS_BALLOON"></span><span id="tts_balloon"></span><dl> <span data-ttu-id="a406f-110"><dt>**\_fumetto TTS**</dt></span><span class="sxs-lookup"><span data-stu-id="a406f-110"><dt>**TTS\_BALLOON**</dt></span></span> </dl>                      | <span data-ttu-id="a406f-111">[Versione 5,80](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="a406f-111">[Version 5.80](common-control-versions.md).</span></span> <span data-ttu-id="a406f-112">Indica che il controllo ToolTip ha l'aspetto di un fumetto "Balloon", con angoli arrotondati e un gambo che punta all'elemento.</span><span class="sxs-lookup"><span data-stu-id="a406f-112">Indicates that the tooltip control has the appearance of a cartoon "balloon," with rounded corners and a stem pointing to the item.</span></span> <br/>                                                                                                                                                                      |
| <span id="TTS_CLOSE"></span><span id="tts_close"></span><dl> <span data-ttu-id="a406f-113"><dt>**TTS \_ chiuso**</dt></span><span class="sxs-lookup"><span data-stu-id="a406f-113"><dt>**TTS\_CLOSE**</dt></span></span> </dl>                            | <span data-ttu-id="a406f-114">Visualizza un pulsante **Chiudi** nella descrizione comando.</span><span class="sxs-lookup"><span data-stu-id="a406f-114">Displays a **Close** button on the tooltip.</span></span> <span data-ttu-id="a406f-115">Valido solo quando la descrizione comando ha lo \_ stile e un titolo del fumetto TTS; vedere [**\_ TTM**](ttm-settitle.md).</span><span class="sxs-lookup"><span data-stu-id="a406f-115">Valid only when the tooltip has the TTS\_BALLOON style and a title; see [**TTM\_SETTITLE**](ttm-settitle.md).</span></span><br/>                                                                                                                                                                                             |
| <span id="TTS_NOANIMATE"></span><span id="tts_noanimate"></span><dl> <span data-ttu-id="a406f-116"><dt>**TTS \_ NOanimate**</dt></span><span class="sxs-lookup"><span data-stu-id="a406f-116"><dt>**TTS\_NOANIMATE**</dt></span></span> </dl>                | <span data-ttu-id="a406f-117">[Versione 5,80](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="a406f-117">[Version 5.80](common-control-versions.md).</span></span> <span data-ttu-id="a406f-118">Disabilita l'animazione scorrevole della descrizione comando nei sistemi Windows 98 e Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="a406f-118">Disables sliding tooltip animation on Windows 98 and Windows 2000 systems.</span></span> <span data-ttu-id="a406f-119">Questo stile viene ignorato nei sistemi precedenti.</span><span class="sxs-lookup"><span data-stu-id="a406f-119">This style is ignored on earlier systems.</span></span><br/>                                                                                                                                                                                      |
| <span id="TTS_NOFADE"></span><span id="tts_nofade"></span><dl> <span data-ttu-id="a406f-120"><dt>**TTS \_ NOfade**</dt></span><span class="sxs-lookup"><span data-stu-id="a406f-120"><dt>**TTS\_NOFADE**</dt></span></span> </dl>                         | <span data-ttu-id="a406f-121">[Versione 5,80](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="a406f-121">[Version 5.80](common-control-versions.md).</span></span> <span data-ttu-id="a406f-122">Disabilita l'animazione della descrizione comando dissolvenza.</span><span class="sxs-lookup"><span data-stu-id="a406f-122">Disables fading tooltip animation.</span></span> <br/>                                                                                                                                                                                                                                                                       |
| <span id="TTS_NOPREFIX"></span><span id="tts_noprefix"></span><dl> <span data-ttu-id="a406f-123"><dt>**\_prefisso TTS**</dt></span><span class="sxs-lookup"><span data-stu-id="a406f-123"><dt>**TTS\_NOPREFIX**</dt></span></span> </dl>                   | <span data-ttu-id="a406f-124">Impedisce al sistema di estrarre i caratteri e commerciale da una stringa o di terminare una stringa in corrispondenza di un carattere di tabulazione.</span><span class="sxs-lookup"><span data-stu-id="a406f-124">Prevents the system from stripping ampersand characters from a string or terminating a string at a tab character.</span></span> <span data-ttu-id="a406f-125">Senza questo stile, il sistema rimuove automaticamente i caratteri e e termina una stringa in corrispondenza del primo carattere di tabulazione.</span><span class="sxs-lookup"><span data-stu-id="a406f-125">Without this style, the system automatically strips ampersand characters and terminates a string at the first tab character.</span></span> <span data-ttu-id="a406f-126">Questo consente a un'applicazione di usare la stessa stringa sia come voce di menu che come testo in un controllo ToolTip.</span><span class="sxs-lookup"><span data-stu-id="a406f-126">This allows an application to use the same string as both a menu item and as text in a tooltip control.</span></span><br/> |
| <span id="TTS_USEVISUALSTYLE"></span><span id="tts_usevisualstyle"></span><dl> <span data-ttu-id="a406f-127"><dt>**\_USEVISUALSTYLE TTS**</dt></span><span class="sxs-lookup"><span data-stu-id="a406f-127"><dt>**TTS\_USEVISUALSTYLE**</dt></span></span> </dl> | <span data-ttu-id="a406f-128">Usa collegamenti ipertestuali con tema.</span><span class="sxs-lookup"><span data-stu-id="a406f-128">Uses themed hyperlinks.</span></span> <span data-ttu-id="a406f-129">Il tema definisce gli stili per tutti i collegamenti nella descrizione comando.</span><span class="sxs-lookup"><span data-stu-id="a406f-129">The theme will define the styles for any links in the tooltip.</span></span> <span data-ttu-id="a406f-130">Per questo stile è sempre necessario \_ impostare ttf PARSELINKS.</span><span class="sxs-lookup"><span data-stu-id="a406f-130">This style always requires TTF\_PARSELINKS to be set.</span></span> <br/>                                                                                                                                                                                                          |



## <a name="remarks"></a><span data-ttu-id="a406f-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="a406f-131">Remarks</span></span>

<span data-ttu-id="a406f-132">Un controllo ToolTip presenta sempre gli \_ stili della finestra WS popup e WS \_ ex \_ TOOLWINDOW, indipendentemente dal fatto che vengano specificati quando si crea il controllo.</span><span class="sxs-lookup"><span data-stu-id="a406f-132">A tooltip control always has the WS\_POPUP and WS\_EX\_TOOLWINDOW window styles, regardless of whether you specify them when creating the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="a406f-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a406f-133">Requirements</span></span>



| <span data-ttu-id="a406f-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="a406f-134">Requirement</span></span> | <span data-ttu-id="a406f-135">Valore</span><span class="sxs-lookup"><span data-stu-id="a406f-135">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a406f-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a406f-136">Header</span></span><br/> | <dl> <span data-ttu-id="a406f-137"><dt>CommCtrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a406f-137"><dt>CommCtrl.h</dt></span></span> </dl> |



 

 





