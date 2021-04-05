---
title: Controllo AUTOCHECKBOX
description: Definisce un controllo casella di controllo automatico.
ms.assetid: 086f5dd3-267f-4ec6-be37-4e9402f7aede
keywords:
- Menu di controllo AUTOCHECKBOX e altre risorse
topic_type:
- apiref
api_name:
- AUTOCHECKBOX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 842bb3ede2b1f96f3e5b343e351e047d112a8403
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725559"
---
# <a name="autocheckbox-control"></a><span data-ttu-id="61d20-104">Controllo AUTOCHECKBOX</span><span class="sxs-lookup"><span data-stu-id="61d20-104">AUTOCHECKBOX control</span></span>

<span data-ttu-id="61d20-105">Definisce un controllo casella di controllo automatico.</span><span class="sxs-lookup"><span data-stu-id="61d20-105">Defines an automatic check box control.</span></span> <span data-ttu-id="61d20-106">Il controllo è un rettangolo di piccole dimensioni (casella di controllo) a cui viene visualizzato il testo specificato (in genere, a destra).</span><span class="sxs-lookup"><span data-stu-id="61d20-106">The control is a small rectangle (check box) that has the specified text displayed next to it (typically, to the right).</span></span> <span data-ttu-id="61d20-107">Quando l'utente sceglie il controllo, il controllo evidenzia il rettangolo e invia un messaggio alla relativa finestra padre.</span><span class="sxs-lookup"><span data-stu-id="61d20-107">When the user chooses the control, the control highlights the rectangle and sends a message to its parent window.</span></span>

<span data-ttu-id="61d20-108">L'istruzione **AUTOCHECKBOX** può essere utilizzata solo nel corpo di una [**finestra di dialogo**](dialog-resource.md) o di un'istruzione [**DIALOGEX**](dialogex-resource.md) .</span><span class="sxs-lookup"><span data-stu-id="61d20-108">The **AUTOCHECKBOX** statement can only be used in the body of a [**DIALOG**](dialog-resource.md) or [**DIALOGEX**](dialogex-resource.md) statement.</span></span>

``` syntax
AUTOCHECKBOX text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span data-ttu-id="61d20-109"><span id="style"></span><span id="STYLE"></span>*stile*</span><span class="sxs-lookup"><span data-stu-id="61d20-109"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="61d20-110">Stili del controllo.</span><span class="sxs-lookup"><span data-stu-id="61d20-110">Styles of the control.</span></span> <span data-ttu-id="61d20-111">Questo valore può essere una combinazione dello stile della classe Button **BS \_ AUTOCHECKBOX** e degli stili **WS \_ TABSTOP** e **WS \_ Group** .</span><span class="sxs-lookup"><span data-stu-id="61d20-111">This value can be a combination of the button class style **BS\_AUTOCHECKBOX** and the **WS\_TABSTOP** and **WS\_GROUP** styles.</span></span>

<span data-ttu-id="61d20-112">Se non si specifica uno stile, lo stile predefinito è `BS_AUTOCHECKBOX | WS_TABSTOP` .</span><span class="sxs-lookup"><span data-stu-id="61d20-112">If you do not specify a style, the default style is `BS_AUTOCHECKBOX | WS_TABSTOP`.</span></span>

</dd> </dl>

<span data-ttu-id="61d20-113">Per ulteriori informazioni sulla sintassi generale di un'istruzione di controllo, vedere [parametri di controllo comuni](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="61d20-113">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="61d20-114">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="61d20-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61d20-115">**AUTO3STATE**</span><span class="sxs-lookup"><span data-stu-id="61d20-115">**AUTO3STATE**</span></span>](auto3state-control.md)
</dt> <dt>

[<span data-ttu-id="61d20-116">Stili dei pulsanti</span><span class="sxs-lookup"><span data-stu-id="61d20-116">Button Styles</span></span>](../controls/button-styles.md)
</dt> <dt>

[<span data-ttu-id="61d20-117">**CASELLA**</span><span class="sxs-lookup"><span data-stu-id="61d20-117">**CHECKBOX**</span></span>](checkbox-control.md)
</dt> <dt>

[<span data-ttu-id="61d20-118">**CONTROLLO**</span><span class="sxs-lookup"><span data-stu-id="61d20-118">**CONTROL**</span></span>](control-control.md)
</dt> <dt>

[<span data-ttu-id="61d20-119">**STATE3**</span><span class="sxs-lookup"><span data-stu-id="61d20-119">**STATE3**</span></span>](state3-control.md)
</dt> </dl>

 

 