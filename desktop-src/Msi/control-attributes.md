---
description: Per informazioni sugli attributi del controllo, vedere il collegamento al particolare controllo che è necessario creare nei controlli e i collegamenti a specifici attributi di controllo negli elenchi seguenti.
ms.assetid: 948ce3d3-e463-40de-8b5f-21ef18b1a0ce
title: Attributi del controllo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61d026e84dadefa67ce9d6e00146c6e1c2017cb9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347791"
---
# <a name="control-attributes"></a><span data-ttu-id="b1cb7-103">Attributi del controllo</span><span class="sxs-lookup"><span data-stu-id="b1cb7-103">Control Attributes</span></span>

<span data-ttu-id="b1cb7-104">Per informazioni sugli attributi del controllo, vedere il collegamento al particolare controllo che è necessario creare nei [controlli](controls.md) e i collegamenti a specifici attributi di controllo negli elenchi seguenti.</span><span class="sxs-lookup"><span data-stu-id="b1cb7-104">For information on control attributes, see the link to the particular control that you need to create in [Controls](controls.md) as well as the links to particular control attributes in the following lists.</span></span>

<span data-ttu-id="b1cb7-105">Per specificare gli attributi di un controllo, vengono usati i metodi seguenti:</span><span class="sxs-lookup"><span data-stu-id="b1cb7-105">The following methods are used for specifying the attributes of a control:</span></span>

