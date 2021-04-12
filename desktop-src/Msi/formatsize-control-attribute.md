---
description: Se questo bit è impostato per un controllo testo statico, il controllo tenta automaticamente di formattare il testo visualizzato come numero che rappresenta un conteggio di byte.
ms.assetid: acf76fff-b7a4-456b-91b9-eb3087879d7b
title: Attributo di controllo FormatSize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d7fa656b81272b8ac60985d3dac0416c0f81bef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226615"
---
# <a name="formatsize-control-attribute"></a><span data-ttu-id="37952-103">Attributo di controllo FormatSize</span><span class="sxs-lookup"><span data-stu-id="37952-103">FormatSize Control Attribute</span></span>

<span data-ttu-id="37952-104">Se questo bit è impostato per un controllo testo statico, il controllo tenta automaticamente di formattare il testo visualizzato come numero che rappresenta un conteggio di byte.</span><span class="sxs-lookup"><span data-stu-id="37952-104">If this bit is set for a static text control, the control automatically attempts to format the displayed text as a number that represents a count of bytes.</span></span> <span data-ttu-id="37952-105">Per una corretta formattazione, il testo del controllo deve essere impostato su una stringa che rappresenta un numero espresso in unità di 512 byte.</span><span class="sxs-lookup"><span data-stu-id="37952-105">For proper formatting, the control's text must be set to a string that represents a number expressed in units of 512 bytes.</span></span> <span data-ttu-id="37952-106">Il valore visualizzato viene quindi formattato in kilobyte (KB), megabyte (MB) o gigabyte (GB) e visualizzato con la stringa appropriata che rappresenta le unità.</span><span class="sxs-lookup"><span data-stu-id="37952-106">The displayed value is then formatted in kilobytes (KB), megabytes (MB), or gigabytes (GB), and displayed with the appropriate string that represents the units.</span></span> <span data-ttu-id="37952-107">Per altre informazioni, vedere [controllo testo](text-control.md).</span><span class="sxs-lookup"><span data-stu-id="37952-107">For more information, see [Text Control](text-control.md).</span></span>



| <span data-ttu-id="37952-108">Valore numerico del testo originale</span><span class="sxs-lookup"><span data-stu-id="37952-108">Numerical value of original text</span></span> | <span data-ttu-id="37952-109">Stringa di unità utilizzata</span><span class="sxs-lookup"><span data-stu-id="37952-109">Unit string used</span></span> |
|----------------------------------|------------------|
| <span data-ttu-id="37952-110">Minore di 20480</span><span class="sxs-lookup"><span data-stu-id="37952-110">Less than 20480</span></span>                  | <span data-ttu-id="37952-111">KB</span><span class="sxs-lookup"><span data-stu-id="37952-111">KB</span></span>               |
| <span data-ttu-id="37952-112">Minore di 20971520</span><span class="sxs-lookup"><span data-stu-id="37952-112">Less than 20971520</span></span>               | <span data-ttu-id="37952-113">MB</span><span class="sxs-lookup"><span data-stu-id="37952-113">MB</span></span>               |
| <span data-ttu-id="37952-114">Minore di 10737418240</span><span class="sxs-lookup"><span data-stu-id="37952-114">Less than 10737418240</span></span>            | <span data-ttu-id="37952-115">GB</span><span class="sxs-lookup"><span data-stu-id="37952-115">GB</span></span>               |



 

## <a name="valid-controls"></a><span data-ttu-id="37952-116">Controlli validi</span><span class="sxs-lookup"><span data-stu-id="37952-116">Valid Controls</span></span>



| <span data-ttu-id="37952-117">Decimal</span><span class="sxs-lookup"><span data-stu-id="37952-117">Decimal</span></span> | <span data-ttu-id="37952-118">Valore esadecimale</span><span class="sxs-lookup"><span data-stu-id="37952-118">Hexadecimal</span></span> | <span data-ttu-id="37952-119">Control</span><span class="sxs-lookup"><span data-stu-id="37952-119">Control</span></span>                          |
|---------|-------------|----------------------------------|
| <span data-ttu-id="37952-120">524288</span><span class="sxs-lookup"><span data-stu-id="37952-120">524288</span></span>  | <span data-ttu-id="37952-121">0x00080000</span><span class="sxs-lookup"><span data-stu-id="37952-121">0x00080000</span></span>  | <span data-ttu-id="37952-122">msidbControlAttributesFormatSize</span><span class="sxs-lookup"><span data-stu-id="37952-122">msidbControlAttributesFormatSize</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="37952-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="37952-123">Remarks</span></span>

