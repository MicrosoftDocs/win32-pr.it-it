---
title: Controllo CTEXT
description: Definisce un controllo di testo centrato.
ms.assetid: 11f42d25-8fe1-4a8b-a5c5-c8cb47cc8c73
keywords:
- Menu di controllo di CTEXT e altre risorse
topic_type:
- apiref
api_name:
- CTEXT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41c12b6c1da5d5bd5c8ce59a01e21b05baf77503
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104117663"
---
# <a name="ctext-control"></a><span data-ttu-id="60252-104">Controllo CTEXT</span><span class="sxs-lookup"><span data-stu-id="60252-104">CTEXT control</span></span>

<span data-ttu-id="60252-105">Definisce un controllo di testo centrato.</span><span class="sxs-lookup"><span data-stu-id="60252-105">Defines a centered-text control.</span></span> <span data-ttu-id="60252-106">Il controllo è un rettangolo semplice che Visualizza il testo specificato centrato nel rettangolo.</span><span class="sxs-lookup"><span data-stu-id="60252-106">The control is a simple rectangle displaying the given text centered in the rectangle.</span></span> <span data-ttu-id="60252-107">Il testo viene formattato prima di essere visualizzato.</span><span class="sxs-lookup"><span data-stu-id="60252-107">The text is formatted before it is displayed.</span></span> <span data-ttu-id="60252-108">Le parole che si estendono oltre la fine di una riga vengono automaticamente racchiuse all'inizio della riga successiva.</span><span class="sxs-lookup"><span data-stu-id="60252-108">Words that would extend past the end of a line are automatically wrapped to the beginning of the next line.</span></span> <span data-ttu-id="60252-109">Le parole più lunghe della larghezza del controllo vengono troncate.</span><span class="sxs-lookup"><span data-stu-id="60252-109">Words that are longer than the width of the control are truncated.</span></span>

<span data-ttu-id="60252-110">L'istruzione [**LTEXT**](ltext-control.md) , che può essere utilizzata solo in un'istruzione REP, definisce il testo, l'identificatore, le dimensioni e gli attributi del controllo.</span><span class="sxs-lookup"><span data-stu-id="60252-110">The [**LTEXT**](ltext-control.md) statement, which can be used only in a rep statement, defines the text, identifier, dimensions, and attributes of the control.</span></span>

``` syntax
CTEXT text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span data-ttu-id="60252-111"><span id="text"></span><span id="TEXT"></span>*testo*</span><span class="sxs-lookup"><span data-stu-id="60252-111"><span id="text"></span><span id="TEXT"></span>*text*</span></span>
</dt> <dd>

<span data-ttu-id="60252-112">Testo che deve essere centrato nell'area rettangolare del controllo.</span><span class="sxs-lookup"><span data-stu-id="60252-112">Text that is to be centered in the rectangular area of the control.</span></span>

</dd> <dt>

<span data-ttu-id="60252-113"><span id="style"></span><span id="STYLE"></span>*stile*</span><span class="sxs-lookup"><span data-stu-id="60252-113"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="60252-114">Stili del controllo.</span><span class="sxs-lookup"><span data-stu-id="60252-114">Control styles.</span></span> <span data-ttu-id="60252-115">Questo valore può essere costituito da qualsiasi combinazione degli stili seguenti: **SS \_ Center**, **WS \_ TABSTOP** e **WS \_ Group**.</span><span class="sxs-lookup"><span data-stu-id="60252-115">This value can be any combination of the following styles: **SS\_CENTER**, **WS\_TABSTOP**, and **WS\_GROUP**.</span></span>

<span data-ttu-id="60252-116">Se non si specifica uno stile, lo stile predefinito è `SS_CENTER | WS_GROUP` .</span><span class="sxs-lookup"><span data-stu-id="60252-116">If you do not specify a style, the default style is `SS_CENTER | WS_GROUP`.</span></span>

</dd> </dl>

<span data-ttu-id="60252-117">Per ulteriori informazioni sulla sintassi generale di un'istruzione di controllo, vedere [parametri di controllo comuni](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="60252-117">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span>

## <a name="examples"></a><span data-ttu-id="60252-118">Esempio</span><span class="sxs-lookup"><span data-stu-id="60252-118">Examples</span></span>

<span data-ttu-id="60252-119">Questo esempio definisce un controllo di testo centrato con etichetta filename:</span><span class="sxs-lookup"><span data-stu-id="60252-119">This example defines a centered-text control that is labeled Filename:</span></span>

``` syntax
CTEXT "Filename", 101, 10, 10, 100, 100 
```

## <a name="see-also"></a><span data-ttu-id="60252-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="60252-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60252-121">**CONTROLLO**</span><span class="sxs-lookup"><span data-stu-id="60252-121">**CONTROL**</span></span>](control-control.md)
</dt> <dt>

[<span data-ttu-id="60252-122">Controlli di modifica</span><span class="sxs-lookup"><span data-stu-id="60252-122">Edit Controls</span></span>](../controls/about-edit-controls.md)
</dt> <dt>

[<span data-ttu-id="60252-123">**LTEXT**</span><span class="sxs-lookup"><span data-stu-id="60252-123">**LTEXT**</span></span>](ltext-control.md)
</dt> <dt>

[<span data-ttu-id="60252-124">**RTEXT**</span><span class="sxs-lookup"><span data-stu-id="60252-124">**RTEXT**</span></span>](rtext-control.md)
</dt> </dl>

 

 