-   <span data-ttu-id="b1cb7-106">Usare la [tabella ControlCondition](controlcondition-table.md) per disabilitare, abilitare, nascondere o mostrare un controllo in base al valore di una proprietà o di un'istruzione condizionale.</span><span class="sxs-lookup"><span data-stu-id="b1cb7-106">Use the [ControlCondition table](controlcondition-table.md) to disable, enable, hide, or show a control according to the value of a property or conditional statement.</span></span> <span data-ttu-id="b1cb7-107">È inoltre possibile utilizzare questa tabella per eseguire l'override del controllo predefinito specificato nella [tabella della finestra di dialogo](dialog-table.md).</span><span class="sxs-lookup"><span data-stu-id="b1cb7-107">You can also use this table to override the default control specified in the [Dialog table](dialog-table.md).</span></span>
-   <span data-ttu-id="b1cb7-108">Sottoscrivere il controllo in un ControlEvent nella [tabella EventMapping](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="b1cb7-108">Subscribe the control to a ControlEvent in the [EventMapping table](eventmapping-table.md).</span></span> <span data-ttu-id="b1cb7-109">Immettere l'identificatore dell'attributo nella colonna Attribute e l'identificatore di ControlEvent nella colonna Event della tabella.</span><span class="sxs-lookup"><span data-stu-id="b1cb7-109">Enter the attribute's identifier in the Attribute column and the ControlEvent's identifier in the Event column of this table.</span></span>
-   <span data-ttu-id="b1cb7-110">Impostare i flag di bit dell'attributo di controllo per il controllo nella colonna attributo della [tabella dei controlli](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="b1cb7-110">Set the control attribute bit flags for the control in the Attribute column of the [Control table](control-table.md).</span></span> <span data-ttu-id="b1cb7-111">Consente di impostare gli attributi durante la creazione del controllo.</span><span class="sxs-lookup"><span data-stu-id="b1cb7-111">This sets the attributes upon the creation of the control.</span></span>

<span data-ttu-id="b1cb7-112">Alcuni attributi non possono essere impostati per ogni controllo o essere specificati da tutti i metodi descritti in precedenza.</span><span class="sxs-lookup"><span data-stu-id="b1cb7-112">Some attributes cannot be set for every control or be specified by all of the above methods.</span></span> <span data-ttu-id="b1cb7-113">Per informazioni dettagliate, vedere gli argomenti relativi a controlli e attributi specifici.</span><span class="sxs-lookup"><span data-stu-id="b1cb7-113">See the particular control and attribute topics for details.</span></span>

<span data-ttu-id="b1cb7-114">I valori iniziali di alcuni attributi di controllo possono essere impostati con bit nella [tabella del controllo](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="b1cb7-114">The initial values of some control attributes can be set with bits in the [Control table](control-table.md).</span></span>



| <span data-ttu-id="b1cb7-115">Attributo</span><span class="sxs-lookup"><span data-stu-id="b1cb7-115">Attribute</span></span>                                          | <span data-ttu-id="b1cb7-116">Decimal</span><span class="sxs-lookup"><span data-stu-id="b1cb7-116">Decimal</span></span> | <span data-ttu-id="b1cb7-117">Valore esadecimale</span><span class="sxs-lookup"><span data-stu-id="b1cb7-117">Hexadecimal</span></span> | <span data-ttu-id="b1cb7-118">Costante</span><span class="sxs-lookup"><span data-stu-id="b1cb7-118">Constant</span></span>                               |
|----------------------------------------------------|---------|-------------|----------------------------------------|
| [<span data-ttu-id="b1cb7-119">BiDi</span><span class="sxs-lookup"><span data-stu-id="b1cb7-119">BiDi</span></span>](bidi-control-attribute.md)                 | <span data-ttu-id="b1cb7-120">224</span><span class="sxs-lookup"><span data-stu-id="b1cb7-120">224</span></span>     | <span data-ttu-id="b1cb7-121">0x000000E0</span><span class="sxs-lookup"><span data-stu-id="b1cb7-121">0x000000E0</span></span>  | <span data-ttu-id="b1cb7-122">**msidbControlAttributesBiDi**</span><span class="sxs-lookup"><span data-stu-id="b1cb7-122">**msidbControlAttributesBiDi**</span></span>         |
| [<span data-ttu-id="b1cb7-123">Enabled</span><span class="sxs-lookup"><span data-stu-id="b1cb7-123">Enabled</span></span>](enabled-control-attribute.md)           | <span data-ttu-id="b1cb7-124">2</span><span class="sxs-lookup"><span data-stu-id="b1cb7-124">2</span></span>       | <span data-ttu-id="b1cb7-125">0x00000002</span><span class="sxs-lookup"><span data-stu-id="b1cb7-125">0x00000002</span></span>  | <span data-ttu-id="b1cb7-126">**msidbControlAttributesEnabled**</span><span class="sxs-lookup"><span data-stu-id="b1cb7-126">**msidbControlAttributesEnabled**</span></span>      |
| [<span data-ttu-id="b1cb7-127">Indiretto</span><span class="sxs-lookup"><span data-stu-id="b1cb7-127">Indirect</span></span>](indirect-control-attribute.md)         | <span data-ttu-id="b1cb7-128">8</span><span class="sxs-lookup"><span data-stu-id="b1cb7-128">8</span></span>       | <span data-ttu-id="b1cb7-129">0x00000008</span><span class="sxs-lookup"><span data-stu-id="b1cb7-129">0x00000008</span></span>  | <span data-ttu-id="b1cb7-130">**msidbControlAttributesIndirect**</span><span class="sxs-lookup"><span data-stu-id="b1cb7-130">**msidbControlAttributesIndirect**</span></span>     |
| [<span data-ttu-id="b1cb7-131">Controllo Integer</span><span class="sxs-lookup"><span data-stu-id="b1cb7-131">Integer Control</span></span>](integer-control-attribute.md)   | <span data-ttu-id="b1cb7-132">16</span><span class="sxs-lookup"><span data-stu-id="b1cb7-132">16</span></span>      | <span data-ttu-id="b1cb7-133">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b1cb7-133">0x00000010</span></span>  | <span data-ttu-id="b1cb7-134">**msidbControlAttributesInteger**</span><span class="sxs-lookup"><span data-stu-id="b1cb7-134">**msidbControlAttributesInteger**</span></span>      |
| [<span data-ttu-id="b1cb7-135">LeftScroll</span><span class="sxs-lookup"><span data-stu-id="b1cb7-135">LeftScroll</span></span>](leftscroll-control-attribute.md)     | <span data-ttu-id="b1cb7-136">128</span><span class="sxs-lookup"><span data-stu-id="b1cb7-136">128</span></span>     | <span data-ttu-id="b1cb7-137">0x00000080</span><span class="sxs-lookup"><span data-stu-id="b1cb7-137">0x00000080</span></span>  | <span data-ttu-id="b1cb7-138">**msidbControlAttributesLeftScroll**</span><span class="sxs-lookup"><span data-stu-id="b1cb7-138">**msidbControlAttributesLeftScroll**</span></span>   |
| [<span data-ttu-id="b1cb7-139">RightAligned</span><span class="sxs-lookup"><span data-stu-id="b1cb7-139">RightAligned</span></span>](rightaligned-control-attribute.md) | <span data-ttu-id="b1cb7-140">64</span><span class="sxs-lookup"><span data-stu-id="b1cb7-140">64</span></span>      | <span data-ttu-id="b1cb7-141">0x00000040</span><span class="sxs-lookup"><span data-stu-id="b1cb7-141">0x00000040</span></span>  | <span data-ttu-id="b1cb7-142">**msidbControlAttributesRightAligned**</span><span class="sxs-lookup"><span data-stu-id="b1cb7-142">**msidbControlAttributesRightAligned**</span></span> |
| [<span data-ttu-id="b1cb7-143">RTLRO</span><span class="sxs-lookup"><span data-stu-id="b1cb7-143">RTLRO</span></span>](rtlro-control-attribute.md)               | <span data-ttu-id="b1cb7-144">32</span><span class="sxs-lookup"><span data-stu-id="b1cb7-144">32</span></span>      | <span data-ttu-id="b1cb7-145">0x00000020</span><span class="sxs-lookup"><span data-stu-id="b1cb7-145">0x00000020</span></span>  | <span data-ttu-id="b1cb7-146">**msidbControlAttributesRTLRO**</span><span class="sxs-lookup"><span data-stu-id="b1cb7-146">**msidbControlAttributesRTLRO**</span></span>        |
| [<span data-ttu-id="b1cb7-147">Sunken</span><span class="sxs-lookup"><span data-stu-id="b1cb7-147">Sunken</span></span>](sunken-control-attribute.md)             | <span data-ttu-id="b1cb7-148">4</span><span class="sxs-lookup"><span data-stu-id="b1cb7-148">4</span></span>       | <span data-ttu-id="b1cb7-149">0x00000004</span><span class="sxs-lookup"><span data-stu-id="b1cb7-149">0x00000004</span></span>  | <span data-ttu-id="b1cb7-150">**msidbControlAttributesSunken**</span><span class="sxs-lookup"><span data-stu-id="b1cb7-150">**msidbControlAttributesSunken**</span></span>       |
| [<span data-ttu-id="b1cb7-151">Visible</span><span class="sxs-lookup"><span data-stu-id="b1cb7-151">Visible</span></span>](visible-control-attribute.md)           | <span data-ttu-id="b1cb7-152">1</span><span class="sxs-lookup"><span data-stu-id="b1cb7-152">1</span></span>       | <span data-ttu-id="b1cb7-153">0x00000001</span><span class="sxs-lookup"><span data-stu-id="b1cb7-153">0x00000001</span></span>  | <span data-ttu-id="b1cb7-154">**msidbControlAttributesVisible**</span><span class="sxs-lookup"><span data-stu-id="b1cb7-154">**msidbControlAttributesVisible**</span></span>      |



 

<span data-ttu-id="b1cb7-155">Questi attributi dei controlli testo sono impostati con BITS.</span><span class="sxs-lookup"><span data-stu-id="b1cb7-155">These attributes of Text controls are set with bits.</span></span>



| <span data-ttu-id="b1cb7-156">Attributo</span><span class="sxs-lookup"><span data-stu-id="b1cb7-156">Attribute</span></span>                                            | <span data-ttu-id="b1cb7-157">Decimal</span><span class="sxs-lookup"><span data-stu-id="b1cb7-157">Decimal</span></span> | <span data-ttu-id="b1cb7-158">Valore esadecimale</span><span class="sxs-lookup"><span data-stu-id="b1cb7-158">Hexadecimal</span></span> | <span data-ttu-id="b1cb7-159">Costante</span><span class="sxs-lookup"><span data-stu-id="b1cb7-159">Constant</span></span>                                |
|------------------------------------------------------|---------|-------------|-----------------------------------------|
| [<span data-ttu-id="b1cb7-160">FormatSize</span><span class="sxs-lookup"><span data-stu-id="b1cb7-160">FormatSize</span></span>](formatsize-control-attribute.md)       | <span data-ttu-id="b1cb7-161">524288</span><span class="sxs-lookup"><span data-stu-id="b1cb7-161">524288</span></span>  | <span data-ttu-id="b1cb7-162">0x00080000</span><span class="sxs-lookup"><span data-stu-id="b1cb7-162">0x00080000</span></span>  | <span data-ttu-id="b1cb7-163">**msidbControlAttributesFormatSize**</span><span class="sxs-lookup"><span data-stu-id="b1cb7-163">**msidbControlAttributesFormatSize**</span></span>    |
| [<span data-ttu-id="b1cb7-164">NoPrefix</span><span class="sxs-lookup"><span data-stu-id="b1cb7-164">NoPrefix</span></span>](noprefix-control-attribute.md)           | <span data-ttu-id="b1cb7-165">131072</span><span class="sxs-lookup"><span data-stu-id="b1cb7-165">131072</span></span>  | <span data-ttu-id="b1cb7-166">0x00020000</span><span class="sxs-lookup"><span data-stu-id="b1cb7-166">0x00020000</span></span>  | <span data-ttu-id="b1cb7-167">**msidbControlAttributesNoPrefix**</span><span class="sxs-lookup"><span data-stu-id="b1cb7-167">**msidbControlAttributesNoPrefix**</span></span>      |
| [<span data-ttu-id="b1cb7-168">NoWrap</span><span class="sxs-lookup"><span data-stu-id="b1cb7-168">NoWrap</span></span>](nowrap-control-attribute.md)               | <span data-ttu-id="b1cb7-169">262144</span><span class="sxs-lookup"><span data-stu-id="b1cb7-169">262144</span></span>  | <span data-ttu-id="b1cb7-170">0x00040000</span><span class="sxs-lookup"><span data-stu-id="b1cb7-170">0x00040000</span></span>  | <span data-ttu-id="b1cb7-171">**msidbControlAttributesNoWrap**</span><span class="sxs-lookup"><span data-stu-id="b1cb7-171">**msidbControlAttributesNoWrap**</span></span>        |
| [<span data-ttu-id="b1cb7-172">Password</span><span class="sxs-lookup"><span data-stu-id="b1cb7-172">Password</span></span>](password-control-attribute.md)           | <span data-ttu-id="b1cb7-173">2097152</span><span class="sxs-lookup"><span data-stu-id="b1cb7-173">2097152</span></span> | <span data-ttu-id="b1cb7-174">0x00200000</span><span class="sxs-lookup"><span data-stu-id="b1cb7-174">0x00200000</span></span>  | <span data-ttu-id="b1cb7-175">**msidbControlAttributesPasswordInput**</span><span class="sxs-lookup"><span data-stu-id="b1cb7-175">**msidbControlAttributesPasswordInput**</span></span> |
| [<span data-ttu-id="b1cb7-176">Modalità trasparente</span><span class="sxs-lookup"><span data-stu-id="b1cb7-176">Transparent</span></span>](transparent-control-attribute.md)     | <span data-ttu-id="b1cb7-177">65536</span><span class="sxs-lookup"><span data-stu-id="b1cb7-177">65536</span></span>   | <span data-ttu-id="b1cb7-178">0x00010000</span><span class="sxs-lookup"><span data-stu-id="b1cb7-178">0x00010000</span></span>  | <span data-ttu-id="b1cb7-179">**msidbControlAttributesTransparent**</span><span class="sxs-lookup"><span data-stu-id="b1cb7-179">**msidbControlAttributesTransparent**</span></span>   |
| [<span data-ttu-id="b1cb7-180">UsersLanguage</span><span class="sxs-lookup"><span data-stu-id="b1cb7-180">UsersLanguage</span></span>](userslanguage-control-attribute.md) | <span data-ttu-id="b1cb7-181">1048576</span><span class="sxs-lookup"><span data-stu-id="b1cb7-181">1048576</span></span> | <span data-ttu-id="b1cb7-182">0x00100000</span><span class="sxs-lookup"><span data-stu-id="b1cb7-182">0x00100000</span></span>  | <span data-ttu-id="b1cb7-183">**msidbControlAttributesUsersLanguage**</span><span class="sxs-lookup"><span data-stu-id="b1cb7-183">**msidbControlAttributesUsersLanguage**</span></span> |



 

<span data-ttu-id="b1cb7-184">Questo attributo del controllo ProgressBar è impostato su un bit.</span><span class="sxs-lookup"><span data-stu-id="b1cb7-184">This attribute of the ProgressBar control is set with a bit.</span></span>



| <span data-ttu-id="b1cb7-185">Attributo</span><span class="sxs-lookup"><span data-stu-id="b1cb7-185">Attribute</span></span>                                      | <span data-ttu-id="b1cb7-186">Decimal</span><span class="sxs-lookup"><span data-stu-id="b1cb7-186">Decimal</span></span> | <span data-ttu-id="b1cb7-187">Valore esadecimale</span><span class="sxs-lookup"><span data-stu-id="b1cb7-187">Hexadecimal</span></span> | <span data-ttu-id="b1cb7-188">Costante</span><span class="sxs-lookup"><span data-stu-id="b1cb7-188">Constant</span></span>                             |
|------------------------------------------------|---------|-------------|--------------------------------------|
| [<span data-ttu-id="b1cb7-189">Progress95</span><span class="sxs-lookup"><span data-stu-id="b1cb7-189">Progress95</span></span>](progress95-control-attribute.md) | <span data-ttu-id="b1cb7-190">65536</span><span class="sxs-lookup"><span data-stu-id="b1cb7-190">65536</span></span>   | <span data-ttu-id="b1cb7-191">0x00010000</span><span class="sxs-lookup"><span data-stu-id="b1cb7-191">0x00010000</span></span>  | <span data-ttu-id="b1cb7-192">**msidbControlAttributesProgress95**</span><span class="sxs-lookup"><span data-stu-id="b1cb7-192">**msidbControlAttributesProgress95**</span></span> |



 

<span data-ttu-id="b1cb7-193">Questi attributi dei controlli SelectCombo del volume e della directory sono impostati con BITS.</span><span class="sxs-lookup"><span data-stu-id="b1cb7-193">These attributes of Volume and Directory SelectCombo controls are set with bits.</span></span>



| <span data-ttu-id="b1cb7-194">Attributo</span><span class="sxs-lookup"><span data-stu-id="b1cb7-194">Attribute</span></span>                                                | <span data-ttu-id="b1cb7-195">Decimal</span><span class="sxs-lookup"><span data-stu-id="b1cb7-195">Decimal</span></span> | <span data-ttu-id="b1cb7-196">Valore esadecimale</span><span class="sxs-lookup"><span data-stu-id="b1cb7-196">Hexadecimal</span></span> | <span data-ttu-id="b1cb7-197">Costante</span><span class="sxs-lookup"><span data-stu-id="b1cb7-197">Constant</span></span>                                  |
|----------------------------------------------------------|---------|-------------|-------------------------------------------|
| [<span data-ttu-id="b1cb7-198">CDROMVolume</span><span class="sxs-lookup"><span data-stu-id="b1cb7-198">CDROMVolume</span></span>](cdromvolume-control-attribute.md)         | <span data-ttu-id="b1cb7-199">524288</span><span class="sxs-lookup"><span data-stu-id="b1cb7-199">524288</span></span>  | <span data-ttu-id="b1cb7-200">0x00080000</span><span class="sxs-lookup"><span data-stu-id="b1cb7-200">0x00080000</span></span>  | <span data-ttu-id="b1cb7-201">**msidbControlAttributesCDROMVolume**</span><span class="sxs-lookup"><span data-stu-id="b1cb7-201">**msidbControlAttributesCDROMVolume**</span></span>     |
| [<span data-ttu-id="b1cb7-202">FixedVolume</span><span class="sxs-lookup"><span data-stu-id="b1cb7-202">FixedVolume</span></span>](fixedvolume-control-attribute.md)         | <span data-ttu-id="b1cb7-203">131072</span><span class="sxs-lookup"><span data-stu-id="b1cb7-203">131072</span></span>  | <span data-ttu-id="b1cb7-204">0x00020000</span><span class="sxs-lookup"><span data-stu-id="b1cb7-204">0x00020000</span></span>  | <span data-ttu-id="b1cb7-205">**msidbControlAttributesFixedVolume**</span><span class="sxs-lookup"><span data-stu-id="b1cb7-205">**msidbControlAttributesFixedVolume**</span></span>     |
| [<span data-ttu-id="b1cb7-206">FloppyVolume</span><span class="sxs-lookup"><span data-stu-id="b1cb7-206">FloppyVolume</span></span>](floppyvolume-control-attribute.md)       | <span data-ttu-id="b1cb7-207">2097152</span><span class="sxs-lookup"><span data-stu-id="b1cb7-207">2097152</span></span> | <span data-ttu-id="b1cb7-208">0x00200000</span><span class="sxs-lookup"><span data-stu-id="b1cb7-208">0x00200000</span></span>  | <span data-ttu-id="b1cb7-209">**msidbControlAttributesFloppyVolume**</span><span class="sxs-lookup"><span data-stu-id="b1cb7-209">**msidbControlAttributesFloppyVolume**</span></span>    |
| [<span data-ttu-id="b1cb7-210">RAMDiskVolume</span><span class="sxs-lookup"><span data-stu-id="b1cb7-210">RAMDiskVolume</span></span>](ramdiskvolume-control-attribute.md)     | <span data-ttu-id="b1cb7-211">1048576</span><span class="sxs-lookup"><span data-stu-id="b1cb7-211">1048576</span></span> | <span data-ttu-id="b1cb7-212">0x00100000</span><span class="sxs-lookup"><span data-stu-id="b1cb7-212">0x00100000</span></span>  | <span data-ttu-id="b1cb7-213">**msidbControlAttributesRAMDiskVolume**</span><span class="sxs-lookup"><span data-stu-id="b1cb7-213">**msidbControlAttributesRAMDiskVolume**</span></span>   |
| [<span data-ttu-id="b1cb7-214">RemoteVolume</span><span class="sxs-lookup"><span data-stu-id="b1cb7-214">RemoteVolume</span></span>](remotevolume-control-attribute.md)       | <span data-ttu-id="b1cb7-215">262144</span><span class="sxs-lookup"><span data-stu-id="b1cb7-215">262144</span></span>  | <span data-ttu-id="b1cb7-216">0x00040000</span><span class="sxs-lookup"><span data-stu-id="b1cb7-216">0x00040000</span></span>  | <span data-ttu-id="b1cb7-217">**msidbControlAttributesRemoteVolume**</span><span class="sxs-lookup"><span data-stu-id="b1cb7-217">**msidbControlAttributesRemoteVolume**</span></span>    |
| [<span data-ttu-id="b1cb7-218">RemovableVolume</span><span class="sxs-lookup"><span data-stu-id="b1cb7-218">RemovableVolume</span></span>](removablevolume-control-attribute.md) | <span data-ttu-id="b1cb7-219">65536</span><span class="sxs-lookup"><span data-stu-id="b1cb7-219">65536</span></span>   | <span data-ttu-id="b1cb7-220">0x00010000</span><span class="sxs-lookup"><span data-stu-id="b1cb7-220">0x00010000</span></span>  | <span data-ttu-id="b1cb7-221">**msidbControlAttributesRemovableVolume**</span><span class="sxs-lookup"><span data-stu-id="b1cb7-221">**msidbControlAttributesRemovableVolume**</span></span> |



 

<span data-ttu-id="b1cb7-222">Questi attributi dei controlli ListBox e ComboBox sono impostati con BITS.</span><span class="sxs-lookup"><span data-stu-id="b1cb7-222">These attributes of ListBox and ComboBox controls are set with bits.</span></span>



| <span data-ttu-id="b1cb7-223">Attributo</span><span class="sxs-lookup"><span data-stu-id="b1cb7-223">Attribute</span></span>                                            | <span data-ttu-id="b1cb7-224">Decimal</span><span class="sxs-lookup"><span data-stu-id="b1cb7-224">Decimal</span></span> | <span data-ttu-id="b1cb7-225">Valore esadecimale</span><span class="sxs-lookup"><span data-stu-id="b1cb7-225">Hexadecimal</span></span> | <span data-ttu-id="b1cb7-226">Costante</span><span class="sxs-lookup"><span data-stu-id="b1cb7-226">Constant</span></span>                            |
|------------------------------------------------------|---------|-------------|-------------------------------------|
| [<span data-ttu-id="b1cb7-227">Controllo ComboBox</span><span class="sxs-lookup"><span data-stu-id="b1cb7-227">ComboList Control</span></span>](combolist-control-attribute.md) | <span data-ttu-id="b1cb7-228">131072</span><span class="sxs-lookup"><span data-stu-id="b1cb7-228">131072</span></span>  | <span data-ttu-id="b1cb7-229">0x00020000</span><span class="sxs-lookup"><span data-stu-id="b1cb7-229">0x00020000</span></span>  | <span data-ttu-id="b1cb7-230">**msidbControlAttributesComboList**</span><span class="sxs-lookup"><span data-stu-id="b1cb7-230">**msidbControlAttributesComboList**</span></span> |
| [<span data-ttu-id="b1cb7-231">Controllo ordinato</span><span class="sxs-lookup"><span data-stu-id="b1cb7-231">Sorted Control</span></span>](sorted-control-attribute.md)       | <span data-ttu-id="b1cb7-232">65536</span><span class="sxs-lookup"><span data-stu-id="b1cb7-232">65536</span></span>   | <span data-ttu-id="b1cb7-233">0x00010000</span><span class="sxs-lookup"><span data-stu-id="b1cb7-233">0x00010000</span></span>  | <span data-ttu-id="b1cb7-234">**msidbControlAttributesSorted**</span><span class="sxs-lookup"><span data-stu-id="b1cb7-234">**msidbControlAttributesSorted**</span></span>    |



 

<span data-ttu-id="b1cb7-235">Questo attributo del controllo di modifica è impostato su un bit.</span><span class="sxs-lookup"><span data-stu-id="b1cb7-235">This attribute of the Edit control is set with a bit.</span></span>



| <span data-ttu-id="b1cb7-236">Attributo</span><span class="sxs-lookup"><span data-stu-id="b1cb7-236">Attribute</span></span>                                    | <span data-ttu-id="b1cb7-237">Decimal</span><span class="sxs-lookup"><span data-stu-id="b1cb7-237">Decimal</span></span> | <span data-ttu-id="b1cb7-238">Valore esadecimale</span><span class="sxs-lookup"><span data-stu-id="b1cb7-238">Hexadecimal</span></span> | <span data-ttu-id="b1cb7-239">Costante</span><span class="sxs-lookup"><span data-stu-id="b1cb7-239">Constant</span></span>                            |
|----------------------------------------------|---------|-------------|-------------------------------------|
| [<span data-ttu-id="b1cb7-240">MultiLine</span><span class="sxs-lookup"><span data-stu-id="b1cb7-240">MultiLine</span></span>](multiline-control-attribute.md) | <span data-ttu-id="b1cb7-241">65536</span><span class="sxs-lookup"><span data-stu-id="b1cb7-241">65536</span></span>   | <span data-ttu-id="b1cb7-242">0x00010000</span><span class="sxs-lookup"><span data-stu-id="b1cb7-242">0x00010000</span></span>  | <span data-ttu-id="b1cb7-243">**msidbControlAttributesMultiline**</span><span class="sxs-lookup"><span data-stu-id="b1cb7-243">**msidbControlAttributesMultiline**</span></span> |



 

<span data-ttu-id="b1cb7-244">Questi attributi dei controlli PictureButton sono impostati con BITS.</span><span class="sxs-lookup"><span data-stu-id="b1cb7-244">These attributes of PictureButton controls are set with bits.</span></span>



| <span data-ttu-id="b1cb7-245">Attributo</span><span class="sxs-lookup"><span data-stu-id="b1cb7-245">Attribute</span></span>                                          | <span data-ttu-id="b1cb7-246">Decimal</span><span class="sxs-lookup"><span data-stu-id="b1cb7-246">Decimal</span></span> | <span data-ttu-id="b1cb7-247">Valore esadecimale</span><span class="sxs-lookup"><span data-stu-id="b1cb7-247">Hexadecimal</span></span> | <span data-ttu-id="b1cb7-248">Costante</span><span class="sxs-lookup"><span data-stu-id="b1cb7-248">Constant</span></span>                             |
|----------------------------------------------------|---------|-------------|--------------------------------------|
| [<span data-ttu-id="b1cb7-249">Bitmap</span><span class="sxs-lookup"><span data-stu-id="b1cb7-249">Bitmap</span></span>](bitmap-control-attribute.md)             | <span data-ttu-id="b1cb7-250">262144</span><span class="sxs-lookup"><span data-stu-id="b1cb7-250">262144</span></span>  | <span data-ttu-id="b1cb7-251">0x00040000</span><span class="sxs-lookup"><span data-stu-id="b1cb7-251">0x00040000</span></span>  | <span data-ttu-id="b1cb7-252">**msidbControlAttributesBitmap**</span><span class="sxs-lookup"><span data-stu-id="b1cb7-252">**msidbControlAttributesBitmap**</span></span>     |
| [<span data-ttu-id="b1cb7-253">FixedSize</span><span class="sxs-lookup"><span data-stu-id="b1cb7-253">FixedSize</span></span>](fixedsize-control-attribute.md)       | <span data-ttu-id="b1cb7-254">1048576</span><span class="sxs-lookup"><span data-stu-id="b1cb7-254">1048576</span></span> | <span data-ttu-id="b1cb7-255">0x00100000</span><span class="sxs-lookup"><span data-stu-id="b1cb7-255">0x00100000</span></span>  | <span data-ttu-id="b1cb7-256">**msidbControlAttributesFixedSize**</span><span class="sxs-lookup"><span data-stu-id="b1cb7-256">**msidbControlAttributesFixedSize**</span></span>  |
| [<span data-ttu-id="b1cb7-257">Icona</span><span class="sxs-lookup"><span data-stu-id="b1cb7-257">Icon</span></span>](icon-control-attribute.md)                 | <span data-ttu-id="b1cb7-258">524288</span><span class="sxs-lookup"><span data-stu-id="b1cb7-258">524288</span></span>  | <span data-ttu-id="b1cb7-259">0x00080000</span><span class="sxs-lookup"><span data-stu-id="b1cb7-259">0x00080000</span></span>  | <span data-ttu-id="b1cb7-260">**msidbControlAttributesIcon**</span><span class="sxs-lookup"><span data-stu-id="b1cb7-260">**msidbControlAttributesIcon**</span></span>       |
| [<span data-ttu-id="b1cb7-261">IconSize16</span><span class="sxs-lookup"><span data-stu-id="b1cb7-261">IconSize16</span></span>](iconsize-control-attribute.md)       | <span data-ttu-id="b1cb7-262">2097152</span><span class="sxs-lookup"><span data-stu-id="b1cb7-262">2097152</span></span> | <span data-ttu-id="b1cb7-263">0x00200000</span><span class="sxs-lookup"><span data-stu-id="b1cb7-263">0x00200000</span></span>  | <span data-ttu-id="b1cb7-264">**msidbControlAttributesIconSize16**</span><span class="sxs-lookup"><span data-stu-id="b1cb7-264">**msidbControlAttributesIconSize16**</span></span> |
| [<span data-ttu-id="b1cb7-265">IconSize32</span><span class="sxs-lookup"><span data-stu-id="b1cb7-265">IconSize32</span></span>](iconsize-control-attribute.md)       | <span data-ttu-id="b1cb7-266">4194304</span><span class="sxs-lookup"><span data-stu-id="b1cb7-266">4194304</span></span> | <span data-ttu-id="b1cb7-267">0x00400000</span><span class="sxs-lookup"><span data-stu-id="b1cb7-267">0x00400000</span></span>  | <span data-ttu-id="b1cb7-268">**msidbControlAttributesIconSize32**</span><span class="sxs-lookup"><span data-stu-id="b1cb7-268">**msidbControlAttributesIconSize32**</span></span> |
| [<span data-ttu-id="b1cb7-269">IconSize48</span><span class="sxs-lookup"><span data-stu-id="b1cb7-269">IconSize48</span></span>](iconsize-control-attribute.md)       | <span data-ttu-id="b1cb7-270">6291456</span><span class="sxs-lookup"><span data-stu-id="b1cb7-270">6291456</span></span> | <span data-ttu-id="b1cb7-271">0x00600000</span><span class="sxs-lookup"><span data-stu-id="b1cb7-271">0x00600000</span></span>  | <span data-ttu-id="b1cb7-272">**msidbControlAttributesIconSize48**</span><span class="sxs-lookup"><span data-stu-id="b1cb7-272">**msidbControlAttributesIconSize48**</span></span> |
| [<span data-ttu-id="b1cb7-273">Controllo PushLike</span><span class="sxs-lookup"><span data-stu-id="b1cb7-273">PushLike Control</span></span>](pushlike-control-attribute.md) | <span data-ttu-id="b1cb7-274">131072</span><span class="sxs-lookup"><span data-stu-id="b1cb7-274">131072</span></span>  | <span data-ttu-id="b1cb7-275">0x00020000</span><span class="sxs-lookup"><span data-stu-id="b1cb7-275">0x00020000</span></span>  | <span data-ttu-id="b1cb7-276">**msidbControlAttributesPushLike**</span><span class="sxs-lookup"><span data-stu-id="b1cb7-276">**msidbControlAttributesPushLike**</span></span>   |



 

<span data-ttu-id="b1cb7-277">Questo attributo del controllo RadioButton è impostato su un bit.</span><span class="sxs-lookup"><span data-stu-id="b1cb7-277">This attribute of RadioButton control is set with a bit.</span></span>



| <span data-ttu-id="b1cb7-278">Attributo</span><span class="sxs-lookup"><span data-stu-id="b1cb7-278">Attribute</span></span>                                    | <span data-ttu-id="b1cb7-279">Decimal</span><span class="sxs-lookup"><span data-stu-id="b1cb7-279">Decimal</span></span>  | <span data-ttu-id="b1cb7-280">Valore esadecimale</span><span class="sxs-lookup"><span data-stu-id="b1cb7-280">Hexadecimal</span></span> | <span data-ttu-id="b1cb7-281">Costante</span><span class="sxs-lookup"><span data-stu-id="b1cb7-281">Constant</span></span>                            |
|----------------------------------------------|----------|-------------|-------------------------------------|
| [<span data-ttu-id="b1cb7-282">HasBorder</span><span class="sxs-lookup"><span data-stu-id="b1cb7-282">HasBorder</span></span>](hasborder-control-attribute.md) | <span data-ttu-id="b1cb7-283">16777216</span><span class="sxs-lookup"><span data-stu-id="b1cb7-283">16777216</span></span> | <span data-ttu-id="b1cb7-284">0x01000000</span><span class="sxs-lookup"><span data-stu-id="b1cb7-284">0x01000000</span></span>  | <span data-ttu-id="b1cb7-285">**msidbControlAttributesHasBorder**</span><span class="sxs-lookup"><span data-stu-id="b1cb7-285">**msidbControlAttributesHasBorder**</span></span> |



 

<span data-ttu-id="b1cb7-286">Questo attributo del controllo pulsante è impostato su un bit.</span><span class="sxs-lookup"><span data-stu-id="b1cb7-286">This attribute of PushButton control is set with a bit.</span></span>



| <span data-ttu-id="b1cb7-287">Attributo</span><span class="sxs-lookup"><span data-stu-id="b1cb7-287">Attribute</span></span>                                        | <span data-ttu-id="b1cb7-288">Decimal</span><span class="sxs-lookup"><span data-stu-id="b1cb7-288">Decimal</span></span> | <span data-ttu-id="b1cb7-289">Valore esadecimale</span><span class="sxs-lookup"><span data-stu-id="b1cb7-289">Hexadecimal</span></span> | <span data-ttu-id="b1cb7-290">Costante</span><span class="sxs-lookup"><span data-stu-id="b1cb7-290">Constant</span></span>                                  |
|--------------------------------------------------|---------|-------------|-------------------------------------------|
| [<span data-ttu-id="b1cb7-291">ElevationShield</span><span class="sxs-lookup"><span data-stu-id="b1cb7-291">ElevationShield</span></span>](elevationshield-attribute.md) | <span data-ttu-id="b1cb7-292">8388608</span><span class="sxs-lookup"><span data-stu-id="b1cb7-292">8388608</span></span> | <span data-ttu-id="b1cb7-293">0x00800000</span><span class="sxs-lookup"><span data-stu-id="b1cb7-293">0x00800000</span></span>  | <span data-ttu-id="b1cb7-294">**msidbControlAttributesElevationShield**</span><span class="sxs-lookup"><span data-stu-id="b1cb7-294">**msidbControlAttributesElevationShield**</span></span> |



 

<span data-ttu-id="b1cb7-295">Questo attributo del controllo VolumeCostList è impostato su un bit.</span><span class="sxs-lookup"><span data-stu-id="b1cb7-295">This attribute of VolumeCostList control is set with a bit.</span></span>



| <span data-ttu-id="b1cb7-296">Attributo</span><span class="sxs-lookup"><span data-stu-id="b1cb7-296">Attribute</span></span>                                                                | <span data-ttu-id="b1cb7-297">Decimal</span><span class="sxs-lookup"><span data-stu-id="b1cb7-297">Decimal</span></span> | <span data-ttu-id="b1cb7-298">Valore esadecimale</span><span class="sxs-lookup"><span data-stu-id="b1cb7-298">Hexadecimal</span></span> | <span data-ttu-id="b1cb7-299">Costante</span><span class="sxs-lookup"><span data-stu-id="b1cb7-299">Constant</span></span>                         |
|--------------------------------------------------------------------------|---------|-------------|----------------------------------|
| [<span data-ttu-id="b1cb7-300">ControlShowRollbackCost</span><span class="sxs-lookup"><span data-stu-id="b1cb7-300">ControlShowRollbackCost</span></span>](controlshowrollbackcost-control-attribute.md) | <span data-ttu-id="b1cb7-301">4194304</span><span class="sxs-lookup"><span data-stu-id="b1cb7-301">4194304</span></span> | <span data-ttu-id="b1cb7-302">0x00400000</span><span class="sxs-lookup"><span data-stu-id="b1cb7-302">0x00400000</span></span>  | <span data-ttu-id="b1cb7-303">**msidbControlShowRollbackCost**</span><span class="sxs-lookup"><span data-stu-id="b1cb7-303">**msidbControlShowRollbackCost**</span></span> |



 

<span data-ttu-id="b1cb7-304">Gli attributi di controllo seguenti non sono impostati con BITS.</span><span class="sxs-lookup"><span data-stu-id="b1cb7-304">The following control attributes are not set with bits.</span></span> <span data-ttu-id="b1cb7-305">Questi attributi vengono creati nelle tabelle dell'interfaccia utente o vengono impostati utilizzando [gli eventi di controllo](control-events.md).</span><span class="sxs-lookup"><span data-stu-id="b1cb7-305">These attributes are authored into the user interface tables or are set using [Control Events](control-events.md).</span></span>

[<span data-ttu-id="b1cb7-306">Billboardname</span><span class="sxs-lookup"><span data-stu-id="b1cb7-306">BillboardName</span></span>](billboardname-control-attribute.md)

 

[<span data-ttu-id="b1cb7-307">IndirectPropertyName</span><span class="sxs-lookup"><span data-stu-id="b1cb7-307">IndirectPropertyName</span></span>](indirectpropertyname-control-attribute.md)

 

[<span data-ttu-id="b1cb7-308">Position</span><span class="sxs-lookup"><span data-stu-id="b1cb7-308">Position</span></span>](position-control-attribute.md)

 

[<span data-ttu-id="b1cb7-309">Controllo dello stato di avanzamento</span><span class="sxs-lookup"><span data-stu-id="b1cb7-309">Progress Control</span></span>](progress-control-attribute.md)

 

[<span data-ttu-id="b1cb7-310">PropertyName</span><span class="sxs-lookup"><span data-stu-id="b1cb7-310">PropertyName</span></span>](propertyname-control-attribute.md)

 

[<span data-ttu-id="b1cb7-311">PropertyValue</span><span class="sxs-lookup"><span data-stu-id="b1cb7-311">PropertyValue</span></span>](propertyvalue-control-attribute.md)

 

[<span data-ttu-id="b1cb7-312">Text Control</span><span class="sxs-lookup"><span data-stu-id="b1cb7-312">Text Control</span></span>](text-control-attribute.md)

 

[<span data-ttu-id="b1cb7-313">TimeRemaining</span><span class="sxs-lookup"><span data-stu-id="b1cb7-313">TimeRemaining</span></span>](timeremaining-control-attribute.md)

<span data-ttu-id="b1cb7-314">Vedere [aggiunta di controlli e testo](adding-controls-and-text.md).</span><span class="sxs-lookup"><span data-stu-id="b1cb7-314">See [Adding Controls and Text](adding-controls-and-text.md).</span></span>

 

 



