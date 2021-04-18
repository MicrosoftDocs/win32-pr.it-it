---
description: Questo attributo specifica se il controllo specificato è abilitato o disabilitato. La maggior parte dei controlli è grigio quando è disabilitata.
ms.assetid: d84b1b55-34e1-4173-b945-39a809014d55
title: Attributo di controllo abilitato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb7c5cbbbc12353fc07cf50404a1feae1d98f1b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309488"
---
# <a name="enabled-control-attribute"></a><span data-ttu-id="54017-104">Attributo di controllo abilitato</span><span class="sxs-lookup"><span data-stu-id="54017-104">Enabled Control Attribute</span></span>

<span data-ttu-id="54017-105">Questo attributo specifica se il controllo specificato è abilitato o disabilitato.</span><span class="sxs-lookup"><span data-stu-id="54017-105">This attribute specifies if the given control is enabled or disabled.</span></span> <span data-ttu-id="54017-106">La maggior parte dei controlli è grigio quando è disabilitata.</span><span class="sxs-lookup"><span data-stu-id="54017-106">Most controls appear gray when disabled.</span></span>

<span data-ttu-id="54017-107">Se questo bit è impostato, il controllo viene creato come abilitato.</span><span class="sxs-lookup"><span data-stu-id="54017-107">If this bit is set, the control is created as enabled.</span></span>

<span data-ttu-id="54017-108">Se questo bit non è impostato, il controllo viene creato come disabilitato.</span><span class="sxs-lookup"><span data-stu-id="54017-108">If this bit is not set, the control is created as disabled.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="54017-109">Controlli validi</span><span class="sxs-lookup"><span data-stu-id="54017-109">Valid Controls</span></span>

<span data-ttu-id="54017-110">Tutti i controlli.</span><span class="sxs-lookup"><span data-stu-id="54017-110">All controls.</span></span> <span data-ttu-id="54017-111">L'aspetto di alcuni controlli che non sono associati a una proprietà, ad esempio bitmap e icone, non è influenzato dall'impostazione di questo attributo.</span><span class="sxs-lookup"><span data-stu-id="54017-111">The appearance of some controls that are not associated with a property, such as Bitmaps and Icons, are unaffected by setting this attribute.</span></span>

## <a name="value"></a><span data-ttu-id="54017-112">Valore</span><span class="sxs-lookup"><span data-stu-id="54017-112">Value</span></span>



| <span data-ttu-id="54017-113">Decimal</span><span class="sxs-lookup"><span data-stu-id="54017-113">Decimal</span></span> | <span data-ttu-id="54017-114">Valore esadecimale</span><span class="sxs-lookup"><span data-stu-id="54017-114">Hexadecimal</span></span> | <span data-ttu-id="54017-115">Costante</span><span class="sxs-lookup"><span data-stu-id="54017-115">Constant</span></span>                          |
|---------|-------------|-----------------------------------|
| <span data-ttu-id="54017-116">2</span><span class="sxs-lookup"><span data-stu-id="54017-116">2</span></span>       | <span data-ttu-id="54017-117">0x00000002</span><span class="sxs-lookup"><span data-stu-id="54017-117">0x00000002</span></span>  | <span data-ttu-id="54017-118">**msidbControlAttributesEnabled**</span><span class="sxs-lookup"><span data-stu-id="54017-118">**msidbControlAttributesEnabled**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="54017-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="54017-119">Remarks</span></span>

<span data-ttu-id="54017-120">È anche possibile usare la [tabella ControlCondition](controlcondition-table.md) per disabilitare o abilitare un controllo in base al valore di una proprietà o di un'istruzione condizionale.</span><span class="sxs-lookup"><span data-stu-id="54017-120">You can also use the [ControlCondition table](controlcondition-table.md) to disable or enable a control according to the value of a property or conditional statement.</span></span>

<span data-ttu-id="54017-121">È anche possibile abilitare o disabilitare un controllo sottoscrivendo il controllo a un [ControlEvent](control-events.md).</span><span class="sxs-lookup"><span data-stu-id="54017-121">You can also enable or disable a control by subscribing the control to a [ControlEvent](control-events.md).</span></span> <span data-ttu-id="54017-122">Immettere l'identificatore dell'attributo nella colonna Attribute e l'identificatore dell'evento nella colonna Event della [tabella EventMapping](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="54017-122">Enter the attribute's identifier in the Attribute column and the event's identifier in the Event column of the [EventMapping table](eventmapping-table.md).</span></span>

<span data-ttu-id="54017-123">Vedere [gli attributi del controllo](control-attributes.md) e il controllo che è necessario creare sotto i [controlli](controls.md).</span><span class="sxs-lookup"><span data-stu-id="54017-123">See [Control Attributes](control-attributes.md) and the control you need to create under [Controls](controls.md).</span></span>

 

 



