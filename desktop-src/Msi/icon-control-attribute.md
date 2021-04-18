---
description: Se questo bit è impostato, il testo viene sostituito da un'immagine dell'icona e la colonna di testo nella tabella del controllo è una chiave esterna nella tabella binaria.
ms.assetid: 5eefdfcb-89a5-4885-bab0-6409ef3ce349
title: Attributo del controllo Icon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e60c19674ac26f108109fad04e0836ed8dfeba6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308904"
---
# <a name="icon-control-attribute"></a><span data-ttu-id="d5058-103">Attributo del controllo Icon</span><span class="sxs-lookup"><span data-stu-id="d5058-103">Icon Control Attribute</span></span>

<span data-ttu-id="d5058-104">Se questo bit è impostato, il testo viene sostituito da un'immagine dell'icona e la colonna di testo nella [tabella del controllo](control-table.md) è una chiave esterna nella [tabella binaria](binary-table.md).</span><span class="sxs-lookup"><span data-stu-id="d5058-104">If this bit is set, text is replaced by an icon image and the Text column in the [Control table](control-table.md) is a foreign key into the [Binary table](binary-table.md).</span></span>

<span data-ttu-id="d5058-105">Se questo bit non è impostato, il testo nel controllo viene specificato nella colonna di testo della [tabella dei controlli](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="d5058-105">If this bit is not set, text in the control is specified in the Text column of the [Control table](control-table.md).</span></span>

## <a name="valid-controls"></a><span data-ttu-id="d5058-106">Controlli validi</span><span class="sxs-lookup"><span data-stu-id="d5058-106">Valid Controls</span></span>

[<span data-ttu-id="d5058-107">CheckBox</span><span class="sxs-lookup"><span data-stu-id="d5058-107">CheckBox</span></span>](checkbox-control.md)

[<span data-ttu-id="d5058-108">Pulsante</span><span class="sxs-lookup"><span data-stu-id="d5058-108">PushButton</span></span>](pushbutton-control.md)

[<span data-ttu-id="d5058-109">RadioButtonGroup</span><span class="sxs-lookup"><span data-stu-id="d5058-109">RadioButtonGroup</span></span>](radiobuttongroup-control.md)

## <a name="value"></a><span data-ttu-id="d5058-110">Valore</span><span class="sxs-lookup"><span data-stu-id="d5058-110">Value</span></span>



| <span data-ttu-id="d5058-111">Decimal</span><span class="sxs-lookup"><span data-stu-id="d5058-111">Decimal</span></span> | <span data-ttu-id="d5058-112">Valore esadecimale</span><span class="sxs-lookup"><span data-stu-id="d5058-112">Hexadecimal</span></span> | <span data-ttu-id="d5058-113">Costante</span><span class="sxs-lookup"><span data-stu-id="d5058-113">Constant</span></span>                       |
|---------|-------------|--------------------------------|
| <span data-ttu-id="d5058-114">5242288</span><span class="sxs-lookup"><span data-stu-id="d5058-114">5242288</span></span> | <span data-ttu-id="d5058-115">0x00080000</span><span class="sxs-lookup"><span data-stu-id="d5058-115">0x00080000</span></span>  | <span data-ttu-id="d5058-116">**msidbControlAttributesIcon**</span><span class="sxs-lookup"><span data-stu-id="d5058-116">**msidbControlAttributesIcon**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="d5058-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="d5058-117">Remarks</span></span>

<span data-ttu-id="d5058-118">Per impostare questo attributo su un controllo, includere i bit dell'icona nella colonna attributi del record del controllo nella tabella del [controllo](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="d5058-118">To set this attribute on a control, include the Icon bits in the Attributes column of the control's record in the [Control table](control-table.md).</span></span>

<span data-ttu-id="d5058-119">La colonna di testo nella tabella dei controlli viene utilizzata come chiave esterna per la [tabella binaria](binary-table.md), pertanto il controllo non può contenere sia un'immagine icona che un testo.</span><span class="sxs-lookup"><span data-stu-id="d5058-119">The Text column in the Control table is used as a foreign key to the [Binary table](binary-table.md), therefore the control cannot contain both an icon image and text.</span></span>

<span data-ttu-id="d5058-120">Non impostare sia l'icona che i bit [bitmap](bitmap-control-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="d5058-120">Do not set both the Icon and [Bitmap](bitmap-control-attribute.md) bits.</span></span>

<span data-ttu-id="d5058-121">Vedere [gli attributi del controllo](control-attributes.md) e il controllo che è necessario creare sotto i [controlli](controls.md).</span><span class="sxs-lookup"><span data-stu-id="d5058-121">See [Control Attributes](control-attributes.md) and the control you need to create under [Controls](controls.md).</span></span>

 

 



