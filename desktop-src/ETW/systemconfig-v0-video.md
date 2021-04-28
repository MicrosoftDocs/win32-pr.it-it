---
description: 'SystemConfig_V0_Video: questa classe è la classe del tipo di evento per gli eventi di configurazione video.'
ms.assetid: 06aab3a3-a55e-4eb8-897a-2ad8349e5900
title: SystemConfig_V0_Video classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_V0_Video
- SystemConfig_V0_Video.MemorySize
- SystemConfig_V0_Video.XResolution
- SystemConfig_V0_Video.YResolution
- SystemConfig_V0_Video.BitsPerPixel
- SystemConfig_V0_Video.VRefresh
- SystemConfig_V0_Video.ChipType
- SystemConfig_V0_Video.DACType
- SystemConfig_V0_Video.AdapterString
- SystemConfig_V0_Video.BiosString
- SystemConfig_V0_Video.DeviceId
- SystemConfig_V0_Video.StateFlags
api_type:
- NA
api_location: ''
ms.openlocfilehash: 94fb9e50344cfbdde4be67815b80e4074ab1a878
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105919"
---
# <a name="systemconfig_v0_video-class"></a><span data-ttu-id="3412f-103">Classe SystemConfig \_ V0 \_ Video</span><span class="sxs-lookup"><span data-stu-id="3412f-103">SystemConfig\_V0\_Video class</span></span>

<span data-ttu-id="3412f-104">Questa classe è la classe del tipo di evento per gli eventi di configurazione video.</span><span class="sxs-lookup"><span data-stu-id="3412f-104">This class is the event type class for video configuration events.</span></span>

<span data-ttu-id="3412f-105">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="3412f-105">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="3412f-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3412f-106">Syntax</span></span>

``` syntax
[EventType(14), EventTypeName("Video")]
class SystemConfig_V0_Video : SystemConfig_V0
{
  uint32 MemorySize;
  uint32 XResolution;
  uint32 YResolution;
  uint32 BitsPerPixel;
  uint32 VRefresh;
  char16 ChipType[];
  char16 DACType[];
  char16 AdapterString[];
  char16 BiosString[];
  char16 DeviceId[];
  uint32 StateFlags;
};
```

## <a name="members"></a><span data-ttu-id="3412f-107">Members</span><span class="sxs-lookup"><span data-stu-id="3412f-107">Members</span></span>

<span data-ttu-id="3412f-108">La **classe SystemConfig \_ V0 \_ Video** include questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="3412f-108">The **SystemConfig\_V0\_Video** class has these types of members:</span></span>

