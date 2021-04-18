---
description: La \_ struttura dell'intestazione non elaborata WIA \_ definisce un'immagine nel formato dati non elaborati di un dispositivo e consente alle applicazioni di utilizzare il formato non elaborato nei trasferimenti WIA (Windows Image Acquisition).
ms.assetid: c7b50816-d596-4c62-a00e-cd8d6e303e42
title: Struttura WIA_RAW_HEADER (Wiadef. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_RAW_HEADER
api_type:
- HeaderDef
api_location:
- Wiadef.h
ms.openlocfilehash: 8da33f0b257168712f1b16fb7f940df5db862d3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307307"
---
# <a name="wia_raw_header-structure"></a><span data-ttu-id="56b1a-103">\_Struttura di intestazione non elaborata WIA \_</span><span class="sxs-lookup"><span data-stu-id="56b1a-103">WIA\_RAW\_HEADER structure</span></span>

<span data-ttu-id="56b1a-104">La struttura dell' **\_ \_ intestazione non elaborata WIA** definisce un'immagine nel formato dati non elaborati di un dispositivo e consente alle applicazioni di utilizzare il formato non elaborato nei trasferimenti WIA (Windows Image Acquisition).</span><span class="sxs-lookup"><span data-stu-id="56b1a-104">The **WIA\_RAW\_HEADER** structure defines an image in the RAW data format of a device and enables applications to use RAW format in Windows Image Acquisition (WIA) transfers.</span></span>

## <a name="syntax"></a><span data-ttu-id="56b1a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="56b1a-105">Syntax</span></span>


```C++
typedef struct _WIA_RAW_HEADER {
  DWORD Tag;
  DWORD Version;
  DWORD HeaderSize;
  DWORD XRes;
  DWORD YRes;
  DWORD XExtent;
  DWORD YExtent;
  DWORD BytesPerLine;
  DWORD BitsPerPixel;
  DWORD ChannelsPerPixel;
  DWORD DataType;
  BYTE  BitsPerChannel[8];
  DWORD Compression;
  DWORD PhotometricInterp;
  DWORD LineOrder;
  DWORD RawDataOffset;
  DWORD RawDataSize;
  DWORD PaletteOffset;
  DWORD PaletteSize;
} WIA_RAW_HEADER;
```



## <a name="members"></a><span data-ttu-id="56b1a-106">Members</span><span class="sxs-lookup"><span data-stu-id="56b1a-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="56b1a-107">**Tag**</span><span class="sxs-lookup"><span data-stu-id="56b1a-107">**Tag**</span></span>
</dt> <dd>

<span data-ttu-id="56b1a-108">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="56b1a-108">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="56b1a-109">Nome del formato.</span><span class="sxs-lookup"><span data-stu-id="56b1a-109">The name of the format.</span></span> <span data-ttu-id="56b1a-110">Deve essere il valore letterale ' WRAW ' (caratteri ASCII a byte singolo).</span><span class="sxs-lookup"><span data-stu-id="56b1a-110">This must be the literal 'WRAW' (four single byte ASCII characters).</span></span>

</dd> <dt>

<span data-ttu-id="56b1a-111">**Versione**</span><span class="sxs-lookup"><span data-stu-id="56b1a-111">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="56b1a-112">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="56b1a-112">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="56b1a-113">Versione del formato non elaborato.</span><span class="sxs-lookup"><span data-stu-id="56b1a-113">The version of the RAW format.</span></span> <span data-ttu-id="56b1a-114">Usare sempre 0x00010000.</span><span class="sxs-lookup"><span data-stu-id="56b1a-114">Always use 0x00010000.</span></span>

</dd> <dt>

<span data-ttu-id="56b1a-115">**HeaderSize**</span><span class="sxs-lookup"><span data-stu-id="56b1a-115">**HeaderSize**</span></span>
</dt> <dd>

<span data-ttu-id="56b1a-116">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="56b1a-116">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="56b1a-117">Byte totali validi nell'intestazione.</span><span class="sxs-lookup"><span data-stu-id="56b1a-117">The total valid bytes in the header.</span></span>

</dd> <dt>

<span data-ttu-id="56b1a-118">**XRes**</span><span class="sxs-lookup"><span data-stu-id="56b1a-118">**XRes**</span></span>
</dt> <dd>

<span data-ttu-id="56b1a-119">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="56b1a-119">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="56b1a-120">Risoluzione orizzontale espressa in punti per pollice.</span><span class="sxs-lookup"><span data-stu-id="56b1a-120">The horizontal resolution in dots per inch.</span></span>

</dd> <dt>

<span data-ttu-id="56b1a-121">**YRes**</span><span class="sxs-lookup"><span data-stu-id="56b1a-121">**YRes**</span></span>
</dt> <dd>

<span data-ttu-id="56b1a-122">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="56b1a-122">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="56b1a-123">Risoluzione verticale espressa in punti per pollice.</span><span class="sxs-lookup"><span data-stu-id="56b1a-123">The vertical resolution in dots per inch.</span></span>

</dd> <dt>

<span data-ttu-id="56b1a-124">**Stampa**</span><span class="sxs-lookup"><span data-stu-id="56b1a-124">**XExtent**</span></span>
</dt> <dd>

<span data-ttu-id="56b1a-125">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="56b1a-125">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="56b1a-126">Larghezza dell'immagine in pixel.</span><span class="sxs-lookup"><span data-stu-id="56b1a-126">The width of the image in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="56b1a-127">**YExtent**</span><span class="sxs-lookup"><span data-stu-id="56b1a-127">**YExtent**</span></span>
</dt> <dd>

<span data-ttu-id="56b1a-128">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="56b1a-128">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="56b1a-129">Altezza dell'immagine in pixel.</span><span class="sxs-lookup"><span data-stu-id="56b1a-129">The height of the image in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="56b1a-130">**BytesPerLine**</span><span class="sxs-lookup"><span data-stu-id="56b1a-130">**BytesPerLine**</span></span>
</dt> <dd>

<span data-ttu-id="56b1a-131">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="56b1a-131">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="56b1a-132">Numero di byte in una riga di un'immagine non compressa.</span><span class="sxs-lookup"><span data-stu-id="56b1a-132">The number of bytes in a line of an uncompressed image.</span></span> <span data-ttu-id="56b1a-133">Utilizzare 0 quando i dati vengono compressi per segnalare che il numero di byte per riga è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="56b1a-133">Use 0 when the data is compressed to signal that the number of bytes per line is unknown.</span></span>

</dd> <dt>

<span data-ttu-id="56b1a-134">**BitsPerPixel**</span><span class="sxs-lookup"><span data-stu-id="56b1a-134">**BitsPerPixel**</span></span>
</dt> <dd>

<span data-ttu-id="56b1a-135">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="56b1a-135">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="56b1a-136">Numero totale di bit per pixel per tutti i canali del pixel.</span><span class="sxs-lookup"><span data-stu-id="56b1a-136">The total number of bits per pixel for all the pixel's channels.</span></span>

</dd> <dt>

<span data-ttu-id="56b1a-137">**ChannelsPerPixel**</span><span class="sxs-lookup"><span data-stu-id="56b1a-137">**ChannelsPerPixel**</span></span>
</dt> <dd>

<span data-ttu-id="56b1a-138">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="56b1a-138">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="56b1a-139">Numero di canali di colore in un pixel.</span><span class="sxs-lookup"><span data-stu-id="56b1a-139">The number of color channels in a pixel.</span></span>

</dd> <dt>

<span data-ttu-id="56b1a-140">**DataType**</span><span class="sxs-lookup"><span data-stu-id="56b1a-140">**DataType**</span></span>
</dt> <dd>

<span data-ttu-id="56b1a-141">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="56b1a-141">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="56b1a-142">\_Tipo di dati IPA WIA \_ dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="56b1a-142">The WIA\_IPA\_DATATYPE of the image.</span></span> <span data-ttu-id="56b1a-143">Poiché \_ il formato dell'IPA WIA \_ è impostato su WiaImgFmt \_ RAW, si tratta di un elenco di valori consentiti da cui l'applicazione sceglie.</span><span class="sxs-lookup"><span data-stu-id="56b1a-143">Since WIA\_IPA\_FORMAT is set to WiaImgFmt\_RAW, this is a list of allowed values from which the application picks.</span></span>

</dd> <dt>

<span data-ttu-id="56b1a-144">**BitsPerChannel \[ 8\]**</span><span class="sxs-lookup"><span data-stu-id="56b1a-144">**BitsPerChannel\[8\]**</span></span>
</dt> <dd>

<span data-ttu-id="56b1a-145">Tipo: **byte**</span><span class="sxs-lookup"><span data-stu-id="56b1a-145">Type: **BYTE**</span></span>

</dd> <dd>

<span data-ttu-id="56b1a-146">Numero di bit in un canale, fino a un massimo di 8.</span><span class="sxs-lookup"><span data-stu-id="56b1a-146">The number of bits in a channel, up to a maximum of 8.</span></span>

</dd> <dt>

<span data-ttu-id="56b1a-147">**Compressione**</span><span class="sxs-lookup"><span data-stu-id="56b1a-147">**Compression**</span></span>
</dt> <dd>

<span data-ttu-id="56b1a-148">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="56b1a-148">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="56b1a-149">Un valore di compressione del pacchetto WIA che \_ \_ specifica il tipo di compressione usato, se presente.</span><span class="sxs-lookup"><span data-stu-id="56b1a-149">A WIA\_IPA\_COMPRESSION value specifying the type of compression used, if any.</span></span>

</dd> <dt>

<span data-ttu-id="56b1a-150">**PhotometricInterp**</span><span class="sxs-lookup"><span data-stu-id="56b1a-150">**PhotometricInterp**</span></span>
</dt> <dd>

<span data-ttu-id="56b1a-151">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="56b1a-151">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="56b1a-152">\_ \_ Valore interp della fotometria IPA WIA che \_ specifica l'interpretazione fotometrica dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="56b1a-152">A WIA\_IPA\_PHOTOMETRIC\_INTERP value specifying the photometric interpretation of the image.</span></span>

</dd> <dt>

<span data-ttu-id="56b1a-153">**LineOrder**</span><span class="sxs-lookup"><span data-stu-id="56b1a-153">**LineOrder**</span></span>
</dt> <dd>

<span data-ttu-id="56b1a-154">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="56b1a-154">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="56b1a-155">Valore che rappresenta l'ordine di riga dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="56b1a-155">A value representing the image line order.</span></span> <span data-ttu-id="56b1a-156">Si tratta sempre dell' \_ ordine della riga WIA \_ \_ dall'alto \_ verso il \_ basso o \_ \_ \_ dal basso \_ verso l'alto nell'ordine della riga \_ .</span><span class="sxs-lookup"><span data-stu-id="56b1a-156">This is always either WIA\_LINE\_ORDER\_TOP\_TO\_BOTTOM or WIA\_LINE\_ORDER\_BOTTOM\_TO\_TOP.</span></span>

</dd> <dt>

<span data-ttu-id="56b1a-157">**RawDataOffset**</span><span class="sxs-lookup"><span data-stu-id="56b1a-157">**RawDataOffset**</span></span>
</dt> <dd>

<span data-ttu-id="56b1a-158">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="56b1a-158">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="56b1a-159">Posizione dei dati dell'immagine non elaborata in byte, a partire dalla posizione in cui termina l'intestazione o dalla posizione in cui termina la tavolozza.</span><span class="sxs-lookup"><span data-stu-id="56b1a-159">The position of the raw image data in bytes, starting from position where the header ends or the position where the palette ends.</span></span>

</dd> <dt>

<span data-ttu-id="56b1a-160">**RawDataSize**</span><span class="sxs-lookup"><span data-stu-id="56b1a-160">**RawDataSize**</span></span>
</dt> <dd>

<span data-ttu-id="56b1a-161">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="56b1a-161">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="56b1a-162">Dimensione, in byte, dei dati dell'immagine non elaborata.</span><span class="sxs-lookup"><span data-stu-id="56b1a-162">The size, in bytes, of the raw image data.</span></span>

</dd> <dt>

<span data-ttu-id="56b1a-163">**PaletteOffset**</span><span class="sxs-lookup"><span data-stu-id="56b1a-163">**PaletteOffset**</span></span>
</dt> <dd>

<span data-ttu-id="56b1a-164">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="56b1a-164">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="56b1a-165">Posizione della tavolozza in byte, a partire dalla posizione in cui termina l'intestazione o dalla posizione in cui terminano i dati.</span><span class="sxs-lookup"><span data-stu-id="56b1a-165">The position of the palette in bytes, starting from the position where the header ends or the position where the data ends.</span></span> <span data-ttu-id="56b1a-166">(Questo valore è 0, se non è presente alcuna tavolozza).</span><span class="sxs-lookup"><span data-stu-id="56b1a-166">(This value is 0, if there is no palette.)</span></span>

</dd> <dt>

<span data-ttu-id="56b1a-167">**PaletteSize**</span><span class="sxs-lookup"><span data-stu-id="56b1a-167">**PaletteSize**</span></span>
</dt> <dd>

<span data-ttu-id="56b1a-168">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="56b1a-168">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="56b1a-169">Dimensione, in byte, della tabella della tavolozza.</span><span class="sxs-lookup"><span data-stu-id="56b1a-169">The size, in bytes, of the palette table.</span></span> <span data-ttu-id="56b1a-170">(Questo è 0, se non è presente alcuna tavolozza).</span><span class="sxs-lookup"><span data-stu-id="56b1a-170">(This is 0, if there is no palette.)</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="56b1a-171">Commenti</span><span class="sxs-lookup"><span data-stu-id="56b1a-171">Remarks</span></span>

<span data-ttu-id="56b1a-172">Poiché non si tratta di un formato di file, utilizzare una stringa vuota per \_ la \_ proprietà dell'estensione del file IPA WIA \_ .</span><span class="sxs-lookup"><span data-stu-id="56b1a-172">Because this is not a file format, use an empty string for the WIA\_IPA\_FILE\_EXTENSION property.</span></span>

<span data-ttu-id="56b1a-173">La tavolozza e i dati possono essere in qualsiasi ordine.</span><span class="sxs-lookup"><span data-stu-id="56b1a-173">The palette and the data can come in either order.</span></span>

<span data-ttu-id="56b1a-174">**RawDataSize** non include l'intestazione o la tavolozza.</span><span class="sxs-lookup"><span data-stu-id="56b1a-174">**RawDataSize** does not include either the header or the palette.</span></span> <span data-ttu-id="56b1a-175">Utilizzare questo campo per verificare che il trasferimento dell'immagine abbia avuto esito positivo.</span><span class="sxs-lookup"><span data-stu-id="56b1a-175">Use this field to verify that the transfer of the image has been successful.</span></span>

<span data-ttu-id="56b1a-176">**PaletteSize** è byte, non il numero di voci nella tavolozza.</span><span class="sxs-lookup"><span data-stu-id="56b1a-176">**PaletteSize** is bytes, not the number of entries in the palette.</span></span>

## <a name="requirements"></a><span data-ttu-id="56b1a-177">Requisiti</span><span class="sxs-lookup"><span data-stu-id="56b1a-177">Requirements</span></span>



| <span data-ttu-id="56b1a-178">Requisito</span><span class="sxs-lookup"><span data-stu-id="56b1a-178">Requirement</span></span> | <span data-ttu-id="56b1a-179">Valore</span><span class="sxs-lookup"><span data-stu-id="56b1a-179">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="56b1a-180">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="56b1a-180">Minimum supported client</span></span><br/> | <span data-ttu-id="56b1a-181">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="56b1a-181">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="56b1a-182">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="56b1a-182">Minimum supported server</span></span><br/> | <span data-ttu-id="56b1a-183">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="56b1a-183">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="56b1a-184">Intestazione</span><span class="sxs-lookup"><span data-stu-id="56b1a-184">Header</span></span><br/>                   | <dl> <span data-ttu-id="56b1a-185"><dt>Wiadef. h</dt></span><span class="sxs-lookup"><span data-stu-id="56b1a-185"><dt>Wiadef.h</dt></span></span> </dl> |



 

 




