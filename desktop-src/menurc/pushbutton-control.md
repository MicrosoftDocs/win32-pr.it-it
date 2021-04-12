---
title: Controllo pulsante (menu e altre risorse)
description: Definisce un controllo pulsante di comando. Il controllo è un rettangolo con angoli arrotondati che contiene il testo specificato. Il testo viene centrato nel controllo. Il controllo Invia un messaggio al relativo elemento padre ogni volta che l'utente sceglie il controllo.
ms.assetid: c5fbcfb7-1b7d-4199-acac-d11bfd899298
keywords:
- Menu di controllo pulsante e altre risorse
topic_type:
- apiref
api_name:
- PUSHBUTTON
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9a303121b7c0eee7ac57fc369164547bd3ae6b9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104337470"
---
# <a name="pushbutton-control"></a><span data-ttu-id="4765d-107">Controllo pulsante</span><span class="sxs-lookup"><span data-stu-id="4765d-107">PUSHBUTTON control</span></span>

<span data-ttu-id="4765d-108">Definisce un controllo pulsante di comando.</span><span class="sxs-lookup"><span data-stu-id="4765d-108">Defines a push-button control.</span></span> <span data-ttu-id="4765d-109">Il controllo è un rettangolo con angoli arrotondati che contiene il testo specificato.</span><span class="sxs-lookup"><span data-stu-id="4765d-109">The control is a round-cornered rectangle containing the given text.</span></span> <span data-ttu-id="4765d-110">Il testo viene centrato nel controllo.</span><span class="sxs-lookup"><span data-stu-id="4765d-110">The text is centered in the control.</span></span> <span data-ttu-id="4765d-111">Il controllo Invia un messaggio al relativo elemento padre ogni volta che l'utente sceglie il controllo.</span><span class="sxs-lookup"><span data-stu-id="4765d-111">The control sends a message to its parent whenever the user chooses the control.</span></span>

``` syntax
PUSHBUTTON text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span data-ttu-id="4765d-112"><span id="style"></span><span id="STYLE"></span>*stile*</span><span class="sxs-lookup"><span data-stu-id="4765d-112"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="4765d-113">Stili per il pulsante, che può essere una combinazione dello stile **del \_ pulsante BS** e degli stili seguenti: **WS \_ TABSTOP**, **WS \_ disabled** e **WS \_ Group**.</span><span class="sxs-lookup"><span data-stu-id="4765d-113">Styles for the pushbutton, which can be a combination of the **BS\_PUSHBUTTON** style and the following styles: **WS\_TABSTOP**, **WS\_DISABLED**, and **WS\_GROUP**.</span></span>

<span data-ttu-id="4765d-114">Se non si specifica uno stile, lo stile predefinito è `BS_PUSHBUTTON | WS_TABSTOP` .</span><span class="sxs-lookup"><span data-stu-id="4765d-114">If you do not specify a style, the default style is `BS_PUSHBUTTON | WS_TABSTOP`.</span></span>

</dd> </dl>

<span data-ttu-id="4765d-115">Per ulteriori informazioni sulla sintassi generale di un'istruzione di controllo, vedere [parametri di controllo comuni](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="4765d-115">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span>

## <a name="examples"></a><span data-ttu-id="4765d-116">Esempio</span><span class="sxs-lookup"><span data-stu-id="4765d-116">Examples</span></span>

<span data-ttu-id="4765d-117">Nell'esempio seguente viene illustrato l'utilizzo dell'istruzione **pulsante** :</span><span class="sxs-lookup"><span data-stu-id="4765d-117">The following example demonstrates the use of the **PUSHBUTTON** statement:</span></span>

``` syntax
PUSHBUTTON "ON", 7, 10, 10, 20, 10
```

## <a name="see-also"></a><span data-ttu-id="4765d-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4765d-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4765d-119">**GetDialogBaseUnits**</span><span class="sxs-lookup"><span data-stu-id="4765d-119">**GetDialogBaseUnits**</span></span>](/windows/win32/api/winuser/nf-winuser-getdialogbaseunits)
</dt> <dt>

[<span data-ttu-id="4765d-120">Pulsanti di push</span><span class="sxs-lookup"><span data-stu-id="4765d-120">Push Buttons</span></span>](https://www.bing.com/search?q=Push+Buttons)
</dt> </dl>

 

 