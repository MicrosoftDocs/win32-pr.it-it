---
title: Controllo LISTBOX (menu e altre risorse)
description: Definisce i controlli di uso comune per una finestra di dialogo o una finestra. Il controllo è un rettangolo contenente un elenco di stringhe, ad esempio i nomi file, da cui l'utente può selezionare.
ms.assetid: 78f6d36e-5079-4f04-87e4-ca55a1161a51
keywords:
- Menu di controllo LISTBOX e altre risorse
topic_type:
- apiref
api_name:
- LISTBOX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9f062387463917438a988c3b023ca656beef722
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104117718"
---
# <a name="listbox-control"></a><span data-ttu-id="39e4d-105">LISTBOX (controllo)</span><span class="sxs-lookup"><span data-stu-id="39e4d-105">LISTBOX control</span></span>

<span data-ttu-id="39e4d-106">Definisce i controlli di uso comune per una finestra di dialogo o una finestra.</span><span class="sxs-lookup"><span data-stu-id="39e4d-106">Defines commonly used controls for a dialog box or window.</span></span> <span data-ttu-id="39e4d-107">Il controllo è un rettangolo contenente un elenco di stringhe, ad esempio i nomi file, da cui l'utente può selezionare.</span><span class="sxs-lookup"><span data-stu-id="39e4d-107">The control is a rectangle containing a list of strings (such as filenames) from which the user can select.</span></span>

<span data-ttu-id="39e4d-108">L'istruzione **ListBox** , che può essere utilizzata solo in un'istruzione [**DIALOGEX**](dialogex-resource.md) o **Window** , definisce l'identificatore, le dimensioni e gli attributi di una finestra del controllo.</span><span class="sxs-lookup"><span data-stu-id="39e4d-108">The **LISTBOX** statement, which can only be used in a [**DIALOGEX**](dialogex-resource.md) or **WINDOW** statement, defines the identifier, dimensions, and attributes of a control window.</span></span>

``` syntax
LISTBOX id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span data-ttu-id="39e4d-109"><span id="style"></span><span id="STYLE"></span>*stile*</span><span class="sxs-lookup"><span data-stu-id="39e4d-109"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="39e4d-110">Stili del controllo.</span><span class="sxs-lookup"><span data-stu-id="39e4d-110">Control styles.</span></span> <span data-ttu-id="39e4d-111">Questo valore può essere costituito da una combinazione degli stili delle classi della casella di riepilogo e da uno qualsiasi degli stili seguenti: **WS \_ Border** e **WS \_ VSCROLL**.</span><span class="sxs-lookup"><span data-stu-id="39e4d-111">This value can be a combination of the list-box class styles and any of the following styles: **WS\_BORDER** and **WS\_VSCROLL**.</span></span>

<span data-ttu-id="39e4d-112">Se non si specifica uno stile, lo stile predefinito è `LBS_NOTIFY | WS_BORDER` .</span><span class="sxs-lookup"><span data-stu-id="39e4d-112">If you do not specify a style, the default style is `LBS_NOTIFY | WS_BORDER`.</span></span>

</dd> </dl>

<span data-ttu-id="39e4d-113">Per ulteriori informazioni sulla sintassi generale di un'istruzione di controllo, vedere [parametri di controllo comuni](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="39e4d-113">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span>

## <a name="examples"></a><span data-ttu-id="39e4d-114">Esempio</span><span class="sxs-lookup"><span data-stu-id="39e4d-114">Examples</span></span>

<span data-ttu-id="39e4d-115">Questo esempio definisce un controllo casella di riepilogo il cui identificatore è 101:</span><span class="sxs-lookup"><span data-stu-id="39e4d-115">This example defines a list-box control whose identifier is 101:</span></span>

``` syntax
LISTBOX 101, 10, 10, 100, 100
```

## <a name="see-also"></a><span data-ttu-id="39e4d-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="39e4d-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39e4d-117">**COMBOBOX**</span><span class="sxs-lookup"><span data-stu-id="39e4d-117">**COMBOBOX**</span></span>](combobox-control.md)
</dt> <dt>

[<span data-ttu-id="39e4d-118">Caselle di riepilogo</span><span class="sxs-lookup"><span data-stu-id="39e4d-118">List Boxes</span></span>](../controls/about-list-boxes.md)
</dt> </dl>

 

 