---
description: Rappresenta un contenitore per le caratteristiche di un intervallo di frequenze supportato.
ms.assetid: eb07c10b-8d92-40bb-8a93-ebc5db46cfd3
title: Classe FrequencyRangeDescriptor
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FrequencyRangeDescriptor
- FrequencyRangeDescriptor.Origin
- FrequencyRangeDescriptor.MinVSyncNumerator
- FrequencyRangeDescriptor.MinVSyncDenominator
- FrequencyRangeDescriptor.MaxVSyncNumerator
- FrequencyRangeDescriptor.MaxVSyncDenominator
- FrequencyRangeDescriptor.MinHSyncNumerator
- FrequencyRangeDescriptor.MinHSyncDenominator
- FrequencyRangeDescriptor.MaxHSyncNumerator
- FrequencyRangeDescriptor.MaxHSyncDenominator
- FrequencyRangeDescriptor.ConstraintType
- FrequencyRangeDescriptor.ActiveWidth
- FrequencyRangeDescriptor.ActiveHeight
- FrequencyRangeDescriptor.MaxPixelRate
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: d18bee8a69fd8663ea54973d6e4e8219f5f74e27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306875"
---
# <a name="frequencyrangedescriptor-class"></a><span data-ttu-id="31f69-103">Classe FrequencyRangeDescriptor</span><span class="sxs-lookup"><span data-stu-id="31f69-103">FrequencyRangeDescriptor class</span></span>

