---
title: Controllo CHECKBOX (compilatore di risorse)
description: Definisce un controllo casella di controllo.
ms.assetid: 24ee25e5-9de2-4843-a55e-96b897f6ae8e
keywords:
- Menu di controllo CHECKBOX e altre risorse
topic_type:
- apiref
api_name:
- CHECKBOX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57b4a86a2f08baf7d6e3af9960bd68db1eba86f1
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299684"
---
# <a name="checkbox-control"></a><span data-ttu-id="041a4-104">CHECKBOX (controllo)</span><span class="sxs-lookup"><span data-stu-id="041a4-104">CHECKBOX control</span></span>

<span data-ttu-id="041a4-105">Definisce un controllo casella di controllo.</span><span class="sxs-lookup"><span data-stu-id="041a4-105">Defines a check box control.</span></span> <span data-ttu-id="041a4-106">Il controllo è un rettangolo di piccole dimensioni (casella di controllo) a cui viene visualizzato il testo specificato (in genere, a destra).</span><span class="sxs-lookup"><span data-stu-id="041a4-106">The control is a small rectangle (check box) that has the specified text displayed next to it (typically, to the right).</span></span> <span data-ttu-id="041a4-107">Quando l'utente seleziona il controllo, il controllo evidenzia il rettangolo e invia un messaggio alla relativa finestra padre.</span><span class="sxs-lookup"><span data-stu-id="041a4-107">When the user selects the control, the control highlights the rectangle and sends a message to its parent window.</span></span>

<span data-ttu-id="041a4-108">L'istruzione **CheckBox** , che può essere utilizzata solo in un'istruzione [**DIALOGEX**](dialogex-resource.md) , definisce il testo, l'identificatore, le dimensioni e gli attributi del controllo.</span><span class="sxs-lookup"><span data-stu-id="041a4-108">The **CHECKBOX** statement, which can only be used in a [**DIALOGEX**](dialogex-resource.md) statement, defines the text, identifier, dimensions, and attributes of the control.</span></span>

``` syntax
CHECKBOX text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span data-ttu-id="041a4-109"><span id="text"></span><span id="TEXT"></span>*testo*</span><span class="sxs-lookup"><span data-stu-id="041a4-109"><span id="text"></span><span id="TEXT"></span>*text*</span></span>
</dt> <dd>

<span data-ttu-id="041a4-110">Testo da visualizzare a destra del controllo.</span><span class="sxs-lookup"><span data-stu-id="041a4-110">Text that is to be displayed to the right of the control.</span></span>

</dd> <dt>

<span data-ttu-id="041a4-111"><span id="style"></span><span id="STYLE"></span>*stile*</span><span class="sxs-lookup"><span data-stu-id="041a4-111"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="041a4-112">Stili del controllo.</span><span class="sxs-lookup"><span data-stu-id="041a4-112">Control styles.</span></span> <span data-ttu-id="041a4-113">Questo valore può essere una combinazione della **\_ casella** di controllo di stile della classe Button e degli stili **di \_ gruppo** **WS \_ TABSTOP** e WS.</span><span class="sxs-lookup"><span data-stu-id="041a4-113">This value can be a combination of the button class style **BS\_CHECKBOX** and the **WS\_TABSTOP** and **WS\_GROUP** styles.</span></span>

<span data-ttu-id="041a4-114">Se non si specifica uno stile, lo stile predefinito è `BS_CHECKBOX | WS_TABSTOP` .</span><span class="sxs-lookup"><span data-stu-id="041a4-114">If you do not specify a style, the default style is `BS_CHECKBOX | WS_TABSTOP`.</span></span>

</dd> </dl>

<span data-ttu-id="041a4-115">Per ulteriori informazioni sulla sintassi generale di un'istruzione di controllo, vedere [parametri di controllo comuni](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="041a4-115">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span>

## <a name="examples"></a><span data-ttu-id="041a4-116">Esempio</span><span class="sxs-lookup"><span data-stu-id="041a4-116">Examples</span></span>

<span data-ttu-id="041a4-117">Questo esempio definisce un controllo casella di controllo con etichetta corsivo:</span><span class="sxs-lookup"><span data-stu-id="041a4-117">This example defines a check-box control that is labeled Italic:</span></span>

``` syntax
CHECKBOX "Italic", 3, 10, 10, 40, 10
```

## <a name="see-also"></a><span data-ttu-id="041a4-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="041a4-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="041a4-119">**CASELLA di controllo AUTOCHECKBOX**</span><span class="sxs-lookup"><span data-stu-id="041a4-119">**AUTOCHECKBOX**</span></span>](autocheckbox-control.md)
</dt> <dt>

[<span data-ttu-id="041a4-120">**AUTO3STATE**</span><span class="sxs-lookup"><span data-stu-id="041a4-120">**AUTO3STATE**</span></span>](auto3state-control.md)
</dt> <dt>

[<span data-ttu-id="041a4-121">Caselle di controllo</span><span class="sxs-lookup"><span data-stu-id="041a4-121">Check Boxes</span></span>](https://www.bing.com/search?q=Check+Boxes)
</dt> <dt>

[<span data-ttu-id="041a4-122">**GetDialogBaseUnits**</span><span class="sxs-lookup"><span data-stu-id="041a4-122">**GetDialogBaseUnits**</span></span>](/windows/win32/api/winuser/nf-winuser-getdialogbaseunits)
</dt> <dt>

[<span data-ttu-id="041a4-123">**STATE3**</span><span class="sxs-lookup"><span data-stu-id="041a4-123">**STATE3**</span></span>](state3-control.md)
</dt> </dl>

 

 