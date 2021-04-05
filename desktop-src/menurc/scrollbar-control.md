---
title: SCROLLBAR (controllo)
description: Definisce un controllo barra di scorrimento.
ms.assetid: 9b0b60b1-4b4b-494e-90d0-aaa67e7ea88c
keywords:
- Menu di controllo SCROLLBAR e altre risorse
topic_type:
- apiref
api_name:
- SCROLLBAR
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44ef4069988603c7c89ec2ed8a363d3515a0b8bb
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104117746"
---
# <a name="scrollbar-control"></a><span data-ttu-id="9cb79-104">SCROLLBAR (controllo)</span><span class="sxs-lookup"><span data-stu-id="9cb79-104">SCROLLBAR control</span></span>

<span data-ttu-id="9cb79-105">Definisce un controllo barra di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="9cb79-105">Defines a scroll-bar control.</span></span> <span data-ttu-id="9cb79-106">Il controllo è un rettangolo che contiene una casella di scorrimento e con frecce di direzione a entrambe le estremità.</span><span class="sxs-lookup"><span data-stu-id="9cb79-106">The control is a rectangle that contains a scroll box and has direction arrows at both ends.</span></span> <span data-ttu-id="9cb79-107">Il controllo barra di scorrimento invia un messaggio di notifica all'elemento padre ogni volta che l'utente fa clic sul mouse nel controllo.</span><span class="sxs-lookup"><span data-stu-id="9cb79-107">The scroll-bar control sends a notification message to its parent whenever the user clicks the mouse in the control.</span></span> <span data-ttu-id="9cb79-108">L'elemento padre è responsabile dell'aggiornamento della posizione della casella di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="9cb79-108">The parent is responsible for updating the scroll-box position.</span></span> <span data-ttu-id="9cb79-109">I controlli barra di scorrimento possono essere posizionati in qualsiasi punto di una finestra e usati quando necessario per fornire input di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="9cb79-109">Scroll-bar controls can be positioned anywhere in a window and used whenever needed to provide scrolling input.</span></span>

``` syntax
SCROLLBAR id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span data-ttu-id="9cb79-110"><span id="style"></span><span id="STYLE"></span>*stile*</span><span class="sxs-lookup"><span data-stu-id="9cb79-110"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="9cb79-111">Zero o una combinazione degli stili seguenti: **WS \_ TABSTOP**, **WS \_ Group** e **WS \_ disabled**.</span><span class="sxs-lookup"><span data-stu-id="9cb79-111">Zero or a combination of the following styles: **WS\_TABSTOP**, **WS\_GROUP**, and **WS\_DISABLED**.</span></span>

<span data-ttu-id="9cb79-112">Oltre a questi stili, il parametro di *stile* può contenere una combinazione (o nessuno) degli stili della classe ScrollBar.</span><span class="sxs-lookup"><span data-stu-id="9cb79-112">In addition to these styles, the *style* parameter may contain a combination (or none) of the SCROLLBAR-class styles.</span></span>

<span data-ttu-id="9cb79-113">Se non si specifica uno stile, lo stile predefinito è **SBS \_ orizzontalmente**.</span><span class="sxs-lookup"><span data-stu-id="9cb79-113">If you do not specify a style, the default style is **SBS\_HORZ**.</span></span>

</dd> </dl>

<span data-ttu-id="9cb79-114">Per ulteriori informazioni sulla sintassi generale di un'istruzione di controllo, vedere [parametri di controllo comuni](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="9cb79-114">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span> <span data-ttu-id="9cb79-115">Si noti che non è possibile specificare il testo per questo controllo.</span><span class="sxs-lookup"><span data-stu-id="9cb79-115">Note that you cannot specify text for this control.</span></span>

## <a name="examples"></a><span data-ttu-id="9cb79-116">Esempio</span><span class="sxs-lookup"><span data-stu-id="9cb79-116">Examples</span></span>

<span data-ttu-id="9cb79-117">Nell'esempio seguente viene illustrato l'utilizzo dell'istruzione **ScrollBar** :</span><span class="sxs-lookup"><span data-stu-id="9cb79-117">The following example demonstrates the use of the **SCROLLBAR** statement:</span></span>

``` syntax
#define IDC_SCROLLBARV                  1010

SCROLLBAR IDC_SCROLLBARV, 7, 55, 187, 44, SBS_VERT
```

## <a name="see-also"></a><span data-ttu-id="9cb79-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9cb79-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9cb79-119">Barre di scorrimento</span><span class="sxs-lookup"><span data-stu-id="9cb79-119">Scroll Bars</span></span>](../controls/about-scroll-bars.md)
</dt> </dl>

 

 