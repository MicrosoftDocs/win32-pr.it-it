---
description: Le convenzioni testuali SNMP sono mappate ai tipi definiti CIM.
ms.assetid: 73bb6c22-0a68-4a4b-8de2-8326ec67a059
ms.tgt_platform: multiple
title: Macro convenzione testuale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 329508ce3d124c0b3954675b3142aeb33c402923
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309765"
---
# <a name="textual-convention-macro"></a><span data-ttu-id="6bf12-103">Macro convenzione testuale</span><span class="sxs-lookup"><span data-stu-id="6bf12-103">TEXTUAL-CONVENTION Macro</span></span>

<span data-ttu-id="6bf12-104">Le convenzioni testuali SNMP sono mappate ai tipi definiti CIM.</span><span class="sxs-lookup"><span data-stu-id="6bf12-104">SNMP textual conventions map to CIM-defined types.</span></span>

> [!Note]  
> <span data-ttu-id="6bf12-105">Per ulteriori informazioni sull'installazione del provider, vedere [configurazione dell'ambiente WMI SNMP](setting-up-the-wmi-snmp-environment.md).</span><span class="sxs-lookup"><span data-stu-id="6bf12-105">For more information about installing the provider, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

 

<span data-ttu-id="6bf12-106">Le regole di mapping seguenti si applicano alle convenzioni testuali SNMP:</span><span class="sxs-lookup"><span data-stu-id="6bf12-106">The following mapping rules apply to SNMP textual conventions:</span></span>

-   <span data-ttu-id="6bf12-107">La definizione del tipo denominato nella clausola della sintassi esegue il mapping Verbatim alla **\_ sintassi dell'oggetto** qualificatore della proprietà CIM.</span><span class="sxs-lookup"><span data-stu-id="6bf12-107">The named type definition in the SYNTAX clause maps verbatim to the CIM property qualifier **object\_syntax**.</span></span>
-   <span data-ttu-id="6bf12-108">Usare la tabella seguente per eseguire il mapping delle convenzioni testuali quando la clausola della sintassi fa riferimento in modo esplicito a una convenzione testuale di una macro della convenzione testuale SNMPv2C o fa riferimento a una convenzione testuale implicita.</span><span class="sxs-lookup"><span data-stu-id="6bf12-108">Use the following table to map textual conventions when the SYNTAX clause explicitly refers to a textual convention of a SNMPv2C TEXTUAL-CONVENTION macro, or refers to an implied textual convention.</span></span> <span data-ttu-id="6bf12-109">Il valore predefinito è sempre **null**.</span><span class="sxs-lookup"><span data-stu-id="6bf12-109">The default value is always **NULL**.</span></span>



