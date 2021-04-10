---
description: Se questo bit è impostato su un controllo di modifica, il programma di installazione crea un controllo di modifica a più righe con una barra di scorrimento verticale.
ms.assetid: cbdbe088-9cf1-4af8-a5f7-072faee7f34e
title: Attributo di controllo su più righe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 936bc4b3901293e950690e878a0f86229bb03b4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226971"
---
# <a name="multiline-control-attribute"></a><span data-ttu-id="0b083-103">Attributo di controllo su più righe</span><span class="sxs-lookup"><span data-stu-id="0b083-103">MultiLine Control Attribute</span></span>

<span data-ttu-id="0b083-104">Se questo bit è impostato su un [controllo di modifica](edit-control.md), il programma di installazione crea un controllo di modifica a più righe con una barra di scorrimento verticale.</span><span class="sxs-lookup"><span data-stu-id="0b083-104">If this bit is set on an [Edit control](edit-control.md), the installer creates a multiple line edit control with a vertical scroll bar.</span></span>

<span data-ttu-id="0b083-105">Se questo bit non è impostato, viene specificato di visualizzare un normale controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="0b083-105">If this bit is not set, it specifies displaying a normal edit control.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="0b083-106">Controlli validi</span><span class="sxs-lookup"><span data-stu-id="0b083-106">Valid Controls</span></span>

<span data-ttu-id="0b083-107">[Controllo di modifica](edit-control.md).</span><span class="sxs-lookup"><span data-stu-id="0b083-107">[Edit control](edit-control.md).</span></span>



| <span data-ttu-id="0b083-108">Decimal</span><span class="sxs-lookup"><span data-stu-id="0b083-108">Decimal</span></span> | <span data-ttu-id="0b083-109">Valore esadecimale</span><span class="sxs-lookup"><span data-stu-id="0b083-109">Hexadecimal</span></span> | <span data-ttu-id="0b083-110">Costante</span><span class="sxs-lookup"><span data-stu-id="0b083-110">Constant</span></span>                            |
|---------|-------------|-------------------------------------|
| <span data-ttu-id="0b083-111">65536</span><span class="sxs-lookup"><span data-stu-id="0b083-111">65536</span></span>   | <span data-ttu-id="0b083-112">0x00010000</span><span class="sxs-lookup"><span data-stu-id="0b083-112">0x00010000</span></span>  | <span data-ttu-id="0b083-113">**msidbControlAttributesMultiline**</span><span class="sxs-lookup"><span data-stu-id="0b083-113">**msidbControlAttributesMultiline**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="0b083-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="0b083-114">Remarks</span></span>

<span data-ttu-id="0b083-115">Per impostare questo attributo su un controllo, includere il bit su più righe nella colonna attributi del record del controllo nella [tabella del controllo](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="0b083-115">To set this attribute on a control, include the MultiLine bit in the Attributes column of the control's record in the [Control table](control-table.md).</span></span>

<span data-ttu-id="0b083-116">Vedere [attributi](control-attributes.md) e [controlli](controls.md)del controllo.</span><span class="sxs-lookup"><span data-stu-id="0b083-116">See [Control Attributes](control-attributes.md) and [Controls](controls.md).</span></span>

 

 



