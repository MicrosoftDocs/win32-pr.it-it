---
title: Controllo LTEXT
description: Definisce un controllo testo allineato a sinistra.
ms.assetid: ef6d7d06-3614-4b54-8a23-684d7ef65115
keywords:
- Menu di controllo di LTEXT e altre risorse
topic_type:
- apiref
api_name:
- LTEXT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f253c55238a36f7f6dd43f578c5ea5862a516869
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299741"
---
# <a name="ltext-control"></a><span data-ttu-id="501d0-104">Controllo LTEXT</span><span class="sxs-lookup"><span data-stu-id="501d0-104">LTEXT control</span></span>

<span data-ttu-id="501d0-105">Definisce un controllo testo allineato a sinistra.</span><span class="sxs-lookup"><span data-stu-id="501d0-105">Defines a left-aligned text control.</span></span> <span data-ttu-id="501d0-106">Il controllo è un rettangolo semplice che Visualizza il testo specificato allineato a sinistra nel rettangolo.</span><span class="sxs-lookup"><span data-stu-id="501d0-106">The control is a simple rectangle displaying the given text left-aligned in the rectangle.</span></span> <span data-ttu-id="501d0-107">Il testo viene formattato prima di essere visualizzato.</span><span class="sxs-lookup"><span data-stu-id="501d0-107">The text is formatted before it is displayed.</span></span> <span data-ttu-id="501d0-108">Le parole che si estendono oltre la fine di una riga vengono automaticamente racchiuse all'inizio della riga successiva.</span><span class="sxs-lookup"><span data-stu-id="501d0-108">Words that would extend past the end of a line are automatically wrapped to the beginning of the next line.</span></span> <span data-ttu-id="501d0-109">Le parole più lunghe della larghezza del controllo vengono troncate.</span><span class="sxs-lookup"><span data-stu-id="501d0-109">Words that are longer than the width of the control are truncated.</span></span>

<span data-ttu-id="501d0-110">L'istruzione **LTEXT** , che può essere utilizzata solo in un'istruzione [**DIALOGEX**](dialogex-resource.md) , definisce il testo, l'identificatore, le dimensioni e gli attributi del controllo.</span><span class="sxs-lookup"><span data-stu-id="501d0-110">The **LTEXT** statement, which can be used only in a [**DIALOGEX**](dialogex-resource.md) statement, defines the text, identifier, dimensions, and attributes of the control.</span></span>

``` syntax
LTEXT text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span data-ttu-id="501d0-111"><span id="style"></span><span id="STYLE"></span>*stile*</span><span class="sxs-lookup"><span data-stu-id="501d0-111"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="501d0-112">Stili del controllo.</span><span class="sxs-lookup"><span data-stu-id="501d0-112">Control styles.</span></span> <span data-ttu-id="501d0-113">Questo valore può essere costituito da qualsiasi combinazione dello stile del **\_ RadioButton BS** e dagli stili seguenti: **SS \_ Left**, **WS \_ TABSTOP** e **WS \_ Group**.</span><span class="sxs-lookup"><span data-stu-id="501d0-113">This value can be any combination of the **BS\_RADIOBUTTON** style and the following styles: **SS\_LEFT**, **WS\_TABSTOP**, and **WS\_GROUP**.</span></span>

<span data-ttu-id="501d0-114">Se non si specifica uno stile, lo stile predefinito è `SS_LEFT | WS_GROUP` .</span><span class="sxs-lookup"><span data-stu-id="501d0-114">If you do not specify a style, the default style is `SS_LEFT | WS_GROUP`.</span></span>

</dd> </dl>

<span data-ttu-id="501d0-115">Per ulteriori informazioni sulla sintassi generale di un'istruzione di controllo, vedere [parametri di controllo comuni](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="501d0-115">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span>

## <a name="examples"></a><span data-ttu-id="501d0-116">Esempio</span><span class="sxs-lookup"><span data-stu-id="501d0-116">Examples</span></span>

<span data-ttu-id="501d0-117">Questo esempio definisce un controllo testo allineato a sinistra con etichetta filename:</span><span class="sxs-lookup"><span data-stu-id="501d0-117">This example defines a left-aligned text control that is labeled Filename:</span></span>

``` syntax
LTEXT "Filename", 101, 10, 10, 100, 100
```

## <a name="see-also"></a><span data-ttu-id="501d0-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="501d0-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="501d0-119">**CONTROLLO**</span><span class="sxs-lookup"><span data-stu-id="501d0-119">**CONTROL**</span></span>](control-control.md)
</dt> <dt>

[<span data-ttu-id="501d0-120">**CTEXT**</span><span class="sxs-lookup"><span data-stu-id="501d0-120">**CTEXT**</span></span>](ctext-control.md)
</dt> <dt>

[<span data-ttu-id="501d0-121">Controlli di modifica</span><span class="sxs-lookup"><span data-stu-id="501d0-121">Edit Controls</span></span>](../controls/about-edit-controls.md)
</dt> <dt>

[<span data-ttu-id="501d0-122">**RTEXT**</span><span class="sxs-lookup"><span data-stu-id="501d0-122">**RTEXT**</span></span>](rtext-control.md)
</dt> </dl>

 

 