| <span data-ttu-id="6bf12-110">Convenzione testuale</span><span class="sxs-lookup"><span data-stu-id="6bf12-110">Textual convention</span></span> | <span data-ttu-id="6bf12-111">Tipo Variant CIM</span><span class="sxs-lookup"><span data-stu-id="6bf12-111">CIM variant type</span></span> | <span data-ttu-id="6bf12-112">Qualificatore CIM</span><span class="sxs-lookup"><span data-stu-id="6bf12-112">CIM qualifier</span></span>                                                                                                                                                        |
|--------------------|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6bf12-113">DateAndTime</span><span class="sxs-lookup"><span data-stu-id="6bf12-113">DateAndTime</span></span>        | <span data-ttu-id="6bf12-114">**\_BSTR VT**</span><span class="sxs-lookup"><span data-stu-id="6bf12-114">**VT\_BSTR**</span></span>     | <span data-ttu-id="6bf12-115">**\_ convenzione testuale**: DateAndTime</span><span class="sxs-lookup"><span data-stu-id="6bf12-115">**textual\_convention**: DateAndTime</span></span><br/> <span data-ttu-id="6bf12-116">**codifica**: OCTETSTRING</span><span class="sxs-lookup"><span data-stu-id="6bf12-116">**encoding**: OCTETSTRING</span></span><br/> <span data-ttu-id="6bf12-117">**\_ sintassi dell'oggetto**: DateAndTime</span><span class="sxs-lookup"><span data-stu-id="6bf12-117">**object\_syntax**: DateAndTime</span></span><br/> <span data-ttu-id="6bf12-118">**CimType**: stringa</span><span class="sxs-lookup"><span data-stu-id="6bf12-118">**cimtype**: string</span></span><br/>       |
| <span data-ttu-id="6bf12-119">DisplayString</span><span class="sxs-lookup"><span data-stu-id="6bf12-119">Displaystring</span></span>      | <span data-ttu-id="6bf12-120">**\_BSTR VT**</span><span class="sxs-lookup"><span data-stu-id="6bf12-120">**VT\_BSTR**</span></span>     | <span data-ttu-id="6bf12-121">**\_ convenzione testuale**: DisplayString</span><span class="sxs-lookup"><span data-stu-id="6bf12-121">**textual\_convention**: Displaystring</span></span><br/> <span data-ttu-id="6bf12-122">**codifica**: OCTETSTRING</span><span class="sxs-lookup"><span data-stu-id="6bf12-122">**encoding**: OCTETSTRING</span></span><br/> <span data-ttu-id="6bf12-123">**\_ sintassi dell'oggetto**: DisplayString</span><span class="sxs-lookup"><span data-stu-id="6bf12-123">**object\_syntax**: Displaystring</span></span><br/> <span data-ttu-id="6bf12-124">**CimType**: stringa</span><span class="sxs-lookup"><span data-stu-id="6bf12-124">**cimtype**: string</span></span><br/>   |
| <span data-ttu-id="6bf12-125">MacAddress</span><span class="sxs-lookup"><span data-stu-id="6bf12-125">MacAddress</span></span>         | <span data-ttu-id="6bf12-126">**\_BSTR VT**</span><span class="sxs-lookup"><span data-stu-id="6bf12-126">**VT\_BSTR**</span></span>     | <span data-ttu-id="6bf12-127">**\_ convenzione testuale**: MacAddress</span><span class="sxs-lookup"><span data-stu-id="6bf12-127">**textual\_convention**: MacAddress</span></span><br/> <span data-ttu-id="6bf12-128">**codifica**: OCTETSTRING</span><span class="sxs-lookup"><span data-stu-id="6bf12-128">**encoding**: OCTETSTRING</span></span><br/> <span data-ttu-id="6bf12-129">**\_ sintassi dell'oggetto**: MacAddress</span><span class="sxs-lookup"><span data-stu-id="6bf12-129">**object\_syntax**: MacAddress</span></span><br/> <span data-ttu-id="6bf12-130">**CimType**: stringa</span><span class="sxs-lookup"><span data-stu-id="6bf12-130">**cimtype**: string</span></span><br/>         |
| <span data-ttu-id="6bf12-131">PhysAddress</span><span class="sxs-lookup"><span data-stu-id="6bf12-131">PhysAddress</span></span>        | <span data-ttu-id="6bf12-132">**\_BSTR VT**</span><span class="sxs-lookup"><span data-stu-id="6bf12-132">**VT\_BSTR**</span></span>     | <span data-ttu-id="6bf12-133">**\_ convenzione testuale**: PhysAddress</span><span class="sxs-lookup"><span data-stu-id="6bf12-133">**textual\_convention**: PhysAddress</span></span><br/> <span data-ttu-id="6bf12-134">**codifica**: OCTETSTRING</span><span class="sxs-lookup"><span data-stu-id="6bf12-134">**encoding**: OCTETSTRING</span></span><br/> <span data-ttu-id="6bf12-135">**\_ sintassi dell'oggetto**: PhysAddress</span><span class="sxs-lookup"><span data-stu-id="6bf12-135">**object\_syntax**: PhysAddress</span></span><br/> <span data-ttu-id="6bf12-136">**CimType**: stringa</span><span class="sxs-lookup"><span data-stu-id="6bf12-136">**cimtype**: string</span></span><br/>       |
| <span data-ttu-id="6bf12-137">SnmpUDPAddress</span><span class="sxs-lookup"><span data-stu-id="6bf12-137">SnmpUDPAddress</span></span>     | <span data-ttu-id="6bf12-138">**\_BSTR VT**</span><span class="sxs-lookup"><span data-stu-id="6bf12-138">**VT\_BSTR**</span></span>     | <span data-ttu-id="6bf12-139">**\_ convenzione testuale**: SnmpUDPAddress</span><span class="sxs-lookup"><span data-stu-id="6bf12-139">**textual\_convention**: SnmpUDPAddress</span></span><br/> <span data-ttu-id="6bf12-140">**codifica**: OCTETSTRING</span><span class="sxs-lookup"><span data-stu-id="6bf12-140">**encoding**: OCTETSTRING</span></span><br/> <span data-ttu-id="6bf12-141">**\_ sintassi dell'oggetto**: SnmpUDPAddress</span><span class="sxs-lookup"><span data-stu-id="6bf12-141">**object\_syntax**: SnmpUDPAddress</span></span><br/> <span data-ttu-id="6bf12-142">**CimType**: stringa</span><span class="sxs-lookup"><span data-stu-id="6bf12-142">**cimtype**: string</span></span><br/> |
| <span data-ttu-id="6bf12-143">SnmpOSIAddress</span><span class="sxs-lookup"><span data-stu-id="6bf12-143">SnmpOSIAddress</span></span>     | <span data-ttu-id="6bf12-144">**\_BSTR VT**</span><span class="sxs-lookup"><span data-stu-id="6bf12-144">**VT\_BSTR**</span></span>     | <span data-ttu-id="6bf12-145">**\_ convenzione testuale**: SnmpOSIAddress</span><span class="sxs-lookup"><span data-stu-id="6bf12-145">**textual\_convention**: SnmpOSIAddress</span></span><br/> <span data-ttu-id="6bf12-146">**codifica**: OCTETSTRING</span><span class="sxs-lookup"><span data-stu-id="6bf12-146">**encoding**: OCTETSTRING</span></span><br/> <span data-ttu-id="6bf12-147">**\_ sintassi dell'oggetto**: SnmpOSIAddress</span><span class="sxs-lookup"><span data-stu-id="6bf12-147">**object\_syntax**: SnmpOSIAddress</span></span><br/> <span data-ttu-id="6bf12-148">**CimType**: stringa</span><span class="sxs-lookup"><span data-stu-id="6bf12-148">**cimtype**: string</span></span><br/> |
| <span data-ttu-id="6bf12-149">SnmpIPXAddress</span><span class="sxs-lookup"><span data-stu-id="6bf12-149">SnmpIPXAddress</span></span>     | <span data-ttu-id="6bf12-150">**\_BSTR VT**</span><span class="sxs-lookup"><span data-stu-id="6bf12-150">**VT\_BSTR**</span></span>     | <span data-ttu-id="6bf12-151">**\_ convenzione testuale**: SnmpIPXAddress</span><span class="sxs-lookup"><span data-stu-id="6bf12-151">**textual\_convention**: SnmpIPXAddress</span></span><br/> <span data-ttu-id="6bf12-152">**codifica**: OCTETSTRING</span><span class="sxs-lookup"><span data-stu-id="6bf12-152">**encoding**: OCTETSTRING</span></span><br/> <span data-ttu-id="6bf12-153">**\_ sintassi dell'oggetto**: SnmpIPXAddress</span><span class="sxs-lookup"><span data-stu-id="6bf12-153">**object\_syntax**: SnmpIPXAddress</span></span><br/> <span data-ttu-id="6bf12-154">**CimType**: stringa</span><span class="sxs-lookup"><span data-stu-id="6bf12-154">**cimtype**: string</span></span><br/> |



 

