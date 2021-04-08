---
title: RADIOBUTTON (controllo)
description: Definisce un controllo pulsante di opzione.
ms.assetid: c427080f-0408-42b4-8888-7333f3eb985d
keywords:
- Menu di controllo RADIOBUTTON e altre risorse
topic_type:
- apiref
api_name:
- RADIOBUTTON
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67dd559c2d61ca8b2735d393170c177a65735b4b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104046743"
---
# <a name="radiobutton-control"></a><span data-ttu-id="bc238-104">RADIOBUTTON (controllo)</span><span class="sxs-lookup"><span data-stu-id="bc238-104">RADIOBUTTON control</span></span>

<span data-ttu-id="bc238-105">Definisce un controllo pulsante di opzione.</span><span class="sxs-lookup"><span data-stu-id="bc238-105">Defines a radio-button control.</span></span> <span data-ttu-id="bc238-106">Il controllo è un piccolo cerchio a cui è visualizzato il testo specificato, in genere a destra.</span><span class="sxs-lookup"><span data-stu-id="bc238-106">The control is a small circle that has the given text displayed next to it, typically to its right.</span></span> <span data-ttu-id="bc238-107">Il controllo evidenzia il cerchio e invia un messaggio alla relativa finestra padre quando l'utente seleziona il pulsante.</span><span class="sxs-lookup"><span data-stu-id="bc238-107">The control highlights the circle and sends a message to its parent window when the user selects the button.</span></span> <span data-ttu-id="bc238-108">Il controllo rimuove l'evidenziazione e invia un messaggio quando viene selezionato il pulsante Avanti.</span><span class="sxs-lookup"><span data-stu-id="bc238-108">The control removes the highlight and sends a message when the button is next selected.</span></span>

``` syntax
RADIOBUTTON text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span data-ttu-id="bc238-109"><span id="style"></span><span id="STYLE"></span>*stile*</span><span class="sxs-lookup"><span data-stu-id="bc238-109"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="bc238-110">Stili per il pulsante di opzione, che può essere una combinazione di stili di classi di pulsanti e gli stili seguenti: **WS \_ TABSTOP**, **WS \_ disabled** e **WS \_ Group**.</span><span class="sxs-lookup"><span data-stu-id="bc238-110">Styles for the radio button, which can be a combination of BUTTON-class styles and the following styles: **WS\_TABSTOP**, **WS\_DISABLED**, and **WS\_GROUP**.</span></span>

<span data-ttu-id="bc238-111">Se non si specifica uno stile, lo stile predefinito è `BS_RADIOBUTTON | WS_TABSTOP` .</span><span class="sxs-lookup"><span data-stu-id="bc238-111">If you do not specify a style, the default style is `BS_RADIOBUTTON | WS_TABSTOP`.</span></span>

</dd> </dl>

<span data-ttu-id="bc238-112">Per ulteriori informazioni sulla sintassi generale di un'istruzione di controllo, vedere [parametri di controllo comuni](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="bc238-112">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span>

## <a name="examples"></a><span data-ttu-id="bc238-113">Esempio</span><span class="sxs-lookup"><span data-stu-id="bc238-113">Examples</span></span>

<span data-ttu-id="bc238-114">Nell'esempio seguente viene illustrato l'utilizzo dell'istruzione **RadioButton** :</span><span class="sxs-lookup"><span data-stu-id="bc238-114">The following example demonstrates the use of the **RADIOBUTTON** statement:</span></span>

``` syntax
RADIOBUTTON "Italic", 100, 10, 10, 40, 10
```

## <a name="see-also"></a><span data-ttu-id="bc238-115">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bc238-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc238-116">**GetDialogBaseUnits**</span><span class="sxs-lookup"><span data-stu-id="bc238-116">**GetDialogBaseUnits**</span></span>](/windows/win32/api/winuser/nf-winuser-getdialogbaseunits)
</dt> <dt>

[<span data-ttu-id="bc238-117">Pulsanti di opzione</span><span class="sxs-lookup"><span data-stu-id="bc238-117">Radio Buttons</span></span>](https://www.bing.com/search?q=Radio+Buttons)
</dt> </dl>

 

 