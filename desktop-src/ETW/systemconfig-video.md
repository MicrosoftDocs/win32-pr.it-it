---
description: 'SystemConfig_Video classe: questa classe è la classe del tipo di evento per gli eventi di configurazione video.'
ms.assetid: ddb5924b-70d9-4693-bf68-0536c3c3fa8d
title: SystemConfig_Video classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_Video
- SystemConfig_Video.MemorySize
- SystemConfig_Video.XResolution
- SystemConfig_Video.YResolution
- SystemConfig_Video.BitsPerPixel
- SystemConfig_Video.VRefresh
- SystemConfig_Video.ChipType
- SystemConfig_Video.DACType
- SystemConfig_Video.AdapterString
- SystemConfig_Video.BiosString
- SystemConfig_Video.DeviceId
- SystemConfig_Video.StateFlags
api_type:
- NA
api_location: ''
ms.openlocfilehash: 716194eb9ceb67b609f886482393795eaef2ef09
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105899"
---
# <a name="systemconfig_video-class"></a><span data-ttu-id="96f68-103">Classe Video \_ SystemConfig</span><span class="sxs-lookup"><span data-stu-id="96f68-103">SystemConfig\_Video class</span></span>

<span data-ttu-id="96f68-104">Questa classe è la classe del tipo di evento per gli eventi di configurazione video.</span><span class="sxs-lookup"><span data-stu-id="96f68-104">This class is the event type class for video configuration events.</span></span>

<span data-ttu-id="96f68-105">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="96f68-105">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="96f68-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="96f68-106">Syntax</span></span>

