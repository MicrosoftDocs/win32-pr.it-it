---
description: La tabella RegLocator include le informazioni necessarie per cercare un file o una directory usando il registro di sistema o per cercare una particolare voce del registro di sistema. Questa tabella contiene le colonne seguenti.
ms.assetid: dc88b083-cc1d-46d7-9be8-29ebbf3767a0
title: Tabella RegLocator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db5084b8c6fd8d10372759bdba65abbb4dfe7261
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311702"
---
# <a name="reglocator-table"></a><span data-ttu-id="542fb-104">Tabella RegLocator</span><span class="sxs-lookup"><span data-stu-id="542fb-104">RegLocator Table</span></span>

<span data-ttu-id="542fb-105">La tabella RegLocator include le informazioni necessarie per cercare un file o una directory usando il registro di sistema o per cercare una particolare voce del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="542fb-105">The RegLocator table holds the information needed to search for a file or directory using the registry, or to search for a particular registry entry itself.</span></span> <span data-ttu-id="542fb-106">Questa tabella contiene le colonne seguenti.</span><span class="sxs-lookup"><span data-stu-id="542fb-106">This table has the following columns.</span></span>



| <span data-ttu-id="542fb-107">Colonna</span><span class="sxs-lookup"><span data-stu-id="542fb-107">Column</span></span>      | <span data-ttu-id="542fb-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="542fb-108">Type</span></span>                         | <span data-ttu-id="542fb-109">Chiave</span><span class="sxs-lookup"><span data-stu-id="542fb-109">Key</span></span> | <span data-ttu-id="542fb-110">Nullable</span><span class="sxs-lookup"><span data-stu-id="542fb-110">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="542fb-111">Firma\_</span><span class="sxs-lookup"><span data-stu-id="542fb-111">Signature\_</span></span> | [<span data-ttu-id="542fb-112">Identificatore</span><span class="sxs-lookup"><span data-stu-id="542fb-112">Identifier</span></span>](identifier.md) | <span data-ttu-id="542fb-113">S</span><span class="sxs-lookup"><span data-stu-id="542fb-113">Y</span></span>   | <span data-ttu-id="542fb-114">N</span><span class="sxs-lookup"><span data-stu-id="542fb-114">N</span></span>        |
| <span data-ttu-id="542fb-115">Radice</span><span class="sxs-lookup"><span data-stu-id="542fb-115">Root</span></span>        | [<span data-ttu-id="542fb-116">Integer</span><span class="sxs-lookup"><span data-stu-id="542fb-116">Integer</span></span>](integer.md)       | <span data-ttu-id="542fb-117">N</span><span class="sxs-lookup"><span data-stu-id="542fb-117">N</span></span>   | <span data-ttu-id="542fb-118">N</span><span class="sxs-lookup"><span data-stu-id="542fb-118">N</span></span>        |
| <span data-ttu-id="542fb-119">Chiave</span><span class="sxs-lookup"><span data-stu-id="542fb-119">Key</span></span>         | [<span data-ttu-id="542fb-120">RegPath</span><span class="sxs-lookup"><span data-stu-id="542fb-120">RegPath</span></span>](regpath.md)       | <span data-ttu-id="542fb-121">N</span><span class="sxs-lookup"><span data-stu-id="542fb-121">N</span></span>   | <span data-ttu-id="542fb-122">N</span><span class="sxs-lookup"><span data-stu-id="542fb-122">N</span></span>        |
| <span data-ttu-id="542fb-123">Nome</span><span class="sxs-lookup"><span data-stu-id="542fb-123">Name</span></span>        | [<span data-ttu-id="542fb-124">Formattato</span><span class="sxs-lookup"><span data-stu-id="542fb-124">Formatted</span></span>](formatted.md)   | <span data-ttu-id="542fb-125">N</span><span class="sxs-lookup"><span data-stu-id="542fb-125">N</span></span>   | <span data-ttu-id="542fb-126">Y</span><span class="sxs-lookup"><span data-stu-id="542fb-126">Y</span></span>        |
| <span data-ttu-id="542fb-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="542fb-127">Type</span></span>        | [<span data-ttu-id="542fb-128">Integer</span><span class="sxs-lookup"><span data-stu-id="542fb-128">Integer</span></span>](integer.md)       | <span data-ttu-id="542fb-129">N</span><span class="sxs-lookup"><span data-stu-id="542fb-129">N</span></span>   | <span data-ttu-id="542fb-130">S</span><span class="sxs-lookup"><span data-stu-id="542fb-130">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="542fb-131">Colonne</span><span class="sxs-lookup"><span data-stu-id="542fb-131">Columns</span></span>