-   [<span data-ttu-id="3412f-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3412f-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3412f-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3412f-110">Properties</span></span>

<span data-ttu-id="3412f-111">La **classe SystemConfig \_ V0 \_ Video** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="3412f-111">The **SystemConfig\_V0\_Video** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3412f-112">**AdapterString**</span><span class="sxs-lookup"><span data-stu-id="3412f-112">**AdapterString**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3412f-113">Tipo di dati: **matrice char16**</span><span class="sxs-lookup"><span data-stu-id="3412f-113">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="3412f-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3412f-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3412f-115">Qualificatori: **WmiDataId** (8), **Max** (256)</span><span class="sxs-lookup"><span data-stu-id="3412f-115">Qualifiers: **WmiDataId** (8), **Max** (256)</span></span>
</dt> </dl>

<span data-ttu-id="3412f-116">Nome o descrizione dell'adattatore.</span><span class="sxs-lookup"><span data-stu-id="3412f-116">Name or description of the adapter.</span></span>

</dd> <dt>

<span data-ttu-id="3412f-117">**BiosString**</span><span class="sxs-lookup"><span data-stu-id="3412f-117">**BiosString**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3412f-118">Tipo di dati: **matrice char16**</span><span class="sxs-lookup"><span data-stu-id="3412f-118">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="3412f-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3412f-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3412f-120">Qualificatori: **WmiDataId** (9), **Max** (256)</span><span class="sxs-lookup"><span data-stu-id="3412f-120">Qualifiers: **WmiDataId** (9), **Max** (256)</span></span>
</dt> </dl>

<span data-ttu-id="3412f-121">Nome BIOS della scheda.</span><span class="sxs-lookup"><span data-stu-id="3412f-121">BIOS name of the adapter.</span></span>

</dd> <dt>

<span data-ttu-id="3412f-122">**BitsPerPixel**</span><span class="sxs-lookup"><span data-stu-id="3412f-122">**BitsPerPixel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3412f-123">Tipo di dati: **uint32**</span><span class="sxs-lookup"><span data-stu-id="3412f-123">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3412f-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3412f-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3412f-125">Qualificatori: **WmiDataId** (4)</span><span class="sxs-lookup"><span data-stu-id="3412f-125">Qualifiers: **WmiDataId** (4)</span></span>
</dt> </dl>

<span data-ttu-id="3412f-126">Numero di bit utilizzati per visualizzare ogni pixel.</span><span class="sxs-lookup"><span data-stu-id="3412f-126">Number of bits used to display each pixel.</span></span>

</dd> <dt>

<span data-ttu-id="3412f-127">**ChipType**</span><span class="sxs-lookup"><span data-stu-id="3412f-127">**ChipType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3412f-128">Tipo di dati: **matrice char16**</span><span class="sxs-lookup"><span data-stu-id="3412f-128">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="3412f-129">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3412f-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3412f-130">Qualificatori: **WmiDataId** (6), **Max** (256)</span><span class="sxs-lookup"><span data-stu-id="3412f-130">Qualifiers: **WmiDataId** (6), **Max** (256)</span></span>
</dt> </dl>

<span data-ttu-id="3412f-131">Nome del chip dell'adapter.</span><span class="sxs-lookup"><span data-stu-id="3412f-131">Chip name of the adapter.</span></span>

</dd> <dt>

<span data-ttu-id="3412f-132">**Dactype**</span><span class="sxs-lookup"><span data-stu-id="3412f-132">**DACType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3412f-133">Tipo di dati: **matrice char16**</span><span class="sxs-lookup"><span data-stu-id="3412f-133">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="3412f-134">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3412f-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3412f-135">Qualificatori: **WmiDataId** (7), **Max** (256)</span><span class="sxs-lookup"><span data-stu-id="3412f-135">Qualifiers: **WmiDataId** (7), **Max** (256)</span></span>
</dt> </dl>

<span data-ttu-id="3412f-136">Nome del chip del convertitore da digitale ad analogico (DAC) dell'adapter.</span><span class="sxs-lookup"><span data-stu-id="3412f-136">Digital-to-analog converter (DAC) chip name of the adapter.</span></span>

</dd> <dt>

<span data-ttu-id="3412f-137">**Deviceid**</span><span class="sxs-lookup"><span data-stu-id="3412f-137">**DeviceId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3412f-138">Tipo di dati: **matrice char16**</span><span class="sxs-lookup"><span data-stu-id="3412f-138">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="3412f-139">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3412f-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3412f-140">Qualificatori: **WmiDataId** (10), **Max** (256)</span><span class="sxs-lookup"><span data-stu-id="3412f-140">Qualifiers: **WmiDataId** (10), **Max** (256)</span></span>
</dt> </dl>

<span data-ttu-id="3412f-141">Indirizzo o altre informazioni di identificazione per assegnare un nome univoco al dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="3412f-141">Address or other identifying information to uniquely name the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="3412f-142">**MemorySize**</span><span class="sxs-lookup"><span data-stu-id="3412f-142">**MemorySize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3412f-143">Tipo di dati: **uint32**</span><span class="sxs-lookup"><span data-stu-id="3412f-143">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3412f-144">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3412f-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3412f-145">Qualificatori: **WmiDataId** (1)</span><span class="sxs-lookup"><span data-stu-id="3412f-145">Qualifiers: **WmiDataId** (1)</span></span>
</dt> </dl>

<span data-ttu-id="3412f-146">Quantità massima di memoria supportata, in byte.</span><span class="sxs-lookup"><span data-stu-id="3412f-146">Maximum amount of memory supported, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="3412f-147">**StateFlags**</span><span class="sxs-lookup"><span data-stu-id="3412f-147">**StateFlags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3412f-148">Tipo di dati: **uint32**</span><span class="sxs-lookup"><span data-stu-id="3412f-148">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3412f-149">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3412f-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3412f-150">Qualificatori: **WmiDataId** (11)</span><span class="sxs-lookup"><span data-stu-id="3412f-150">Qualifiers: **WmiDataId** (11)</span></span>
</dt> </dl>

<span data-ttu-id="3412f-151">Flag di stato del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3412f-151">Device state flags.</span></span> <span data-ttu-id="3412f-152">Può essere qualsiasi combinazione ragionevole di quanto segue.</span><span class="sxs-lookup"><span data-stu-id="3412f-152">It can be any reasonable combination of the following.</span></span>



| <span data-ttu-id="3412f-153">Valore</span><span class="sxs-lookup"><span data-stu-id="3412f-153">Value</span></span>                                                                                                                                                                                                                                                                                        | <span data-ttu-id="3412f-154">Significato</span><span class="sxs-lookup"><span data-stu-id="3412f-154">Meaning</span></span>                                                                                                                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DISPLAY_DEVICE_ATTACHED_TO_DESKTOP"></span><span id="display_device_attached_to_desktop"></span><dl> <span data-ttu-id="3412f-155"><dt>**VISUALIZZAZIONE \_ DISPOSITIVO \_ COLLEGATO \_ AL \_ DESKTOP**</dt> <dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="3412f-155"><dt>**DISPLAY\_DEVICE\_ATTACHED\_TO\_DESKTOP**</dt> <dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="3412f-156">Il dispositivo fa parte del desktop.</span><span class="sxs-lookup"><span data-stu-id="3412f-156">The device is part of the desktop.</span></span><br/>                                                                                                                                                                                |
| <span id="DISPLAY_DEVICE_MIRRORING_DRIVER"></span><span id="display_device_mirroring_driver"></span><dl> <span data-ttu-id="3412f-157"><dt>**VISUALIZZAZIONE \_ \_DRIVER MIRRORING DEL \_ DISPOSITIVO**</dt> <dt>8 (0x8)</dt></span><span class="sxs-lookup"><span data-stu-id="3412f-157"><dt>**DISPLAY\_DEVICE\_MIRRORING\_DRIVER**</dt> <dt>8 (0x8)</dt></span></span> </dl>           | <span data-ttu-id="3412f-158">Rappresenta una pseudo-periferica utilizzata per eseguire il mirroring del disegno dell'applicazione per la connessione a un computer remoto o ad altri scopi.</span><span class="sxs-lookup"><span data-stu-id="3412f-158">Represents a pseudo device used to mirror application drawing for connecting to a remote computer or other purposes.</span></span> <span data-ttu-id="3412f-159">A questo dispositivo è associato uno pseudo monitor invisibile.</span><span class="sxs-lookup"><span data-stu-id="3412f-159">An invisible pseudo monitor is associated with this device.</span></span> <span data-ttu-id="3412f-160">Ad esempio, Viene utilizzato da NetMeeting.</span><span class="sxs-lookup"><span data-stu-id="3412f-160">For example, NetMeeting uses it.</span></span><br/> |
| <span id="DISPLAY_DEVICE_MODESPRUNED"></span><span id="display_device_modespruned"></span><dl> <span data-ttu-id="3412f-161"><dt>**VISUALIZZAZIONE \_ DEVICE \_ MODESPRUNED**</dt> <dt>134217728 (0x8000000)</dt></span><span class="sxs-lookup"><span data-stu-id="3412f-161"><dt>**DISPLAY\_DEVICE\_MODESPRUNED**</dt> <dt>134217728 (0x8000000)</dt></span></span> </dl>             | <span data-ttu-id="3412f-162">Il dispositivo ha più modalità di visualizzazione di quelle supportate dai dispositivi di output.</span><span class="sxs-lookup"><span data-stu-id="3412f-162">The device has more display modes than its output devices support.</span></span><br/>                                                                                                                                                |
| <span id="DISPLAY_DEVICE_PRIMARY_DEVICE"></span><span id="display_device_primary_device"></span><dl> <span data-ttu-id="3412f-163"><dt>**VISUALIZZAZIONE \_ DISPOSITIVO \_ PRIMARIO \_ DISPOSITIVO**</dt> <dt>4 (0x4)</dt></span><span class="sxs-lookup"><span data-stu-id="3412f-163"><dt>**DISPLAY\_DEVICE\_PRIMARY\_DEVICE**</dt> <dt>4 (0x4)</dt></span></span> </dl>                 | <span data-ttu-id="3412f-164">Il desktop primario si trova nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3412f-164">The primary desktop is on the device.</span></span> <span data-ttu-id="3412f-165">Per un sistema con una singola scheda video, questa opzione è sempre impostata.</span><span class="sxs-lookup"><span data-stu-id="3412f-165">For a system with a single display card, this is always set.</span></span> <span data-ttu-id="3412f-166">Per un sistema con più schede video, questo set può essere impostato su un solo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3412f-166">For a system with multiple display cards, only one device can have this set.</span></span><br/>                                   |
| <span id="DISPLAY_DEVICE_REMOVABLE"></span><span id="display_device_removable"></span><dl> <span data-ttu-id="3412f-167"><dt>**VISUALIZZAZIONE \_ DISPOSITIVO \_ RIMOVIBILE**</dt> <dt>32 (0x20)</dt></span><span class="sxs-lookup"><span data-stu-id="3412f-167"><dt>**DISPLAY\_DEVICE\_REMOVABLE**</dt> <dt>32 (0x20)</dt></span></span> </dl>                               | <span data-ttu-id="3412f-168">Il dispositivo è rimovibile. non può essere la visualizzazione principale.</span><span class="sxs-lookup"><span data-stu-id="3412f-168">The device is removable; it cannot be the primary display.</span></span><br/>                                                                                                                                                        |
| <span id="DISPLAY_DEVICE_VGA_COMPATIBLE"></span><span id="display_device_vga_compatible"></span><dl> <span data-ttu-id="3412f-169"><dt>**VISUALIZZAZIONE \_ DISPOSITIVO \_ COMPATIBILE \_ VGA**</dt> <dt>16 (0x10)</dt></span><span class="sxs-lookup"><span data-stu-id="3412f-169"><dt>**DISPLAY\_DEVICE\_VGA\_COMPATIBLE**</dt> <dt>16 (0x10)</dt></span></span> </dl>               | <span data-ttu-id="3412f-170">Il dispositivo è compatibile con VGA.</span><span class="sxs-lookup"><span data-stu-id="3412f-170">The device is VGA compatible.</span></span><br/>                                                                                                                                                                                     |



 

</dd> <dt>

<span data-ttu-id="3412f-171">**VRefresh**</span><span class="sxs-lookup"><span data-stu-id="3412f-171">**VRefresh**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3412f-172">Tipo di dati: **uint32**</span><span class="sxs-lookup"><span data-stu-id="3412f-172">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3412f-173">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3412f-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3412f-174">Qualificatori: **WmiDataId** (5)</span><span class="sxs-lookup"><span data-stu-id="3412f-174">Qualifiers: **WmiDataId** (5)</span></span>
</dt> </dl>

<span data-ttu-id="3412f-175">Frequenza di aggiornamento corrente, in hertz.</span><span class="sxs-lookup"><span data-stu-id="3412f-175">Current refresh rate, in hertz.</span></span>

</dd> <dt>

<span data-ttu-id="3412f-176">**XResolution**</span><span class="sxs-lookup"><span data-stu-id="3412f-176">**XResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3412f-177">Tipo di dati: **uint32**</span><span class="sxs-lookup"><span data-stu-id="3412f-177">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3412f-178">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3412f-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3412f-179">Qualificatori: **WmiDataId** (2)</span><span class="sxs-lookup"><span data-stu-id="3412f-179">Qualifiers: **WmiDataId** (2)</span></span>
</dt> </dl>

<span data-ttu-id="3412f-180">Numero corrente di pixel orizzontali.</span><span class="sxs-lookup"><span data-stu-id="3412f-180">Current number of horizontal pixels.</span></span>

</dd> <dt>

<span data-ttu-id="3412f-181">**YResolution**</span><span class="sxs-lookup"><span data-stu-id="3412f-181">**YResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3412f-182">Tipo di dati: **uint32**</span><span class="sxs-lookup"><span data-stu-id="3412f-182">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3412f-183">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3412f-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3412f-184">Qualificatori: **WmiDataId** (3)</span><span class="sxs-lookup"><span data-stu-id="3412f-184">Qualifiers: **WmiDataId** (3)</span></span>
</dt> </dl>

<span data-ttu-id="3412f-185">Numero corrente di pixel verticali.</span><span class="sxs-lookup"><span data-stu-id="3412f-185">Current number of vertical pixels.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3412f-186">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3412f-186">Requirements</span></span>



| <span data-ttu-id="3412f-187">Requisito</span><span class="sxs-lookup"><span data-stu-id="3412f-187">Requirement</span></span> | <span data-ttu-id="3412f-188">Valore</span><span class="sxs-lookup"><span data-stu-id="3412f-188">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3412f-189">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3412f-189">Minimum supported client</span></span><br/> | <span data-ttu-id="3412f-190">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="3412f-190">None supported</span></span><br/>                            |
| <span data-ttu-id="3412f-191">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3412f-191">Minimum supported server</span></span><br/> | <span data-ttu-id="3412f-192">Solo app desktop di Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="3412f-192">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3412f-193">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3412f-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3412f-194">**SystemConfig \_ V0**</span><span class="sxs-lookup"><span data-stu-id="3412f-194">**SystemConfig\_V0**</span></span>](systemconfig-v0.md)
</dt> </dl>

 

 