<span data-ttu-id="37952-124">Per impostare questo attributo su un controllo, includere i bit FormatSize nella colonna Attributes del record del controllo nella tabella del [controllo](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="37952-124">To set this attribute on a control, include the FormatSize bits in the Attributes column of the control's record in the [Control Table](control-table.md).</span></span> <span data-ttu-id="37952-125">Il testo del controllo deve essere impostato su una stringa che rappresenta un numero espresso in unità di 512 byte.</span><span class="sxs-lookup"><span data-stu-id="37952-125">The control's text must be set to a string representing a number expressed in units of 512 bytes.</span></span> <span data-ttu-id="37952-126">Il testo delle stringhe di unità viene definito nella [tabella UIText](uitext-table.md).</span><span class="sxs-lookup"><span data-stu-id="37952-126">The text of the unit strings are defined in the [UIText Table](uitext-table.md).</span></span> <span data-ttu-id="37952-127">Il posizionamento della stringa di unità è controllato dalla proprietà [**LeftUnit**](leftunit.md) .</span><span class="sxs-lookup"><span data-stu-id="37952-127">The positioning of the unit string is controlled by the [**LeftUnit**](leftunit.md) Property.</span></span> <span data-ttu-id="37952-128">Se la proprietà **LeftUnit** è definita come qualsiasi valore, la stringa di unità viene visualizzata prima del valore numerico.</span><span class="sxs-lookup"><span data-stu-id="37952-128">If the **LeftUnit** Property is defined to be any value, the unit string appears before the numerical value.</span></span> <span data-ttu-id="37952-129">Se nel testo associato al controllo è presente un valore diverso da caratteri numerici, il valore visualizzato non è definito.</span><span class="sxs-lookup"><span data-stu-id="37952-129">If anything other than numerical characters appears in the text associated with the control, the displayed value is undefined.</span></span>

<span data-ttu-id="37952-130">In fase di esecuzione, il programma di installazione risolve la proprietà [**PrimaryVolumeSpaceRequired**](primaryvolumespacerequired.md) nel numero totale di byte necessari per l'installazione in unità di 512.</span><span class="sxs-lookup"><span data-stu-id="37952-130">At run time, the installer resolves the [**PrimaryVolumeSpaceRequired**](primaryvolumespacerequired.md) Property to the total number of bytes required for the installation in units of 512.</span></span> <span data-ttu-id="37952-131">Un controllo testo statico con bit FormatSize può essere usato per formattare automaticamente ed etichettare il numero totale di byte necessari per l'installazione in KB, MB o GB, a seconda dei casi.</span><span class="sxs-lookup"><span data-stu-id="37952-131">A static text control with FormatSize bit can be used to automatically format and label the total number of bytes required for the installation in KB, MB, or GB as appropriate.</span></span> <span data-ttu-id="37952-132">Ai fini di questo esempio, si supponga che il numero totale di byte sia 18.336.768.</span><span class="sxs-lookup"><span data-stu-id="37952-132">For the purposes of this example, assume the total number of bytes is 18,336,768.</span></span> <span data-ttu-id="37952-133">Il programma di installazione imposta il valore della proprietà PrimaryVolumeSpaceRequired su 18.336.768 diviso per 512 o 35.814.</span><span class="sxs-lookup"><span data-stu-id="37952-133">The installer sets the value of the PrimaryVolumeSpaceRequired property to 18,336,768 divided by 512, or 35,814.</span></span> <span data-ttu-id="37952-134">Il numero visualizzato dal controllo testo con FormatSize è 17MB.</span><span class="sxs-lookup"><span data-stu-id="37952-134">The number displayed by the text control with FormatSize would be 17MB.</span></span>

<span data-ttu-id="37952-135">I valori numerici del testo originale sono espressi in unità di 512.</span><span class="sxs-lookup"><span data-stu-id="37952-135">The numerical values of the original text are given in units of 512.</span></span> <span data-ttu-id="37952-136">Nella tabella precedente la stringa 20.480 corrisponde alla stringa KB perché 20.480 volte 512 restituisce un risultato di 10.485.760 byte o 10.240 KB.</span><span class="sxs-lookup"><span data-stu-id="37952-136">In the table above, the string 20,480 corresponds to the KB string because 20,480 times 512 yields a result of 10,485,760 bytes or 10,240 KB.</span></span>

<span data-ttu-id="37952-137">Le stringhe di unità elencate nella tabella precedente si riferiscono alle chiavi della [tabella UIText](uitext-table.md), in cui è definito il testo della stringa di unità.</span><span class="sxs-lookup"><span data-stu-id="37952-137">The unit strings listed in the previous table refer to keys in the [UIText Table](uitext-table.md), where the text of the unit string is defined.</span></span>

<span data-ttu-id="37952-138">Il posizionamento della stringa di unità è controllato dalla proprietà [**LeftUnit**](leftunit.md) .</span><span class="sxs-lookup"><span data-stu-id="37952-138">The positioning of the unit string is controlled by the [**LeftUnit**](leftunit.md) Property.</span></span> <span data-ttu-id="37952-139">Se la proprietà **LeftUnit** è definita come qualsiasi valore, la stringa di unità viene visualizzata prima del valore numerico.</span><span class="sxs-lookup"><span data-stu-id="37952-139">If the **LeftUnit** Property is defined to be any value, the unit string appears before the numerical value.</span></span>

<span data-ttu-id="37952-140">Se nel testo associato al controllo è presente un valore diverso da caratteri numerici, il valore visualizzato non è definito.</span><span class="sxs-lookup"><span data-stu-id="37952-140">If anything other than numerical characters appears in the text associated with the control, the displayed value is undefined.</span></span>

<span data-ttu-id="37952-141">Per altre informazioni, vedere [controllare gli attributi](control-attributes.md) e i [controlli](controls.md).</span><span class="sxs-lookup"><span data-stu-id="37952-141">For more information, see [Control Attributes](control-attributes.md) and [Controls](controls.md).</span></span>

 

 



