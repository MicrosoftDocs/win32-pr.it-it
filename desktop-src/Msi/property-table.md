---
description: La tabella delle proprietà contiene i nomi e i valori delle proprietà per tutte le proprietà definite nell'installazione. Le proprietà con valori null non sono presenti nella tabella.
ms.assetid: 1f4215b2-dc71-4e6e-bc2e-3b43316806b9
title: Tabella delle proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 612ab63aa36de6cf91ec8176eefec84cef591c55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756482"
---
# <a name="property-table"></a><span data-ttu-id="5b83c-104">Tabella delle proprietà</span><span class="sxs-lookup"><span data-stu-id="5b83c-104">Property Table</span></span>

<span data-ttu-id="5b83c-105">La tabella delle proprietà contiene i nomi e i valori delle proprietà per tutte le proprietà definite nell'installazione.</span><span class="sxs-lookup"><span data-stu-id="5b83c-105">The Property table contains the property names and values for all defined properties in the installation.</span></span> <span data-ttu-id="5b83c-106">Le proprietà con valori null non sono presenti nella tabella.</span><span class="sxs-lookup"><span data-stu-id="5b83c-106">Properties with Null values are not present in the table.</span></span>

<span data-ttu-id="5b83c-107">La tabella delle proprietà contiene le colonne seguenti.</span><span class="sxs-lookup"><span data-stu-id="5b83c-107">The Property table has the following columns.</span></span>



