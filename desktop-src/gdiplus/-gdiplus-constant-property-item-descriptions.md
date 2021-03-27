---
description: Nell'elenco seguente vengono fornite le descrizioni degli elementi della proprietà supportati da Windows GDI+.
ms.assetid: fc95aa3f-8381-430d-8cbf-6d23816a738d
title: Descrizioni degli elementi delle proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfc2a627ec809bb4f7d7299c522fd0e9d3e1cc05
ms.sourcegitcommit: 80ee822f6ebcbcc8f60042e0d14a39ef6989c731
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/27/2021
ms.locfileid: "105636123"
---
# <a name="property-item-descriptions"></a><span data-ttu-id="b8c96-103">Descrizioni degli elementi delle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-103">Property Item Descriptions</span></span>

<span data-ttu-id="b8c96-104">Nell'elenco seguente vengono fornite le descrizioni degli elementi della proprietà supportati da Windows GDI+.</span><span class="sxs-lookup"><span data-stu-id="b8c96-104">The following list gives descriptions of the property items supported by Windows GDI+.</span></span> <span data-ttu-id="b8c96-105">Le descrizioni sono brevi e generali in modo da essere valide per un'ampia gamma di formati di file di immagine.</span><span class="sxs-lookup"><span data-stu-id="b8c96-105">The descriptions are brief and general so that they apply to a variety of image file formats.</span></span> <span data-ttu-id="b8c96-106">Per una descrizione dettagliata del modo in cui un elemento di proprietà viene usato da un particolare formato di file, vedere la specifica del formato di file.</span><span class="sxs-lookup"><span data-stu-id="b8c96-106">For a detailed description of how a property item is used by a particular file format, see the specification for that file format.</span></span> <span data-ttu-id="b8c96-107">Per i collegamenti a diverse specifiche di file e ad altri documenti che descrivono i metadati in dettaglio, vedere [specifiche del formato del file di immagine](-gdiplus-constant-image-file-format-specifications.md).</span><span class="sxs-lookup"><span data-stu-id="b8c96-107">For links to several file specifications and other documents that describe metadata in detail, see [Image File Format Specifications](-gdiplus-constant-image-file-format-specifications.md).</span></span>

<span data-ttu-id="b8c96-108">Il formato EXIF (Exchangeable image file) è uno standard JEIDA (Japan Electronic Industry Development Association), modificato il 1998 giugno come versione 2,1.</span><span class="sxs-lookup"><span data-stu-id="b8c96-108">The Exchangeable Image File (EXIF) format is a Japan Electronic Industry Development Association (JEIDA) standard, revised June 1998 as version 2.1.</span></span> <span data-ttu-id="b8c96-109">Le parti della specifica EXIF vengono usate con l'autorizzazione di JEIDA.</span><span class="sxs-lookup"><span data-stu-id="b8c96-109">Portions of the EXIF specification are used with permission of JEIDA.</span></span>

## <a name="propertytaggpsver"></a><span data-ttu-id="b8c96-110">PropertyTagGpsVer</span><span class="sxs-lookup"><span data-stu-id="b8c96-110">PropertyTagGpsVer</span></span>

<span data-ttu-id="b8c96-111">Versione di Global Positioning Systems (GPS) IFD, specificata come 2.0.0.0.</span><span class="sxs-lookup"><span data-stu-id="b8c96-111">Version of the Global Positioning Systems (GPS) IFD, given as 2.0.0.0.</span></span> <span data-ttu-id="b8c96-112">Questo tag è obbligatorio quando è presente il tag PropertyTagGpsIFD.</span><span class="sxs-lookup"><span data-stu-id="b8c96-112">This tag is mandatory when the PropertyTagGpsIFD tag is present.</span></span> <span data-ttu-id="b8c96-113">Quando la versione è 2.0.0.0, il valore del tag è 0x02000000.</span><span class="sxs-lookup"><span data-stu-id="b8c96-113">When the version is 2.0.0.0, the tag value is 0x02000000.</span></span>



| <span data-ttu-id="b8c96-114">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-114">Property info</span></span> | <span data-ttu-id="b8c96-115">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-115">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="b8c96-116">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-116">Tag</span></span>   | <span data-ttu-id="b8c96-117">0x0000</span><span class="sxs-lookup"><span data-stu-id="b8c96-117">0x0000</span></span>              |
| <span data-ttu-id="b8c96-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-118">Type</span></span>  | <span data-ttu-id="b8c96-119">PropertyTagTypeByte</span><span class="sxs-lookup"><span data-stu-id="b8c96-119">PropertyTagTypeByte</span></span> |
| <span data-ttu-id="b8c96-120">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-120">Count</span></span> | <span data-ttu-id="b8c96-121">4</span><span class="sxs-lookup"><span data-stu-id="b8c96-121">4</span></span>                   |



 

## <a name="propertytaggpslatituderef"></a><span data-ttu-id="b8c96-122">PropertyTagGpsLatitudeRef</span><span class="sxs-lookup"><span data-stu-id="b8c96-122">PropertyTagGpsLatitudeRef</span></span>

<span data-ttu-id="b8c96-123">Stringa di caratteri con terminazione null che specifica se la latitudine è nord o sud.</span><span class="sxs-lookup"><span data-stu-id="b8c96-123">Null-terminated character string that specifies whether the latitude is north or south.</span></span> <span data-ttu-id="b8c96-124">`N` Specifica la latitudine nord e `S` specifica la latitudine sud.</span><span class="sxs-lookup"><span data-stu-id="b8c96-124">`N` specifies north latitude, and `S` specifies south latitude.</span></span>



| <span data-ttu-id="b8c96-125">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-125">Property info</span></span> | <span data-ttu-id="b8c96-126">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-126">Value</span></span> |
|-------|--------------------------------------------|
| <span data-ttu-id="b8c96-127">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-127">Tag</span></span>   | <span data-ttu-id="b8c96-128">0x0001</span><span class="sxs-lookup"><span data-stu-id="b8c96-128">0x0001</span></span>                                     |
| <span data-ttu-id="b8c96-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-129">Type</span></span>  | <span data-ttu-id="b8c96-130">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="b8c96-130">PropertyTagTypeASCII</span></span>                       |
| <span data-ttu-id="b8c96-131">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-131">Count</span></span> | <span data-ttu-id="b8c96-132">2 (un carattere più il carattere di terminazione NULL)</span><span class="sxs-lookup"><span data-stu-id="b8c96-132">2 (one character plus the NULL terminator)</span></span> |



 

## <a name="propertytaggpslatitude"></a><span data-ttu-id="b8c96-133">PropertyTagGpsLatitude</span><span class="sxs-lookup"><span data-stu-id="b8c96-133">PropertyTagGpsLatitude</span></span>

<span data-ttu-id="b8c96-134">Latitudine.</span><span class="sxs-lookup"><span data-stu-id="b8c96-134">Latitude.</span></span> <span data-ttu-id="b8c96-135">La latitudine è espressa come tre valori razionali che assegnano rispettivamente i gradi, i minuti e i secondi.</span><span class="sxs-lookup"><span data-stu-id="b8c96-135">Latitude is expressed as three rational values giving the degrees, minutes, and seconds respectively.</span></span> <span data-ttu-id="b8c96-136">Quando vengono espressi i gradi, i minuti e i secondi, il formato è gg/1, mm/1, SS/1.</span><span class="sxs-lookup"><span data-stu-id="b8c96-136">When degrees, minutes, and seconds are expressed, the format is dd/1, mm/1, ss/1.</span></span> <span data-ttu-id="b8c96-137">Quando vengono utilizzati gradi e minuti e, ad esempio, frazioni di minuti vengono assegnate fino a due posizioni decimali, il formato è DD/1, mmmm/100, 0/1.</span><span class="sxs-lookup"><span data-stu-id="b8c96-137">When degrees and minutes are used and, for example, fractions of minutes are given up to two decimal places, the format is dd/1, mmmm/100, 0/1.</span></span>



| <span data-ttu-id="b8c96-138">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-138">Property info</span></span> | <span data-ttu-id="b8c96-139">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-139">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="b8c96-140">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-140">Tag</span></span>   | <span data-ttu-id="b8c96-141">0x0002</span><span class="sxs-lookup"><span data-stu-id="b8c96-141">0x0002</span></span>                  |
| <span data-ttu-id="b8c96-142">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-142">Type</span></span>  | <span data-ttu-id="b8c96-143">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="b8c96-143">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="b8c96-144">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-144">Count</span></span> | <span data-ttu-id="b8c96-145">3</span><span class="sxs-lookup"><span data-stu-id="b8c96-145">3</span></span>                       |



 

## <a name="propertytaggpslongituderef"></a><span data-ttu-id="b8c96-146">PropertyTagGpsLongitudeRef</span><span class="sxs-lookup"><span data-stu-id="b8c96-146">PropertyTagGpsLongitudeRef</span></span>

<span data-ttu-id="b8c96-147">Stringa di caratteri con terminazione null che specifica se la longitudine è la longitudine est o ovest.</span><span class="sxs-lookup"><span data-stu-id="b8c96-147">Null-terminated character string that specifies whether the longitude is east or west longitude.</span></span> <span data-ttu-id="b8c96-148">`E` Specifica la longitudine est e `W` specifica la longitudine ovest.</span><span class="sxs-lookup"><span data-stu-id="b8c96-148">`E` specifies east longitude, and `W` specifies west longitude.</span></span>



| <span data-ttu-id="b8c96-149">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-149">Property info</span></span> | <span data-ttu-id="b8c96-150">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-150">Value</span></span> |
|-------|--------------------------------------------|
| <span data-ttu-id="b8c96-151">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-151">Tag</span></span>   | <span data-ttu-id="b8c96-152">0x0003</span><span class="sxs-lookup"><span data-stu-id="b8c96-152">0x0003</span></span>                                     |
| <span data-ttu-id="b8c96-153">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-153">Type</span></span>  | <span data-ttu-id="b8c96-154">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="b8c96-154">PropertyTagTypeASCII</span></span>                       |
| <span data-ttu-id="b8c96-155">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-155">Count</span></span> | <span data-ttu-id="b8c96-156">2 (un carattere più il carattere di terminazione NULL)</span><span class="sxs-lookup"><span data-stu-id="b8c96-156">2 (one character plus the NULL terminator)</span></span> |



 

## <a name="propertytaggpslongitude"></a><span data-ttu-id="b8c96-157">PropertyTagGpsLongitude</span><span class="sxs-lookup"><span data-stu-id="b8c96-157">PropertyTagGpsLongitude</span></span>

<span data-ttu-id="b8c96-158">Longitudine.</span><span class="sxs-lookup"><span data-stu-id="b8c96-158">Longitude.</span></span> <span data-ttu-id="b8c96-159">La longitudine è espressa come tre valori razionali che assegnano rispettivamente i gradi, i minuti e i secondi.</span><span class="sxs-lookup"><span data-stu-id="b8c96-159">Longitude is expressed as three rational values giving the degrees, minutes, and seconds respectively.</span></span> <span data-ttu-id="b8c96-160">Quando vengono espressi i gradi, i minuti e i secondi, il formato è DDD/1, mm/1, SS/1.</span><span class="sxs-lookup"><span data-stu-id="b8c96-160">When degrees, minutes and seconds are expressed, the format is ddd/1, mm/1, ss/1.</span></span> <span data-ttu-id="b8c96-161">Quando vengono utilizzati gradi e minuti e, ad esempio, frazioni di minuti vengono assegnate fino a due posizioni decimali, il formato è DDD/1, mmmm/100, 0/1.</span><span class="sxs-lookup"><span data-stu-id="b8c96-161">When degrees and minutes are used and, for example, fractions of minutes are given up to two decimal places, the format is ddd/1, mmmm/100, 0/1.</span></span>



| <span data-ttu-id="b8c96-162">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-162">Property info</span></span> | <span data-ttu-id="b8c96-163">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-163">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="b8c96-164">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-164">Tag</span></span>   | <span data-ttu-id="b8c96-165">0x0004</span><span class="sxs-lookup"><span data-stu-id="b8c96-165">0x0004</span></span>                  |
| <span data-ttu-id="b8c96-166">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-166">Type</span></span>  | <span data-ttu-id="b8c96-167">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="b8c96-167">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="b8c96-168">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-168">Count</span></span> | <span data-ttu-id="b8c96-169">3</span><span class="sxs-lookup"><span data-stu-id="b8c96-169">3</span></span>                       |



 

## <a name="propertytaggpsaltituderef"></a><span data-ttu-id="b8c96-170">PropertyTagGpsAltitudeRef</span><span class="sxs-lookup"><span data-stu-id="b8c96-170">PropertyTagGpsAltitudeRef</span></span>

<span data-ttu-id="b8c96-171">Altitudine di riferimento, in metri.</span><span class="sxs-lookup"><span data-stu-id="b8c96-171">Reference altitude, in meters.</span></span>



| <span data-ttu-id="b8c96-172">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-172">Property info</span></span> | <span data-ttu-id="b8c96-173">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-173">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="b8c96-174">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-174">Tag</span></span>   | <span data-ttu-id="b8c96-175">0x0005</span><span class="sxs-lookup"><span data-stu-id="b8c96-175">0x0005</span></span>              |
| <span data-ttu-id="b8c96-176">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-176">Type</span></span>  | <span data-ttu-id="b8c96-177">PropertyTagTypeByte</span><span class="sxs-lookup"><span data-stu-id="b8c96-177">PropertyTagTypeByte</span></span> |
| <span data-ttu-id="b8c96-178">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-178">Count</span></span> | <span data-ttu-id="b8c96-179">1</span><span class="sxs-lookup"><span data-stu-id="b8c96-179">1</span></span>                   |



 

## <a name="propertytaggpsaltitude"></a><span data-ttu-id="b8c96-180">PropertyTagGpsAltitude</span><span class="sxs-lookup"><span data-stu-id="b8c96-180">PropertyTagGpsAltitude</span></span>

<span data-ttu-id="b8c96-181">Altitudine, in metri, basata sull'altitudine di riferimento specificata da PropertyTagGpsAltitudeRef.</span><span class="sxs-lookup"><span data-stu-id="b8c96-181">Altitude, in meters, based on the reference altitude specified by PropertyTagGpsAltitudeRef.</span></span>



| <span data-ttu-id="b8c96-182">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-182">Property info</span></span> | <span data-ttu-id="b8c96-183">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-183">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="b8c96-184">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-184">Tag</span></span>   | <span data-ttu-id="b8c96-185">0x0006</span><span class="sxs-lookup"><span data-stu-id="b8c96-185">0x0006</span></span>                  |
| <span data-ttu-id="b8c96-186">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-186">Type</span></span>  | <span data-ttu-id="b8c96-187">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="b8c96-187">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="b8c96-188">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-188">Count</span></span> | <span data-ttu-id="b8c96-189">1</span><span class="sxs-lookup"><span data-stu-id="b8c96-189">1</span></span>                       |



 

## <a name="propertytaggpsgpstime"></a><span data-ttu-id="b8c96-190">PropertyTagGpsGpsTime</span><span class="sxs-lookup"><span data-stu-id="b8c96-190">PropertyTagGpsGpsTime</span></span>

<span data-ttu-id="b8c96-191">Ora UTC (Coordinated Universal Time).</span><span class="sxs-lookup"><span data-stu-id="b8c96-191">Time as Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="b8c96-192">Il valore viene espresso come tre numeri razionali che forniscono l'ora, il minuto e il secondo.</span><span class="sxs-lookup"><span data-stu-id="b8c96-192">The value is expressed as three rational numbers that give the hour, minute, and second.</span></span>



| <span data-ttu-id="b8c96-193">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-193">Property info</span></span> | <span data-ttu-id="b8c96-194">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-194">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="b8c96-195">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-195">Tag</span></span>   | <span data-ttu-id="b8c96-196">0x0007</span><span class="sxs-lookup"><span data-stu-id="b8c96-196">0x0007</span></span>                  |
| <span data-ttu-id="b8c96-197">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-197">Type</span></span>  | <span data-ttu-id="b8c96-198">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="b8c96-198">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="b8c96-199">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-199">Count</span></span> | <span data-ttu-id="b8c96-200">3</span><span class="sxs-lookup"><span data-stu-id="b8c96-200">3</span></span>                       |



 

## <a name="propertytaggpsgpssatellites"></a><span data-ttu-id="b8c96-201">PropertyTagGpsGpsSatellites</span><span class="sxs-lookup"><span data-stu-id="b8c96-201">PropertyTagGpsGpsSatellites</span></span>

<span data-ttu-id="b8c96-202">Stringa di caratteri con terminazione null che specifica i satelliti GPS usati per le misurazioni.</span><span class="sxs-lookup"><span data-stu-id="b8c96-202">Null-terminated character string that specifies the GPS satellites used for measurements.</span></span> <span data-ttu-id="b8c96-203">Questo tag può essere usato per specificare il numero di ID, l'angolo di elevazione, Azimut, SNR e altre informazioni su ogni satellite.</span><span class="sxs-lookup"><span data-stu-id="b8c96-203">This tag can be used to specify the ID number, angle of elevation, azimuth, SNR, and other information about each satellite.</span></span> <span data-ttu-id="b8c96-204">Il formato non è specificato.</span><span class="sxs-lookup"><span data-stu-id="b8c96-204">The format is not specified.</span></span> <span data-ttu-id="b8c96-205">Se il ricevitore GPS non è in grado di eseguire misure, il valore del tag deve essere impostato su **null**.</span><span class="sxs-lookup"><span data-stu-id="b8c96-205">If the GPS receiver is incapable of taking measurements, the value of the tag must be set to **NULL**.</span></span>



| <span data-ttu-id="b8c96-206">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-206">Property info</span></span> | <span data-ttu-id="b8c96-207">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-207">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="b8c96-208">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-208">Tag</span></span>   | <span data-ttu-id="b8c96-209">0x0008</span><span class="sxs-lookup"><span data-stu-id="b8c96-209">0x0008</span></span>                                             |
| <span data-ttu-id="b8c96-210">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-210">Type</span></span>  | <span data-ttu-id="b8c96-211">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="b8c96-211">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="b8c96-212">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-212">Count</span></span> | <span data-ttu-id="b8c96-213">Lunghezza della stringa che include il carattere di terminazione NULL</span><span class="sxs-lookup"><span data-stu-id="b8c96-213">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytaggpsgpsstatus"></a><span data-ttu-id="b8c96-214">PropertyTagGpsGpsStatus</span><span class="sxs-lookup"><span data-stu-id="b8c96-214">PropertyTagGpsGpsStatus</span></span>

<span data-ttu-id="b8c96-215">Stringa di caratteri con terminazione null che specifica lo stato del ricevitore GPS quando l'immagine viene registrata.</span><span class="sxs-lookup"><span data-stu-id="b8c96-215">Null-terminated character string that specifies the status of the GPS receiver when the image is recorded.</span></span> <span data-ttu-id="b8c96-216">`A` indica che la misurazione è in corso e `V` indica che la misura è interoperabilità.</span><span class="sxs-lookup"><span data-stu-id="b8c96-216">`A` means measurement is in progress, and `V` means the measurement is Interoperability.</span></span>



| <span data-ttu-id="b8c96-217">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-217">Property info</span></span> | <span data-ttu-id="b8c96-218">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-218">Value</span></span> |
|-------|--------------------------------------------|
| <span data-ttu-id="b8c96-219">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-219">Tag</span></span>   | <span data-ttu-id="b8c96-220">0x0009</span><span class="sxs-lookup"><span data-stu-id="b8c96-220">0x0009</span></span>                                     |
| <span data-ttu-id="b8c96-221">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-221">Type</span></span>  | <span data-ttu-id="b8c96-222">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="b8c96-222">PropertyTagTypeASCII</span></span>                       |
| <span data-ttu-id="b8c96-223">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-223">Count</span></span> | <span data-ttu-id="b8c96-224">2 (un carattere più il carattere di terminazione NULL)</span><span class="sxs-lookup"><span data-stu-id="b8c96-224">2 (one character plus the NULL terminator)</span></span> |



 

## <a name="propertytaggpsgpsmeasuremode"></a><span data-ttu-id="b8c96-225">PropertyTagGpsGpsMeasureMode</span><span class="sxs-lookup"><span data-stu-id="b8c96-225">PropertyTagGpsGpsMeasureMode</span></span>

<span data-ttu-id="b8c96-226">Stringa di caratteri con terminazione null che specifica la modalità di misurazione GPS.</span><span class="sxs-lookup"><span data-stu-id="b8c96-226">Null-terminated character string that specifies the GPS measurement mode.</span></span> <span data-ttu-id="b8c96-227">`2` Specifica la misurazione 2D e specifica la `3` misurazione 3D.</span><span class="sxs-lookup"><span data-stu-id="b8c96-227">`2` specifies 2-D measurement, and `3` specifies 3-D measurement.</span></span>



| <span data-ttu-id="b8c96-228">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-228">Property info</span></span> | <span data-ttu-id="b8c96-229">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-229">Value</span></span> |
|-------|--------------------------------------------|
| <span data-ttu-id="b8c96-230">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-230">Tag</span></span>   | <span data-ttu-id="b8c96-231">0x000A</span><span class="sxs-lookup"><span data-stu-id="b8c96-231">0x000A</span></span>                                     |
| <span data-ttu-id="b8c96-232">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-232">Type</span></span>  | <span data-ttu-id="b8c96-233">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="b8c96-233">PropertyTagTypeASCII</span></span>                       |
| <span data-ttu-id="b8c96-234">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-234">Count</span></span> | <span data-ttu-id="b8c96-235">2 (un carattere più il carattere di terminazione NULL)</span><span class="sxs-lookup"><span data-stu-id="b8c96-235">2 (one character plus the NULL terminator)</span></span> |



 

## <a name="propertytaggpsgpsdop"></a><span data-ttu-id="b8c96-236">PropertyTagGpsGpsDop</span><span class="sxs-lookup"><span data-stu-id="b8c96-236">PropertyTagGpsGpsDop</span></span>

<span data-ttu-id="b8c96-237">DOP GPS (grado di precisione dei dati).</span><span class="sxs-lookup"><span data-stu-id="b8c96-237">GPS DOP (data degree of precision).</span></span> <span data-ttu-id="b8c96-238">Un valore HDOP viene scritto durante la misurazione 2D e viene scritto un valore PDOP durante la misurazione 3D.</span><span class="sxs-lookup"><span data-stu-id="b8c96-238">An HDOP value is written during 2-D measurement, and a PDOP value is written during 3-D measurement.</span></span>



| <span data-ttu-id="b8c96-239">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-239">Property info</span></span> | <span data-ttu-id="b8c96-240">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-240">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="b8c96-241">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-241">Tag</span></span>   | <span data-ttu-id="b8c96-242">0x000B</span><span class="sxs-lookup"><span data-stu-id="b8c96-242">0x000B</span></span>                  |
| <span data-ttu-id="b8c96-243">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-243">Type</span></span>  | <span data-ttu-id="b8c96-244">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="b8c96-244">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="b8c96-245">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-245">Count</span></span> | <span data-ttu-id="b8c96-246">1</span><span class="sxs-lookup"><span data-stu-id="b8c96-246">1</span></span>                       |



 

## <a name="propertytaggpsspeedref"></a><span data-ttu-id="b8c96-247">PropertyTagGpsSpeedRef</span><span class="sxs-lookup"><span data-stu-id="b8c96-247">PropertyTagGpsSpeedRef</span></span>

<span data-ttu-id="b8c96-248">Stringa di caratteri con terminazione null che specifica l'unità utilizzata per esprimere la velocità di spostamento del ricevitore GPS.</span><span class="sxs-lookup"><span data-stu-id="b8c96-248">Null-terminated character string that specifies the unit used to express the GPS receiver speed of movement.</span></span> <span data-ttu-id="b8c96-249">`K`, `M` e `N` rappresentano rispettivamente i chilometri all'ora, le miglia all'ora e i nodi.</span><span class="sxs-lookup"><span data-stu-id="b8c96-249">`K`, `M`, and `N` represent kilometers per hour, miles per hour, and knots respectively.</span></span>



| <span data-ttu-id="b8c96-250">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-250">Property info</span></span> | <span data-ttu-id="b8c96-251">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-251">Value</span></span> |
|-------|--------------------------------------------|
| <span data-ttu-id="b8c96-252">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-252">Tag</span></span>   | <span data-ttu-id="b8c96-253">0x000C</span><span class="sxs-lookup"><span data-stu-id="b8c96-253">0x000C</span></span>                                     |
| <span data-ttu-id="b8c96-254">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-254">Type</span></span>  | <span data-ttu-id="b8c96-255">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="b8c96-255">PropertyTagTypeASCII</span></span>                       |
| <span data-ttu-id="b8c96-256">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-256">Count</span></span> | <span data-ttu-id="b8c96-257">2 (un carattere più il carattere di terminazione NULL)</span><span class="sxs-lookup"><span data-stu-id="b8c96-257">2 (one character plus the NULL terminator)</span></span> |



 

## <a name="propertytaggpsspeed"></a><span data-ttu-id="b8c96-258">PropertyTagGpsSpeed</span><span class="sxs-lookup"><span data-stu-id="b8c96-258">PropertyTagGpsSpeed</span></span>

<span data-ttu-id="b8c96-259">Velocità di spostamento del ricevitore GPS.</span><span class="sxs-lookup"><span data-stu-id="b8c96-259">Speed of the GPS receiver movement.</span></span>



| <span data-ttu-id="b8c96-260">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-260">Property info</span></span> | <span data-ttu-id="b8c96-261">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-261">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="b8c96-262">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-262">Tag</span></span>   | <span data-ttu-id="b8c96-263">0x000D</span><span class="sxs-lookup"><span data-stu-id="b8c96-263">0x000D</span></span>                  |
| <span data-ttu-id="b8c96-264">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-264">Type</span></span>  | <span data-ttu-id="b8c96-265">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="b8c96-265">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="b8c96-266">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-266">Count</span></span> | <span data-ttu-id="b8c96-267">1</span><span class="sxs-lookup"><span data-stu-id="b8c96-267">1</span></span>                       |



 

## <a name="propertytaggpstrackref"></a><span data-ttu-id="b8c96-268">PropertyTagGpsTrackRef</span><span class="sxs-lookup"><span data-stu-id="b8c96-268">PropertyTagGpsTrackRef</span></span>

<span data-ttu-id="b8c96-269">Stringa di caratteri con terminazione null che specifica il riferimento per fornire la direzione dello spostamento del ricevitore GPS.</span><span class="sxs-lookup"><span data-stu-id="b8c96-269">Null-terminated character string that specifies the reference for giving the direction of GPS receiver movement.</span></span> <span data-ttu-id="b8c96-270">`T` Specifica la direzione vera e `M` specifica la direzione magnetica.</span><span class="sxs-lookup"><span data-stu-id="b8c96-270">`T` specifies true direction, and `M` specifies magnetic direction.</span></span>



| <span data-ttu-id="b8c96-271">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-271">Property info</span></span> | <span data-ttu-id="b8c96-272">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-272">Value</span></span> |
|-------|--------------------------------------------|
| <span data-ttu-id="b8c96-273">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-273">Tag</span></span>   | <span data-ttu-id="b8c96-274">0x000E</span><span class="sxs-lookup"><span data-stu-id="b8c96-274">0x000E</span></span>                                     |
| <span data-ttu-id="b8c96-275">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-275">Type</span></span>  | <span data-ttu-id="b8c96-276">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="b8c96-276">PropertyTagTypeASCII</span></span>                       |
| <span data-ttu-id="b8c96-277">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-277">Count</span></span> | <span data-ttu-id="b8c96-278">2 (un carattere più il carattere di terminazione NULL)</span><span class="sxs-lookup"><span data-stu-id="b8c96-278">2 (one character plus the NULL terminator)</span></span> |



 

## <a name="propertytaggpstrack"></a><span data-ttu-id="b8c96-279">PropertyTagGpsTrack</span><span class="sxs-lookup"><span data-stu-id="b8c96-279">PropertyTagGpsTrack</span></span>

<span data-ttu-id="b8c96-280">Direzione dello spostamento del ricevitore GPS.</span><span class="sxs-lookup"><span data-stu-id="b8c96-280">Direction of GPS receiver movement.</span></span> <span data-ttu-id="b8c96-281">L'intervallo di valori è compreso tra 0,00 e 359,99.</span><span class="sxs-lookup"><span data-stu-id="b8c96-281">The range of values is from 0.00 to 359.99.</span></span>



| <span data-ttu-id="b8c96-282">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-282">Property info</span></span> | <span data-ttu-id="b8c96-283">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-283">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="b8c96-284">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-284">Tag</span></span>   | <span data-ttu-id="b8c96-285">0x000F</span><span class="sxs-lookup"><span data-stu-id="b8c96-285">0x000F</span></span>                  |
| <span data-ttu-id="b8c96-286">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-286">Type</span></span>  | <span data-ttu-id="b8c96-287">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="b8c96-287">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="b8c96-288">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-288">Count</span></span> | <span data-ttu-id="b8c96-289">1</span><span class="sxs-lookup"><span data-stu-id="b8c96-289">1</span></span>                       |



 

## <a name="propertytaggpsimgdirref"></a><span data-ttu-id="b8c96-290">PropertyTagGpsImgDirRef</span><span class="sxs-lookup"><span data-stu-id="b8c96-290">PropertyTagGpsImgDirRef</span></span>

<span data-ttu-id="b8c96-291">Stringa di caratteri con terminazione null che specifica il riferimento per la direzione dell'immagine quando viene acquisita.</span><span class="sxs-lookup"><span data-stu-id="b8c96-291">Null-terminated character string that specifies the reference for the direction of the image when it is captured.</span></span> <span data-ttu-id="b8c96-292">`T` Specifica la direzione vera e `M` specifica la direzione magnetica.</span><span class="sxs-lookup"><span data-stu-id="b8c96-292">`T` specifies true direction, and `M` specifies magnetic direction.</span></span>



| <span data-ttu-id="b8c96-293">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-293">Property info</span></span> | <span data-ttu-id="b8c96-294">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-294">Value</span></span> |
|-------|--------------------------------------------|
| <span data-ttu-id="b8c96-295">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-295">Tag</span></span>   | <span data-ttu-id="b8c96-296">0x0010</span><span class="sxs-lookup"><span data-stu-id="b8c96-296">0x0010</span></span>                                     |
| <span data-ttu-id="b8c96-297">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-297">Type</span></span>  | <span data-ttu-id="b8c96-298">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="b8c96-298">PropertyTagTypeASCII</span></span>                       |
| <span data-ttu-id="b8c96-299">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-299">Count</span></span> | <span data-ttu-id="b8c96-300">2 (un carattere più il carattere di terminazione NULL)</span><span class="sxs-lookup"><span data-stu-id="b8c96-300">2 (one character plus the NULL terminator)</span></span> |



 

## <a name="propertytaggpsimgdir"></a><span data-ttu-id="b8c96-301">PropertyTagGpsImgDir</span><span class="sxs-lookup"><span data-stu-id="b8c96-301">PropertyTagGpsImgDir</span></span>

<span data-ttu-id="b8c96-302">Direzione dell'immagine al momento dell'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="b8c96-302">Direction of the image when it was captured.</span></span> <span data-ttu-id="b8c96-303">L'intervallo di valori è compreso tra 0,00 e 359,99.</span><span class="sxs-lookup"><span data-stu-id="b8c96-303">The range of values is from 0.00 to 359.99.</span></span>



| <span data-ttu-id="b8c96-304">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-304">Property info</span></span> | <span data-ttu-id="b8c96-305">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-305">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="b8c96-306">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-306">Tag</span></span>   | <span data-ttu-id="b8c96-307">0x0011</span><span class="sxs-lookup"><span data-stu-id="b8c96-307">0x0011</span></span>                  |
| <span data-ttu-id="b8c96-308">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-308">Type</span></span>  | <span data-ttu-id="b8c96-309">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="b8c96-309">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="b8c96-310">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-310">Count</span></span> | <span data-ttu-id="b8c96-311">1</span><span class="sxs-lookup"><span data-stu-id="b8c96-311">1</span></span>                       |



 

## <a name="propertytaggpsmapdatum"></a><span data-ttu-id="b8c96-312">PropertyTagGpsMapDatum</span><span class="sxs-lookup"><span data-stu-id="b8c96-312">PropertyTagGpsMapDatum</span></span>

<span data-ttu-id="b8c96-313">Stringa di caratteri con terminazione null che specifica i dati del sondaggio geodetici utilizzati dal ricevitore GPS.</span><span class="sxs-lookup"><span data-stu-id="b8c96-313">Null-terminated character string that specifies geodetic survey data used by the GPS receiver.</span></span> <span data-ttu-id="b8c96-314">Se i dati del sondaggio sono limitati al Giappone, il valore di questo tag è `TOKYO` o `WGS-84` .</span><span class="sxs-lookup"><span data-stu-id="b8c96-314">If the survey data is restricted to Japan, the value of this tag is `TOKYO` or `WGS-84`.</span></span>



| <span data-ttu-id="b8c96-315">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-315">Property info</span></span> | <span data-ttu-id="b8c96-316">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-316">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="b8c96-317">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-317">Tag</span></span>   | <span data-ttu-id="b8c96-318">0x0012</span><span class="sxs-lookup"><span data-stu-id="b8c96-318">0x0012</span></span>                                             |
| <span data-ttu-id="b8c96-319">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-319">Type</span></span>  | <span data-ttu-id="b8c96-320">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="b8c96-320">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="b8c96-321">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-321">Count</span></span> | <span data-ttu-id="b8c96-322">Lunghezza della stringa che include il carattere di terminazione NULL</span><span class="sxs-lookup"><span data-stu-id="b8c96-322">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytaggpsdestlatref"></a><span data-ttu-id="b8c96-323">PropertyTagGpsDestLatRef</span><span class="sxs-lookup"><span data-stu-id="b8c96-323">PropertyTagGpsDestLatRef</span></span>

<span data-ttu-id="b8c96-324">Stringa di caratteri con terminazione null che specifica se la latitudine del punto di destinazione è la latitudine nord o sud.</span><span class="sxs-lookup"><span data-stu-id="b8c96-324">Null-terminated character string that specifies whether the latitude of the destination point is north or south latitude.</span></span> <span data-ttu-id="b8c96-325">`N` Specifica la latitudine nord e `S` specifica la latitudine sud.</span><span class="sxs-lookup"><span data-stu-id="b8c96-325">`N` specifies north latitude, and `S` specifies south latitude.</span></span>



| <span data-ttu-id="b8c96-326">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-326">Property info</span></span> | <span data-ttu-id="b8c96-327">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-327">Value</span></span> |
|-------|--------------------------------------------|
| <span data-ttu-id="b8c96-328">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-328">Tag</span></span>   | <span data-ttu-id="b8c96-329">0x0013</span><span class="sxs-lookup"><span data-stu-id="b8c96-329">0x0013</span></span>                                     |
| <span data-ttu-id="b8c96-330">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-330">Type</span></span>  | <span data-ttu-id="b8c96-331">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="b8c96-331">PropertyTagTypeASCII</span></span>                       |
| <span data-ttu-id="b8c96-332">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-332">Count</span></span> | <span data-ttu-id="b8c96-333">2 (un carattere più il carattere di terminazione NULL)</span><span class="sxs-lookup"><span data-stu-id="b8c96-333">2 (one character plus the NULL terminator)</span></span> |



 

## <a name="propertytaggpsdestlat"></a><span data-ttu-id="b8c96-334">PropertyTagGpsDestLat</span><span class="sxs-lookup"><span data-stu-id="b8c96-334">PropertyTagGpsDestLat</span></span>

<span data-ttu-id="b8c96-335">Latitudine del punto di destinazione.</span><span class="sxs-lookup"><span data-stu-id="b8c96-335">Latitude of the destination point.</span></span> <span data-ttu-id="b8c96-336">La latitudine è espressa come tre valori razionali che assegnano rispettivamente i gradi, i minuti e i secondi.</span><span class="sxs-lookup"><span data-stu-id="b8c96-336">The latitude is expressed as three rational values giving the degrees, minutes, and seconds respectively.</span></span> <span data-ttu-id="b8c96-337">Quando vengono espressi i gradi, i minuti e i secondi, il formato è gg/1, mm/1, SS/1.</span><span class="sxs-lookup"><span data-stu-id="b8c96-337">When degrees, minutes, and seconds are expressed, the format is dd/1, mm/1, ss/1.</span></span> <span data-ttu-id="b8c96-338">Quando vengono utilizzati gradi e minuti e, ad esempio, frazioni di minuti vengono assegnate fino a due posizioni decimali, il formato è DD/1, mmmm/100, 0/1.</span><span class="sxs-lookup"><span data-stu-id="b8c96-338">When degrees and minutes are used and, for example, fractions of minutes are given up to two decimal places, the format is dd/1, mmmm/100, 0/1.</span></span>



| <span data-ttu-id="b8c96-339">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-339">Property info</span></span> | <span data-ttu-id="b8c96-340">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-340">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="b8c96-341">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-341">Tag</span></span>   | <span data-ttu-id="b8c96-342">0x0014</span><span class="sxs-lookup"><span data-stu-id="b8c96-342">0x0014</span></span>                  |
| <span data-ttu-id="b8c96-343">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-343">Type</span></span>  | <span data-ttu-id="b8c96-344">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="b8c96-344">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="b8c96-345">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-345">Count</span></span> | <span data-ttu-id="b8c96-346">3</span><span class="sxs-lookup"><span data-stu-id="b8c96-346">3</span></span>                       |



 

## <a name="propertytaggpsdestlongref"></a><span data-ttu-id="b8c96-347">PropertyTagGpsDestLongRef</span><span class="sxs-lookup"><span data-stu-id="b8c96-347">PropertyTagGpsDestLongRef</span></span>

<span data-ttu-id="b8c96-348">Stringa di caratteri con terminazione null che specifica se la longitudine del punto di destinazione è la longitudine est o ovest.</span><span class="sxs-lookup"><span data-stu-id="b8c96-348">Null-terminated character string that specifies whether the longitude of the destination point is east or west longitude.</span></span> <span data-ttu-id="b8c96-349">`E` Specifica la longitudine est e `W` specifica la longitudine ovest.</span><span class="sxs-lookup"><span data-stu-id="b8c96-349">`E` specifies east longitude, and `W` specifies west longitude.</span></span>



| <span data-ttu-id="b8c96-350">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-350">Property info</span></span> | <span data-ttu-id="b8c96-351">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-351">Value</span></span> |
|-------|--------------------------------------------|
| <span data-ttu-id="b8c96-352">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-352">Tag</span></span>   | <span data-ttu-id="b8c96-353">0x0015</span><span class="sxs-lookup"><span data-stu-id="b8c96-353">0x0015</span></span>                                     |
| <span data-ttu-id="b8c96-354">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-354">Type</span></span>  | <span data-ttu-id="b8c96-355">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="b8c96-355">PropertyTagTypeASCII</span></span>                       |
| <span data-ttu-id="b8c96-356">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-356">Count</span></span> | <span data-ttu-id="b8c96-357">2 (un carattere più il carattere di terminazione NULL)</span><span class="sxs-lookup"><span data-stu-id="b8c96-357">2 (one character plus the NULL terminator)</span></span> |



 

## <a name="propertytaggpsdestlong"></a><span data-ttu-id="b8c96-358">PropertyTagGpsDestLong</span><span class="sxs-lookup"><span data-stu-id="b8c96-358">PropertyTagGpsDestLong</span></span>

<span data-ttu-id="b8c96-359">Longitudine del punto di destinazione.</span><span class="sxs-lookup"><span data-stu-id="b8c96-359">Longitude of the destination point.</span></span> <span data-ttu-id="b8c96-360">La longitudine è espressa come tre valori razionali che assegnano rispettivamente i gradi, i minuti e i secondi.</span><span class="sxs-lookup"><span data-stu-id="b8c96-360">The longitude is expressed as three rational values giving the degrees, minutes, and seconds respectively.</span></span> <span data-ttu-id="b8c96-361">Quando vengono espressi i gradi, i minuti e i secondi, il formato è DDD/1, mm/1, SS/1.</span><span class="sxs-lookup"><span data-stu-id="b8c96-361">When degrees, minutes, and seconds are expressed, the format is ddd/1, mm/1, ss/1.</span></span> <span data-ttu-id="b8c96-362">Quando vengono utilizzati gradi e minuti e, ad esempio, frazioni di minuti vengono assegnate fino a due posizioni decimali, il formato è DDD/1, mmmm/100, 0/1.</span><span class="sxs-lookup"><span data-stu-id="b8c96-362">When degrees and minutes are used and, for example, fractions of minutes are given up to two decimal places, the format is ddd/1, mmmm/100, 0/1.</span></span>



| <span data-ttu-id="b8c96-363">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-363">Property info</span></span> | <span data-ttu-id="b8c96-364">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-364">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="b8c96-365">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-365">Tag</span></span>   | <span data-ttu-id="b8c96-366">0x0016</span><span class="sxs-lookup"><span data-stu-id="b8c96-366">0x0016</span></span>                  |
| <span data-ttu-id="b8c96-367">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-367">Type</span></span>  | <span data-ttu-id="b8c96-368">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="b8c96-368">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="b8c96-369">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-369">Count</span></span> | <span data-ttu-id="b8c96-370">3</span><span class="sxs-lookup"><span data-stu-id="b8c96-370">3</span></span>                       |



 

## <a name="propertytaggpsdestbearref"></a><span data-ttu-id="b8c96-371">PropertyTagGpsDestBearRef</span><span class="sxs-lookup"><span data-stu-id="b8c96-371">PropertyTagGpsDestBearRef</span></span>

<span data-ttu-id="b8c96-372">Stringa di caratteri con terminazione null che specifica il riferimento usato per assegnare il cuscinetto al punto di destinazione.</span><span class="sxs-lookup"><span data-stu-id="b8c96-372">Null-terminated character string that specifies the reference used for giving the bearing to the destination point.</span></span> <span data-ttu-id="b8c96-373">`T` Specifica la direzione vera e `M` specifica la direzione magnetica.</span><span class="sxs-lookup"><span data-stu-id="b8c96-373">`T` specifies true direction, and `M` specifies magnetic direction.</span></span>



| <span data-ttu-id="b8c96-374">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-374">Property info</span></span> | <span data-ttu-id="b8c96-375">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-375">Value</span></span> |
|-------|--------------------------------------------|
| <span data-ttu-id="b8c96-376">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-376">Tag</span></span>   | <span data-ttu-id="b8c96-377">0x0017</span><span class="sxs-lookup"><span data-stu-id="b8c96-377">0x0017</span></span>                                     |
| <span data-ttu-id="b8c96-378">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-378">Type</span></span>  | <span data-ttu-id="b8c96-379">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="b8c96-379">PropertyTagTypeASCII</span></span>                       |
| <span data-ttu-id="b8c96-380">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-380">Count</span></span> | <span data-ttu-id="b8c96-381">2 (un carattere più il carattere di terminazione NULL)</span><span class="sxs-lookup"><span data-stu-id="b8c96-381">2 (one character plus the NULL terminator)</span></span> |



 

## <a name="propertytaggpsdestbear"></a><span data-ttu-id="b8c96-382">PropertyTagGpsDestBear</span><span class="sxs-lookup"><span data-stu-id="b8c96-382">PropertyTagGpsDestBear</span></span>

<span data-ttu-id="b8c96-383">Che comportano il punto di destinazione.</span><span class="sxs-lookup"><span data-stu-id="b8c96-383">Bearing to the destination point.</span></span> <span data-ttu-id="b8c96-384">L'intervallo di valori è compreso tra 0,00 e 359,99.</span><span class="sxs-lookup"><span data-stu-id="b8c96-384">The range of values is from 0.00 to 359.99.</span></span>



| <span data-ttu-id="b8c96-385">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-385">Property info</span></span> | <span data-ttu-id="b8c96-386">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-386">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="b8c96-387">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-387">Tag</span></span>   | <span data-ttu-id="b8c96-388">0x0018</span><span class="sxs-lookup"><span data-stu-id="b8c96-388">0x0018</span></span>                  |
| <span data-ttu-id="b8c96-389">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-389">Type</span></span>  | <span data-ttu-id="b8c96-390">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="b8c96-390">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="b8c96-391">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-391">Count</span></span> | <span data-ttu-id="b8c96-392">1</span><span class="sxs-lookup"><span data-stu-id="b8c96-392">1</span></span>                       |



 

## <a name="propertytaggpsdestdistref"></a><span data-ttu-id="b8c96-393">PropertyTagGpsDestDistRef</span><span class="sxs-lookup"><span data-stu-id="b8c96-393">PropertyTagGpsDestDistRef</span></span>

<span data-ttu-id="b8c96-394">Stringa di caratteri con terminazione null che specifica l'unità utilizzata per esprimere la distanza al punto di destinazione.</span><span class="sxs-lookup"><span data-stu-id="b8c96-394">Null-terminated character string that specifies the unit used to express the distance to the destination point.</span></span> <span data-ttu-id="b8c96-395">K, M e N rappresentano rispettivamente i chilometri, le miglia e i nodi.</span><span class="sxs-lookup"><span data-stu-id="b8c96-395">K, M, and N represent kilometers, miles, and knots respectively.</span></span>



| <span data-ttu-id="b8c96-396">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-396">Property info</span></span> | <span data-ttu-id="b8c96-397">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-397">Value</span></span> |
|-------|--------------------------------------------|
| <span data-ttu-id="b8c96-398">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-398">Tag</span></span>   | <span data-ttu-id="b8c96-399">0x0019</span><span class="sxs-lookup"><span data-stu-id="b8c96-399">0x0019</span></span>                                     |
| <span data-ttu-id="b8c96-400">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-400">Type</span></span>  | <span data-ttu-id="b8c96-401">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="b8c96-401">PropertyTagTypeASCII</span></span>                       |
| <span data-ttu-id="b8c96-402">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-402">Count</span></span> | <span data-ttu-id="b8c96-403">2 (un carattere più il carattere di terminazione NULL)</span><span class="sxs-lookup"><span data-stu-id="b8c96-403">2 (one character plus the NULL terminator)</span></span> |



 

## <a name="propertytaggpsdestdist"></a><span data-ttu-id="b8c96-404">PropertyTagGpsDestDist</span><span class="sxs-lookup"><span data-stu-id="b8c96-404">PropertyTagGpsDestDist</span></span>

<span data-ttu-id="b8c96-405">Distanza al punto di destinazione.</span><span class="sxs-lookup"><span data-stu-id="b8c96-405">Distance to the destination point.</span></span>



| <span data-ttu-id="b8c96-406">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-406">Property info</span></span> | <span data-ttu-id="b8c96-407">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-407">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="b8c96-408">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-408">Tag</span></span>   | <span data-ttu-id="b8c96-409">0x001A</span><span class="sxs-lookup"><span data-stu-id="b8c96-409">0x001A</span></span>                  |
| <span data-ttu-id="b8c96-410">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-410">Type</span></span>  | <span data-ttu-id="b8c96-411">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="b8c96-411">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="b8c96-412">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-412">Count</span></span> | <span data-ttu-id="b8c96-413">1</span><span class="sxs-lookup"><span data-stu-id="b8c96-413">1</span></span>                       |



 

## <a name="propertytagnewsubfiletype"></a><span data-ttu-id="b8c96-414">PropertyTagNewSubfileType</span><span class="sxs-lookup"><span data-stu-id="b8c96-414">PropertyTagNewSubfileType</span></span>

<span data-ttu-id="b8c96-415">Tipo di dati in un file di dati.</span><span class="sxs-lookup"><span data-stu-id="b8c96-415">Type of data in a subfile.</span></span>



| <span data-ttu-id="b8c96-416">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-416">Property info</span></span> | <span data-ttu-id="b8c96-417">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-417">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="b8c96-418">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-418">Tag</span></span>   | <span data-ttu-id="b8c96-419">0x00FE</span><span class="sxs-lookup"><span data-stu-id="b8c96-419">0x00FE</span></span>              |
| <span data-ttu-id="b8c96-420">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-420">Type</span></span>  | <span data-ttu-id="b8c96-421">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="b8c96-421">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="b8c96-422">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-422">Count</span></span> | <span data-ttu-id="b8c96-423">1</span><span class="sxs-lookup"><span data-stu-id="b8c96-423">1</span></span>                   |



 

## <a name="propertytagsubfiletype"></a><span data-ttu-id="b8c96-424">PropertyTagSubfileType</span><span class="sxs-lookup"><span data-stu-id="b8c96-424">PropertyTagSubfileType</span></span>

<span data-ttu-id="b8c96-425">Tipo di dati in un file di dati.</span><span class="sxs-lookup"><span data-stu-id="b8c96-425">Type of data in a subfile.</span></span>



| <span data-ttu-id="b8c96-426">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-426">Property info</span></span> | <span data-ttu-id="b8c96-427">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-427">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="b8c96-428">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-428">Tag</span></span>   | <span data-ttu-id="b8c96-429">0x00FF</span><span class="sxs-lookup"><span data-stu-id="b8c96-429">0x00FF</span></span>               |
| <span data-ttu-id="b8c96-430">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-430">Type</span></span>  | <span data-ttu-id="b8c96-431">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="b8c96-431">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="b8c96-432">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-432">Count</span></span> | <span data-ttu-id="b8c96-433">1</span><span class="sxs-lookup"><span data-stu-id="b8c96-433">1</span></span>                    |



 

## <a name="propertytagimagewidth"></a><span data-ttu-id="b8c96-434">PropertyTagImageWidth</span><span class="sxs-lookup"><span data-stu-id="b8c96-434">PropertyTagImageWidth</span></span>

<span data-ttu-id="b8c96-435">Numero di pixel per riga.</span><span class="sxs-lookup"><span data-stu-id="b8c96-435">Number of pixels per row.</span></span>



| <span data-ttu-id="b8c96-436">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-436">Property info</span></span> | <span data-ttu-id="b8c96-437">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-437">Value</span></span> |
|-------|---------------------------------------------|
| <span data-ttu-id="b8c96-438">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-438">Tag</span></span>   | <span data-ttu-id="b8c96-439">0x0100</span><span class="sxs-lookup"><span data-stu-id="b8c96-439">0x0100</span></span>                                      |
| <span data-ttu-id="b8c96-440">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-440">Type</span></span>  | <span data-ttu-id="b8c96-441">PropertyTagTypeShort o PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="b8c96-441">PropertyTagTypeShort or PropertyTagTypeLong</span></span> |
| <span data-ttu-id="b8c96-442">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-442">Count</span></span> | <span data-ttu-id="b8c96-443">1</span><span class="sxs-lookup"><span data-stu-id="b8c96-443">1</span></span>                                           |



 

## <a name="propertytagimageheight"></a><span data-ttu-id="b8c96-444">PropertyTagImageHeight</span><span class="sxs-lookup"><span data-stu-id="b8c96-444">PropertyTagImageHeight</span></span>

<span data-ttu-id="b8c96-445">Numero di righe in pixel.</span><span class="sxs-lookup"><span data-stu-id="b8c96-445">Number of pixel rows.</span></span>



| <span data-ttu-id="b8c96-446">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-446">Property info</span></span> | <span data-ttu-id="b8c96-447">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-447">Value</span></span> |
|-------|---------------------------------------------|
| <span data-ttu-id="b8c96-448">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-448">Tag</span></span>   | <span data-ttu-id="b8c96-449">0x0101</span><span class="sxs-lookup"><span data-stu-id="b8c96-449">0x0101</span></span>                                      |
| <span data-ttu-id="b8c96-450">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-450">Type</span></span>  | <span data-ttu-id="b8c96-451">PropertyTagTypeShort o PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="b8c96-451">PropertyTagTypeShort or PropertyTagTypeLong</span></span> |
| <span data-ttu-id="b8c96-452">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-452">Count</span></span> | <span data-ttu-id="b8c96-453">1</span><span class="sxs-lookup"><span data-stu-id="b8c96-453">1</span></span>                                           |



 

## <a name="propertytagbitspersample"></a><span data-ttu-id="b8c96-454">PropertyTagBitsPerSample</span><span class="sxs-lookup"><span data-stu-id="b8c96-454">PropertyTagBitsPerSample</span></span>

<span data-ttu-id="b8c96-455">Numero di bit per componente colore.</span><span class="sxs-lookup"><span data-stu-id="b8c96-455">Number of bits per color component.</span></span> <span data-ttu-id="b8c96-456">Vedere anche [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).</span><span class="sxs-lookup"><span data-stu-id="b8c96-456">See also [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).</span></span>



| <span data-ttu-id="b8c96-457">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-457">Property info</span></span> | <span data-ttu-id="b8c96-458">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-458">Value</span></span> |
|-------|------------------------------------------|
| <span data-ttu-id="b8c96-459">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-459">Tag</span></span>   | <span data-ttu-id="b8c96-460">0x0102</span><span class="sxs-lookup"><span data-stu-id="b8c96-460">0x0102</span></span>                                   |
| <span data-ttu-id="b8c96-461">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-461">Type</span></span>  | <span data-ttu-id="b8c96-462">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="b8c96-462">PropertyTagTypeShort</span></span>                     |
| <span data-ttu-id="b8c96-463">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-463">Count</span></span> | <span data-ttu-id="b8c96-464">Numero di campioni (componenti) per pixel</span><span class="sxs-lookup"><span data-stu-id="b8c96-464">Number of samples (components) per pixel</span></span> |



 

## <a name="propertytagcompression"></a><span data-ttu-id="b8c96-465">PropertyTagCompression</span><span class="sxs-lookup"><span data-stu-id="b8c96-465">PropertyTagCompression</span></span>

<span data-ttu-id="b8c96-466">Schema di compressione usato per i dati dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="b8c96-466">Compression scheme used for the image data.</span></span>



| <span data-ttu-id="b8c96-467">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-467">Property info</span></span> | <span data-ttu-id="b8c96-468">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-468">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="b8c96-469">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-469">Tag</span></span>   | <span data-ttu-id="b8c96-470">0x0103</span><span class="sxs-lookup"><span data-stu-id="b8c96-470">0x0103</span></span>               |
| <span data-ttu-id="b8c96-471">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-471">Type</span></span>  | <span data-ttu-id="b8c96-472">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="b8c96-472">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="b8c96-473">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-473">Count</span></span> | <span data-ttu-id="b8c96-474">1</span><span class="sxs-lookup"><span data-stu-id="b8c96-474">1</span></span>                    |



 

## <a name="propertytagphotometricinterp"></a><span data-ttu-id="b8c96-475">PropertyTagPhotometricInterp</span><span class="sxs-lookup"><span data-stu-id="b8c96-475">PropertyTagPhotometricInterp</span></span>

<span data-ttu-id="b8c96-476">Come verranno interpretati i dati pixel.</span><span class="sxs-lookup"><span data-stu-id="b8c96-476">How pixel data will be interpreted.</span></span>



| <span data-ttu-id="b8c96-477">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-477">Property info</span></span> | <span data-ttu-id="b8c96-478">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-478">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="b8c96-479">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-479">Tag</span></span>   | <span data-ttu-id="b8c96-480">0x0106</span><span class="sxs-lookup"><span data-stu-id="b8c96-480">0x0106</span></span>               |
| <span data-ttu-id="b8c96-481">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-481">Type</span></span>  | <span data-ttu-id="b8c96-482">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="b8c96-482">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="b8c96-483">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-483">Count</span></span> | <span data-ttu-id="b8c96-484">1</span><span class="sxs-lookup"><span data-stu-id="b8c96-484">1</span></span>                    |



 

## <a name="propertytagthreshholding"></a><span data-ttu-id="b8c96-485">PropertyTagThreshHolding</span><span class="sxs-lookup"><span data-stu-id="b8c96-485">PropertyTagThreshHolding</span></span>

<span data-ttu-id="b8c96-486">Tecnica utilizzata per eseguire la conversione da pixel grigi a pixel neri e bianchi.</span><span class="sxs-lookup"><span data-stu-id="b8c96-486">Technique used to convert from gray pixels to black and white pixels.</span></span>



| <span data-ttu-id="b8c96-487">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-487">Property info</span></span> | <span data-ttu-id="b8c96-488">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-488">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="b8c96-489">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-489">Tag</span></span>   | <span data-ttu-id="b8c96-490">0x0107</span><span class="sxs-lookup"><span data-stu-id="b8c96-490">0x0107</span></span>               |
| <span data-ttu-id="b8c96-491">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-491">Type</span></span>  | <span data-ttu-id="b8c96-492">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="b8c96-492">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="b8c96-493">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-493">Count</span></span> | <span data-ttu-id="b8c96-494">1</span><span class="sxs-lookup"><span data-stu-id="b8c96-494">1</span></span>                    |



 

## <a name="propertytagcellwidth"></a><span data-ttu-id="b8c96-495">PropertyTagCellWidth</span><span class="sxs-lookup"><span data-stu-id="b8c96-495">PropertyTagCellWidth</span></span>

<span data-ttu-id="b8c96-496">Larghezza della matrice di retinatura o di mezzitoni.</span><span class="sxs-lookup"><span data-stu-id="b8c96-496">Width of the dithering or halftoning matrix.</span></span>



| <span data-ttu-id="b8c96-497">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-497">Property info</span></span> | <span data-ttu-id="b8c96-498">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-498">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="b8c96-499">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-499">Tag</span></span>   | <span data-ttu-id="b8c96-500">0x0108</span><span class="sxs-lookup"><span data-stu-id="b8c96-500">0x0108</span></span>               |
| <span data-ttu-id="b8c96-501">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-501">Type</span></span>  | <span data-ttu-id="b8c96-502">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="b8c96-502">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="b8c96-503">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-503">Count</span></span> | <span data-ttu-id="b8c96-504">1</span><span class="sxs-lookup"><span data-stu-id="b8c96-504">1</span></span>                    |



 

## <a name="propertytagcellheight"></a><span data-ttu-id="b8c96-505">PropertyTagCellHeight</span><span class="sxs-lookup"><span data-stu-id="b8c96-505">PropertyTagCellHeight</span></span>

<span data-ttu-id="b8c96-506">Altezza della matrice di retinatura o di mezzitoni.</span><span class="sxs-lookup"><span data-stu-id="b8c96-506">Height of the dithering or halftoning matrix.</span></span>



| <span data-ttu-id="b8c96-507">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-507">Property info</span></span> | <span data-ttu-id="b8c96-508">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-508">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="b8c96-509">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-509">Tag</span></span>   | <span data-ttu-id="b8c96-510">0x0109</span><span class="sxs-lookup"><span data-stu-id="b8c96-510">0x0109</span></span>               |
| <span data-ttu-id="b8c96-511">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-511">Type</span></span>  | <span data-ttu-id="b8c96-512">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="b8c96-512">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="b8c96-513">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-513">Count</span></span> | <span data-ttu-id="b8c96-514">1</span><span class="sxs-lookup"><span data-stu-id="b8c96-514">1</span></span>                    |



 

## <a name="propertytagfillorder"></a><span data-ttu-id="b8c96-515">PropertyTagFillOrder</span><span class="sxs-lookup"><span data-stu-id="b8c96-515">PropertyTagFillOrder</span></span>

<span data-ttu-id="b8c96-516">Ordine logico dei bit in un byte.</span><span class="sxs-lookup"><span data-stu-id="b8c96-516">Logical order of bits in a byte.</span></span>



| <span data-ttu-id="b8c96-517">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-517">Property info</span></span> | <span data-ttu-id="b8c96-518">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-518">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="b8c96-519">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-519">Tag</span></span>   | <span data-ttu-id="b8c96-520">0x010A</span><span class="sxs-lookup"><span data-stu-id="b8c96-520">0x010A</span></span>               |
| <span data-ttu-id="b8c96-521">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-521">Type</span></span>  | <span data-ttu-id="b8c96-522">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="b8c96-522">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="b8c96-523">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-523">Count</span></span> | <span data-ttu-id="b8c96-524">1</span><span class="sxs-lookup"><span data-stu-id="b8c96-524">1</span></span>                    |



 

## <a name="propertytagdocumentname"></a><span data-ttu-id="b8c96-525">PropertyTagDocumentName</span><span class="sxs-lookup"><span data-stu-id="b8c96-525">PropertyTagDocumentName</span></span>

<span data-ttu-id="b8c96-526">Stringa di caratteri con terminazione null che specifica il nome del documento da cui è stata analizzata l'immagine.</span><span class="sxs-lookup"><span data-stu-id="b8c96-526">Null-terminated character string that specifies the name of the document from which the image was scanned.</span></span>



| <span data-ttu-id="b8c96-527">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-527">Property info</span></span> | <span data-ttu-id="b8c96-528">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-528">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="b8c96-529">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-529">Tag</span></span>   | <span data-ttu-id="b8c96-530">0x010D</span><span class="sxs-lookup"><span data-stu-id="b8c96-530">0x010D</span></span>                                             |
| <span data-ttu-id="b8c96-531">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-531">Type</span></span>  | <span data-ttu-id="b8c96-532">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="b8c96-532">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="b8c96-533">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-533">Count</span></span> | <span data-ttu-id="b8c96-534">Lunghezza della stringa che include il carattere di terminazione NULL</span><span class="sxs-lookup"><span data-stu-id="b8c96-534">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagimagedescription"></a><span data-ttu-id="b8c96-535">PropertyTagImageDescription</span><span class="sxs-lookup"><span data-stu-id="b8c96-535">PropertyTagImageDescription</span></span>

<span data-ttu-id="b8c96-536">Stringa di caratteri con terminazione null che specifica il titolo dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="b8c96-536">Null-terminated character string that specifies the title of the image.</span></span>



| <span data-ttu-id="b8c96-537">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-537">Property info</span></span> | <span data-ttu-id="b8c96-538">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-538">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="b8c96-539">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-539">Tag</span></span>   | <span data-ttu-id="b8c96-540">0x010E</span><span class="sxs-lookup"><span data-stu-id="b8c96-540">0x010E</span></span>                                             |
| <span data-ttu-id="b8c96-541">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-541">Type</span></span>  | <span data-ttu-id="b8c96-542">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="b8c96-542">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="b8c96-543">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-543">Count</span></span> | <span data-ttu-id="b8c96-544">Lunghezza della stringa che include il carattere di terminazione NULL</span><span class="sxs-lookup"><span data-stu-id="b8c96-544">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagequipmake"></a><span data-ttu-id="b8c96-545">PropertyTagEquipMake</span><span class="sxs-lookup"><span data-stu-id="b8c96-545">PropertyTagEquipMake</span></span>

<span data-ttu-id="b8c96-546">Stringa di caratteri con terminazione null che specifica il produttore dell'apparecchiatura utilizzata per registrare l'immagine.</span><span class="sxs-lookup"><span data-stu-id="b8c96-546">Null-terminated character string that specifies the manufacturer of the equipment used to record the image.</span></span>



| <span data-ttu-id="b8c96-547">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-547">Property info</span></span> | <span data-ttu-id="b8c96-548">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-548">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="b8c96-549">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-549">Tag</span></span>   | <span data-ttu-id="b8c96-550">0x010F</span><span class="sxs-lookup"><span data-stu-id="b8c96-550">0x010F</span></span>                                             |
| <span data-ttu-id="b8c96-551">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-551">Type</span></span>  | <span data-ttu-id="b8c96-552">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="b8c96-552">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="b8c96-553">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-553">Count</span></span> | <span data-ttu-id="b8c96-554">Lunghezza della stringa che include il carattere di terminazione NULL</span><span class="sxs-lookup"><span data-stu-id="b8c96-554">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagequipmodel"></a><span data-ttu-id="b8c96-555">PropertyTagEquipModel</span><span class="sxs-lookup"><span data-stu-id="b8c96-555">PropertyTagEquipModel</span></span>

<span data-ttu-id="b8c96-556">Stringa di caratteri con terminazione null che specifica il nome del modello o il numero di modello dell'apparecchiatura utilizzata per registrare l'immagine.</span><span class="sxs-lookup"><span data-stu-id="b8c96-556">Null-terminated character string that specifies the model name or model number of the equipment used to record the image.</span></span>



| <span data-ttu-id="b8c96-557">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-557">Property info</span></span> | <span data-ttu-id="b8c96-558">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-558">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="b8c96-559">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-559">Tag</span></span>   | <span data-ttu-id="b8c96-560">0x0110</span><span class="sxs-lookup"><span data-stu-id="b8c96-560">0x0110</span></span>                                             |
| <span data-ttu-id="b8c96-561">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-561">Type</span></span>  | <span data-ttu-id="b8c96-562">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="b8c96-562">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="b8c96-563">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-563">Count</span></span> | <span data-ttu-id="b8c96-564">Lunghezza della stringa che include il carattere di terminazione NULL</span><span class="sxs-lookup"><span data-stu-id="b8c96-564">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagstripoffsets"></a><span data-ttu-id="b8c96-565">PropertyTagStripOffsets</span><span class="sxs-lookup"><span data-stu-id="b8c96-565">PropertyTagStripOffsets</span></span>

<span data-ttu-id="b8c96-566">Per ogni striscia, l'offset dei byte di tale striscia.</span><span class="sxs-lookup"><span data-stu-id="b8c96-566">For each strip, the byte offset of that strip.</span></span> <span data-ttu-id="b8c96-567">Vedere anche [PropertyTagRowsPerStrip](#propertytagrowsperstrip) e [PropertyTagStripBytesCount](#propertytagstripbytescount).</span><span class="sxs-lookup"><span data-stu-id="b8c96-567">See also [PropertyTagRowsPerStrip](#propertytagrowsperstrip) and [PropertyTagStripBytesCount](#propertytagstripbytescount).</span></span>



| <span data-ttu-id="b8c96-568">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-568">Property info</span></span> | <span data-ttu-id="b8c96-569">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-569">Value</span></span> |
|-------|---------------------------------------------|
| <span data-ttu-id="b8c96-570">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-570">Tag</span></span>   | <span data-ttu-id="b8c96-571">0x0111</span><span class="sxs-lookup"><span data-stu-id="b8c96-571">0x0111</span></span>                                      |
| <span data-ttu-id="b8c96-572">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-572">Type</span></span>  | <span data-ttu-id="b8c96-573">PropertyTagTypeShort o PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="b8c96-573">PropertyTagTypeShort or PropertyTagTypeLong</span></span> |
| <span data-ttu-id="b8c96-574">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-574">Count</span></span> | <span data-ttu-id="b8c96-575">Numero di strisce</span><span class="sxs-lookup"><span data-stu-id="b8c96-575">Number of strips</span></span>                            |



 

## <a name="propertytagorientation"></a><span data-ttu-id="b8c96-576">PropertyTagOrientation</span><span class="sxs-lookup"><span data-stu-id="b8c96-576">PropertyTagOrientation</span></span>

<span data-ttu-id="b8c96-577">Orientamento dell'immagine visualizzato in termini di righe e colonne.</span><span class="sxs-lookup"><span data-stu-id="b8c96-577">Image orientation viewed in terms of rows and columns.</span></span>



<span data-ttu-id="b8c96-578">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-578">Tag</span></span>

<span data-ttu-id="b8c96-579">0x0112</span><span class="sxs-lookup"><span data-stu-id="b8c96-579">0x0112</span></span>

<span data-ttu-id="b8c96-580">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-580">Type</span></span>

<span data-ttu-id="b8c96-581">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="b8c96-581">PropertyTagTypeShort</span></span>

<span data-ttu-id="b8c96-582">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-582">Count</span></span>

<span data-ttu-id="b8c96-583">1</span><span class="sxs-lookup"><span data-stu-id="b8c96-583">1</span></span>

<span data-ttu-id="b8c96-584">1-la riga 0A si trova nella parte superiore dell'immagine visiva e la colonna 0A è il lato sinistro dell'oggetto visivo.</span><span class="sxs-lookup"><span data-stu-id="b8c96-584">1 - The 0th row is at the top of the visual image, and the 0th column is the visual left side.</span></span> <span data-ttu-id="b8c96-585">2-la riga 0A si trova nella parte superiore dell'immagine e la colonna 0A è il lato destro dell'oggetto visivo.</span><span class="sxs-lookup"><span data-stu-id="b8c96-585">2 - The 0th row is at the visual top of the image, and the 0th column is the visual right side.</span></span> <span data-ttu-id="b8c96-586">3-la riga 0A si trova nella parte inferiore dell'immagine e la colonna 0A è il lato destro dell'oggetto visivo.</span><span class="sxs-lookup"><span data-stu-id="b8c96-586">3 - The 0th row is at the visual bottom of the image, and the 0th column is the visual right side.</span></span> <span data-ttu-id="b8c96-587">4-la riga 0A si trova nella parte inferiore dell'immagine e la colonna 0A è il lato sinistro dell'oggetto visivo.</span><span class="sxs-lookup"><span data-stu-id="b8c96-587">4 - The 0th row is at the visual bottom of the image, and the 0th column is the visual left side.</span></span> <span data-ttu-id="b8c96-588">5-la riga 0A è il lato sinistro dell'immagine e la colonna 0A è la parte superiore dell'oggetto visivo.</span><span class="sxs-lookup"><span data-stu-id="b8c96-588">5 - The 0th row is the visual left side of the image, and the 0th column is the visual top.</span></span> <span data-ttu-id="b8c96-589">6: la riga 0A è il lato visivo destro dell'immagine e la colonna 0A è la parte superiore dell'oggetto visivo.</span><span class="sxs-lookup"><span data-stu-id="b8c96-589">6 - The 0th row is the visual right side of the image, and the 0th column is the visual top.</span></span> <span data-ttu-id="b8c96-590">7-la riga 0A è il lato visivo destro dell'immagine e la colonna 0A è la parte inferiore dell'oggetto visivo.</span><span class="sxs-lookup"><span data-stu-id="b8c96-590">7 - The 0th row is the visual right side of the image, and the 0th column is the visual bottom.</span></span> <span data-ttu-id="b8c96-591">8: la riga 0A è il lato sinistro dell'immagine e la colonna 0A è la parte inferiore dell'oggetto visivo.</span><span class="sxs-lookup"><span data-stu-id="b8c96-591">8 - The 0th row is the visual left side of the image, and the 0th column is the visual bottom.</span></span>



 

## <a name="propertytagsamplesperpixel"></a><span data-ttu-id="b8c96-592">PropertyTagSamplesPerPixel</span><span class="sxs-lookup"><span data-stu-id="b8c96-592">PropertyTagSamplesPerPixel</span></span>

<span data-ttu-id="b8c96-593">Numero di componenti colore per pixel.</span><span class="sxs-lookup"><span data-stu-id="b8c96-593">Number of color components per pixel.</span></span>



| <span data-ttu-id="b8c96-594">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-594">Property info</span></span> | <span data-ttu-id="b8c96-595">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-595">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="b8c96-596">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-596">Tag</span></span>   | <span data-ttu-id="b8c96-597">0x0115</span><span class="sxs-lookup"><span data-stu-id="b8c96-597">0x0115</span></span>               |
| <span data-ttu-id="b8c96-598">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-598">Type</span></span>  | <span data-ttu-id="b8c96-599">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="b8c96-599">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="b8c96-600">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-600">Count</span></span> | <span data-ttu-id="b8c96-601">1</span><span class="sxs-lookup"><span data-stu-id="b8c96-601">1</span></span>                    |



 

## <a name="propertytagrowsperstrip"></a><span data-ttu-id="b8c96-602">PropertyTagRowsPerStrip</span><span class="sxs-lookup"><span data-stu-id="b8c96-602">PropertyTagRowsPerStrip</span></span>

<span data-ttu-id="b8c96-603">Numero di righe per striscia.</span><span class="sxs-lookup"><span data-stu-id="b8c96-603">Number of rows per strip.</span></span> <span data-ttu-id="b8c96-604">Vedere anche [PropertyTagStripBytesCount](#propertytagstripbytescount) e [PropertyTagStripOffsets](#propertytagstripoffsets).</span><span class="sxs-lookup"><span data-stu-id="b8c96-604">See also [PropertyTagStripBytesCount](#propertytagstripbytescount) and [PropertyTagStripOffsets](#propertytagstripoffsets).</span></span>



| <span data-ttu-id="b8c96-605">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-605">Property info</span></span> | <span data-ttu-id="b8c96-606">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-606">Value</span></span> |
|-------|---------------------------------------------|
| <span data-ttu-id="b8c96-607">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-607">Tag</span></span>   | <span data-ttu-id="b8c96-608">0x0116</span><span class="sxs-lookup"><span data-stu-id="b8c96-608">0x0116</span></span>                                      |
| <span data-ttu-id="b8c96-609">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-609">Type</span></span>  | <span data-ttu-id="b8c96-610">PropertyTagTypeShort o PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="b8c96-610">PropertyTagTypeShort or PropertyTagTypeLong</span></span> |
| <span data-ttu-id="b8c96-611">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-611">Count</span></span> | <span data-ttu-id="b8c96-612">1</span><span class="sxs-lookup"><span data-stu-id="b8c96-612">1</span></span>                                           |



 

## <a name="propertytagstripbytescount"></a><span data-ttu-id="b8c96-613">PropertyTagStripBytesCount</span><span class="sxs-lookup"><span data-stu-id="b8c96-613">PropertyTagStripBytesCount</span></span>

<span data-ttu-id="b8c96-614">Per ogni striscia, il numero totale di byte in tale striping.</span><span class="sxs-lookup"><span data-stu-id="b8c96-614">For each strip, the total number of bytes in that strip.</span></span>



| <span data-ttu-id="b8c96-615">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-615">Property info</span></span> | <span data-ttu-id="b8c96-616">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-616">Value</span></span> |
|-------|---------------------------------------------|
| <span data-ttu-id="b8c96-617">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-617">Tag</span></span>   | <span data-ttu-id="b8c96-618">0x0117</span><span class="sxs-lookup"><span data-stu-id="b8c96-618">0x0117</span></span>                                      |
| <span data-ttu-id="b8c96-619">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-619">Type</span></span>  | <span data-ttu-id="b8c96-620">PropertyTagTypeShort o PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="b8c96-620">PropertyTagTypeShort or PropertyTagTypeLong</span></span> |
| <span data-ttu-id="b8c96-621">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-621">Count</span></span> | <span data-ttu-id="b8c96-622">Numero di strisce</span><span class="sxs-lookup"><span data-stu-id="b8c96-622">Number of strips</span></span>                            |



 

## <a name="propertytagminsamplevalue"></a><span data-ttu-id="b8c96-623">PropertyTagMinSampleValue</span><span class="sxs-lookup"><span data-stu-id="b8c96-623">PropertyTagMinSampleValue</span></span>

<span data-ttu-id="b8c96-624">Per ogni componente del colore, valore minimo assegnato a tale componente.</span><span class="sxs-lookup"><span data-stu-id="b8c96-624">For each color component, the minimum value assigned to that component.</span></span> <span data-ttu-id="b8c96-625">Vedere anche [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).</span><span class="sxs-lookup"><span data-stu-id="b8c96-625">See also [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).</span></span>



| <span data-ttu-id="b8c96-626">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-626">Property info</span></span> | <span data-ttu-id="b8c96-627">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-627">Value</span></span> |
|-------|------------------------------------------|
| <span data-ttu-id="b8c96-628">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-628">Tag</span></span>   | <span data-ttu-id="b8c96-629">0x0118</span><span class="sxs-lookup"><span data-stu-id="b8c96-629">0x0118</span></span>                                   |
| <span data-ttu-id="b8c96-630">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-630">Type</span></span>  | <span data-ttu-id="b8c96-631">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="b8c96-631">PropertyTagTypeShort</span></span>                     |
| <span data-ttu-id="b8c96-632">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-632">Count</span></span> | <span data-ttu-id="b8c96-633">Numero di campioni (componenti) per pixel</span><span class="sxs-lookup"><span data-stu-id="b8c96-633">Number of samples (components) per pixel</span></span> |



 

## <a name="propertytagmaxsamplevalue"></a><span data-ttu-id="b8c96-634">PropertyTagMaxSampleValue</span><span class="sxs-lookup"><span data-stu-id="b8c96-634">PropertyTagMaxSampleValue</span></span>

<span data-ttu-id="b8c96-635">Per ogni componente del colore, valore massimo assegnato a tale componente.</span><span class="sxs-lookup"><span data-stu-id="b8c96-635">For each color component, the maximum value assigned to that component.</span></span> <span data-ttu-id="b8c96-636">Vedere anche [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).</span><span class="sxs-lookup"><span data-stu-id="b8c96-636">See also [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).</span></span>



| <span data-ttu-id="b8c96-637">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-637">Property info</span></span> | <span data-ttu-id="b8c96-638">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-638">Value</span></span> |
|-------|------------------------------------------|
| <span data-ttu-id="b8c96-639">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-639">Tag</span></span>   | <span data-ttu-id="b8c96-640">0x0119</span><span class="sxs-lookup"><span data-stu-id="b8c96-640">0x0119</span></span>                                   |
| <span data-ttu-id="b8c96-641">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-641">Type</span></span>  | <span data-ttu-id="b8c96-642">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="b8c96-642">PropertyTagTypeShort</span></span>                     |
| <span data-ttu-id="b8c96-643">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-643">Count</span></span> | <span data-ttu-id="b8c96-644">Numero di campioni (componenti) per pixel</span><span class="sxs-lookup"><span data-stu-id="b8c96-644">Number of samples (components) per pixel</span></span> |



 

## <a name="propertytagxresolution"></a><span data-ttu-id="b8c96-645">PropertyTagXResolution</span><span class="sxs-lookup"><span data-stu-id="b8c96-645">PropertyTagXResolution</span></span>

<span data-ttu-id="b8c96-646">Numero di pixel per unità nella direzione della larghezza dell'immagine (x).</span><span class="sxs-lookup"><span data-stu-id="b8c96-646">Number of pixels per unit in the image width (x) direction.</span></span> <span data-ttu-id="b8c96-647">L'unità è specificata da [PropertyTagResolutionUnit](#propertytagresolutionunit).</span><span class="sxs-lookup"><span data-stu-id="b8c96-647">The unit is specified by [PropertyTagResolutionUnit](#propertytagresolutionunit).</span></span>



| <span data-ttu-id="b8c96-648">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-648">Property info</span></span> | <span data-ttu-id="b8c96-649">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-649">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="b8c96-650">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-650">Tag</span></span>   | <span data-ttu-id="b8c96-651">0x011A</span><span class="sxs-lookup"><span data-stu-id="b8c96-651">0x011A</span></span>                  |
| <span data-ttu-id="b8c96-652">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-652">Type</span></span>  | <span data-ttu-id="b8c96-653">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="b8c96-653">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="b8c96-654">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-654">Count</span></span> | <span data-ttu-id="b8c96-655">1</span><span class="sxs-lookup"><span data-stu-id="b8c96-655">1</span></span>                       |



 

## <a name="propertytagyresolution"></a><span data-ttu-id="b8c96-656">PropertyTagYResolution</span><span class="sxs-lookup"><span data-stu-id="b8c96-656">PropertyTagYResolution</span></span>

<span data-ttu-id="b8c96-657">Numero di pixel per unità nella direzione altezza (y) immagine.</span><span class="sxs-lookup"><span data-stu-id="b8c96-657">Number of pixels per unit in the image height (y) direction.</span></span> <span data-ttu-id="b8c96-658">L'unità è specificata da [PropertyTagResolutionUnit](#propertytagresolutionunit).</span><span class="sxs-lookup"><span data-stu-id="b8c96-658">The unit is specified by [PropertyTagResolutionUnit](#propertytagresolutionunit).</span></span>



| <span data-ttu-id="b8c96-659">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-659">Property info</span></span> | <span data-ttu-id="b8c96-660">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-660">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="b8c96-661">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-661">Tag</span></span>   | <span data-ttu-id="b8c96-662">0x011B</span><span class="sxs-lookup"><span data-stu-id="b8c96-662">0x011B</span></span>                  |
| <span data-ttu-id="b8c96-663">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-663">Type</span></span>  | <span data-ttu-id="b8c96-664">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="b8c96-664">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="b8c96-665">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-665">Count</span></span> | <span data-ttu-id="b8c96-666">1</span><span class="sxs-lookup"><span data-stu-id="b8c96-666">1</span></span>                       |



 

## <a name="propertytagplanarconfig"></a><span data-ttu-id="b8c96-667">PropertyTagPlanarConfig</span><span class="sxs-lookup"><span data-stu-id="b8c96-667">PropertyTagPlanarConfig</span></span>

<span data-ttu-id="b8c96-668">Indica se i componenti pixel sono registrati in formato a più grossi o planari.</span><span class="sxs-lookup"><span data-stu-id="b8c96-668">Whether pixel components are recorded in chunky or planar format.</span></span>



| <span data-ttu-id="b8c96-669">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-669">Property info</span></span> | <span data-ttu-id="b8c96-670">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-670">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="b8c96-671">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-671">Tag</span></span>   | <span data-ttu-id="b8c96-672">0x011C</span><span class="sxs-lookup"><span data-stu-id="b8c96-672">0x011C</span></span>               |
| <span data-ttu-id="b8c96-673">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-673">Type</span></span>  | <span data-ttu-id="b8c96-674">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="b8c96-674">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="b8c96-675">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-675">Count</span></span> | <span data-ttu-id="b8c96-676">1</span><span class="sxs-lookup"><span data-stu-id="b8c96-676">1</span></span>                    |



 

## <a name="propertytagpagename"></a><span data-ttu-id="b8c96-677">PropertyTagPageName</span><span class="sxs-lookup"><span data-stu-id="b8c96-677">PropertyTagPageName</span></span>

<span data-ttu-id="b8c96-678">Stringa di caratteri con terminazione null che specifica il nome della pagina da cui è stata analizzata l'immagine.</span><span class="sxs-lookup"><span data-stu-id="b8c96-678">Null-terminated character string that specifies the name of the page from which the image was scanned.</span></span>



| <span data-ttu-id="b8c96-679">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-679">Property info</span></span> | <span data-ttu-id="b8c96-680">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-680">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="b8c96-681">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-681">Tag</span></span>   | <span data-ttu-id="b8c96-682">0x011D</span><span class="sxs-lookup"><span data-stu-id="b8c96-682">0x011D</span></span>                                             |
| <span data-ttu-id="b8c96-683">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-683">Type</span></span>  | <span data-ttu-id="b8c96-684">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="b8c96-684">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="b8c96-685">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-685">Count</span></span> | <span data-ttu-id="b8c96-686">Lunghezza della stringa che include il carattere di terminazione NULL</span><span class="sxs-lookup"><span data-stu-id="b8c96-686">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagxposition"></a><span data-ttu-id="b8c96-687">PropertyTagXPosition</span><span class="sxs-lookup"><span data-stu-id="b8c96-687">PropertyTagXPosition</span></span>

<span data-ttu-id="b8c96-688">Offset dal lato sinistro della pagina al lato sinistro dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="b8c96-688">Offset from the left side of the page to the left side of the image.</span></span> <span data-ttu-id="b8c96-689">L'unità di misura viene specificata da [PropertyTagResolutionUnit](#propertytagresolutionunit).</span><span class="sxs-lookup"><span data-stu-id="b8c96-689">The unit of measure is specified by [PropertyTagResolutionUnit](#propertytagresolutionunit).</span></span>



| <span data-ttu-id="b8c96-690">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-690">Property info</span></span> | <span data-ttu-id="b8c96-691">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-691">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="b8c96-692">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-692">Tag</span></span>   | <span data-ttu-id="b8c96-693">0x011E</span><span class="sxs-lookup"><span data-stu-id="b8c96-693">0x011E</span></span>                  |
| <span data-ttu-id="b8c96-694">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-694">Type</span></span>  | <span data-ttu-id="b8c96-695">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="b8c96-695">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="b8c96-696">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-696">Count</span></span> | <span data-ttu-id="b8c96-697">1</span><span class="sxs-lookup"><span data-stu-id="b8c96-697">1</span></span>                       |



 

## <a name="propertytagyposition"></a><span data-ttu-id="b8c96-698">PropertyTagYPosition</span><span class="sxs-lookup"><span data-stu-id="b8c96-698">PropertyTagYPosition</span></span>

<span data-ttu-id="b8c96-699">Offset dalla parte superiore della pagina alla parte superiore dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="b8c96-699">Offset from the top of the page to the top of the image.</span></span> <span data-ttu-id="b8c96-700">L'unità di misura viene specificata da [PropertyTagResolutionUnit](#propertytagresolutionunit).</span><span class="sxs-lookup"><span data-stu-id="b8c96-700">The unit of measure is specified by [PropertyTagResolutionUnit](#propertytagresolutionunit).</span></span>



| <span data-ttu-id="b8c96-701">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-701">Property info</span></span> | <span data-ttu-id="b8c96-702">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-702">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="b8c96-703">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-703">Tag</span></span>   | <span data-ttu-id="b8c96-704">0x011F</span><span class="sxs-lookup"><span data-stu-id="b8c96-704">0x011F</span></span>                  |
| <span data-ttu-id="b8c96-705">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-705">Type</span></span>  | <span data-ttu-id="b8c96-706">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="b8c96-706">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="b8c96-707">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-707">Count</span></span> | <span data-ttu-id="b8c96-708">1</span><span class="sxs-lookup"><span data-stu-id="b8c96-708">1</span></span>                       |



 

## <a name="propertytagfreeoffset"></a><span data-ttu-id="b8c96-709">PropertyTagFreeOffset</span><span class="sxs-lookup"><span data-stu-id="b8c96-709">PropertyTagFreeOffset</span></span>

<span data-ttu-id="b8c96-710">Per ogni stringa di byte contigui non utilizzati, offset di byte di tale stringa.</span><span class="sxs-lookup"><span data-stu-id="b8c96-710">For each string of contiguous unused bytes, the byte offset of that string.</span></span>



| <span data-ttu-id="b8c96-711">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-711">Property info</span></span> | <span data-ttu-id="b8c96-712">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-712">Value</span></span> |
|------|---------------------|
| <span data-ttu-id="b8c96-713">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-713">Tag</span></span>  | <span data-ttu-id="b8c96-714">0x0120</span><span class="sxs-lookup"><span data-stu-id="b8c96-714">0x0120</span></span>              |
| <span data-ttu-id="b8c96-715">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-715">Type</span></span> | <span data-ttu-id="b8c96-716">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="b8c96-716">PropertyTagTypeLong</span></span> |



 

## <a name="propertytagfreebytecounts"></a><span data-ttu-id="b8c96-717">PropertyTagFreeByteCounts</span><span class="sxs-lookup"><span data-stu-id="b8c96-717">PropertyTagFreeByteCounts</span></span>

<span data-ttu-id="b8c96-718">Per ogni stringa di byte contigui non utilizzati, numero di byte in tale stringa.</span><span class="sxs-lookup"><span data-stu-id="b8c96-718">For each string of contiguous unused bytes, the number of bytes in that string.</span></span>



| <span data-ttu-id="b8c96-719">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-719">Property info</span></span> | <span data-ttu-id="b8c96-720">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-720">Value</span></span> |
|-------|-----------------------------------------------|
| <span data-ttu-id="b8c96-721">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-721">Tag</span></span>   | <span data-ttu-id="b8c96-722">0x0121</span><span class="sxs-lookup"><span data-stu-id="b8c96-722">0x0121</span></span>                                        |
| <span data-ttu-id="b8c96-723">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-723">Type</span></span>  | <span data-ttu-id="b8c96-724">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="b8c96-724">PropertyTagTypeLong</span></span>                           |
| <span data-ttu-id="b8c96-725">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-725">Count</span></span> | <span data-ttu-id="b8c96-726">Numero di stringhe di byte contigui non utilizzati.</span><span class="sxs-lookup"><span data-stu-id="b8c96-726">Number of strings of contiguous unused bytes.</span></span> |



 

## <a name="propertytaggrayresponseunit"></a><span data-ttu-id="b8c96-727">PropertyTagGrayResponseUnit</span><span class="sxs-lookup"><span data-stu-id="b8c96-727">PropertyTagGrayResponseUnit</span></span>

<span data-ttu-id="b8c96-728">Precisione del numero specificato da PropertyTagGrayResponseCurve.</span><span class="sxs-lookup"><span data-stu-id="b8c96-728">Precision of the number specified by PropertyTagGrayResponseCurve.</span></span> <span data-ttu-id="b8c96-729">1 specifica i decimi, 2 specifica i centesimi, 3 specifica i millesimi e così via.</span><span class="sxs-lookup"><span data-stu-id="b8c96-729">1 specifies tenths, 2 specifies hundredths, 3 specifies thousandths, and so on.</span></span>



| <span data-ttu-id="b8c96-730">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-730">Property info</span></span> | <span data-ttu-id="b8c96-731">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-731">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="b8c96-732">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-732">Tag</span></span>   | <span data-ttu-id="b8c96-733">0x0122</span><span class="sxs-lookup"><span data-stu-id="b8c96-733">0x0122</span></span>               |
| <span data-ttu-id="b8c96-734">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-734">Type</span></span>  | <span data-ttu-id="b8c96-735">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="b8c96-735">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="b8c96-736">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-736">Count</span></span> | <span data-ttu-id="b8c96-737">1</span><span class="sxs-lookup"><span data-stu-id="b8c96-737">1</span></span>                    |



 

## <a name="propertytaggrayresponsecurve"></a><span data-ttu-id="b8c96-738">PropertyTagGrayResponseCurve</span><span class="sxs-lookup"><span data-stu-id="b8c96-738">PropertyTagGrayResponseCurve</span></span>

<span data-ttu-id="b8c96-739">Per ogni possibile valore in pixel in un'immagine in scala di grigi, la densità ottica del valore del pixel.</span><span class="sxs-lookup"><span data-stu-id="b8c96-739">For each possible pixel value in a grayscale image, the optical density of that pixel value.</span></span>



| <span data-ttu-id="b8c96-740">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-740">Property info</span></span> | <span data-ttu-id="b8c96-741">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-741">Value</span></span> |
|-------|---------------------------------|
| <span data-ttu-id="b8c96-742">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-742">Tag</span></span>   | <span data-ttu-id="b8c96-743">0x0123</span><span class="sxs-lookup"><span data-stu-id="b8c96-743">0x0123</span></span>                          |
| <span data-ttu-id="b8c96-744">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-744">Type</span></span>  | <span data-ttu-id="b8c96-745">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="b8c96-745">PropertyTagTypeShort</span></span>            |
| <span data-ttu-id="b8c96-746">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-746">Count</span></span> | <span data-ttu-id="b8c96-747">Numero di possibili valori pixel</span><span class="sxs-lookup"><span data-stu-id="b8c96-747">Number of possible pixel values</span></span> |



 

## <a name="propertytagt4option"></a><span data-ttu-id="b8c96-748">PropertyTagT4Option</span><span class="sxs-lookup"><span data-stu-id="b8c96-748">PropertyTagT4Option</span></span>

<span data-ttu-id="b8c96-749">Set di flag correlati alla codifica T4.</span><span class="sxs-lookup"><span data-stu-id="b8c96-749">Set of flags that relate to T4 encoding.</span></span>



| <span data-ttu-id="b8c96-750">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-750">Property info</span></span> | <span data-ttu-id="b8c96-751">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-751">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="b8c96-752">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-752">Tag</span></span>   | <span data-ttu-id="b8c96-753">0x0124</span><span class="sxs-lookup"><span data-stu-id="b8c96-753">0x0124</span></span>              |
| <span data-ttu-id="b8c96-754">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-754">Type</span></span>  | <span data-ttu-id="b8c96-755">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="b8c96-755">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="b8c96-756">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-756">Count</span></span> | <span data-ttu-id="b8c96-757">1</span><span class="sxs-lookup"><span data-stu-id="b8c96-757">1</span></span>                   |



 

## <a name="propertytagt6option"></a><span data-ttu-id="b8c96-758">PropertyTagT6Option</span><span class="sxs-lookup"><span data-stu-id="b8c96-758">PropertyTagT6Option</span></span>

<span data-ttu-id="b8c96-759">Set di flag correlati alla codifica T6.</span><span class="sxs-lookup"><span data-stu-id="b8c96-759">Set of flags that relate to T6 encoding.</span></span>



| <span data-ttu-id="b8c96-760">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-760">Property info</span></span> | <span data-ttu-id="b8c96-761">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-761">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="b8c96-762">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-762">Tag</span></span>   | <span data-ttu-id="b8c96-763">0x0125</span><span class="sxs-lookup"><span data-stu-id="b8c96-763">0x0125</span></span>              |
| <span data-ttu-id="b8c96-764">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-764">Type</span></span>  | <span data-ttu-id="b8c96-765">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="b8c96-765">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="b8c96-766">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-766">Count</span></span> | <span data-ttu-id="b8c96-767">1</span><span class="sxs-lookup"><span data-stu-id="b8c96-767">1</span></span>                   |



 

## <a name="propertytagresolutionunit"></a><span data-ttu-id="b8c96-768">PropertyTagResolutionUnit</span><span class="sxs-lookup"><span data-stu-id="b8c96-768">PropertyTagResolutionUnit</span></span>

<span data-ttu-id="b8c96-769">Unità di misura per la risoluzione orizzontale e la risoluzione verticale.</span><span class="sxs-lookup"><span data-stu-id="b8c96-769">Unit of measure for the horizontal resolution and the vertical resolution.</span></span>



<span data-ttu-id="b8c96-770">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-770">Tag</span></span>

<span data-ttu-id="b8c96-771">0x0128</span><span class="sxs-lookup"><span data-stu-id="b8c96-771">0x0128</span></span>

<span data-ttu-id="b8c96-772">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-772">Type</span></span>

<span data-ttu-id="b8c96-773">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="b8c96-773">PropertyTagTypeShort</span></span>

<span data-ttu-id="b8c96-774">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-774">Count</span></span>

<span data-ttu-id="b8c96-775">1</span><span class="sxs-lookup"><span data-stu-id="b8c96-775">1</span></span>

<span data-ttu-id="b8c96-776">2-pollice 3 centimetri</span><span class="sxs-lookup"><span data-stu-id="b8c96-776">2 - inch 3 - centimeter</span></span>



 

## <a name="propertytagpagenumber"></a><span data-ttu-id="b8c96-777">PropertyTagPageNumber</span><span class="sxs-lookup"><span data-stu-id="b8c96-777">PropertyTagPageNumber</span></span>

<span data-ttu-id="b8c96-778">Numero di pagina della pagina da cui è stata analizzata l'immagine.</span><span class="sxs-lookup"><span data-stu-id="b8c96-778">Page number of the page from which the image was scanned.</span></span>



| <span data-ttu-id="b8c96-779">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-779">Property info</span></span> | <span data-ttu-id="b8c96-780">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-780">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="b8c96-781">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-781">Tag</span></span>   | <span data-ttu-id="b8c96-782">0x0129</span><span class="sxs-lookup"><span data-stu-id="b8c96-782">0x0129</span></span>               |
| <span data-ttu-id="b8c96-783">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-783">Type</span></span>  | <span data-ttu-id="b8c96-784">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="b8c96-784">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="b8c96-785">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-785">Count</span></span> | <span data-ttu-id="b8c96-786">1</span><span class="sxs-lookup"><span data-stu-id="b8c96-786">1</span></span>                    |



 

## <a name="propertytagtransferfunction"></a><span data-ttu-id="b8c96-787">PropertyTagTransferFunction</span><span class="sxs-lookup"><span data-stu-id="b8c96-787">PropertyTagTransferFunction</span></span>

<span data-ttu-id="b8c96-788">Tabelle che specificano le funzioni di trasferimento per l'immagine.</span><span class="sxs-lookup"><span data-stu-id="b8c96-788">Tables that specify transfer functions for the image.</span></span>



| <span data-ttu-id="b8c96-789">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-789">Property info</span></span> | <span data-ttu-id="b8c96-790">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-790">Value</span></span> |
|-------|------------------------------------------------------|
| <span data-ttu-id="b8c96-791">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-791">Tag</span></span>   | <span data-ttu-id="b8c96-792">0x012D</span><span class="sxs-lookup"><span data-stu-id="b8c96-792">0x012D</span></span>                                               |
| <span data-ttu-id="b8c96-793">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-793">Type</span></span>  | <span data-ttu-id="b8c96-794">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="b8c96-794">PropertyTagTypeShort</span></span>                                 |
| <span data-ttu-id="b8c96-795">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-795">Count</span></span> | <span data-ttu-id="b8c96-796">Numero totale di parole a 16 bit necessarie per le tabelle</span><span class="sxs-lookup"><span data-stu-id="b8c96-796">Total number of 16-bit words required for the tables</span></span> |



 

## <a name="propertytagsoftwareused"></a><span data-ttu-id="b8c96-797">PropertyTagSoftwareUsed</span><span class="sxs-lookup"><span data-stu-id="b8c96-797">PropertyTagSoftwareUsed</span></span>

<span data-ttu-id="b8c96-798">Stringa di caratteri con terminazione null che specifica il nome e la versione del software o del firmware del dispositivo usato per generare l'immagine.</span><span class="sxs-lookup"><span data-stu-id="b8c96-798">Null-terminated character string that specifies the name and version of the software or firmware of the device used to generate the image.</span></span>



| <span data-ttu-id="b8c96-799">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-799">Property info</span></span> | <span data-ttu-id="b8c96-800">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-800">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="b8c96-801">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-801">Tag</span></span>   | <span data-ttu-id="b8c96-802">0x0131</span><span class="sxs-lookup"><span data-stu-id="b8c96-802">0x0131</span></span>                                             |
| <span data-ttu-id="b8c96-803">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-803">Type</span></span>  | <span data-ttu-id="b8c96-804">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="b8c96-804">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="b8c96-805">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-805">Count</span></span> | <span data-ttu-id="b8c96-806">Lunghezza della stringa che include il carattere di terminazione NULL</span><span class="sxs-lookup"><span data-stu-id="b8c96-806">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagdatetime"></a><span data-ttu-id="b8c96-807">PropertyTagDateTime</span><span class="sxs-lookup"><span data-stu-id="b8c96-807">PropertyTagDateTime</span></span>

<span data-ttu-id="b8c96-808">Data e ora di creazione dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="b8c96-808">Date and time the image was created.</span></span>



| <span data-ttu-id="b8c96-809">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-809">Property info</span></span> | <span data-ttu-id="b8c96-810">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-810">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="b8c96-811">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-811">Tag</span></span>   | <span data-ttu-id="b8c96-812">0x0132</span><span class="sxs-lookup"><span data-stu-id="b8c96-812">0x0132</span></span>               |
| <span data-ttu-id="b8c96-813">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-813">Type</span></span>  | <span data-ttu-id="b8c96-814">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="b8c96-814">PropertyTagTypeASCII</span></span> |
| <span data-ttu-id="b8c96-815">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-815">Count</span></span> | <span data-ttu-id="b8c96-816">20</span><span class="sxs-lookup"><span data-stu-id="b8c96-816">20</span></span>                   |



 

## <a name="propertytagartist"></a><span data-ttu-id="b8c96-817">PropertyTagArtist</span><span class="sxs-lookup"><span data-stu-id="b8c96-817">PropertyTagArtist</span></span>

<span data-ttu-id="b8c96-818">Stringa di caratteri con terminazione null che specifica il nome della persona che ha creato l'immagine.</span><span class="sxs-lookup"><span data-stu-id="b8c96-818">Null-terminated character string that specifies the name of the person who created the image.</span></span>



| <span data-ttu-id="b8c96-819">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-819">Property info</span></span> | <span data-ttu-id="b8c96-820">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-820">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="b8c96-821">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-821">Tag</span></span>   | <span data-ttu-id="b8c96-822">0x013B</span><span class="sxs-lookup"><span data-stu-id="b8c96-822">0x013B</span></span>                                             |
| <span data-ttu-id="b8c96-823">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-823">Type</span></span>  | <span data-ttu-id="b8c96-824">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="b8c96-824">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="b8c96-825">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-825">Count</span></span> | <span data-ttu-id="b8c96-826">Lunghezza della stringa che include il carattere di terminazione NULL</span><span class="sxs-lookup"><span data-stu-id="b8c96-826">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytaghostcomputer"></a><span data-ttu-id="b8c96-827">PropertyTagHostComputer</span><span class="sxs-lookup"><span data-stu-id="b8c96-827">PropertyTagHostComputer</span></span>

<span data-ttu-id="b8c96-828">Stringa di caratteri con terminazione null che specifica il computer e/o il sistema operativo utilizzato per creare l'immagine.</span><span class="sxs-lookup"><span data-stu-id="b8c96-828">Null-terminated character string that specifies the computer and/or operating system used to create the image.</span></span>



| <span data-ttu-id="b8c96-829">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-829">Property info</span></span> | <span data-ttu-id="b8c96-830">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-830">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="b8c96-831">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-831">Tag</span></span>   | <span data-ttu-id="b8c96-832">0x013C</span><span class="sxs-lookup"><span data-stu-id="b8c96-832">0x013C</span></span>                                             |
| <span data-ttu-id="b8c96-833">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-833">Type</span></span>  | <span data-ttu-id="b8c96-834">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="b8c96-834">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="b8c96-835">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-835">Count</span></span> | <span data-ttu-id="b8c96-836">Lunghezza della stringa che include il carattere di terminazione NULL</span><span class="sxs-lookup"><span data-stu-id="b8c96-836">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagpredictor"></a><span data-ttu-id="b8c96-837">PropertyTagPredictor</span><span class="sxs-lookup"><span data-stu-id="b8c96-837">PropertyTagPredictor</span></span>

<span data-ttu-id="b8c96-838">Tipo di schema di stima applicato ai dati dell'immagine prima dell'applicazione dello schema di codifica.</span><span class="sxs-lookup"><span data-stu-id="b8c96-838">Type of prediction scheme that was applied to the image data before the encoding scheme was applied.</span></span>



| <span data-ttu-id="b8c96-839">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-839">Property info</span></span> | <span data-ttu-id="b8c96-840">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-840">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="b8c96-841">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-841">Tag</span></span>   | <span data-ttu-id="b8c96-842">0x013D</span><span class="sxs-lookup"><span data-stu-id="b8c96-842">0x013D</span></span>               |
| <span data-ttu-id="b8c96-843">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-843">Type</span></span>  | <span data-ttu-id="b8c96-844">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="b8c96-844">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="b8c96-845">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-845">Count</span></span> | <span data-ttu-id="b8c96-846">1</span><span class="sxs-lookup"><span data-stu-id="b8c96-846">1</span></span>                    |



 

## <a name="propertytagwhitepoint"></a><span data-ttu-id="b8c96-847">PropertyTagWhitePoint</span><span class="sxs-lookup"><span data-stu-id="b8c96-847">PropertyTagWhitePoint</span></span>

<span data-ttu-id="b8c96-848">Cromaticità del punto bianco dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="b8c96-848">Chromaticity of the white point of the image.</span></span>



| <span data-ttu-id="b8c96-849">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-849">Property info</span></span> | <span data-ttu-id="b8c96-850">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-850">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="b8c96-851">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-851">Tag</span></span>   | <span data-ttu-id="b8c96-852">0x013E</span><span class="sxs-lookup"><span data-stu-id="b8c96-852">0x013E</span></span>                  |
| <span data-ttu-id="b8c96-853">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-853">Type</span></span>  | <span data-ttu-id="b8c96-854">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="b8c96-854">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="b8c96-855">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-855">Count</span></span> | <span data-ttu-id="b8c96-856">2</span><span class="sxs-lookup"><span data-stu-id="b8c96-856">2</span></span>                       |



 

## <a name="propertytagprimarychromaticities"></a><span data-ttu-id="b8c96-857">PropertyTagPrimaryChromaticities</span><span class="sxs-lookup"><span data-stu-id="b8c96-857">PropertyTagPrimaryChromaticities</span></span>

<span data-ttu-id="b8c96-858">Per ognuno dei tre colori primari nell'immagine, la cromaticità di tale colore.</span><span class="sxs-lookup"><span data-stu-id="b8c96-858">For each of the three primary colors in the image, the chromaticity of that color.</span></span>



| <span data-ttu-id="b8c96-859">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-859">Property info</span></span> | <span data-ttu-id="b8c96-860">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-860">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="b8c96-861">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-861">Tag</span></span>   | <span data-ttu-id="b8c96-862">0x013F</span><span class="sxs-lookup"><span data-stu-id="b8c96-862">0x013F</span></span>                  |
| <span data-ttu-id="b8c96-863">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-863">Type</span></span>  | <span data-ttu-id="b8c96-864">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="b8c96-864">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="b8c96-865">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-865">Count</span></span> | <span data-ttu-id="b8c96-866">6</span><span class="sxs-lookup"><span data-stu-id="b8c96-866">6</span></span>                       |



 

## <a name="propertytagcolormap"></a><span data-ttu-id="b8c96-867">PropertyTagColorMap</span><span class="sxs-lookup"><span data-stu-id="b8c96-867">PropertyTagColorMap</span></span>

<span data-ttu-id="b8c96-868">Tavolozza dei colori (tabella di ricerca) per un'immagine con indicizzazione della tavolozza.</span><span class="sxs-lookup"><span data-stu-id="b8c96-868">Color palette (lookup table) for a palette-indexed image.</span></span>



| <span data-ttu-id="b8c96-869">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-869">Property info</span></span> | <span data-ttu-id="b8c96-870">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-870">Value</span></span> |
|-------|-------------------------------------------------|
| <span data-ttu-id="b8c96-871">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-871">Tag</span></span>   | <span data-ttu-id="b8c96-872">0x0140</span><span class="sxs-lookup"><span data-stu-id="b8c96-872">0x0140</span></span>                                          |
| <span data-ttu-id="b8c96-873">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-873">Type</span></span>  | <span data-ttu-id="b8c96-874">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="b8c96-874">PropertyTagTypeShort</span></span>                            |
| <span data-ttu-id="b8c96-875">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-875">Count</span></span> | <span data-ttu-id="b8c96-876">Numero di parole a 16 bit richieste per la tavolozza</span><span class="sxs-lookup"><span data-stu-id="b8c96-876">Number of 16-bit words required for the palette</span></span> |



 

## <a name="propertytaghalftonehints"></a><span data-ttu-id="b8c96-877">PropertyTagHalftoneHints</span><span class="sxs-lookup"><span data-stu-id="b8c96-877">PropertyTagHalftoneHints</span></span>

<span data-ttu-id="b8c96-878">Informazioni usate dalla funzione mezzitoni</span><span class="sxs-lookup"><span data-stu-id="b8c96-878">Information used by the halftone function</span></span>



| <span data-ttu-id="b8c96-879">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-879">Property info</span></span> | <span data-ttu-id="b8c96-880">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-880">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="b8c96-881">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-881">Tag</span></span>   | <span data-ttu-id="b8c96-882">0x0141</span><span class="sxs-lookup"><span data-stu-id="b8c96-882">0x0141</span></span>               |
| <span data-ttu-id="b8c96-883">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-883">Type</span></span>  | <span data-ttu-id="b8c96-884">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="b8c96-884">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="b8c96-885">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-885">Count</span></span> | <span data-ttu-id="b8c96-886">2</span><span class="sxs-lookup"><span data-stu-id="b8c96-886">2</span></span>                    |



 

## <a name="propertytagtilewidth"></a><span data-ttu-id="b8c96-887">PropertyTagTileWidth</span><span class="sxs-lookup"><span data-stu-id="b8c96-887">PropertyTagTileWidth</span></span>

<span data-ttu-id="b8c96-888">Numero di colonne in pixel in ogni sezione.</span><span class="sxs-lookup"><span data-stu-id="b8c96-888">Number of pixel columns in each tile.</span></span>



| <span data-ttu-id="b8c96-889">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-889">Property info</span></span> | <span data-ttu-id="b8c96-890">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-890">Value</span></span> |
|-------|---------------------------------------------|
| <span data-ttu-id="b8c96-891">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-891">Tag</span></span>   | <span data-ttu-id="b8c96-892">0x0142</span><span class="sxs-lookup"><span data-stu-id="b8c96-892">0x0142</span></span>                                      |
| <span data-ttu-id="b8c96-893">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-893">Type</span></span>  | <span data-ttu-id="b8c96-894">PropertyTagTypeShort o PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="b8c96-894">PropertyTagTypeShort or PropertyTagTypeLong</span></span> |
| <span data-ttu-id="b8c96-895">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-895">Count</span></span> | <span data-ttu-id="b8c96-896">1</span><span class="sxs-lookup"><span data-stu-id="b8c96-896">1</span></span>                                           |



 

## <a name="propertytagtilelength"></a><span data-ttu-id="b8c96-897">PropertyTagTileLength</span><span class="sxs-lookup"><span data-stu-id="b8c96-897">PropertyTagTileLength</span></span>

<span data-ttu-id="b8c96-898">Numero di righe in pixel in ogni sezione.</span><span class="sxs-lookup"><span data-stu-id="b8c96-898">Number of pixel rows in each tile.</span></span>



| <span data-ttu-id="b8c96-899">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-899">Property info</span></span> | <span data-ttu-id="b8c96-900">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-900">Value</span></span> |
|-------|---------------------------------------------|
| <span data-ttu-id="b8c96-901">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-901">Tag</span></span>   | <span data-ttu-id="b8c96-902">0x0143</span><span class="sxs-lookup"><span data-stu-id="b8c96-902">0x0143</span></span>                                      |
| <span data-ttu-id="b8c96-903">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-903">Type</span></span>  | <span data-ttu-id="b8c96-904">PropertyTagTypeShort o PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="b8c96-904">PropertyTagTypeShort or PropertyTagTypeLong</span></span> |
| <span data-ttu-id="b8c96-905">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-905">Count</span></span> | <span data-ttu-id="b8c96-906">1</span><span class="sxs-lookup"><span data-stu-id="b8c96-906">1</span></span>                                           |



 

## <a name="propertytagtileoffset"></a><span data-ttu-id="b8c96-907">PropertyTagTileOffset</span><span class="sxs-lookup"><span data-stu-id="b8c96-907">PropertyTagTileOffset</span></span>

<span data-ttu-id="b8c96-908">Per ogni sezione, l'offset dei byte di tale riquadro.</span><span class="sxs-lookup"><span data-stu-id="b8c96-908">For each tile, the byte offset of that tile.</span></span>



| <span data-ttu-id="b8c96-909">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-909">Property info</span></span> | <span data-ttu-id="b8c96-910">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-910">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="b8c96-911">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-911">Tag</span></span>   | <span data-ttu-id="b8c96-912">0x0144</span><span class="sxs-lookup"><span data-stu-id="b8c96-912">0x0144</span></span>              |
| <span data-ttu-id="b8c96-913">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-913">Type</span></span>  | <span data-ttu-id="b8c96-914">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="b8c96-914">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="b8c96-915">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-915">Count</span></span> | <span data-ttu-id="b8c96-916">Numero di riquadri</span><span class="sxs-lookup"><span data-stu-id="b8c96-916">Number of tiles</span></span>     |



 

## <a name="propertytagtilebytecounts"></a><span data-ttu-id="b8c96-917">PropertyTagTileByteCounts</span><span class="sxs-lookup"><span data-stu-id="b8c96-917">PropertyTagTileByteCounts</span></span>

<span data-ttu-id="b8c96-918">Per ogni riquadro, il numero di byte in tale riquadro.</span><span class="sxs-lookup"><span data-stu-id="b8c96-918">For each tile, the number of bytes in that tile.</span></span>



| <span data-ttu-id="b8c96-919">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-919">Property info</span></span> | <span data-ttu-id="b8c96-920">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-920">Value</span></span> |
|-------|---------------------------------------------|
| <span data-ttu-id="b8c96-921">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-921">Tag</span></span>   | <span data-ttu-id="b8c96-922">0x0145</span><span class="sxs-lookup"><span data-stu-id="b8c96-922">0x0145</span></span>                                      |
| <span data-ttu-id="b8c96-923">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-923">Type</span></span>  | <span data-ttu-id="b8c96-924">PropertyTagTypeShort o PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="b8c96-924">PropertyTagTypeShort or PropertyTagTypeLong</span></span> |
| <span data-ttu-id="b8c96-925">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-925">Count</span></span> | <span data-ttu-id="b8c96-926">Numero di riquadri</span><span class="sxs-lookup"><span data-stu-id="b8c96-926">Number of tiles</span></span>                             |



 

## <a name="propertytaginkset"></a><span data-ttu-id="b8c96-927">PropertyTagInkSet</span><span class="sxs-lookup"><span data-stu-id="b8c96-927">PropertyTagInkSet</span></span>

<span data-ttu-id="b8c96-928">Set di inchiostri utilizzati in un'immagine separata.</span><span class="sxs-lookup"><span data-stu-id="b8c96-928">Set of inks used in a separated image.</span></span>



| <span data-ttu-id="b8c96-929">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-929">Property info</span></span> | <span data-ttu-id="b8c96-930">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-930">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="b8c96-931">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-931">Tag</span></span>   | <span data-ttu-id="b8c96-932">0x014C</span><span class="sxs-lookup"><span data-stu-id="b8c96-932">0x014C</span></span>               |
| <span data-ttu-id="b8c96-933">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-933">Type</span></span>  | <span data-ttu-id="b8c96-934">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="b8c96-934">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="b8c96-935">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-935">Count</span></span> | <span data-ttu-id="b8c96-936">1</span><span class="sxs-lookup"><span data-stu-id="b8c96-936">1</span></span>                    |



 

## <a name="propertytaginknames"></a><span data-ttu-id="b8c96-937">PropertyTagInkNames</span><span class="sxs-lookup"><span data-stu-id="b8c96-937">PropertyTagInkNames</span></span>

<span data-ttu-id="b8c96-938">Sequenza di stringhe di caratteri concatenate con terminazione null che specificano i nomi degli inchiostri utilizzati in un'immagine separata.</span><span class="sxs-lookup"><span data-stu-id="b8c96-938">Sequence of concatenated, null-terminated, character strings that specify the names of the inks used in a separated image.</span></span>



| <span data-ttu-id="b8c96-939">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-939">Property info</span></span> | <span data-ttu-id="b8c96-940">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-940">Value</span></span> |
|-------|------------------------------------------------------------------------|
| <span data-ttu-id="b8c96-941">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-941">Tag</span></span>   | <span data-ttu-id="b8c96-942">0x014D</span><span class="sxs-lookup"><span data-stu-id="b8c96-942">0x014D</span></span>                                                                 |
| <span data-ttu-id="b8c96-943">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-943">Type</span></span>  | <span data-ttu-id="b8c96-944">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="b8c96-944">PropertyTagTypeASCII</span></span>                                                   |
| <span data-ttu-id="b8c96-945">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-945">Count</span></span> | <span data-ttu-id="b8c96-946">Lunghezza totale della sequenza di stringhe, inclusi i caratteri di terminazione NULL</span><span class="sxs-lookup"><span data-stu-id="b8c96-946">Total length of the sequence of strings including the NULL terminators</span></span> |



 

## <a name="propertytagnumberofinks"></a><span data-ttu-id="b8c96-947">PropertyTagNumberOfInks</span><span class="sxs-lookup"><span data-stu-id="b8c96-947">PropertyTagNumberOfInks</span></span>

<span data-ttu-id="b8c96-948">Numero di inchiostri.</span><span class="sxs-lookup"><span data-stu-id="b8c96-948">Number of inks.</span></span>



| <span data-ttu-id="b8c96-949">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-949">Property info</span></span> | <span data-ttu-id="b8c96-950">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-950">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="b8c96-951">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-951">Tag</span></span>   | <span data-ttu-id="b8c96-952">0x014E</span><span class="sxs-lookup"><span data-stu-id="b8c96-952">0x014E</span></span>               |
| <span data-ttu-id="b8c96-953">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-953">Type</span></span>  | <span data-ttu-id="b8c96-954">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="b8c96-954">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="b8c96-955">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-955">Count</span></span> | <span data-ttu-id="b8c96-956">1</span><span class="sxs-lookup"><span data-stu-id="b8c96-956">1</span></span>                    |



 

## <a name="propertytagdotrange"></a><span data-ttu-id="b8c96-957">PropertyTagDotRange</span><span class="sxs-lookup"><span data-stu-id="b8c96-957">PropertyTagDotRange</span></span>

<span data-ttu-id="b8c96-958">Valori dei componenti colore che corrispondono a un punto 0% e a un punto 100%.</span><span class="sxs-lookup"><span data-stu-id="b8c96-958">Color component values that correspond to a 0 percent dot and a 100 percent dot.</span></span>



| <span data-ttu-id="b8c96-959">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-959">Property info</span></span> | <span data-ttu-id="b8c96-960">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-960">Value</span></span> |
|-------|---------------------------------------------|
| <span data-ttu-id="b8c96-961">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-961">Tag</span></span>   | <span data-ttu-id="b8c96-962">0x0150</span><span class="sxs-lookup"><span data-stu-id="b8c96-962">0x0150</span></span>                                      |
| <span data-ttu-id="b8c96-963">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-963">Type</span></span>  | <span data-ttu-id="b8c96-964">PropertyTagTypeByte o PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="b8c96-964">PropertyTagTypeByte or PropertyTagTypeShort</span></span> |
| <span data-ttu-id="b8c96-965">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-965">Count</span></span> | <span data-ttu-id="b8c96-966">2 o 2 × PropertyTagSamplesPerPixel</span><span class="sxs-lookup"><span data-stu-id="b8c96-966">2 or 2×PropertyTagSamplesPerPixel</span></span>           |



 

## <a name="propertytagtargetprinter"></a><span data-ttu-id="b8c96-967">PropertyTagTargetPrinter</span><span class="sxs-lookup"><span data-stu-id="b8c96-967">PropertyTagTargetPrinter</span></span>

<span data-ttu-id="b8c96-968">Stringa di caratteri con terminazione null che descrive l'ambiente di stampa previsto.</span><span class="sxs-lookup"><span data-stu-id="b8c96-968">Null-terminated character string that describes the intended printing environment.</span></span>



| <span data-ttu-id="b8c96-969">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-969">Property info</span></span> | <span data-ttu-id="b8c96-970">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-970">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="b8c96-971">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-971">Tag</span></span>   | <span data-ttu-id="b8c96-972">0x0151</span><span class="sxs-lookup"><span data-stu-id="b8c96-972">0x0151</span></span>                                             |
| <span data-ttu-id="b8c96-973">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-973">Type</span></span>  | <span data-ttu-id="b8c96-974">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="b8c96-974">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="b8c96-975">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-975">Count</span></span> | <span data-ttu-id="b8c96-976">Lunghezza della stringa che include il carattere di terminazione NULL</span><span class="sxs-lookup"><span data-stu-id="b8c96-976">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagextrasamples"></a><span data-ttu-id="b8c96-977">PropertyTagExtraSamples</span><span class="sxs-lookup"><span data-stu-id="b8c96-977">PropertyTagExtraSamples</span></span>

<span data-ttu-id="b8c96-978">Numero di componenti dei colori aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="b8c96-978">Number of extra color components.</span></span> <span data-ttu-id="b8c96-979">Ad esempio, un componente aggiuntivo potrebbe avere un valore alfa.</span><span class="sxs-lookup"><span data-stu-id="b8c96-979">For example, one extra component might hold an alpha value.</span></span>



| <span data-ttu-id="b8c96-980">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-980">Property info</span></span> | <span data-ttu-id="b8c96-981">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-981">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="b8c96-982">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-982">Tag</span></span>   | <span data-ttu-id="b8c96-983">0x0152</span><span class="sxs-lookup"><span data-stu-id="b8c96-983">0x0152</span></span>               |
| <span data-ttu-id="b8c96-984">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-984">Type</span></span>  | <span data-ttu-id="b8c96-985">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="b8c96-985">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="b8c96-986">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-986">Count</span></span> | <span data-ttu-id="b8c96-987">1</span><span class="sxs-lookup"><span data-stu-id="b8c96-987">1</span></span>                    |



 

## <a name="propertytagsampleformat"></a><span data-ttu-id="b8c96-988">PropertyTagSampleFormat</span><span class="sxs-lookup"><span data-stu-id="b8c96-988">PropertyTagSampleFormat</span></span>

<span data-ttu-id="b8c96-989">Per ogni componente del colore, formato numerico (senza segno, firmato, a virgola mobile) del componente.</span><span class="sxs-lookup"><span data-stu-id="b8c96-989">For each color component, the numerical format (unsigned, signed, floating point) of that component.</span></span> <span data-ttu-id="b8c96-990">Vedere anche [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).</span><span class="sxs-lookup"><span data-stu-id="b8c96-990">See also [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).</span></span>



| <span data-ttu-id="b8c96-991">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-991">Property info</span></span> | <span data-ttu-id="b8c96-992">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-992">Value</span></span> |
|-------|------------------------------------------|
| <span data-ttu-id="b8c96-993">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-993">Tag</span></span>   | <span data-ttu-id="b8c96-994">0x0153</span><span class="sxs-lookup"><span data-stu-id="b8c96-994">0x0153</span></span>                                   |
| <span data-ttu-id="b8c96-995">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-995">Type</span></span>  | <span data-ttu-id="b8c96-996">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="b8c96-996">PropertyTagTypeShort</span></span>                     |
| <span data-ttu-id="b8c96-997">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-997">Count</span></span> | <span data-ttu-id="b8c96-998">Numero di campioni (componenti) per pixel</span><span class="sxs-lookup"><span data-stu-id="b8c96-998">Number of samples (components) per pixel</span></span> |



 

## <a name="propertytagsminsamplevalue"></a><span data-ttu-id="b8c96-999">PropertyTagSMinSampleValue</span><span class="sxs-lookup"><span data-stu-id="b8c96-999">PropertyTagSMinSampleValue</span></span>

<span data-ttu-id="b8c96-1000">Per ogni componente del colore, valore minimo di tale componente.</span><span class="sxs-lookup"><span data-stu-id="b8c96-1000">For each color component, the minimum value of that component.</span></span> <span data-ttu-id="b8c96-1001">Vedere anche [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).</span><span class="sxs-lookup"><span data-stu-id="b8c96-1001">See also [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).</span></span>



| <span data-ttu-id="b8c96-1002">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-1002">Property info</span></span> | <span data-ttu-id="b8c96-1003">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-1003">Value</span></span> |
|-------|-----------------------------------------------------|
| <span data-ttu-id="b8c96-1004">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-1004">Tag</span></span>   | <span data-ttu-id="b8c96-1005">0x0154</span><span class="sxs-lookup"><span data-stu-id="b8c96-1005">0x0154</span></span>                                              |
| <span data-ttu-id="b8c96-1006">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-1006">Type</span></span>  | <span data-ttu-id="b8c96-1007">Il tipo più adatto ai dati del componente pixel</span><span class="sxs-lookup"><span data-stu-id="b8c96-1007">The type that best matches the pixel component data</span></span> |
| <span data-ttu-id="b8c96-1008">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-1008">Count</span></span> | <span data-ttu-id="b8c96-1009">Numero di campioni (componenti) per pixel</span><span class="sxs-lookup"><span data-stu-id="b8c96-1009">Number of samples (components) per pixel</span></span>            |



 

## <a name="propertytagsmaxsamplevalue"></a><span data-ttu-id="b8c96-1010">PropertyTagSMaxSampleValue</span><span class="sxs-lookup"><span data-stu-id="b8c96-1010">PropertyTagSMaxSampleValue</span></span>

<span data-ttu-id="b8c96-1011">Per ogni componente del colore, valore massimo di tale componente.</span><span class="sxs-lookup"><span data-stu-id="b8c96-1011">For each color component, the maximum value of that component.</span></span> <span data-ttu-id="b8c96-1012">Vedere anche [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).</span><span class="sxs-lookup"><span data-stu-id="b8c96-1012">See also [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).</span></span>



| <span data-ttu-id="b8c96-1013">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-1013">Property info</span></span> | <span data-ttu-id="b8c96-1014">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-1014">Value</span></span> |
|-------|-----------------------------------------------------|
| <span data-ttu-id="b8c96-1015">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-1015">Tag</span></span>   | <span data-ttu-id="b8c96-1016">0x0155</span><span class="sxs-lookup"><span data-stu-id="b8c96-1016">0x0155</span></span>                                              |
| <span data-ttu-id="b8c96-1017">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-1017">Type</span></span>  | <span data-ttu-id="b8c96-1018">Il tipo più adatto ai dati del componente pixel</span><span class="sxs-lookup"><span data-stu-id="b8c96-1018">The type that best matches the pixel component data</span></span> |
| <span data-ttu-id="b8c96-1019">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-1019">Count</span></span> | <span data-ttu-id="b8c96-1020">Numero di campioni (componenti) per pixel</span><span class="sxs-lookup"><span data-stu-id="b8c96-1020">Number of samples (components) per pixel</span></span>            |



 

## <a name="propertytagtransferrange"></a><span data-ttu-id="b8c96-1021">PropertyTagTransferRange</span><span class="sxs-lookup"><span data-stu-id="b8c96-1021">PropertyTagTransferRange</span></span>

<span data-ttu-id="b8c96-1022">Tabella di valori che estende l'intervallo della funzione di trasferimento.</span><span class="sxs-lookup"><span data-stu-id="b8c96-1022">Table of values that extends the range of the transfer function.</span></span>



| <span data-ttu-id="b8c96-1023">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-1023">Property info</span></span> | <span data-ttu-id="b8c96-1024">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-1024">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="b8c96-1025">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-1025">Tag</span></span>   | <span data-ttu-id="b8c96-1026">0x0156</span><span class="sxs-lookup"><span data-stu-id="b8c96-1026">0x0156</span></span>               |
| <span data-ttu-id="b8c96-1027">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-1027">Type</span></span>  | <span data-ttu-id="b8c96-1028">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="b8c96-1028">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="b8c96-1029">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-1029">Count</span></span> | <span data-ttu-id="b8c96-1030">6</span><span class="sxs-lookup"><span data-stu-id="b8c96-1030">6</span></span>                    |



 

## <a name="propertytagjpegproc"></a><span data-ttu-id="b8c96-1031">PropertyTagJPEGProc</span><span class="sxs-lookup"><span data-stu-id="b8c96-1031">PropertyTagJPEGProc</span></span>

<span data-ttu-id="b8c96-1032">Processo di compressione JPEG.</span><span class="sxs-lookup"><span data-stu-id="b8c96-1032">JPEG compression process.</span></span>



| <span data-ttu-id="b8c96-1033">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-1033">Property info</span></span> | <span data-ttu-id="b8c96-1034">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-1034">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="b8c96-1035">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-1035">Tag</span></span>   | <span data-ttu-id="b8c96-1036">0x0200</span><span class="sxs-lookup"><span data-stu-id="b8c96-1036">0x0200</span></span>               |
| <span data-ttu-id="b8c96-1037">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-1037">Type</span></span>  | <span data-ttu-id="b8c96-1038">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="b8c96-1038">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="b8c96-1039">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-1039">Count</span></span> | <span data-ttu-id="b8c96-1040">1</span><span class="sxs-lookup"><span data-stu-id="b8c96-1040">1</span></span>                    |



 

## <a name="propertytagjpeginterformat"></a><span data-ttu-id="b8c96-1041">PropertyTagJPEGInterFormat</span><span class="sxs-lookup"><span data-stu-id="b8c96-1041">PropertyTagJPEGInterFormat</span></span>

<span data-ttu-id="b8c96-1042">Offset all'inizio di un bitstream JPEG.</span><span class="sxs-lookup"><span data-stu-id="b8c96-1042">Offset to the start of a JPEG bitstream.</span></span>



| <span data-ttu-id="b8c96-1043">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-1043">Property info</span></span> | <span data-ttu-id="b8c96-1044">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-1044">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="b8c96-1045">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-1045">Tag</span></span>   | <span data-ttu-id="b8c96-1046">0x0201</span><span class="sxs-lookup"><span data-stu-id="b8c96-1046">0x0201</span></span>              |
| <span data-ttu-id="b8c96-1047">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-1047">Type</span></span>  | <span data-ttu-id="b8c96-1048">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="b8c96-1048">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="b8c96-1049">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-1049">Count</span></span> | <span data-ttu-id="b8c96-1050">1</span><span class="sxs-lookup"><span data-stu-id="b8c96-1050">1</span></span>                   |



 

## <a name="propertytagjpeginterlength"></a><span data-ttu-id="b8c96-1051">PropertyTagJPEGInterLength</span><span class="sxs-lookup"><span data-stu-id="b8c96-1051">PropertyTagJPEGInterLength</span></span>

<span data-ttu-id="b8c96-1052">Lunghezza, in byte, del file Bitstream JPEG.</span><span class="sxs-lookup"><span data-stu-id="b8c96-1052">Length, in bytes, of the JPEG bitstream.</span></span>



| <span data-ttu-id="b8c96-1053">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-1053">Property info</span></span> | <span data-ttu-id="b8c96-1054">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-1054">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="b8c96-1055">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-1055">Tag</span></span>   | <span data-ttu-id="b8c96-1056">0x0202</span><span class="sxs-lookup"><span data-stu-id="b8c96-1056">0x0202</span></span>              |
| <span data-ttu-id="b8c96-1057">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-1057">Type</span></span>  | <span data-ttu-id="b8c96-1058">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="b8c96-1058">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="b8c96-1059">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-1059">Count</span></span> | <span data-ttu-id="b8c96-1060">1</span><span class="sxs-lookup"><span data-stu-id="b8c96-1060">1</span></span>                   |



 

## <a name="propertytagjpegrestartinterval"></a><span data-ttu-id="b8c96-1061">PropertyTagJPEGRestartInterval</span><span class="sxs-lookup"><span data-stu-id="b8c96-1061">PropertyTagJPEGRestartInterval</span></span>

<span data-ttu-id="b8c96-1062">Lunghezza dell'intervallo di riavvio.</span><span class="sxs-lookup"><span data-stu-id="b8c96-1062">Length of the restart interval.</span></span>



| <span data-ttu-id="b8c96-1063">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-1063">Property info</span></span> | <span data-ttu-id="b8c96-1064">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-1064">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="b8c96-1065">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-1065">Tag</span></span>   | <span data-ttu-id="b8c96-1066">0x0203</span><span class="sxs-lookup"><span data-stu-id="b8c96-1066">0x0203</span></span>               |
| <span data-ttu-id="b8c96-1067">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-1067">Type</span></span>  | <span data-ttu-id="b8c96-1068">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="b8c96-1068">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="b8c96-1069">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-1069">Count</span></span> | <span data-ttu-id="b8c96-1070">1</span><span class="sxs-lookup"><span data-stu-id="b8c96-1070">1</span></span>                    |



 

## <a name="propertytagjpeglosslesspredictors"></a><span data-ttu-id="b8c96-1071">PropertyTagJPEGLosslessPredictors</span><span class="sxs-lookup"><span data-stu-id="b8c96-1071">PropertyTagJPEGLosslessPredictors</span></span>

<span data-ttu-id="b8c96-1072">Per ogni componente del colore, valore di predittore senza perdita di selezione per il componente.</span><span class="sxs-lookup"><span data-stu-id="b8c96-1072">For each color component, a lossless predictor-selection value for that component.</span></span> <span data-ttu-id="b8c96-1073">Vedere anche [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).</span><span class="sxs-lookup"><span data-stu-id="b8c96-1073">See also [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).</span></span>



| <span data-ttu-id="b8c96-1074">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-1074">Property info</span></span> | <span data-ttu-id="b8c96-1075">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-1075">Value</span></span> |
|-------|------------------------------------------|
| <span data-ttu-id="b8c96-1076">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-1076">Tag</span></span>   | <span data-ttu-id="b8c96-1077">0x0205</span><span class="sxs-lookup"><span data-stu-id="b8c96-1077">0x0205</span></span>                                   |
| <span data-ttu-id="b8c96-1078">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-1078">Type</span></span>  | <span data-ttu-id="b8c96-1079">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="b8c96-1079">PropertyTagTypeShort</span></span>                     |
| <span data-ttu-id="b8c96-1080">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-1080">Count</span></span> | <span data-ttu-id="b8c96-1081">Numero di campioni (componenti) per pixel</span><span class="sxs-lookup"><span data-stu-id="b8c96-1081">Number of samples (components) per pixel</span></span> |



 

## <a name="propertytagjpegpointtransforms"></a><span data-ttu-id="b8c96-1082">PropertyTagJPEGPointTransforms</span><span class="sxs-lookup"><span data-stu-id="b8c96-1082">PropertyTagJPEGPointTransforms</span></span>

<span data-ttu-id="b8c96-1083">Per ogni componente del colore, un valore di trasformazione punto per tale componente.</span><span class="sxs-lookup"><span data-stu-id="b8c96-1083">For each color component, a point transformation value for that component.</span></span> <span data-ttu-id="b8c96-1084">Vedere anche [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).</span><span class="sxs-lookup"><span data-stu-id="b8c96-1084">See also [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).</span></span>



| <span data-ttu-id="b8c96-1085">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-1085">Property info</span></span> | <span data-ttu-id="b8c96-1086">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-1086">Value</span></span> |
|-------|------------------------------------------|
| <span data-ttu-id="b8c96-1087">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-1087">Tag</span></span>   | <span data-ttu-id="b8c96-1088">0x0206</span><span class="sxs-lookup"><span data-stu-id="b8c96-1088">0x0206</span></span>                                   |
| <span data-ttu-id="b8c96-1089">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-1089">Type</span></span>  | <span data-ttu-id="b8c96-1090">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="b8c96-1090">PropertyTagTypeShort</span></span>                     |
| <span data-ttu-id="b8c96-1091">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-1091">Count</span></span> | <span data-ttu-id="b8c96-1092">Numero di campioni (componenti) per pixel</span><span class="sxs-lookup"><span data-stu-id="b8c96-1092">Number of samples (components) per pixel</span></span> |



 

## <a name="propertytagjpegqtables"></a><span data-ttu-id="b8c96-1093">PropertyTagJPEGQTables</span><span class="sxs-lookup"><span data-stu-id="b8c96-1093">PropertyTagJPEGQTables</span></span>

<span data-ttu-id="b8c96-1094">Per ogni componente del colore, offset della tabella di quantizzazione per il componente.</span><span class="sxs-lookup"><span data-stu-id="b8c96-1094">For each color component, the offset to the quantization table for that component.</span></span> <span data-ttu-id="b8c96-1095">Vedere anche [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).</span><span class="sxs-lookup"><span data-stu-id="b8c96-1095">See also [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).</span></span>



| <span data-ttu-id="b8c96-1096">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-1096">Property info</span></span> | <span data-ttu-id="b8c96-1097">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-1097">Value</span></span> |
|-------|------------------------------------------|
| <span data-ttu-id="b8c96-1098">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-1098">Tag</span></span>   | <span data-ttu-id="b8c96-1099">0x0207</span><span class="sxs-lookup"><span data-stu-id="b8c96-1099">0x0207</span></span>                                   |
| <span data-ttu-id="b8c96-1100">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-1100">Type</span></span>  | <span data-ttu-id="b8c96-1101">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="b8c96-1101">PropertyTagTypeLong</span></span>                      |
| <span data-ttu-id="b8c96-1102">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-1102">Count</span></span> | <span data-ttu-id="b8c96-1103">Numero di campioni (componenti) per pixel</span><span class="sxs-lookup"><span data-stu-id="b8c96-1103">Number of samples (components) per pixel</span></span> |



 

## <a name="propertytagjpegdctables"></a><span data-ttu-id="b8c96-1104">PropertyTagJPEGDCTables</span><span class="sxs-lookup"><span data-stu-id="b8c96-1104">PropertyTagJPEGDCTables</span></span>

<span data-ttu-id="b8c96-1105">Per ogni componente del colore, l'offset della tabella di Huffman del controller di dominio (o della tabella Huffman) per quel componente.</span><span class="sxs-lookup"><span data-stu-id="b8c96-1105">For each color component, the offset to the DC Huffman table (or lossless Huffman table) for that component.</span></span> <span data-ttu-id="b8c96-1106">Vedere anche [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).</span><span class="sxs-lookup"><span data-stu-id="b8c96-1106">See also [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).</span></span>



| <span data-ttu-id="b8c96-1107">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-1107">Property info</span></span> | <span data-ttu-id="b8c96-1108">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-1108">Value</span></span> |
|-------|------------------------------------------|
| <span data-ttu-id="b8c96-1109">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-1109">Tag</span></span>   | <span data-ttu-id="b8c96-1110">0x0208</span><span class="sxs-lookup"><span data-stu-id="b8c96-1110">0x0208</span></span>                                   |
| <span data-ttu-id="b8c96-1111">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-1111">Type</span></span>  | <span data-ttu-id="b8c96-1112">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="b8c96-1112">PropertyTagTypeLong</span></span>                      |
| <span data-ttu-id="b8c96-1113">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-1113">Count</span></span> | <span data-ttu-id="b8c96-1114">Numero di campioni (componenti) per pixel</span><span class="sxs-lookup"><span data-stu-id="b8c96-1114">Number of samples (components) per pixel</span></span> |



 

## <a name="propertytagjpegactables"></a><span data-ttu-id="b8c96-1115">PropertyTagJPEGACTables</span><span class="sxs-lookup"><span data-stu-id="b8c96-1115">PropertyTagJPEGACTables</span></span>

<span data-ttu-id="b8c96-1116">Per ogni componente del colore, l'offset alla tabella del Huffman AC per quel componente.</span><span class="sxs-lookup"><span data-stu-id="b8c96-1116">For each color component, the offset to the AC Huffman table for that component.</span></span> <span data-ttu-id="b8c96-1117">Vedere anche [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).</span><span class="sxs-lookup"><span data-stu-id="b8c96-1117">See also [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel).</span></span>



| <span data-ttu-id="b8c96-1118">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-1118">Property info</span></span> | <span data-ttu-id="b8c96-1119">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-1119">Value</span></span> |
|-------|------------------------------------------|
| <span data-ttu-id="b8c96-1120">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-1120">Tag</span></span>   | <span data-ttu-id="b8c96-1121">0x0209</span><span class="sxs-lookup"><span data-stu-id="b8c96-1121">0x0209</span></span>                                   |
| <span data-ttu-id="b8c96-1122">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-1122">Type</span></span>  | <span data-ttu-id="b8c96-1123">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="b8c96-1123">PropertyTagTypeLong</span></span>                      |
| <span data-ttu-id="b8c96-1124">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-1124">Count</span></span> | <span data-ttu-id="b8c96-1125">Numero di campioni (componenti) per pixel</span><span class="sxs-lookup"><span data-stu-id="b8c96-1125">Number of samples (components) per pixel</span></span> |



 

## <a name="propertytagycbcrcoefficients"></a><span data-ttu-id="b8c96-1126">PropertyTagYCbCrCoefficients</span><span class="sxs-lookup"><span data-stu-id="b8c96-1126">PropertyTagYCbCrCoefficients</span></span>

<span data-ttu-id="b8c96-1127">Coefficienti per la trasformazione da RGB a dati di immagine YCbCr.</span><span class="sxs-lookup"><span data-stu-id="b8c96-1127">Coefficients for transformation from RGB to YCbCr image data.</span></span>



| <span data-ttu-id="b8c96-1128">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-1128">Property info</span></span> | <span data-ttu-id="b8c96-1129">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-1129">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="b8c96-1130">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-1130">Tag</span></span>   | <span data-ttu-id="b8c96-1131">0x0211</span><span class="sxs-lookup"><span data-stu-id="b8c96-1131">0x0211</span></span>                  |
| <span data-ttu-id="b8c96-1132">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-1132">Type</span></span>  | <span data-ttu-id="b8c96-1133">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="b8c96-1133">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="b8c96-1134">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-1134">Count</span></span> | <span data-ttu-id="b8c96-1135">3</span><span class="sxs-lookup"><span data-stu-id="b8c96-1135">3</span></span>                       |



 

## <a name="propertytagycbcrsubsampling"></a><span data-ttu-id="b8c96-1136">PropertyTagYCbCrSubsampling</span><span class="sxs-lookup"><span data-stu-id="b8c96-1136">PropertyTagYCbCrSubsampling</span></span>

<span data-ttu-id="b8c96-1137">Rapporto di campionamento dei componenti cromatura in relazione al componente luminanza.</span><span class="sxs-lookup"><span data-stu-id="b8c96-1137">Sampling ratio of chrominance components in relation to the luminance component.</span></span>



| <span data-ttu-id="b8c96-1138">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-1138">Property info</span></span> | <span data-ttu-id="b8c96-1139">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-1139">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="b8c96-1140">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-1140">Tag</span></span>   | <span data-ttu-id="b8c96-1141">0x0212</span><span class="sxs-lookup"><span data-stu-id="b8c96-1141">0x0212</span></span>               |
| <span data-ttu-id="b8c96-1142">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-1142">Type</span></span>  | <span data-ttu-id="b8c96-1143">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="b8c96-1143">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="b8c96-1144">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-1144">Count</span></span> | <span data-ttu-id="b8c96-1145">2</span><span class="sxs-lookup"><span data-stu-id="b8c96-1145">2</span></span>                    |



 

## <a name="propertytagycbcrpositioning"></a><span data-ttu-id="b8c96-1146">PropertyTagYCbCrPositioning</span><span class="sxs-lookup"><span data-stu-id="b8c96-1146">PropertyTagYCbCrPositioning</span></span>

<span data-ttu-id="b8c96-1147">Posizione dei componenti cromatura in relazione al componente di luminanza.</span><span class="sxs-lookup"><span data-stu-id="b8c96-1147">Position of chrominance components in relation to the luminance component.</span></span>



| <span data-ttu-id="b8c96-1148">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-1148">Property info</span></span> | <span data-ttu-id="b8c96-1149">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-1149">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="b8c96-1150">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-1150">Tag</span></span>   | <span data-ttu-id="b8c96-1151">0x0213</span><span class="sxs-lookup"><span data-stu-id="b8c96-1151">0x0213</span></span>               |
| <span data-ttu-id="b8c96-1152">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-1152">Type</span></span>  | <span data-ttu-id="b8c96-1153">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="b8c96-1153">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="b8c96-1154">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-1154">Count</span></span> | <span data-ttu-id="b8c96-1155">1</span><span class="sxs-lookup"><span data-stu-id="b8c96-1155">1</span></span>                    |



 

## <a name="propertytagrefblackwhite"></a><span data-ttu-id="b8c96-1156">PropertyTagREFBlackWhite</span><span class="sxs-lookup"><span data-stu-id="b8c96-1156">PropertyTagREFBlackWhite</span></span>

<span data-ttu-id="b8c96-1157">Valore punto nero di riferimento e valore punto bianco di riferimento.</span><span class="sxs-lookup"><span data-stu-id="b8c96-1157">Reference black point value and reference white point value.</span></span>



| <span data-ttu-id="b8c96-1158">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-1158">Property info</span></span> | <span data-ttu-id="b8c96-1159">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-1159">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="b8c96-1160">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-1160">Tag</span></span>   | <span data-ttu-id="b8c96-1161">0x0214</span><span class="sxs-lookup"><span data-stu-id="b8c96-1161">0x0214</span></span>                  |
| <span data-ttu-id="b8c96-1162">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-1162">Type</span></span>  | <span data-ttu-id="b8c96-1163">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="b8c96-1163">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="b8c96-1164">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-1164">Count</span></span> | <span data-ttu-id="b8c96-1165">6</span><span class="sxs-lookup"><span data-stu-id="b8c96-1165">6</span></span>                       |



 

## <a name="propertytaggamma"></a><span data-ttu-id="b8c96-1166">PropertyTagGamma</span><span class="sxs-lookup"><span data-stu-id="b8c96-1166">PropertyTagGamma</span></span>

<span data-ttu-id="b8c96-1167">Valore gamma associato all'immagine.</span><span class="sxs-lookup"><span data-stu-id="b8c96-1167">Gamma value attached to the image.</span></span> <span data-ttu-id="b8c96-1168">Il valore gamma viene archiviato come numero razionale (coppia di **caratteri Long**) con un numeratore di 100000.</span><span class="sxs-lookup"><span data-stu-id="b8c96-1168">The gamma value is stored as a rational number (pair of **long**) with a numerator of 100000.</span></span> <span data-ttu-id="b8c96-1169">Ad esempio, un valore gamma di 2,2 viene archiviato come coppia (100000, 45455).</span><span class="sxs-lookup"><span data-stu-id="b8c96-1169">For example, a gamma value of 2.2 is stored as the pair (100000, 45455).</span></span>



| <span data-ttu-id="b8c96-1170">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-1170">Property info</span></span> | <span data-ttu-id="b8c96-1171">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-1171">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="b8c96-1172">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-1172">Tag</span></span>   | <span data-ttu-id="b8c96-1173">0x0301</span><span class="sxs-lookup"><span data-stu-id="b8c96-1173">0x0301</span></span>                  |
| <span data-ttu-id="b8c96-1174">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-1174">Type</span></span>  | <span data-ttu-id="b8c96-1175">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="b8c96-1175">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="b8c96-1176">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-1176">Count</span></span> | <span data-ttu-id="b8c96-1177">1</span><span class="sxs-lookup"><span data-stu-id="b8c96-1177">1</span></span>                       |



 

## <a name="propertytagiccprofiledescriptor"></a><span data-ttu-id="b8c96-1178">PropertyTagICCProfileDescriptor</span><span class="sxs-lookup"><span data-stu-id="b8c96-1178">PropertyTagICCProfileDescriptor</span></span>

<span data-ttu-id="b8c96-1179">Stringa di caratteri con terminazione null che identifica un profilo ICC.</span><span class="sxs-lookup"><span data-stu-id="b8c96-1179">Null-terminated character string that identifies an ICC profile.</span></span>



| <span data-ttu-id="b8c96-1180">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-1180">Property info</span></span> | <span data-ttu-id="b8c96-1181">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-1181">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="b8c96-1182">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-1182">Tag</span></span>   | <span data-ttu-id="b8c96-1183">0x0302</span><span class="sxs-lookup"><span data-stu-id="b8c96-1183">0x0302</span></span>                                             |
| <span data-ttu-id="b8c96-1184">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-1184">Type</span></span>  | <span data-ttu-id="b8c96-1185">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="b8c96-1185">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="b8c96-1186">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-1186">Count</span></span> | <span data-ttu-id="b8c96-1187">Lunghezza della stringa che include il carattere di terminazione NULL</span><span class="sxs-lookup"><span data-stu-id="b8c96-1187">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagsrgbrenderingintent"></a><span data-ttu-id="b8c96-1188">PropertyTagSRGBRenderingIntent</span><span class="sxs-lookup"><span data-stu-id="b8c96-1188">PropertyTagSRGBRenderingIntent</span></span>

<span data-ttu-id="b8c96-1189">Modalità di visualizzazione dell'immagine in base a quanto definito da International Color Consortium (ICC).</span><span class="sxs-lookup"><span data-stu-id="b8c96-1189">How the image should be displayed as defined by the International Color Consortium (ICC).</span></span> <span data-ttu-id="b8c96-1190">Se un oggetto  [**immagine**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) GDI+ viene costruito con il parametro *UseEmbeddedColorManagement* impostato su **true**, GDI+ esegue il rendering dell'immagine in base alla finalità di rendering specificata.</span><span class="sxs-lookup"><span data-stu-id="b8c96-1190">If a GDI+  [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object is constructed with the *useEmbeddedColorManagement* parameter set to **TRUE**, then GDI+ renders the image according to the specified rendering intent.</span></span> <span data-ttu-id="b8c96-1191">Lo scopo può essere impostato su percettivo, colorimetrico relativo, saturazione o colorimetrico assoluto.</span><span class="sxs-lookup"><span data-stu-id="b8c96-1191">The intent can be set to perceptual, relative colorimetric, saturation, or absolute colorimetric.</span></span>

-   <span data-ttu-id="b8c96-1192">Finalità percettiva, ideale per le fotografie, offre un adattamento ottimale alla gamma di dispositivi di visualizzazione a scapito dell'accuratezza di colorimetrico.</span><span class="sxs-lookup"><span data-stu-id="b8c96-1192">Perceptual intent, which is suitable for photographs, gives good adaptation to the display device gamut at the expense of colorimetric accuracy.</span></span>
-   <span data-ttu-id="b8c96-1193">La finalità colorimetrico relativa è adatta per le immagini (ad esempio, i loghi) che richiedono la corrispondenza dell'aspetto dei colori rispetto al punto bianco del dispositivo di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="b8c96-1193">Relative colorimetric intent is suitable for images (for example, logos) that require color appearance matching that is relative to the display device white point.</span></span>
-   <span data-ttu-id="b8c96-1194">Il livello di saturazione, adatto per grafici e grafici, conserva la saturazione a scapito di tonalità e luminosità.</span><span class="sxs-lookup"><span data-stu-id="b8c96-1194">Saturation intent, which is suitable for charts and graphs, preserves saturation at the expense of hue and lightness.</span></span>
-   <span data-ttu-id="b8c96-1195">Lo scopo di colorimetrico assoluto è adatto alle prove (anteprime delle immagini destinate a un dispositivo di visualizzazione diverso) che richiedono la conservazione dei colorimetria assoluti.</span><span class="sxs-lookup"><span data-stu-id="b8c96-1195">Absolute colorimetric intent is suitable for proofs (previews of images destined for a different display device) that require preservation of absolute colorimetry.</span></span>



<span data-ttu-id="b8c96-1196">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-1196">Tag</span></span>

<span data-ttu-id="b8c96-1197">0x0303</span><span class="sxs-lookup"><span data-stu-id="b8c96-1197">0x0303</span></span>

<span data-ttu-id="b8c96-1198">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-1198">Type</span></span>

<span data-ttu-id="b8c96-1199">BYTE</span><span class="sxs-lookup"><span data-stu-id="b8c96-1199">BYTE</span></span>

<span data-ttu-id="b8c96-1200">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-1200">Count</span></span>

<span data-ttu-id="b8c96-1201">1</span><span class="sxs-lookup"><span data-stu-id="b8c96-1201">1</span></span>

<span data-ttu-id="b8c96-1202">0-percettivo 1: colorimetrico relativo 2-saturazione 3-colorimetrico assoluto</span><span class="sxs-lookup"><span data-stu-id="b8c96-1202">0 - perceptual 1 - relative colorimetric 2 - saturation 3 - absolute colorimetric</span></span>



 

## <a name="propertytagimagetitle"></a><span data-ttu-id="b8c96-1203">PropertyTagImageTitle</span><span class="sxs-lookup"><span data-stu-id="b8c96-1203">PropertyTagImageTitle</span></span>

<span data-ttu-id="b8c96-1204">Stringa di caratteri con terminazione null che specifica il titolo dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="b8c96-1204">Null-terminated character string that specifies the title of the image.</span></span>



| <span data-ttu-id="b8c96-1205">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-1205">Property info</span></span> | <span data-ttu-id="b8c96-1206">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-1206">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="b8c96-1207">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-1207">Tag</span></span>   | <span data-ttu-id="b8c96-1208">0x0320</span><span class="sxs-lookup"><span data-stu-id="b8c96-1208">0x0320</span></span>                                             |
| <span data-ttu-id="b8c96-1209">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-1209">Type</span></span>  | <span data-ttu-id="b8c96-1210">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="b8c96-1210">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="b8c96-1211">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-1211">Count</span></span> | <span data-ttu-id="b8c96-1212">Lunghezza della stringa che include il carattere di terminazione NULL</span><span class="sxs-lookup"><span data-stu-id="b8c96-1212">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagresolutionxunit"></a><span data-ttu-id="b8c96-1213">PropertyTagResolutionXUnit</span><span class="sxs-lookup"><span data-stu-id="b8c96-1213">PropertyTagResolutionXUnit</span></span>

<span data-ttu-id="b8c96-1214">Unità in cui visualizzare la risoluzione orizzontale.</span><span class="sxs-lookup"><span data-stu-id="b8c96-1214">Units in which to display horizontal resolution.</span></span>



<span data-ttu-id="b8c96-1215">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-1215">Tag</span></span>

<span data-ttu-id="b8c96-1216">0x5001</span><span class="sxs-lookup"><span data-stu-id="b8c96-1216">0x5001</span></span>

<span data-ttu-id="b8c96-1217">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-1217">Type</span></span>

<span data-ttu-id="b8c96-1218">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="b8c96-1218">PropertyTagTypeShort</span></span>

<span data-ttu-id="b8c96-1219">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-1219">Count</span></span>

<span data-ttu-id="b8c96-1220">1</span><span class="sxs-lookup"><span data-stu-id="b8c96-1220">1</span></span>

<span data-ttu-id="b8c96-1221">1-pixel per pollice 2-pixel per centimetro</span><span class="sxs-lookup"><span data-stu-id="b8c96-1221">1 - pixels per inch 2 - pixels per centimeter</span></span>



 

## <a name="propertytagresolutionyunit"></a><span data-ttu-id="b8c96-1222">PropertyTagResolutionYUnit</span><span class="sxs-lookup"><span data-stu-id="b8c96-1222">PropertyTagResolutionYUnit</span></span>

<span data-ttu-id="b8c96-1223">Unità in cui visualizzare la risoluzione verticale.</span><span class="sxs-lookup"><span data-stu-id="b8c96-1223">Units in which to display vertical resolution.</span></span>



<span data-ttu-id="b8c96-1224">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-1224">Tag</span></span>

<span data-ttu-id="b8c96-1225">0x5002</span><span class="sxs-lookup"><span data-stu-id="b8c96-1225">0x5002</span></span>

<span data-ttu-id="b8c96-1226">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-1226">Type</span></span>

<span data-ttu-id="b8c96-1227">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="b8c96-1227">PropertyTagTypeShort</span></span>

<span data-ttu-id="b8c96-1228">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-1228">Count</span></span>

<span data-ttu-id="b8c96-1229">1</span><span class="sxs-lookup"><span data-stu-id="b8c96-1229">1</span></span>

<span data-ttu-id="b8c96-1230">1-pixel per pollice 2-pixel per centimetro</span><span class="sxs-lookup"><span data-stu-id="b8c96-1230">1 - pixels per inch 2 - pixels per centimeter</span></span>



 

## <a name="propertytagresolutionxlengthunit"></a><span data-ttu-id="b8c96-1231">PropertyTagResolutionXLengthUnit</span><span class="sxs-lookup"><span data-stu-id="b8c96-1231">PropertyTagResolutionXLengthUnit</span></span>

<span data-ttu-id="b8c96-1232">Unità in cui visualizzare la larghezza dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="b8c96-1232">Units in which to display the image width.</span></span>



<span data-ttu-id="b8c96-1233">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-1233">Tag</span></span>

<span data-ttu-id="b8c96-1234">0x5003</span><span class="sxs-lookup"><span data-stu-id="b8c96-1234">0x5003</span></span>

<span data-ttu-id="b8c96-1235">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-1235">Type</span></span>

<span data-ttu-id="b8c96-1236">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="b8c96-1236">PropertyTagTypeShort</span></span>

<span data-ttu-id="b8c96-1237">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-1237">Count</span></span>

<span data-ttu-id="b8c96-1238">1</span><span class="sxs-lookup"><span data-stu-id="b8c96-1238">1</span></span>

<span data-ttu-id="b8c96-1239">1-pollici 2-centimetri 3-punti 4-Pica 5-colonne</span><span class="sxs-lookup"><span data-stu-id="b8c96-1239">1 - inches 2 - centimeters 3 - points 4 - picas 5 - columns</span></span>



 

## <a name="propertytagresolutionylengthunit"></a><span data-ttu-id="b8c96-1240">PropertyTagResolutionYLengthUnit</span><span class="sxs-lookup"><span data-stu-id="b8c96-1240">PropertyTagResolutionYLengthUnit</span></span>

<span data-ttu-id="b8c96-1241">Unità in cui visualizzare l'altezza dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="b8c96-1241">Units in which to display the image height.</span></span>



<span data-ttu-id="b8c96-1242">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-1242">Tag</span></span>

<span data-ttu-id="b8c96-1243">0x5004</span><span class="sxs-lookup"><span data-stu-id="b8c96-1243">0x5004</span></span>

<span data-ttu-id="b8c96-1244">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-1244">Type</span></span>

<span data-ttu-id="b8c96-1245">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="b8c96-1245">PropertyTagTypeShort</span></span>

<span data-ttu-id="b8c96-1246">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-1246">Count</span></span>

<span data-ttu-id="b8c96-1247">1</span><span class="sxs-lookup"><span data-stu-id="b8c96-1247">1</span></span>

<span data-ttu-id="b8c96-1248">1-pollici 2-centimetri 3-punti 4-Pica 5-colonne</span><span class="sxs-lookup"><span data-stu-id="b8c96-1248">1 - inches 2 - centimeters 3 - points 4 - picas 5 - columns</span></span>



 

## <a name="propertytagprintflags"></a><span data-ttu-id="b8c96-1249">PropertyTagPrintFlags</span><span class="sxs-lookup"><span data-stu-id="b8c96-1249">PropertyTagPrintFlags</span></span>

<span data-ttu-id="b8c96-1250">Sequenza di valori booleani a un byte che specificano le opzioni di stampa.</span><span class="sxs-lookup"><span data-stu-id="b8c96-1250">Sequence of one-byte Boolean values that specify printing options.</span></span>



| <span data-ttu-id="b8c96-1251">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-1251">Property info</span></span> | <span data-ttu-id="b8c96-1252">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-1252">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="b8c96-1253">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-1253">Tag</span></span>   | <span data-ttu-id="b8c96-1254">0x5005</span><span class="sxs-lookup"><span data-stu-id="b8c96-1254">0x5005</span></span>               |
| <span data-ttu-id="b8c96-1255">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-1255">Type</span></span>  | <span data-ttu-id="b8c96-1256">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="b8c96-1256">PropertyTagTypeASCII</span></span> |
| <span data-ttu-id="b8c96-1257">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-1257">Count</span></span> | <span data-ttu-id="b8c96-1258">Numero di flag</span><span class="sxs-lookup"><span data-stu-id="b8c96-1258">Number of flags</span></span>      |



 

## <a name="propertytagprintflagsversion"></a><span data-ttu-id="b8c96-1259">PropertyTagPrintFlagsVersion</span><span class="sxs-lookup"><span data-stu-id="b8c96-1259">PropertyTagPrintFlagsVersion</span></span>

<span data-ttu-id="b8c96-1260">Versione dei flag di stampa.</span><span class="sxs-lookup"><span data-stu-id="b8c96-1260">Print flags version.</span></span>



| <span data-ttu-id="b8c96-1261">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-1261">Property info</span></span> | <span data-ttu-id="b8c96-1262">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-1262">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="b8c96-1263">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-1263">Tag</span></span>   | <span data-ttu-id="b8c96-1264">0x5006</span><span class="sxs-lookup"><span data-stu-id="b8c96-1264">0x5006</span></span>               |
| <span data-ttu-id="b8c96-1265">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-1265">Type</span></span>  | <span data-ttu-id="b8c96-1266">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="b8c96-1266">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="b8c96-1267">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-1267">Count</span></span> | <span data-ttu-id="b8c96-1268">1</span><span class="sxs-lookup"><span data-stu-id="b8c96-1268">1</span></span>                    |



 

## <a name="propertytagprintflagscrop"></a><span data-ttu-id="b8c96-1269">PropertyTagPrintFlagsCrop</span><span class="sxs-lookup"><span data-stu-id="b8c96-1269">PropertyTagPrintFlagsCrop</span></span>

<span data-ttu-id="b8c96-1270">Segni di ritaglio al centro di flag di stampa.</span><span class="sxs-lookup"><span data-stu-id="b8c96-1270">Print flags center crop marks.</span></span>



| <span data-ttu-id="b8c96-1271">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-1271">Property info</span></span> | <span data-ttu-id="b8c96-1272">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-1272">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="b8c96-1273">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-1273">Tag</span></span>   | <span data-ttu-id="b8c96-1274">0x5007</span><span class="sxs-lookup"><span data-stu-id="b8c96-1274">0x5007</span></span>              |
| <span data-ttu-id="b8c96-1275">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-1275">Type</span></span>  | <span data-ttu-id="b8c96-1276">PropertyTagTypeByte</span><span class="sxs-lookup"><span data-stu-id="b8c96-1276">PropertyTagTypeByte</span></span> |
| <span data-ttu-id="b8c96-1277">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-1277">Count</span></span> | <span data-ttu-id="b8c96-1278">1</span><span class="sxs-lookup"><span data-stu-id="b8c96-1278">1</span></span>                   |



 

## <a name="propertytagprintflagsbleedwidth"></a><span data-ttu-id="b8c96-1279">PropertyTagPrintFlagsBleedWidth</span><span class="sxs-lookup"><span data-stu-id="b8c96-1279">PropertyTagPrintFlagsBleedWidth</span></span>

<span data-ttu-id="b8c96-1280">Larghezza del Bleed del flag di stampa.</span><span class="sxs-lookup"><span data-stu-id="b8c96-1280">Print flags bleed width.</span></span>



| <span data-ttu-id="b8c96-1281">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-1281">Property info</span></span> | <span data-ttu-id="b8c96-1282">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-1282">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="b8c96-1283">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-1283">Tag</span></span>   | <span data-ttu-id="b8c96-1284">0x5008</span><span class="sxs-lookup"><span data-stu-id="b8c96-1284">0x5008</span></span>              |
| <span data-ttu-id="b8c96-1285">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-1285">Type</span></span>  | <span data-ttu-id="b8c96-1286">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="b8c96-1286">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="b8c96-1287">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-1287">Count</span></span> | <span data-ttu-id="b8c96-1288">1</span><span class="sxs-lookup"><span data-stu-id="b8c96-1288">1</span></span>                   |



 

## <a name="propertytagprintflagsbleedwidthscale"></a><span data-ttu-id="b8c96-1289">PropertyTagPrintFlagsBleedWidthScale</span><span class="sxs-lookup"><span data-stu-id="b8c96-1289">PropertyTagPrintFlagsBleedWidthScale</span></span>

<span data-ttu-id="b8c96-1290">Ridimensionamento della larghezza del Bleed del flag di stampa.</span><span class="sxs-lookup"><span data-stu-id="b8c96-1290">Print flags bleed width scale.</span></span>



| <span data-ttu-id="b8c96-1291">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-1291">Property info</span></span> | <span data-ttu-id="b8c96-1292">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-1292">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="b8c96-1293">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-1293">Tag</span></span>   | <span data-ttu-id="b8c96-1294">0x5009</span><span class="sxs-lookup"><span data-stu-id="b8c96-1294">0x5009</span></span>               |
| <span data-ttu-id="b8c96-1295">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-1295">Type</span></span>  | <span data-ttu-id="b8c96-1296">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="b8c96-1296">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="b8c96-1297">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-1297">Count</span></span> | <span data-ttu-id="b8c96-1298">1</span><span class="sxs-lookup"><span data-stu-id="b8c96-1298">1</span></span>                    |



 

## <a name="propertytaghalftonelpi"></a><span data-ttu-id="b8c96-1299">PropertyTagHalftoneLPI</span><span class="sxs-lookup"><span data-stu-id="b8c96-1299">PropertyTagHalftoneLPI</span></span>

<span data-ttu-id="b8c96-1300">Frequenza dello schermo dell'input penna, in linee per pollice.</span><span class="sxs-lookup"><span data-stu-id="b8c96-1300">Ink's screen frequency, in lines per inch.</span></span>



| <span data-ttu-id="b8c96-1301">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-1301">Property info</span></span> | <span data-ttu-id="b8c96-1302">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-1302">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="b8c96-1303">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-1303">Tag</span></span>   | <span data-ttu-id="b8c96-1304">0x500A</span><span class="sxs-lookup"><span data-stu-id="b8c96-1304">0x500A</span></span>                  |
| <span data-ttu-id="b8c96-1305">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-1305">Type</span></span>  | <span data-ttu-id="b8c96-1306">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="b8c96-1306">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="b8c96-1307">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-1307">Count</span></span> | <span data-ttu-id="b8c96-1308">1</span><span class="sxs-lookup"><span data-stu-id="b8c96-1308">1</span></span>                       |



 

## <a name="propertytaghalftonelpiunit"></a><span data-ttu-id="b8c96-1309">PropertyTagHalftoneLPIUnit</span><span class="sxs-lookup"><span data-stu-id="b8c96-1309">PropertyTagHalftoneLPIUnit</span></span>

<span data-ttu-id="b8c96-1310">Unità per la frequenza dello schermo.</span><span class="sxs-lookup"><span data-stu-id="b8c96-1310">Units for the screen frequency.</span></span>



<span data-ttu-id="b8c96-1311">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-1311">Tag</span></span>

<span data-ttu-id="b8c96-1312">0x500B</span><span class="sxs-lookup"><span data-stu-id="b8c96-1312">0x500B</span></span>

<span data-ttu-id="b8c96-1313">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-1313">Type</span></span>

<span data-ttu-id="b8c96-1314">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="b8c96-1314">PropertyTagTypeShort</span></span>

<span data-ttu-id="b8c96-1315">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-1315">Count</span></span>

<span data-ttu-id="b8c96-1316">1</span><span class="sxs-lookup"><span data-stu-id="b8c96-1316">1</span></span>

<span data-ttu-id="b8c96-1317">1-righe per pollice 2-linee per centimetro</span><span class="sxs-lookup"><span data-stu-id="b8c96-1317">1 - lines per inch 2 - lines per centimeter</span></span>



 

## <a name="propertytaghalftonedegree"></a><span data-ttu-id="b8c96-1318">PropertyTagHalftoneDegree</span><span class="sxs-lookup"><span data-stu-id="b8c96-1318">PropertyTagHalftoneDegree</span></span>

<span data-ttu-id="b8c96-1319">Angolo per lo schermo.</span><span class="sxs-lookup"><span data-stu-id="b8c96-1319">Angle for screen.</span></span>



| <span data-ttu-id="b8c96-1320">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-1320">Property info</span></span> | <span data-ttu-id="b8c96-1321">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-1321">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="b8c96-1322">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-1322">Tag</span></span>   | <span data-ttu-id="b8c96-1323">0x500C</span><span class="sxs-lookup"><span data-stu-id="b8c96-1323">0x500C</span></span>                  |
| <span data-ttu-id="b8c96-1324">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-1324">Type</span></span>  | <span data-ttu-id="b8c96-1325">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="b8c96-1325">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="b8c96-1326">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-1326">Count</span></span> | <span data-ttu-id="b8c96-1327">1</span><span class="sxs-lookup"><span data-stu-id="b8c96-1327">1</span></span>                       |



 

## <a name="propertytaghalftoneshape"></a><span data-ttu-id="b8c96-1328">PropertyTagHalftoneShape</span><span class="sxs-lookup"><span data-stu-id="b8c96-1328">PropertyTagHalftoneShape</span></span>

<span data-ttu-id="b8c96-1329">Forma dei punti di mezzitoni.</span><span class="sxs-lookup"><span data-stu-id="b8c96-1329">Shape of the halftone dots.</span></span>



<span data-ttu-id="b8c96-1330">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-1330">Tag</span></span>

<span data-ttu-id="b8c96-1331">0x500D</span><span class="sxs-lookup"><span data-stu-id="b8c96-1331">0x500D</span></span>

<span data-ttu-id="b8c96-1332">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-1332">Type</span></span>

<span data-ttu-id="b8c96-1333">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="b8c96-1333">PropertyTagTypeShort</span></span>

<span data-ttu-id="b8c96-1334">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-1334">Count</span></span>

<span data-ttu-id="b8c96-1335">1</span><span class="sxs-lookup"><span data-stu-id="b8c96-1335">1</span></span>

<span data-ttu-id="b8c96-1336">0-Round 1-ellisse 2-line 3-Square 4-Cross 6-Diamond</span><span class="sxs-lookup"><span data-stu-id="b8c96-1336">0 - round 1 - ellipse 2 - line 3 - square 4 - cross 6 - diamond</span></span>



 

## <a name="propertytaghalftonemisc"></a><span data-ttu-id="b8c96-1337">PropertyTagHalftoneMisc</span><span class="sxs-lookup"><span data-stu-id="b8c96-1337">PropertyTagHalftoneMisc</span></span>

<span data-ttu-id="b8c96-1338">Informazioni varie su mezzitoni.</span><span class="sxs-lookup"><span data-stu-id="b8c96-1338">Miscellaneous halftone information.</span></span>



| <span data-ttu-id="b8c96-1339">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-1339">Property info</span></span> | <span data-ttu-id="b8c96-1340">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-1340">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="b8c96-1341">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-1341">Tag</span></span>   | <span data-ttu-id="b8c96-1342">0x500E</span><span class="sxs-lookup"><span data-stu-id="b8c96-1342">0x500E</span></span>              |
| <span data-ttu-id="b8c96-1343">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-1343">Type</span></span>  | <span data-ttu-id="b8c96-1344">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="b8c96-1344">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="b8c96-1345">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-1345">Count</span></span> | <span data-ttu-id="b8c96-1346">1</span><span class="sxs-lookup"><span data-stu-id="b8c96-1346">1</span></span>                   |



 

## <a name="propertytaghalftonescreen"></a><span data-ttu-id="b8c96-1347">PropertyTagHalftoneScreen</span><span class="sxs-lookup"><span data-stu-id="b8c96-1347">PropertyTagHalftoneScreen</span></span>

<span data-ttu-id="b8c96-1348">Valore booleano che specifica se utilizzare le schermate predefinite della stampante.</span><span class="sxs-lookup"><span data-stu-id="b8c96-1348">Boolean value that specifies whether to use the printer's default screens.</span></span>



<span data-ttu-id="b8c96-1349">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-1349">Tag</span></span>

<span data-ttu-id="b8c96-1350">0x500F</span><span class="sxs-lookup"><span data-stu-id="b8c96-1350">0x500F</span></span>

<span data-ttu-id="b8c96-1351">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-1351">Type</span></span>

<span data-ttu-id="b8c96-1352">PropertyTagTypeByte</span><span class="sxs-lookup"><span data-stu-id="b8c96-1352">PropertyTagTypeByte</span></span>

<span data-ttu-id="b8c96-1353">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-1353">Count</span></span>

<span data-ttu-id="b8c96-1354">1</span><span class="sxs-lookup"><span data-stu-id="b8c96-1354">1</span></span>

<span data-ttu-id="b8c96-1355">1-utilizzare le schermate predefinite della stampante 2-altro</span><span class="sxs-lookup"><span data-stu-id="b8c96-1355">1 - use printer's default screens 2 - other</span></span>



 

## <a name="propertytagjpegquality"></a><span data-ttu-id="b8c96-1356">PropertyTagJPEGQuality</span><span class="sxs-lookup"><span data-stu-id="b8c96-1356">PropertyTagJPEGQuality</span></span>

<span data-ttu-id="b8c96-1357">Tag privato usato dal formato Adobe Photoshop.</span><span class="sxs-lookup"><span data-stu-id="b8c96-1357">Private tag used by the Adobe Photoshop format.</span></span> <span data-ttu-id="b8c96-1358">Non per uso pubblico.</span><span class="sxs-lookup"><span data-stu-id="b8c96-1358">Not for public use.</span></span>



| <span data-ttu-id="b8c96-1359">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-1359">Property info</span></span> | <span data-ttu-id="b8c96-1360">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-1360">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="b8c96-1361">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-1361">Tag</span></span>   | <span data-ttu-id="b8c96-1362">0x5010</span><span class="sxs-lookup"><span data-stu-id="b8c96-1362">0x5010</span></span>               |
| <span data-ttu-id="b8c96-1363">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-1363">Type</span></span>  | <span data-ttu-id="b8c96-1364">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="b8c96-1364">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="b8c96-1365">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-1365">Count</span></span> | <span data-ttu-id="b8c96-1366">Qualsiasi</span><span class="sxs-lookup"><span data-stu-id="b8c96-1366">Any</span></span>                  |



 

## <a name="propertytaggridsize"></a><span data-ttu-id="b8c96-1367">PropertyTagGridSize</span><span class="sxs-lookup"><span data-stu-id="b8c96-1367">PropertyTagGridSize</span></span>

<span data-ttu-id="b8c96-1368">Blocco di informazioni su griglie e guide.</span><span class="sxs-lookup"><span data-stu-id="b8c96-1368">Block of information about grids and guides.</span></span>



| <span data-ttu-id="b8c96-1369">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-1369">Property info</span></span> | <span data-ttu-id="b8c96-1370">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-1370">Value</span></span> |
|-------|--------------------------|
| <span data-ttu-id="b8c96-1371">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-1371">Tag</span></span>   | <span data-ttu-id="b8c96-1372">0x5011</span><span class="sxs-lookup"><span data-stu-id="b8c96-1372">0x5011</span></span>                   |
| <span data-ttu-id="b8c96-1373">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-1373">Type</span></span>  | <span data-ttu-id="b8c96-1374">PropertyTagTypeUndefined</span><span class="sxs-lookup"><span data-stu-id="b8c96-1374">PropertyTagTypeUndefined</span></span> |
| <span data-ttu-id="b8c96-1375">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-1375">Count</span></span> | <span data-ttu-id="b8c96-1376">Qualsiasi</span><span class="sxs-lookup"><span data-stu-id="b8c96-1376">Any</span></span>                      |



 

## <a name="propertytagthumbnailformat"></a><span data-ttu-id="b8c96-1377">PropertyTagThumbnailFormat</span><span class="sxs-lookup"><span data-stu-id="b8c96-1377">PropertyTagThumbnailFormat</span></span>

<span data-ttu-id="b8c96-1378">Formato dell'immagine di anteprima.</span><span class="sxs-lookup"><span data-stu-id="b8c96-1378">Format of the thumbnail image.</span></span>



<span data-ttu-id="b8c96-1379">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-1379">Tag</span></span>

<span data-ttu-id="b8c96-1380">0x5012</span><span class="sxs-lookup"><span data-stu-id="b8c96-1380">0x5012</span></span>

<span data-ttu-id="b8c96-1381">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-1381">Type</span></span>

<span data-ttu-id="b8c96-1382">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="b8c96-1382">PropertyTagTypeLong</span></span>

<span data-ttu-id="b8c96-1383">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-1383">Count</span></span>

<span data-ttu-id="b8c96-1384">1</span><span class="sxs-lookup"><span data-stu-id="b8c96-1384">1</span></span>

<span data-ttu-id="b8c96-1385">0-RGB RAW 1-JPEG</span><span class="sxs-lookup"><span data-stu-id="b8c96-1385">0 - raw RGB 1 - JPEG</span></span>



 

## <a name="propertytagthumbnailwidth"></a><span data-ttu-id="b8c96-1386">PropertyTagThumbnailWidth</span><span class="sxs-lookup"><span data-stu-id="b8c96-1386">PropertyTagThumbnailWidth</span></span>

<span data-ttu-id="b8c96-1387">Larghezza, in pixel, dell'immagine di anteprima.</span><span class="sxs-lookup"><span data-stu-id="b8c96-1387">Width, in pixels, of the thumbnail image.</span></span>



| <span data-ttu-id="b8c96-1388">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-1388">Property info</span></span> | <span data-ttu-id="b8c96-1389">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-1389">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="b8c96-1390">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-1390">Tag</span></span>   | <span data-ttu-id="b8c96-1391">0x5013</span><span class="sxs-lookup"><span data-stu-id="b8c96-1391">0x5013</span></span>              |
| <span data-ttu-id="b8c96-1392">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-1392">Type</span></span>  | <span data-ttu-id="b8c96-1393">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="b8c96-1393">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="b8c96-1394">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-1394">Count</span></span> | <span data-ttu-id="b8c96-1395">1</span><span class="sxs-lookup"><span data-stu-id="b8c96-1395">1</span></span>                   |



 

## <a name="propertytagthumbnailheight"></a><span data-ttu-id="b8c96-1396">PropertyTagThumbnailHeight</span><span class="sxs-lookup"><span data-stu-id="b8c96-1396">PropertyTagThumbnailHeight</span></span>

<span data-ttu-id="b8c96-1397">Altezza, in pixel, dell'immagine di anteprima.</span><span class="sxs-lookup"><span data-stu-id="b8c96-1397">Height, in pixels, of the thumbnail image.</span></span>



| <span data-ttu-id="b8c96-1398">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-1398">Property info</span></span> | <span data-ttu-id="b8c96-1399">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-1399">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="b8c96-1400">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-1400">Tag</span></span>   | <span data-ttu-id="b8c96-1401">0x5014</span><span class="sxs-lookup"><span data-stu-id="b8c96-1401">0x5014</span></span>              |
| <span data-ttu-id="b8c96-1402">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-1402">Type</span></span>  | <span data-ttu-id="b8c96-1403">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="b8c96-1403">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="b8c96-1404">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-1404">Count</span></span> | <span data-ttu-id="b8c96-1405">1</span><span class="sxs-lookup"><span data-stu-id="b8c96-1405">1</span></span>                   |



 

## <a name="propertytagthumbnailcolordepth"></a><span data-ttu-id="b8c96-1406">PropertyTagThumbnailColorDepth</span><span class="sxs-lookup"><span data-stu-id="b8c96-1406">PropertyTagThumbnailColorDepth</span></span>

<span data-ttu-id="b8c96-1407">bit per pixel (BPP) per l'immagine di anteprima.</span><span class="sxs-lookup"><span data-stu-id="b8c96-1407">bits per pixel (BPP) for the thumbnail image.</span></span>



| <span data-ttu-id="b8c96-1408">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-1408">Property info</span></span> | <span data-ttu-id="b8c96-1409">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-1409">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="b8c96-1410">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-1410">Tag</span></span>   | <span data-ttu-id="b8c96-1411">0x5015</span><span class="sxs-lookup"><span data-stu-id="b8c96-1411">0x5015</span></span>               |
| <span data-ttu-id="b8c96-1412">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-1412">Type</span></span>  | <span data-ttu-id="b8c96-1413">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="b8c96-1413">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="b8c96-1414">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-1414">Count</span></span> | <span data-ttu-id="b8c96-1415">1</span><span class="sxs-lookup"><span data-stu-id="b8c96-1415">1</span></span>                    |



 

## <a name="propertytagthumbnailplanes"></a><span data-ttu-id="b8c96-1416">PropertyTagThumbnailPlanes</span><span class="sxs-lookup"><span data-stu-id="b8c96-1416">PropertyTagThumbnailPlanes</span></span>

<span data-ttu-id="b8c96-1417">Numero di piani di colore per l'immagine di anteprima.</span><span class="sxs-lookup"><span data-stu-id="b8c96-1417">Number of color planes for the thumbnail image.</span></span>



| <span data-ttu-id="b8c96-1418">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-1418">Property info</span></span> | <span data-ttu-id="b8c96-1419">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-1419">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="b8c96-1420">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-1420">Tag</span></span>   | <span data-ttu-id="b8c96-1421">0x5016</span><span class="sxs-lookup"><span data-stu-id="b8c96-1421">0x5016</span></span>               |
| <span data-ttu-id="b8c96-1422">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-1422">Type</span></span>  | <span data-ttu-id="b8c96-1423">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="b8c96-1423">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="b8c96-1424">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-1424">Count</span></span> | <span data-ttu-id="b8c96-1425">1</span><span class="sxs-lookup"><span data-stu-id="b8c96-1425">1</span></span>                    |



 

## <a name="propertytagthumbnailrawbytes"></a><span data-ttu-id="b8c96-1426">PropertyTagThumbnailRawBytes</span><span class="sxs-lookup"><span data-stu-id="b8c96-1426">PropertyTagThumbnailRawBytes</span></span>

<span data-ttu-id="b8c96-1427">Offset dei byte tra le righe di dati pixel.</span><span class="sxs-lookup"><span data-stu-id="b8c96-1427">Byte offset between rows of pixel data.</span></span>



| <span data-ttu-id="b8c96-1428">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-1428">Property info</span></span> | <span data-ttu-id="b8c96-1429">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-1429">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="b8c96-1430">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-1430">Tag</span></span>   | <span data-ttu-id="b8c96-1431">0x5017</span><span class="sxs-lookup"><span data-stu-id="b8c96-1431">0x5017</span></span>              |
| <span data-ttu-id="b8c96-1432">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-1432">Type</span></span>  | <span data-ttu-id="b8c96-1433">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="b8c96-1433">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="b8c96-1434">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-1434">Count</span></span> | <span data-ttu-id="b8c96-1435">1</span><span class="sxs-lookup"><span data-stu-id="b8c96-1435">1</span></span>                   |



 

## <a name="propertytagthumbnailsize"></a><span data-ttu-id="b8c96-1436">PropertyTagThumbnailSize</span><span class="sxs-lookup"><span data-stu-id="b8c96-1436">PropertyTagThumbnailSize</span></span>

<span data-ttu-id="b8c96-1437">Dimensioni totali, in byte, dell'immagine di anteprima.</span><span class="sxs-lookup"><span data-stu-id="b8c96-1437">Total size, in bytes, of the thumbnail image.</span></span>



| <span data-ttu-id="b8c96-1438">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-1438">Property info</span></span> | <span data-ttu-id="b8c96-1439">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-1439">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="b8c96-1440">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-1440">Tag</span></span>   | <span data-ttu-id="b8c96-1441">0x5018</span><span class="sxs-lookup"><span data-stu-id="b8c96-1441">0x5018</span></span>              |
| <span data-ttu-id="b8c96-1442">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-1442">Type</span></span>  | <span data-ttu-id="b8c96-1443">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="b8c96-1443">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="b8c96-1444">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-1444">Count</span></span> | <span data-ttu-id="b8c96-1445">1</span><span class="sxs-lookup"><span data-stu-id="b8c96-1445">1</span></span>                   |



 

## <a name="propertytagthumbnailcompressedsize"></a><span data-ttu-id="b8c96-1446">PropertyTagThumbnailCompressedSize</span><span class="sxs-lookup"><span data-stu-id="b8c96-1446">PropertyTagThumbnailCompressedSize</span></span>

<span data-ttu-id="b8c96-1447">Dimensioni compresse, in byte, dell'immagine di anteprima.</span><span class="sxs-lookup"><span data-stu-id="b8c96-1447">Compressed size, in bytes, of the thumbnail image.</span></span>



| <span data-ttu-id="b8c96-1448">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-1448">Property info</span></span> | <span data-ttu-id="b8c96-1449">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-1449">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="b8c96-1450">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-1450">Tag</span></span>   | <span data-ttu-id="b8c96-1451">0x5019</span><span class="sxs-lookup"><span data-stu-id="b8c96-1451">0x5019</span></span>              |
| <span data-ttu-id="b8c96-1452">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-1452">Type</span></span>  | <span data-ttu-id="b8c96-1453">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="b8c96-1453">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="b8c96-1454">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-1454">Count</span></span> | <span data-ttu-id="b8c96-1455">1</span><span class="sxs-lookup"><span data-stu-id="b8c96-1455">1</span></span>                   |



 

## <a name="propertytagcolortransferfunction"></a><span data-ttu-id="b8c96-1456">PropertyTagColorTransferFunction</span><span class="sxs-lookup"><span data-stu-id="b8c96-1456">PropertyTagColorTransferFunction</span></span>

<span data-ttu-id="b8c96-1457">Tabella di valori che specificano le funzioni di trasferimento dei colori.</span><span class="sxs-lookup"><span data-stu-id="b8c96-1457">Table of values that specify color transfer functions.</span></span>



| <span data-ttu-id="b8c96-1458">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-1458">Property info</span></span> | <span data-ttu-id="b8c96-1459">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-1459">Value</span></span> |
|-------|--------------------------|
| <span data-ttu-id="b8c96-1460">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-1460">Tag</span></span>   | <span data-ttu-id="b8c96-1461">0x501A</span><span class="sxs-lookup"><span data-stu-id="b8c96-1461">0x501A</span></span>                   |
| <span data-ttu-id="b8c96-1462">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-1462">Type</span></span>  | <span data-ttu-id="b8c96-1463">PropertyTagTypeUndefined</span><span class="sxs-lookup"><span data-stu-id="b8c96-1463">PropertyTagTypeUndefined</span></span> |
| <span data-ttu-id="b8c96-1464">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-1464">Count</span></span> | <span data-ttu-id="b8c96-1465">Qualsiasi</span><span class="sxs-lookup"><span data-stu-id="b8c96-1465">Any</span></span>                      |



 

## <a name="propertytagthumbnaildata"></a><span data-ttu-id="b8c96-1466">PropertyTagThumbnailData</span><span class="sxs-lookup"><span data-stu-id="b8c96-1466">PropertyTagThumbnailData</span></span>

<span data-ttu-id="b8c96-1467">Bit di anteprima non elaborati in formato JPEG o RGB.</span><span class="sxs-lookup"><span data-stu-id="b8c96-1467">Raw thumbnail bits in JPEG or RGB format.</span></span> <span data-ttu-id="b8c96-1468">Dipende da PropertyTagThumbnailFormat.</span><span class="sxs-lookup"><span data-stu-id="b8c96-1468">Depends on PropertyTagThumbnailFormat.</span></span>



| <span data-ttu-id="b8c96-1469">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-1469">Property info</span></span> | <span data-ttu-id="b8c96-1470">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-1470">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="b8c96-1471">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-1471">Tag</span></span>   | <span data-ttu-id="b8c96-1472">0x501B</span><span class="sxs-lookup"><span data-stu-id="b8c96-1472">0x501B</span></span>              |
| <span data-ttu-id="b8c96-1473">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-1473">Type</span></span>  | <span data-ttu-id="b8c96-1474">PropertyTagTypeByte</span><span class="sxs-lookup"><span data-stu-id="b8c96-1474">PropertyTagTypeByte</span></span> |
| <span data-ttu-id="b8c96-1475">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-1475">Count</span></span> | <span data-ttu-id="b8c96-1476">Variabile</span><span class="sxs-lookup"><span data-stu-id="b8c96-1476">Variable</span></span>            |



 

## <a name="propertytagthumbnailimagewidth"></a><span data-ttu-id="b8c96-1477">PropertyTagThumbnailImageWidth</span><span class="sxs-lookup"><span data-stu-id="b8c96-1477">PropertyTagThumbnailImageWidth</span></span>

<span data-ttu-id="b8c96-1478">Numero di pixel per riga nell'immagine di anteprima.</span><span class="sxs-lookup"><span data-stu-id="b8c96-1478">Number of pixels per row in the thumbnail image.</span></span>



| <span data-ttu-id="b8c96-1479">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-1479">Property info</span></span> | <span data-ttu-id="b8c96-1480">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-1480">Value</span></span> |
|-------|---------------------------------------------|
| <span data-ttu-id="b8c96-1481">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-1481">Tag</span></span>   | <span data-ttu-id="b8c96-1482">0x5020</span><span class="sxs-lookup"><span data-stu-id="b8c96-1482">0x5020</span></span>                                      |
| <span data-ttu-id="b8c96-1483">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-1483">Type</span></span>  | <span data-ttu-id="b8c96-1484">PropertyTagTypeShort o PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="b8c96-1484">PropertyTagTypeShort or PropertyTagTypeLong</span></span> |
| <span data-ttu-id="b8c96-1485">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-1485">Count</span></span> | <span data-ttu-id="b8c96-1486">1</span><span class="sxs-lookup"><span data-stu-id="b8c96-1486">1</span></span>                                           |



 

## <a name="propertytagthumbnailimageheight"></a><span data-ttu-id="b8c96-1487">PropertyTagThumbnailImageHeight</span><span class="sxs-lookup"><span data-stu-id="b8c96-1487">PropertyTagThumbnailImageHeight</span></span>

<span data-ttu-id="b8c96-1488">Numero di righe in pixel nell'immagine di anteprima.</span><span class="sxs-lookup"><span data-stu-id="b8c96-1488">Number of pixel rows in the thumbnail image.</span></span>



| <span data-ttu-id="b8c96-1489">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-1489">Property info</span></span> | <span data-ttu-id="b8c96-1490">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-1490">Value</span></span> |
|-------|---------------------------------------------|
| <span data-ttu-id="b8c96-1491">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-1491">Tag</span></span>   | <span data-ttu-id="b8c96-1492">0x5021</span><span class="sxs-lookup"><span data-stu-id="b8c96-1492">0x5021</span></span>                                      |
| <span data-ttu-id="b8c96-1493">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-1493">Type</span></span>  | <span data-ttu-id="b8c96-1494">PropertyTagTypeShort o PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="b8c96-1494">PropertyTagTypeShort or PropertyTagTypeLong</span></span> |
| <span data-ttu-id="b8c96-1495">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-1495">Count</span></span> | <span data-ttu-id="b8c96-1496">1</span><span class="sxs-lookup"><span data-stu-id="b8c96-1496">1</span></span>                                           |



 

## <a name="propertytagthumbnailbitspersample"></a><span data-ttu-id="b8c96-1497">PropertyTagThumbnailBitsPerSample</span><span class="sxs-lookup"><span data-stu-id="b8c96-1497">PropertyTagThumbnailBitsPerSample</span></span>

<span data-ttu-id="b8c96-1498">Numero di bit per componente colore nell'immagine di anteprima.</span><span class="sxs-lookup"><span data-stu-id="b8c96-1498">Number of bits per color component in the thumbnail image.</span></span> <span data-ttu-id="b8c96-1499">Vedere anche [PropertyTagThumbnailSamplesPerPixel](#propertytagthumbnailsamplesperpixel).</span><span class="sxs-lookup"><span data-stu-id="b8c96-1499">See also [PropertyTagThumbnailSamplesPerPixel](#propertytagthumbnailsamplesperpixel).</span></span>



| <span data-ttu-id="b8c96-1500">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-1500">Property info</span></span> | <span data-ttu-id="b8c96-1501">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-1501">Value</span></span> |
|-------|-----------------------------------------------------------------|
| <span data-ttu-id="b8c96-1502">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-1502">Tag</span></span>   | <span data-ttu-id="b8c96-1503">0x5022</span><span class="sxs-lookup"><span data-stu-id="b8c96-1503">0x5022</span></span>                                                          |
| <span data-ttu-id="b8c96-1504">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-1504">Type</span></span>  | <span data-ttu-id="b8c96-1505">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="b8c96-1505">PropertyTagTypeShort</span></span>                                            |
| <span data-ttu-id="b8c96-1506">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-1506">Count</span></span> | <span data-ttu-id="b8c96-1507">Numero di campioni (componenti) per pixel nell'immagine di anteprima</span><span class="sxs-lookup"><span data-stu-id="b8c96-1507">Number of samples (components) per pixel in the thumbnail image</span></span> |



 

## <a name="propertytagthumbnailcompression"></a><span data-ttu-id="b8c96-1508">PropertyTagThumbnailCompression</span><span class="sxs-lookup"><span data-stu-id="b8c96-1508">PropertyTagThumbnailCompression</span></span>

<span data-ttu-id="b8c96-1509">Schema di compressione usato per i dati dell'immagine di anteprima.</span><span class="sxs-lookup"><span data-stu-id="b8c96-1509">Compression scheme used for thumbnail image data.</span></span>



| <span data-ttu-id="b8c96-1510">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-1510">Property info</span></span> | <span data-ttu-id="b8c96-1511">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-1511">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="b8c96-1512">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-1512">Tag</span></span>   | <span data-ttu-id="b8c96-1513">0x5023</span><span class="sxs-lookup"><span data-stu-id="b8c96-1513">0x5023</span></span>               |
| <span data-ttu-id="b8c96-1514">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-1514">Type</span></span>  | <span data-ttu-id="b8c96-1515">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="b8c96-1515">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="b8c96-1516">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-1516">Count</span></span> | <span data-ttu-id="b8c96-1517">1</span><span class="sxs-lookup"><span data-stu-id="b8c96-1517">1</span></span>                    |



 

## <a name="propertytagthumbnailphotometricinterp"></a><span data-ttu-id="b8c96-1518">PropertyTagThumbnailPhotometricInterp</span><span class="sxs-lookup"><span data-stu-id="b8c96-1518">PropertyTagThumbnailPhotometricInterp</span></span>

<span data-ttu-id="b8c96-1519">Come verranno interpretati i dati di Anteprima pixel.</span><span class="sxs-lookup"><span data-stu-id="b8c96-1519">How thumbnail pixel data will be interpreted.</span></span>



| <span data-ttu-id="b8c96-1520">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-1520">Property info</span></span> | <span data-ttu-id="b8c96-1521">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-1521">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="b8c96-1522">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-1522">Tag</span></span>   | <span data-ttu-id="b8c96-1523">0x5024</span><span class="sxs-lookup"><span data-stu-id="b8c96-1523">0x5024</span></span>               |
| <span data-ttu-id="b8c96-1524">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-1524">Type</span></span>  | <span data-ttu-id="b8c96-1525">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="b8c96-1525">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="b8c96-1526">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-1526">Count</span></span> | <span data-ttu-id="b8c96-1527">1</span><span class="sxs-lookup"><span data-stu-id="b8c96-1527">1</span></span>                    |



 

## <a name="propertytagthumbnailimagedescription"></a><span data-ttu-id="b8c96-1528">PropertyTagThumbnailImageDescription</span><span class="sxs-lookup"><span data-stu-id="b8c96-1528">PropertyTagThumbnailImageDescription</span></span>

<span data-ttu-id="b8c96-1529">Stringa di caratteri con terminazione null che specifica il titolo dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="b8c96-1529">Null-terminated character string that specifies the title of the image.</span></span>



| <span data-ttu-id="b8c96-1530">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-1530">Property info</span></span> | <span data-ttu-id="b8c96-1531">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-1531">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="b8c96-1532">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-1532">Tag</span></span>   | <span data-ttu-id="b8c96-1533">0x5025</span><span class="sxs-lookup"><span data-stu-id="b8c96-1533">0x5025</span></span>                                             |
| <span data-ttu-id="b8c96-1534">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-1534">Type</span></span>  | <span data-ttu-id="b8c96-1535">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="b8c96-1535">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="b8c96-1536">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-1536">Count</span></span> | <span data-ttu-id="b8c96-1537">Lunghezza della stringa che include il carattere di terminazione NULL</span><span class="sxs-lookup"><span data-stu-id="b8c96-1537">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagthumbnailequipmake"></a><span data-ttu-id="b8c96-1538">PropertyTagThumbnailEquipMake</span><span class="sxs-lookup"><span data-stu-id="b8c96-1538">PropertyTagThumbnailEquipMake</span></span>

<span data-ttu-id="b8c96-1539">Stringa di caratteri con terminazione null che specifica il produttore delle apparecchiature usate per registrare l'immagine di anteprima.</span><span class="sxs-lookup"><span data-stu-id="b8c96-1539">Null-terminated character string that specifies the manufacturer of the equipment used to record the thumbnail image.</span></span>



| <span data-ttu-id="b8c96-1540">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-1540">Property info</span></span> | <span data-ttu-id="b8c96-1541">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-1541">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="b8c96-1542">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-1542">Tag</span></span>   | <span data-ttu-id="b8c96-1543">0x5026</span><span class="sxs-lookup"><span data-stu-id="b8c96-1543">0x5026</span></span>                                             |
| <span data-ttu-id="b8c96-1544">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-1544">Type</span></span>  | <span data-ttu-id="b8c96-1545">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="b8c96-1545">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="b8c96-1546">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-1546">Count</span></span> | <span data-ttu-id="b8c96-1547">Lunghezza della stringa che include il carattere di terminazione NULL</span><span class="sxs-lookup"><span data-stu-id="b8c96-1547">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagthumbnailequipmodel"></a><span data-ttu-id="b8c96-1548">PropertyTagThumbnailEquipModel</span><span class="sxs-lookup"><span data-stu-id="b8c96-1548">PropertyTagThumbnailEquipModel</span></span>

<span data-ttu-id="b8c96-1549">Stringa di caratteri con terminazione null che specifica il nome del modello o il numero di modello dell'apparecchiatura utilizzata per registrare l'immagine di anteprima.</span><span class="sxs-lookup"><span data-stu-id="b8c96-1549">Null-terminated character string that specifies the model name or model number of the equipment used to record the thumbnail image.</span></span>



| <span data-ttu-id="b8c96-1550">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-1550">Property info</span></span> | <span data-ttu-id="b8c96-1551">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-1551">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="b8c96-1552">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-1552">Tag</span></span>   | <span data-ttu-id="b8c96-1553">0x5027</span><span class="sxs-lookup"><span data-stu-id="b8c96-1553">0x5027</span></span>                                             |
| <span data-ttu-id="b8c96-1554">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-1554">Type</span></span>  | <span data-ttu-id="b8c96-1555">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="b8c96-1555">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="b8c96-1556">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-1556">Count</span></span> | <span data-ttu-id="b8c96-1557">Lunghezza della stringa che include il carattere di terminazione NULL</span><span class="sxs-lookup"><span data-stu-id="b8c96-1557">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagthumbnailstripoffsets"></a><span data-ttu-id="b8c96-1558">PropertyTagThumbnailStripOffsets</span><span class="sxs-lookup"><span data-stu-id="b8c96-1558">PropertyTagThumbnailStripOffsets</span></span>

<span data-ttu-id="b8c96-1559">Per ogni striscia nell'immagine di anteprima, l'offset dei byte di tale striscia.</span><span class="sxs-lookup"><span data-stu-id="b8c96-1559">For each strip in the thumbnail image, the byte offset of that strip.</span></span> <span data-ttu-id="b8c96-1560">Vedere anche [PropertyTagThumbnailRowsPerStrip](#propertytagthumbnailrowsperstrip) e [PropertyTagThumbnailStripBytesCount](#propertytagthumbnailstripbytescount).</span><span class="sxs-lookup"><span data-stu-id="b8c96-1560">See also [PropertyTagThumbnailRowsPerStrip](#propertytagthumbnailrowsperstrip) and [PropertyTagThumbnailStripBytesCount](#propertytagthumbnailstripbytescount).</span></span>



| <span data-ttu-id="b8c96-1561">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-1561">Property info</span></span> | <span data-ttu-id="b8c96-1562">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-1562">Value</span></span> |
|-------|---------------------------------------------|
| <span data-ttu-id="b8c96-1563">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-1563">Tag</span></span>   | <span data-ttu-id="b8c96-1564">0x5028</span><span class="sxs-lookup"><span data-stu-id="b8c96-1564">0x5028</span></span>                                      |
| <span data-ttu-id="b8c96-1565">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-1565">Type</span></span>  | <span data-ttu-id="b8c96-1566">PropertyTagTypeShort o PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="b8c96-1566">PropertyTagTypeShort or PropertyTagTypeLong</span></span> |
| <span data-ttu-id="b8c96-1567">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-1567">Count</span></span> | <span data-ttu-id="b8c96-1568">Numero di strisce</span><span class="sxs-lookup"><span data-stu-id="b8c96-1568">Number of strips</span></span>                            |



 

## <a name="propertytagthumbnailorientation"></a><span data-ttu-id="b8c96-1569">PropertyTagThumbnailOrientation</span><span class="sxs-lookup"><span data-stu-id="b8c96-1569">PropertyTagThumbnailOrientation</span></span>

<span data-ttu-id="b8c96-1570">Orientamento dell'immagine di anteprima in termini di righe e colonne.</span><span class="sxs-lookup"><span data-stu-id="b8c96-1570">Thumbnail image orientation in terms of rows and columns.</span></span> <span data-ttu-id="b8c96-1571">Vedere anche [PropertyTagOrientation](#propertytagorientation).</span><span class="sxs-lookup"><span data-stu-id="b8c96-1571">See also [PropertyTagOrientation](#propertytagorientation).</span></span>



| <span data-ttu-id="b8c96-1572">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-1572">Property info</span></span> | <span data-ttu-id="b8c96-1573">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-1573">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="b8c96-1574">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-1574">Tag</span></span>   | <span data-ttu-id="b8c96-1575">0x5029</span><span class="sxs-lookup"><span data-stu-id="b8c96-1575">0x5029</span></span>               |
| <span data-ttu-id="b8c96-1576">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-1576">Type</span></span>  | <span data-ttu-id="b8c96-1577">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="b8c96-1577">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="b8c96-1578">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-1578">Count</span></span> | <span data-ttu-id="b8c96-1579">1</span><span class="sxs-lookup"><span data-stu-id="b8c96-1579">1</span></span>                    |



 

## <a name="propertytagthumbnailsamplesperpixel"></a><span data-ttu-id="b8c96-1580">PropertyTagThumbnailSamplesPerPixel</span><span class="sxs-lookup"><span data-stu-id="b8c96-1580">PropertyTagThumbnailSamplesPerPixel</span></span>

<span data-ttu-id="b8c96-1581">Numero di componenti colore per pixel nell'immagine di anteprima.</span><span class="sxs-lookup"><span data-stu-id="b8c96-1581">Number of color components per pixel in the thumbnail image.</span></span>



| <span data-ttu-id="b8c96-1582">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-1582">Property info</span></span> | <span data-ttu-id="b8c96-1583">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-1583">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="b8c96-1584">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-1584">Tag</span></span>   | <span data-ttu-id="b8c96-1585">0x502A</span><span class="sxs-lookup"><span data-stu-id="b8c96-1585">0x502A</span></span>               |
| <span data-ttu-id="b8c96-1586">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-1586">Type</span></span>  | <span data-ttu-id="b8c96-1587">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="b8c96-1587">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="b8c96-1588">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-1588">Count</span></span> | <span data-ttu-id="b8c96-1589">1</span><span class="sxs-lookup"><span data-stu-id="b8c96-1589">1</span></span>                    |



 

## <a name="propertytagthumbnailrowsperstrip"></a><span data-ttu-id="b8c96-1590">PropertyTagThumbnailRowsPerStrip</span><span class="sxs-lookup"><span data-stu-id="b8c96-1590">PropertyTagThumbnailRowsPerStrip</span></span>

<span data-ttu-id="b8c96-1591">Numero di righe per strip nell'immagine di anteprima.</span><span class="sxs-lookup"><span data-stu-id="b8c96-1591">Number of rows per strip in the thumbnail image.</span></span> <span data-ttu-id="b8c96-1592">Vedere anche [PropertyTagThumbnailStripBytesCount](#propertytagthumbnailstripbytescount) e [PropertyTagThumbnailStripOffsets](#propertytagthumbnailstripoffsets).</span><span class="sxs-lookup"><span data-stu-id="b8c96-1592">See also [PropertyTagThumbnailStripBytesCount](#propertytagthumbnailstripbytescount) and [PropertyTagThumbnailStripOffsets](#propertytagthumbnailstripoffsets).</span></span>



| <span data-ttu-id="b8c96-1593">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-1593">Property info</span></span> | <span data-ttu-id="b8c96-1594">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-1594">Value</span></span> |
|-------|---------------------------------------------|
| <span data-ttu-id="b8c96-1595">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-1595">Tag</span></span>   | <span data-ttu-id="b8c96-1596">0x502B</span><span class="sxs-lookup"><span data-stu-id="b8c96-1596">0x502B</span></span>                                      |
| <span data-ttu-id="b8c96-1597">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-1597">Type</span></span>  | <span data-ttu-id="b8c96-1598">PropertyTagTypeShort o PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="b8c96-1598">PropertyTagTypeShort or PropertyTagTypeLong</span></span> |
| <span data-ttu-id="b8c96-1599">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-1599">Count</span></span> | <span data-ttu-id="b8c96-1600">1</span><span class="sxs-lookup"><span data-stu-id="b8c96-1600">1</span></span>                                           |



 

## <a name="propertytagthumbnailstripbytescount"></a><span data-ttu-id="b8c96-1601">PropertyTagThumbnailStripBytesCount</span><span class="sxs-lookup"><span data-stu-id="b8c96-1601">PropertyTagThumbnailStripBytesCount</span></span>

<span data-ttu-id="b8c96-1602">Per ogni striscia di immagine di anteprima, il numero totale di byte in tale striping.</span><span class="sxs-lookup"><span data-stu-id="b8c96-1602">For each thumbnail image strip, the total number of bytes in that strip.</span></span>



| <span data-ttu-id="b8c96-1603">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-1603">Property info</span></span> | <span data-ttu-id="b8c96-1604">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-1604">Value</span></span> |
|-------|---------------------------------------------|
| <span data-ttu-id="b8c96-1605">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-1605">Tag</span></span>   | <span data-ttu-id="b8c96-1606">0x502C</span><span class="sxs-lookup"><span data-stu-id="b8c96-1606">0x502C</span></span>                                      |
| <span data-ttu-id="b8c96-1607">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-1607">Type</span></span>  | <span data-ttu-id="b8c96-1608">PropertyTagTypeShort o PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="b8c96-1608">PropertyTagTypeShort or PropertyTagTypeLong</span></span> |
| <span data-ttu-id="b8c96-1609">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-1609">Count</span></span> | <span data-ttu-id="b8c96-1610">Numero di strisce nell'immagine di anteprima</span><span class="sxs-lookup"><span data-stu-id="b8c96-1610">Number of strips in the thumbnail image</span></span>     |



 

## <a name="propertytagthumbnailresolutionx"></a><span data-ttu-id="b8c96-1611">PropertyTagThumbnailResolutionX</span><span class="sxs-lookup"><span data-stu-id="b8c96-1611">PropertyTagThumbnailResolutionX</span></span>

<span data-ttu-id="b8c96-1612">Risoluzione delle anteprime nella direzione della larghezza.</span><span class="sxs-lookup"><span data-stu-id="b8c96-1612">Thumbnail resolution in the width direction.</span></span> <span data-ttu-id="b8c96-1613">L'unità di risoluzione viene specificata in [PropertyTagThumbnailResolutionUnit](#propertytagthumbnailresolutionunit).</span><span class="sxs-lookup"><span data-stu-id="b8c96-1613">The resolution unit is given in [PropertyTagThumbnailResolutionUnit](#propertytagthumbnailresolutionunit).</span></span>



| <span data-ttu-id="b8c96-1614">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-1614">Property info</span></span> | <span data-ttu-id="b8c96-1615">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-1615">Value</span></span> |
|-----|--------|
| <span data-ttu-id="b8c96-1616">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-1616">Tag</span></span> | <span data-ttu-id="b8c96-1617">0x502D</span><span class="sxs-lookup"><span data-stu-id="b8c96-1617">0x502D</span></span> |



 

## <a name="propertytagthumbnailresolutiony"></a><span data-ttu-id="b8c96-1618">PropertyTagThumbnailResolutionY</span><span class="sxs-lookup"><span data-stu-id="b8c96-1618">PropertyTagThumbnailResolutionY</span></span>

<span data-ttu-id="b8c96-1619">Risoluzione dell'anteprima nella direzione dell'altezza.</span><span class="sxs-lookup"><span data-stu-id="b8c96-1619">Thumbnail resolution in the height direction.</span></span> <span data-ttu-id="b8c96-1620">L'unità di risoluzione viene specificata in [PropertyTagThumbnailResolutionUnit](#propertytagthumbnailresolutionunit).</span><span class="sxs-lookup"><span data-stu-id="b8c96-1620">The resolution unit is given in [PropertyTagThumbnailResolutionUnit](#propertytagthumbnailresolutionunit).</span></span>



| <span data-ttu-id="b8c96-1621">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-1621">Property info</span></span> | <span data-ttu-id="b8c96-1622">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-1622">Value</span></span> |
|-----|--------|
| <span data-ttu-id="b8c96-1623">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-1623">Tag</span></span> | <span data-ttu-id="b8c96-1624">0x502E</span><span class="sxs-lookup"><span data-stu-id="b8c96-1624">0x502E</span></span> |



 

## <a name="propertytagthumbnailplanarconfig"></a><span data-ttu-id="b8c96-1625">PropertyTagThumbnailPlanarConfig</span><span class="sxs-lookup"><span data-stu-id="b8c96-1625">PropertyTagThumbnailPlanarConfig</span></span>

<span data-ttu-id="b8c96-1626">Indica se i componenti dei pixel nell'immagine di anteprima vengono registrati in formato Chunk o Planar.</span><span class="sxs-lookup"><span data-stu-id="b8c96-1626">Whether pixel components in the thumbnail image are recorded in chunky or planar format.</span></span> <span data-ttu-id="b8c96-1627">Vedere anche [PropertyTagPlanarConfig](#propertytagplanarconfig).</span><span class="sxs-lookup"><span data-stu-id="b8c96-1627">See also [PropertyTagPlanarConfig](#propertytagplanarconfig).</span></span>



| <span data-ttu-id="b8c96-1628">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-1628">Property info</span></span> | <span data-ttu-id="b8c96-1629">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-1629">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="b8c96-1630">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-1630">Tag</span></span>   | <span data-ttu-id="b8c96-1631">0x502F</span><span class="sxs-lookup"><span data-stu-id="b8c96-1631">0x502F</span></span>               |
| <span data-ttu-id="b8c96-1632">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-1632">Type</span></span>  | <span data-ttu-id="b8c96-1633">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="b8c96-1633">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="b8c96-1634">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-1634">Count</span></span> | <span data-ttu-id="b8c96-1635">1</span><span class="sxs-lookup"><span data-stu-id="b8c96-1635">1</span></span>                    |



 

## <a name="propertytagthumbnailresolutionunit"></a><span data-ttu-id="b8c96-1636">PropertyTagThumbnailResolutionUnit</span><span class="sxs-lookup"><span data-stu-id="b8c96-1636">PropertyTagThumbnailResolutionUnit</span></span>

<span data-ttu-id="b8c96-1637">Unità di misura per la risoluzione orizzontale e la risoluzione verticale dell'immagine di anteprima.</span><span class="sxs-lookup"><span data-stu-id="b8c96-1637">Unit of measure for the horizontal resolution and the vertical resolution of the thumbnail image.</span></span> <span data-ttu-id="b8c96-1638">Vedere anche [PropertyTagResolutionUnit](#propertytagresolutionunit).</span><span class="sxs-lookup"><span data-stu-id="b8c96-1638">See also [PropertyTagResolutionUnit](#propertytagresolutionunit).</span></span>



| <span data-ttu-id="b8c96-1639">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-1639">Property info</span></span> | <span data-ttu-id="b8c96-1640">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-1640">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="b8c96-1641">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-1641">Tag</span></span>   | <span data-ttu-id="b8c96-1642">0x5030</span><span class="sxs-lookup"><span data-stu-id="b8c96-1642">0x5030</span></span>               |
| <span data-ttu-id="b8c96-1643">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-1643">Type</span></span>  | <span data-ttu-id="b8c96-1644">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="b8c96-1644">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="b8c96-1645">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-1645">Count</span></span> | <span data-ttu-id="b8c96-1646">1</span><span class="sxs-lookup"><span data-stu-id="b8c96-1646">1</span></span>                    |



 

## <a name="propertytagthumbnailtransferfunction"></a><span data-ttu-id="b8c96-1647">PropertyTagThumbnailTransferFunction</span><span class="sxs-lookup"><span data-stu-id="b8c96-1647">PropertyTagThumbnailTransferFunction</span></span>

<span data-ttu-id="b8c96-1648">Tabelle che specificano le funzioni di trasferimento per l'immagine di anteprima.</span><span class="sxs-lookup"><span data-stu-id="b8c96-1648">Tables that specify transfer functions for the thumbnail image.</span></span> <span data-ttu-id="b8c96-1649">Vedere anche [PropertyTagTransferFunction](#propertytagtransferfunction).</span><span class="sxs-lookup"><span data-stu-id="b8c96-1649">See also [PropertyTagTransferFunction](#propertytagtransferfunction).</span></span>



| <span data-ttu-id="b8c96-1650">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-1650">Property info</span></span> | <span data-ttu-id="b8c96-1651">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-1651">Value</span></span> |
|-------|------------------------------------------------------|
| <span data-ttu-id="b8c96-1652">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-1652">Tag</span></span>   | <span data-ttu-id="b8c96-1653">0x5031</span><span class="sxs-lookup"><span data-stu-id="b8c96-1653">0x5031</span></span>                                               |
| <span data-ttu-id="b8c96-1654">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-1654">Type</span></span>  | <span data-ttu-id="b8c96-1655">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="b8c96-1655">PropertyTagTypeShort</span></span>                                 |
| <span data-ttu-id="b8c96-1656">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-1656">Count</span></span> | <span data-ttu-id="b8c96-1657">Numero totale di parole a 16 bit necessarie per le tabelle</span><span class="sxs-lookup"><span data-stu-id="b8c96-1657">Total number of 16-bit words required for the tables</span></span> |



 

## <a name="propertytagthumbnailsoftwareused"></a><span data-ttu-id="b8c96-1658">PropertyTagThumbnailSoftwareUsed</span><span class="sxs-lookup"><span data-stu-id="b8c96-1658">PropertyTagThumbnailSoftwareUsed</span></span>

<span data-ttu-id="b8c96-1659">Stringa di caratteri con terminazione null che specifica il nome e la versione del software o del firmware del dispositivo usato per generare l'immagine di anteprima.</span><span class="sxs-lookup"><span data-stu-id="b8c96-1659">Null-terminated character string that specifies the name and version of the software or firmware of the device used to generate the thumbnail image.</span></span>



| <span data-ttu-id="b8c96-1660">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-1660">Property info</span></span> | <span data-ttu-id="b8c96-1661">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-1661">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="b8c96-1662">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-1662">Tag</span></span>   | <span data-ttu-id="b8c96-1663">0x5032</span><span class="sxs-lookup"><span data-stu-id="b8c96-1663">0x5032</span></span>                                             |
| <span data-ttu-id="b8c96-1664">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-1664">Type</span></span>  | <span data-ttu-id="b8c96-1665">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="b8c96-1665">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="b8c96-1666">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-1666">Count</span></span> | <span data-ttu-id="b8c96-1667">Lunghezza della stringa che include il carattere di terminazione NULL</span><span class="sxs-lookup"><span data-stu-id="b8c96-1667">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagthumbnaildatetime"></a><span data-ttu-id="b8c96-1668">PropertyTagThumbnailDateTime</span><span class="sxs-lookup"><span data-stu-id="b8c96-1668">PropertyTagThumbnailDateTime</span></span>

<span data-ttu-id="b8c96-1669">Data e ora di creazione dell'immagine di anteprima.</span><span class="sxs-lookup"><span data-stu-id="b8c96-1669">Date and time the thumbnail image was created.</span></span> <span data-ttu-id="b8c96-1670">Vedere anche [PropertyTagDateTime](#propertytagdatetime).</span><span class="sxs-lookup"><span data-stu-id="b8c96-1670">See also [PropertyTagDateTime](#propertytagdatetime).</span></span>



| <span data-ttu-id="b8c96-1671">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-1671">Property info</span></span> | <span data-ttu-id="b8c96-1672">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-1672">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="b8c96-1673">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-1673">Tag</span></span>   | <span data-ttu-id="b8c96-1674">0x5033</span><span class="sxs-lookup"><span data-stu-id="b8c96-1674">0x5033</span></span>               |
| <span data-ttu-id="b8c96-1675">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-1675">Type</span></span>  | <span data-ttu-id="b8c96-1676">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="b8c96-1676">PropertyTagTypeASCII</span></span> |
| <span data-ttu-id="b8c96-1677">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-1677">Count</span></span> | <span data-ttu-id="b8c96-1678">20</span><span class="sxs-lookup"><span data-stu-id="b8c96-1678">20</span></span>                   |



 

## <a name="propertytagthumbnailartist"></a><span data-ttu-id="b8c96-1679">PropertyTagThumbnailArtist</span><span class="sxs-lookup"><span data-stu-id="b8c96-1679">PropertyTagThumbnailArtist</span></span>

<span data-ttu-id="b8c96-1680">Stringa di caratteri con terminazione null che specifica il nome della persona che ha creato l'immagine di anteprima.</span><span class="sxs-lookup"><span data-stu-id="b8c96-1680">Null-terminated character string that specifies the name of the person who created the thumbnail image.</span></span>



| <span data-ttu-id="b8c96-1681">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-1681">Property info</span></span> | <span data-ttu-id="b8c96-1682">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-1682">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="b8c96-1683">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-1683">Tag</span></span>   | <span data-ttu-id="b8c96-1684">0x5034</span><span class="sxs-lookup"><span data-stu-id="b8c96-1684">0x5034</span></span>                                             |
| <span data-ttu-id="b8c96-1685">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-1685">Type</span></span>  | <span data-ttu-id="b8c96-1686">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="b8c96-1686">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="b8c96-1687">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-1687">Count</span></span> | <span data-ttu-id="b8c96-1688">Lunghezza della stringa che include il carattere di terminazione NULL</span><span class="sxs-lookup"><span data-stu-id="b8c96-1688">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagthumbnailwhitepoint"></a><span data-ttu-id="b8c96-1689">PropertyTagThumbnailWhitePoint</span><span class="sxs-lookup"><span data-stu-id="b8c96-1689">PropertyTagThumbnailWhitePoint</span></span>

<span data-ttu-id="b8c96-1690">Cromaticità del punto bianco dell'immagine di anteprima.</span><span class="sxs-lookup"><span data-stu-id="b8c96-1690">Chromaticity of the white point of the thumbnail image.</span></span> <span data-ttu-id="b8c96-1691">Vedere anche [PropertyTagWhitePoint](#propertytagwhitepoint).</span><span class="sxs-lookup"><span data-stu-id="b8c96-1691">See also [PropertyTagWhitePoint](#propertytagwhitepoint).</span></span>



| <span data-ttu-id="b8c96-1692">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-1692">Property info</span></span> | <span data-ttu-id="b8c96-1693">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-1693">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="b8c96-1694">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-1694">Tag</span></span>   | <span data-ttu-id="b8c96-1695">0x5035</span><span class="sxs-lookup"><span data-stu-id="b8c96-1695">0x5035</span></span>                  |
| <span data-ttu-id="b8c96-1696">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-1696">Type</span></span>  | <span data-ttu-id="b8c96-1697">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="b8c96-1697">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="b8c96-1698">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-1698">Count</span></span> | <span data-ttu-id="b8c96-1699">2</span><span class="sxs-lookup"><span data-stu-id="b8c96-1699">2</span></span>                       |



 

## <a name="propertytagthumbnailprimarychromaticities"></a><span data-ttu-id="b8c96-1700">PropertyTagThumbnailPrimaryChromaticities</span><span class="sxs-lookup"><span data-stu-id="b8c96-1700">PropertyTagThumbnailPrimaryChromaticities</span></span>

<span data-ttu-id="b8c96-1701">Per ognuno dei tre colori primari nell'immagine di anteprima, la cromaticità di tale colore.</span><span class="sxs-lookup"><span data-stu-id="b8c96-1701">For each of the three primary colors in the thumbnail image, the chromaticity of that color.</span></span> <span data-ttu-id="b8c96-1702">Vedere anche [PropertyTagPrimaryChromaticities](#propertytagprimarychromaticities).</span><span class="sxs-lookup"><span data-stu-id="b8c96-1702">See also [PropertyTagPrimaryChromaticities](#propertytagprimarychromaticities).</span></span>



| <span data-ttu-id="b8c96-1703">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-1703">Property info</span></span> | <span data-ttu-id="b8c96-1704">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-1704">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="b8c96-1705">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-1705">Tag</span></span>   | <span data-ttu-id="b8c96-1706">0x5036</span><span class="sxs-lookup"><span data-stu-id="b8c96-1706">0x5036</span></span>                  |
| <span data-ttu-id="b8c96-1707">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-1707">Type</span></span>  | <span data-ttu-id="b8c96-1708">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="b8c96-1708">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="b8c96-1709">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-1709">Count</span></span> | <span data-ttu-id="b8c96-1710">6</span><span class="sxs-lookup"><span data-stu-id="b8c96-1710">6</span></span>                       |



 

## <a name="propertytagthumbnailycbcrcoefficients"></a><span data-ttu-id="b8c96-1711">PropertyTagThumbnailYCbCrCoefficients</span><span class="sxs-lookup"><span data-stu-id="b8c96-1711">PropertyTagThumbnailYCbCrCoefficients</span></span>

<span data-ttu-id="b8c96-1712">Coefficienti per la trasformazione da RGB a dati YCbCr per l'immagine di anteprima.</span><span class="sxs-lookup"><span data-stu-id="b8c96-1712">Coefficients for transformation from RGB to YCbCr data for the thumbnail image.</span></span> <span data-ttu-id="b8c96-1713">Vedere anche [PropertyTagYCbCrCoefficients](#propertytagycbcrcoefficients).</span><span class="sxs-lookup"><span data-stu-id="b8c96-1713">See also [PropertyTagYCbCrCoefficients](#propertytagycbcrcoefficients).</span></span>



| <span data-ttu-id="b8c96-1714">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-1714">Property info</span></span> | <span data-ttu-id="b8c96-1715">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-1715">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="b8c96-1716">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-1716">Tag</span></span>   | <span data-ttu-id="b8c96-1717">0x5037</span><span class="sxs-lookup"><span data-stu-id="b8c96-1717">0x5037</span></span>                  |
| <span data-ttu-id="b8c96-1718">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-1718">Type</span></span>  | <span data-ttu-id="b8c96-1719">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="b8c96-1719">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="b8c96-1720">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-1720">Count</span></span> | <span data-ttu-id="b8c96-1721">3</span><span class="sxs-lookup"><span data-stu-id="b8c96-1721">3</span></span>                       |



 

## <a name="propertytagthumbnailycbcrsubsampling"></a><span data-ttu-id="b8c96-1722">PropertyTagThumbnailYCbCrSubsampling</span><span class="sxs-lookup"><span data-stu-id="b8c96-1722">PropertyTagThumbnailYCbCrSubsampling</span></span>

<span data-ttu-id="b8c96-1723">Rapporto di campionamento dei componenti cromatura in relazione al componente di luminanza per l'immagine di anteprima.</span><span class="sxs-lookup"><span data-stu-id="b8c96-1723">Sampling ratio of chrominance components in relation to the luminance component for the thumbnail image.</span></span> <span data-ttu-id="b8c96-1724">Vedere anche [PropertyTagYCbCrSubsampling](#propertytagycbcrsubsampling).</span><span class="sxs-lookup"><span data-stu-id="b8c96-1724">See also [PropertyTagYCbCrSubsampling](#propertytagycbcrsubsampling).</span></span>



| <span data-ttu-id="b8c96-1725">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-1725">Property info</span></span> | <span data-ttu-id="b8c96-1726">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-1726">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="b8c96-1727">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-1727">Tag</span></span>   | <span data-ttu-id="b8c96-1728">0x5038</span><span class="sxs-lookup"><span data-stu-id="b8c96-1728">0x5038</span></span>               |
| <span data-ttu-id="b8c96-1729">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-1729">Type</span></span>  | <span data-ttu-id="b8c96-1730">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="b8c96-1730">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="b8c96-1731">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-1731">Count</span></span> | <span data-ttu-id="b8c96-1732">2</span><span class="sxs-lookup"><span data-stu-id="b8c96-1732">2</span></span>                    |



 

## <a name="propertytagthumbnailycbcrpositioning"></a><span data-ttu-id="b8c96-1733">PropertyTagThumbnailYCbCrPositioning</span><span class="sxs-lookup"><span data-stu-id="b8c96-1733">PropertyTagThumbnailYCbCrPositioning</span></span>

<span data-ttu-id="b8c96-1734">Posizione dei componenti cromatura in relazione al componente di luminanza per l'immagine di anteprima.</span><span class="sxs-lookup"><span data-stu-id="b8c96-1734">Position of chrominance components in relation to the luminance component for the thumbnail image.</span></span> <span data-ttu-id="b8c96-1735">Vedere anche [PropertyTagYCbCrPositioning](#propertytagycbcrpositioning).</span><span class="sxs-lookup"><span data-stu-id="b8c96-1735">See also [PropertyTagYCbCrPositioning](#propertytagycbcrpositioning).</span></span>



| <span data-ttu-id="b8c96-1736">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-1736">Property info</span></span> | <span data-ttu-id="b8c96-1737">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-1737">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="b8c96-1738">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-1738">Tag</span></span>   | <span data-ttu-id="b8c96-1739">0x5039</span><span class="sxs-lookup"><span data-stu-id="b8c96-1739">0x5039</span></span>               |
| <span data-ttu-id="b8c96-1740">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-1740">Type</span></span>  | <span data-ttu-id="b8c96-1741">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="b8c96-1741">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="b8c96-1742">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-1742">Count</span></span> | <span data-ttu-id="b8c96-1743">1</span><span class="sxs-lookup"><span data-stu-id="b8c96-1743">1</span></span>                    |



 

## <a name="propertytagthumbnailrefblackwhite"></a><span data-ttu-id="b8c96-1744">PropertyTagThumbnailRefBlackWhite</span><span class="sxs-lookup"><span data-stu-id="b8c96-1744">PropertyTagThumbnailRefBlackWhite</span></span>

<span data-ttu-id="b8c96-1745">Valore del punto nero di riferimento e valore del punto bianco di riferimento per l'immagine di anteprima.</span><span class="sxs-lookup"><span data-stu-id="b8c96-1745">Reference black point value and reference white point value for the thumbnail image.</span></span> <span data-ttu-id="b8c96-1746">Vedere anche [PropertyTagREFBlackWhite](#propertytagrefblackwhite).</span><span class="sxs-lookup"><span data-stu-id="b8c96-1746">See also [PropertyTagREFBlackWhite](#propertytagrefblackwhite).</span></span>



| <span data-ttu-id="b8c96-1747">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-1747">Property info</span></span> | <span data-ttu-id="b8c96-1748">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-1748">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="b8c96-1749">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-1749">Tag</span></span>   | <span data-ttu-id="b8c96-1750">0x503A</span><span class="sxs-lookup"><span data-stu-id="b8c96-1750">0x503A</span></span>                  |
| <span data-ttu-id="b8c96-1751">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-1751">Type</span></span>  | <span data-ttu-id="b8c96-1752">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="b8c96-1752">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="b8c96-1753">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-1753">Count</span></span> | <span data-ttu-id="b8c96-1754">6</span><span class="sxs-lookup"><span data-stu-id="b8c96-1754">6</span></span>                       |



 

## <a name="propertytagthumbnailcopyright"></a><span data-ttu-id="b8c96-1755">PropertyTagThumbnailCopyRight</span><span class="sxs-lookup"><span data-stu-id="b8c96-1755">PropertyTagThumbnailCopyRight</span></span>

<span data-ttu-id="b8c96-1756">Stringa di caratteri con terminazione null che contiene informazioni sul copyright per l'immagine di anteprima.</span><span class="sxs-lookup"><span data-stu-id="b8c96-1756">Null-terminated character string that contains copyright information for the thumbnail image.</span></span>



| <span data-ttu-id="b8c96-1757">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-1757">Property info</span></span> | <span data-ttu-id="b8c96-1758">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-1758">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="b8c96-1759">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-1759">Tag</span></span>   | <span data-ttu-id="b8c96-1760">0x503B</span><span class="sxs-lookup"><span data-stu-id="b8c96-1760">0x503B</span></span>                                             |
| <span data-ttu-id="b8c96-1761">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-1761">Type</span></span>  | <span data-ttu-id="b8c96-1762">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="b8c96-1762">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="b8c96-1763">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-1763">Count</span></span> | <span data-ttu-id="b8c96-1764">Lunghezza della stringa che include il carattere di terminazione NULL</span><span class="sxs-lookup"><span data-stu-id="b8c96-1764">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagluminancetable"></a><span data-ttu-id="b8c96-1765">PropertyTagLuminanceTable</span><span class="sxs-lookup"><span data-stu-id="b8c96-1765">PropertyTagLuminanceTable</span></span>

<span data-ttu-id="b8c96-1766">Tabella luminanza.</span><span class="sxs-lookup"><span data-stu-id="b8c96-1766">Luminance table.</span></span> <span data-ttu-id="b8c96-1767">La tabella luminanza e la tabella cromatura vengono usate per controllare la qualità JPEG.</span><span class="sxs-lookup"><span data-stu-id="b8c96-1767">The luminance table and the chrominance table are used to control JPEG quality.</span></span> <span data-ttu-id="b8c96-1768">Una tabella luminanza o cromatura valida contiene 64 voci di tipo PropertyTagTypeShort.</span><span class="sxs-lookup"><span data-stu-id="b8c96-1768">A valid luminance or chrominance table has 64 entries of type PropertyTagTypeShort.</span></span> <span data-ttu-id="b8c96-1769">Se un'immagine include una tabella di luminanza o una tabella cromatura, deve disporre di entrambe le tabelle.</span><span class="sxs-lookup"><span data-stu-id="b8c96-1769">If an image has either a luminance table or a chrominance table, then it must have both tables.</span></span>



| <span data-ttu-id="b8c96-1770">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-1770">Property info</span></span> | <span data-ttu-id="b8c96-1771">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-1771">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="b8c96-1772">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-1772">Tag</span></span>   | <span data-ttu-id="b8c96-1773">0x5090</span><span class="sxs-lookup"><span data-stu-id="b8c96-1773">0x5090</span></span>               |
| <span data-ttu-id="b8c96-1774">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-1774">Type</span></span>  | <span data-ttu-id="b8c96-1775">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="b8c96-1775">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="b8c96-1776">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-1776">Count</span></span> | <span data-ttu-id="b8c96-1777">64</span><span class="sxs-lookup"><span data-stu-id="b8c96-1777">64</span></span>                   |



 

## <a name="propertytagchrominancetable"></a><span data-ttu-id="b8c96-1778">PropertyTagChrominanceTable</span><span class="sxs-lookup"><span data-stu-id="b8c96-1778">PropertyTagChrominanceTable</span></span>

<span data-ttu-id="b8c96-1779">Tabella cromatura.</span><span class="sxs-lookup"><span data-stu-id="b8c96-1779">Chrominance table.</span></span> <span data-ttu-id="b8c96-1780">La tabella luminanza e la tabella cromatura vengono usate per controllare la qualità JPEG.</span><span class="sxs-lookup"><span data-stu-id="b8c96-1780">The luminance table and the chrominance table are used to control JPEG quality.</span></span> <span data-ttu-id="b8c96-1781">Una tabella luminanza o cromatura valida contiene 64 voci di tipo PropertyTagTypeShort.</span><span class="sxs-lookup"><span data-stu-id="b8c96-1781">A valid luminance or chrominance table has 64 entries of type PropertyTagTypeShort.</span></span> <span data-ttu-id="b8c96-1782">Se un'immagine include una tabella di luminanza o una tabella cromatura, deve disporre di entrambe le tabelle.</span><span class="sxs-lookup"><span data-stu-id="b8c96-1782">If an image has either a luminance table or a chrominance table, then it must have both tables.</span></span>



| <span data-ttu-id="b8c96-1783">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-1783">Property info</span></span> | <span data-ttu-id="b8c96-1784">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-1784">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="b8c96-1785">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-1785">Tag</span></span>   | <span data-ttu-id="b8c96-1786">0x5091</span><span class="sxs-lookup"><span data-stu-id="b8c96-1786">0x5091</span></span>               |
| <span data-ttu-id="b8c96-1787">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-1787">Type</span></span>  | <span data-ttu-id="b8c96-1788">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="b8c96-1788">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="b8c96-1789">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-1789">Count</span></span> | <span data-ttu-id="b8c96-1790">64</span><span class="sxs-lookup"><span data-stu-id="b8c96-1790">64</span></span>                   |



 

## <a name="propertytagframedelay"></a><span data-ttu-id="b8c96-1791">PropertyTagFrameDelay</span><span class="sxs-lookup"><span data-stu-id="b8c96-1791">PropertyTagFrameDelay</span></span>

<span data-ttu-id="b8c96-1792">Ritardo di tempo, in centesimi di secondo, tra due fotogrammi in un'immagine GIF animata.</span><span class="sxs-lookup"><span data-stu-id="b8c96-1792">Time delay, in hundredths of a second, between two frames in an animated GIF image.</span></span>



| <span data-ttu-id="b8c96-1793">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-1793">Property info</span></span> | <span data-ttu-id="b8c96-1794">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-1794">Value</span></span> |
|-------|-------------------------------|
| <span data-ttu-id="b8c96-1795">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-1795">Tag</span></span>   | <span data-ttu-id="b8c96-1796">0x5100</span><span class="sxs-lookup"><span data-stu-id="b8c96-1796">0x5100</span></span>                        |
| <span data-ttu-id="b8c96-1797">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-1797">Type</span></span>  | <span data-ttu-id="b8c96-1798">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="b8c96-1798">PropertyTagTypeLong</span></span>           |
| <span data-ttu-id="b8c96-1799">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-1799">Count</span></span> | <span data-ttu-id="b8c96-1800">Numero di frame nell'immagine</span><span class="sxs-lookup"><span data-stu-id="b8c96-1800">Number of frames in the image</span></span> |



 

## <a name="propertytagloopcount"></a><span data-ttu-id="b8c96-1801">PropertyTagLoopCount</span><span class="sxs-lookup"><span data-stu-id="b8c96-1801">PropertyTagLoopCount</span></span>

<span data-ttu-id="b8c96-1802">Per un'immagine GIF animata, il numero di volte in cui visualizzare l'animazione.</span><span class="sxs-lookup"><span data-stu-id="b8c96-1802">For an animated GIF image, the number of times to display the animation.</span></span> <span data-ttu-id="b8c96-1803">Il valore 0 indica che l'animazione deve essere visualizzata infinitamente.</span><span class="sxs-lookup"><span data-stu-id="b8c96-1803">A value of 0 specifies that the animation should be displayed infinitely.</span></span>



| <span data-ttu-id="b8c96-1804">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-1804">Property info</span></span> | <span data-ttu-id="b8c96-1805">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-1805">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="b8c96-1806">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-1806">Tag</span></span>   | <span data-ttu-id="b8c96-1807">0x5101</span><span class="sxs-lookup"><span data-stu-id="b8c96-1807">0x5101</span></span>               |
| <span data-ttu-id="b8c96-1808">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-1808">Type</span></span>  | <span data-ttu-id="b8c96-1809">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="b8c96-1809">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="b8c96-1810">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-1810">Count</span></span> | <span data-ttu-id="b8c96-1811">1</span><span class="sxs-lookup"><span data-stu-id="b8c96-1811">1</span></span>                    |



 

## <a name="propertytagglobalpalette"></a><span data-ttu-id="b8c96-1812">PropertyTagGlobalPalette</span><span class="sxs-lookup"><span data-stu-id="b8c96-1812">PropertyTagGlobalPalette</span></span>

<span data-ttu-id="b8c96-1813">Tavolozza dei colori per una bitmap indicizzata in un'immagine GIF.</span><span class="sxs-lookup"><span data-stu-id="b8c96-1813">Color palette for an indexed bitmap in a GIF image.</span></span>



| <span data-ttu-id="b8c96-1814">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-1814">Property info</span></span> | <span data-ttu-id="b8c96-1815">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-1815">Value</span></span> |
|-------|-------------------------------|
| <span data-ttu-id="b8c96-1816">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-1816">Tag</span></span>   | <span data-ttu-id="b8c96-1817">0x5102</span><span class="sxs-lookup"><span data-stu-id="b8c96-1817">0x5102</span></span>                        |
| <span data-ttu-id="b8c96-1818">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-1818">Type</span></span>  | <span data-ttu-id="b8c96-1819">PropertyTagTypeByte</span><span class="sxs-lookup"><span data-stu-id="b8c96-1819">PropertyTagTypeByte</span></span>           |
| <span data-ttu-id="b8c96-1820">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-1820">Count</span></span> | <span data-ttu-id="b8c96-1821">3 x numero di voci della tavolozza</span><span class="sxs-lookup"><span data-stu-id="b8c96-1821">3 x number of palette entries</span></span> |



 

## <a name="propertytagindexbackground"></a><span data-ttu-id="b8c96-1822">PropertyTagIndexBackground</span><span class="sxs-lookup"><span data-stu-id="b8c96-1822">PropertyTagIndexBackground</span></span>

<span data-ttu-id="b8c96-1823">Indice del colore di sfondo nella tavolozza di un'immagine GIF.</span><span class="sxs-lookup"><span data-stu-id="b8c96-1823">Index of the background color in the palette of a GIF image.</span></span>



| <span data-ttu-id="b8c96-1824">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-1824">Property info</span></span> | <span data-ttu-id="b8c96-1825">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-1825">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="b8c96-1826">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-1826">Tag</span></span>   | <span data-ttu-id="b8c96-1827">0x5103</span><span class="sxs-lookup"><span data-stu-id="b8c96-1827">0x5103</span></span>              |
| <span data-ttu-id="b8c96-1828">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-1828">Type</span></span>  | <span data-ttu-id="b8c96-1829">PropertyTagTypeByte</span><span class="sxs-lookup"><span data-stu-id="b8c96-1829">PropertyTagTypeByte</span></span> |
| <span data-ttu-id="b8c96-1830">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-1830">Count</span></span> | <span data-ttu-id="b8c96-1831">1</span><span class="sxs-lookup"><span data-stu-id="b8c96-1831">1</span></span>                   |



 

## <a name="propertytagindextransparent"></a><span data-ttu-id="b8c96-1832">PropertyTagIndexTransparent</span><span class="sxs-lookup"><span data-stu-id="b8c96-1832">PropertyTagIndexTransparent</span></span>

<span data-ttu-id="b8c96-1833">Indice del colore trasparente nella tavolozza di un'immagine GIF.</span><span class="sxs-lookup"><span data-stu-id="b8c96-1833">Index of the transparent color in the palette of a GIF image.</span></span>



| <span data-ttu-id="b8c96-1834">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-1834">Property info</span></span> | <span data-ttu-id="b8c96-1835">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-1835">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="b8c96-1836">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-1836">Tag</span></span>   | <span data-ttu-id="b8c96-1837">0x5104</span><span class="sxs-lookup"><span data-stu-id="b8c96-1837">0x5104</span></span>              |
| <span data-ttu-id="b8c96-1838">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-1838">Type</span></span>  | <span data-ttu-id="b8c96-1839">PropertyTagTypeByte</span><span class="sxs-lookup"><span data-stu-id="b8c96-1839">PropertyTagTypeByte</span></span> |
| <span data-ttu-id="b8c96-1840">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-1840">Count</span></span> | <span data-ttu-id="b8c96-1841">1</span><span class="sxs-lookup"><span data-stu-id="b8c96-1841">1</span></span>                   |



 

## <a name="propertytagpixelunit"></a><span data-ttu-id="b8c96-1842">PropertyTagPixelUnit</span><span class="sxs-lookup"><span data-stu-id="b8c96-1842">PropertyTagPixelUnit</span></span>

<span data-ttu-id="b8c96-1843">Unità per PropertyTagPixelPerUnitX e PropertyTagPixelPerUnitY.</span><span class="sxs-lookup"><span data-stu-id="b8c96-1843">Unit for PropertyTagPixelPerUnitX and PropertyTagPixelPerUnitY.</span></span>



<span data-ttu-id="b8c96-1844">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-1844">Tag</span></span>

<span data-ttu-id="b8c96-1845">0x5110</span><span class="sxs-lookup"><span data-stu-id="b8c96-1845">0x5110</span></span>

<span data-ttu-id="b8c96-1846">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-1846">Type</span></span>

<span data-ttu-id="b8c96-1847">PropertyTagTypeByte</span><span class="sxs-lookup"><span data-stu-id="b8c96-1847">PropertyTagTypeByte</span></span>

<span data-ttu-id="b8c96-1848">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-1848">Count</span></span>

<span data-ttu-id="b8c96-1849">1</span><span class="sxs-lookup"><span data-stu-id="b8c96-1849">1</span></span>

<span data-ttu-id="b8c96-1850">0-sconosciuto</span><span class="sxs-lookup"><span data-stu-id="b8c96-1850">0 - unknown</span></span>



 

## <a name="propertytagpixelperunitx"></a><span data-ttu-id="b8c96-1851">PropertyTagPixelPerUnitX</span><span class="sxs-lookup"><span data-stu-id="b8c96-1851">PropertyTagPixelPerUnitX</span></span>

<span data-ttu-id="b8c96-1852">Pixel per unità nella direzione x.</span><span class="sxs-lookup"><span data-stu-id="b8c96-1852">Pixels per unit in the x direction.</span></span>



| <span data-ttu-id="b8c96-1853">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-1853">Property info</span></span> | <span data-ttu-id="b8c96-1854">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-1854">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="b8c96-1855">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-1855">Tag</span></span>   | <span data-ttu-id="b8c96-1856">0x5111</span><span class="sxs-lookup"><span data-stu-id="b8c96-1856">0x5111</span></span>              |
| <span data-ttu-id="b8c96-1857">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-1857">Type</span></span>  | <span data-ttu-id="b8c96-1858">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="b8c96-1858">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="b8c96-1859">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-1859">Count</span></span> | <span data-ttu-id="b8c96-1860">1</span><span class="sxs-lookup"><span data-stu-id="b8c96-1860">1</span></span>                   |



 

## <a name="propertytagpixelperunity"></a><span data-ttu-id="b8c96-1861">PropertyTagPixelPerUnitY</span><span class="sxs-lookup"><span data-stu-id="b8c96-1861">PropertyTagPixelPerUnitY</span></span>

<span data-ttu-id="b8c96-1862">Pixel per unità nella direzione y.</span><span class="sxs-lookup"><span data-stu-id="b8c96-1862">Pixels per unit in the y direction.</span></span>



| <span data-ttu-id="b8c96-1863">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-1863">Property info</span></span> | <span data-ttu-id="b8c96-1864">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-1864">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="b8c96-1865">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-1865">Tag</span></span>   | <span data-ttu-id="b8c96-1866">0x5112</span><span class="sxs-lookup"><span data-stu-id="b8c96-1866">0x5112</span></span>              |
| <span data-ttu-id="b8c96-1867">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-1867">Type</span></span>  | <span data-ttu-id="b8c96-1868">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="b8c96-1868">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="b8c96-1869">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-1869">Count</span></span> | <span data-ttu-id="b8c96-1870">1</span><span class="sxs-lookup"><span data-stu-id="b8c96-1870">1</span></span>                   |



 

## <a name="propertytagpalettehistogram"></a><span data-ttu-id="b8c96-1871">PropertyTagPaletteHistogram</span><span class="sxs-lookup"><span data-stu-id="b8c96-1871">PropertyTagPaletteHistogram</span></span>

<span data-ttu-id="b8c96-1872">Istogramma tavolozza.</span><span class="sxs-lookup"><span data-stu-id="b8c96-1872">Palette histogram.</span></span>



| <span data-ttu-id="b8c96-1873">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-1873">Property info</span></span> | <span data-ttu-id="b8c96-1874">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-1874">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="b8c96-1875">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-1875">Tag</span></span>   | <span data-ttu-id="b8c96-1876">0x5113</span><span class="sxs-lookup"><span data-stu-id="b8c96-1876">0x5113</span></span>                  |
| <span data-ttu-id="b8c96-1877">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-1877">Type</span></span>  | <span data-ttu-id="b8c96-1878">PropertyTagTypeByte</span><span class="sxs-lookup"><span data-stu-id="b8c96-1878">PropertyTagTypeByte</span></span>     |
| <span data-ttu-id="b8c96-1879">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-1879">Count</span></span> | <span data-ttu-id="b8c96-1880">Lunghezza dell'istogramma</span><span class="sxs-lookup"><span data-stu-id="b8c96-1880">Length of the histogram</span></span> |



 

## <a name="propertytagcopyright"></a><span data-ttu-id="b8c96-1881">PropertyTagCopyright</span><span class="sxs-lookup"><span data-stu-id="b8c96-1881">PropertyTagCopyright</span></span>

<span data-ttu-id="b8c96-1882">Stringa di caratteri con terminazione null che contiene informazioni sul copyright.</span><span class="sxs-lookup"><span data-stu-id="b8c96-1882">Null-terminated character string that contains copyright information.</span></span>



| <span data-ttu-id="b8c96-1883">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-1883">Property info</span></span> | <span data-ttu-id="b8c96-1884">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-1884">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="b8c96-1885">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-1885">Tag</span></span>   | <span data-ttu-id="b8c96-1886">0x8298</span><span class="sxs-lookup"><span data-stu-id="b8c96-1886">0x8298</span></span>                                             |
| <span data-ttu-id="b8c96-1887">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-1887">Type</span></span>  | <span data-ttu-id="b8c96-1888">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="b8c96-1888">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="b8c96-1889">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-1889">Count</span></span> | <span data-ttu-id="b8c96-1890">Lunghezza della stringa che include il carattere di terminazione NULL</span><span class="sxs-lookup"><span data-stu-id="b8c96-1890">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagexifexposuretime"></a><span data-ttu-id="b8c96-1891">PropertyTagExifExposureTime</span><span class="sxs-lookup"><span data-stu-id="b8c96-1891">PropertyTagExifExposureTime</span></span>

<span data-ttu-id="b8c96-1892">Tempo di esposizione, espresso in secondi.</span><span class="sxs-lookup"><span data-stu-id="b8c96-1892">Exposure time, measured in seconds.</span></span>



| <span data-ttu-id="b8c96-1893">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-1893">Property info</span></span> | <span data-ttu-id="b8c96-1894">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-1894">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="b8c96-1895">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-1895">Tag</span></span>   | <span data-ttu-id="b8c96-1896">0x829A</span><span class="sxs-lookup"><span data-stu-id="b8c96-1896">0x829A</span></span>                  |
| <span data-ttu-id="b8c96-1897">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-1897">Type</span></span>  | <span data-ttu-id="b8c96-1898">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="b8c96-1898">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="b8c96-1899">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-1899">Count</span></span> | <span data-ttu-id="b8c96-1900">1</span><span class="sxs-lookup"><span data-stu-id="b8c96-1900">1</span></span>                       |



 

## <a name="propertytagexiffnumber"></a><span data-ttu-id="b8c96-1901">PropertyTagExifFNumber</span><span class="sxs-lookup"><span data-stu-id="b8c96-1901">PropertyTagExifFNumber</span></span>

<span data-ttu-id="b8c96-1902">Numero F.</span><span class="sxs-lookup"><span data-stu-id="b8c96-1902">F number.</span></span>



| <span data-ttu-id="b8c96-1903">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-1903">Property info</span></span> | <span data-ttu-id="b8c96-1904">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-1904">Value</span></span> |
|-------|----------|
| <span data-ttu-id="b8c96-1905">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-1905">Tag</span></span>   | <span data-ttu-id="b8c96-1906">0x829D</span><span class="sxs-lookup"><span data-stu-id="b8c96-1906">0x829D</span></span>   |
| <span data-ttu-id="b8c96-1907">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-1907">Type</span></span>  | <span data-ttu-id="b8c96-1908">RAZIONALE</span><span class="sxs-lookup"><span data-stu-id="b8c96-1908">RATIONAL</span></span> |
| <span data-ttu-id="b8c96-1909">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-1909">Count</span></span> | <span data-ttu-id="b8c96-1910">1</span><span class="sxs-lookup"><span data-stu-id="b8c96-1910">1</span></span>        |



 

## <a name="propertytagexififd"></a><span data-ttu-id="b8c96-1911">PropertyTagExifIFD</span><span class="sxs-lookup"><span data-stu-id="b8c96-1911">PropertyTagExifIFD</span></span>

<span data-ttu-id="b8c96-1912">Tag privato utilizzato da GDI+.</span><span class="sxs-lookup"><span data-stu-id="b8c96-1912">Private tag used by GDI+.</span></span> <span data-ttu-id="b8c96-1913">Non per uso pubblico.</span><span class="sxs-lookup"><span data-stu-id="b8c96-1913">Not for public use.</span></span> <span data-ttu-id="b8c96-1914">GDI+ utilizza questo tag per individuare informazioni specifiche di EXIF.</span><span class="sxs-lookup"><span data-stu-id="b8c96-1914">GDI+ uses this tag to locate Exif-specific information.</span></span>



| <span data-ttu-id="b8c96-1915">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-1915">Property info</span></span> | <span data-ttu-id="b8c96-1916">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-1916">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="b8c96-1917">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-1917">Tag</span></span>   | <span data-ttu-id="b8c96-1918">0x8769</span><span class="sxs-lookup"><span data-stu-id="b8c96-1918">0x8769</span></span>              |
| <span data-ttu-id="b8c96-1919">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-1919">Type</span></span>  | <span data-ttu-id="b8c96-1920">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="b8c96-1920">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="b8c96-1921">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-1921">Count</span></span> | <span data-ttu-id="b8c96-1922">1</span><span class="sxs-lookup"><span data-stu-id="b8c96-1922">1</span></span>                   |



 

## <a name="propertytagiccprofile"></a><span data-ttu-id="b8c96-1923">PropertyTagICCProfile</span><span class="sxs-lookup"><span data-stu-id="b8c96-1923">PropertyTagICCProfile</span></span>

<span data-ttu-id="b8c96-1924">Profilo ICC incorporato nell'immagine.</span><span class="sxs-lookup"><span data-stu-id="b8c96-1924">ICC profile embedded in the image.</span></span>



| <span data-ttu-id="b8c96-1925">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-1925">Property info</span></span> | <span data-ttu-id="b8c96-1926">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-1926">Value</span></span> |
|-------|-----------------------|
| <span data-ttu-id="b8c96-1927">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-1927">Tag</span></span>   | <span data-ttu-id="b8c96-1928">0x8773</span><span class="sxs-lookup"><span data-stu-id="b8c96-1928">0x8773</span></span>                |
| <span data-ttu-id="b8c96-1929">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-1929">Type</span></span>  | <span data-ttu-id="b8c96-1930">PropertyTagTypeByte</span><span class="sxs-lookup"><span data-stu-id="b8c96-1930">PropertyTagTypeByte</span></span>   |
| <span data-ttu-id="b8c96-1931">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-1931">Count</span></span> | <span data-ttu-id="b8c96-1932">Lunghezza del profilo</span><span class="sxs-lookup"><span data-stu-id="b8c96-1932">Length of the profile</span></span> |



 

## <a name="propertytagexifexposureprog"></a><span data-ttu-id="b8c96-1933">PropertyTagExifExposureProg</span><span class="sxs-lookup"><span data-stu-id="b8c96-1933">PropertyTagExifExposureProg</span></span>

<span data-ttu-id="b8c96-1934">Classe del programma utilizzata dalla fotocamera per impostare l'esposizione quando viene acquisita l'immagine.</span><span class="sxs-lookup"><span data-stu-id="b8c96-1934">Class of the program used by the camera to set exposure when the picture is taken.</span></span>



<span data-ttu-id="b8c96-1935">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-1935">Tag</span></span>

<span data-ttu-id="b8c96-1936">0x8822</span><span class="sxs-lookup"><span data-stu-id="b8c96-1936">0x8822</span></span>

<span data-ttu-id="b8c96-1937">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-1937">Type</span></span>

<span data-ttu-id="b8c96-1938">SHORT</span><span class="sxs-lookup"><span data-stu-id="b8c96-1938">SHORT</span></span>

<span data-ttu-id="b8c96-1939">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-1939">Count</span></span>

<span data-ttu-id="b8c96-1940">1</span><span class="sxs-lookup"><span data-stu-id="b8c96-1940">1</span></span>

<span data-ttu-id="b8c96-1941">Predefinito</span><span class="sxs-lookup"><span data-stu-id="b8c96-1941">Default</span></span>

<span data-ttu-id="b8c96-1942">0</span><span class="sxs-lookup"><span data-stu-id="b8c96-1942">0</span></span>

<span data-ttu-id="b8c96-1943">0-non definito 1-manuale 2-programma normale 3-priorità di apertura 4-priorità di otturazione 5-programma creativo (distorto verso la profondità del campo) 6-programma di azione (polarizzato verso Fast velocità dell'otturatore) 7-modalità verticale (per le foto di chiusura con lo sfondo non attivo) 8-modalità orizzontale (per le foto paesaggistiche con lo sfondo attivo) da 9 a 255-riservato</span><span class="sxs-lookup"><span data-stu-id="b8c96-1943">0 - not defined 1 - manual 2 - normal program 3 - aperture priority 4 - shutter priority 5 - creative program (biased toward depth of field) 6 - action program (biased toward fast shutter speed) 7 - portrait mode (for close-up photos with the background out of focus) 8 - landscape mode (for landscape photos with the background in focus) 9 to 255 - reserved</span></span>



 

## <a name="propertytagexifspectralsense"></a><span data-ttu-id="b8c96-1944">PropertyTagExifSpectralSense</span><span class="sxs-lookup"><span data-stu-id="b8c96-1944">PropertyTagExifSpectralSense</span></span>

<span data-ttu-id="b8c96-1945">Stringa di caratteri con terminazione null che specifica la sensibilità spettrale di ogni canale della fotocamera usata.</span><span class="sxs-lookup"><span data-stu-id="b8c96-1945">Null-terminated character string that specifies the spectral sensitivity of each channel of the camera used.</span></span> <span data-ttu-id="b8c96-1946">La stringa è compatibile con lo standard sviluppato dal comitato tecnico ASTM.</span><span class="sxs-lookup"><span data-stu-id="b8c96-1946">The string is compatible with the standard developed by the ASTM Technical Committee.</span></span>



| <span data-ttu-id="b8c96-1947">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-1947">Property info</span></span> | <span data-ttu-id="b8c96-1948">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-1948">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="b8c96-1949">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-1949">Tag</span></span>   | <span data-ttu-id="b8c96-1950">0x8824</span><span class="sxs-lookup"><span data-stu-id="b8c96-1950">0x8824</span></span>                                             |
| <span data-ttu-id="b8c96-1951">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-1951">Type</span></span>  | <span data-ttu-id="b8c96-1952">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="b8c96-1952">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="b8c96-1953">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-1953">Count</span></span> | <span data-ttu-id="b8c96-1954">Lunghezza della stringa che include il carattere di terminazione NULL</span><span class="sxs-lookup"><span data-stu-id="b8c96-1954">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytaggpsifd"></a><span data-ttu-id="b8c96-1955">PropertyTagGpsIFD</span><span class="sxs-lookup"><span data-stu-id="b8c96-1955">PropertyTagGpsIFD</span></span>

<span data-ttu-id="b8c96-1956">Offset a un blocco di elementi di proprietà GPS.</span><span class="sxs-lookup"><span data-stu-id="b8c96-1956">Offset to a block of GPS property items.</span></span> <span data-ttu-id="b8c96-1957">Gli elementi di proprietà i cui tag hanno il prefisso PropertyTagGps vengono archiviati nel blocco GPS.</span><span class="sxs-lookup"><span data-stu-id="b8c96-1957">Property items whose tags have the prefix PropertyTagGps are stored in the GPS block.</span></span> <span data-ttu-id="b8c96-1958">Gli elementi delle proprietà GPS sono definiti nella specifica EXIF.</span><span class="sxs-lookup"><span data-stu-id="b8c96-1958">The GPS property items are defined in the EXIF specification.</span></span> <span data-ttu-id="b8c96-1959">GDI+ utilizza questo tag per individuare le informazioni GPS, ma GDI+ non espone questo tag per l'utilizzo pubblico.</span><span class="sxs-lookup"><span data-stu-id="b8c96-1959">GDI+ uses this tag to locate GPS information, but GDI+ does not expose this tag for public use.</span></span>



| <span data-ttu-id="b8c96-1960">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-1960">Property info</span></span> | <span data-ttu-id="b8c96-1961">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-1961">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="b8c96-1962">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-1962">Tag</span></span>   | <span data-ttu-id="b8c96-1963">0x8825</span><span class="sxs-lookup"><span data-stu-id="b8c96-1963">0x8825</span></span>              |
| <span data-ttu-id="b8c96-1964">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-1964">Type</span></span>  | <span data-ttu-id="b8c96-1965">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="b8c96-1965">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="b8c96-1966">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-1966">Count</span></span> | <span data-ttu-id="b8c96-1967">1</span><span class="sxs-lookup"><span data-stu-id="b8c96-1967">1</span></span>                   |



 

## <a name="propertytagexifisospeed"></a><span data-ttu-id="b8c96-1968">PropertyTagExifISOSpeed</span><span class="sxs-lookup"><span data-stu-id="b8c96-1968">PropertyTagExifISOSpeed</span></span>

<span data-ttu-id="b8c96-1969">Velocità ISO e latitudine ISO della fotocamera o del dispositivo di input come specificato in ISO 12232.</span><span class="sxs-lookup"><span data-stu-id="b8c96-1969">ISO speed and ISO latitude of the camera or input device as specified in ISO 12232.</span></span>



| <span data-ttu-id="b8c96-1970">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-1970">Property info</span></span> | <span data-ttu-id="b8c96-1971">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-1971">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="b8c96-1972">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-1972">Tag</span></span>   | <span data-ttu-id="b8c96-1973">0x8827</span><span class="sxs-lookup"><span data-stu-id="b8c96-1973">0x8827</span></span>               |
| <span data-ttu-id="b8c96-1974">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-1974">Type</span></span>  | <span data-ttu-id="b8c96-1975">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="b8c96-1975">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="b8c96-1976">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-1976">Count</span></span> | <span data-ttu-id="b8c96-1977">Qualsiasi</span><span class="sxs-lookup"><span data-stu-id="b8c96-1977">Any</span></span>                  |



 

## <a name="propertytagexifoecf"></a><span data-ttu-id="b8c96-1978">PropertyTagExifOECF</span><span class="sxs-lookup"><span data-stu-id="b8c96-1978">PropertyTagExifOECF</span></span>

<span data-ttu-id="b8c96-1979">Funzione di conversione optoelettronica (OECF) specificata in ISO 14524.</span><span class="sxs-lookup"><span data-stu-id="b8c96-1979">Optoelectronic conversion function (OECF) specified in ISO 14524.</span></span> <span data-ttu-id="b8c96-1980">OECF è la relazione tra l'input ottico della fotocamera e i valori di immagine.</span><span class="sxs-lookup"><span data-stu-id="b8c96-1980">The OECF is the relationship between the camera optical input and the image values.</span></span>



| <span data-ttu-id="b8c96-1981">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-1981">Property info</span></span> | <span data-ttu-id="b8c96-1982">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-1982">Value</span></span> |
|-------|--------------------------|
| <span data-ttu-id="b8c96-1983">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-1983">Tag</span></span>   | <span data-ttu-id="b8c96-1984">0x8828</span><span class="sxs-lookup"><span data-stu-id="b8c96-1984">0x8828</span></span>                   |
| <span data-ttu-id="b8c96-1985">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-1985">Type</span></span>  | <span data-ttu-id="b8c96-1986">PropertyTagTypeUndefined</span><span class="sxs-lookup"><span data-stu-id="b8c96-1986">PropertyTagTypeUndefined</span></span> |
| <span data-ttu-id="b8c96-1987">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-1987">Count</span></span> | <span data-ttu-id="b8c96-1988">Qualsiasi</span><span class="sxs-lookup"><span data-stu-id="b8c96-1988">Any</span></span>                      |



 

## <a name="propertytagexifver"></a><span data-ttu-id="b8c96-1989">PropertyTagExifVer</span><span class="sxs-lookup"><span data-stu-id="b8c96-1989">PropertyTagExifVer</span></span>

<span data-ttu-id="b8c96-1990">Versione dello standard EXIF supportata.</span><span class="sxs-lookup"><span data-stu-id="b8c96-1990">Version of the EXIF standard supported.</span></span> <span data-ttu-id="b8c96-1991">La mancata esistenza di questo campo viene utilizzata per indicare la non conformità allo standard.</span><span class="sxs-lookup"><span data-stu-id="b8c96-1991">Nonexistence of this field is taken to mean nonconformance to the standard.</span></span> <span data-ttu-id="b8c96-1992">La conformità allo standard è indicata dalla registrazione di 0210 come stringa ASCII a 4 byte.</span><span class="sxs-lookup"><span data-stu-id="b8c96-1992">Conformance to the standard is indicated by recording 0210 as a 4-byte ASCII string.</span></span> <span data-ttu-id="b8c96-1993">Poiché il tipo è PropertyTagTypeUndefined, non esiste alcun carattere di terminazione NULL.</span><span class="sxs-lookup"><span data-stu-id="b8c96-1993">Because the type is PropertyTagTypeUndefined, there is no NULL terminator.</span></span>



| <span data-ttu-id="b8c96-1994">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-1994">Property info</span></span> | <span data-ttu-id="b8c96-1995">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-1995">Value</span></span> |
|---------|--------------------------|
| <span data-ttu-id="b8c96-1996">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-1996">Tag</span></span>     | <span data-ttu-id="b8c96-1997">0x9000</span><span class="sxs-lookup"><span data-stu-id="b8c96-1997">0x9000</span></span>                   |
| <span data-ttu-id="b8c96-1998">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-1998">Type</span></span>    | <span data-ttu-id="b8c96-1999">PropertyTagTypeUndefined</span><span class="sxs-lookup"><span data-stu-id="b8c96-1999">PropertyTagTypeUndefined</span></span> |
| <span data-ttu-id="b8c96-2000">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-2000">Count</span></span>   | <span data-ttu-id="b8c96-2001">4</span><span class="sxs-lookup"><span data-stu-id="b8c96-2001">4</span></span>                        |
| <span data-ttu-id="b8c96-2002">Predefinito</span><span class="sxs-lookup"><span data-stu-id="b8c96-2002">Default</span></span> | <span data-ttu-id="b8c96-2003">0210</span><span class="sxs-lookup"><span data-stu-id="b8c96-2003">0210</span></span>                     |



 

## <a name="propertytagexifdtorig"></a><span data-ttu-id="b8c96-2004">PropertyTagExifDTOrig</span><span class="sxs-lookup"><span data-stu-id="b8c96-2004">PropertyTagExifDTOrig</span></span>

<span data-ttu-id="b8c96-2005">Data e ora di generazione dei dati dell'immagine originale.</span><span class="sxs-lookup"><span data-stu-id="b8c96-2005">Date and time when the original image data was generated.</span></span> <span data-ttu-id="b8c96-2006">Per un DSC, la data e l'ora in cui è stata acquisita l'immagine.</span><span class="sxs-lookup"><span data-stu-id="b8c96-2006">For a DSC, the date and time when the picture was taken.</span></span> <span data-ttu-id="b8c96-2007">Il formato è aaaa: MM: GG HH: MM: SS con ora indicata nel formato a 24 ore e la data e l'ora separate da un carattere vuoto (0x2000).</span><span class="sxs-lookup"><span data-stu-id="b8c96-2007">The format is YYYY:MM:DD HH:MM:SS with time shown in 24-hour format and the date and time separated by one blank character (0x2000).</span></span> <span data-ttu-id="b8c96-2008">La lunghezza della stringa di caratteri è 20 byte, incluso il terminatore NULL.</span><span class="sxs-lookup"><span data-stu-id="b8c96-2008">The character string length is 20 bytes including the NULL terminator.</span></span> <span data-ttu-id="b8c96-2009">Quando il campo è vuoto, viene considerato sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="b8c96-2009">When the field is empty, it is treated as unknown.</span></span>



| <span data-ttu-id="b8c96-2010">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-2010">Property info</span></span> | <span data-ttu-id="b8c96-2011">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-2011">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="b8c96-2012">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-2012">Tag</span></span>   | <span data-ttu-id="b8c96-2013">0x9003</span><span class="sxs-lookup"><span data-stu-id="b8c96-2013">0x9003</span></span>               |
| <span data-ttu-id="b8c96-2014">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-2014">Type</span></span>  | <span data-ttu-id="b8c96-2015">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="b8c96-2015">PropertyTagTypeASCII</span></span> |
| <span data-ttu-id="b8c96-2016">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-2016">Count</span></span> | <span data-ttu-id="b8c96-2017">20</span><span class="sxs-lookup"><span data-stu-id="b8c96-2017">20</span></span>                   |



 

## <a name="propertytagexifdtdigitized"></a><span data-ttu-id="b8c96-2018">PropertyTagExifDTDigitized</span><span class="sxs-lookup"><span data-stu-id="b8c96-2018">PropertyTagExifDTDigitized</span></span>

<span data-ttu-id="b8c96-2019">Data e ora in cui l'immagine è stata archiviata come dati digitali.</span><span class="sxs-lookup"><span data-stu-id="b8c96-2019">Date and time when the image was stored as digital data.</span></span> <span data-ttu-id="b8c96-2020">Se, ad esempio, un'immagine è stata acquisita da DSC e nello stesso momento in cui il file è stato registrato, DateTimeOriginal e DateTimeDigitized avranno lo stesso contenuto.</span><span class="sxs-lookup"><span data-stu-id="b8c96-2020">If, for example, an image was captured by DSC and at the same time the file was recorded, then DateTimeOriginal and DateTimeDigitized will have the same contents.</span></span>

<span data-ttu-id="b8c96-2021">Il formato è aaaa: MM: GG HH: MM: SS con ora indicata nel formato a 24 ore e la data e l'ora separate da un carattere vuoto (0x2000).</span><span class="sxs-lookup"><span data-stu-id="b8c96-2021">The format is YYYY:MM:DD HH:MM:SS with time shown in 24-hour format and the date and time separated by one blank character (0x2000).</span></span> <span data-ttu-id="b8c96-2022">La lunghezza della stringa di caratteri è 20 byte, incluso il terminatore NULL.</span><span class="sxs-lookup"><span data-stu-id="b8c96-2022">The character string length is 20 bytes including the NULL terminator.</span></span> <span data-ttu-id="b8c96-2023">Quando il campo è vuoto, viene considerato sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="b8c96-2023">When the field is empty, it is treated as unknown.</span></span>



| <span data-ttu-id="b8c96-2024">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-2024">Property info</span></span> | <span data-ttu-id="b8c96-2025">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-2025">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="b8c96-2026">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-2026">Tag</span></span>   | <span data-ttu-id="b8c96-2027">0x9004</span><span class="sxs-lookup"><span data-stu-id="b8c96-2027">0x9004</span></span>               |
| <span data-ttu-id="b8c96-2028">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-2028">Type</span></span>  | <span data-ttu-id="b8c96-2029">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="b8c96-2029">PropertyTagTypeASCII</span></span> |
| <span data-ttu-id="b8c96-2030">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-2030">Count</span></span> | <span data-ttu-id="b8c96-2031">20</span><span class="sxs-lookup"><span data-stu-id="b8c96-2031">20</span></span>                   |



 

## <a name="propertytagexifcompconfig"></a><span data-ttu-id="b8c96-2032">PropertyTagExifCompConfig</span><span class="sxs-lookup"><span data-stu-id="b8c96-2032">PropertyTagExifCompConfig</span></span>

<span data-ttu-id="b8c96-2033">Informazioni specifiche per i dati compressi.</span><span class="sxs-lookup"><span data-stu-id="b8c96-2033">Information specific to compressed data.</span></span> <span data-ttu-id="b8c96-2034">I canali di ogni componente sono disposti in ordine dal primo componente al quarto.</span><span class="sxs-lookup"><span data-stu-id="b8c96-2034">The channels of each component are arranged in order from the first component to the fourth.</span></span> <span data-ttu-id="b8c96-2035">Per i dati non compressi, la disposizione dei dati viene fornita nel tag PropertyTagPhotometricInterp.</span><span class="sxs-lookup"><span data-stu-id="b8c96-2035">For uncompressed data, the data arrangement is given in the PropertyTagPhotometricInterp tag.</span></span>

<span data-ttu-id="b8c96-2036">Tuttavia, poiché PropertyTagPhotometricInterp è in grado di esprimere solo l'ordine di Y, CB e CR, questo tag viene fornito nei casi in cui i dati compressi utilizzano componenti diversi da Y, CB e CR e per supportare altre sequenze.</span><span class="sxs-lookup"><span data-stu-id="b8c96-2036">However, because PropertyTagPhotometricInterp can only express the order of Y, Cb, and Cr, this tag is provided for cases when compressed data uses components other than Y, Cb, and Cr and to support other sequences.</span></span>



<span data-ttu-id="b8c96-2037">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-2037">Tag</span></span>

<span data-ttu-id="b8c96-2038">0x9101</span><span class="sxs-lookup"><span data-stu-id="b8c96-2038">0x9101</span></span>

<span data-ttu-id="b8c96-2039">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-2039">Type</span></span>

<span data-ttu-id="b8c96-2040">PropertyTagTypeUndefined</span><span class="sxs-lookup"><span data-stu-id="b8c96-2040">PropertyTagTypeUndefined</span></span>

<span data-ttu-id="b8c96-2041">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-2041">Count</span></span>

<span data-ttu-id="b8c96-2042">4</span><span class="sxs-lookup"><span data-stu-id="b8c96-2042">4</span></span>

<span data-ttu-id="b8c96-2043">Predefinito</span><span class="sxs-lookup"><span data-stu-id="b8c96-2043">Default</span></span>

<span data-ttu-id="b8c96-2044">4 5 6 0 (se RGB non compresso) 1 2 3 0 (altri casi)</span><span class="sxs-lookup"><span data-stu-id="b8c96-2044">4 5 6 0 (if RGB uncompressed) 1 2 3 0 (other cases)</span></span>

<span data-ttu-id="b8c96-2045">0: non esiste 1-Y 2-CB 3-CR 4-R 5-G 6-B other-reserved</span><span class="sxs-lookup"><span data-stu-id="b8c96-2045">0 - does not exist 1 - Y 2 - Cb 3 - Cr 4 - R 5 - G 6 - B Other - reserved</span></span>



 

## <a name="propertytagexifcompbpp"></a><span data-ttu-id="b8c96-2046">PropertyTagExifCompBPP</span><span class="sxs-lookup"><span data-stu-id="b8c96-2046">PropertyTagExifCompBPP</span></span>

<span data-ttu-id="b8c96-2047">Informazioni specifiche per i dati compressi.</span><span class="sxs-lookup"><span data-stu-id="b8c96-2047">Information specific to compressed data.</span></span> <span data-ttu-id="b8c96-2048">La modalità di compressione utilizzata per un'immagine compressa è indicata in unità BPP.</span><span class="sxs-lookup"><span data-stu-id="b8c96-2048">The compression mode used for a compressed image is indicated in unit BPP.</span></span>



| <span data-ttu-id="b8c96-2049">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-2049">Property info</span></span> | <span data-ttu-id="b8c96-2050">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-2050">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="b8c96-2051">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-2051">Tag</span></span>   | <span data-ttu-id="b8c96-2052">0x9102</span><span class="sxs-lookup"><span data-stu-id="b8c96-2052">0x9102</span></span>                  |
| <span data-ttu-id="b8c96-2053">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-2053">Type</span></span>  | <span data-ttu-id="b8c96-2054">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="b8c96-2054">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="b8c96-2055">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-2055">Count</span></span> | <span data-ttu-id="b8c96-2056">1</span><span class="sxs-lookup"><span data-stu-id="b8c96-2056">1</span></span>                       |



 

## <a name="propertytagexifshutterspeed"></a><span data-ttu-id="b8c96-2057">PropertyTagExifShutterSpeed</span><span class="sxs-lookup"><span data-stu-id="b8c96-2057">PropertyTagExifShutterSpeed</span></span>

<span data-ttu-id="b8c96-2058">Velocità dell'otturatore.</span><span class="sxs-lookup"><span data-stu-id="b8c96-2058">Shutter speed.</span></span> <span data-ttu-id="b8c96-2059">L'unità è il valore di sistema additivo per l'esposizione fotografica (apice).</span><span class="sxs-lookup"><span data-stu-id="b8c96-2059">The unit is the Additive System of Photographic Exposure (APEX) value.</span></span>



| <span data-ttu-id="b8c96-2060">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-2060">Property info</span></span> | <span data-ttu-id="b8c96-2061">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-2061">Value</span></span> |
|-------|--------------------------|
| <span data-ttu-id="b8c96-2062">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-2062">Tag</span></span>   | <span data-ttu-id="b8c96-2063">0x9201</span><span class="sxs-lookup"><span data-stu-id="b8c96-2063">0x9201</span></span>                   |
| <span data-ttu-id="b8c96-2064">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-2064">Type</span></span>  | <span data-ttu-id="b8c96-2065">PropertyTagTypeSRational</span><span class="sxs-lookup"><span data-stu-id="b8c96-2065">PropertyTagTypeSRational</span></span> |
| <span data-ttu-id="b8c96-2066">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-2066">Count</span></span> | <span data-ttu-id="b8c96-2067">1</span><span class="sxs-lookup"><span data-stu-id="b8c96-2067">1</span></span>                        |



 

## <a name="propertytagexifaperture"></a><span data-ttu-id="b8c96-2068">PropertyTagExifAperture</span><span class="sxs-lookup"><span data-stu-id="b8c96-2068">PropertyTagExifAperture</span></span>

<span data-ttu-id="b8c96-2069">Apertura dell'obiettivo.</span><span class="sxs-lookup"><span data-stu-id="b8c96-2069">Lens aperture.</span></span> <span data-ttu-id="b8c96-2070">L'unità è il valore apice.</span><span class="sxs-lookup"><span data-stu-id="b8c96-2070">The unit is the APEX value.</span></span>



| <span data-ttu-id="b8c96-2071">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-2071">Property info</span></span> | <span data-ttu-id="b8c96-2072">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-2072">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="b8c96-2073">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-2073">Tag</span></span>   | <span data-ttu-id="b8c96-2074">0x9202</span><span class="sxs-lookup"><span data-stu-id="b8c96-2074">0x9202</span></span>                  |
| <span data-ttu-id="b8c96-2075">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-2075">Type</span></span>  | <span data-ttu-id="b8c96-2076">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="b8c96-2076">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="b8c96-2077">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-2077">Count</span></span> | <span data-ttu-id="b8c96-2078">1</span><span class="sxs-lookup"><span data-stu-id="b8c96-2078">1</span></span>                       |



 

## <a name="propertytagexifbrightness"></a><span data-ttu-id="b8c96-2079">PropertyTagExifBrightness</span><span class="sxs-lookup"><span data-stu-id="b8c96-2079">PropertyTagExifBrightness</span></span>

<span data-ttu-id="b8c96-2080">Valore di luminosità.</span><span class="sxs-lookup"><span data-stu-id="b8c96-2080">Brightness value.</span></span> <span data-ttu-id="b8c96-2081">L'unità è il valore apice.</span><span class="sxs-lookup"><span data-stu-id="b8c96-2081">The unit is the APEX value.</span></span> <span data-ttu-id="b8c96-2082">Normalmente viene specificato nell'intervallo compreso tra-99,99 e 99,99.</span><span class="sxs-lookup"><span data-stu-id="b8c96-2082">Ordinarily it is given in the range of -99.99 to 99.99.</span></span>



| <span data-ttu-id="b8c96-2083">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-2083">Property info</span></span> | <span data-ttu-id="b8c96-2084">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-2084">Value</span></span> |
|-------|--------------------------|
| <span data-ttu-id="b8c96-2085">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-2085">Tag</span></span>   | <span data-ttu-id="b8c96-2086">0x9203</span><span class="sxs-lookup"><span data-stu-id="b8c96-2086">0x9203</span></span>                   |
| <span data-ttu-id="b8c96-2087">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-2087">Type</span></span>  | <span data-ttu-id="b8c96-2088">PropertyTagTypeSRational</span><span class="sxs-lookup"><span data-stu-id="b8c96-2088">PropertyTagTypeSRational</span></span> |
| <span data-ttu-id="b8c96-2089">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-2089">Count</span></span> | <span data-ttu-id="b8c96-2090">1</span><span class="sxs-lookup"><span data-stu-id="b8c96-2090">1</span></span>                        |



 

## <a name="propertytagexifexposurebias"></a><span data-ttu-id="b8c96-2091">PropertyTagExifExposureBias</span><span class="sxs-lookup"><span data-stu-id="b8c96-2091">PropertyTagExifExposureBias</span></span>

<span data-ttu-id="b8c96-2092">Distorsione dell'esposizione.</span><span class="sxs-lookup"><span data-stu-id="b8c96-2092">Exposure bias.</span></span> <span data-ttu-id="b8c96-2093">L'unità è il valore apice.</span><span class="sxs-lookup"><span data-stu-id="b8c96-2093">The unit is the APEX value.</span></span> <span data-ttu-id="b8c96-2094">Normalmente viene specificato nell'intervallo compreso tra-99,99 e 99,99.</span><span class="sxs-lookup"><span data-stu-id="b8c96-2094">Ordinarily it is given in the range -99.99 to 99.99.</span></span>



| <span data-ttu-id="b8c96-2095">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-2095">Property info</span></span> | <span data-ttu-id="b8c96-2096">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-2096">Value</span></span> |
|-------|--------------------------|
| <span data-ttu-id="b8c96-2097">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-2097">Tag</span></span>   | <span data-ttu-id="b8c96-2098">0x9204</span><span class="sxs-lookup"><span data-stu-id="b8c96-2098">0x9204</span></span>                   |
| <span data-ttu-id="b8c96-2099">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-2099">Type</span></span>  | <span data-ttu-id="b8c96-2100">PropertyTagTypeSRational</span><span class="sxs-lookup"><span data-stu-id="b8c96-2100">PropertyTagTypeSRational</span></span> |
| <span data-ttu-id="b8c96-2101">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-2101">Count</span></span> | <span data-ttu-id="b8c96-2102">1</span><span class="sxs-lookup"><span data-stu-id="b8c96-2102">1</span></span>                        |



 

## <a name="propertytagexifmaxaperture"></a><span data-ttu-id="b8c96-2103">PropertyTagExifMaxAperture</span><span class="sxs-lookup"><span data-stu-id="b8c96-2103">PropertyTagExifMaxAperture</span></span>

<span data-ttu-id="b8c96-2104">Numero F più piccolo dell'obiettivo.</span><span class="sxs-lookup"><span data-stu-id="b8c96-2104">Smallest F number of the lens.</span></span> <span data-ttu-id="b8c96-2105">L'unità è il valore apice.</span><span class="sxs-lookup"><span data-stu-id="b8c96-2105">The unit is the APEX value.</span></span> <span data-ttu-id="b8c96-2106">Normalmente viene specificato nell'intervallo compreso tra 00,00 e 99,99, ma non è limitato a questo intervallo.</span><span class="sxs-lookup"><span data-stu-id="b8c96-2106">Ordinarily it is given in the range of 00.00 to 99.99, but it is not limited to this range.</span></span>



| <span data-ttu-id="b8c96-2107">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-2107">Property info</span></span> | <span data-ttu-id="b8c96-2108">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-2108">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="b8c96-2109">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-2109">Tag</span></span>   | <span data-ttu-id="b8c96-2110">0x9205</span><span class="sxs-lookup"><span data-stu-id="b8c96-2110">0x9205</span></span>                  |
| <span data-ttu-id="b8c96-2111">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-2111">Type</span></span>  | <span data-ttu-id="b8c96-2112">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="b8c96-2112">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="b8c96-2113">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-2113">Count</span></span> | <span data-ttu-id="b8c96-2114">1</span><span class="sxs-lookup"><span data-stu-id="b8c96-2114">1</span></span>                       |



 

## <a name="propertytagexifsubjectdist"></a><span data-ttu-id="b8c96-2115">PropertyTagExifSubjectDist</span><span class="sxs-lookup"><span data-stu-id="b8c96-2115">PropertyTagExifSubjectDist</span></span>

<span data-ttu-id="b8c96-2116">Distanza al soggetto, misurata in metri.</span><span class="sxs-lookup"><span data-stu-id="b8c96-2116">Distance to the subject, measured in meters.</span></span>



| <span data-ttu-id="b8c96-2117">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-2117">Property info</span></span> | <span data-ttu-id="b8c96-2118">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-2118">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="b8c96-2119">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-2119">Tag</span></span>   | <span data-ttu-id="b8c96-2120">0x9206</span><span class="sxs-lookup"><span data-stu-id="b8c96-2120">0x9206</span></span>                  |
| <span data-ttu-id="b8c96-2121">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-2121">Type</span></span>  | <span data-ttu-id="b8c96-2122">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="b8c96-2122">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="b8c96-2123">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-2123">Count</span></span> | <span data-ttu-id="b8c96-2124">1</span><span class="sxs-lookup"><span data-stu-id="b8c96-2124">1</span></span>                       |



 

## <a name="propertytagexifmeteringmode"></a><span data-ttu-id="b8c96-2125">PropertyTagExifMeteringMode</span><span class="sxs-lookup"><span data-stu-id="b8c96-2125">PropertyTagExifMeteringMode</span></span>

<span data-ttu-id="b8c96-2126">Modalità di misurazione.</span><span class="sxs-lookup"><span data-stu-id="b8c96-2126">Metering mode.</span></span>



<span data-ttu-id="b8c96-2127">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-2127">Tag</span></span>

<span data-ttu-id="b8c96-2128">0x9207</span><span class="sxs-lookup"><span data-stu-id="b8c96-2128">0x9207</span></span>

<span data-ttu-id="b8c96-2129">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-2129">Type</span></span>

<span data-ttu-id="b8c96-2130">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="b8c96-2130">PropertyTagTypeShort</span></span>

<span data-ttu-id="b8c96-2131">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-2131">Count</span></span>

<span data-ttu-id="b8c96-2132">1</span><span class="sxs-lookup"><span data-stu-id="b8c96-2132">1</span></span>

<span data-ttu-id="b8c96-2133">Predefinito</span><span class="sxs-lookup"><span data-stu-id="b8c96-2133">Default</span></span>

<span data-ttu-id="b8c96-2134">0</span><span class="sxs-lookup"><span data-stu-id="b8c96-2134">0</span></span>

<span data-ttu-id="b8c96-2135">0: Unknown 1-Average 2-CenterWeightedAverage 3-spot 4-multispot 5-pattern 6-partial 7 to 254-reserved 255-other</span><span class="sxs-lookup"><span data-stu-id="b8c96-2135">0 - unknown 1 - Average 2 - CenterWeightedAverage 3 - Spot 4 - MultiSpot 5 - Pattern 6 - Partial 7 to 254 - reserved 255 - other</span></span>



 

## <a name="propertytagexiflightsource"></a><span data-ttu-id="b8c96-2136">PropertyTagExifLightSource</span><span class="sxs-lookup"><span data-stu-id="b8c96-2136">PropertyTagExifLightSource</span></span>

<span data-ttu-id="b8c96-2137">Tipo di origine di luce.</span><span class="sxs-lookup"><span data-stu-id="b8c96-2137">Type of light source.</span></span>



<span data-ttu-id="b8c96-2138">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-2138">Tag</span></span>

<span data-ttu-id="b8c96-2139">0x9208</span><span class="sxs-lookup"><span data-stu-id="b8c96-2139">0x9208</span></span>

<span data-ttu-id="b8c96-2140">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-2140">Type</span></span>

<span data-ttu-id="b8c96-2141">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="b8c96-2141">PropertyTagTypeShort</span></span>

<span data-ttu-id="b8c96-2142">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-2142">Count</span></span>

<span data-ttu-id="b8c96-2143">1</span><span class="sxs-lookup"><span data-stu-id="b8c96-2143">1</span></span>

<span data-ttu-id="b8c96-2144">Predefinito</span><span class="sxs-lookup"><span data-stu-id="b8c96-2144">Default</span></span>

<span data-ttu-id="b8c96-2145">0</span><span class="sxs-lookup"><span data-stu-id="b8c96-2145">0</span></span>

<span data-ttu-id="b8c96-2146">0-Unknown 1-Daylight 2-fluorescente 3-Tungsten 17-standard Light A 18-standard Light B 19-standard Light C 20-D55 21-D65 22-D75 23 to 254-reserved 255-other</span><span class="sxs-lookup"><span data-stu-id="b8c96-2146">0 - unknown 1 - Daylight 2 - Flourescent 3 - Tungsten 17 - Standard Light A 18 - Standard Light B 19 - Standard Light C 20 - D55 21 - D65 22 - D75 23 to 254 - reserved 255 - other</span></span>



 

## <a name="propertytagexifflash"></a><span data-ttu-id="b8c96-2147">PropertyTagExifFlash</span><span class="sxs-lookup"><span data-stu-id="b8c96-2147">PropertyTagExifFlash</span></span>

<span data-ttu-id="b8c96-2148">Stato del flash.</span><span class="sxs-lookup"><span data-stu-id="b8c96-2148">Flash status.</span></span> <span data-ttu-id="b8c96-2149">Questo tag viene registrato quando un'immagine viene eseguita utilizzando una luce stroboscopica (Flash).</span><span class="sxs-lookup"><span data-stu-id="b8c96-2149">This tag is recorded when an image is taken using a strobe light (flash).</span></span> <span data-ttu-id="b8c96-2150">Il bit 0 indica lo stato di attivazione del flash e i bit 1 e 2 indicano lo stato di restituzione del flash.</span><span class="sxs-lookup"><span data-stu-id="b8c96-2150">Bit 0 indicates the flash firing status, and bits 1 and 2 indicate the flash return status.</span></span>



<span data-ttu-id="b8c96-2151">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-2151">Tag</span></span>

<span data-ttu-id="b8c96-2152">0x9209</span><span class="sxs-lookup"><span data-stu-id="b8c96-2152">0x9209</span></span>

<span data-ttu-id="b8c96-2153">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-2153">Type</span></span>

<span data-ttu-id="b8c96-2154">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="b8c96-2154">PropertyTagTypeShort</span></span>

<span data-ttu-id="b8c96-2155">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-2155">Count</span></span>

<span data-ttu-id="b8c96-2156">1</span><span class="sxs-lookup"><span data-stu-id="b8c96-2156">1</span></span>

<span data-ttu-id="b8c96-2157">Valori per bit 0 che indicano se il flash generato: 0B-Flash non ha attivato 1B-Flash attivato</span><span class="sxs-lookup"><span data-stu-id="b8c96-2157">Values for bit 0 that indicate whether the flash fired: 0b - flash did not fire 1b - flash fired</span></span>

<span data-ttu-id="b8c96-2158">Valori per BITS 1 e 2 che indicano lo stato della luce restituita: 00B-nessuna funzione di rilevamento del ritorno stroboscopio 01B-riservato 10B-Strobe return Light non rilevato 11b-Strobe return light rilevato</span><span class="sxs-lookup"><span data-stu-id="b8c96-2158">Values for bits 1 and 2 that indicate the status of returned light: 00b - no strobe return detection function 01b - reserved 10b - strobe return light not detected 11b - strobe return light detected</span></span>

<span data-ttu-id="b8c96-2159">Valori dei tag flash derivati: 0x0000-Flash non ha attivato 0x0001-Flash fired 0x0005-Strobe return Light non rilevato</span><span class="sxs-lookup"><span data-stu-id="b8c96-2159">Resulting flash tag values: 0x0000 - flash did not fire 0x0001 - flash fired 0x0005 - strobe return light not detected</span></span>



 

## <a name="propertytagexiffocallength"></a><span data-ttu-id="b8c96-2160">PropertyTagExifFocalLength</span><span class="sxs-lookup"><span data-stu-id="b8c96-2160">PropertyTagExifFocalLength</span></span>

<span data-ttu-id="b8c96-2161">Lunghezza focale effettiva, in millimetri, della lente.</span><span class="sxs-lookup"><span data-stu-id="b8c96-2161">Actual focal length, in millimeters, of the lens.</span></span> <span data-ttu-id="b8c96-2162">La conversione non viene eseguita alla lunghezza focale di una fotocamera a pellicola 35 millimetri.</span><span class="sxs-lookup"><span data-stu-id="b8c96-2162">Conversion is not made to the focal length of a 35 millimeter film camera.</span></span>



| <span data-ttu-id="b8c96-2163">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-2163">Property info</span></span> | <span data-ttu-id="b8c96-2164">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-2164">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="b8c96-2165">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-2165">Tag</span></span>   | <span data-ttu-id="b8c96-2166">0x920A</span><span class="sxs-lookup"><span data-stu-id="b8c96-2166">0x920A</span></span>                  |
| <span data-ttu-id="b8c96-2167">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-2167">Type</span></span>  | <span data-ttu-id="b8c96-2168">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="b8c96-2168">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="b8c96-2169">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-2169">Count</span></span> | <span data-ttu-id="b8c96-2170">1</span><span class="sxs-lookup"><span data-stu-id="b8c96-2170">1</span></span>                       |



 

## <a name="propertytagexifmakernote"></a><span data-ttu-id="b8c96-2171">PropertyTagExifMakerNote</span><span class="sxs-lookup"><span data-stu-id="b8c96-2171">PropertyTagExifMakerNote</span></span>

<span data-ttu-id="b8c96-2172">Tag di nota.</span><span class="sxs-lookup"><span data-stu-id="b8c96-2172">Note tag.</span></span> <span data-ttu-id="b8c96-2173">Tag utilizzato dai produttori dei writer EXIF per registrare le informazioni.</span><span class="sxs-lookup"><span data-stu-id="b8c96-2173">A tag used by manufacturers of EXIF writers to record information.</span></span> <span data-ttu-id="b8c96-2174">Il contenuto spetta al produttore.</span><span class="sxs-lookup"><span data-stu-id="b8c96-2174">The contents are up to the manufacturer.</span></span>



| <span data-ttu-id="b8c96-2175">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-2175">Property info</span></span> | <span data-ttu-id="b8c96-2176">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-2176">Value</span></span> |
|-------|--------------------------|
| <span data-ttu-id="b8c96-2177">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-2177">Tag</span></span>   | <span data-ttu-id="b8c96-2178">0x927C</span><span class="sxs-lookup"><span data-stu-id="b8c96-2178">0x927C</span></span>                   |
| <span data-ttu-id="b8c96-2179">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-2179">Type</span></span>  | <span data-ttu-id="b8c96-2180">PropertyTagTypeUndefined</span><span class="sxs-lookup"><span data-stu-id="b8c96-2180">PropertyTagTypeUndefined</span></span> |
| <span data-ttu-id="b8c96-2181">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-2181">Count</span></span> | <span data-ttu-id="b8c96-2182">Qualsiasi</span><span class="sxs-lookup"><span data-stu-id="b8c96-2182">Any</span></span>                      |



 

## <a name="propertytagexifusercomment"></a><span data-ttu-id="b8c96-2183">PropertyTagExifUserComment</span><span class="sxs-lookup"><span data-stu-id="b8c96-2183">PropertyTagExifUserComment</span></span>

<span data-ttu-id="b8c96-2184">Tag di commento.</span><span class="sxs-lookup"><span data-stu-id="b8c96-2184">Comment tag.</span></span> <span data-ttu-id="b8c96-2185">Tag utilizzato dagli utenti EXIF per scrivere parole chiave o commenti sull'immagine oltre a quelli presenti in PropertyTagImageDescription e senza le limitazioni del codice carattere del tag PropertyTagImageDescription.</span><span class="sxs-lookup"><span data-stu-id="b8c96-2185">A tag used by EXIF users to write keywords or comments about the image besides those in PropertyTagImageDescription and without the character-code limitations of the PropertyTagImageDescription tag.</span></span>



| <span data-ttu-id="b8c96-2186">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-2186">Property info</span></span> | <span data-ttu-id="b8c96-2187">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-2187">Value</span></span> |
|-------|--------------------------|
| <span data-ttu-id="b8c96-2188">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-2188">Tag</span></span>   | <span data-ttu-id="b8c96-2189">0x9286</span><span class="sxs-lookup"><span data-stu-id="b8c96-2189">0x9286</span></span>                   |
| <span data-ttu-id="b8c96-2190">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-2190">Type</span></span>  | <span data-ttu-id="b8c96-2191">PropertyTagTypeUndefined</span><span class="sxs-lookup"><span data-stu-id="b8c96-2191">PropertyTagTypeUndefined</span></span> |
| <span data-ttu-id="b8c96-2192">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-2192">Count</span></span> | <span data-ttu-id="b8c96-2193">Qualsiasi</span><span class="sxs-lookup"><span data-stu-id="b8c96-2193">Any</span></span>                      |



 

<span data-ttu-id="b8c96-2194">Il codice carattere usato nel tag PropertyTagExifUserComment viene identificato in base a un codice ID in un'area fissa a 8 byte all'inizio dell'area dati del tag.</span><span class="sxs-lookup"><span data-stu-id="b8c96-2194">The character code used in the PropertyTagExifUserComment tag is identified based on an ID code in a fixed 8-byte area at the start of the tag data area.</span></span> <span data-ttu-id="b8c96-2195">La parte inutilizzata dell'area viene riempita con caratteri null (0).</span><span class="sxs-lookup"><span data-stu-id="b8c96-2195">The unused portion of the area is padded with null characters (0).</span></span> <span data-ttu-id="b8c96-2196">I codici ID vengono assegnati per mezzo della registrazione.</span><span class="sxs-lookup"><span data-stu-id="b8c96-2196">ID codes are assigned by means of registration.</span></span> <span data-ttu-id="b8c96-2197">Poiché il tipo non è ASCII, non è necessario usare un carattere di terminazione NULL.</span><span class="sxs-lookup"><span data-stu-id="b8c96-2197">Because the type is not ASCII, it is not necessary to use a NULL terminator.</span></span>

## <a name="propertytagexifdtsubsec"></a><span data-ttu-id="b8c96-2198">PropertyTagExifDTSubsec</span><span class="sxs-lookup"><span data-stu-id="b8c96-2198">PropertyTagExifDTSubsec</span></span>

<span data-ttu-id="b8c96-2199">Stringa di caratteri con terminazione null che specifica una frazione di secondo per il tag PropertyTagDateTime.</span><span class="sxs-lookup"><span data-stu-id="b8c96-2199">Null-terminated character string that specifies a fraction of a second for the PropertyTagDateTime tag.</span></span>



| <span data-ttu-id="b8c96-2200">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-2200">Property info</span></span> | <span data-ttu-id="b8c96-2201">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-2201">Value</span></span> |
|-------|----------------------------------------------------|
| <span data-ttu-id="b8c96-2202">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-2202">Tag</span></span>   | <span data-ttu-id="b8c96-2203">0x9290</span><span class="sxs-lookup"><span data-stu-id="b8c96-2203">0x9290</span></span>                                             |
| <span data-ttu-id="b8c96-2204">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-2204">Type</span></span>  | <span data-ttu-id="b8c96-2205">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="b8c96-2205">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="b8c96-2206">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-2206">Count</span></span> | <span data-ttu-id="b8c96-2207">Lunghezza della stringa che include il carattere di terminazione NULL</span><span class="sxs-lookup"><span data-stu-id="b8c96-2207">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagexifdtorigss"></a><span data-ttu-id="b8c96-2208">PropertyTagExifDTOrigSS</span><span class="sxs-lookup"><span data-stu-id="b8c96-2208">PropertyTagExifDTOrigSS</span></span>

<span data-ttu-id="b8c96-2209">Stringa di caratteri con terminazione null che specifica una frazione di secondo per il tag PropertyTagExifDTOrig.</span><span class="sxs-lookup"><span data-stu-id="b8c96-2209">Null-terminated character string that specifies a fraction of a second for the PropertyTagExifDTOrig tag.</span></span>



| <span data-ttu-id="b8c96-2210">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-2210">Property info</span></span> | <span data-ttu-id="b8c96-2211">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-2211">Value</span></span> |
|------|----------------------------------------------------|
| <span data-ttu-id="b8c96-2212">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-2212">Tag</span></span>  | <span data-ttu-id="b8c96-2213">0x9291</span><span class="sxs-lookup"><span data-stu-id="b8c96-2213">0x9291</span></span>                                             |
| <span data-ttu-id="b8c96-2214">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-2214">Type</span></span> | <span data-ttu-id="b8c96-2215">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="b8c96-2215">PropertyTagTypeASCII</span></span>                               |
| <span data-ttu-id="b8c96-2216">N</span><span class="sxs-lookup"><span data-stu-id="b8c96-2216">N</span></span>    | <span data-ttu-id="b8c96-2217">Lunghezza della stringa che include il carattere di terminazione NULL</span><span class="sxs-lookup"><span data-stu-id="b8c96-2217">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagexifdtdigss"></a><span data-ttu-id="b8c96-2218">PropertyTagExifDTDigSS</span><span class="sxs-lookup"><span data-stu-id="b8c96-2218">PropertyTagExifDTDigSS</span></span>

<span data-ttu-id="b8c96-2219">Stringa di caratteri con terminazione null che specifica una frazione di secondo per il tag PropertyTagExifDTDigitized.</span><span class="sxs-lookup"><span data-stu-id="b8c96-2219">Null-terminated character string that specifies a fraction of a second for the PropertyTagExifDTDigitized tag.</span></span>



| <span data-ttu-id="b8c96-2220">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-2220">Property info</span></span> | <span data-ttu-id="b8c96-2221">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-2221">Value</span></span> |
|------|----------------------------------------------------|
| <span data-ttu-id="b8c96-2222">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-2222">Tag</span></span>  | <span data-ttu-id="b8c96-2223">0x9292</span><span class="sxs-lookup"><span data-stu-id="b8c96-2223">0x9292</span></span>                                             |
| <span data-ttu-id="b8c96-2224">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-2224">Type</span></span> | <span data-ttu-id="b8c96-2225">ASCII</span><span class="sxs-lookup"><span data-stu-id="b8c96-2225">ASCII</span></span>                                              |
| <span data-ttu-id="b8c96-2226">N</span><span class="sxs-lookup"><span data-stu-id="b8c96-2226">N</span></span>    | <span data-ttu-id="b8c96-2227">Lunghezza della stringa che include il carattere di terminazione NULL</span><span class="sxs-lookup"><span data-stu-id="b8c96-2227">Length of the string including the NULL terminator</span></span> |



 

## <a name="propertytagexiffpxver"></a><span data-ttu-id="b8c96-2228">PropertyTagExifFPXVer</span><span class="sxs-lookup"><span data-stu-id="b8c96-2228">PropertyTagExifFPXVer</span></span>

<span data-ttu-id="b8c96-2229">Versione del formato FlashPix supportata da un file FPXR.</span><span class="sxs-lookup"><span data-stu-id="b8c96-2229">FlashPix format version supported by an FPXR file.</span></span> <span data-ttu-id="b8c96-2230">Se la funzione FPXR supporta la versione 1,0 del formato FlashPix, questo è indicato in modo analogo a PropertyTagExifVer registrando 0100 come stringa ASCII a 4 byte.</span><span class="sxs-lookup"><span data-stu-id="b8c96-2230">If the FPXR function supports FlashPix format version 1.0, this is indicated similarly to PropertyTagExifVer by recording 0100 as a 4-byte ASCII string.</span></span> <span data-ttu-id="b8c96-2231">Poiché il tipo è PropertyTagTypeUndefined, non esiste alcun carattere di terminazione NULL.</span><span class="sxs-lookup"><span data-stu-id="b8c96-2231">Because the type is PropertyTagTypeUndefined, there is no NULL terminator.</span></span>



<span data-ttu-id="b8c96-2232">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-2232">Tag</span></span>

<span data-ttu-id="b8c96-2233">0xA000</span><span class="sxs-lookup"><span data-stu-id="b8c96-2233">0xA000</span></span>

<span data-ttu-id="b8c96-2234">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-2234">Type</span></span>

<span data-ttu-id="b8c96-2235">PropertyTagTypeUndefined</span><span class="sxs-lookup"><span data-stu-id="b8c96-2235">PropertyTagTypeUndefined</span></span>

<span data-ttu-id="b8c96-2236">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-2236">Count</span></span>

<span data-ttu-id="b8c96-2237">4</span><span class="sxs-lookup"><span data-stu-id="b8c96-2237">4</span></span>

<span data-ttu-id="b8c96-2238">Predefinito</span><span class="sxs-lookup"><span data-stu-id="b8c96-2238">Default</span></span>

<span data-ttu-id="b8c96-2239">0100</span><span class="sxs-lookup"><span data-stu-id="b8c96-2239">0100</span></span>

<span data-ttu-id="b8c96-2240">0100-FlashPix formato versione 1,0 altro-riservato</span><span class="sxs-lookup"><span data-stu-id="b8c96-2240">0100 - FlashPix format version 1.0 Other - reserved</span></span>



 

## <a name="propertytagexifcolorspace"></a><span data-ttu-id="b8c96-2241">PropertyTagExifColorSpace</span><span class="sxs-lookup"><span data-stu-id="b8c96-2241">PropertyTagExifColorSpace</span></span>

<span data-ttu-id="b8c96-2242">Identificatore dello spazio colori.</span><span class="sxs-lookup"><span data-stu-id="b8c96-2242">Color space specifier.</span></span> <span data-ttu-id="b8c96-2243">Normalmente sRGB (= 1) viene utilizzato per definire lo spazio dei colori in base alle condizioni di monitoraggio del PC e all'ambiente.</span><span class="sxs-lookup"><span data-stu-id="b8c96-2243">Normally sRGB (=1) is used to define the color space based on the PC monitor conditions and environment.</span></span> <span data-ttu-id="b8c96-2244">Se viene utilizzato uno spazio dei colori diverso da sRGB, viene impostato uncalibrato (= 0xFFFF).</span><span class="sxs-lookup"><span data-stu-id="b8c96-2244">If a color space other than sRGB is used, Uncalibrated (=0xFFFF) is set.</span></span> <span data-ttu-id="b8c96-2245">I dati dell'immagine registrati come non calibrati possono essere considerati come sRGB quando vengono convertiti in FlashPix.</span><span class="sxs-lookup"><span data-stu-id="b8c96-2245">Image data recorded as Uncalibrated can be treated as sRGB when it is converted to FlashPix.</span></span>



<span data-ttu-id="b8c96-2246">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-2246">Tag</span></span>

<span data-ttu-id="b8c96-2247">0xA001</span><span class="sxs-lookup"><span data-stu-id="b8c96-2247">0xA001</span></span>

<span data-ttu-id="b8c96-2248">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-2248">Type</span></span>

<span data-ttu-id="b8c96-2249">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="b8c96-2249">PropertyTagTypeShort</span></span>

<span data-ttu-id="b8c96-2250">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-2250">Count</span></span>

<span data-ttu-id="b8c96-2251">1</span><span class="sxs-lookup"><span data-stu-id="b8c96-2251">1</span></span>

<span data-ttu-id="b8c96-2252">0x1-sRGB 0xFFFF-uncalibred other-reserved</span><span class="sxs-lookup"><span data-stu-id="b8c96-2252">0x1 - sRGB 0xFFFF - uncalibrated Other - reserved</span></span>



 

## <a name="propertytagexifpixxdim"></a><span data-ttu-id="b8c96-2253">PropertyTagExifPixXDim</span><span class="sxs-lookup"><span data-stu-id="b8c96-2253">PropertyTagExifPixXDim</span></span>

<span data-ttu-id="b8c96-2254">Informazioni specifiche per i dati compressi.</span><span class="sxs-lookup"><span data-stu-id="b8c96-2254">Information specific to compressed data.</span></span> <span data-ttu-id="b8c96-2255">Quando viene registrato un file compresso, la larghezza valida dell'immagine significativa deve essere registrata in questo tag, indipendentemente dal fatto che siano presenti dati di riempimento o un marcatore di riavvio.</span><span class="sxs-lookup"><span data-stu-id="b8c96-2255">When a compressed file is recorded, the valid width of the meaningful image must be recorded in this tag, whether or not there is padding data or a restart marker.</span></span> <span data-ttu-id="b8c96-2256">Questo tag non deve esistere in un file non compresso.</span><span class="sxs-lookup"><span data-stu-id="b8c96-2256">This tag should not exist in an uncompressed file.</span></span>



| <span data-ttu-id="b8c96-2257">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-2257">Property info</span></span> | <span data-ttu-id="b8c96-2258">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-2258">Value</span></span> |
|-------|---------------------------------------------|
| <span data-ttu-id="b8c96-2259">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-2259">Tag</span></span>   | <span data-ttu-id="b8c96-2260">0xA002</span><span class="sxs-lookup"><span data-stu-id="b8c96-2260">0xA002</span></span>                                      |
| <span data-ttu-id="b8c96-2261">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-2261">Type</span></span>  | <span data-ttu-id="b8c96-2262">PropertyTagTypeShort o PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="b8c96-2262">PropertyTagTypeShort or PropertyTagTypeLong</span></span> |
| <span data-ttu-id="b8c96-2263">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-2263">Count</span></span> | <span data-ttu-id="b8c96-2264">1</span><span class="sxs-lookup"><span data-stu-id="b8c96-2264">1</span></span>                                           |



 

## <a name="propertytagexifpixydim"></a><span data-ttu-id="b8c96-2265">PropertyTagExifPixYDim</span><span class="sxs-lookup"><span data-stu-id="b8c96-2265">PropertyTagExifPixYDim</span></span>

<span data-ttu-id="b8c96-2266">Informazioni specifiche per i dati compressi.</span><span class="sxs-lookup"><span data-stu-id="b8c96-2266">Information specific to compressed data.</span></span> <span data-ttu-id="b8c96-2267">Quando viene registrato un file compresso, l'altezza valida dell'immagine significativa deve essere registrata in questo tag se sono presenti o meno dati di riempimento o un marcatore di riavvio.</span><span class="sxs-lookup"><span data-stu-id="b8c96-2267">When a compressed file is recorded, the valid height of the meaningful image must be recorded in this tag whether or not there is padding data or a restart marker.</span></span> <span data-ttu-id="b8c96-2268">Questo tag non deve esistere in un file non compresso.</span><span class="sxs-lookup"><span data-stu-id="b8c96-2268">This tag should not exist in an uncompressed file.</span></span> <span data-ttu-id="b8c96-2269">Poiché la spaziatura interna dei dati non è necessaria nella direzione verticale, il numero di righe registrate in questo tag di altezza dell'immagine valido sarà identico a quello registrato in SOF.</span><span class="sxs-lookup"><span data-stu-id="b8c96-2269">Because data padding is unnecessary in the vertical direction, the number of lines recorded in this valid image height tag will be the same as that recorded in the SOF.</span></span>



| <span data-ttu-id="b8c96-2270">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-2270">Property info</span></span> | <span data-ttu-id="b8c96-2271">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-2271">Value</span></span> |
|-------|---------------------------------------------|
| <span data-ttu-id="b8c96-2272">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-2272">Tag</span></span>   | <span data-ttu-id="b8c96-2273">0xA003</span><span class="sxs-lookup"><span data-stu-id="b8c96-2273">0xA003</span></span>                                      |
| <span data-ttu-id="b8c96-2274">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-2274">Type</span></span>  | <span data-ttu-id="b8c96-2275">PropertyTagTypeShort o PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="b8c96-2275">PropertyTagTypeShort or PropertyTagTypeLong</span></span> |
| <span data-ttu-id="b8c96-2276">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-2276">Count</span></span> | <span data-ttu-id="b8c96-2277">1</span><span class="sxs-lookup"><span data-stu-id="b8c96-2277">1</span></span>                                           |



 

## <a name="propertytagexifrelatedwav"></a><span data-ttu-id="b8c96-2278">PropertyTagExifRelatedWav</span><span class="sxs-lookup"><span data-stu-id="b8c96-2278">PropertyTagExifRelatedWav</span></span>

<span data-ttu-id="b8c96-2279">Nome di un file audio correlato ai dati dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="b8c96-2279">The name of an audio file related to the image data.</span></span> <span data-ttu-id="b8c96-2280">Le uniche informazioni relazionali registrate sono il nome e l'estensione del file audio EXIF, ovvero una stringa ASCII costituita da 8 caratteri e un punto (.), più 3 caratteri.</span><span class="sxs-lookup"><span data-stu-id="b8c96-2280">The only relational information recorded is the EXIF audio file name and extension (an ASCII string that consists of 8 characters plus a period (.), plus 3 characters).</span></span> <span data-ttu-id="b8c96-2281">Il percorso non viene registrato.</span><span class="sxs-lookup"><span data-stu-id="b8c96-2281">The path is not recorded.</span></span> <span data-ttu-id="b8c96-2282">Quando si usa questo tag, i file audio devono essere registrati in conformità con il formato audio EXIF.</span><span class="sxs-lookup"><span data-stu-id="b8c96-2282">When you use this tag, audio files must be recorded in conformance with the EXIF audio format.</span></span> <span data-ttu-id="b8c96-2283">I writer possono inoltre archiviare dati audio all'interno di APP2 come dati del flusso di estensione FlashPix.</span><span class="sxs-lookup"><span data-stu-id="b8c96-2283">Writers can also store audio data within APP2 as FlashPix extension stream data.</span></span>



| <span data-ttu-id="b8c96-2284">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-2284">Property info</span></span> | <span data-ttu-id="b8c96-2285">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-2285">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="b8c96-2286">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-2286">Tag</span></span>   | <span data-ttu-id="b8c96-2287">0xA004</span><span class="sxs-lookup"><span data-stu-id="b8c96-2287">0xA004</span></span>               |
| <span data-ttu-id="b8c96-2288">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-2288">Type</span></span>  | <span data-ttu-id="b8c96-2289">PropertyTagTypeASCII</span><span class="sxs-lookup"><span data-stu-id="b8c96-2289">PropertyTagTypeASCII</span></span> |
| <span data-ttu-id="b8c96-2290">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-2290">Count</span></span> | <span data-ttu-id="b8c96-2291">13</span><span class="sxs-lookup"><span data-stu-id="b8c96-2291">13</span></span>                   |



 

## <a name="propertytagexifinterop"></a><span data-ttu-id="b8c96-2292">PropertyTagExifInterop</span><span class="sxs-lookup"><span data-stu-id="b8c96-2292">PropertyTagExifInterop</span></span>

<span data-ttu-id="b8c96-2293">Offset a un blocco di elementi di proprietà che contengono informazioni di interoperabilità.</span><span class="sxs-lookup"><span data-stu-id="b8c96-2293">Offset to a block of property items that contain interoperability information.</span></span>



| <span data-ttu-id="b8c96-2294">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-2294">Property info</span></span> | <span data-ttu-id="b8c96-2295">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-2295">Value</span></span> |
|-------|---------------------|
| <span data-ttu-id="b8c96-2296">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-2296">Tag</span></span>   | <span data-ttu-id="b8c96-2297">0xA005</span><span class="sxs-lookup"><span data-stu-id="b8c96-2297">0xA005</span></span>              |
| <span data-ttu-id="b8c96-2298">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-2298">Type</span></span>  | <span data-ttu-id="b8c96-2299">PropertyTagTypeLong</span><span class="sxs-lookup"><span data-stu-id="b8c96-2299">PropertyTagTypeLong</span></span> |
| <span data-ttu-id="b8c96-2300">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-2300">Count</span></span> | <span data-ttu-id="b8c96-2301">1</span><span class="sxs-lookup"><span data-stu-id="b8c96-2301">1</span></span>                   |



 

## <a name="propertytagexifflashenergy"></a><span data-ttu-id="b8c96-2302">PropertyTagExifFlashEnergy</span><span class="sxs-lookup"><span data-stu-id="b8c96-2302">PropertyTagExifFlashEnergy</span></span>

<span data-ttu-id="b8c96-2303">Energia stroboscopica, in secondi di potenza candela (BCPS), nel momento in cui l'immagine è stata acquisita.</span><span class="sxs-lookup"><span data-stu-id="b8c96-2303">Strobe energy, in Beam Candle Power Seconds (BCPS), at the time the image was captured.</span></span>



| <span data-ttu-id="b8c96-2304">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-2304">Property info</span></span> | <span data-ttu-id="b8c96-2305">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-2305">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="b8c96-2306">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-2306">Tag</span></span>   | <span data-ttu-id="b8c96-2307">0xA20B</span><span class="sxs-lookup"><span data-stu-id="b8c96-2307">0xA20B</span></span>                  |
| <span data-ttu-id="b8c96-2308">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-2308">Type</span></span>  | <span data-ttu-id="b8c96-2309">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="b8c96-2309">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="b8c96-2310">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-2310">Count</span></span> | <span data-ttu-id="b8c96-2311">1</span><span class="sxs-lookup"><span data-stu-id="b8c96-2311">1</span></span>                       |



 

## <a name="propertytagexifspatialfr"></a><span data-ttu-id="b8c96-2312">PropertyTagExifSpatialFR</span><span class="sxs-lookup"><span data-stu-id="b8c96-2312">PropertyTagExifSpatialFR</span></span>

<span data-ttu-id="b8c96-2313">La tabella o la frequenza spaziale del dispositivo di input e i valori SFR nella larghezza dell'immagine, nell'altezza dell'immagine e nella direzione diagonale, come specificato in ISO 12233.</span><span class="sxs-lookup"><span data-stu-id="b8c96-2313">Camera or input device spatial frequency table and SFR values in the image width, image height, and diagonal direction, as specified in ISO 12233.</span></span>



| <span data-ttu-id="b8c96-2314">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-2314">Property info</span></span> | <span data-ttu-id="b8c96-2315">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-2315">Value</span></span> |
|-------|--------------------------|
| <span data-ttu-id="b8c96-2316">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-2316">Tag</span></span>   | <span data-ttu-id="b8c96-2317">0xA20C</span><span class="sxs-lookup"><span data-stu-id="b8c96-2317">0xA20C</span></span>                   |
| <span data-ttu-id="b8c96-2318">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-2318">Type</span></span>  | <span data-ttu-id="b8c96-2319">PropertyTagTypeUndefined</span><span class="sxs-lookup"><span data-stu-id="b8c96-2319">PropertyTagTypeUndefined</span></span> |
| <span data-ttu-id="b8c96-2320">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-2320">Count</span></span> | <span data-ttu-id="b8c96-2321">Qualsiasi</span><span class="sxs-lookup"><span data-stu-id="b8c96-2321">Any</span></span>                      |



 

## <a name="propertytagexiffocalxres"></a><span data-ttu-id="b8c96-2322">PropertyTagExifFocalXRes</span><span class="sxs-lookup"><span data-stu-id="b8c96-2322">PropertyTagExifFocalXRes</span></span>

<span data-ttu-id="b8c96-2323">Numero di pixel nella direzione della larghezza dell'immagine (x) per unità sul piano focale della fotocamera.</span><span class="sxs-lookup"><span data-stu-id="b8c96-2323">Number of pixels in the image width (x) direction per unit on the camera focal plane.</span></span> <span data-ttu-id="b8c96-2324">L'unità viene specificata in PropertyTagExifFocalResUnit.</span><span class="sxs-lookup"><span data-stu-id="b8c96-2324">The unit is specified in PropertyTagExifFocalResUnit.</span></span>



| <span data-ttu-id="b8c96-2325">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-2325">Property info</span></span> | <span data-ttu-id="b8c96-2326">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-2326">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="b8c96-2327">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-2327">Tag</span></span>   | <span data-ttu-id="b8c96-2328">0xA20E</span><span class="sxs-lookup"><span data-stu-id="b8c96-2328">0xA20E</span></span>                  |
| <span data-ttu-id="b8c96-2329">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-2329">Type</span></span>  | <span data-ttu-id="b8c96-2330">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="b8c96-2330">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="b8c96-2331">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-2331">Count</span></span> | <span data-ttu-id="b8c96-2332">1</span><span class="sxs-lookup"><span data-stu-id="b8c96-2332">1</span></span>                       |



 

## <a name="propertytagexiffocalyres"></a><span data-ttu-id="b8c96-2333">PropertyTagExifFocalYRes</span><span class="sxs-lookup"><span data-stu-id="b8c96-2333">PropertyTagExifFocalYRes</span></span>

<span data-ttu-id="b8c96-2334">Numero di pixel nella direzione altezza (y) immagine per unità sul piano focale della fotocamera.</span><span class="sxs-lookup"><span data-stu-id="b8c96-2334">Number of pixels in the image height (y) direction per unit on the camera focal plane.</span></span> <span data-ttu-id="b8c96-2335">L'unità viene specificata in PropertyTagExifFocalResUnit.</span><span class="sxs-lookup"><span data-stu-id="b8c96-2335">The unit is specified in PropertyTagExifFocalResUnit.</span></span>



| <span data-ttu-id="b8c96-2336">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-2336">Property info</span></span> | <span data-ttu-id="b8c96-2337">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-2337">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="b8c96-2338">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-2338">Tag</span></span>   | <span data-ttu-id="b8c96-2339">0xA20F</span><span class="sxs-lookup"><span data-stu-id="b8c96-2339">0xA20F</span></span>                  |
| <span data-ttu-id="b8c96-2340">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-2340">Type</span></span>  | <span data-ttu-id="b8c96-2341">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="b8c96-2341">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="b8c96-2342">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-2342">Count</span></span> | <span data-ttu-id="b8c96-2343">1</span><span class="sxs-lookup"><span data-stu-id="b8c96-2343">1</span></span>                       |



 

## <a name="propertytagexiffocalresunit"></a><span data-ttu-id="b8c96-2344">PropertyTagExifFocalResUnit</span><span class="sxs-lookup"><span data-stu-id="b8c96-2344">PropertyTagExifFocalResUnit</span></span>

<span data-ttu-id="b8c96-2345">Unità di misura per PropertyTagExifFocalXRes e PropertyTagExifFocalYRes.</span><span class="sxs-lookup"><span data-stu-id="b8c96-2345">Unit of measure for PropertyTagExifFocalXRes and PropertyTagExifFocalYRes.</span></span>



<span data-ttu-id="b8c96-2346">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-2346">Tag</span></span>

<span data-ttu-id="b8c96-2347">0xA210</span><span class="sxs-lookup"><span data-stu-id="b8c96-2347">0xA210</span></span>

<span data-ttu-id="b8c96-2348">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-2348">Type</span></span>

<span data-ttu-id="b8c96-2349">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="b8c96-2349">PropertyTagTypeShort</span></span>

<span data-ttu-id="b8c96-2350">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-2350">Count</span></span>

<span data-ttu-id="b8c96-2351">1</span><span class="sxs-lookup"><span data-stu-id="b8c96-2351">1</span></span>

<span data-ttu-id="b8c96-2352">2-pollice 3 centimetri</span><span class="sxs-lookup"><span data-stu-id="b8c96-2352">2 - inch 3 - centimeter</span></span>



 

## <a name="propertytagexifsubjectloc"></a><span data-ttu-id="b8c96-2353">PropertyTagExifSubjectLoc</span><span class="sxs-lookup"><span data-stu-id="b8c96-2353">PropertyTagExifSubjectLoc</span></span>

<span data-ttu-id="b8c96-2354">Posizione dell'oggetto principale nella scena.</span><span class="sxs-lookup"><span data-stu-id="b8c96-2354">Location of the main subject in the scene.</span></span> <span data-ttu-id="b8c96-2355">Il valore di questo tag rappresenta il pixel al centro dell'oggetto principale relativo al bordo sinistro.</span><span class="sxs-lookup"><span data-stu-id="b8c96-2355">The value of this tag represents the pixel at the center of the main subject relative to the left edge.</span></span> <span data-ttu-id="b8c96-2356">Il primo valore indica il numero di colonna e il secondo valore indica il numero di riga.</span><span class="sxs-lookup"><span data-stu-id="b8c96-2356">The first value indicates the column number, and the second value indicates the row number.</span></span>



| <span data-ttu-id="b8c96-2357">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-2357">Property info</span></span> | <span data-ttu-id="b8c96-2358">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-2358">Value</span></span> |
|-------|----------------------|
| <span data-ttu-id="b8c96-2359">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-2359">Tag</span></span>   | <span data-ttu-id="b8c96-2360">0xA214</span><span class="sxs-lookup"><span data-stu-id="b8c96-2360">0xA214</span></span>               |
| <span data-ttu-id="b8c96-2361">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-2361">Type</span></span>  | <span data-ttu-id="b8c96-2362">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="b8c96-2362">PropertyTagTypeShort</span></span> |
| <span data-ttu-id="b8c96-2363">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-2363">Count</span></span> | <span data-ttu-id="b8c96-2364">2</span><span class="sxs-lookup"><span data-stu-id="b8c96-2364">2</span></span>                    |



 

## <a name="propertytagexifexposureindex"></a><span data-ttu-id="b8c96-2365">PropertyTagExifExposureIndex</span><span class="sxs-lookup"><span data-stu-id="b8c96-2365">PropertyTagExifExposureIndex</span></span>

<span data-ttu-id="b8c96-2366">Indice di esposizione selezionato nella fotocamera o nel dispositivo di input nel momento in cui l'immagine è stata acquisita.</span><span class="sxs-lookup"><span data-stu-id="b8c96-2366">Exposure index selected on the camera or input device at the time the image was captured.</span></span>



| <span data-ttu-id="b8c96-2367">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-2367">Property info</span></span> | <span data-ttu-id="b8c96-2368">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-2368">Value</span></span> |
|-------|-------------------------|
| <span data-ttu-id="b8c96-2369">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-2369">Tag</span></span>   | <span data-ttu-id="b8c96-2370">0xA215</span><span class="sxs-lookup"><span data-stu-id="b8c96-2370">0xA215</span></span>                  |
| <span data-ttu-id="b8c96-2371">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-2371">Type</span></span>  | <span data-ttu-id="b8c96-2372">PropertyTagTypeRational</span><span class="sxs-lookup"><span data-stu-id="b8c96-2372">PropertyTagTypeRational</span></span> |
| <span data-ttu-id="b8c96-2373">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-2373">Count</span></span> | <span data-ttu-id="b8c96-2374">1</span><span class="sxs-lookup"><span data-stu-id="b8c96-2374">1</span></span>                       |



 

## <a name="propertytagexifsensingmethod"></a><span data-ttu-id="b8c96-2375">PropertyTagExifSensingMethod</span><span class="sxs-lookup"><span data-stu-id="b8c96-2375">PropertyTagExifSensingMethod</span></span>

<span data-ttu-id="b8c96-2376">Tipo di sensore immagine nella fotocamera o nel dispositivo di input.</span><span class="sxs-lookup"><span data-stu-id="b8c96-2376">Image sensor type on the camera or input device.</span></span>



<span data-ttu-id="b8c96-2377">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-2377">Tag</span></span>

<span data-ttu-id="b8c96-2378">0xA217</span><span class="sxs-lookup"><span data-stu-id="b8c96-2378">0xA217</span></span>

<span data-ttu-id="b8c96-2379">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-2379">Type</span></span>

<span data-ttu-id="b8c96-2380">PropertyTagTypeShort</span><span class="sxs-lookup"><span data-stu-id="b8c96-2380">PropertyTagTypeShort</span></span>

<span data-ttu-id="b8c96-2381">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-2381">Count</span></span>

<span data-ttu-id="b8c96-2382">1</span><span class="sxs-lookup"><span data-stu-id="b8c96-2382">1</span></span>

<span data-ttu-id="b8c96-2383">1-non definito 2-un sensore area colori a un chip 3-sensore area colore a due chip 4-sensore area colori a tre chip 5-colore sensore area di colore 7-sensore trilineario 8-sensore lineare sequenziale altro-riservato</span><span class="sxs-lookup"><span data-stu-id="b8c96-2383">1 - not defined 2 - one-chip color area sensor 3 - two-chip color area sensor 4 - three-chip color area sensor 5 - color sequential area sensor 7 - trilinear sensor 8 - color sequential linear sensor Other - reserved</span></span>



 

## <a name="propertytagexiffilesource"></a><span data-ttu-id="b8c96-2384">PropertyTagExifFileSource</span><span class="sxs-lookup"><span data-stu-id="b8c96-2384">PropertyTagExifFileSource</span></span>

<span data-ttu-id="b8c96-2385">Origine dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="b8c96-2385">The image source.</span></span> <span data-ttu-id="b8c96-2386">Se un DSC ha registrato l'immagine, il valore di questo tag è 3.</span><span class="sxs-lookup"><span data-stu-id="b8c96-2386">If a DSC recorded the image, the value of this tag is 3.</span></span>



| <span data-ttu-id="b8c96-2387">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-2387">Property info</span></span> | <span data-ttu-id="b8c96-2388">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-2388">Value</span></span> |
|-------|--------------------------|
| <span data-ttu-id="b8c96-2389">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-2389">Tag</span></span>   | <span data-ttu-id="b8c96-2390">0xA300</span><span class="sxs-lookup"><span data-stu-id="b8c96-2390">0xA300</span></span>                   |
| <span data-ttu-id="b8c96-2391">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-2391">Type</span></span>  | <span data-ttu-id="b8c96-2392">PropertyTagTypeUndefined</span><span class="sxs-lookup"><span data-stu-id="b8c96-2392">PropertyTagTypeUndefined</span></span> |
| <span data-ttu-id="b8c96-2393">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-2393">Count</span></span> | <span data-ttu-id="b8c96-2394">1</span><span class="sxs-lookup"><span data-stu-id="b8c96-2394">1</span></span>                        |



 

## <a name="propertytagexifscenetype"></a><span data-ttu-id="b8c96-2395">PropertyTagExifSceneType</span><span class="sxs-lookup"><span data-stu-id="b8c96-2395">PropertyTagExifSceneType</span></span>

<span data-ttu-id="b8c96-2396">Tipo di scena.</span><span class="sxs-lookup"><span data-stu-id="b8c96-2396">The type of scene.</span></span> <span data-ttu-id="b8c96-2397">Se un DSC ha registrato l'immagine, il valore del tag deve essere impostato su 1, a indicare che l'immagine è stata fotografata direttamente.</span><span class="sxs-lookup"><span data-stu-id="b8c96-2397">If a DSC recorded the image, the value of this tag must be set to 1, indicating that the image was directly photographed.</span></span>



| <span data-ttu-id="b8c96-2398">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-2398">Property info</span></span> | <span data-ttu-id="b8c96-2399">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-2399">Value</span></span> |
|-------|--------------------------|
| <span data-ttu-id="b8c96-2400">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-2400">Tag</span></span>   | <span data-ttu-id="b8c96-2401">0xA301</span><span class="sxs-lookup"><span data-stu-id="b8c96-2401">0xA301</span></span>                   |
| <span data-ttu-id="b8c96-2402">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-2402">Type</span></span>  | <span data-ttu-id="b8c96-2403">PropertyTagTypeUndefined</span><span class="sxs-lookup"><span data-stu-id="b8c96-2403">PropertyTagTypeUndefined</span></span> |
| <span data-ttu-id="b8c96-2404">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-2404">Count</span></span> | <span data-ttu-id="b8c96-2405">1</span><span class="sxs-lookup"><span data-stu-id="b8c96-2405">1</span></span>                        |



 

## <a name="propertytagexifcfapattern"></a><span data-ttu-id="b8c96-2406">PropertyTagExifCfaPattern</span><span class="sxs-lookup"><span data-stu-id="b8c96-2406">PropertyTagExifCfaPattern</span></span>

<span data-ttu-id="b8c96-2407">Modello geometrico della matrice di filtri colori (CFA) del sensore di immagine quando viene usato un sensore di area colore a un chip.</span><span class="sxs-lookup"><span data-stu-id="b8c96-2407">The color filter array (CFA) geometric pattern of the image sensor when a one-chip color area sensor is used.</span></span> <span data-ttu-id="b8c96-2408">Non si applica a tutti i metodi di rilevamento.</span><span class="sxs-lookup"><span data-stu-id="b8c96-2408">It does not apply to all sensing methods.</span></span>



| <span data-ttu-id="b8c96-2409">Informazioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="b8c96-2409">Property info</span></span> | <span data-ttu-id="b8c96-2410">Valore</span><span class="sxs-lookup"><span data-stu-id="b8c96-2410">Value</span></span> |
|-------|--------------------------|
| <span data-ttu-id="b8c96-2411">Tag</span><span class="sxs-lookup"><span data-stu-id="b8c96-2411">Tag</span></span>   | <span data-ttu-id="b8c96-2412">0xA302</span><span class="sxs-lookup"><span data-stu-id="b8c96-2412">0xA302</span></span>                   |
| <span data-ttu-id="b8c96-2413">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8c96-2413">Type</span></span>  | <span data-ttu-id="b8c96-2414">PropertyTagTypeUndefined</span><span class="sxs-lookup"><span data-stu-id="b8c96-2414">PropertyTagTypeUndefined</span></span> |
| <span data-ttu-id="b8c96-2415">Conteggio</span><span class="sxs-lookup"><span data-stu-id="b8c96-2415">Count</span></span> | <span data-ttu-id="b8c96-2416">Qualsiasi</span><span class="sxs-lookup"><span data-stu-id="b8c96-2416">Any</span></span>                      |



 

## <a name="related-topics"></a><span data-ttu-id="b8c96-2417">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b8c96-2417">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b8c96-2418">Specifiche di formato dei file di immagine</span><span class="sxs-lookup"><span data-stu-id="b8c96-2418">Image File Format Specifications</span></span>](-gdiplus-constant-image-file-format-specifications.md)
</dt> <dt>

[<span data-ttu-id="b8c96-2419">Costanti Tag proprietà immagine</span><span class="sxs-lookup"><span data-stu-id="b8c96-2419">Image Property Tag Constants</span></span>](-gdiplus-constant-image-property-tag-constants.md)
</dt> <dt>

[<span data-ttu-id="b8c96-2420">**Costanti del tipo di tag della proprietà Image**</span><span class="sxs-lookup"><span data-stu-id="b8c96-2420">**Image Property Tag Type Constants**</span></span>](-gdiplus-constant-image-property-tag-type-constants.md)
</dt> <dt>

[<span data-ttu-id="b8c96-2421">Tag di proprietà in ordine alfabetico</span><span class="sxs-lookup"><span data-stu-id="b8c96-2421">Property Tags in Alphabetical Order</span></span>](-gdiplus-constant-property-tags-in-alphabetical-order.md)
</dt> <dt>

[<span data-ttu-id="b8c96-2422">Tag di proprietà in ordine numerico</span><span class="sxs-lookup"><span data-stu-id="b8c96-2422">Property Tags in Numerical Order</span></span>](-gdiplus-constant-property-tags-in-numerical-order.md)
</dt> <dt>

[<span data-ttu-id="b8c96-2423">Lettura e scrittura di metadati</span><span class="sxs-lookup"><span data-stu-id="b8c96-2423">Reading and Writing Metadata</span></span>](-gdiplus-reading-and-writing-metadata-use.md)
</dt> </dl>

 

 



