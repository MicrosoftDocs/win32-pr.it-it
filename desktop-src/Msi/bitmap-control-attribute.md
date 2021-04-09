---
description: Se viene impostato il bit del controllo bitmap, il testo nel controllo viene sostituito da un'immagine bitmap. La colonna di testo nella tabella dei controlli è una chiave esterna nella tabella binaria.
ms.assetid: ec774f31-7712-4a70-8c69-1cc731009049
title: Attributo di controllo bitmap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bda78231c1689c4c5faebeab98fbf6566c7e667
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881081"
---
# <a name="bitmap-control-attribute"></a><span data-ttu-id="98b08-104">Attributo di controllo bitmap</span><span class="sxs-lookup"><span data-stu-id="98b08-104">Bitmap Control Attribute</span></span>

<span data-ttu-id="98b08-105">Se viene impostato il bit del controllo bitmap, il testo nel controllo viene sostituito da un'immagine bitmap.</span><span class="sxs-lookup"><span data-stu-id="98b08-105">If the Bitmap Control bit is set, the text in the control is replaced by a bitmap image.</span></span> <span data-ttu-id="98b08-106">La colonna di testo nella [tabella dei controlli](control-table.md) è una chiave esterna nella [tabella binaria](binary-table.md).</span><span class="sxs-lookup"><span data-stu-id="98b08-106">The Text column in the [Control table](control-table.md) is a foreign key into the [Binary table](binary-table.md).</span></span>

<span data-ttu-id="98b08-107">Se questo bit non è impostato, il testo nel controllo viene specificato nella colonna di testo della tabella dei [controlli](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="98b08-107">If this bit is not set, the text in the control is specified in the Text column of the [Control table](control-table.md).</span></span>

## <a name="valid-controls"></a><span data-ttu-id="98b08-108">Controlli validi</span><span class="sxs-lookup"><span data-stu-id="98b08-108">Valid Controls</span></span>

[<span data-ttu-id="98b08-109">CheckBox</span><span class="sxs-lookup"><span data-stu-id="98b08-109">CheckBox</span></span>](checkbox-control.md)

 

[<span data-ttu-id="98b08-110">Pulsante</span><span class="sxs-lookup"><span data-stu-id="98b08-110">PushButton</span></span>](pushbutton-control.md)

 

[<span data-ttu-id="98b08-111">RadioButtonGroup</span><span class="sxs-lookup"><span data-stu-id="98b08-111">RadioButtonGroup</span></span>](radiobuttongroup-control.md)

## <a name="value"></a><span data-ttu-id="98b08-112">Valore</span><span class="sxs-lookup"><span data-stu-id="98b08-112">Value</span></span>



| <span data-ttu-id="98b08-113">Decimal</span><span class="sxs-lookup"><span data-stu-id="98b08-113">Decimal</span></span> | <span data-ttu-id="98b08-114">Valore esadecimale</span><span class="sxs-lookup"><span data-stu-id="98b08-114">Hexadecimal</span></span> | <span data-ttu-id="98b08-115">Costante</span><span class="sxs-lookup"><span data-stu-id="98b08-115">Constant</span></span>                         |
|---------|-------------|----------------------------------|
| <span data-ttu-id="98b08-116">262144</span><span class="sxs-lookup"><span data-stu-id="98b08-116">262144</span></span>  | <span data-ttu-id="98b08-117">0x00040000</span><span class="sxs-lookup"><span data-stu-id="98b08-117">0x00040000</span></span>  | <span data-ttu-id="98b08-118">**msidbControlAttributesBitmap**</span><span class="sxs-lookup"><span data-stu-id="98b08-118">**msidbControlAttributesBitmap**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="98b08-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="98b08-119">Remarks</span></span>

<span data-ttu-id="98b08-120">Per impostare questo attributo su un controllo, includere il bit bitmap nella colonna attributi del record del controllo nella [tabella dei controlli](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="98b08-120">To set this attribute on a control, include the Bitmap bit in the Attributes column of the control's record in the [Control table](control-table.md).</span></span>

<span data-ttu-id="98b08-121">La colonna di testo nella tabella dei controlli viene utilizzata come chiave esterna per la [tabella binaria](binary-table.md), pertanto il controllo non può contenere sia un'immagine icona che un testo.</span><span class="sxs-lookup"><span data-stu-id="98b08-121">The Text column in the Control table is used as a foreign key to the [Binary table](binary-table.md), therefore the control cannot contain both an icon image and text.</span></span>

<span data-ttu-id="98b08-122">Non impostare sia l' [icona](icon-control-attribute.md) che i bit bitmap.</span><span class="sxs-lookup"><span data-stu-id="98b08-122">Do not set both the [Icon](icon-control-attribute.md) and Bitmap bits.</span></span>

<span data-ttu-id="98b08-123">Vedere [gli attributi del controllo](control-attributes.md) e il controllo che è necessario creare sotto i [controlli](controls.md).</span><span class="sxs-lookup"><span data-stu-id="98b08-123">See [Control Attributes](control-attributes.md) and the control you need to create under [Controls](controls.md).</span></span>

 

 



