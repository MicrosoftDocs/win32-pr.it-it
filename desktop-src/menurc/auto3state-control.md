---
title: Controllo AUTO3STATE
description: Definisce una casella di controllo automatica a tre stati.
ms.assetid: 8b27367c-30d0-4591-93d0-756c65255b26
keywords:
- Menu di controllo di AUTO3STATE e altre risorse
topic_type:
- apiref
api_name:
- AUTO3STATE
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de184a639de7beee7ac05bdf63609ae29a0f034b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104117667"
---
# <a name="auto3state-control"></a><span data-ttu-id="460e7-104">Controllo AUTO3STATE</span><span class="sxs-lookup"><span data-stu-id="460e7-104">AUTO3STATE control</span></span>

<span data-ttu-id="460e7-105">Definisce una casella di controllo automatica a tre stati.</span><span class="sxs-lookup"><span data-stu-id="460e7-105">Defines an automatic three-state check box.</span></span> <span data-ttu-id="460e7-106">Il controllo è una casella aperta con il testo specificato posizionato a destra della casella.</span><span class="sxs-lookup"><span data-stu-id="460e7-106">The control is an open box with the given text positioned to the right of the box.</span></span> <span data-ttu-id="460e7-107">Quando viene scelto, la casella viene spostata automaticamente tra tre stati: selezionata, deselezionata e disabilitata (in grigio).</span><span class="sxs-lookup"><span data-stu-id="460e7-107">When chosen, the box automatically advances between three states: checked, unchecked, and disabled (grayed).</span></span> <span data-ttu-id="460e7-108">Il controllo Invia un messaggio al relativo elemento padre ogni volta che l'utente sceglie il controllo.</span><span class="sxs-lookup"><span data-stu-id="460e7-108">The control sends a message to its parent whenever the user chooses the control.</span></span>

``` syntax
AUTO3STATE text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span data-ttu-id="460e7-109"><span id="style"></span><span id="STYLE"></span>*stile*</span><span class="sxs-lookup"><span data-stu-id="460e7-109"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="460e7-110">Stili per il controllo, che può essere una combinazione dello stile **BS \_ AUTO3STATE** e degli stili seguenti: **WS \_ TABSTOP**, **WS \_ disabled** e **WS \_ Group**.</span><span class="sxs-lookup"><span data-stu-id="460e7-110">Styles for the control, which can be a combination of the **BS\_AUTO3STATE** style and the following styles: **WS\_TABSTOP**, **WS\_DISABLED**, and **WS\_GROUP**.</span></span>

<span data-ttu-id="460e7-111">Se non si specifica uno stile, lo stile predefinito è `BS_AUTO3STATE | WS_TABSTOP` .</span><span class="sxs-lookup"><span data-stu-id="460e7-111">If you do not specify a style, the default style is `BS_AUTO3STATE | WS_TABSTOP`.</span></span>

</dd> </dl>

<span data-ttu-id="460e7-112">Per ulteriori informazioni sulla sintassi generale di un'istruzione di controllo, vedere [parametri di controllo comuni](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="460e7-112">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="460e7-113">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="460e7-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="460e7-114">**CASELLA di controllo AUTOCHECKBOX**</span><span class="sxs-lookup"><span data-stu-id="460e7-114">**AUTOCHECKBOX**</span></span>](autocheckbox-control.md)
</dt> <dt>

[<span data-ttu-id="460e7-115">Caselle di controllo</span><span class="sxs-lookup"><span data-stu-id="460e7-115">Check Boxes</span></span>](https://www.bing.com/search?q=Check+Boxes)
</dt> <dt>

[<span data-ttu-id="460e7-116">**CASELLA**</span><span class="sxs-lookup"><span data-stu-id="460e7-116">**CHECKBOX**</span></span>](checkbox-control.md)
</dt> <dt>

[<span data-ttu-id="460e7-117">**CONTROLLO**</span><span class="sxs-lookup"><span data-stu-id="460e7-117">**CONTROL**</span></span>](control-control.md)
</dt> <dt>

[<span data-ttu-id="460e7-118">**STATE3**</span><span class="sxs-lookup"><span data-stu-id="460e7-118">**STATE3**</span></span>](state3-control.md)
</dt> <dt>

[<span data-ttu-id="460e7-119">Stili finestra</span><span class="sxs-lookup"><span data-stu-id="460e7-119">Window Styles</span></span>](/windows/desktop/winmsg/window-styles)
</dt> </dl>

 

 