---
description: Rappresenta un controller di visualizzazione.
ms.assetid: 14598ae6-58e2-46ca-8653-b57e5833a224
title: Classe CIM_DisplayController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DisplayController
- CIM_DisplayController.Description
- CIM_DisplayController.VideoProcessor
- CIM_DisplayController.VideoMemoryType
- CIM_DisplayController.OtherVideoMemoryType
- CIM_DisplayController.NumberOfVideoPages
- CIM_DisplayController.MaxMemorySupported
- CIM_DisplayController.AcceleratorCapabilities
- CIM_DisplayController.CapabilityDescriptions
- CIM_DisplayController.OtherVideoArchitecture
- CIM_DisplayController.VideoArchitecture
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 59db37a89ce1f57e01a6a9a27fb9c24177221b00
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308352"
---
# <a name="cim_displaycontroller-class"></a><span data-ttu-id="4119e-103">CIM \_ DisplayController (classe)</span><span class="sxs-lookup"><span data-stu-id="4119e-103">CIM\_DisplayController class</span></span>

<span data-ttu-id="4119e-104">Rappresenta un controller di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="4119e-104">Represents a display controller.</span></span>

## <a name="syntax"></a><span data-ttu-id="4119e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4119e-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.25.0"), UMLPackagePath("CIM::Device::Controller"), AMENDMENT]
class CIM_DisplayController : CIM_Controller
{
  string Description;
  string VideoProcessor;
  uint16 VideoMemoryType;
  string OtherVideoMemoryType;
  uint32 NumberOfVideoPages;
  uint32 MaxMemorySupported;
  uint16 AcceleratorCapabilities[];
  string CapabilityDescriptions[];
  string OtherVideoArchitecture;
  uint16 VideoArchitecture;
};
```

## <a name="members"></a><span data-ttu-id="4119e-106">Members</span><span class="sxs-lookup"><span data-stu-id="4119e-106">Members</span></span>

<span data-ttu-id="4119e-107">La classe **CIM \_ DisplayController** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="4119e-107">The **CIM\_DisplayController** class has these types of members:</span></span>

-   [<span data-ttu-id="4119e-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="4119e-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4119e-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="4119e-109">Properties</span></span>

<span data-ttu-id="4119e-110">La classe **CIM \_ DisplayController** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="4119e-110">The **CIM\_DisplayController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4119e-111">**AcceleratorCapabilities**</span><span class="sxs-lookup"><span data-stu-id="4119e-111">**AcceleratorCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4119e-112">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4119e-112">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="4119e-113">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4119e-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4119e-114">Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ DisplayController**.**CapabilityDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="4119e-114">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_DisplayController**.**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="4119e-115">Funzionalità grafiche e 3D del controller di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="4119e-115">The graphics and 3D capabilities of the display controller.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4119e-116">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="4119e-116">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="4119e-117">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="4119e-117">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Graphics_Accelerator"></span><span id="graphics_accelerator"></span><span id="GRAPHICS_ACCELERATOR"></span>

<span data-ttu-id="4119e-118">**Acceleratore grafico** (2)</span><span class="sxs-lookup"><span data-stu-id="4119e-118">**Graphics Accelerator** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="3D_Accelerator"></span><span id="3d_accelerator"></span><span id="3D_ACCELERATOR"></span>

<span data-ttu-id="4119e-119">**acceleratore 3D** (3)</span><span class="sxs-lookup"><span data-stu-id="4119e-119">**3D Accelerator** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI_Fast_Write"></span><span id="pci_fast_write"></span><span id="PCI_FAST_WRITE"></span>

<span data-ttu-id="4119e-120">**Scrittura veloce PCI** (4)</span><span class="sxs-lookup"><span data-stu-id="4119e-120">**PCI Fast Write** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="MultiMonitor_Support"></span><span id="multimonitor_support"></span><span id="MULTIMONITOR_SUPPORT"></span>

<span data-ttu-id="4119e-121">**Supporto di multimonitor** (5)</span><span class="sxs-lookup"><span data-stu-id="4119e-121">**MultiMonitor Support** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI_Mastering"></span><span id="pci_mastering"></span><span id="PCI_MASTERING"></span>

<span data-ttu-id="4119e-122">**Master PCI** (6)</span><span class="sxs-lookup"><span data-stu-id="4119e-122">**PCI Mastering** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Second_Monochrome_Adapter_Support"></span><span id="second_monochrome_adapter_support"></span><span id="SECOND_MONOCHROME_ADAPTER_SUPPORT"></span>

<span data-ttu-id="4119e-123">**Supporto per la seconda scheda monocromatica** (7)</span><span class="sxs-lookup"><span data-stu-id="4119e-123">**Second Monochrome Adapter Support** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Large_Memory_Address_Support"></span><span id="large_memory_address_support"></span><span id="LARGE_MEMORY_ADDRESS_SUPPORT"></span>

<span data-ttu-id="4119e-124">**Supporto per indirizzi di memoria di grandi dimensioni** (8)</span><span class="sxs-lookup"><span data-stu-id="4119e-124">**Large Memory Address Support** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4119e-125">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="4119e-125">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4119e-126">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="4119e-126">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="4119e-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4119e-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4119e-128">Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ DisplayController**.**AcceleratorCapabilities**")</span><span class="sxs-lookup"><span data-stu-id="4119e-128">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_DisplayController**.**AcceleratorCapabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="4119e-129">Spiegazione dettagliata delle funzionalità dell'acceleratore video della matrice **AcceleratorCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="4119e-129">Detailed explanations for video accelerator features of the **AcceleratorCapabilities** array.</span></span> <span data-ttu-id="4119e-130">Gli elementi in questa matrice corrispondono agli elementi della matrice in **AcceleratorCapabilities**.</span><span class="sxs-lookup"><span data-stu-id="4119e-130">The items in this array correspond to the array items in **AcceleratorCapabilities**.</span></span>

</dd> <dt>

<span data-ttu-id="4119e-131">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="4119e-131">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4119e-132">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="4119e-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4119e-133">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4119e-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4119e-134">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Video di DMTF \| \| 004,18 ")</span><span class="sxs-lookup"><span data-stu-id="4119e-134">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|004.18")</span></span>
</dt> </dl>

<span data-ttu-id="4119e-135">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="4119e-135">A text description of the object.</span></span>

</dd> <dt>

<span data-ttu-id="4119e-136">**MaxMemorySupported**</span><span class="sxs-lookup"><span data-stu-id="4119e-136">**MaxMemorySupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4119e-137">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4119e-137">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4119e-138">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4119e-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4119e-139">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("byte"), **punito** ("byte")</span><span class="sxs-lookup"><span data-stu-id="4119e-139">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes"), **PUnit** ("byte")</span></span>
</dt> </dl>

<span data-ttu-id="4119e-140">Quantità massima di memoria, in byte, supportata.</span><span class="sxs-lookup"><span data-stu-id="4119e-140">The maximum amount of memory supported, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="4119e-141">**NumberOfVideoPages**</span><span class="sxs-lookup"><span data-stu-id="4119e-141">**NumberOfVideoPages**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4119e-142">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4119e-142">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4119e-143">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4119e-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4119e-144">Il numero di pagine video supportate in base alle risoluzioni correnti e alla memoria disponibile.</span><span class="sxs-lookup"><span data-stu-id="4119e-144">The number of video pages supported given the current resolutions and available memory.</span></span>

</dd> <dt>

<span data-ttu-id="4119e-145">**OtherVideoArchitecture**</span><span class="sxs-lookup"><span data-stu-id="4119e-145">**OtherVideoArchitecture**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4119e-146">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="4119e-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4119e-147">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4119e-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4119e-148">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ DisplayController**.**VideoArchitecture**")</span><span class="sxs-lookup"><span data-stu-id="4119e-148">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_DisplayController**.**VideoArchitecture**")</span></span>
</dt> </dl>

<span data-ttu-id="4119e-149">Descrizione del tipo di architettura video quando la proprietà **VideoArchitecture** contiene "1" (other).</span><span class="sxs-lookup"><span data-stu-id="4119e-149">A description of the video architecture type when the **VideoArchitecture** property contains "1" (Other).</span></span>

</dd> <dt>

<span data-ttu-id="4119e-150">**OtherVideoMemoryType**</span><span class="sxs-lookup"><span data-stu-id="4119e-150">**OtherVideoMemoryType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4119e-151">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="4119e-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4119e-152">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4119e-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4119e-153">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ DisplayController**.**VideoMemoryType**")</span><span class="sxs-lookup"><span data-stu-id="4119e-153">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_DisplayController**.**VideoMemoryType**")</span></span>
</dt> </dl>

<span data-ttu-id="4119e-154">Tipo di memoria video quando la proprietà **VideoMemoryType** è "1" (other).</span><span class="sxs-lookup"><span data-stu-id="4119e-154">The video memory type when the **VideoMemoryType** property is "1" (Other).</span></span>

</dd> <dt>

<span data-ttu-id="4119e-155">**VideoArchitecture**</span><span class="sxs-lookup"><span data-stu-id="4119e-155">**VideoArchitecture**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4119e-156">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4119e-156">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4119e-157">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4119e-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4119e-158">L'architettura video dei controller di visualizzazione usata per generare il segnale video.</span><span class="sxs-lookup"><span data-stu-id="4119e-158">The display controllers video architecture used to generate the video signal.</span></span> <span data-ttu-id="4119e-159">In genere, un processore video dedicato genera il segnale video in conformità con l'architettura specificata.</span><span class="sxs-lookup"><span data-stu-id="4119e-159">Usually, a dedicated video processor generates the video signal in accordance with the specified architecture.</span></span> <span data-ttu-id="4119e-160">L'architettura indica la capacità massima di risoluzione del controller di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="4119e-160">The architecture indicates of the maximum resolution capability of the display controller.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4119e-161">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="4119e-161">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="4119e-162">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="4119e-162">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="CGA"></span><span id="cga"></span>

<span data-ttu-id="4119e-163">**CGA** (2)</span><span class="sxs-lookup"><span data-stu-id="4119e-163">**CGA** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="EGA"></span><span id="ega"></span>

<span data-ttu-id="4119e-164">**EGA** (3)</span><span class="sxs-lookup"><span data-stu-id="4119e-164">**EGA** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="VGA"></span><span id="vga"></span>

<span data-ttu-id="4119e-165">**VGA** (4)</span><span class="sxs-lookup"><span data-stu-id="4119e-165">**VGA** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="SVGA"></span><span id="svga"></span>

<span data-ttu-id="4119e-166">**SVGA** (5)</span><span class="sxs-lookup"><span data-stu-id="4119e-166">**SVGA** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="MDA"></span><span id="mda"></span>

<span data-ttu-id="4119e-167">**MDA** (6)</span><span class="sxs-lookup"><span data-stu-id="4119e-167">**MDA** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="HGC"></span><span id="hgc"></span>

<span data-ttu-id="4119e-168">**HGC** (7)</span><span class="sxs-lookup"><span data-stu-id="4119e-168">**HGC** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="MCGA"></span><span id="mcga"></span>

<span data-ttu-id="4119e-169">**MCGA** (8)</span><span class="sxs-lookup"><span data-stu-id="4119e-169">**MCGA** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="8514A"></span><span id="8514a"></span>

<span data-ttu-id="4119e-170">**8514a** (9)</span><span class="sxs-lookup"><span data-stu-id="4119e-170">**8514A** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="XGA"></span><span id="xga"></span>

<span data-ttu-id="4119e-171">**XGA** (10)</span><span class="sxs-lookup"><span data-stu-id="4119e-171">**XGA** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Linear_Frame_Buffer"></span><span id="linear_frame_buffer"></span><span id="LINEAR_FRAME_BUFFER"></span>

<span data-ttu-id="4119e-172">**Buffer frame lineare** (11)</span><span class="sxs-lookup"><span data-stu-id="4119e-172">**Linear Frame Buffer** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98"></span><span id="pc-98"></span>

<span data-ttu-id="4119e-173">**PC-98** (160)</span><span class="sxs-lookup"><span data-stu-id="4119e-173">**PC-98** (160)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="4119e-174">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="4119e-174">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="4119e-175">**Fornitore riservato** (0x8000..)</span><span class="sxs-lookup"><span data-stu-id="4119e-175">**Vendor Reserved** (0x8000..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4119e-176">**VideoMemoryType**</span><span class="sxs-lookup"><span data-stu-id="4119e-176">**VideoMemoryType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4119e-177">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4119e-177">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4119e-178">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4119e-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4119e-179">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Video \| 004,6 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ DisplayController**.**OtherVideoMemoryType**")</span><span class="sxs-lookup"><span data-stu-id="4119e-179">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|004.6"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_DisplayController**.**OtherVideoMemoryType**")</span></span>
</dt> </dl>

<span data-ttu-id="4119e-180">Tipo di memoria video.</span><span class="sxs-lookup"><span data-stu-id="4119e-180">The type of video memory.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4119e-181">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="4119e-181">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="4119e-182">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="4119e-182">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="VRAM"></span><span id="vram"></span>

<span data-ttu-id="4119e-183">**VRAM** (2)</span><span class="sxs-lookup"><span data-stu-id="4119e-183">**VRAM** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="DRAM"></span><span id="dram"></span>

<span data-ttu-id="4119e-184">**DRAM** (3)</span><span class="sxs-lookup"><span data-stu-id="4119e-184">**DRAM** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="SRAM"></span><span id="sram"></span>

<span data-ttu-id="4119e-185">**SRAM** (4)</span><span class="sxs-lookup"><span data-stu-id="4119e-185">**SRAM** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="WRAM"></span><span id="wram"></span>

<span data-ttu-id="4119e-186">**WRAM** (5)</span><span class="sxs-lookup"><span data-stu-id="4119e-186">**WRAM** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="EDO_RAM"></span><span id="edo_ram"></span>

<span data-ttu-id="4119e-187">**RAM EDO** (6)</span><span class="sxs-lookup"><span data-stu-id="4119e-187">**EDO RAM** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Burst_Synchronous_DRAM"></span><span id="burst_synchronous_dram"></span><span id="BURST_SYNCHRONOUS_DRAM"></span>

<span data-ttu-id="4119e-188">**DRAM sincrona a impulsi** (7)</span><span class="sxs-lookup"><span data-stu-id="4119e-188">**Burst Synchronous DRAM** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Pipelined_Burst_SRAM"></span><span id="pipelined_burst_sram"></span><span id="PIPELINED_BURST_SRAM"></span>

<span data-ttu-id="4119e-189">**SRAM** (8)</span><span class="sxs-lookup"><span data-stu-id="4119e-189">**Pipelined Burst SRAM** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="CDRAM"></span><span id="cdram"></span>

<span data-ttu-id="4119e-190">**CDRAM** (9)</span><span class="sxs-lookup"><span data-stu-id="4119e-190">**CDRAM** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="3DRAM"></span><span id="3dram"></span>

<span data-ttu-id="4119e-191">**3DRAM** (10)</span><span class="sxs-lookup"><span data-stu-id="4119e-191">**3DRAM** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="SDRAM"></span><span id="sdram"></span>

<span data-ttu-id="4119e-192">**SDRAM** (11)</span><span class="sxs-lookup"><span data-stu-id="4119e-192">**SDRAM** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SGRAM"></span><span id="sgram"></span>

<span data-ttu-id="4119e-193">**SGRAM** (12)</span><span class="sxs-lookup"><span data-stu-id="4119e-193">**SGRAM** (12)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4119e-194">**VideoProcessor**</span><span class="sxs-lookup"><span data-stu-id="4119e-194">**VideoProcessor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4119e-195">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="4119e-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4119e-196">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4119e-196">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4119e-197">Descrizione testuale del processore/controller video.</span><span class="sxs-lookup"><span data-stu-id="4119e-197">A text description of the video processor/controller.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4119e-198">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4119e-198">Requirements</span></span>



| <span data-ttu-id="4119e-199">Requisito</span><span class="sxs-lookup"><span data-stu-id="4119e-199">Requirement</span></span> | <span data-ttu-id="4119e-200">Valore</span><span class="sxs-lookup"><span data-stu-id="4119e-200">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4119e-201">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4119e-201">Minimum supported client</span></span><br/> | <span data-ttu-id="4119e-202">Windows 8</span><span class="sxs-lookup"><span data-stu-id="4119e-202">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="4119e-203">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4119e-203">Minimum supported server</span></span><br/> | <span data-ttu-id="4119e-204">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4119e-204">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="4119e-205">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="4119e-205">Namespace</span></span><br/>                | <span data-ttu-id="4119e-206">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="4119e-206">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="4119e-207">MOF</span><span class="sxs-lookup"><span data-stu-id="4119e-207">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4119e-208"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4119e-208"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4119e-209">DLL</span><span class="sxs-lookup"><span data-stu-id="4119e-209">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4119e-210"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4119e-210"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="4119e-211">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4119e-211">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4119e-212">**\_Controller CIM**</span><span class="sxs-lookup"><span data-stu-id="4119e-212">**CIM\_Controller**</span></span>](cim-controller.md)
</dt> </dl>

 

