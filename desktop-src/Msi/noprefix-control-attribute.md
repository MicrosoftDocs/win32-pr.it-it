---
description: Se questo bit è impostato su un controllo di testo, l'occorrenza del carattere &\# 0034; &&\# 0034; in una stringa di testo viene visualizzata come se stessa. Se questo bit non è impostato, il carattere che segue &\# 0034; &&\# 0034; nella stringa di testo viene visualizzato come carattere di sottolineatura.
ms.assetid: b958eecb-2f44-420f-8c93-7a4bd8b589da
title: NoPrefix (attributo di controllo)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae1e1a0c6da65605efca1aacc4582b34a8f673d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226612"
---
# <a name="noprefix-control-attribute"></a><span data-ttu-id="27cee-104">NoPrefix (attributo di controllo)</span><span class="sxs-lookup"><span data-stu-id="27cee-104">NoPrefix Control Attribute</span></span>

<span data-ttu-id="27cee-105">Se questo bit è impostato su un controllo di testo, l'occorrenza del carattere "&" in una stringa di testo viene visualizzata come se stessa.</span><span class="sxs-lookup"><span data-stu-id="27cee-105">If this bit is set on a text control, the occurrence of the character "&" in a text string is displayed as itself.</span></span> <span data-ttu-id="27cee-106">Se questo bit non è impostato, il carattere che segue "&" nella stringa di testo viene visualizzato come carattere di sottolineatura.</span><span class="sxs-lookup"><span data-stu-id="27cee-106">If this bit is not set, then the character following "&" in the text string is displayed as an underscored character.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="27cee-107">Controlli validi</span><span class="sxs-lookup"><span data-stu-id="27cee-107">Valid Controls</span></span>

[<span data-ttu-id="27cee-108">Text</span><span class="sxs-lookup"><span data-stu-id="27cee-108">Text</span></span>](text-control.md)

## <a name="value"></a><span data-ttu-id="27cee-109">Valore</span><span class="sxs-lookup"><span data-stu-id="27cee-109">Value</span></span>



| <span data-ttu-id="27cee-110">Decimal</span><span class="sxs-lookup"><span data-stu-id="27cee-110">Decimal</span></span> | <span data-ttu-id="27cee-111">Valore esadecimale</span><span class="sxs-lookup"><span data-stu-id="27cee-111">Hexadecimal</span></span> | <span data-ttu-id="27cee-112">Costante</span><span class="sxs-lookup"><span data-stu-id="27cee-112">Constant</span></span>                           |
|---------|-------------|------------------------------------|
| <span data-ttu-id="27cee-113">131072</span><span class="sxs-lookup"><span data-stu-id="27cee-113">131072</span></span>  | <span data-ttu-id="27cee-114">0x20000</span><span class="sxs-lookup"><span data-stu-id="27cee-114">0x20000</span></span>     | <span data-ttu-id="27cee-115">**msidbControlAttributesNoPrefix**</span><span class="sxs-lookup"><span data-stu-id="27cee-115">**msidbControlAttributesNoPrefix**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="27cee-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="27cee-116">Remarks</span></span>

<span data-ttu-id="27cee-117">Per impostare questo attributo su un controllo, includere il bit NoPrefix nella colonna attributi del record del controllo nella [tabella dei controlli](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="27cee-117">To set this attribute on a control, include the NoPrefix bit in the Attributes column of the control's record in the [Control table](control-table.md).</span></span>

<span data-ttu-id="27cee-118">Vedere [attributi](control-attributes.md) e [controlli](controls.md)del controllo.</span><span class="sxs-lookup"><span data-stu-id="27cee-118">See [Control Attributes](control-attributes.md) and [Controls](controls.md).</span></span>

 

 



