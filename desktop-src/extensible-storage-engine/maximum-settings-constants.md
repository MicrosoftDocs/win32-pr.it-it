---
description: 'Altre informazioni su: costanti impostazioni massime'
title: Costanti di impostazioni massime
TOCTitle: Maximum Settings Constants
ms:assetid: 1111051f-55af-4c33-be38-6a3973c2c815
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269189(v=EXCHG.10)
ms:contentKeyID: 32765492
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
ms.openlocfilehash: 3754732e59c9a90c74366558d9904fc13376db7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879534"
---
# <a name="maximum-settings-constants"></a><span data-ttu-id="40f37-103">Costanti di impostazioni massime</span><span class="sxs-lookup"><span data-stu-id="40f37-103">Maximum Settings Constants</span></span>


<span data-ttu-id="40f37-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="40f37-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="maximum-settings-constants"></a><span data-ttu-id="40f37-105">Costanti di impostazioni massime</span><span class="sxs-lookup"><span data-stu-id="40f37-105">Maximum Settings Constants</span></span>

<span data-ttu-id="40f37-106">Queste costanti forniscono le impostazioni massime consentite per gli elementi di un database ESE.</span><span class="sxs-lookup"><span data-stu-id="40f37-106">These constants provide the maximum settings that are allowed on items in an ESE database.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="40f37-107">Costante/valore</span><span class="sxs-lookup"><span data-stu-id="40f37-107">Constant/value</span></span></p></th>
<th><p><span data-ttu-id="40f37-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="40f37-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="40f37-109">JET_BASE_NAME_LENGTH</span><span class="sxs-lookup"><span data-stu-id="40f37-109">JET_BASE_NAME_LENGTH</span></span><br />
<span data-ttu-id="40f37-110">3</span><span class="sxs-lookup"><span data-stu-id="40f37-110">3</span></span></p></td>
<td><p><span data-ttu-id="40f37-111">Imposta la lunghezza per il prefisso utilizzato per denominare i file utilizzati dal motore di database.</span><span class="sxs-lookup"><span data-stu-id="40f37-111">Sets the length for the prefix used to name files that are used by the database engine.</span></span> <span data-ttu-id="40f37-112">Questa lunghezza è applicabile al nome impostato per il parametro di sistema <a href="gg269235(v=exchg.10).md">JET_paramBaseName</a> .</span><span class="sxs-lookup"><span data-stu-id="40f37-112">This length is applicable to the name set for the <a href="gg269235(v=exchg.10).md">JET_paramBaseName</a> system parameter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f37-113">JET_MAX_COMPUTERNAME_LENGTH</span><span class="sxs-lookup"><span data-stu-id="40f37-113">JET_MAX_COMPUTERNAME_LENGTH</span></span><br />
<span data-ttu-id="40f37-114">15</span><span class="sxs-lookup"><span data-stu-id="40f37-114">15</span></span></p></td>
<td><p><span data-ttu-id="40f37-115">Imposta la lunghezza massima per <a href="gg269340(v=exchg.10).md">JET_SIGNATURE</a>.</span><span class="sxs-lookup"><span data-stu-id="40f37-115">Sets the maximum length for <a href="gg269340(v=exchg.10).md">JET_SIGNATURE</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f37-116">JET_cbBookmarkMost</span><span class="sxs-lookup"><span data-stu-id="40f37-116">JET_cbBookmarkMost</span></span><br />
<span data-ttu-id="40f37-117">256</span><span class="sxs-lookup"><span data-stu-id="40f37-117">256</span></span></p></td>
<td><p><span data-ttu-id="40f37-118">Dimensioni massime predefinite di un segnalibro.</span><span class="sxs-lookup"><span data-stu-id="40f37-118">The default maximum size of a bookmark.</span></span> <span data-ttu-id="40f37-119">Questo valore è valido quando la dimensione della chiave viene lasciata sul valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="40f37-119">This is valid when the key size is left at its default value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f37-120">JET_cbBookmarkMostMost</span><span class="sxs-lookup"><span data-stu-id="40f37-120">JET_cbBookmarkMostMost</span></span><br />
<span data-ttu-id="40f37-121">2000</span><span class="sxs-lookup"><span data-stu-id="40f37-121">2000</span></span></p></td>
<td><p><span data-ttu-id="40f37-122">Dimensione massima di un segnalibro quando ESENT è configurato in modo da avere le chiavi maggiori possibili.</span><span class="sxs-lookup"><span data-stu-id="40f37-122">The maximum size of a bookmark when esent is configured to have the largest keys possible.</span></span></p>
<p><span data-ttu-id="40f37-123"><strong>Windows 7:</strong> JET_cbBookmarkMostMost è stato introdotto in Windows 7.</span><span class="sxs-lookup"><span data-stu-id="40f37-123"><strong>Windows 7:</strong> JET_cbBookmarkMostMost is introduced in Windows 7.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f37-124">JET_cbNameMost</span><span class="sxs-lookup"><span data-stu-id="40f37-124">JET_cbNameMost</span></span><br />
<span data-ttu-id="40f37-125">64</span><span class="sxs-lookup"><span data-stu-id="40f37-125">64</span></span></p></td>
<td><p><span data-ttu-id="40f37-126">Lunghezza massima di un oggetto, una colonna, un indice o un nome di proprietà.</span><span class="sxs-lookup"><span data-stu-id="40f37-126">The maximum length of a object, column, index, or property name.</span></span></p>
<p><span data-ttu-id="40f37-127"><strong>Nota</strong>  Se Unicode, il valore è 128.</span><span class="sxs-lookup"><span data-stu-id="40f37-127"><strong>Note</strong>  If Unicode, the value is 128.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f37-128">JET_cbFullNameMost</span><span class="sxs-lookup"><span data-stu-id="40f37-128">JET_cbFullNameMost</span></span><br />
<span data-ttu-id="40f37-129">255</span><span class="sxs-lookup"><span data-stu-id="40f37-129">255</span></span></p></td>
<td><p><span data-ttu-id="40f37-130">Lunghezza massima di un &quot; costrutto Name.Name.Name.... &quot;</span><span class="sxs-lookup"><span data-stu-id="40f37-130">The maximum length of a &quot;name.name.name...&quot; construct.</span></span></p>
<p><span data-ttu-id="40f37-131"><strong>Nota</strong>  Se Unicode, il valore è 510.</span><span class="sxs-lookup"><span data-stu-id="40f37-131"><strong>Note</strong>  If Unicode, the value is 510.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f37-132">JET_cbColumnLVPageOverhead</span><span class="sxs-lookup"><span data-stu-id="40f37-132">JET_cbColumnLVPageOverhead</span></span><br />
<span data-ttu-id="40f37-133">82</span><span class="sxs-lookup"><span data-stu-id="40f37-133">82</span></span></p></td>
<td><p><span data-ttu-id="40f37-134">Questo numero può essere utilizzato per calcolare la quantità massima di un BLOB che può essere archiviato dal motore di database in una singola pagina di database.</span><span class="sxs-lookup"><span data-stu-id="40f37-134">This number can be used to compute the maximum amount of a BLOB that can be stored by the database engine on a single database page.</span></span> <span data-ttu-id="40f37-135">La formula è max size = JET_paramDatabasePageSize-JET_cbColumnLVPageOverhead.</span><span class="sxs-lookup"><span data-stu-id="40f37-135">The formula is max size = JET_paramDatabasePageSize–JET_cbColumnLVPageOverhead.</span></span></p>
<p><span data-ttu-id="40f37-136">Questo valore è ora obsoleto.</span><span class="sxs-lookup"><span data-stu-id="40f37-136">This value is now obsolete.</span></span> <span data-ttu-id="40f37-137">È necessario recuperare le dimensioni del blocco con valore Long con il parametro JET_paramLVChunkSizeMost.</span><span class="sxs-lookup"><span data-stu-id="40f37-137">The long-value chunk size should be retrieved with the JET_paramLVChunkSizeMost parameter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f37-138">JET_cbColumnMost</span><span class="sxs-lookup"><span data-stu-id="40f37-138">JET_cbColumnMost</span></span><br />
<span data-ttu-id="40f37-139">255</span><span class="sxs-lookup"><span data-stu-id="40f37-139">255</span></span></p></td>
<td><p><span data-ttu-id="40f37-140">Dimensione massima dei dati della colonna non di valori Long.</span><span class="sxs-lookup"><span data-stu-id="40f37-140">The maximum size of non-long-value column data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f37-141">JET_cbLVDefaultValueMost</span><span class="sxs-lookup"><span data-stu-id="40f37-141">JET_cbLVDefaultValueMost</span></span><br />
<span data-ttu-id="40f37-142">255</span><span class="sxs-lookup"><span data-stu-id="40f37-142">255</span></span></p></td>
<td><p><span data-ttu-id="40f37-143">Dimensione massima di un valore predefinito della colonna con valore Long (LongBinary o LongText).</span><span class="sxs-lookup"><span data-stu-id="40f37-143">The maximum size of a long-value (LongBinary or LongText) column default value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f37-144">JET_cbKeyMost</span><span class="sxs-lookup"><span data-stu-id="40f37-144">JET_cbKeyMost</span></span><br />
<span data-ttu-id="40f37-145">255</span><span class="sxs-lookup"><span data-stu-id="40f37-145">255</span></span></p></td>
<td><p><span data-ttu-id="40f37-146">Dimensioni massime predefinite di una chiave di ordinamento o di indice.</span><span class="sxs-lookup"><span data-stu-id="40f37-146">The default maximum size of a sort or index key.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f37-147">JET_cbKeyMostMost</span><span class="sxs-lookup"><span data-stu-id="40f37-147">JET_cbKeyMostMost</span></span><br />
<span data-ttu-id="40f37-148">2000</span><span class="sxs-lookup"><span data-stu-id="40f37-148">2000</span></span></p></td>
<td><p><span data-ttu-id="40f37-149">Dimensioni massime configurabili di una chiave di ordinamento o di indice per qualsiasi dimensione di pagina.</span><span class="sxs-lookup"><span data-stu-id="40f37-149">The maximum configurable size of a sort or index key for any page size.</span></span> <span data-ttu-id="40f37-150">(Vedere JET_INDEXCREATE2. cbKeyMost)</span><span class="sxs-lookup"><span data-stu-id="40f37-150">(See JET_INDEXCREATE2.cbKeyMost)</span></span></p>
<p><span data-ttu-id="40f37-151"><strong>Windows 7:</strong> JET_cbKeyMostMost è stato introdotto nel sistema operativo Windows 7.</span><span class="sxs-lookup"><span data-stu-id="40f37-151"><strong>Windows 7:</strong> JET_cbKeyMostMost is introduced in the Windows 7 operating system.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f37-152">JET_cbKeyMost2KBytePage</span><span class="sxs-lookup"><span data-stu-id="40f37-152">JET_cbKeyMost2KBytePage</span></span><br />
<span data-ttu-id="40f37-153">500</span><span class="sxs-lookup"><span data-stu-id="40f37-153">500</span></span></p></td>
<td><p><span data-ttu-id="40f37-154">Dimensioni massime consentite configurabili per una chiave di indice in un database che utilizza pagine a 2048 byte.</span><span class="sxs-lookup"><span data-stu-id="40f37-154">The maximum allowable maximum configurable size for an index key in a database using 2048 byte pages.</span></span> <span data-ttu-id="40f37-155">Per ulteriori informazioni, vedere <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> .</span><span class="sxs-lookup"><span data-stu-id="40f37-155">See <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> for more information.</span></span></p>
<p><span data-ttu-id="40f37-156"><strong>Windows Vista:</strong> JET_cbKeyMost2KBytePage è stato introdotto nel sistema operativo Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="40f37-156"><strong>Windows Vista:</strong> JET_cbKeyMost2KBytePage is introduced in the Windows Vista operating system.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f37-157">JET_cbKeyMost4KBytePage</span><span class="sxs-lookup"><span data-stu-id="40f37-157">JET_cbKeyMost4KBytePage</span></span><br />
<span data-ttu-id="40f37-158">1000</span><span class="sxs-lookup"><span data-stu-id="40f37-158">1000</span></span></p></td>
<td><p><span data-ttu-id="40f37-159">Dimensioni massime consentite configurabili per una chiave di indice in un database che utilizza pagine a 4096 byte.</span><span class="sxs-lookup"><span data-stu-id="40f37-159">The maximum allowable maximum configurable size for an index key in a database using 4096 byte pages.</span></span> <span data-ttu-id="40f37-160">Per ulteriori informazioni, vedere <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> .</span><span class="sxs-lookup"><span data-stu-id="40f37-160">See <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> for more information.</span></span></p>
<p><span data-ttu-id="40f37-161"><strong>Windows Vista:</strong> JET_cbKeyMost4KBytePage è stato introdotto in Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="40f37-161"><strong>Windows Vista:</strong> JET_cbKeyMost4KBytePage is introduced in Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f37-162">JET_cbKeyMost8KBytePage</span><span class="sxs-lookup"><span data-stu-id="40f37-162">JET_cbKeyMost8KBytePage</span></span><br />
<span data-ttu-id="40f37-163">2000</span><span class="sxs-lookup"><span data-stu-id="40f37-163">2000</span></span></p></td>
<td><p><span data-ttu-id="40f37-164">Dimensioni massime consentite configurabili per una chiave di indice in un database che utilizza pagine a 8192 byte.</span><span class="sxs-lookup"><span data-stu-id="40f37-164">The maximum allowable maximum configurable size for an index key in a database using 8192 byte pages.</span></span> <span data-ttu-id="40f37-165">Per ulteriori informazioni, vedere <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> .</span><span class="sxs-lookup"><span data-stu-id="40f37-165">See <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> for more information.</span></span></p>
<p><span data-ttu-id="40f37-166"><strong>Windows Vista:  </strong> JET_cbKeyMost8KBytePage è stato introdotto in Windows Vista</span><span class="sxs-lookup"><span data-stu-id="40f37-166"><strong>Windows Vista:  </strong>JET_cbKeyMost8KBytePage is introduced in Windows Vista</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f37-167">JET_cbKeyMostMin</span><span class="sxs-lookup"><span data-stu-id="40f37-167">JET_cbKeyMostMin</span></span><br />
<span data-ttu-id="40f37-168">255</span><span class="sxs-lookup"><span data-stu-id="40f37-168">255</span></span></p></td>
<td><p><span data-ttu-id="40f37-169">Dimensioni massime consentite minime per una chiave di indice.</span><span class="sxs-lookup"><span data-stu-id="40f37-169">The minimum allowable maximum size for an index key.</span></span> <span data-ttu-id="40f37-170">Per ulteriori informazioni, vedere <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> .</span><span class="sxs-lookup"><span data-stu-id="40f37-170">See <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> for more information.</span></span></p>
<p><span data-ttu-id="40f37-171"><strong>Windows Vista:  </strong> JET_cbKeyMostMin è stato introdotto in Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="40f37-171"><strong>Windows Vista:  </strong>JET_cbKeyMostMin is introduced in Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f37-172">JET_cbLimitKeyMost</span><span class="sxs-lookup"><span data-stu-id="40f37-172">JET_cbLimitKeyMost</span></span><br />
<span data-ttu-id="40f37-173">256</span><span class="sxs-lookup"><span data-stu-id="40f37-173">256</span></span></p></td>
<td><p><span data-ttu-id="40f37-174">Dimensione massima della chiave quando la chiave viene formata usando un limite <em>grbit</em>, ad esempio JET_bitStrLimit, che viene usato nella funzione <a href="gg269329(v=exchg.10).md">JetMakeKey</a> .</span><span class="sxs-lookup"><span data-stu-id="40f37-174">The maximum key size when the key is formed by using a limit <em>grbit</em>, such as JET_bitStrLimit, which is used in the <a href="gg269329(v=exchg.10).md">JetMakeKey</a> function.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f37-175">JET_cbPrimaryKeyMost</span><span class="sxs-lookup"><span data-stu-id="40f37-175">JET_cbPrimaryKeyMost</span></span><br />
<span data-ttu-id="40f37-176">255</span><span class="sxs-lookup"><span data-stu-id="40f37-176">255</span></span></p></td>
<td><p><span data-ttu-id="40f37-177">Dimensione massima dell'indice primario.</span><span class="sxs-lookup"><span data-stu-id="40f37-177">The maximum size of the primary index.</span></span> <span data-ttu-id="40f37-178">Questa operazione è ora obsoleta.</span><span class="sxs-lookup"><span data-stu-id="40f37-178">This is now obsolete.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f37-179">JET_cbSecondaryKeyMost</span><span class="sxs-lookup"><span data-stu-id="40f37-179">JET_cbSecondaryKeyMost</span></span><br />
<span data-ttu-id="40f37-180">255</span><span class="sxs-lookup"><span data-stu-id="40f37-180">255</span></span></p></td>
<td><p><span data-ttu-id="40f37-181">Dimensione massima dell'indice secondario.</span><span class="sxs-lookup"><span data-stu-id="40f37-181">The maximum size of the secondary index.</span></span> <span data-ttu-id="40f37-182">Questa operazione è ora obsoleta.</span><span class="sxs-lookup"><span data-stu-id="40f37-182">This is now obsolete.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f37-183">JET_ccolKeyMost</span><span class="sxs-lookup"><span data-stu-id="40f37-183">JET_ccolKeyMost</span></span><br />
<span data-ttu-id="40f37-184">12</span><span class="sxs-lookup"><span data-stu-id="40f37-184">12</span></span></p></td>
<td><p><span data-ttu-id="40f37-185">Numero massimo di componenti in una chiave di ordinamento o di indice.</span><span class="sxs-lookup"><span data-stu-id="40f37-185">The maximum number of components in a sort or index key.</span></span></p>
<p><span data-ttu-id="40f37-186"><strong>Windows Vista:  </strong> In Windows Vista e nelle versioni successive di Windows il valore è 16.</span><span class="sxs-lookup"><span data-stu-id="40f37-186"><strong>Windows Vista:  </strong>In Windows Vista and later versions of Windows the value is 16.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f37-187">JET_ccolMost</span><span class="sxs-lookup"><span data-stu-id="40f37-187">JET_ccolMost</span></span><br />
<span data-ttu-id="40f37-188">0x0000fee0</span><span class="sxs-lookup"><span data-stu-id="40f37-188">0x0000fee0</span></span></p></td>
<td><p><span data-ttu-id="40f37-189">Numero massimo di colonne consentite in una tabella.</span><span class="sxs-lookup"><span data-stu-id="40f37-189">The maximum number of columns allowed in a table.</span></span></p>
<p><span data-ttu-id="40f37-190"><strong>Windows XP:  </strong> Il valore 0x0000fee0 viene utilizzato in Windows XP e versioni successive e successive di Windows</span><span class="sxs-lookup"><span data-stu-id="40f37-190"><strong>Windows XP:  </strong>The value 0x0000fee0 is used in Windows XP and later and later versions of Windows</span></span></p>
<p><span data-ttu-id="40f37-191"><strong>Windows 2000:  </strong> Il valore 0x00007ffe viene usato in Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="40f37-191"><strong>Windows 2000:  </strong>The value 0x00007ffe is used in Windows 2000.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f37-192">JET_ccolFixedMost</span><span class="sxs-lookup"><span data-stu-id="40f37-192">JET_ccolFixedMost</span></span><br />
<span data-ttu-id="40f37-193">0x0000007F</span><span class="sxs-lookup"><span data-stu-id="40f37-193">0x0000007f</span></span></p></td>
<td><p><span data-ttu-id="40f37-194">Numero massimo di colonne fisse consentite in una tabella, attualmente 127.</span><span class="sxs-lookup"><span data-stu-id="40f37-194">The maximum number of fixed columns allowed in a table, currently 127.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f37-195">JET_ccolVarMost</span><span class="sxs-lookup"><span data-stu-id="40f37-195">JET_ccolVarMost</span></span><br />
<span data-ttu-id="40f37-196">0x00000080</span><span class="sxs-lookup"><span data-stu-id="40f37-196">0x00000080</span></span></p></td>
<td><p><span data-ttu-id="40f37-197">Numero massimo di colonne a lunghezza variabile che possono essere contenute in una tabella, attualmente 128.</span><span class="sxs-lookup"><span data-stu-id="40f37-197">The maximum number of variable-length columns that can be contained in a table, currently 128.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f37-198">JET_ccolTaggedMost</span><span class="sxs-lookup"><span data-stu-id="40f37-198">JET_ccolTaggedMost</span></span><br />
<span data-ttu-id="40f37-199">(JET_ccolMost-0x000000FF)</span><span class="sxs-lookup"><span data-stu-id="40f37-199">( JET_ccolMost - 0x000000ff )</span></span></p></td>
<td><p><span data-ttu-id="40f37-200">Numero massimo di colonne con tag che possono essere contenute in una tabella, attualmente 64993.</span><span class="sxs-lookup"><span data-stu-id="40f37-200">The maximum number of tagged columns that can be contained in a table, currently 64993.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="40f37-201">Requisiti</span><span class="sxs-lookup"><span data-stu-id="40f37-201">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="40f37-202"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="40f37-202"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="40f37-203">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="40f37-203">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40f37-204"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="40f37-204"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="40f37-205">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="40f37-205">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40f37-206"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="40f37-206"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="40f37-207">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="40f37-207">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>

