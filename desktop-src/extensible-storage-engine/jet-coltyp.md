---
description: 'Altre informazioni su: JET_COLTYP'
title: JET_COLTYP
TOCTitle: JET_COLTYP
ms:assetid: 2c30c025-629d-4b94-bcb9-9c8fc3d4e039
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269213(v=EXCHG.10)
ms:contentKeyID: 32765516
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 04588d6a057c25c0d39e42997a67a611fdfd92d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884709"
---
# <a name="jet_coltyp"></a><span data-ttu-id="ec1a8-103">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="ec1a8-103">JET_COLTYP</span></span>


<span data-ttu-id="ec1a8-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="ec1a8-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_coltyp"></a><span data-ttu-id="ec1a8-105">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="ec1a8-105">JET_COLTYP</span></span>

<span data-ttu-id="ec1a8-106">Il gruppo **JET_COLTYP** di costanti descrive tutti i possibili tipi di colonna che è possibile trovare in una tabella.</span><span class="sxs-lookup"><span data-stu-id="ec1a8-106">The **JET_COLTYP** group of constants describe all possible column types that can be found in a table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ec1a8-107">Costante/valore</span><span class="sxs-lookup"><span data-stu-id="ec1a8-107">Constant/value</span></span></p></th>
<th><p><span data-ttu-id="ec1a8-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ec1a8-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ec1a8-109">JET_coltypNil</span><span class="sxs-lookup"><span data-stu-id="ec1a8-109">JET_coltypNil</span></span><br />
<span data-ttu-id="ec1a8-110">0</span><span class="sxs-lookup"><span data-stu-id="ec1a8-110">0</span></span></p></td>
<td><p><span data-ttu-id="ec1a8-111">Tipo di colonna non valido.</span><span class="sxs-lookup"><span data-stu-id="ec1a8-111">An invalid column type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec1a8-112">JET_coltypBit</span><span class="sxs-lookup"><span data-stu-id="ec1a8-112">JET_coltypBit</span></span><br />
<span data-ttu-id="ec1a8-113">1</span><span class="sxs-lookup"><span data-stu-id="ec1a8-113">1</span></span></p></td>
<td><p><span data-ttu-id="ec1a8-114">Tipo di colonna che consente tre valori: <strong>true</strong>, <strong>false</strong>o <strong>null</strong>.</span><span class="sxs-lookup"><span data-stu-id="ec1a8-114">A column type that allows three values: <strong>True</strong>, <strong>False</strong>, or <strong>NULL</strong>.</span></span> <span data-ttu-id="ec1a8-115">Questo tipo di colonna ha una lunghezza di un byte e è di dimensioni fisse.</span><span class="sxs-lookup"><span data-stu-id="ec1a8-115">This type of column is one byte in length and is a fixed size.</span></span> <span data-ttu-id="ec1a8-116"><strong>False</strong> Ordina prima di <strong>true</strong>.</span><span class="sxs-lookup"><span data-stu-id="ec1a8-116"><strong>False</strong> sorts before <strong>True</strong>.</span></span> <span data-ttu-id="ec1a8-117">Si noti che la dimensione di questo tipo non corrisponde alla dimensione del tipo Boolean Variant.</span><span class="sxs-lookup"><span data-stu-id="ec1a8-117">Note that the size of this type does not match the size of the variant Boolean type.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec1a8-118">JET_coltypUnsignedByte</span><span class="sxs-lookup"><span data-stu-id="ec1a8-118">JET_coltypUnsignedByte</span></span><br />
<span data-ttu-id="ec1a8-119">2</span><span class="sxs-lookup"><span data-stu-id="ec1a8-119">2</span></span></p></td>
<td><p><span data-ttu-id="ec1a8-120">Unsigned Integer a 1 byte che può assumere valori compresi tra 0 (zero) e 255.</span><span class="sxs-lookup"><span data-stu-id="ec1a8-120">A 1-byte unsigned integer that can take on values between 0 (zero) and 255.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec1a8-121">JET_coltypShort</span><span class="sxs-lookup"><span data-stu-id="ec1a8-121">JET_coltypShort</span></span><br />
<span data-ttu-id="ec1a8-122">3</span><span class="sxs-lookup"><span data-stu-id="ec1a8-122">3</span></span></p></td>
<td><p><span data-ttu-id="ec1a8-123">Intero con segno a 2 byte che può assumere valori compresi tra-32768 e 32767.</span><span class="sxs-lookup"><span data-stu-id="ec1a8-123">A 2-byte signed integer that can take on values between -32768 and 32767.</span></span> <span data-ttu-id="ec1a8-124">I valori negativi vengono ordinati prima dei valori positivi.</span><span class="sxs-lookup"><span data-stu-id="ec1a8-124">Negative values sort before positive values.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec1a8-125">JET_coltypLong</span><span class="sxs-lookup"><span data-stu-id="ec1a8-125">JET_coltypLong</span></span><br />
<span data-ttu-id="ec1a8-126">4</span><span class="sxs-lookup"><span data-stu-id="ec1a8-126">4</span></span></p></td>
<td><p><span data-ttu-id="ec1a8-127">Intero con segno a 4 byte che può assumere valori compresi tra-2147483648 e 2147483647.</span><span class="sxs-lookup"><span data-stu-id="ec1a8-127">A 4-byte signed integer that can take on values between - 2147483648 and 2147483647.</span></span> <span data-ttu-id="ec1a8-128">I valori negativi vengono ordinati prima dei valori positivi.</span><span class="sxs-lookup"><span data-stu-id="ec1a8-128">Negative values sort before positive values.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec1a8-129">JET_coltypCurrency</span><span class="sxs-lookup"><span data-stu-id="ec1a8-129">JET_coltypCurrency</span></span><br />
<span data-ttu-id="ec1a8-130">5</span><span class="sxs-lookup"><span data-stu-id="ec1a8-130">5</span></span></p></td>
<td><p><span data-ttu-id="ec1a8-131">Intero con segno a 8 byte che può assumere valori compresi tra-9.223.372.036.854.775.808 e 9223372036854775807.</span><span class="sxs-lookup"><span data-stu-id="ec1a8-131">An 8-byte signed integer that can take on values between - 9223372036854775808 and 9223372036854775807.</span></span> <span data-ttu-id="ec1a8-132">I valori negativi vengono ordinati prima dei valori positivi.</span><span class="sxs-lookup"><span data-stu-id="ec1a8-132">Negative values sort before positive values.</span></span> <span data-ttu-id="ec1a8-133">Questo tipo di colonna è identico al tipo di valuta Variant.</span><span class="sxs-lookup"><span data-stu-id="ec1a8-133">This column type is identical to the variant currency type.</span></span> <span data-ttu-id="ec1a8-134">Questo tipo di colonna può essere utilizzato anche come intero con segno a 8 byte nativo.</span><span class="sxs-lookup"><span data-stu-id="ec1a8-134">This column type can also be used as a native 8-byte signed integer.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec1a8-135">JET_coltypIEEESingle</span><span class="sxs-lookup"><span data-stu-id="ec1a8-135">JET_coltypIEEESingle</span></span><br />
<span data-ttu-id="ec1a8-136">6</span><span class="sxs-lookup"><span data-stu-id="ec1a8-136">6</span></span></p></td>
<td><p><span data-ttu-id="ec1a8-137">Numero a virgola mobile A precisione singola (4 byte).</span><span class="sxs-lookup"><span data-stu-id="ec1a8-137">A single-precision (4-byte) floating point number.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec1a8-138">JET_coltypIEEEDouble</span><span class="sxs-lookup"><span data-stu-id="ec1a8-138">JET_coltypIEEEDouble</span></span><br />
<span data-ttu-id="ec1a8-139">7</span><span class="sxs-lookup"><span data-stu-id="ec1a8-139">7</span></span></p></td>
<td><p><span data-ttu-id="ec1a8-140">Numero a virgola mobile a precisione doppia (8 byte).</span><span class="sxs-lookup"><span data-stu-id="ec1a8-140">A double-precision (8-byte) floating point number.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec1a8-141">JET_coltypDateTime</span><span class="sxs-lookup"><span data-stu-id="ec1a8-141">JET_coltypDateTime</span></span><br />
<span data-ttu-id="ec1a8-142">8</span><span class="sxs-lookup"><span data-stu-id="ec1a8-142">8</span></span></p></td>
<td><p><span data-ttu-id="ec1a8-143">Numero a virgola mobile a precisione doppia (8 byte) che rappresenta una data in giorni frazionari dall'anno 1900.</span><span class="sxs-lookup"><span data-stu-id="ec1a8-143">A double-precision (8-byte) floating point number that represents a date in fractional days since the year 1900.</span></span> <span data-ttu-id="ec1a8-144">Questo tipo di colonna è identico al tipo di data Variant.</span><span class="sxs-lookup"><span data-stu-id="ec1a8-144">This column type is identical to the variant date type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec1a8-145">JET_coltypBinary</span><span class="sxs-lookup"><span data-stu-id="ec1a8-145">JET_coltypBinary</span></span><br />
<span data-ttu-id="ec1a8-146">9</span><span class="sxs-lookup"><span data-stu-id="ec1a8-146">9</span></span></p></td>
<td><p><span data-ttu-id="ec1a8-147">Una colonna binaria non elaborata a lunghezza fissa o variabile che può avere una lunghezza fino a 255 byte.</span><span class="sxs-lookup"><span data-stu-id="ec1a8-147">A fixed or variable length, raw binary column that can be up to 255 bytes in length.</span></span></p>
<p><span data-ttu-id="ec1a8-148">Questo tipo di colonna può essere utilizzato per implementare un GUID se configurato come colonna binaria a 16 byte a lunghezza fissa.</span><span class="sxs-lookup"><span data-stu-id="ec1a8-148">This column type can be used to implement a GUID if configured as a fixed length, 16-byte binary column.</span></span> <span data-ttu-id="ec1a8-149">L'unica avvertenza è che l'ordinamento relativo dei valori in un indice su tale colonna non corrisponderà all'ordinamento relativo del rendering della stringa del registro di sistema standard di un GUID (ovvero &quot; {0d6cec99-3f3f-4dc7-a5e6-f87aefeb908b} &quot; ).</span><span class="sxs-lookup"><span data-stu-id="ec1a8-149">The only caveat is that the relative ordering of values in an index over such a column will not match the relative ordering of the standard registry-string rendering of a GUID (that is &quot;{ 0d6cec99-3f3f-4dc7-a5e6-f87aefeb908b}&quot;).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec1a8-150">JET_coltypText</span><span class="sxs-lookup"><span data-stu-id="ec1a8-150">JET_coltypText</span></span><br />
<span data-ttu-id="ec1a8-151">10</span><span class="sxs-lookup"><span data-stu-id="ec1a8-151">10</span></span></p></td>
<td><p><span data-ttu-id="ec1a8-152">Una colonna di testo a lunghezza fissa o variabile che può avere una lunghezza fino a 255 caratteri ASCII o 127 caratteri Unicode.</span><span class="sxs-lookup"><span data-stu-id="ec1a8-152">A fixed or variable length text column that can be up to 255 ASCII characters in length or 127 Unicode characters in length.</span></span></p>
<p><span data-ttu-id="ec1a8-153">Tutte le stringhe vengono archiviate come numero conteggiato di caratteri.</span><span class="sxs-lookup"><span data-stu-id="ec1a8-153">All strings are stored as a counted number of characters.</span></span> <span data-ttu-id="ec1a8-154">Non è necessario terminare con null le stringhe.</span><span class="sxs-lookup"><span data-stu-id="ec1a8-154">The strings need not be null terminated.</span></span> <span data-ttu-id="ec1a8-155">Non è inoltre necessario che il conteggio includa un carattere di terminazione null.</span><span class="sxs-lookup"><span data-stu-id="ec1a8-155">Further, it is not necessary for the count to include a null terminator.</span></span> <span data-ttu-id="ec1a8-156">Infine, è possibile archiviare i caratteri null incorporati.</span><span class="sxs-lookup"><span data-stu-id="ec1a8-156">Finally, embedded null characters can be stored.</span></span></p>
<p><span data-ttu-id="ec1a8-157">Le stringhe ASCII vengono sempre considerate senza distinzione tra maiuscole e minuscole per scopi di ordinamento e ricerca.</span><span class="sxs-lookup"><span data-stu-id="ec1a8-157">ASCII strings are always treated as case insensitive for sorting and searching purposes.</span></span> <span data-ttu-id="ec1a8-158">Inoltre, per l'ordinamento e la ricerca vengono considerati solo i caratteri che precedono il primo carattere null (se presente).</span><span class="sxs-lookup"><span data-stu-id="ec1a8-158">Further, only the characters preceding the first null character (if any) are considered for sorting and searching.</span></span></p>
<p><span data-ttu-id="ec1a8-159">Le stringhe Unicode utilizzano l'API Win32 <a href="/windows/win32/api/winnls/nf-winnls-lcmapstringa">LCMapString</a> per creare chiavi di ordinamento che vengono successivamente utilizzate per l'ordinamento e la ricerca di tali dati.</span><span class="sxs-lookup"><span data-stu-id="ec1a8-159">Unicode strings use the Win32 API <a href="/windows/win32/api/winnls/nf-winnls-lcmapstringa">LCMapString</a> to create sort keys that are subsequently used for sorting and searching that data.</span></span> <span data-ttu-id="ec1a8-160">Per impostazione predefinita, le stringhe Unicode sono considerate nelle impostazioni locali per l'inglese (Stati Uniti) e vengono ordinate e cercate usando i flag di normalizzazione seguenti: NORM_IGNORECASE, NORM_IGNOREKANATYPE e NORM_IGNOREWIDTH.</span><span class="sxs-lookup"><span data-stu-id="ec1a8-160">By default, Unicode strings are considered to be in the U.S. English locale and are sorted and searched using the following normalization flags: NORM_IGNORECASE, NORM_IGNOREKANATYPE, and NORM_IGNOREWIDTH.</span></span> <span data-ttu-id="ec1a8-161">In Windows 2000 è possibile personalizzare questi flag per ogni indice in modo da includere anche NORM_IGNORENONSPACE.</span><span class="sxs-lookup"><span data-stu-id="ec1a8-161">In Windows 2000, it is possible to customize these flags per index to also include NORM_IGNORENONSPACE.</span></span> <span data-ttu-id="ec1a8-162">In Windows XP e versioni successive, è possibile richiedere qualsiasi combinazione dei seguenti flag di normalizzazione per indice: LCMAP_SORTKEY, LCMAP_BYTEREV, NORM_IGNORECASE, NORM_IGNORENONSPACE, NORM_IGNORESYMBOLS, NORM_IGNOREKANATYPE, NORM_IGNOREWIDTH e SORT_STRINGSORT.</span><span class="sxs-lookup"><span data-stu-id="ec1a8-162">In Windows XP and later releases, it is possible to request any combination of the following normalization flags per index: LCMAP_SORTKEY, LCMAP_BYTEREV, NORM_IGNORECASE, NORM_IGNORENONSPACE, NORM_IGNORESYMBOLS, NORM_IGNOREKANATYPE, NORM_IGNOREWIDTH, and SORT_STRINGSORT.</span></span></p>
<p><span data-ttu-id="ec1a8-163">In tutte le versioni, è possibile personalizzare le impostazioni locali per ogni indice.</span><span class="sxs-lookup"><span data-stu-id="ec1a8-163">In all releases, it is possible to customize the locale per index.</span></span> <span data-ttu-id="ec1a8-164">Le impostazioni locali possono essere usate purché nel computer sia installato il Language Pack appropriato.</span><span class="sxs-lookup"><span data-stu-id="ec1a8-164">Any locale may be used as long as the appropriate language pack has been installed on the machine.</span></span> <span data-ttu-id="ec1a8-165">Infine, tutti i caratteri null rilevati in una stringa Unicode vengono completamente ignorati.</span><span class="sxs-lookup"><span data-stu-id="ec1a8-165">Finally, any null characters encountered in a Unicode string are completely ignored.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec1a8-166">JET_coltypLongBinary</span><span class="sxs-lookup"><span data-stu-id="ec1a8-166">JET_coltypLongBinary</span></span><br />
<span data-ttu-id="ec1a8-167">11</span><span class="sxs-lookup"><span data-stu-id="ec1a8-167">11</span></span></p></td>
<td><p><span data-ttu-id="ec1a8-168">Una colonna binaria non elaborata a lunghezza fissa o variabile che può avere una lunghezza fino a 2147483647 byte.</span><span class="sxs-lookup"><span data-stu-id="ec1a8-168">A fixed or variable length, raw binary column that can be up to 2147483647 bytes in length.</span></span> <span data-ttu-id="ec1a8-169">Questo tipo è considerato un valore Long.</span><span class="sxs-lookup"><span data-stu-id="ec1a8-169">This type is considered to be a Long Value.</span></span> <span data-ttu-id="ec1a8-170">Un valore Long è speciale perché può essere di grandi dimensioni e perché può essere accessibile come flusso.</span><span class="sxs-lookup"><span data-stu-id="ec1a8-170">A Long Value is special because it can be large and because it can be accessed as a stream.</span></span> <span data-ttu-id="ec1a8-171">Questo tipo è altrimenti identico a JET_coltypBinary.</span><span class="sxs-lookup"><span data-stu-id="ec1a8-171">This type is otherwise identical to JET_coltypBinary.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec1a8-172">JET_coltypLongText</span><span class="sxs-lookup"><span data-stu-id="ec1a8-172">JET_coltypLongText</span></span><br />
<span data-ttu-id="ec1a8-173">12</span><span class="sxs-lookup"><span data-stu-id="ec1a8-173">12</span></span></p></td>
<td><p><span data-ttu-id="ec1a8-174">Lunghezza fissa o variabile, colonna di testo che può contenere fino a 2147483647 caratteri ASCII di lunghezza o 1073741823 caratteri Unicode di lunghezza.</span><span class="sxs-lookup"><span data-stu-id="ec1a8-174">A fixed or variable length, text column that can be up to 2147483647 ASCII characters in length or 1073741823 Unicode characters in length.</span></span> <span data-ttu-id="ec1a8-175">Questo tipo è considerato un valore Long.</span><span class="sxs-lookup"><span data-stu-id="ec1a8-175">This type is considered to be a Long Value.</span></span> <span data-ttu-id="ec1a8-176">Un valore Long è speciale perché può essere di grandi dimensioni e perché può essere accessibile come flusso.</span><span class="sxs-lookup"><span data-stu-id="ec1a8-176">A Long Value is special because it can be large and because it can be accessed as a stream.</span></span> <span data-ttu-id="ec1a8-177">Questo tipo è altrimenti identico a JET_coltypText.</span><span class="sxs-lookup"><span data-stu-id="ec1a8-177">This type is otherwise identical to JET_coltypText.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec1a8-178">JET_coltypSLV</span><span class="sxs-lookup"><span data-stu-id="ec1a8-178">JET_coltypSLV</span></span><br />
<span data-ttu-id="ec1a8-179">13</span><span class="sxs-lookup"><span data-stu-id="ec1a8-179">13</span></span></p></td>
<td><p><span data-ttu-id="ec1a8-180">Questo tipo di colonna è obsoleto.</span><span class="sxs-lookup"><span data-stu-id="ec1a8-180">This column type is obsolete.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec1a8-181">JET_coltypUnsignedLong</span><span class="sxs-lookup"><span data-stu-id="ec1a8-181">JET_coltypUnsignedLong</span></span><br />
<span data-ttu-id="ec1a8-182">14</span><span class="sxs-lookup"><span data-stu-id="ec1a8-182">14</span></span></p></td>
<td><p><span data-ttu-id="ec1a8-183">Unsigned Integer a 4 byte che può assumere valori compresi tra 0 (zero) e 4294967295.</span><span class="sxs-lookup"><span data-stu-id="ec1a8-183">A 4-byte unsigned integer that can take on values between 0 (zero) and 4294967295.</span></span></p>
<p><span data-ttu-id="ec1a8-184"><strong>Windows Vista e Windows Server 2008:</strong>  Questo tipo di colonna è supportato in Windows Vista, Windows Server 2008 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="ec1a8-184"><strong>Windows Vista and Windows Server 2008:</strong>  This column type is supported on Windows Vista, Windows Server 2008 and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec1a8-185">JET_coltypLongLong</span><span class="sxs-lookup"><span data-stu-id="ec1a8-185">JET_coltypLongLong</span></span><br />
<span data-ttu-id="ec1a8-186">15</span><span class="sxs-lookup"><span data-stu-id="ec1a8-186">15</span></span></p></td>
<td><p><span data-ttu-id="ec1a8-187">Intero con segno a 8 byte che può assumere valori compresi tra-9.223.372.036.854.775.808 e 9223372036854775807.</span><span class="sxs-lookup"><span data-stu-id="ec1a8-187">An 8-byte signed integer that can take on values between - 9223372036854775808 and 9223372036854775807.</span></span> <span data-ttu-id="ec1a8-188">I valori negativi vengono ordinati prima dei valori positivi.</span><span class="sxs-lookup"><span data-stu-id="ec1a8-188">Negative values sort before positive values.</span></span></p>
<p><span data-ttu-id="ec1a8-189"><strong>Windows Vista e Windows Server 2008:</strong>  Questo tipo di colonna è supportato in Windows Vista, Windows Server 2008 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="ec1a8-189"><strong>Windows Vista and Windows Server 2008:</strong>  This column type is supported on Windows Vista, Windows Server 2008 and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec1a8-190">JET_coltypGUID</span><span class="sxs-lookup"><span data-stu-id="ec1a8-190">JET_coltypGUID</span></span><br />
<span data-ttu-id="ec1a8-191">16</span><span class="sxs-lookup"><span data-stu-id="ec1a8-191">16</span></span></p></td>
<td><p><span data-ttu-id="ec1a8-192">Una colonna binaria A 16 byte A lunghezza fissa che rappresenta in modo nativo il tipo di dati GUID.</span><span class="sxs-lookup"><span data-stu-id="ec1a8-192">A fixed length 16 byte binary column that natively represents the GUID data type.</span></span> <span data-ttu-id="ec1a8-193">I valori della colonna GUID vengono ordinati nello stesso modo in cui tali valori verrebbero ordinati come stringhe nel formato standard (ad esempio {4999b5c0-7657-42D9-BDC1-4b779784e013}).</span><span class="sxs-lookup"><span data-stu-id="ec1a8-193">GUID column values sort in the same way that those values would sort as strings when in standard form (i.e. {4999b5c0-7657-42d9-bdc1-4b779784e013}).</span></span></p>
<p><span data-ttu-id="ec1a8-194"><strong>Windows Vista e Windows Server 2008:</strong>  Questo tipo di colonna è supportato in Windows Vista, Windows Server 2008 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="ec1a8-194"><strong>Windows Vista and Windows Server 2008:</strong>  This column type is supported on Windows Vista, Windows Server 2008 and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec1a8-195">JET_coltypUnsignedShort</span><span class="sxs-lookup"><span data-stu-id="ec1a8-195">JET_coltypUnsignedShort</span></span><br />
<span data-ttu-id="ec1a8-196">17</span><span class="sxs-lookup"><span data-stu-id="ec1a8-196">17</span></span></p></td>
<td><p><span data-ttu-id="ec1a8-197">Unsigned Integer a 2 byte che può assumere valori compresi tra 0 e 65535.</span><span class="sxs-lookup"><span data-stu-id="ec1a8-197">A 2-byte unsigned integer that can take on values between 0 and 65535.</span></span></p>
<p><span data-ttu-id="ec1a8-198"><strong>Windows Vista e Windows Server 2008:</strong>  Questo tipo di colonna è supportato in Windows Vista, Windows Server 2008 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="ec1a8-198"><strong>Windows Vista and Windows Server 2008:</strong>  This column type is supported on Windows Vista, Windows Server 2008 and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec1a8-199">JET_coltypMax</span><span class="sxs-lookup"><span data-stu-id="ec1a8-199">JET_coltypMax</span></span><br />
<span data-ttu-id="ec1a8-200">18</span><span class="sxs-lookup"><span data-stu-id="ec1a8-200">18</span></span></p></td>
<td><p><span data-ttu-id="ec1a8-201">Costante che descrive il tipo di colonna massimo, ovvero uno oltre il valore valido più grande, supportato dal motore.</span><span class="sxs-lookup"><span data-stu-id="ec1a8-201">A constant describing the maximum (that is, one beyond the largest valid) column type supported by the engine.</span></span></p>
<p><span data-ttu-id="ec1a8-202">Questo valore deve essere utilizzato con cautela perché verrà modificato quando sono supportati i nuovi tipi di colonna.</span><span class="sxs-lookup"><span data-stu-id="ec1a8-202">This value should be used with care because it will change as new column types are supported.</span></span> <span data-ttu-id="ec1a8-203">Ad esempio, ha un valore letterale diverso in Windows 2000 rispetto a Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="ec1a8-203">For example, it has a different literal value on Windows 2000 than it does on Windows XP and later releases.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="ec1a8-204">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ec1a8-204">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ec1a8-205"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="ec1a8-205"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="ec1a8-206">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="ec1a8-206">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec1a8-207"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="ec1a8-207"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="ec1a8-208">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="ec1a8-208">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec1a8-209"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="ec1a8-209"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="ec1a8-210">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="ec1a8-210">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="ec1a8-211">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="ec1a8-211">See Also</span></span>

[<span data-ttu-id="ec1a8-212">JetAddColumn</span><span class="sxs-lookup"><span data-stu-id="ec1a8-212">JetAddColumn</span></span>](./jetaddcolumn-function.md)  
[<span data-ttu-id="ec1a8-213">JetCreateTableColumnIndex</span><span class="sxs-lookup"><span data-stu-id="ec1a8-213">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)
