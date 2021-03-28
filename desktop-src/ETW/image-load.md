---
description: Questa classe è la classe del tipo di evento per gli eventi di immagine. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: 70ec0542-16d3-4186-a346-7f3c44dedf67
title: Classe Image_Load
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Image_Load
- Image_Load.ImageBase
- Image_Load.ImageSize
- Image_Load.ProcessId
- Image_Load.ImageCheckSum
- Image_Load.TimeDateStamp
- Image_Load.Reserved0
- Image_Load.DefaultBase
- Image_Load.Reserved1
- Image_Load.Reserved2
- Image_Load.Reserved3
- Image_Load.Reserved4
- Image_Load.FileName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 647879b972c7cff2c086f656f76fa8decedb49a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528651"
---
# <a name="image_load-class"></a><span data-ttu-id="ba491-104">\_Classe di caricamento immagini</span><span class="sxs-lookup"><span data-stu-id="ba491-104">Image\_Load class</span></span>

<span data-ttu-id="ba491-105">Questa classe è la classe del tipo di evento per gli eventi di immagine.</span><span class="sxs-lookup"><span data-stu-id="ba491-105">This class is the event type class for image events.</span></span>

<span data-ttu-id="ba491-106">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="ba491-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba491-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ba491-107">Syntax</span></span>

``` syntax
[EventType(10, 2, 3, 4), EventTypeName("Load", "Unload", "DCStart", "DCEnd")]
class Image_Load : Image
{
  uint32 ImageBase;
  uint32 ImageSize;
  uint32 ProcessId;
  uint32 ImageCheckSum;
  uint32 TimeDateStamp;
  uint32 Reserved0;
  uint32 DefaultBase;
  uint32 Reserved1;
  uint32 Reserved2;
  uint32 Reserved3;
  uint32 Reserved4;
  string FileName;
};
```

## <a name="members"></a><span data-ttu-id="ba491-108">Members</span><span class="sxs-lookup"><span data-stu-id="ba491-108">Members</span></span>

<span data-ttu-id="ba491-109">La classe di **\_ caricamento dell'immagine** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="ba491-109">The **Image\_Load** class has these types of members:</span></span>