<dl> <dt>

<span data-ttu-id="542fb-132"><span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Firma\_</span><span class="sxs-lookup"><span data-stu-id="542fb-132"><span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Signature\_</span></span>
</dt> <dd>

<span data-ttu-id="542fb-133">Il valore nel campo firma \_ rappresenta una firma univoca che è una chiave esterna nella colonna uno della tabella della [firma](signature-table.md) .</span><span class="sxs-lookup"><span data-stu-id="542fb-133">The value in the Signature\_ field represents a unique signature that is an external key into column one of the [Signature](signature-table.md) table.</span></span> <span data-ttu-id="542fb-134">Se la firma è presente nella tabella della firma, la ricerca è relativa a un file.</span><span class="sxs-lookup"><span data-stu-id="542fb-134">If this signature is present in the Signature table, the search is for a file.</span></span> <span data-ttu-id="542fb-135">Se la firma non è presente nella tabella della firma e il valore della colonna del tipo è **msidbLocatorTypeRawValue**, la ricerca è relativa al nome della chiave del registro di sistema a cui punta la tabella RegLocator.</span><span class="sxs-lookup"><span data-stu-id="542fb-135">If this signature is absent from the Signature table, and the value of the Type column is **msidbLocatorTypeRawValue**, the search is for the registry key name pointed to by the RegLocator table.</span></span> <span data-ttu-id="542fb-136">In caso contrario, la ricerca è relativa a una directory a cui fa riferimento la tabella RegLocator.</span><span class="sxs-lookup"><span data-stu-id="542fb-136">Otherwise the search is for a directory pointed to by the RegLocator table.</span></span>

</dd> <dt>

<span data-ttu-id="542fb-137"><span id="Root"></span><span id="root"></span><span id="ROOT"></span>Radice</span><span class="sxs-lookup"><span data-stu-id="542fb-137"><span id="Root"></span><span id="root"></span><span id="ROOT"></span>Root</span></span>
</dt> <dd>

<span data-ttu-id="542fb-138">Chiave radice predefinita per il valore del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="542fb-138">The predefined root key for the registry value.</span></span>



| <span data-ttu-id="542fb-139">Costante</span><span class="sxs-lookup"><span data-stu-id="542fb-139">Constant</span></span>                          | <span data-ttu-id="542fb-140">Valore esadecimale</span><span class="sxs-lookup"><span data-stu-id="542fb-140">Hexadecimal</span></span> | <span data-ttu-id="542fb-141">Decimal</span><span class="sxs-lookup"><span data-stu-id="542fb-141">Decimal</span></span> | <span data-ttu-id="542fb-142">Chiave radice</span><span class="sxs-lookup"><span data-stu-id="542fb-142">Root key</span></span>             |
|-----------------------------------|-------------|---------|----------------------|
| <span data-ttu-id="542fb-143">**msidbRegistryRootClassesRoot**</span><span class="sxs-lookup"><span data-stu-id="542fb-143">**msidbRegistryRootClassesRoot**</span></span>  | <span data-ttu-id="542fb-144">0x000</span><span class="sxs-lookup"><span data-stu-id="542fb-144">0x000</span></span>       | <span data-ttu-id="542fb-145">0</span><span class="sxs-lookup"><span data-stu-id="542fb-145">0</span></span>       | <span data-ttu-id="542fb-146">HKEY\_CLASSI\_RADICE</span><span class="sxs-lookup"><span data-stu-id="542fb-146">HKEY\_CLASSES\_ROOT</span></span>  |
| <span data-ttu-id="542fb-147">**msidbRegistryRootCurrentUser**</span><span class="sxs-lookup"><span data-stu-id="542fb-147">**msidbRegistryRootCurrentUser**</span></span>  | <span data-ttu-id="542fb-148">0x001</span><span class="sxs-lookup"><span data-stu-id="542fb-148">0x001</span></span>       | <span data-ttu-id="542fb-149">1</span><span class="sxs-lookup"><span data-stu-id="542fb-149">1</span></span>       | <span data-ttu-id="542fb-150">HKEY\_CORRENTE\_UTENTE</span><span class="sxs-lookup"><span data-stu-id="542fb-150">HKEY\_CURRENT\_USER</span></span>  |
| <span data-ttu-id="542fb-151">**msidbRegistryRootLocalMachine**</span><span class="sxs-lookup"><span data-stu-id="542fb-151">**msidbRegistryRootLocalMachine**</span></span> | <span data-ttu-id="542fb-152">0x002</span><span class="sxs-lookup"><span data-stu-id="542fb-152">0x002</span></span>       | <span data-ttu-id="542fb-153">2</span><span class="sxs-lookup"><span data-stu-id="542fb-153">2</span></span>       | <span data-ttu-id="542fb-154">HKEY\_LOCALE\_MACCHINA</span><span class="sxs-lookup"><span data-stu-id="542fb-154">HKEY\_LOCAL\_MACHINE</span></span> |
| <span data-ttu-id="542fb-155">**msidbRegistryRootUsers**</span><span class="sxs-lookup"><span data-stu-id="542fb-155">**msidbRegistryRootUsers**</span></span>        | <span data-ttu-id="542fb-156">0x003</span><span class="sxs-lookup"><span data-stu-id="542fb-156">0x003</span></span>       | <span data-ttu-id="542fb-157">3</span><span class="sxs-lookup"><span data-stu-id="542fb-157">3</span></span>       | <span data-ttu-id="542fb-158">HKEY\_UTENTI</span><span class="sxs-lookup"><span data-stu-id="542fb-158">HKEY\_USERS</span></span>          |



 

