---
title: Controllo DEFPUSHBUTTON
description: Definisce un controllo pulsante di comando predefinito.
ms.assetid: 17b2ffcb-0611-4d92-9108-bf27b1c07049
keywords:
- Menu di controllo di DEFPUSHBUTTON e altre risorse
topic_type:
- apiref
api_name:
- DEFPUSHBUTTON
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49b958e60d812c3372ad6a6e6ed2a8d02d56c0f6
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "106299267"
---
# <a name="defpushbutton-control"></a><span data-ttu-id="486d8-104">Controllo DEFPUSHBUTTON</span><span class="sxs-lookup"><span data-stu-id="486d8-104">DEFPUSHBUTTON control</span></span>

<span data-ttu-id="486d8-105">Definisce un controllo pulsante di comando predefinito.</span><span class="sxs-lookup"><span data-stu-id="486d8-105">Defines a default push-button control.</span></span> <span data-ttu-id="486d8-106">Il controllo è un rettangolo di piccole dimensioni con un contorno in grassetto che rappresenta la risposta predefinita per l'utente.</span><span class="sxs-lookup"><span data-stu-id="486d8-106">The control is a small rectangle with a bold outline that represents the default response for the user.</span></span> <span data-ttu-id="486d8-107">Il testo specificato viene visualizzato all'interno del pulsante.</span><span class="sxs-lookup"><span data-stu-id="486d8-107">The given text is displayed inside the button.</span></span> <span data-ttu-id="486d8-108">Il controllo evidenzia il pulsante nel modo consueto quando l'utente fa clic sul mouse e invia un messaggio alla finestra padre.</span><span class="sxs-lookup"><span data-stu-id="486d8-108">The control highlights the button in the usual way when the user clicks the mouse in it and sends a message to its parent window.</span></span>

``` syntax
DEFPUSHBUTTON text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span data-ttu-id="486d8-109"><span id="text"></span><span id="TEXT"></span>*testo*</span><span class="sxs-lookup"><span data-stu-id="486d8-109"><span id="text"></span><span id="TEXT"></span>*text*</span></span>
</dt> <dd>

<span data-ttu-id="486d8-110">Testo che deve essere centrato nell'area rettangolare del controllo.</span><span class="sxs-lookup"><span data-stu-id="486d8-110">Text that is to be centered in the rectangular area of the control.</span></span>

</dd> <dt>

<span data-ttu-id="486d8-111"><span id="style"></span><span id="STYLE"></span>*stile*</span><span class="sxs-lookup"><span data-stu-id="486d8-111"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="486d8-112">Stili del controllo.</span><span class="sxs-lookup"><span data-stu-id="486d8-112">Control styles.</span></span> <span data-ttu-id="486d8-113">Questo valore può essere una combinazione degli stili seguenti: **BS \_ DEFPUSHBUTTON**, **WS \_ TABSTOP**, **WS \_ Group** e **WS \_ disabled**.</span><span class="sxs-lookup"><span data-stu-id="486d8-113">This value can be a combination of the following styles: **BS\_DEFPUSHBUTTON**, **WS\_TABSTOP**, **WS\_GROUP**, and **WS\_DISABLED**.</span></span>

<span data-ttu-id="486d8-114">Se non si specifica uno stile, lo stile predefinito è `BS_DEFPUSHBUTTON | WS_TABSTOP` .</span><span class="sxs-lookup"><span data-stu-id="486d8-114">If you do not specify a style, the default style is `BS_DEFPUSHBUTTON | WS_TABSTOP`.</span></span>

</dd> </dl>

<span data-ttu-id="486d8-115">Per ulteriori informazioni sulla sintassi generale di un'istruzione di controllo, vedere [parametri di controllo comuni](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="486d8-115">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span>

## <a name="examples"></a><span data-ttu-id="486d8-116">Esempio</span><span class="sxs-lookup"><span data-stu-id="486d8-116">Examples</span></span>

<span data-ttu-id="486d8-117">Questo esempio definisce un controllo pulsante di comando predefinito con etichetta Annulla:</span><span class="sxs-lookup"><span data-stu-id="486d8-117">This example defines a default push-button control that is labeled Cancel:</span></span>

``` syntax
DEFPUSHBUTTON "Cancel", 101, 10, 10, 24, 50
```

## <a name="see-also"></a><span data-ttu-id="486d8-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="486d8-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="486d8-119">Pulsanti di push</span><span class="sxs-lookup"><span data-stu-id="486d8-119">Push Buttons</span></span>](https://www.bing.com/search?q=Push+Buttons)
</dt> <dt>

[<span data-ttu-id="486d8-120">**PULSANTE**</span><span class="sxs-lookup"><span data-stu-id="486d8-120">**PUSHBUTTON**</span></span>](pushbutton-control.md)
</dt> <dt>

[<span data-ttu-id="486d8-121">**RADIOBUTTON**</span><span class="sxs-lookup"><span data-stu-id="486d8-121">**RADIOBUTTON**</span></span>](radiobutton-control.md)
</dt> </dl>

 

 




