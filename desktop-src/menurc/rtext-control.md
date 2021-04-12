---
title: Controllo RTEXT
description: Definisce un controllo di testo allineato a destra.
ms.assetid: 66b890db-598e-4255-9d65-a21647005f8e
keywords:
- Menu di controllo di RTEXT e altre risorse
topic_type:
- apiref
api_name:
- RTEXT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bc56a870df7ebf5d2696e70573ae320220e803c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104473094"
---
# <a name="rtext-control"></a><span data-ttu-id="0fc3c-104">Controllo RTEXT</span><span class="sxs-lookup"><span data-stu-id="0fc3c-104">RTEXT control</span></span>

<span data-ttu-id="0fc3c-105">Definisce un controllo di testo allineato a destra.</span><span class="sxs-lookup"><span data-stu-id="0fc3c-105">Defines a right-aligned text control.</span></span> <span data-ttu-id="0fc3c-106">Il controllo è un rettangolo semplice che Visualizza il testo specificato allineato a destra nel rettangolo.</span><span class="sxs-lookup"><span data-stu-id="0fc3c-106">The control is a simple rectangle displaying the given text right-aligned in the rectangle.</span></span> <span data-ttu-id="0fc3c-107">Il testo viene formattato prima di essere visualizzato.</span><span class="sxs-lookup"><span data-stu-id="0fc3c-107">The text is formatted before it is displayed.</span></span> <span data-ttu-id="0fc3c-108">Le parole che si estendono oltre la fine di una riga vengono automaticamente racchiuse all'inizio della riga successiva.</span><span class="sxs-lookup"><span data-stu-id="0fc3c-108">Words that would extend past the end of a line are automatically wrapped to the beginning of the next line.</span></span> <span data-ttu-id="0fc3c-109">Le parole più lunghe della larghezza del controllo vengono troncate.</span><span class="sxs-lookup"><span data-stu-id="0fc3c-109">Words that are longer than the width of the control are truncated.</span></span>

<span data-ttu-id="0fc3c-110">L'istruzione **RTEXT** , che può essere utilizzata solo in un'istruzione [**DIALOGEX**](dialogex-resource.md) , definisce il testo, l'identificatore, le dimensioni e gli attributi del controllo.</span><span class="sxs-lookup"><span data-stu-id="0fc3c-110">The **RTEXT** statement, which can be used only in a [**DIALOGEX**](dialogex-resource.md) statement, defines the text, identifier, dimensions, and attributes of the control.</span></span>

``` syntax
RTEXT text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span data-ttu-id="0fc3c-111"><span id="style"></span><span id="STYLE"></span>*stile*</span><span class="sxs-lookup"><span data-stu-id="0fc3c-111"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="0fc3c-112">Stili per il controllo testo, che può essere una qualsiasi combinazione delle seguenti: **WS \_ TABSTOP** e **WS \_ Group**.</span><span class="sxs-lookup"><span data-stu-id="0fc3c-112">Styles for the text control, which can be any combination of the following: **WS\_TABSTOP** and **WS\_GROUP**.</span></span>

<span data-ttu-id="0fc3c-113">Se non si specifica uno stile, lo stile predefinito è `SS_RIGHT | WS_GROUP` .</span><span class="sxs-lookup"><span data-stu-id="0fc3c-113">If you do not specify a style, the default style is `SS_RIGHT | WS_GROUP`.</span></span>

</dd> </dl>

<span data-ttu-id="0fc3c-114">Per ulteriori informazioni sulla sintassi generale di un'istruzione di controllo, vedere [parametri di controllo comuni](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="0fc3c-114">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span>

## <a name="examples"></a><span data-ttu-id="0fc3c-115">Esempio</span><span class="sxs-lookup"><span data-stu-id="0fc3c-115">Examples</span></span>

<span data-ttu-id="0fc3c-116">Nell'esempio seguente viene illustrato l'utilizzo dell'istruzione **RTEXT** :</span><span class="sxs-lookup"><span data-stu-id="0fc3c-116">The following example demonstrates the use of the **RTEXT** statement:</span></span>

``` syntax
RTEXT "Number of Messages", 4, 30, 50, 100, 10
```

## <a name="see-also"></a><span data-ttu-id="0fc3c-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0fc3c-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0fc3c-118">**CONTROLLO**</span><span class="sxs-lookup"><span data-stu-id="0fc3c-118">**CONTROL**</span></span>](control-control.md)
</dt> <dt>

[<span data-ttu-id="0fc3c-119">**CTEXT**</span><span class="sxs-lookup"><span data-stu-id="0fc3c-119">**CTEXT**</span></span>](ctext-control.md)
</dt> <dt>

[<span data-ttu-id="0fc3c-120">Controlli di modifica</span><span class="sxs-lookup"><span data-stu-id="0fc3c-120">Edit Controls</span></span>](../controls/about-edit-controls.md)
</dt> <dt>

[<span data-ttu-id="0fc3c-121">**LTEXT**</span><span class="sxs-lookup"><span data-stu-id="0fc3c-121">**LTEXT**</span></span>](ltext-control.md)
</dt> </dl>

 

 