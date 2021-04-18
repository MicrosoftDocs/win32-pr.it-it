---
description: Rappresenta le funzionalità di visualizzazione supportate del monitoraggio.
ms.assetid: 28eeead3-8fb9-4720-8d93-1c6757dfb31b
title: Classe SupportedDisplayFeaturesDescriptor
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SupportedDisplayFeaturesDescriptor
- SupportedDisplayFeaturesDescriptor.ActiveOffSupported
- SupportedDisplayFeaturesDescriptor.DisplayType
- SupportedDisplayFeaturesDescriptor.GTFSupported
- SupportedDisplayFeaturesDescriptor.HasPreferredTimingMode
- SupportedDisplayFeaturesDescriptor.sRGBSupported
- SupportedDisplayFeaturesDescriptor.StandbySupported
- SupportedDisplayFeaturesDescriptor.SuspendSupported
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 30350d477533b7e51ba8b3130c5a24d81c12f10e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308855"
---
# <a name="supporteddisplayfeaturesdescriptor-class"></a><span data-ttu-id="6c2ea-103">Classe SupportedDisplayFeaturesDescriptor</span><span class="sxs-lookup"><span data-stu-id="6c2ea-103">SupportedDisplayFeaturesDescriptor class</span></span>

<span data-ttu-id="6c2ea-104">**SupportedDisplayFeaturesDescriptor** rappresenta le funzionalità di visualizzazione supportate del monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="6c2ea-104">The **SupportedDisplayFeaturesDescriptor** represents the supported display features of the monitor.</span></span> <span data-ttu-id="6c2ea-105">Le informazioni contenute in questa classe corrispondono ai dati nella definizione di input video dello standard EDID (video Electronics Standard Association) Enhanced Extended Display Data (VESA).</span><span class="sxs-lookup"><span data-stu-id="6c2ea-105">The information in this class corresponds to data in the Video Input Definition of the Video Electronics Standard Association (VESA) Enhanced Extended Display Identification Data (E-EDID) standard.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c2ea-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6c2ea-106">Syntax</span></span>

``` syntax
class SupportedDisplayFeaturesDescriptor
{
  boolean ActiveOffSupported;
  uint8   DisplayType;
  boolean GTFSupported;
  boolean HasPreferredTimingMode;
  boolean sRGBSupported;
  boolean StandbySupported;
  boolean SuspendSupported;
};
```

## <a name="members"></a><span data-ttu-id="6c2ea-107">Members</span><span class="sxs-lookup"><span data-stu-id="6c2ea-107">Members</span></span>

<span data-ttu-id="6c2ea-108">La classe **SupportedDisplayFeaturesDescriptor** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="6c2ea-108">The **SupportedDisplayFeaturesDescriptor** class has these types of members:</span></span>