``` syntax
[EventType(14), EventTypeName("Video")]
class SystemConfig_Video : SystemConfig
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

## <a name="members"></a><span data-ttu-id="96f68-107">Members</span><span class="sxs-lookup"><span data-stu-id="96f68-107">Members</span></span>

<span data-ttu-id="96f68-108">La **classe SystemConfig \_ Video** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="96f68-108">The **SystemConfig\_Video** class has these types of members:</span></span>

-   [<span data-ttu-id="96f68-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="96f68-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="96f68-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="96f68-110">Properties</span></span>

<span data-ttu-id="96f68-111">La **classe SystemConfig \_ Video** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="96f68-111">The **SystemConfig\_Video** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="96f68-112">**AdapterString**</span><span class="sxs-lookup"><span data-stu-id="96f68-112">**AdapterString**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="96f68-113">Tipo di dati: **matrice char16**</span><span class="sxs-lookup"><span data-stu-id="96f68-113">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="96f68-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="96f68-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="96f68-115">Qualificatori: **WmiDataId** (8), **Max** (256), **Format("s")**</span><span class="sxs-lookup"><span data-stu-id="96f68-115">Qualifiers: **WmiDataId** (8), **Max** (256), **Format("s")**</span></span>
</dt> </dl>

<span data-ttu-id="96f68-116">Nome o descrizione dell'adapter.</span><span class="sxs-lookup"><span data-stu-id="96f68-116">Name or description of the adapter.</span></span>

</dd> <dt>

<span data-ttu-id="96f68-117">**BiosString**</span><span class="sxs-lookup"><span data-stu-id="96f68-117">**BiosString**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="96f68-118">Tipo di dati: **matrice char16**</span><span class="sxs-lookup"><span data-stu-id="96f68-118">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="96f68-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="96f68-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="96f68-120">Qualificatori: **WmiDataId** (9), **Max** (256), **Format("s")**</span><span class="sxs-lookup"><span data-stu-id="96f68-120">Qualifiers: **WmiDataId** (9), **Max** (256), **Format("s")**</span></span>
</dt> </dl>

<span data-ttu-id="96f68-121">Nome BIOS della scheda.</span><span class="sxs-lookup"><span data-stu-id="96f68-121">BIOS name of the adapter.</span></span>

</dd> <dt>

<span data-ttu-id="96f68-122">**BitsPerPixel**</span><span class="sxs-lookup"><span data-stu-id="96f68-122">**BitsPerPixel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="96f68-123">Tipo di dati: **uint32**</span><span class="sxs-lookup"><span data-stu-id="96f68-123">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="96f68-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="96f68-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="96f68-125">Qualificatori: **WmiDataId** (4)</span><span class="sxs-lookup"><span data-stu-id="96f68-125">Qualifiers: **WmiDataId** (4)</span></span>
</dt> </dl>

<span data-ttu-id="96f68-126">Numero di bit usati per visualizzare ogni pixel.</span><span class="sxs-lookup"><span data-stu-id="96f68-126">Number of bits used to display each pixel.</span></span>

</dd> <dt>

<span data-ttu-id="96f68-127">**ChipType**</span><span class="sxs-lookup"><span data-stu-id="96f68-127">**ChipType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="96f68-128">Tipo di dati: **matrice char16**</span><span class="sxs-lookup"><span data-stu-id="96f68-128">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="96f68-129">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="96f68-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="96f68-130">Qualificatori: **WmiDataId** (6), **Max** (256), **Format("s")**</span><span class="sxs-lookup"><span data-stu-id="96f68-130">Qualifiers: **WmiDataId** (6), **Max** (256), **Format("s")**</span></span>
</dt> </dl>

<span data-ttu-id="96f68-131">Nome del chip dell'adattatore.</span><span class="sxs-lookup"><span data-stu-id="96f68-131">Chip name of the adapter.</span></span>

</dd> <dt>

<span data-ttu-id="96f68-132">**Dactype**</span><span class="sxs-lookup"><span data-stu-id="96f68-132">**DACType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="96f68-133">Tipo di dati: **matrice char16**</span><span class="sxs-lookup"><span data-stu-id="96f68-133">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="96f68-134">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="96f68-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="96f68-135">Qualificatori: **WmiDataId** (7), **Max** (256), **Format("s")**</span><span class="sxs-lookup"><span data-stu-id="96f68-135">Qualifiers: **WmiDataId** (7), **Max** (256), **Format("s")**</span></span>
</dt> </dl>

<span data-ttu-id="96f68-136">Nome del chip daC (Digital-to-Analog Converter) dell'adattatore.</span><span class="sxs-lookup"><span data-stu-id="96f68-136">Digital-to-analog converter (DAC) chip name of the adapter.</span></span>

</dd> <dt>

<span data-ttu-id="96f68-137">**Deviceid**</span><span class="sxs-lookup"><span data-stu-id="96f68-137">**DeviceId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="96f68-138">Tipo di dati: **matrice char16**</span><span class="sxs-lookup"><span data-stu-id="96f68-138">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="96f68-139">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="96f68-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="96f68-140">Qualificatori: **WmiDataId** (10), **Max** (256), **Format("s")**</span><span class="sxs-lookup"><span data-stu-id="96f68-140">Qualifiers: **WmiDataId** (10), **Max** (256), **Format("s")**</span></span>
</dt> </dl>

<span data-ttu-id="96f68-141">Indirizzo o altre informazioni di identificazione per assegnare un nome univoco al dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="96f68-141">Address or other identifying information to uniquely name the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="96f68-142">**MemorySize**</span><span class="sxs-lookup"><span data-stu-id="96f68-142">**MemorySize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="96f68-143">Tipo di dati: **uint32**</span><span class="sxs-lookup"><span data-stu-id="96f68-143">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="96f68-144">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="96f68-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="96f68-145">Qualificatori: **WmiDataId** (1)</span><span class="sxs-lookup"><span data-stu-id="96f68-145">Qualifiers: **WmiDataId** (1)</span></span>
</dt> </dl>

<span data-ttu-id="96f68-146">Quantità massima di memoria supportata, in byte.</span><span class="sxs-lookup"><span data-stu-id="96f68-146">Maximum amount of memory supported, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="96f68-147">**Flag di stato**</span><span class="sxs-lookup"><span data-stu-id="96f68-147">**StateFlags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="96f68-148">Tipo di dati: **uint32**</span><span class="sxs-lookup"><span data-stu-id="96f68-148">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="96f68-149">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="96f68-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="96f68-150">Qualificatori: **WmiDataId** (11), **Format("x")**</span><span class="sxs-lookup"><span data-stu-id="96f68-150">Qualifiers: **WmiDataId** (11), **Format("x")**</span></span>
</dt> </dl>

<span data-ttu-id="96f68-151">Flag di stato del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="96f68-151">Device state flags.</span></span> <span data-ttu-id="96f68-152">Può essere qualsiasi combinazione ragionevole di quanto segue.</span><span class="sxs-lookup"><span data-stu-id="96f68-152">It can be any reasonable combination of the following.</span></span>



| <span data-ttu-id="96f68-153">Valore</span><span class="sxs-lookup"><span data-stu-id="96f68-153">Value</span></span>                                                                                                                                                                                                                                                                                        | <span data-ttu-id="96f68-154">Significato</span><span class="sxs-lookup"><span data-stu-id="96f68-154">Meaning</span></span>                                                                                                                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DISPLAY_DEVICE_ATTACHED_TO_DESKTOP"></span><span id="display_device_attached_to_desktop"></span><dl> <span data-ttu-id="96f68-155"><dt>**VISUALIZZAZIONE \_ DISPOSITIVO \_ COLLEGATO \_ A \_ DESKTOP**</dt> <dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="96f68-155"><dt>**DISPLAY\_DEVICE\_ATTACHED\_TO\_DESKTOP**</dt> <dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="96f68-156">Il dispositivo fa parte del desktop.</span><span class="sxs-lookup"><span data-stu-id="96f68-156">The device is part of the desktop.</span></span><br/>                                                                                                                                                                                |
| <span id="DISPLAY_DEVICE_MIRRORING_DRIVER"></span><span id="display_device_mirroring_driver"></span><dl> <span data-ttu-id="96f68-157"><dt>**VISUALIZZAZIONE \_ DRIVER \_ DI \_ MIRRORING DEL**</dt> DISPOSITIVO <dt>8 (0x8)</dt></span><span class="sxs-lookup"><span data-stu-id="96f68-157"><dt>**DISPLAY\_DEVICE\_MIRRORING\_DRIVER**</dt> <dt>8 (0x8)</dt></span></span> </dl>           | <span data-ttu-id="96f68-158">Rappresenta uno pseudo dispositivo usato per eseguire il mirroring del disegno dell'applicazione per la connessione a un computer remoto o ad altri scopi.</span><span class="sxs-lookup"><span data-stu-id="96f68-158">Represents a pseudo device used to mirror application drawing for connecting to a remote computer or other purposes.</span></span> <span data-ttu-id="96f68-159">A questo dispositivo è associato uno pseudo monitor invisibile.</span><span class="sxs-lookup"><span data-stu-id="96f68-159">An invisible pseudo monitor is associated with this device.</span></span> <span data-ttu-id="96f68-160">Ad esempio, Viene utilizzato da NetMeeting.</span><span class="sxs-lookup"><span data-stu-id="96f68-160">For example, NetMeeting uses it.</span></span><br/> |
| <span id="DISPLAY_DEVICE_MODESPRUNED"></span><span id="display_device_modespruned"></span><dl> <span data-ttu-id="96f68-161"><dt>**VISUALIZZAZIONE \_ DEVICE \_ MODESPRUNED**</dt> <dt>134217728 (0x8000000)</dt></span><span class="sxs-lookup"><span data-stu-id="96f68-161"><dt>**DISPLAY\_DEVICE\_MODESPRUNED**</dt> <dt>134217728 (0x8000000)</dt></span></span> </dl>             | <span data-ttu-id="96f68-162">Il dispositivo ha più modalità di visualizzazione di quelle supportate dai dispositivi di output.</span><span class="sxs-lookup"><span data-stu-id="96f68-162">The device has more display modes than its output devices support.</span></span><br/>                                                                                                                                                |
| <span id="DISPLAY_DEVICE_PRIMARY_DEVICE"></span><span id="display_device_primary_device"></span><dl> <span data-ttu-id="96f68-163"><dt>**VISUALIZZAZIONE \_ DISPOSITIVO \_ PRIMARIO \_ DISPOSITIVO**</dt> <dt>4 (0x4)</dt></span><span class="sxs-lookup"><span data-stu-id="96f68-163"><dt>**DISPLAY\_DEVICE\_PRIMARY\_DEVICE**</dt> <dt>4 (0x4)</dt></span></span> </dl>                 | <span data-ttu-id="96f68-164">Il desktop primario si trova nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="96f68-164">The primary desktop is on the device.</span></span> <span data-ttu-id="96f68-165">Per un sistema con una singola scheda di visualizzazione, questa opzione è sempre impostata.</span><span class="sxs-lookup"><span data-stu-id="96f68-165">For a system with a single display card, this is always set.</span></span> <span data-ttu-id="96f68-166">Per un sistema con più schede video, solo un dispositivo può avere questo set.</span><span class="sxs-lookup"><span data-stu-id="96f68-166">For a system with multiple display cards, only one device can have this set.</span></span><br/>                                   |
| <span id="DISPLAY_DEVICE_REMOVABLE"></span><span id="display_device_removable"></span><dl> <span data-ttu-id="96f68-167"><dt>**VISUALIZZAZIONE \_ DISPOSITIVO \_ RIMOVIBILE**</dt> <dt>32 (0x20)</dt></span><span class="sxs-lookup"><span data-stu-id="96f68-167"><dt>**DISPLAY\_DEVICE\_REMOVABLE**</dt> <dt>32 (0x20)</dt></span></span> </dl>                               | <span data-ttu-id="96f68-168">Il dispositivo è rimovibile. non può essere la visualizzazione primaria.</span><span class="sxs-lookup"><span data-stu-id="96f68-168">The device is removable; it cannot be the primary display.</span></span><br/>                                                                                                                                                        |
| <span id="DISPLAY_DEVICE_VGA_COMPATIBLE"></span><span id="display_device_vga_compatible"></span><dl> <span data-ttu-id="96f68-169"><dt>**VISUALIZZAZIONE \_ COMPATIBILE \_ CON VGA \_ DEL DISPOSITIVO**</dt> <dt>16 (0x10)</dt></span><span class="sxs-lookup"><span data-stu-id="96f68-169"><dt>**DISPLAY\_DEVICE\_VGA\_COMPATIBLE**</dt> <dt>16 (0x10)</dt></span></span> </dl>               | <span data-ttu-id="96f68-170">Il dispositivo è compatibile con VGA.</span><span class="sxs-lookup"><span data-stu-id="96f68-170">The device is VGA compatible.</span></span><br/>                                                                                                                                                                                     |



 

</dd> <dt>

<span data-ttu-id="96f68-171">**VRefresh**</span><span class="sxs-lookup"><span data-stu-id="96f68-171">**VRefresh**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="96f68-172">Tipo di dati: **uint32**</span><span class="sxs-lookup"><span data-stu-id="96f68-172">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="96f68-173">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="96f68-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="96f68-174">Qualificatori: **WmiDataId** (5)</span><span class="sxs-lookup"><span data-stu-id="96f68-174">Qualifiers: **WmiDataId** (5)</span></span>
</dt> </dl>

<span data-ttu-id="96f68-175">Frequenza di aggiornamento corrente, in hertz.</span><span class="sxs-lookup"><span data-stu-id="96f68-175">Current refresh rate, in hertz.</span></span>

</dd> <dt>

<span data-ttu-id="96f68-176">**XResolution**</span><span class="sxs-lookup"><span data-stu-id="96f68-176">**XResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="96f68-177">Tipo di dati: **uint32**</span><span class="sxs-lookup"><span data-stu-id="96f68-177">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="96f68-178">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="96f68-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="96f68-179">Qualificatori: **WmiDataId** (2)</span><span class="sxs-lookup"><span data-stu-id="96f68-179">Qualifiers: **WmiDataId** (2)</span></span>
</dt> </dl>

<span data-ttu-id="96f68-180">Numero corrente di pixel orizzontali.</span><span class="sxs-lookup"><span data-stu-id="96f68-180">Current number of horizontal pixels.</span></span>

</dd> <dt>

<span data-ttu-id="96f68-181">**YResolution**</span><span class="sxs-lookup"><span data-stu-id="96f68-181">**YResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="96f68-182">Tipo di dati: **uint32**</span><span class="sxs-lookup"><span data-stu-id="96f68-182">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="96f68-183">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="96f68-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="96f68-184">Qualificatori: **WmiDataId** (3)</span><span class="sxs-lookup"><span data-stu-id="96f68-184">Qualifiers: **WmiDataId** (3)</span></span>
</dt> </dl>

<span data-ttu-id="96f68-185">Numero corrente di pixel verticali.</span><span class="sxs-lookup"><span data-stu-id="96f68-185">Current number of vertical pixels.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="96f68-186">Requisiti</span><span class="sxs-lookup"><span data-stu-id="96f68-186">Requirements</span></span>



| <span data-ttu-id="96f68-187">Requisito</span><span class="sxs-lookup"><span data-stu-id="96f68-187">Requirement</span></span> | <span data-ttu-id="96f68-188">Valore</span><span class="sxs-lookup"><span data-stu-id="96f68-188">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="96f68-189">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="96f68-189">Minimum supported client</span></span><br/> | <span data-ttu-id="96f68-190">Solo app desktop di Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="96f68-190">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="96f68-191">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="96f68-191">Minimum supported server</span></span><br/> | <span data-ttu-id="96f68-192">Solo app desktop di Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="96f68-192">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="96f68-193">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="96f68-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96f68-194">**SystemConfig**</span><span class="sxs-lookup"><span data-stu-id="96f68-194">**SystemConfig**</span></span>](systemconfig.md)
</dt> </dl>

 

 




