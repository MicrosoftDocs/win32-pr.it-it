---
title: EXSTYLE-istruzione
description: Definisce gli stili estesi della finestra per una finestra di dialogo. In una definizione di risorsa, l'istruzione EXSTYLE viene inserita con le istruzioni facoltative prima dell'inizio del corpo della definizione di risorsa.
ms.assetid: 5dc74bab-e385-457c-80c4-5e04eed589b5
keywords:
- Menu di istruzioni EXSTYLE e altre risorse
topic_type:
- apiref
api_name:
- EXSTYLE
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 277727757daeaafe5ad11cfd2e4f5fb6ee726458
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104472915"
---
# <a name="exstyle-statement"></a><span data-ttu-id="bde16-105">EXSTYLE-istruzione</span><span class="sxs-lookup"><span data-stu-id="bde16-105">EXSTYLE statement</span></span>

<span data-ttu-id="bde16-106">Definisce gli stili estesi della finestra per una finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="bde16-106">Defines extended window styles for a dialog box.</span></span> <span data-ttu-id="bde16-107">In una definizione di risorsa, l'istruzione **ExStyle** viene inserita con le istruzioni facoltative prima dell'inizio del corpo della definizione di risorsa.</span><span class="sxs-lookup"><span data-stu-id="bde16-107">In a resource definition, the **EXSTYLE** statement is placed with the optional statements before the beginning of the body of the resource definition.</span></span>

``` syntax
EXSTYLE extended-style
```

<dl> <dt>

<span data-ttu-id="bde16-108"><span id="extended-style"></span><span id="EXTENDED-STYLE"></span>*stile esteso*</span><span class="sxs-lookup"><span data-stu-id="bde16-108"><span id="extended-style"></span><span id="EXTENDED-STYLE"></span>*extended-style*</span></span>
</dt> <dd>

<span data-ttu-id="bde16-109">Stile di finestra esteso per la finestra di dialogo o il controllo.</span><span class="sxs-lookup"><span data-stu-id="bde16-109">Extended window style for the dialog box or control.</span></span> <span data-ttu-id="bde16-110">Per un elenco degli stili estesi della finestra, vedere [**stili finestra estesi**](/windows/desktop/winmsg/extended-window-styles).</span><span class="sxs-lookup"><span data-stu-id="bde16-110">For a list of extended window styles, see [**Extended Window Styles**](/windows/desktop/winmsg/extended-window-styles).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bde16-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="bde16-111">Remarks</span></span>

<span data-ttu-id="bde16-112">Per i controlli, gli stili estesi vengono specificati dopo l'opzione *stile* nell'istruzione di definizione della risorsa del controllo.</span><span class="sxs-lookup"><span data-stu-id="bde16-112">For controls, extended styles are specified after the *style* option in the control resource-definition statement.</span></span> <span data-ttu-id="bde16-113">Per ulteriori informazioni, vedere l'istruzione di definizione delle risorse per il singolo controllo.</span><span class="sxs-lookup"><span data-stu-id="bde16-113">For more information, see the resource-definition statement for the individual control.</span></span>

## <a name="see-also"></a><span data-ttu-id="bde16-114">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bde16-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bde16-115">**ACCELERATORI**</span><span class="sxs-lookup"><span data-stu-id="bde16-115">**ACCELERATORS**</span></span>](accelerators-resource.md)
</dt> <dt>

[<span data-ttu-id="bde16-116">**CONTROLLO**</span><span class="sxs-lookup"><span data-stu-id="bde16-116">**CONTROL**</span></span>](control-control.md)
</dt> <dt>

[<span data-ttu-id="bde16-117">**DIALOGO**</span><span class="sxs-lookup"><span data-stu-id="bde16-117">**DIALOG**</span></span>](dialog-resource.md)
</dt> <dt>

[<span data-ttu-id="bde16-118">**MENU**</span><span class="sxs-lookup"><span data-stu-id="bde16-118">**MENU**</span></span>](menu-resource.md)
</dt> <dt>

[<span data-ttu-id="bde16-119">**POPUP**</span><span class="sxs-lookup"><span data-stu-id="bde16-119">**POPUP**</span></span>](popup-resource.md)
</dt> <dt>

[<span data-ttu-id="bde16-120">**RCDATA**</span><span class="sxs-lookup"><span data-stu-id="bde16-120">**RCDATA**</span></span>](rcdata-resource.md)
</dt> <dt>

[<span data-ttu-id="bde16-121">**UN'STRINGTABLE**</span><span class="sxs-lookup"><span data-stu-id="bde16-121">**STRINGTABLE**</span></span>](stringtable-resource.md)
</dt> <dt>

[<span data-ttu-id="bde16-122">Risorsa definita dall'utente</span><span class="sxs-lookup"><span data-stu-id="bde16-122">User-Defined Resource</span></span>](user-defined-resource.md)
</dt> </dl>

 

 