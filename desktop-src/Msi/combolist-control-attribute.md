---
description: Se il bit del controllo ComboBox è impostato su una casella combinata, il campo Edit viene sostituito da un campo di testo statico. In questo modo si impedisce a un utente di immettere un nuovo valore e l'utente deve scegliere solo uno dei valori predefiniti.
ms.assetid: 79af4bb0-1e0f-4df3-ae25-d2798842adb6
title: Attributo del controllo combogroup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2dcb1c51e8eccaba03c3b4d905b0501e8a3f97a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315481"
---
# <a name="combolist-control-attribute"></a><span data-ttu-id="fb2ac-104">Attributo del controllo combogroup</span><span class="sxs-lookup"><span data-stu-id="fb2ac-104">ComboList Control Attribute</span></span>

<span data-ttu-id="fb2ac-105">Se il bit del controllo ComboBox è impostato su una casella combinata, il campo Edit viene sostituito da un campo di testo statico.</span><span class="sxs-lookup"><span data-stu-id="fb2ac-105">If the ComboList Control bit is set on a combo box, the edit field is replaced by a static text field.</span></span> <span data-ttu-id="fb2ac-106">In questo modo si impedisce a un utente di immettere un nuovo valore e l'utente deve scegliere solo uno dei valori predefiniti.</span><span class="sxs-lookup"><span data-stu-id="fb2ac-106">This prevents a user from entering a new value and requires the user to choose only one of the predefined values.</span></span>

<span data-ttu-id="fb2ac-107">Se questo bit non è impostato, la casella combinata dispone di un campo di modifica.</span><span class="sxs-lookup"><span data-stu-id="fb2ac-107">If this bit is not set, the combo box has an edit field.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="fb2ac-108">Controlli validi</span><span class="sxs-lookup"><span data-stu-id="fb2ac-108">Valid Controls</span></span>

[<span data-ttu-id="fb2ac-109">ComboBox</span><span class="sxs-lookup"><span data-stu-id="fb2ac-109">ComboBox</span></span>](combobox-control.md)

## <a name="value"></a><span data-ttu-id="fb2ac-110">Valore</span><span class="sxs-lookup"><span data-stu-id="fb2ac-110">Value</span></span>



| <span data-ttu-id="fb2ac-111">Decimal</span><span class="sxs-lookup"><span data-stu-id="fb2ac-111">Decimal</span></span> | <span data-ttu-id="fb2ac-112">Valore esadecimale</span><span class="sxs-lookup"><span data-stu-id="fb2ac-112">Hexadecimal</span></span> | <span data-ttu-id="fb2ac-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fb2ac-113">Description</span></span>                     |
|---------|-------------|---------------------------------|
| <span data-ttu-id="fb2ac-114">131072</span><span class="sxs-lookup"><span data-stu-id="fb2ac-114">131072</span></span>  | <span data-ttu-id="fb2ac-115">0x00020000</span><span class="sxs-lookup"><span data-stu-id="fb2ac-115">0x00020000</span></span>  | <span data-ttu-id="fb2ac-116">msidbControlAttributesComboList</span><span class="sxs-lookup"><span data-stu-id="fb2ac-116">msidbControlAttributesComboList</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="fb2ac-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="fb2ac-117">Remarks</span></span>

<span data-ttu-id="fb2ac-118">Per impostare questo attributo su un controllo, includere il bit dell'oggetto ComboBox nella colonna attributi del record del controllo nella tabella dei [controlli](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="fb2ac-118">To set this attribute on a control, include the ComboList bit in the Attributes column of the control's record in the [Control table](control-table.md).</span></span>

<span data-ttu-id="fb2ac-119">Vedere [gli attributi del controllo](control-attributes.md) e il controllo che è necessario creare sotto i [controlli](controls.md).</span><span class="sxs-lookup"><span data-stu-id="fb2ac-119">See [Control Attributes](control-attributes.md) and the control you need to create under [Controls](controls.md).</span></span>

 

 