-   [<span data-ttu-id="6c2ea-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="6c2ea-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6c2ea-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="6c2ea-110">Properties</span></span>

<span data-ttu-id="6c2ea-111">La classe **SupportedDisplayFeaturesDescriptor** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="6c2ea-111">The **SupportedDisplayFeaturesDescriptor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6c2ea-112">**ActiveOffSupported**</span><span class="sxs-lookup"><span data-stu-id="6c2ea-112">**ActiveOffSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c2ea-113">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="6c2ea-113">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6c2ea-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6c2ea-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6c2ea-115">Supporto per il risparmio di energia attivo e molto basso.</span><span class="sxs-lookup"><span data-stu-id="6c2ea-115">Support for active off and very low power.</span></span> <span data-ttu-id="6c2ea-116">La visualizzazione consuma meno energia quando riceve un segnale temporale che non rientra nell'intervallo operativo attivo dichiarato.</span><span class="sxs-lookup"><span data-stu-id="6c2ea-116">The display consumes less power when it receives a timing signal that is outside the declared active operating range.</span></span> <span data-ttu-id="6c2ea-117">Se il segnale di temporizzazione torna al normale intervallo operativo, verrà ripristinata l'operazione normale.</span><span class="sxs-lookup"><span data-stu-id="6c2ea-117">The display will revert to normal operation if the timing signal returns to the normal operating range.</span></span> <span data-ttu-id="6c2ea-118">Esempi di segnali di temporizzazione al di fuori dell'intervallo operativo normale non sono segnali di sincronizzazione o nessun segnale.</span><span class="sxs-lookup"><span data-stu-id="6c2ea-118">Examples of timing signals outside the normal operating range are no sync signals or no DE signal.</span></span>

</dd> <dt>

<span data-ttu-id="6c2ea-119">**DisplayType**</span><span class="sxs-lookup"><span data-stu-id="6c2ea-119">**DisplayType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c2ea-120">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="6c2ea-120">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="6c2ea-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6c2ea-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6c2ea-122">Tipo di visualizzazione per il monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="6c2ea-122">Type of display for the monitor.</span></span> <span data-ttu-id="6c2ea-123">Nella tabella seguente sono elencati i valori possibili.</span><span class="sxs-lookup"><span data-stu-id="6c2ea-123">The following table lists possible values.</span></span>



| <span data-ttu-id="6c2ea-124">Valore</span><span class="sxs-lookup"><span data-stu-id="6c2ea-124">Value</span></span>                                                                              | <span data-ttu-id="6c2ea-125">Significato</span><span class="sxs-lookup"><span data-stu-id="6c2ea-125">Meaning</span></span>                                 |
|------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="6c2ea-126"><dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="6c2ea-126"><dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="6c2ea-127">Visualizzazione monocromatico/scala di grigi</span><span class="sxs-lookup"><span data-stu-id="6c2ea-127">Monochrome/grayscale display</span></span><br/> |
| <dl> <span data-ttu-id="6c2ea-128"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="6c2ea-128"><dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="6c2ea-129">Visualizzazione colori RGB</span><span class="sxs-lookup"><span data-stu-id="6c2ea-129">RGB color display</span></span><br/>            |
| <dl> <span data-ttu-id="6c2ea-130"><dt>2 (0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="6c2ea-130"><dt>2 (0x2)</dt></span></span> </dl> | <span data-ttu-id="6c2ea-131">Visualizzazione multicolore non RGB</span><span class="sxs-lookup"><span data-stu-id="6c2ea-131">Non-RGB multicolor display</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="6c2ea-132">**GTFSupported**</span><span class="sxs-lookup"><span data-stu-id="6c2ea-132">**GTFSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c2ea-133">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="6c2ea-133">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6c2ea-134">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6c2ea-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6c2ea-135">Indica se la visualizzazione dispone del supporto GTF.</span><span class="sxs-lookup"><span data-stu-id="6c2ea-135">Indicates whether the display has GTF support.</span></span> <span data-ttu-id="6c2ea-136">Se **true**, la visualizzazione supporta le tempistiche basate sullo standard GTF usando i valori predefiniti del parametro GTF.</span><span class="sxs-lookup"><span data-stu-id="6c2ea-136">If **True**, the display supports timings based on the GTF standard using default GTF parameter values.</span></span>

</dd> <dt>

<span data-ttu-id="6c2ea-137">**HasPreferredTimingMode**</span><span class="sxs-lookup"><span data-stu-id="6c2ea-137">**HasPreferredTimingMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c2ea-138">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="6c2ea-138">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6c2ea-139">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6c2ea-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6c2ea-140">Indica se la visualizzazione ha una modalità temporizzata preferita.</span><span class="sxs-lookup"><span data-stu-id="6c2ea-140">Indicates whether the display has has a preferred timing mode.</span></span> <span data-ttu-id="6c2ea-141">Se **true**, il primo blocco di intervallo dettagliato contiene la modalità di temporizzazione preferita del monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="6c2ea-141">If **True**, the first detailed timing block contains the preferred timing mode of the monitor.</span></span> <span data-ttu-id="6c2ea-142">L'uso della modalità di temporizzazione preferita è richiesto da EDID v. 1.3 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="6c2ea-142">Use of preferred timing mode is required by EDID v.1.3 and higher.</span></span>

</dd> <dt>

<span data-ttu-id="6c2ea-143">**sRGBSupported**</span><span class="sxs-lookup"><span data-stu-id="6c2ea-143">**sRGBSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c2ea-144">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="6c2ea-144">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6c2ea-145">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6c2ea-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6c2ea-146">Se **true**, la visualizzazione supporta sRGB.</span><span class="sxs-lookup"><span data-stu-id="6c2ea-146">If **True**, the display supports sRGB.</span></span>

</dd> <dt>

<span data-ttu-id="6c2ea-147">**StandbySupported**</span><span class="sxs-lookup"><span data-stu-id="6c2ea-147">**StandbySupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c2ea-148">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="6c2ea-148">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6c2ea-149">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6c2ea-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6c2ea-150">Indica se la visualizzazione supporta la modalità standby per la segnalazione di risparmio energia DPMS (VESA).</span><span class="sxs-lookup"><span data-stu-id="6c2ea-150">Indicates whether the display supports VESA Display Power Management Signaling (DPMS) standby.</span></span> <span data-ttu-id="6c2ea-151">Se è **true**, DPMS standby è supportato.</span><span class="sxs-lookup"><span data-stu-id="6c2ea-151">If **True**, DPMS standby is supported.</span></span>

</dd> <dt>

<span data-ttu-id="6c2ea-152">**SuspendSupported**</span><span class="sxs-lookup"><span data-stu-id="6c2ea-152">**SuspendSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c2ea-153">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="6c2ea-153">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6c2ea-154">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6c2ea-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6c2ea-155">Indica se la visualizzazione supporta la sospensione di DPMS (Display Power Management Signaling).</span><span class="sxs-lookup"><span data-stu-id="6c2ea-155">Indicates whether the display supports VESA Display Power Management Signaling (DPMS) suspend.</span></span> <span data-ttu-id="6c2ea-156">Se è **true**, DPMS Suspend è supportato.</span><span class="sxs-lookup"><span data-stu-id="6c2ea-156">If **True**, DPMS suspend is supported.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6c2ea-157">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6c2ea-157">Requirements</span></span>



| <span data-ttu-id="6c2ea-158">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c2ea-158">Requirement</span></span> | <span data-ttu-id="6c2ea-159">Valore</span><span class="sxs-lookup"><span data-stu-id="6c2ea-159">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6c2ea-160">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6c2ea-160">Minimum supported client</span></span><br/> | <span data-ttu-id="6c2ea-161">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6c2ea-161">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="6c2ea-162">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6c2ea-162">Minimum supported server</span></span><br/> | <span data-ttu-id="6c2ea-163">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6c2ea-163">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="6c2ea-164">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="6c2ea-164">Namespace</span></span><br/>                | <span data-ttu-id="6c2ea-165">\\WMI radice</span><span class="sxs-lookup"><span data-stu-id="6c2ea-165">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="6c2ea-166">MOF</span><span class="sxs-lookup"><span data-stu-id="6c2ea-166">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6c2ea-167"><dt>WmiCore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6c2ea-167"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="6c2ea-168">DLL</span><span class="sxs-lookup"><span data-stu-id="6c2ea-168">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6c2ea-169"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6c2ea-169"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c2ea-170">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6c2ea-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c2ea-171">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="6c2ea-171">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

 




