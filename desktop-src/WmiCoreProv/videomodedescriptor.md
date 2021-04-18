---
description: Contiene gli elementi del descrittore della modalità per la matrice MonitorSourceModes nella classe WmiMonitorListedSupportedSourceModes.
ms.assetid: 6d6c846d-caec-41a8-8a88-1c1e14bc0473
title: Classe VideoModeDescriptor
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- VideoModeDescriptor
- VideoModeDescriptor.CompositePolarityType
- VideoModeDescriptor.HorizontalActivePixels
- VideoModeDescriptor.HorizontalBlankingPixels
- VideoModeDescriptor.HorizontalBorder
- VideoModeDescriptor.HorizontalImageSize
- VideoModeDescriptor.HorizontalPolarityType
- VideoModeDescriptor.HorizontalRefreshRateDenominator
- VideoModeDescriptor.HorizontalRefreshRateNumerator
- VideoModeDescriptor.HorizontalSyncOffset
- VideoModeDescriptor.HorizontalSyncPulseWidth
- VideoModeDescriptor.IsInterlaced
- VideoModeDescriptor.IsSerrationRequired
- VideoModeDescriptor.IsSyncOnRGB
- VideoModeDescriptor.PixelClockRate
- VideoModeDescriptor.StereoModeType
- VideoModeDescriptor.SyncSignalType
- VideoModeDescriptor.VerticalActivePixels
- VideoModeDescriptor.VerticalBlankingPixels
- VideoModeDescriptor.VerticalBorder
- VideoModeDescriptor.VerticalImageSize
- VideoModeDescriptor.VerticalRefreshRateDenominator
- VideoModeDescriptor.VerticalRefreshRateNumerator
- VideoModeDescriptor.VerticalSyncOffset
- VideoModeDescriptor.VerticalPolarityType
- VideoModeDescriptor.VerticalSyncPulseWidth
- VideoModeDescriptor.VideoStandardType
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 06094b24b6b8197eab89b65cd5a9a83f46b39f95
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348426"
---
# <a name="videomodedescriptor-class"></a><span data-ttu-id="8f88d-103">Classe VideoModeDescriptor</span><span class="sxs-lookup"><span data-stu-id="8f88d-103">VideoModeDescriptor class</span></span>

<span data-ttu-id="8f88d-104">La classe WMI **VideoModeDescriptorVideo** contiene elementi del descrittore della modalità per la matrice **MonitorSourceModes** nella classe [**WmiMonitorListedSupportedSourceModes**](wmimonitorlistedsupportedsourcemodes.md) .</span><span class="sxs-lookup"><span data-stu-id="8f88d-104">The **VideoModeDescriptorVideo** WMI class contains mode descriptor elements for the **MonitorSourceModes** array in the [**WmiMonitorListedSupportedSourceModes**](wmimonitorlistedsupportedsourcemodes.md) class.</span></span> <span data-ttu-id="8f88d-105">Questi elementi includono funzionalità di monitoraggio, ad esempio frequenza di aggiornamento, caratteristiche dei pixel o dimensioni dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="8f88d-105">These elements include monitor features such as refresh rate, pixel characteristics, or image size.</span></span> <span data-ttu-id="8f88d-106">La classe **VideoModeDescriptorVideo** contiene informazioni che sono un superset dei dati disponibili nei blocchi temporali stabiliti, standard e dettagliati.</span><span class="sxs-lookup"><span data-stu-id="8f88d-106">The **VideoModeDescriptorVideo** class contains information that is a superset of the data available from established, standard, and detailed timing blocks.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f88d-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8f88d-107">Syntax</span></span>

``` syntax
class VideoModeDescriptor : WmiMonitorSupportedVideoModes
{
  uint8   CompositePolarityType;
  uint16  HorizontalActivePixels;
  uint16  HorizontalBlankingPixels;
  uint16  HorizontalBorder;
  uint16  HorizontalImageSize;
  uint8   HorizontalPolarityType;
  uint16  HorizontalRefreshRateDenominator;
  uint16  HorizontalRefreshRateNumerator;
  uint16  HorizontalSyncOffset;
  uint16  HorizontalSyncPulseWidth;
  boolean IsInterlaced;
  uint8   IsSerrationRequired;
  uint8   IsSyncOnRGB;
  uint32  PixelClockRate;
  uint8   StereoModeType;
  uint8   SyncSignalType;
  uint16  VerticalActivePixels;
  uint16  VerticalBlankingPixels;
  uint16  VerticalBorder;
  uint16  VerticalImageSize;
  uint16  VerticalRefreshRateDenominator;
  uint16  VerticalRefreshRateNumerator;
  uint16  VerticalSyncOffset;
  uint8   VerticalPolarityType;
  uint16  VerticalSyncPulseWidth;
  uint8   VideoStandardType;
};
```

## <a name="members"></a><span data-ttu-id="8f88d-108">Members</span><span class="sxs-lookup"><span data-stu-id="8f88d-108">Members</span></span>

<span data-ttu-id="8f88d-109">La classe **VideoModeDescriptor** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="8f88d-109">The **VideoModeDescriptor** class has these types of members:</span></span>