| <span data-ttu-id="5b83c-108">Colonna</span><span class="sxs-lookup"><span data-stu-id="5b83c-108">Column</span></span>   | <span data-ttu-id="5b83c-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="5b83c-109">Type</span></span>                         | <span data-ttu-id="5b83c-110">Chiave</span><span class="sxs-lookup"><span data-stu-id="5b83c-110">Key</span></span> | <span data-ttu-id="5b83c-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="5b83c-111">Nullable</span></span> |
|----------|------------------------------|-----|----------|
| <span data-ttu-id="5b83c-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5b83c-112">Property</span></span> | [<span data-ttu-id="5b83c-113">Identificatore</span><span class="sxs-lookup"><span data-stu-id="5b83c-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="5b83c-114">S</span><span class="sxs-lookup"><span data-stu-id="5b83c-114">Y</span></span>   | <span data-ttu-id="5b83c-115">N</span><span class="sxs-lookup"><span data-stu-id="5b83c-115">N</span></span>        |
| <span data-ttu-id="5b83c-116">Valore</span><span class="sxs-lookup"><span data-stu-id="5b83c-116">Value</span></span>    | [<span data-ttu-id="5b83c-117">Text</span><span class="sxs-lookup"><span data-stu-id="5b83c-117">Text</span></span>](text.md)             | <span data-ttu-id="5b83c-118">N</span><span class="sxs-lookup"><span data-stu-id="5b83c-118">N</span></span>   | <span data-ttu-id="5b83c-119">N</span><span class="sxs-lookup"><span data-stu-id="5b83c-119">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="5b83c-120">Colonne</span><span class="sxs-lookup"><span data-stu-id="5b83c-120">Columns</span></span>

<dl> <dt>

<span data-ttu-id="5b83c-121"><span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Proprietà</span><span class="sxs-lookup"><span data-stu-id="5b83c-121"><span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Property</span></span>
</dt> <dd>

<span data-ttu-id="5b83c-122">Il nome di una proprietà.</span><span class="sxs-lookup"><span data-stu-id="5b83c-122">The name of a property.</span></span> <span data-ttu-id="5b83c-123">Vedere [Proprietà](properties.md).</span><span class="sxs-lookup"><span data-stu-id="5b83c-123">See [Properties](properties.md).</span></span>

</dd> <dt>

<span data-ttu-id="5b83c-124"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valore</span><span class="sxs-lookup"><span data-stu-id="5b83c-124"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Value</span></span>
</dt> <dd>

<span data-ttu-id="5b83c-125">Valore stringa localizzabile per la proprietà.</span><span class="sxs-lookup"><span data-stu-id="5b83c-125">A localizable string value for the property.</span></span> <span data-ttu-id="5b83c-126">Non può mai essere null o una stringa vuota.</span><span class="sxs-lookup"><span data-stu-id="5b83c-126">This may never be Null or an empty string.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5b83c-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="5b83c-127">Remarks</span></span>

<span data-ttu-id="5b83c-128">Si noti che non è possibile utilizzare la tabella delle proprietà per impostare una proprietà sul valore di un'altra proprietà.</span><span class="sxs-lookup"><span data-stu-id="5b83c-128">Note that you cannot use the Property table to set a property to the value of another property.</span></span> <span data-ttu-id="5b83c-129">Il programma di installazione non esegue alcuna operazione sulla stringa di testo immessa nella colonna valore prima di impostare la proprietà nella colonna proprietà.</span><span class="sxs-lookup"><span data-stu-id="5b83c-129">The installer does nothing to the text string entered in the Value column before setting the property in the Property column.</span></span> <span data-ttu-id="5b83c-130">Se FirstProperty viene immesso nella colonna proprietà e \[ SecondProperty \] nella colonna valore, il valore di FirstProperty viene impostato sulla stringa di testo " \[ SecondProperty \] " e non sul valore della proprietà SecondProperty.</span><span class="sxs-lookup"><span data-stu-id="5b83c-130">If FirstProperty is entered into the Property column and \[SecondProperty\] in the Value column, the value of FirstProperty is set to the text string "\[SecondProperty\]" and not to the value of the SecondProperty property.</span></span> <span data-ttu-id="5b83c-131">Questa operazione è necessaria per evitare la creazione di riferimenti circolari nella tabella delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="5b83c-131">This is necessary to prevent creating circular references in the Property table.</span></span> <span data-ttu-id="5b83c-132">È invece possibile impostare una proprietà su un'altra usando un' [azione personalizzata di tipo 51](custom-action-type-51.md).</span><span class="sxs-lookup"><span data-stu-id="5b83c-132">Instead, you can set one property to another by using a [Custom Action Type 51](custom-action-type-51.md).</span></span>

<span data-ttu-id="5b83c-133">Si noti che la proprietà [**AdminProperties**](adminproperties.md) può essere utilizzata per eseguire l'override dei valori nella tabella delle proprietà durante un' [installazione amministrativa](administrative-installation.md).</span><span class="sxs-lookup"><span data-stu-id="5b83c-133">Note that the [**AdminProperties**](adminproperties.md) property can be used to override the values in the Property table during an [Administrative Installation](administrative-installation.md).</span></span>

<span data-ttu-id="5b83c-134">Non usare le proprietà per le password o altre informazioni che devono rimanere sicure.</span><span class="sxs-lookup"><span data-stu-id="5b83c-134">Do not use properties for passwords or other information that must remain secure.</span></span> <span data-ttu-id="5b83c-135">Il programma di installazione può scrivere il valore di una proprietà creata nella tabella delle proprietà o creato in fase di esecuzione in un log o nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="5b83c-135">The installer may write the value of a property authored into the Property table, or created at runtime, into a log or the system registry.</span></span>

## <a name="validation"></a><span data-ttu-id="5b83c-136">Convalida</span><span class="sxs-lookup"><span data-stu-id="5b83c-136">Validation</span></span>

<dl>

[<span data-ttu-id="5b83c-137">ICE03</span><span class="sxs-lookup"><span data-stu-id="5b83c-137">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="5b83c-138">ICE05</span><span class="sxs-lookup"><span data-stu-id="5b83c-138">ICE05</span></span>](ice05.md)  
[<span data-ttu-id="5b83c-139">ICE06</span><span class="sxs-lookup"><span data-stu-id="5b83c-139">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="5b83c-140">ICE16</span><span class="sxs-lookup"><span data-stu-id="5b83c-140">ICE16</span></span>](ice16.md)  
[<span data-ttu-id="5b83c-141">ICE24</span><span class="sxs-lookup"><span data-stu-id="5b83c-141">ICE24</span></span>](ice24.md)  
[<span data-ttu-id="5b83c-142">ICE31</span><span class="sxs-lookup"><span data-stu-id="5b83c-142">ICE31</span></span>](ice31.md)  
[<span data-ttu-id="5b83c-143">ICE34</span><span class="sxs-lookup"><span data-stu-id="5b83c-143">ICE34</span></span>](ice34.md)  
[<span data-ttu-id="5b83c-144">ICE36</span><span class="sxs-lookup"><span data-stu-id="5b83c-144">ICE36</span></span>](ice36.md)  
[<span data-ttu-id="5b83c-145">ICE40</span><span class="sxs-lookup"><span data-stu-id="5b83c-145">ICE40</span></span>](ice40.md)  
[<span data-ttu-id="5b83c-146">ICE46</span><span class="sxs-lookup"><span data-stu-id="5b83c-146">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="5b83c-147">ICE48</span><span class="sxs-lookup"><span data-stu-id="5b83c-147">ICE48</span></span>](ice48.md)  
[<span data-ttu-id="5b83c-148">ICE52</span><span class="sxs-lookup"><span data-stu-id="5b83c-148">ICE52</span></span>](ice52.md)  
[<span data-ttu-id="5b83c-149">ICE61</span><span class="sxs-lookup"><span data-stu-id="5b83c-149">ICE61</span></span>](ice61.md)  
[<span data-ttu-id="5b83c-150">ICE73</span><span class="sxs-lookup"><span data-stu-id="5b83c-150">ICE73</span></span>](ice73.md)  
[<span data-ttu-id="5b83c-151">ICE74</span><span class="sxs-lookup"><span data-stu-id="5b83c-151">ICE74</span></span>](ice74.md)  
[<span data-ttu-id="5b83c-152">ICE80</span><span class="sxs-lookup"><span data-stu-id="5b83c-152">ICE80</span></span>](ice80.md)  
[<span data-ttu-id="5b83c-153">ICE87</span><span class="sxs-lookup"><span data-stu-id="5b83c-153">ICE87</span></span>](ice87.md)  
[<span data-ttu-id="5b83c-154">ICE88</span><span class="sxs-lookup"><span data-stu-id="5b83c-154">ICE88</span></span>](ice88.md)  
[<span data-ttu-id="5b83c-155">ICE91</span><span class="sxs-lookup"><span data-stu-id="5b83c-155">ICE91</span></span>](ice91.md)  
[<span data-ttu-id="5b83c-156">ICE99</span><span class="sxs-lookup"><span data-stu-id="5b83c-156">ICE99</span></span>](ice99.md)  
</dl>

 

 