-   [<span data-ttu-id="ba491-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ba491-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ba491-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ba491-111">Properties</span></span>

<span data-ttu-id="ba491-112">Questa proprietà è **configurata nella classe \_ Load** .</span><span class="sxs-lookup"><span data-stu-id="ba491-112">The **Image\_Load** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ba491-113">DefaultBase</span><span class="sxs-lookup"><span data-stu-id="ba491-113">DefaultBase</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba491-114">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ba491-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ba491-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ba491-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ba491-116">Qualificatori: WmiDataId (7), puntatore</span><span class="sxs-lookup"><span data-stu-id="ba491-116">Qualifiers: WmiDataId(7), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="ba491-117">Indirizzo di base predefinito.</span><span class="sxs-lookup"><span data-stu-id="ba491-117">Default base address.</span></span>

</dd> <dt>

<span data-ttu-id="ba491-118">FileName</span><span class="sxs-lookup"><span data-stu-id="ba491-118">FileName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba491-119">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ba491-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ba491-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ba491-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ba491-121">Qualificatori: WmiDataId (12), StringTermination ("NullTerminated"), Format ("w")</span><span class="sxs-lookup"><span data-stu-id="ba491-121">Qualifiers: WmiDataId(12), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="ba491-122">Nome file ed estensione della DLL o dell'immagine eseguibile.</span><span class="sxs-lookup"><span data-stu-id="ba491-122">File name and extension of the DLL or executable image.</span></span>

</dd> <dt>

<span data-ttu-id="ba491-123">ImageBase sul</span><span class="sxs-lookup"><span data-stu-id="ba491-123">ImageBase</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba491-124">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ba491-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ba491-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ba491-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ba491-126">Qualificatori: WmiDataId (1), puntatore</span><span class="sxs-lookup"><span data-stu-id="ba491-126">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="ba491-127">Indirizzo di base dell'applicazione in cui viene caricata l'immagine.</span><span class="sxs-lookup"><span data-stu-id="ba491-127">Base address of the application in which the image is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="ba491-128">ImageCheckSum</span><span class="sxs-lookup"><span data-stu-id="ba491-128">ImageCheckSum</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba491-129">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ba491-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ba491-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ba491-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ba491-131">Qualificatori: WmiDataId (4)</span><span class="sxs-lookup"><span data-stu-id="ba491-131">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="ba491-132">Somma controllo immagine.</span><span class="sxs-lookup"><span data-stu-id="ba491-132">Image check sum.</span></span>

</dd> <dt>

<span data-ttu-id="ba491-133">ImageSize</span><span class="sxs-lookup"><span data-stu-id="ba491-133">ImageSize</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba491-134">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ba491-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ba491-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ba491-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ba491-136">Qualificatori: WmiDataId (2), puntatore</span><span class="sxs-lookup"><span data-stu-id="ba491-136">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="ba491-137">Dimensione dell'immagine da caricare.</span><span class="sxs-lookup"><span data-stu-id="ba491-137">Size of the image being loaded.</span></span>

<span data-ttu-id="ba491-138">Quando si utilizza questa proprietà, il tipo di dati per questa proprietà è effettivamente size \_ t.</span><span class="sxs-lookup"><span data-stu-id="ba491-138">When consuming this property, the data type for this property is actually size\_t.</span></span> <span data-ttu-id="ba491-139">Il qualificatore del puntatore viene utilizzato per determinare se la dimensione \_ t è di 4 byte o 8 byte.</span><span class="sxs-lookup"><span data-stu-id="ba491-139">The Pointer qualifier is used to determine if the size\_t is 4-bytes or 8-bytes.</span></span>

</dd> <dt>

<span data-ttu-id="ba491-140">ProcessId</span><span class="sxs-lookup"><span data-stu-id="ba491-140">ProcessId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba491-141">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ba491-141">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ba491-142">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ba491-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ba491-143">Qualificatori: WmiDataId (3)</span><span class="sxs-lookup"><span data-stu-id="ba491-143">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="ba491-144">Identifica il processo in cui viene caricata l'immagine.</span><span class="sxs-lookup"><span data-stu-id="ba491-144">Identifies the process into which the image is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="ba491-145">Reserved0</span><span class="sxs-lookup"><span data-stu-id="ba491-145">Reserved0</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba491-146">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ba491-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ba491-147">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ba491-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ba491-148">Qualificatori: WmiDataId (6)</span><span class="sxs-lookup"><span data-stu-id="ba491-148">Qualifiers: WmiDataId(6)</span></span>
</dt> </dl>

<span data-ttu-id="ba491-149">Riservato.</span><span class="sxs-lookup"><span data-stu-id="ba491-149">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="ba491-150">Reserved1</span><span class="sxs-lookup"><span data-stu-id="ba491-150">Reserved1</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba491-151">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ba491-151">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ba491-152">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ba491-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ba491-153">Qualificatori: WmiDataId (8)</span><span class="sxs-lookup"><span data-stu-id="ba491-153">Qualifiers: WmiDataId(8)</span></span>
</dt> </dl>

<span data-ttu-id="ba491-154">Riservato.</span><span class="sxs-lookup"><span data-stu-id="ba491-154">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="ba491-155">Reserved2</span><span class="sxs-lookup"><span data-stu-id="ba491-155">Reserved2</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba491-156">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ba491-156">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ba491-157">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ba491-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ba491-158">Qualificatori: WmiDataId (9)</span><span class="sxs-lookup"><span data-stu-id="ba491-158">Qualifiers: WmiDataId(9)</span></span>
</dt> </dl>

<span data-ttu-id="ba491-159">Riservato.</span><span class="sxs-lookup"><span data-stu-id="ba491-159">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="ba491-160">Reserved3</span><span class="sxs-lookup"><span data-stu-id="ba491-160">Reserved3</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba491-161">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ba491-161">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ba491-162">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ba491-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ba491-163">Qualificatori: WmiDataId (10)</span><span class="sxs-lookup"><span data-stu-id="ba491-163">Qualifiers: WmiDataId(10)</span></span>
</dt> </dl>

<span data-ttu-id="ba491-164">Riservato.</span><span class="sxs-lookup"><span data-stu-id="ba491-164">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="ba491-165">Reserved4</span><span class="sxs-lookup"><span data-stu-id="ba491-165">Reserved4</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba491-166">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ba491-166">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ba491-167">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ba491-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ba491-168">Qualificatori: WmiDataId (11)</span><span class="sxs-lookup"><span data-stu-id="ba491-168">Qualifiers: WmiDataId(11)</span></span>
</dt> </dl>

<span data-ttu-id="ba491-169">Riservato.</span><span class="sxs-lookup"><span data-stu-id="ba491-169">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="ba491-170">TimeDateStamp</span><span class="sxs-lookup"><span data-stu-id="ba491-170">TimeDateStamp</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba491-171">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ba491-171">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ba491-172">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ba491-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ba491-173">Qualificatori: WmiDataId (5)</span><span class="sxs-lookup"><span data-stu-id="ba491-173">Qualifiers: WmiDataId(5)</span></span>
</dt> </dl>

<span data-ttu-id="ba491-174">Data e ora in cui l'immagine è stata caricata o scaricata.</span><span class="sxs-lookup"><span data-stu-id="ba491-174">Time and date that the image was loaded or unloaded.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ba491-175">Commenti</span><span class="sxs-lookup"><span data-stu-id="ba491-175">Remarks</span></span>

<span data-ttu-id="ba491-176">Gli eventi DCStart e DCEnd enumerano tutte le immagini caricate rispettivamente all'inizio e alla fine della traccia.</span><span class="sxs-lookup"><span data-stu-id="ba491-176">The DCStart and DCEnd events enumerate all loaded images at the beginning and end of the trace, respectively.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba491-177">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ba491-177">Requirements</span></span>



| <span data-ttu-id="ba491-178">Requisito</span><span class="sxs-lookup"><span data-stu-id="ba491-178">Requirement</span></span> | <span data-ttu-id="ba491-179">Valore</span><span class="sxs-lookup"><span data-stu-id="ba491-179">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ba491-180">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ba491-180">Minimum supported client</span></span><br/> | <span data-ttu-id="ba491-181">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ba491-181">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ba491-182">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ba491-182">Minimum supported server</span></span><br/> | <span data-ttu-id="ba491-183">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ba491-183">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ba491-184">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ba491-184">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba491-185">**Immagine**</span><span class="sxs-lookup"><span data-stu-id="ba491-185">**Image**</span></span>](image.md)
</dt> <dt>

[<span data-ttu-id="ba491-186">**Immagine \_ V0**</span><span class="sxs-lookup"><span data-stu-id="ba491-186">**Image\_V0**</span></span>](image-v0.md)
</dt> <dt>

[<span data-ttu-id="ba491-187">**Immagine \_ V1**</span><span class="sxs-lookup"><span data-stu-id="ba491-187">**Image\_V1**</span></span>](image-v1.md)
</dt> </dl>

 

 




