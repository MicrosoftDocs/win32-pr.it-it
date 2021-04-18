---
description: Se viene impostato il bit del controllo visibile, il controllo è visibile nella finestra di dialogo. Se questo bit non è impostato, il controllo è nascosto nella finestra di dialogo. Lo stato visibile o nascosto dell'attributo del controllo visibile può essere modificato in seguito da un evento del controllo.
ms.assetid: 77d3164c-ea8a-4dcf-afd5-02bb2c2568c6
title: Attributo controllo visibile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 550513f6bd0e40e58694c2c15a9986b5b02f289c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306565"
---
# <a name="visible-control-attribute"></a><span data-ttu-id="c83fd-105">Attributo controllo visibile</span><span class="sxs-lookup"><span data-stu-id="c83fd-105">Visible Control Attribute</span></span>

<span data-ttu-id="c83fd-106">Se viene impostato il bit del controllo visibile, il controllo è visibile nella finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="c83fd-106">If the Visible Control bit is set, the control is visible on the dialog box.</span></span> <span data-ttu-id="c83fd-107">Se questo bit non è impostato, il controllo è nascosto nella finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="c83fd-107">If this bit is not set, the control is hidden on the dialog box.</span></span> <span data-ttu-id="c83fd-108">Lo stato visibile o nascosto dell'attributo del controllo visibile può essere modificato in seguito da un [evento del controllo](control-events.md).</span><span class="sxs-lookup"><span data-stu-id="c83fd-108">The visible or hidden state of the Visible control attribute can be later changed by a [Control Event](control-events.md).</span></span>

## <a name="valid-controls"></a><span data-ttu-id="c83fd-109">Controlli validi</span><span class="sxs-lookup"><span data-stu-id="c83fd-109">Valid Controls</span></span>

<span data-ttu-id="c83fd-110">Tutti i controlli.</span><span class="sxs-lookup"><span data-stu-id="c83fd-110">All controls.</span></span>

## <a name="value"></a><span data-ttu-id="c83fd-111">Valore</span><span class="sxs-lookup"><span data-stu-id="c83fd-111">Value</span></span>



| <span data-ttu-id="c83fd-112">Decimal</span><span class="sxs-lookup"><span data-stu-id="c83fd-112">Decimal</span></span> | <span data-ttu-id="c83fd-113">Valore esadecimale</span><span class="sxs-lookup"><span data-stu-id="c83fd-113">Hexadecimal</span></span> | <span data-ttu-id="c83fd-114">Costante</span><span class="sxs-lookup"><span data-stu-id="c83fd-114">Constant</span></span>                          |
|---------|-------------|-----------------------------------|
| <span data-ttu-id="c83fd-115">1</span><span class="sxs-lookup"><span data-stu-id="c83fd-115">1</span></span>       | <span data-ttu-id="c83fd-116">0x00000001</span><span class="sxs-lookup"><span data-stu-id="c83fd-116">0x00000001</span></span>  | <span data-ttu-id="c83fd-117">**msidbControlAttributesVisible**</span><span class="sxs-lookup"><span data-stu-id="c83fd-117">**msidbControlAttributesVisible**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="c83fd-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="c83fd-118">Remarks</span></span>

<span data-ttu-id="c83fd-119">È possibile utilizzare la [tabella ControlCondition](controlcondition-table.md) per visualizzare o nascondere un controllo in base al valore di una proprietà o di un'istruzione condizionale.</span><span class="sxs-lookup"><span data-stu-id="c83fd-119">You can use the [ControlCondition table](controlcondition-table.md) to show or hide a control according to the value of a property or conditional statement.</span></span> <span data-ttu-id="c83fd-120">È anche possibile visualizzare o nascondere un controllo sottoscrivendo il controllo a un [ControlEvent](control-events.md).</span><span class="sxs-lookup"><span data-stu-id="c83fd-120">You can also show or hide a control by subscribing the control to a [ControlEvent](control-events.md).</span></span> <span data-ttu-id="c83fd-121">Immettere l'identificatore dell'attributo nella colonna Attribute e l'identificatore dell'evento nella colonna Event della [tabella EventMapping](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="c83fd-121">Enter the attribute's identifier in the Attribute column and the event's identifier in the Event column of the [EventMapping table](eventmapping-table.md).</span></span>

<span data-ttu-id="c83fd-122">Vedere [attributi](control-attributes.md) e [controlli](controls.md)del controllo.</span><span class="sxs-lookup"><span data-stu-id="c83fd-122">See [Control Attributes](control-attributes.md) and [Controls](controls.md).</span></span>

 

 