-   [<span data-ttu-id="8f88d-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="8f88d-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8f88d-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="8f88d-111">Properties</span></span>

<span data-ttu-id="8f88d-112">La classe **VideoModeDescriptor** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="8f88d-112">The **VideoModeDescriptor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8f88d-113">**CompositePolarityType**</span><span class="sxs-lookup"><span data-stu-id="8f88d-113">**CompositePolarityType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f88d-114">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="8f88d-114">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="8f88d-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8f88d-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f88d-116">Tipo di polarità composita.</span><span class="sxs-lookup"><span data-stu-id="8f88d-116">Composite polarity type.</span></span> <span data-ttu-id="8f88d-117">Si tratta di una polarità degli impulsi di sincronizzazione orizzontali al di fuori della sincronizzazione verticale.</span><span class="sxs-lookup"><span data-stu-id="8f88d-117">This is polarity of horizontal sync pulses outside of vertical sync.</span></span>



| <span data-ttu-id="8f88d-118">Valore</span><span class="sxs-lookup"><span data-stu-id="8f88d-118">Value</span></span>                                                                              | <span data-ttu-id="8f88d-119">Significato</span><span class="sxs-lookup"><span data-stu-id="8f88d-119">Meaning</span></span>                                                                    |
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8f88d-120"><dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="8f88d-120"><dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="8f88d-121">La polarità composita è positiva.</span><span class="sxs-lookup"><span data-stu-id="8f88d-121">Composite polarity is positive.</span></span><br/>                                 |
| <dl> <span data-ttu-id="8f88d-122"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="8f88d-122"><dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="8f88d-123">La polarità composita è negativa.</span><span class="sxs-lookup"><span data-stu-id="8f88d-123">Composite polarity is negative.</span></span><br/>                                 |
| <dl> <span data-ttu-id="8f88d-124"><dt>2 (0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="8f88d-124"><dt>2 (0x2)</dt></span></span> </dl> | <span data-ttu-id="8f88d-125">Non applicabile.</span><span class="sxs-lookup"><span data-stu-id="8f88d-125">Not applicable.</span></span> <span data-ttu-id="8f88d-126">Il tipo di sincronizzazione del segnale deve essere composto da una composizione digitale.</span><span class="sxs-lookup"><span data-stu-id="8f88d-126">The signal sync type must be digital composite.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="8f88d-127">**HorizontalActivePixels**</span><span class="sxs-lookup"><span data-stu-id="8f88d-127">**HorizontalActivePixels**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f88d-128">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8f88d-128">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8f88d-129">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8f88d-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f88d-130">Numero di pixel attivi orizzontalmente.</span><span class="sxs-lookup"><span data-stu-id="8f88d-130">Number of horizontally active pixels.</span></span>

</dd> <dt>

<span data-ttu-id="8f88d-131">**HorizontalBlankingPixels**</span><span class="sxs-lookup"><span data-stu-id="8f88d-131">**HorizontalBlankingPixels**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f88d-132">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8f88d-132">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8f88d-133">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8f88d-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f88d-134">Numero di pixel vuoti orizzontalmente</span><span class="sxs-lookup"><span data-stu-id="8f88d-134">Number of horizontally blanking pixels</span></span>

</dd> <dt>

<span data-ttu-id="8f88d-135">**HorizontalBorder**</span><span class="sxs-lookup"><span data-stu-id="8f88d-135">**HorizontalBorder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f88d-136">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8f88d-136">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8f88d-137">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8f88d-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f88d-138">Bordo orizzontale.</span><span class="sxs-lookup"><span data-stu-id="8f88d-138">Horizontal border.</span></span>

</dd> <dt>

<span data-ttu-id="8f88d-139">**HorizontalImageSize**</span><span class="sxs-lookup"><span data-stu-id="8f88d-139">**HorizontalImageSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f88d-140">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8f88d-140">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8f88d-141">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8f88d-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f88d-142">Dimensione dell'immagine orizzontale in millimetri (mm).</span><span class="sxs-lookup"><span data-stu-id="8f88d-142">Horizontal image size in millimeters (mm).</span></span>

</dd> <dt>

<span data-ttu-id="8f88d-143">**HorizontalPolarityType**</span><span class="sxs-lookup"><span data-stu-id="8f88d-143">**HorizontalPolarityType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f88d-144">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="8f88d-144">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="8f88d-145">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8f88d-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f88d-146">Tipo di polarità orizzontale.</span><span class="sxs-lookup"><span data-stu-id="8f88d-146">Horizontal polarity type.</span></span>



| <span data-ttu-id="8f88d-147">Valore</span><span class="sxs-lookup"><span data-stu-id="8f88d-147">Value</span></span>                                                                              | <span data-ttu-id="8f88d-148">Significato</span><span class="sxs-lookup"><span data-stu-id="8f88d-148">Meaning</span></span>                                                                   |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8f88d-149"><dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="8f88d-149"><dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="8f88d-150">La polarità orizzontale è positiva.</span><span class="sxs-lookup"><span data-stu-id="8f88d-150">Horizontal polarity is positive.</span></span><br/>                               |
| <dl> <span data-ttu-id="8f88d-151"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="8f88d-151"><dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="8f88d-152">La polarità orizzontale è negativa.</span><span class="sxs-lookup"><span data-stu-id="8f88d-152">Horizontal polarity is negative.</span></span><br/>                               |
| <dl> <span data-ttu-id="8f88d-153"><dt>2 (0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="8f88d-153"><dt>2 (0x2)</dt></span></span> </dl> | <span data-ttu-id="8f88d-154">Non applicabile.</span><span class="sxs-lookup"><span data-stu-id="8f88d-154">Not applicable.</span></span> <span data-ttu-id="8f88d-155">Il tipo di sincronizzazione del segnale deve essere digitale separato.</span><span class="sxs-lookup"><span data-stu-id="8f88d-155">The signal sync type must be digital separate.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="8f88d-156">**HorizontalRefreshRateDenominator**</span><span class="sxs-lookup"><span data-stu-id="8f88d-156">**HorizontalRefreshRateDenominator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f88d-157">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8f88d-157">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8f88d-158">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8f88d-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f88d-159">Denominatore frequenza di aggiornamento orizzontale.</span><span class="sxs-lookup"><span data-stu-id="8f88d-159">Horizontal refresh rate denominator.</span></span>

</dd> <dt>

<span data-ttu-id="8f88d-160">**HorizontalRefreshRateNumerator**</span><span class="sxs-lookup"><span data-stu-id="8f88d-160">**HorizontalRefreshRateNumerator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f88d-161">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8f88d-161">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8f88d-162">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8f88d-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f88d-163">Numeratore della frequenza di aggiornamento orizzontale in Hertz (Hz).</span><span class="sxs-lookup"><span data-stu-id="8f88d-163">Horizontal refresh rate numerator in Hertz (Hz).</span></span>

</dd> <dt>

<span data-ttu-id="8f88d-164">**HorizontalSyncOffset**</span><span class="sxs-lookup"><span data-stu-id="8f88d-164">**HorizontalSyncOffset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f88d-165">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8f88d-165">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8f88d-166">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8f88d-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f88d-167">Offset della sincronizzazione orizzontale.</span><span class="sxs-lookup"><span data-stu-id="8f88d-167">Horizontal sync offset.</span></span>

</dd> <dt>

<span data-ttu-id="8f88d-168">**HorizontalSyncPulseWidth**</span><span class="sxs-lookup"><span data-stu-id="8f88d-168">**HorizontalSyncPulseWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f88d-169">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8f88d-169">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8f88d-170">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8f88d-170">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f88d-171">Larghezza impulso della sincronizzazione orizzontale.</span><span class="sxs-lookup"><span data-stu-id="8f88d-171">Horizontal sync pulse width.</span></span>

</dd> <dt>

<span data-ttu-id="8f88d-172">**IsInterlaced**</span><span class="sxs-lookup"><span data-stu-id="8f88d-172">**IsInterlaced**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f88d-173">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="8f88d-173">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8f88d-174">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8f88d-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f88d-175">Indica se la modalità di visualizzazione è interlacciata.</span><span class="sxs-lookup"><span data-stu-id="8f88d-175">Indicates whether the display mode is interlaced.</span></span>

</dd> <dt>

<span data-ttu-id="8f88d-176">**IsSerrationRequired**</span><span class="sxs-lookup"><span data-stu-id="8f88d-176">**IsSerrationRequired**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f88d-177">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="8f88d-177">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="8f88d-178">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8f88d-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f88d-179">Indica il tipo di seghettazione obbligatorio, se appropriato.</span><span class="sxs-lookup"><span data-stu-id="8f88d-179">Indicates what type of serration is required, if appropriate.</span></span>



| <span data-ttu-id="8f88d-180">Valore</span><span class="sxs-lookup"><span data-stu-id="8f88d-180">Value</span></span>                                                                              | <span data-ttu-id="8f88d-181">Significato</span><span class="sxs-lookup"><span data-stu-id="8f88d-181">Meaning</span></span>                                                                                                  |
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8f88d-182"><dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="8f88d-182"><dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="8f88d-183">Il controller deve fornire la sincronizzazione orizzontale durante la sincronizzazione verticale.</span><span class="sxs-lookup"><span data-stu-id="8f88d-183">Controller shall supply horizontal sync during vertical sync.</span></span><br/>                                 |
| <dl> <span data-ttu-id="8f88d-184"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="8f88d-184"><dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="8f88d-185">Il controller non deve fornire la sincronizzazione orizzontale durante la sincronizzazione verticale.</span><span class="sxs-lookup"><span data-stu-id="8f88d-185">Controller shall not supply horizontal sync during vertical sync.</span></span><br/>                             |
| <dl> <span data-ttu-id="8f88d-186"><dt>2 (0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="8f88d-186"><dt>2 (0x2)</dt></span></span> </dl> | <span data-ttu-id="8f88d-187">Non applicabile.</span><span class="sxs-lookup"><span data-stu-id="8f88d-187">Not applicable.</span></span> <span data-ttu-id="8f88d-188">Il tipo di sincronizzazione del segnale deve essere bipolare, composito analogico o composito digitale.</span><span class="sxs-lookup"><span data-stu-id="8f88d-188">The signal sync type must be bipolar, analog composite, or digital composite.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="8f88d-189">**IsSyncOnRGB**</span><span class="sxs-lookup"><span data-stu-id="8f88d-189">**IsSyncOnRGB**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f88d-190">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="8f88d-190">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="8f88d-191">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8f88d-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f88d-192">Indica quali righe del segnale video devono essere sincronizzate, se appropriato.</span><span class="sxs-lookup"><span data-stu-id="8f88d-192">Indicates which video signal lines should be synchronized, if appropriate.</span></span>



| <span data-ttu-id="8f88d-193">Valore</span><span class="sxs-lookup"><span data-stu-id="8f88d-193">Value</span></span>                                                                              | <span data-ttu-id="8f88d-194">Significato</span><span class="sxs-lookup"><span data-stu-id="8f88d-194">Meaning</span></span>                                                                           |
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8f88d-195"><dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="8f88d-195"><dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="8f88d-196">L'impulso di sincronizzazione dovrebbe essere visualizzato in tutte e 3 le linee del segnale video.</span><span class="sxs-lookup"><span data-stu-id="8f88d-196">Sync pulse should appear on all 3 video signal lines.</span></span><br/>                  |
| <dl> <span data-ttu-id="8f88d-197"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="8f88d-197"><dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="8f88d-198">L'impulso di sincronizzazione dovrebbe essere visualizzato solo sulla linea del segnale video verde.</span><span class="sxs-lookup"><span data-stu-id="8f88d-198">Sync pulse should only appear on the green video signal line.</span></span><br/>          |
| <dl> <span data-ttu-id="8f88d-199"><dt>2 (0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="8f88d-199"><dt>2 (0x2)</dt></span></span> </dl> | <span data-ttu-id="8f88d-200">Non applicabile.</span><span class="sxs-lookup"><span data-stu-id="8f88d-200">Not applicable.</span></span> <span data-ttu-id="8f88d-201">Il tipo di sincronizzazione del segnale deve essere composito analogico bipolare.</span><span class="sxs-lookup"><span data-stu-id="8f88d-201">The signal sync type must be bipolar analog composite.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="8f88d-202">**PixelClockRate**</span><span class="sxs-lookup"><span data-stu-id="8f88d-202">**PixelClockRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f88d-203">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8f88d-203">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f88d-204">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8f88d-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f88d-205">Frequenza di clock in pixel in Hertz (Hz).</span><span class="sxs-lookup"><span data-stu-id="8f88d-205">Pixel clock rate in Hertz (Hz).</span></span>

</dd> <dt>

<span data-ttu-id="8f88d-206">**StereoModeType**</span><span class="sxs-lookup"><span data-stu-id="8f88d-206">**StereoModeType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f88d-207">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="8f88d-207">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="8f88d-208">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8f88d-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f88d-209">Tipo di modalità stereo.</span><span class="sxs-lookup"><span data-stu-id="8f88d-209">Stereo mode type.</span></span> <span data-ttu-id="8f88d-210">Nella tabella seguente sono elencati i valori possibili.</span><span class="sxs-lookup"><span data-stu-id="8f88d-210">The following table lists the possible values.</span></span>



| <span data-ttu-id="8f88d-211">Valore</span><span class="sxs-lookup"><span data-stu-id="8f88d-211">Value</span></span>                                                                              | <span data-ttu-id="8f88d-212">Significato</span><span class="sxs-lookup"><span data-stu-id="8f88d-212">Meaning</span></span>                                                             |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <span data-ttu-id="8f88d-213"><dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="8f88d-213"><dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="8f88d-214">Nessun stereo.</span><span class="sxs-lookup"><span data-stu-id="8f88d-214">No stereo.</span></span><br/>                                               |
| <dl> <span data-ttu-id="8f88d-215"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="8f88d-215"><dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="8f88d-216">Campo stereo sequenziale con immagine a destra nella sincronizzazione stereo.</span><span class="sxs-lookup"><span data-stu-id="8f88d-216">Field sequential stereo with right image on stereo sync.</span></span><br/> |
| <dl> <span data-ttu-id="8f88d-217"><dt>2 (0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="8f88d-217"><dt>2 (0x2)</dt></span></span> </dl> | <span data-ttu-id="8f88d-218">Campo stereo sequenziale con immagine a sinistra in sincronizzazione stereo.</span><span class="sxs-lookup"><span data-stu-id="8f88d-218">Field sequential stereo with left image on stereo sync.</span></span><br/>  |
| <dl> <span data-ttu-id="8f88d-219"><dt>3 (0x3)</dt></span><span class="sxs-lookup"><span data-stu-id="8f88d-219"><dt>3 (0x3)</dt></span></span> </dl> | <span data-ttu-id="8f88d-220">Stereo Interleaved a 2 vie con immagine corretta su righe pari.</span><span class="sxs-lookup"><span data-stu-id="8f88d-220">2-way Interleaved Stereo with Right Image on Even Lines.</span></span><br/> |
| <dl> <span data-ttu-id="8f88d-221"><dt>4 (0x4)</dt></span><span class="sxs-lookup"><span data-stu-id="8f88d-221"><dt>4 (0x4)</dt></span></span> </dl> | <span data-ttu-id="8f88d-222">Stereo a 2 vie con interfoliazione con immagine a sinistra in linee pari.</span><span class="sxs-lookup"><span data-stu-id="8f88d-222">2-way Interleaved Stereo with Left Image on Even Lines.</span></span><br/>  |
| <dl> <span data-ttu-id="8f88d-223"><dt>5 (0x5)</dt></span><span class="sxs-lookup"><span data-stu-id="8f88d-223"><dt>5 (0x5)</dt></span></span> </dl> | <span data-ttu-id="8f88d-224">Stereo con interfoliazione a 4 vie.</span><span class="sxs-lookup"><span data-stu-id="8f88d-224">4-way Interleaved Stereo.</span></span><br/>                                |
| <dl> <span data-ttu-id="8f88d-225"><dt>6 (0x6)</dt></span><span class="sxs-lookup"><span data-stu-id="8f88d-225"><dt>6 (0x6)</dt></span></span> </dl> | <span data-ttu-id="8f88d-226">Stereo con interfoliazione affiancati.</span><span class="sxs-lookup"><span data-stu-id="8f88d-226">Side-by-Side Interleaved Stereo.</span></span><br/>                         |



 

</dd> <dt>

<span data-ttu-id="8f88d-227">**SyncSignalType**</span><span class="sxs-lookup"><span data-stu-id="8f88d-227">**SyncSignalType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f88d-228">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="8f88d-228">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="8f88d-229">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8f88d-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f88d-230">Tipo di sincronizzazione segnale.</span><span class="sxs-lookup"><span data-stu-id="8f88d-230">Signal sync type.</span></span> <span data-ttu-id="8f88d-231">Nella tabella seguente sono elencati i valori possibili.</span><span class="sxs-lookup"><span data-stu-id="8f88d-231">The following table lists the possible values.</span></span>



| <span data-ttu-id="8f88d-232">Valore</span><span class="sxs-lookup"><span data-stu-id="8f88d-232">Value</span></span>                                                                              | <span data-ttu-id="8f88d-233">Significato</span><span class="sxs-lookup"><span data-stu-id="8f88d-233">Meaning</span></span>                             |
|------------------------------------------------------------------------------------|-------------------------------------|
| <dl> <span data-ttu-id="8f88d-234"><dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="8f88d-234"><dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="8f88d-235">Composito analogico</span><span class="sxs-lookup"><span data-stu-id="8f88d-235">Analog Composite</span></span><br/>         |
| <dl> <span data-ttu-id="8f88d-236"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="8f88d-236"><dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="8f88d-237">Composite analogico bipolare</span><span class="sxs-lookup"><span data-stu-id="8f88d-237">Bipolar Analog Composite</span></span><br/> |
| <dl> <span data-ttu-id="8f88d-238"><dt>2 (0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="8f88d-238"><dt>2 (0x2)</dt></span></span> </dl> | <span data-ttu-id="8f88d-239">Composizione digitale</span><span class="sxs-lookup"><span data-stu-id="8f88d-239">Digital Composite</span></span><br/>        |
| <dl> <span data-ttu-id="8f88d-240"><dt>3 (0x3)</dt></span><span class="sxs-lookup"><span data-stu-id="8f88d-240"><dt>3 (0x3)</dt></span></span> </dl> | <span data-ttu-id="8f88d-241">Separato digitale</span><span class="sxs-lookup"><span data-stu-id="8f88d-241">Digital Separate</span></span><br/>         |



 

</dd> <dt>

<span data-ttu-id="8f88d-242">**VerticalActivePixels**</span><span class="sxs-lookup"><span data-stu-id="8f88d-242">**VerticalActivePixels**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f88d-243">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8f88d-243">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8f88d-244">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8f88d-244">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f88d-245">Numero di pixel attivi verticalmente.</span><span class="sxs-lookup"><span data-stu-id="8f88d-245">Number of vertically active pixels.</span></span>

</dd> <dt>

<span data-ttu-id="8f88d-246">**VerticalBlankingPixels**</span><span class="sxs-lookup"><span data-stu-id="8f88d-246">**VerticalBlankingPixels**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f88d-247">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8f88d-247">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8f88d-248">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8f88d-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f88d-249">Numero di pixel vuoti verticali.</span><span class="sxs-lookup"><span data-stu-id="8f88d-249">Number of vertically blanking pixels.</span></span>

</dd> <dt>

<span data-ttu-id="8f88d-250">**VerticalBorder**</span><span class="sxs-lookup"><span data-stu-id="8f88d-250">**VerticalBorder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f88d-251">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8f88d-251">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8f88d-252">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8f88d-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f88d-253">Bordo verticale.</span><span class="sxs-lookup"><span data-stu-id="8f88d-253">Vertical border.</span></span>

</dd> <dt>

<span data-ttu-id="8f88d-254">**VerticalImageSize**</span><span class="sxs-lookup"><span data-stu-id="8f88d-254">**VerticalImageSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f88d-255">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8f88d-255">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8f88d-256">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8f88d-256">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f88d-257">Dimensioni verticali dell'immagine in millimetri (mm).</span><span class="sxs-lookup"><span data-stu-id="8f88d-257">Vertical image size in millimeters (mm).</span></span>

</dd> <dt>

<span data-ttu-id="8f88d-258">**VerticalPolarityType**</span><span class="sxs-lookup"><span data-stu-id="8f88d-258">**VerticalPolarityType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f88d-259">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="8f88d-259">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="8f88d-260">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8f88d-260">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f88d-261">Tipo di polarità verticale.</span><span class="sxs-lookup"><span data-stu-id="8f88d-261">Vertical polarity type.</span></span>



| <span data-ttu-id="8f88d-262">Valore</span><span class="sxs-lookup"><span data-stu-id="8f88d-262">Value</span></span>                                                                              | <span data-ttu-id="8f88d-263">Significato</span><span class="sxs-lookup"><span data-stu-id="8f88d-263">Meaning</span></span>                                                                   |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8f88d-264"><dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="8f88d-264"><dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="8f88d-265">La polarità verticale è positiva.</span><span class="sxs-lookup"><span data-stu-id="8f88d-265">Vertical polarity is positive.</span></span><br/>                                 |
| <dl> <span data-ttu-id="8f88d-266"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="8f88d-266"><dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="8f88d-267">La polarità verticale è negativa</span><span class="sxs-lookup"><span data-stu-id="8f88d-267">Vertical polarity is negative</span></span><br/>                                  |
| <dl> <span data-ttu-id="8f88d-268"><dt>2 (0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="8f88d-268"><dt>2 (0x2)</dt></span></span> </dl> | <span data-ttu-id="8f88d-269">Non applicabile.</span><span class="sxs-lookup"><span data-stu-id="8f88d-269">Not applicable.</span></span> <span data-ttu-id="8f88d-270">Il tipo di sincronizzazione del segnale deve essere digitale separato.</span><span class="sxs-lookup"><span data-stu-id="8f88d-270">The signal sync type must be digital separate.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="8f88d-271">**VerticalRefreshRateDenominator**</span><span class="sxs-lookup"><span data-stu-id="8f88d-271">**VerticalRefreshRateDenominator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f88d-272">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8f88d-272">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8f88d-273">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8f88d-273">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f88d-274">Denominatore frequenza di aggiornamento verticale.</span><span class="sxs-lookup"><span data-stu-id="8f88d-274">Vertical refresh rate denominator.</span></span>

</dd> <dt>

<span data-ttu-id="8f88d-275">**VerticalRefreshRateNumerator**</span><span class="sxs-lookup"><span data-stu-id="8f88d-275">**VerticalRefreshRateNumerator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f88d-276">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8f88d-276">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8f88d-277">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8f88d-277">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f88d-278">Numeratore della frequenza di aggiornamento verticale in Hertz (Hz).</span><span class="sxs-lookup"><span data-stu-id="8f88d-278">Vertical refresh rate numerator in Hertz (Hz).</span></span>

</dd> <dt>

<span data-ttu-id="8f88d-279">**VerticalSyncOffset**</span><span class="sxs-lookup"><span data-stu-id="8f88d-279">**VerticalSyncOffset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f88d-280">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8f88d-280">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8f88d-281">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8f88d-281">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f88d-282">Offset sincronizzazione verticale.</span><span class="sxs-lookup"><span data-stu-id="8f88d-282">Vertical sync offset.</span></span>

</dd> <dt>

<span data-ttu-id="8f88d-283">**VerticalSyncPulseWidth**</span><span class="sxs-lookup"><span data-stu-id="8f88d-283">**VerticalSyncPulseWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f88d-284">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8f88d-284">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8f88d-285">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8f88d-285">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f88d-286">Larghezza impulso della sincronizzazione verticale.</span><span class="sxs-lookup"><span data-stu-id="8f88d-286">Vertical sync pulse width.</span></span>

</dd> <dt>

<span data-ttu-id="8f88d-287">VideoStandardType</span><span class="sxs-lookup"><span data-stu-id="8f88d-287">VideoStandardType</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f88d-288">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="8f88d-288">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="8f88d-289">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8f88d-289">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f88d-290">Tipo di video standard.</span><span class="sxs-lookup"><span data-stu-id="8f88d-290">Video standard type.</span></span>



| <span data-ttu-id="8f88d-291">Valore</span><span class="sxs-lookup"><span data-stu-id="8f88d-291">Value</span></span>                                                                                | <span data-ttu-id="8f88d-292">Significato</span><span class="sxs-lookup"><span data-stu-id="8f88d-292">Meaning</span></span>                                                                                                        |
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8f88d-293"><dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="8f88d-293"><dt>0 (0x0)</dt></span></span> </dl>   | <span data-ttu-id="8f88d-294">Altro</span><span class="sxs-lookup"><span data-stu-id="8f88d-294">Other</span></span><br/>                                                                                               |
| <dl> <span data-ttu-id="8f88d-295"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="8f88d-295"><dt>1 (0x1)</dt></span></span> </dl>   | <span data-ttu-id="8f88d-296">VESA DMT.</span><span class="sxs-lookup"><span data-stu-id="8f88d-296">VESA DMT.</span></span> <span data-ttu-id="8f88d-297">Da video Electronics Standard Association (VESA) display monitor Times Specification.</span><span class="sxs-lookup"><span data-stu-id="8f88d-297">From Video Electronics Standard Association (VESA) Display Monitor Timings specification.</span></span><br/> |
| <dl> <span data-ttu-id="8f88d-298"><dt>2 (0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="8f88d-298"><dt>2 (0x2)</dt></span></span> </dl>   | <span data-ttu-id="8f88d-299">GTF VESA.</span><span class="sxs-lookup"><span data-stu-id="8f88d-299">VESA GTF.</span></span> <span data-ttu-id="8f88d-300">Dallo standard delle formule per la temporizzazione VESA generalizzata.</span><span class="sxs-lookup"><span data-stu-id="8f88d-300">From VESA Generalized Timing Formula standard.</span></span><br/>                                            |
| <dl> <span data-ttu-id="8f88d-301"><dt>3 (0x3)</dt></span><span class="sxs-lookup"><span data-stu-id="8f88d-301"><dt>3 (0x3)</dt></span></span> </dl>   | <span data-ttu-id="8f88d-302">Standard VESA CVT/da VESA Coordinated video Times standard.</span><span class="sxs-lookup"><span data-stu-id="8f88d-302">VESA CVT/ From VESA Coordinated Video Timings standard.</span></span><br/>                                             |
| <dl> <span data-ttu-id="8f88d-303"><dt>4 (0x4)</dt></span><span class="sxs-lookup"><span data-stu-id="8f88d-303"><dt>4 (0x4)</dt></span></span> </dl>   | <span data-ttu-id="8f88d-304">IBM</span><span class="sxs-lookup"><span data-stu-id="8f88d-304">IBM</span></span><br/>                                                                                                 |
| <dl> <span data-ttu-id="8f88d-305"><dt>5 (0x5)</dt></span><span class="sxs-lookup"><span data-stu-id="8f88d-305"><dt>5 (0x5)</dt></span></span> </dl>   | <span data-ttu-id="8f88d-306">APPLE</span><span class="sxs-lookup"><span data-stu-id="8f88d-306">APPLE</span></span><br/>                                                                                               |
| <dl> <span data-ttu-id="8f88d-307"><dt>6 (0x6)</dt></span><span class="sxs-lookup"><span data-stu-id="8f88d-307"><dt>6 (0x6)</dt></span></span> </dl>   | <span data-ttu-id="8f88d-308">NTSC M</span><span class="sxs-lookup"><span data-stu-id="8f88d-308">NTSC M</span></span><br/>                                                                                              |
| <dl> <span data-ttu-id="8f88d-309"><dt>7 (0x7)</dt></span><span class="sxs-lookup"><span data-stu-id="8f88d-309"><dt>7 (0x7)</dt></span></span> </dl>   | <span data-ttu-id="8f88d-310">NTSC J</span><span class="sxs-lookup"><span data-stu-id="8f88d-310">NTSC J</span></span><br/>                                                                                              |
| <dl> <span data-ttu-id="8f88d-311"><dt>8 (0x8)</dt></span><span class="sxs-lookup"><span data-stu-id="8f88d-311"><dt>8 (0x8)</dt></span></span> </dl>   | <span data-ttu-id="8f88d-312">NTSC 433</span><span class="sxs-lookup"><span data-stu-id="8f88d-312">NTSC 433</span></span><br/>                                                                                            |
| <dl> <span data-ttu-id="8f88d-313"><dt>9 (0x9)</dt></span><span class="sxs-lookup"><span data-stu-id="8f88d-313"><dt>9 (0x9)</dt></span></span> </dl>   | <span data-ttu-id="8f88d-314">PAL B</span><span class="sxs-lookup"><span data-stu-id="8f88d-314">PAL B</span></span><br/>                                                                                               |
| <dl> <span data-ttu-id="8f88d-315"><dt>10 (0xA)</dt></span><span class="sxs-lookup"><span data-stu-id="8f88d-315"><dt>10 (0xA)</dt></span></span> </dl>  | <span data-ttu-id="8f88d-316">PAL B1</span><span class="sxs-lookup"><span data-stu-id="8f88d-316">PAL B1</span></span><br/>                                                                                              |
| <dl> <span data-ttu-id="8f88d-317"><dt>11 (0xB)</dt></span><span class="sxs-lookup"><span data-stu-id="8f88d-317"><dt>11 (0xB)</dt></span></span> </dl>  | <span data-ttu-id="8f88d-318">PAL G</span><span class="sxs-lookup"><span data-stu-id="8f88d-318">PAL G</span></span><br/>                                                                                               |
| <dl> <span data-ttu-id="8f88d-319"><dt>12 (0xC)</dt></span><span class="sxs-lookup"><span data-stu-id="8f88d-319"><dt>12 (0xC)</dt></span></span> </dl>  | <span data-ttu-id="8f88d-320">PAL H</span><span class="sxs-lookup"><span data-stu-id="8f88d-320">PAL H</span></span><br/>                                                                                               |
| <dl> <span data-ttu-id="8f88d-321"><dt>13 (0xD)</dt></span><span class="sxs-lookup"><span data-stu-id="8f88d-321"><dt>13 (0xD)</dt></span></span> </dl>  | <span data-ttu-id="8f88d-322">ELENCO DI ACCESSO ALLA PUBBLICAZIONE</span><span class="sxs-lookup"><span data-stu-id="8f88d-322">PAL I</span></span><br/>                                                                                               |
| <dl> <span data-ttu-id="8f88d-323"><dt>14 (0xE)</dt></span><span class="sxs-lookup"><span data-stu-id="8f88d-323"><dt>14 (0xE)</dt></span></span> </dl>  | <span data-ttu-id="8f88d-324">PAL D</span><span class="sxs-lookup"><span data-stu-id="8f88d-324">PAL D</span></span><br/>                                                                                               |
| <dl> <span data-ttu-id="8f88d-325"><dt>15 (0xF)</dt></span><span class="sxs-lookup"><span data-stu-id="8f88d-325"><dt>15 (0xF)</dt></span></span> </dl>  | <span data-ttu-id="8f88d-326">PAL N</span><span class="sxs-lookup"><span data-stu-id="8f88d-326">PAL N</span></span><br/>                                                                                               |
| <dl> <span data-ttu-id="8f88d-327"><dt>16 (0x10)</dt></span><span class="sxs-lookup"><span data-stu-id="8f88d-327"><dt>16 (0x10)</dt></span></span> </dl> | <span data-ttu-id="8f88d-328">NC PAL</span><span class="sxs-lookup"><span data-stu-id="8f88d-328">PAL NC</span></span><br/>                                                                                              |
| <dl> <span data-ttu-id="8f88d-329"><dt>17 (0x11)</dt></span><span class="sxs-lookup"><span data-stu-id="8f88d-329"><dt>17 (0x11)</dt></span></span> </dl> | <span data-ttu-id="8f88d-330">SECAM B</span><span class="sxs-lookup"><span data-stu-id="8f88d-330">SECAM B</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="8f88d-331"><dt>18 (0x12)</dt></span><span class="sxs-lookup"><span data-stu-id="8f88d-331"><dt>18 (0x12)</dt></span></span> </dl> | <span data-ttu-id="8f88d-332">SECAM D</span><span class="sxs-lookup"><span data-stu-id="8f88d-332">SECAM D</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="8f88d-333"><dt>19 (0x13)</dt></span><span class="sxs-lookup"><span data-stu-id="8f88d-333"><dt>19 (0x13)</dt></span></span> </dl> | <span data-ttu-id="8f88d-334">SECAM G</span><span class="sxs-lookup"><span data-stu-id="8f88d-334">SECAM G</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="8f88d-335"><dt>20 (0x14)</dt></span><span class="sxs-lookup"><span data-stu-id="8f88d-335"><dt>20 (0x14)</dt></span></span> </dl> | <span data-ttu-id="8f88d-336">SECAM H</span><span class="sxs-lookup"><span data-stu-id="8f88d-336">SECAM H</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="8f88d-337"><dt>21 (0x15)</dt></span><span class="sxs-lookup"><span data-stu-id="8f88d-337"><dt>21 (0x15)</dt></span></span> </dl> | <span data-ttu-id="8f88d-338">SECAM K</span><span class="sxs-lookup"><span data-stu-id="8f88d-338">SECAM K</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="8f88d-339"><dt>22 (0x16)</dt></span><span class="sxs-lookup"><span data-stu-id="8f88d-339"><dt>22 (0x16)</dt></span></span> </dl> | <span data-ttu-id="8f88d-340">SECAM K1</span><span class="sxs-lookup"><span data-stu-id="8f88d-340">SECAM K1</span></span><br/>                                                                                            |
| <dl> <span data-ttu-id="8f88d-341"><dt>23 (0x17)</dt></span><span class="sxs-lookup"><span data-stu-id="8f88d-341"><dt>23 (0x17)</dt></span></span> </dl> | <span data-ttu-id="8f88d-342">SECAM L</span><span class="sxs-lookup"><span data-stu-id="8f88d-342">SECAM L</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="8f88d-343"><dt>24 (0x18)</dt></span><span class="sxs-lookup"><span data-stu-id="8f88d-343"><dt>24 (0x18)</dt></span></span> </dl> | <span data-ttu-id="8f88d-344">SECAM L1</span><span class="sxs-lookup"><span data-stu-id="8f88d-344">SECAM L1</span></span><br/>                                                                                            |
| <dl> <span data-ttu-id="8f88d-345"><dt>25 (0x19)</dt></span><span class="sxs-lookup"><span data-stu-id="8f88d-345"><dt>25 (0x19)</dt></span></span> </dl> | <span data-ttu-id="8f88d-346">EIA861</span><span class="sxs-lookup"><span data-stu-id="8f88d-346">EIA861</span></span><br/>                                                                                              |
| <dl> <span data-ttu-id="8f88d-347"><dt>26 (0x1A)</dt></span><span class="sxs-lookup"><span data-stu-id="8f88d-347"><dt>26 (0x1A)</dt></span></span> </dl> | <span data-ttu-id="8f88d-348">EIA861A</span><span class="sxs-lookup"><span data-stu-id="8f88d-348">EIA861A</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="8f88d-349"><dt>27 (0x1B)</dt></span><span class="sxs-lookup"><span data-stu-id="8f88d-349"><dt>27 (0x1B)</dt></span></span> </dl> | <span data-ttu-id="8f88d-350">EIA861B</span><span class="sxs-lookup"><span data-stu-id="8f88d-350">EIA861B</span></span><br/>                                                                                             |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8f88d-351">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8f88d-351">Requirements</span></span>



| <span data-ttu-id="8f88d-352">Requisito</span><span class="sxs-lookup"><span data-stu-id="8f88d-352">Requirement</span></span> | <span data-ttu-id="8f88d-353">Valore</span><span class="sxs-lookup"><span data-stu-id="8f88d-353">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8f88d-354">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8f88d-354">Minimum supported client</span></span><br/> | <span data-ttu-id="8f88d-355">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8f88d-355">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="8f88d-356">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8f88d-356">Minimum supported server</span></span><br/> | <span data-ttu-id="8f88d-357">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8f88d-357">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="8f88d-358">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="8f88d-358">Namespace</span></span><br/>                | <span data-ttu-id="8f88d-359">\\WMI radice</span><span class="sxs-lookup"><span data-stu-id="8f88d-359">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="8f88d-360">MOF</span><span class="sxs-lookup"><span data-stu-id="8f88d-360">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8f88d-361"><dt>WmiCore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8f88d-361"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="8f88d-362">DLL</span><span class="sxs-lookup"><span data-stu-id="8f88d-362">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8f88d-363"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8f88d-363"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f88d-364">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8f88d-364">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f88d-365">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="8f88d-365">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

 




