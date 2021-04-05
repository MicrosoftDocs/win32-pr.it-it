---
title: Controllo AUTORADIOBUTTON
description: Definisce un controllo pulsante di opzione automatico. Questo controllo esegue automaticamente l'esclusione reciproca con gli altri controlli di AUTORADIOBUTTON nello stesso gruppo. Quando si sceglie il pulsante, l'applicazione riceve una notifica con un \_ clic su BN.
ms.assetid: af843084-5213-4934-b291-0787b88ef62d
keywords:
- Menu di controllo AUTORADIOBUTTON e altre risorse
topic_type:
- apiref
api_name:
- AUTORADIOBUTTON
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67395437303de0adc8c1af226210f8ca2f45958d
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103718352"
---
# <a name="autoradiobutton-control"></a><span data-ttu-id="9e13c-106">Controllo AUTORADIOBUTTON</span><span class="sxs-lookup"><span data-stu-id="9e13c-106">AUTORADIOBUTTON control</span></span>

<span data-ttu-id="9e13c-107">Definisce un controllo pulsante di opzione automatico.</span><span class="sxs-lookup"><span data-stu-id="9e13c-107">Defines an automatic radio button control.</span></span> <span data-ttu-id="9e13c-108">Questo controllo esegue automaticamente l'esclusione reciproca con gli altri controlli di **AUTORADIOBUTTON** nello stesso gruppo.</span><span class="sxs-lookup"><span data-stu-id="9e13c-108">This control automatically performs mutual exclusion with the other **AUTORADIOBUTTON** controls in the same group.</span></span> <span data-ttu-id="9e13c-109">Quando si sceglie il pulsante, l'applicazione riceve una notifica con un **\_ clic su BN**.</span><span class="sxs-lookup"><span data-stu-id="9e13c-109">When the button is chosen, the application is notified with **BN\_CLICKED**.</span></span>

``` syntax
AUTORADIOBUTTON text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span data-ttu-id="9e13c-110"><span id="text"></span><span id="TEXT"></span>*testo*</span><span class="sxs-lookup"><span data-stu-id="9e13c-110"><span id="text"></span><span id="TEXT"></span>*text*</span></span>
</dt> <dd>

<span data-ttu-id="9e13c-111">Testo che verrà visualizzato accanto al pulsante di opzione.</span><span class="sxs-lookup"><span data-stu-id="9e13c-111">Text that will appear next to the radio button.</span></span>

</dd> <dt>

<span data-ttu-id="9e13c-112"><span id="style"></span><span id="STYLE"></span>*stile*</span><span class="sxs-lookup"><span data-stu-id="9e13c-112"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="9e13c-113">Stili per il pulsante di opzione automatico, che può essere una combinazione di stili di classi di pulsanti e gli stili seguenti: **WS \_ TABSTOP**, **WS \_ disabled** e **WS \_ Group**.</span><span class="sxs-lookup"><span data-stu-id="9e13c-113">Styles for the automatic radio button, which can be a combination of BUTTON-class styles and the following styles: **WS\_TABSTOP**, **WS\_DISABLED**, and **WS\_GROUP**.</span></span>

<span data-ttu-id="9e13c-114">Se non si specifica uno stile, lo stile predefinito è `BS_AUTORADIOBUTTON | WS_TABSTOP` .</span><span class="sxs-lookup"><span data-stu-id="9e13c-114">If you do not specify a style, the default style is `BS_AUTORADIOBUTTON | WS_TABSTOP`.</span></span>

</dd> </dl>

<span data-ttu-id="9e13c-115">Per ulteriori informazioni sulla sintassi generale di un'istruzione di controllo, vedere [parametri di controllo comuni](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="9e13c-115">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="9e13c-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9e13c-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e13c-117">**CONTROLLO**</span><span class="sxs-lookup"><span data-stu-id="9e13c-117">**CONTROL**</span></span>](control-control.md)
</dt> <dt>

[<span data-ttu-id="9e13c-118">Pulsanti di opzione</span><span class="sxs-lookup"><span data-stu-id="9e13c-118">Radio Buttons</span></span>](https://www.bing.com/search?q=Radio+Buttons)
</dt> <dt>

[<span data-ttu-id="9e13c-119">**RADIOBUTTON**</span><span class="sxs-lookup"><span data-stu-id="9e13c-119">**RADIOBUTTON**</span></span>](radiobutton-control.md)
</dt> </dl>

 

 