</dd> <dt>

<span data-ttu-id="542fb-159"><span id="Key"></span><span id="key"></span><span id="KEY"></span>Chiave</span><span class="sxs-lookup"><span data-stu-id="542fb-159"><span id="Key"></span><span id="key"></span><span id="KEY"></span>Key</span></span>
</dt> <dd>

<span data-ttu-id="542fb-160">Chiave per il valore del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="542fb-160">The key for the registry value.</span></span>

</dd> <dt>

<span data-ttu-id="542fb-161"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Nome</span><span class="sxs-lookup"><span data-stu-id="542fb-161"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span></span>
</dt> <dd>

<span data-ttu-id="542fb-162">Nome del valore del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="542fb-162">The registry value name.</span></span> <span data-ttu-id="542fb-163">Se questo valore è null, viene recuperato il valore della chiave senza nome o il valore predefinito, se disponibile.</span><span class="sxs-lookup"><span data-stu-id="542fb-163">If this value is null, then the value from the key's unnamed or default value, if any, is retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="542fb-164"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>Tipo</span><span class="sxs-lookup"><span data-stu-id="542fb-164"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>Type</span></span>
</dt> <dd>

<span data-ttu-id="542fb-165">Valore che determina se il valore del registro di sistema è un nome file, un percorso di directory o un valore del registro di sistema non elaborato.</span><span class="sxs-lookup"><span data-stu-id="542fb-165">A value that determines if the registry value is a file name, a directory location, or raw registry value.</span></span>

<span data-ttu-id="542fb-166">Nella tabella seguente sono elencati i valori validi.</span><span class="sxs-lookup"><span data-stu-id="542fb-166">The following table lists valid values.</span></span> <span data-ttu-id="542fb-167">Impostare uno dei primi tre valori e **msidbLocatorType64bit** , se necessario.</span><span class="sxs-lookup"><span data-stu-id="542fb-167">Set one of the first three values and **msidbLocatorType64bit** if necessary.</span></span> <span data-ttu-id="542fb-168">Se la voce in questo campo è assente, Type è impostato su 1.</span><span class="sxs-lookup"><span data-stu-id="542fb-168">If the entry in this field is absent, Type is set to be 1.</span></span>



