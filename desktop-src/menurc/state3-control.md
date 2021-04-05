---
title: Controllo STATE3
description: Definisce un controllo casella di controllo a tre stati. Il controllo è identico a una casella di controllo, ad eccezione del fatto che ha tre stati controllati, deselezionati e disabilitati (in grigio).
ms.assetid: 74659827-ce46-4d36-a5e2-3a97e8fd1c04
keywords:
- Menu di controllo di STATE3 e altre risorse
topic_type:
- apiref
api_name:
- STATE3
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24333fa9567db5613896f26429b72ff68e029335
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103718130"
---
# <a name="state3-control"></a><span data-ttu-id="9ad62-105">Controllo STATE3</span><span class="sxs-lookup"><span data-stu-id="9ad62-105">STATE3 control</span></span>

<span data-ttu-id="9ad62-106">Definisce un controllo casella di controllo a tre stati.</span><span class="sxs-lookup"><span data-stu-id="9ad62-106">Defines a three-state check box control.</span></span> <span data-ttu-id="9ad62-107">Il controllo è identico a una [**casella**](checkbox-control.md)di controllo, ad eccezione del fatto che ha tre stati: checked, dechecked e Disabled (grigio).</span><span class="sxs-lookup"><span data-stu-id="9ad62-107">The control is identical to a [**CHECKBOX**](checkbox-control.md), except that it has three states: checked, unchecked, and disabled (grayed).</span></span>

``` syntax
STATE3 text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span data-ttu-id="9ad62-108"><span id="text"></span><span id="TEXT"></span>*testo*</span><span class="sxs-lookup"><span data-stu-id="9ad62-108"><span id="text"></span><span id="TEXT"></span>*text*</span></span>
</dt> <dd>

<span data-ttu-id="9ad62-109">Testo da visualizzare a destra del controllo.</span><span class="sxs-lookup"><span data-stu-id="9ad62-109">Text that is to be displayed to the right of the control.</span></span>

</dd> <dt>

<span data-ttu-id="9ad62-110"><span id="style"></span><span id="STYLE"></span>*stile*</span><span class="sxs-lookup"><span data-stu-id="9ad62-110"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="9ad62-111">Stili del controllo.</span><span class="sxs-lookup"><span data-stu-id="9ad62-111">Control styles.</span></span> <span data-ttu-id="9ad62-112">Questo valore può essere una combinazione dello stile della classe Button **BS \_ 3STATE** e degli stili di **\_ gruppo** **WS \_ TABSTOP** e WS.</span><span class="sxs-lookup"><span data-stu-id="9ad62-112">This value can be a combination of the button class style **BS\_3STATE** and the **WS\_TABSTOP** and **WS\_GROUP** styles.</span></span>

<span data-ttu-id="9ad62-113">Se non si specifica uno stile, lo stile predefinito è `BS_3STATE | WS_TABSTOP` .</span><span class="sxs-lookup"><span data-stu-id="9ad62-113">If you do not specify a style, the default style is `BS_3STATE | WS_TABSTOP`.</span></span>

</dd> </dl>

<span data-ttu-id="9ad62-114">Per ulteriori informazioni sulla sintassi generale di un'istruzione di controllo, vedere [parametri di controllo comuni](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="9ad62-114">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="9ad62-115">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9ad62-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ad62-116">**CASELLA di controllo AUTOCHECKBOX**</span><span class="sxs-lookup"><span data-stu-id="9ad62-116">**AUTOCHECKBOX**</span></span>](autocheckbox-control.md)
</dt> <dt>

[<span data-ttu-id="9ad62-117">Caselle di controllo</span><span class="sxs-lookup"><span data-stu-id="9ad62-117">Check Boxes</span></span>](https://www.bing.com/search?q=Check+Boxes)
</dt> <dt>

[<span data-ttu-id="9ad62-118">**CASELLA**</span><span class="sxs-lookup"><span data-stu-id="9ad62-118">**CHECKBOX**</span></span>](checkbox-control.md)
</dt> <dt>

[<span data-ttu-id="9ad62-119">**CONTROLLO**</span><span class="sxs-lookup"><span data-stu-id="9ad62-119">**CONTROL**</span></span>](control-control.md)
</dt> </dl>

 

 




