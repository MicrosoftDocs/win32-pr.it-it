---
title: Controllo EDITTEXT
description: Definisce un controllo di modifica appartenente alla classe di modifica.
ms.assetid: 9dc4be90-9503-4c97-813d-db246869ba3c
keywords:
- Menu di controllo di EDITTEXT e altre risorse
topic_type:
- apiref
api_name:
- EDITTEXT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 511cff6791703b30ec975625e0cd5cb044f4f492
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725879"
---
# <a name="edittext-control"></a><span data-ttu-id="7a76c-104">Controllo EDITTEXT</span><span class="sxs-lookup"><span data-stu-id="7a76c-104">EDITTEXT control</span></span>

<span data-ttu-id="7a76c-105">Definisce un controllo di modifica appartenente alla classe di modifica.</span><span class="sxs-lookup"><span data-stu-id="7a76c-105">Defines an edit control belonging to the EDIT class.</span></span> <span data-ttu-id="7a76c-106">Viene creata un'area rettangolare in cui l'utente può digitare e modificare il testo.</span><span class="sxs-lookup"><span data-stu-id="7a76c-106">It creates a rectangular region in which the user can type and edit text.</span></span> <span data-ttu-id="7a76c-107">Il controllo Visualizza un cursore quando l'utente fa clic sul mouse.</span><span class="sxs-lookup"><span data-stu-id="7a76c-107">The control displays a cursor when the user clicks the mouse in it.</span></span> <span data-ttu-id="7a76c-108">L'utente può quindi utilizzare la tastiera per immettere testo o modificare il testo esistente.</span><span class="sxs-lookup"><span data-stu-id="7a76c-108">The user can then use the keyboard to enter text or edit the existing text.</span></span> <span data-ttu-id="7a76c-109">La modifica delle chiavi include le chiavi backspace ed DELETE.</span><span class="sxs-lookup"><span data-stu-id="7a76c-109">Editing keys include the BACKSPACE and DELETE keys.</span></span> <span data-ttu-id="7a76c-110">L'utente può inoltre utilizzare il mouse per selezionare i caratteri da eliminare o per selezionare la posizione in cui inserire nuovi caratteri.</span><span class="sxs-lookup"><span data-stu-id="7a76c-110">The user can also use the mouse to select characters to be deleted or to select the place to insert new characters.</span></span>

``` syntax
EDITTEXT id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span data-ttu-id="7a76c-111"><span id="style"></span><span id="STYLE"></span>*stile*</span><span class="sxs-lookup"><span data-stu-id="7a76c-111"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="7a76c-112">Stili del controllo.</span><span class="sxs-lookup"><span data-stu-id="7a76c-112">Control styles.</span></span> <span data-ttu-id="7a76c-113">Questo valore può essere una combinazione degli stili della classe Edit e degli stili seguenti: **WS \_ TABSTOP**, **WS \_ Group**, **WS \_ VSCROLL**, **WS \_ HSCROLL** e **WS \_ disabled**.</span><span class="sxs-lookup"><span data-stu-id="7a76c-113">This value can be a combination of the edit class styles and the following styles: **WS\_TABSTOP**, **WS\_GROUP**, **WS\_VSCROLL**, **WS\_HSCROLL**, and **WS\_DISABLED**.</span></span>

<span data-ttu-id="7a76c-114">Se non si specifica uno stile, lo stile predefinito è `ES_LEFT | WS_BORDER | WS_TABSTOP` .</span><span class="sxs-lookup"><span data-stu-id="7a76c-114">If you do not specify a style, the default style is `ES_LEFT | WS_BORDER | WS_TABSTOP`.</span></span>

</dd> </dl>

<span data-ttu-id="7a76c-115">Per ulteriori informazioni sulla sintassi generale di un'istruzione di controllo, vedere [parametri di controllo comuni](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="7a76c-115">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span>

## <a name="examples"></a><span data-ttu-id="7a76c-116">Esempio</span><span class="sxs-lookup"><span data-stu-id="7a76c-116">Examples</span></span>

<span data-ttu-id="7a76c-117">Nell'esempio seguente viene illustrato l'utilizzo dell'istruzione **EDITTEXT** :</span><span class="sxs-lookup"><span data-stu-id="7a76c-117">The following example demonstrates the use of the **EDITTEXT** statement:</span></span>

``` syntax
EDITTEXT  3, 10, 10, 100, 10
```

## <a name="see-also"></a><span data-ttu-id="7a76c-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7a76c-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a76c-119">Controlli di modifica</span><span class="sxs-lookup"><span data-stu-id="7a76c-119">Edit Controls</span></span>](../controls/about-edit-controls.md)
</dt> </dl>

 

 