| <span data-ttu-id="542fb-169">Costante</span><span class="sxs-lookup"><span data-stu-id="542fb-169">Constant</span></span>                      | <span data-ttu-id="542fb-170">Valore esadecimale</span><span class="sxs-lookup"><span data-stu-id="542fb-170">Hexadecimal</span></span> | <span data-ttu-id="542fb-171">Decimal</span><span class="sxs-lookup"><span data-stu-id="542fb-171">Decimal</span></span> | <span data-ttu-id="542fb-172">Descrizione</span><span class="sxs-lookup"><span data-stu-id="542fb-172">Description</span></span>                                                                                                                                                        |
|-------------------------------|-------------|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="542fb-173">**msidbLocatorTypeDirectory**</span><span class="sxs-lookup"><span data-stu-id="542fb-173">**msidbLocatorTypeDirectory**</span></span> | <span data-ttu-id="542fb-174">0x000</span><span class="sxs-lookup"><span data-stu-id="542fb-174">0x000</span></span>       | <span data-ttu-id="542fb-175">0</span><span class="sxs-lookup"><span data-stu-id="542fb-175">0</span></span>       | <span data-ttu-id="542fb-176">Il percorso della chiave è una directory.</span><span class="sxs-lookup"><span data-stu-id="542fb-176">Key path is a directory.</span></span>                                                                                                                                           |
| <span data-ttu-id="542fb-177">**msidbLocatorTypeFileName**</span><span class="sxs-lookup"><span data-stu-id="542fb-177">**msidbLocatorTypeFileName**</span></span>  | <span data-ttu-id="542fb-178">0x001</span><span class="sxs-lookup"><span data-stu-id="542fb-178">0x001</span></span>       | <span data-ttu-id="542fb-179">1</span><span class="sxs-lookup"><span data-stu-id="542fb-179">1</span></span>       | <span data-ttu-id="542fb-180">Il percorso della chiave è un nome di file.</span><span class="sxs-lookup"><span data-stu-id="542fb-180">Key path is a file name.</span></span>                                                                                                                                           |
| <span data-ttu-id="542fb-181">**msidbLocatorTypeRawValue**</span><span class="sxs-lookup"><span data-stu-id="542fb-181">**msidbLocatorTypeRawValue**</span></span>  | <span data-ttu-id="542fb-182">0x002</span><span class="sxs-lookup"><span data-stu-id="542fb-182">0x002</span></span>       | <span data-ttu-id="542fb-183">2</span><span class="sxs-lookup"><span data-stu-id="542fb-183">2</span></span>       | <span data-ttu-id="542fb-184">Il percorso della chiave è un valore del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="542fb-184">Key path is a registry value.</span></span>                                                                                                                                      |
| <span data-ttu-id="542fb-185">**msidbLocatorType64bit**</span><span class="sxs-lookup"><span data-stu-id="542fb-185">**msidbLocatorType64bit**</span></span>     | <span data-ttu-id="542fb-186">0x010</span><span class="sxs-lookup"><span data-stu-id="542fb-186">0x010</span></span>       | <span data-ttu-id="542fb-187">16</span><span class="sxs-lookup"><span data-stu-id="542fb-187">16</span></span>      | <span data-ttu-id="542fb-188">Impostare questo bit in modo che il programma di installazione cerchi la parte del registro di sistema a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="542fb-188">Set this bit to have the installer search the 64-bit portion of the registry.</span></span> <span data-ttu-id="542fb-189">Non impostare questo bit per fare in modo che il programma di installazione cerchi la parte del registro di sistema a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="542fb-189">Do not set this bit to have the installer search the 32-bit portion of the registry.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="542fb-190">Commenti</span><span class="sxs-lookup"><span data-stu-id="542fb-190">Remarks</span></span>

<span data-ttu-id="542fb-191">Si noti che se il valore nel campo tipo è **msidbLocatorTypeRawValue**, il programma di installazione imposta il valore della proprietà specificata nel campo della proprietà della tabella [AppSearch](appsearch-table.md) sul valore del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="542fb-191">Note that if the value in the Type field is **msidbLocatorTypeRawValue**, the installer sets the value of the property specified in the Property field of the [AppSearch](appsearch-table.md) table to the registry value.</span></span> <span data-ttu-id="542fb-192">Il programma di installazione aggiunge un prefisso al valore del registro di sistema che identifica il tipo di valore del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="542fb-192">The installer adds a prefix to the registry value that identifies the type of registry value.</span></span> <span data-ttu-id="542fb-193">Per ulteriori informazioni sui tipi di valori del registro di sistema, vedere [tipi di valore del registro di sistema](../sysinfo/registry-value-types.md).</span><span class="sxs-lookup"><span data-stu-id="542fb-193">For more information about types of registry values, see [Registry Value Types](../sysinfo/registry-value-types.md).</span></span>