<span data-ttu-id="31f69-104">La classe WMI **FrequencyRangeDescriptor** rappresenta un contenitore per le caratteristiche di un intervallo di frequenze supportato.</span><span class="sxs-lookup"><span data-stu-id="31f69-104">The **FrequencyRangeDescriptor** WMI class represents a container for characteristics of a supported frequency range.</span></span> <span data-ttu-id="31f69-105">Le istanze di questa classe sono elementi della matrice **MonitorFreqRanges** in [**WmiMonitorListedFrequencyRanges**](wmimonitorlistedfrequencyranges.md).</span><span class="sxs-lookup"><span data-stu-id="31f69-105">Instances of this class are elements of the **MonitorFreqRanges** array in [**WmiMonitorListedFrequencyRanges**](wmimonitorlistedfrequencyranges.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="31f69-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="31f69-106">Syntax</span></span>

``` syntax
class FrequencyRangeDescriptor
{
  uint8  Origin;
  uint32 MinVSyncNumerator;
  uint32 MinVSyncDenominator;
  uint32 MaxVSyncNumerator;
  uint32 MaxVSyncDenominator;
  uint32 MinHSyncNumerator;
  uint32 MinHSyncDenominator;
  uint32 MaxHSyncNumerator;
  uint32 MaxHSyncDenominator;
  uint32 ConstraintType;
  uint32 ActiveWidth;
  uint32 ActiveHeight;
  uint32 MaxPixelRate;
};
```

## <a name="members"></a><span data-ttu-id="31f69-107">Members</span><span class="sxs-lookup"><span data-stu-id="31f69-107">Members</span></span>

<span data-ttu-id="31f69-108">La classe **FrequencyRangeDescriptor** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="31f69-108">The **FrequencyRangeDescriptor** class has these types of members:</span></span>

-   [<span data-ttu-id="31f69-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="31f69-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="31f69-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="31f69-110">Properties</span></span>

<span data-ttu-id="31f69-111">La classe **FrequencyRangeDescriptor** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="31f69-111">The **FrequencyRangeDescriptor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="31f69-112">**ActiveHeight**</span><span class="sxs-lookup"><span data-stu-id="31f69-112">**ActiveHeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31f69-113">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="31f69-113">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="31f69-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="31f69-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="31f69-115">Altezza, in pixel, dell'immagine attiva.</span><span class="sxs-lookup"><span data-stu-id="31f69-115">Height, in pixels, of the active image.</span></span>

</dd> <dt>

<span data-ttu-id="31f69-116">**ActiveWidth**</span><span class="sxs-lookup"><span data-stu-id="31f69-116">**ActiveWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31f69-117">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="31f69-117">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="31f69-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="31f69-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="31f69-119">Larghezza, in pixel, dell'immagine attiva.</span><span class="sxs-lookup"><span data-stu-id="31f69-119">Width, in pixels, of the active image.</span></span>

</dd> <dt>

<span data-ttu-id="31f69-120">**ConstraintType**</span><span class="sxs-lookup"><span data-stu-id="31f69-120">**ConstraintType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31f69-121">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="31f69-121">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="31f69-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="31f69-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="31f69-123">Tipo di vincolo per l'intervallo di frequenza.</span><span class="sxs-lookup"><span data-stu-id="31f69-123">Constraint type for the frequency range.</span></span>

</dd> <dt>

<span data-ttu-id="31f69-124">**MaxHSyncDenominator**</span><span class="sxs-lookup"><span data-stu-id="31f69-124">**MaxHSyncDenominator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31f69-125">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="31f69-125">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="31f69-126">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="31f69-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="31f69-127">Denominatore massimo di sincronizzazione orizzontale.</span><span class="sxs-lookup"><span data-stu-id="31f69-127">Maximum horizontal sync denominator.</span></span>

</dd> <dt>

<span data-ttu-id="31f69-128">**MaxHSyncNumerator**</span><span class="sxs-lookup"><span data-stu-id="31f69-128">**MaxHSyncNumerator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31f69-129">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="31f69-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="31f69-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="31f69-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="31f69-131">Numeratore di sincronizzazione orizzontale massimo in kilohertz (KHz).</span><span class="sxs-lookup"><span data-stu-id="31f69-131">Maximum horizontal sync numerator in kilohertz (KHz).</span></span>

</dd> <dt>

<span data-ttu-id="31f69-132">**MaxPixelRate**</span><span class="sxs-lookup"><span data-stu-id="31f69-132">**MaxPixelRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31f69-133">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="31f69-133">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="31f69-134">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="31f69-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="31f69-135">Frequenza massima in pixel in Hertz (Hz).</span><span class="sxs-lookup"><span data-stu-id="31f69-135">Maximum pixel rate in Hertz (Hz).</span></span>

</dd> <dt>

<span data-ttu-id="31f69-136">**MaxVSyncDenominator**</span><span class="sxs-lookup"><span data-stu-id="31f69-136">**MaxVSyncDenominator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31f69-137">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="31f69-137">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="31f69-138">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="31f69-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="31f69-139">Denominatore massimo di sincronizzazione verticale.</span><span class="sxs-lookup"><span data-stu-id="31f69-139">Maximum vertical sync denominator.</span></span>

</dd> <dt>

<span data-ttu-id="31f69-140">**MaxVSyncNumerator**</span><span class="sxs-lookup"><span data-stu-id="31f69-140">**MaxVSyncNumerator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31f69-141">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="31f69-141">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="31f69-142">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="31f69-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="31f69-143">Numeratore di sincronizzazione verticale massimo, in Hertz (Hz).</span><span class="sxs-lookup"><span data-stu-id="31f69-143">Maximum vertical sync numerator, in Hertz (Hz).</span></span>

</dd> <dt>

<span data-ttu-id="31f69-144">**MinHSyncDenominator**</span><span class="sxs-lookup"><span data-stu-id="31f69-144">**MinHSyncDenominator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31f69-145">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="31f69-145">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="31f69-146">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="31f69-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="31f69-147">Denominatore di sincronizzazione orizzontale minimo.</span><span class="sxs-lookup"><span data-stu-id="31f69-147">Minimum horizontal sync denominator.</span></span>

</dd> <dt>

<span data-ttu-id="31f69-148">**MinHSyncNumerator**</span><span class="sxs-lookup"><span data-stu-id="31f69-148">**MinHSyncNumerator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31f69-149">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="31f69-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="31f69-150">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="31f69-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="31f69-151">Numeratore di sincronizzazione orizzontale minimo in, kilohertz (KHz).</span><span class="sxs-lookup"><span data-stu-id="31f69-151">Minimum horizontal sync numerator in, kilohertz (KHz).</span></span>

</dd> <dt>

<span data-ttu-id="31f69-152">**MinVSyncDenominator**</span><span class="sxs-lookup"><span data-stu-id="31f69-152">**MinVSyncDenominator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31f69-153">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="31f69-153">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="31f69-154">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="31f69-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="31f69-155">Denominatore minimo di sincronizzazione verticale.</span><span class="sxs-lookup"><span data-stu-id="31f69-155">Minimum vertical sync denominator.</span></span>

</dd> <dt>

<span data-ttu-id="31f69-156">**MinVSyncNumerator**</span><span class="sxs-lookup"><span data-stu-id="31f69-156">**MinVSyncNumerator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31f69-157">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="31f69-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="31f69-158">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="31f69-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="31f69-159">Numeratore di sincronizzazione verticale minimo, in Hertz (Hz).</span><span class="sxs-lookup"><span data-stu-id="31f69-159">Minimum vertical sync numerator, in Hertz (Hz).</span></span>

</dd> <dt>

<span data-ttu-id="31f69-160">**Origine**</span><span class="sxs-lookup"><span data-stu-id="31f69-160">**Origin**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31f69-161">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="31f69-161">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="31f69-162">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="31f69-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="31f69-163">Origine.</span><span class="sxs-lookup"><span data-stu-id="31f69-163">Origin.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="31f69-164">Requisiti</span><span class="sxs-lookup"><span data-stu-id="31f69-164">Requirements</span></span>



| <span data-ttu-id="31f69-165">Requisito</span><span class="sxs-lookup"><span data-stu-id="31f69-165">Requirement</span></span> | <span data-ttu-id="31f69-166">Valore</span><span class="sxs-lookup"><span data-stu-id="31f69-166">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="31f69-167">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="31f69-167">Minimum supported client</span></span><br/> | <span data-ttu-id="31f69-168">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="31f69-168">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="31f69-169">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="31f69-169">Minimum supported server</span></span><br/> | <span data-ttu-id="31f69-170">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="31f69-170">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="31f69-171">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="31f69-171">Namespace</span></span><br/>                | <span data-ttu-id="31f69-172">\\WMI radice</span><span class="sxs-lookup"><span data-stu-id="31f69-172">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="31f69-173">MOF</span><span class="sxs-lookup"><span data-stu-id="31f69-173">MOF</span></span><br/>                      | <dl> <span data-ttu-id="31f69-174"><dt>WmiCore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="31f69-174"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="31f69-175">DLL</span><span class="sxs-lookup"><span data-stu-id="31f69-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="31f69-176"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="31f69-176"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31f69-177">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="31f69-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31f69-178">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="31f69-178">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

 