-   <span data-ttu-id="6bf12-155">Il tipo Variant definito da CIM e i qualificatori di proprietà **CIM \_ ,** la **codifica**, **la \_ sintassi dell'oggetto** e la mappa **CimType** usando il tipo primitivo sottostante.</span><span class="sxs-lookup"><span data-stu-id="6bf12-155">The CIM-defined variant type and the CIM property qualifiers **textual\_convention**, **encoding**, **object\_syntax**, and **cimtype** map using the underlying primitive type.</span></span>
-   <span data-ttu-id="6bf12-156">La clausola DISPLAY-HINT della macro della convenzione testuale SNMPv2C esegue il mapping Verbatim all' **\_ hint di visualizzazione** del qualificatore della proprietà CIM.</span><span class="sxs-lookup"><span data-stu-id="6bf12-156">The DISPLAY-HINT clause of the SNMPv2C TEXTUAL-CONVENTION macro maps verbatim to the CIM property qualifier **display\_hint**.</span></span> <span data-ttu-id="6bf12-157">Questo qualificatore non viene generato se non è presente una macro della convenzione testuale o la macro non contiene una clausola DISPLAY-HINT.</span><span class="sxs-lookup"><span data-stu-id="6bf12-157">This qualifier is not generated if there is no TEXTUAL-CONVENTION macro, or the macro does not contain a DISPLAY-HINT clause.</span></span>

## <a name="example-code"></a><span data-ttu-id="6bf12-158">Codice di esempio</span><span class="sxs-lookup"><span data-stu-id="6bf12-158">Example Code</span></span>

<span data-ttu-id="6bf12-159">Nell'esempio seguente viene descritta una convenzione testuale SNMPv1.</span><span class="sxs-lookup"><span data-stu-id="6bf12-159">The following example describes an SNMPv1 textual convention.</span></span>

``` syntax
myNamedType ::= DISPLAYSTRING (SIZE (0..127))

myNamedProperty OBJECT-TYPE
SYNTAX  myNamedType
ACCESS read-only
STATUS MANDATORY
DESCRIPTION ""
```

<span data-ttu-id="6bf12-160">Questo esempio genera i qualificatori CIM seguenti.</span><span class="sxs-lookup"><span data-stu-id="6bf12-160">This example generates the following CIM qualifiers.</span></span>

``` syntax
object_syntax("myNamedType"),
textual_convention("DISPLAYSTRING"),
encoding("OCTETSTRING"),
variable_length("0..127")
```

<span data-ttu-id="6bf12-161">Nell'esempio seguente viene descritta una convenzione testuale SNMPv2.</span><span class="sxs-lookup"><span data-stu-id="6bf12-161">The following example describes an SNMPv2 textual convention.</span></span>

``` syntax
myDisplaystring ::= TEXTUAL-CONVENTION
DISPLAY-HINT "255a"
STATUS current
DESCRIPTION "" 
SYNTAX OCTET STRING (SIZE (0..127))

myNamedProperty OBJECT-TYPE
SYNTAX  myDisplaystring
MAX-ACCESS read-only
STATUS current
DESCRIPTION ""
```

<span data-ttu-id="6bf12-162">Questo esempio genera i qualificatori CIM seguenti.</span><span class="sxs-lookup"><span data-stu-id="6bf12-162">This example generates the following CIM qualifiers.</span></span>

``` syntax
object_syntax("myDisplaystring"),
textual_convention("OCTETSTRING"),
encoding("OCTETSTRING"),
display_hint("255a"),
variable_length("0..127")
```

 

 