| <span data-ttu-id="542fb-194">Tipo di registro</span><span class="sxs-lookup"><span data-stu-id="542fb-194">Registry type</span></span>   | <span data-ttu-id="542fb-195">Prefisso aggiunto dal programma di installazione</span><span class="sxs-lookup"><span data-stu-id="542fb-195">Prefix added by Installer</span></span>                                                                                                               |
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="542fb-196">REG \_ SZ</span><span class="sxs-lookup"><span data-stu-id="542fb-196">REG\_SZ</span></span>         | <span data-ttu-id="542fb-197">None, ma se il primo carattere del valore del registro di sistema è \# , il programma di installazione evita il carattere anteponendo un altro \# .</span><span class="sxs-lookup"><span data-stu-id="542fb-197">None, but if the first character of the registry value is \#, the installer escapes the character by prefixing a another \#.</span></span>            |
| <span data-ttu-id="542fb-198">DWORD</span><span class="sxs-lookup"><span data-stu-id="542fb-198">DWORD</span></span>           | <span data-ttu-id="542fb-199">" \# " seguito facoltativamente da' +' o da'-'</span><span class="sxs-lookup"><span data-stu-id="542fb-199">"\#" optionally followed by '+' or '-'</span></span>                                                                                                  |
| <span data-ttu-id="542fb-200">REG \_ Espandi \_ SZ</span><span class="sxs-lookup"><span data-stu-id="542fb-200">REG\_EXPAND\_SZ</span></span> | <span data-ttu-id="542fb-201">"\#%"</span><span class="sxs-lookup"><span data-stu-id="542fb-201">"\#%"</span></span>                                                                                                                                   |
| <span data-ttu-id="542fb-202">REG \_ - \_ SZ</span><span class="sxs-lookup"><span data-stu-id="542fb-202">REG\_MULTI\_SZ</span></span>  | <span data-ttu-id="542fb-203">Null.</span><span class="sxs-lookup"><span data-stu-id="542fb-203">Null.</span></span> <span data-ttu-id="542fb-204">Il programma di installazione imposta la proprietà su un valore che inizia con un valore null e termina con un valore null.</span><span class="sxs-lookup"><span data-stu-id="542fb-204">The installer sets the property to a value beginning with a null and ending with a null.</span></span>                                          |
| <span data-ttu-id="542fb-205">REG \_ binario</span><span class="sxs-lookup"><span data-stu-id="542fb-205">REG\_BINARY</span></span>     | <span data-ttu-id="542fb-206">" \# x" nel caso del \_ file binario REG, il programma di installazione converte e salva ogni cifra esadecimale (bocconcino) come carattere ASCII preceduto da " \# x".</span><span class="sxs-lookup"><span data-stu-id="542fb-206">"\#x" In case of REG\_BINARY, the installer converts and saves each hexadecimal digit (nibble) as an ASCII character prefixed by "\#x".</span></span> |



 

<span data-ttu-id="542fb-207">In genere, le colonne in questa tabella non sono localizzate.</span><span class="sxs-lookup"><span data-stu-id="542fb-207">Typically, the columns in this table are not localized.</span></span> <span data-ttu-id="542fb-208">Se un autore decide di cercare i prodotti in più lingue, è necessario che nella tabella sia inclusa una voce separata per ogni lingua.</span><span class="sxs-lookup"><span data-stu-id="542fb-208">If an author decides to search for products in multiple languages, then there must be a separate entry included in the table for each language.</span></span>

<span data-ttu-id="542fb-209">Si noti che non è possibile usare la tabella RegLocator per verificare solo la presenza della chiave.</span><span class="sxs-lookup"><span data-stu-id="542fb-209">Note that it is not possible to use the RegLocator table to check only for the presence of the key.</span></span> <span data-ttu-id="542fb-210">Tuttavia, è possibile cercare il valore predefinito di una chiave e recuperare il relativo valore se non è vuoto.</span><span class="sxs-lookup"><span data-stu-id="542fb-210">However, you can search for the default value of a key and retrieve its value if it is not empty.</span></span>

<span data-ttu-id="542fb-211">Per ulteriori informazioni, vedere [ricerca di applicazioni esistenti, file, voci del registro di sistema o voci del file ini](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md).</span><span class="sxs-lookup"><span data-stu-id="542fb-211">For more information, see [Searching for Existing Applications, Files, Registry Entries or .ini File Entries](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md).</span></span>

## <a name="validation"></a><span data-ttu-id="542fb-212">Convalida</span><span class="sxs-lookup"><span data-stu-id="542fb-212">Validation</span></span>

<dl>

[<span data-ttu-id="542fb-213">ICE03</span><span class="sxs-lookup"><span data-stu-id="542fb-213">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="542fb-214">ICE06</span><span class="sxs-lookup"><span data-stu-id="542fb-214">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="542fb-215">ICE46</span><span class="sxs-lookup"><span data-stu-id="542fb-215">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="542fb-216">ICE80</span><span class="sxs-lookup"><span data-stu-id="542fb-216">ICE80</span></span>](ice80.md)  
</dl>

 

 
