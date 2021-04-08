---
description: La tabella del registro di sistema include le informazioni del registro di sistema che l'applicazione deve impostare nel registro di sistema.
ms.assetid: 809ffd02-cf97-42d8-aed9-c13a14dcd8b4
title: Tabella del registro di sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b16cb2084716ea8cb9830056808e9c6be7da667f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967408"
---
# <a name="registry-table"></a><span data-ttu-id="fc10b-103">Tabella del registro di sistema</span><span class="sxs-lookup"><span data-stu-id="fc10b-103">Registry Table</span></span>

<span data-ttu-id="fc10b-104">La tabella del registro di sistema include le informazioni del registro di sistema che l'applicazione deve impostare nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="fc10b-104">The Registry table holds the registry information that the application needs to set in the system registry.</span></span>

<span data-ttu-id="fc10b-105">La tabella del registro di sistema contiene le colonne seguenti.</span><span class="sxs-lookup"><span data-stu-id="fc10b-105">The Registry table has the following columns.</span></span>



| <span data-ttu-id="fc10b-106">Colonna</span><span class="sxs-lookup"><span data-stu-id="fc10b-106">Column</span></span>      | <span data-ttu-id="fc10b-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="fc10b-107">Type</span></span>                         | <span data-ttu-id="fc10b-108">Chiave</span><span class="sxs-lookup"><span data-stu-id="fc10b-108">Key</span></span> | <span data-ttu-id="fc10b-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="fc10b-109">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="fc10b-110">Registro</span><span class="sxs-lookup"><span data-stu-id="fc10b-110">Registry</span></span>    | [<span data-ttu-id="fc10b-111">Identificatore</span><span class="sxs-lookup"><span data-stu-id="fc10b-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="fc10b-112">S</span><span class="sxs-lookup"><span data-stu-id="fc10b-112">Y</span></span>   | <span data-ttu-id="fc10b-113">N</span><span class="sxs-lookup"><span data-stu-id="fc10b-113">N</span></span>        |
| <span data-ttu-id="fc10b-114">Radice</span><span class="sxs-lookup"><span data-stu-id="fc10b-114">Root</span></span>        | [<span data-ttu-id="fc10b-115">Integer</span><span class="sxs-lookup"><span data-stu-id="fc10b-115">Integer</span></span>](integer.md)       | <span data-ttu-id="fc10b-116">N</span><span class="sxs-lookup"><span data-stu-id="fc10b-116">N</span></span>   | <span data-ttu-id="fc10b-117">N</span><span class="sxs-lookup"><span data-stu-id="fc10b-117">N</span></span>        |
| <span data-ttu-id="fc10b-118">Chiave</span><span class="sxs-lookup"><span data-stu-id="fc10b-118">Key</span></span>         | [<span data-ttu-id="fc10b-119">RegPath</span><span class="sxs-lookup"><span data-stu-id="fc10b-119">RegPath</span></span>](regpath.md)       | <span data-ttu-id="fc10b-120">N</span><span class="sxs-lookup"><span data-stu-id="fc10b-120">N</span></span>   | <span data-ttu-id="fc10b-121">N</span><span class="sxs-lookup"><span data-stu-id="fc10b-121">N</span></span>        |
| <span data-ttu-id="fc10b-122">Nome</span><span class="sxs-lookup"><span data-stu-id="fc10b-122">Name</span></span>        | [<span data-ttu-id="fc10b-123">Formattato</span><span class="sxs-lookup"><span data-stu-id="fc10b-123">Formatted</span></span>](formatted.md)   | <span data-ttu-id="fc10b-124">N</span><span class="sxs-lookup"><span data-stu-id="fc10b-124">N</span></span>   | <span data-ttu-id="fc10b-125">S</span><span class="sxs-lookup"><span data-stu-id="fc10b-125">Y</span></span>        |
| <span data-ttu-id="fc10b-126">Valore</span><span class="sxs-lookup"><span data-stu-id="fc10b-126">Value</span></span>       | [<span data-ttu-id="fc10b-127">Formattato</span><span class="sxs-lookup"><span data-stu-id="fc10b-127">Formatted</span></span>](formatted.md)   | <span data-ttu-id="fc10b-128">N</span><span class="sxs-lookup"><span data-stu-id="fc10b-128">N</span></span>   | <span data-ttu-id="fc10b-129">S</span><span class="sxs-lookup"><span data-stu-id="fc10b-129">Y</span></span>        |
| <span data-ttu-id="fc10b-130">Componente\_</span><span class="sxs-lookup"><span data-stu-id="fc10b-130">Component\_</span></span> | [<span data-ttu-id="fc10b-131">Identificatore</span><span class="sxs-lookup"><span data-stu-id="fc10b-131">Identifier</span></span>](identifier.md) | <span data-ttu-id="fc10b-132">N</span><span class="sxs-lookup"><span data-stu-id="fc10b-132">N</span></span>   | <span data-ttu-id="fc10b-133">N</span><span class="sxs-lookup"><span data-stu-id="fc10b-133">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="fc10b-134">Colonne</span><span class="sxs-lookup"><span data-stu-id="fc10b-134">Columns</span></span>

<dl> <dt>

<span data-ttu-id="fc10b-135"><span id="Registry"></span><span id="registry"></span><span id="REGISTRY"></span>Del registro</span><span class="sxs-lookup"><span data-stu-id="fc10b-135"><span id="Registry"></span><span id="registry"></span><span id="REGISTRY"></span>Registry</span></span>
</dt> <dd>

<span data-ttu-id="fc10b-136">Chiave primaria utilizzata per identificare un record del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="fc10b-136">Primary key used to identify a registry record.</span></span>

</dd> <dt>

<span data-ttu-id="fc10b-137"><span id="Root"></span><span id="root"></span><span id="ROOT"></span>Radice</span><span class="sxs-lookup"><span data-stu-id="fc10b-137"><span id="Root"></span><span id="root"></span><span id="ROOT"></span>Root</span></span>
</dt> <dd>

<span data-ttu-id="fc10b-138">Chiave radice predefinita per il valore del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="fc10b-138">The predefined root key for the registry value.</span></span> <span data-ttu-id="fc10b-139">Immettere un valore pari a-1 in questo campo per fare in modo che la chiave radice dipenda dal tipo di installazione.</span><span class="sxs-lookup"><span data-stu-id="fc10b-139">Enter a value of -1 in this field to make the root key dependent on the type of installation.</span></span> <span data-ttu-id="fc10b-140">Immettere uno degli altri valori nella tabella seguente per forzare la scrittura del valore del registro di sistema in una particolare chiave radice.</span><span class="sxs-lookup"><span data-stu-id="fc10b-140">Enter one of the other values in the following table to force the registry value to be written under a particular root key.</span></span>



| <span data-ttu-id="fc10b-141">Costante</span><span class="sxs-lookup"><span data-stu-id="fc10b-141">Constant</span></span>                          | <span data-ttu-id="fc10b-142">Valore esadecimale</span><span class="sxs-lookup"><span data-stu-id="fc10b-142">Hexadecimal</span></span> | <span data-ttu-id="fc10b-143">Decimal</span><span class="sxs-lookup"><span data-stu-id="fc10b-143">Decimal</span></span> | <span data-ttu-id="fc10b-144">Chiave radice</span><span class="sxs-lookup"><span data-stu-id="fc10b-144">Root key</span></span>                                                                                                                                                                                                                                                                                                                                     |
|-----------------------------------|-------------|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc10b-145">(nessuna)</span><span class="sxs-lookup"><span data-stu-id="fc10b-145">(none)</span></span>                            | <span data-ttu-id="fc10b-146">\- 0x001</span><span class="sxs-lookup"><span data-stu-id="fc10b-146">\- 0x001</span></span>    | <span data-ttu-id="fc10b-147">-1</span><span class="sxs-lookup"><span data-stu-id="fc10b-147">-1</span></span>      | <span data-ttu-id="fc10b-148">Se si tratta di un'installazione per utente, il valore del registro di sistema viene scritto in **HKEY \_ Current \_ User**.</span><span class="sxs-lookup"><span data-stu-id="fc10b-148">If this is a per-user installation, the registry value is written under **HKEY\_CURRENT\_USER**.</span></span> <span data-ttu-id="fc10b-149">Se si tratta di un'installazione per computer, il valore del registro di sistema viene scritto in **HKEY \_ Local \_ Machine**.</span><span class="sxs-lookup"><span data-stu-id="fc10b-149">If this is a per-machine installation, the registry value is written under **HKEY\_LOCAL\_MACHINE**.</span></span> <span data-ttu-id="fc10b-150">Si noti che un'installazione per computer viene specificata impostando la proprietà [**ALLUSERS**](allusers.md) su 1.</span><span class="sxs-lookup"><span data-stu-id="fc10b-150">Note that a per-machine installation is specified by setting the [**ALLUSERS**](allusers.md) property to 1.</span></span><br/>                |
| <span data-ttu-id="fc10b-151">**msidbRegistryRootClassesRoot**</span><span class="sxs-lookup"><span data-stu-id="fc10b-151">**msidbRegistryRootClassesRoot**</span></span>  | <span data-ttu-id="fc10b-152">0x000</span><span class="sxs-lookup"><span data-stu-id="fc10b-152">0x000</span></span>       | <span data-ttu-id="fc10b-153">0</span><span class="sxs-lookup"><span data-stu-id="fc10b-153">0</span></span>       | <span data-ttu-id="fc10b-154">**HKEY \_ CLASSI \_ radice** il programma di installazione scrive o rimuove il valore da **HKCU \\ software \\ Classes** hive durante l'installazione nel [contesto di installazione](installation-context.md)per utente.</span><span class="sxs-lookup"><span data-stu-id="fc10b-154">**HKEY\_CLASSES\_ROOT** The installer writes or removes the value from the **HKCU\\Software\\Classes** hive during installation in the per-user [installation context](installation-context.md).</span></span><br/> <span data-ttu-id="fc10b-155">Il programma di installazione scrive o rimuove il valore dall'hive **\\ \\ classi Software HKLM** durante le installazioni per computer.</span><span class="sxs-lookup"><span data-stu-id="fc10b-155">The installer writes or removes the value from the **HKLM\\Software\\Classes** hive during per-machine installations.</span></span><br/> |
| <span data-ttu-id="fc10b-156">**msidbRegistryRootCurrentUser**</span><span class="sxs-lookup"><span data-stu-id="fc10b-156">**msidbRegistryRootCurrentUser**</span></span>  | <span data-ttu-id="fc10b-157">0x001</span><span class="sxs-lookup"><span data-stu-id="fc10b-157">0x001</span></span>       | <span data-ttu-id="fc10b-158">1</span><span class="sxs-lookup"><span data-stu-id="fc10b-158">1</span></span>       | <span data-ttu-id="fc10b-159">**HKEY \_ \_ utente corrente**</span><span class="sxs-lookup"><span data-stu-id="fc10b-159">**HKEY\_CURRENT\_USER**</span></span>                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="fc10b-160">**msidbRegistryRootLocalMachine**</span><span class="sxs-lookup"><span data-stu-id="fc10b-160">**msidbRegistryRootLocalMachine**</span></span> | <span data-ttu-id="fc10b-161">0x002</span><span class="sxs-lookup"><span data-stu-id="fc10b-161">0x002</span></span>       | <span data-ttu-id="fc10b-162">2</span><span class="sxs-lookup"><span data-stu-id="fc10b-162">2</span></span>       | <span data-ttu-id="fc10b-163">**\_computer locale \_ HKEY**</span><span class="sxs-lookup"><span data-stu-id="fc10b-163">**HKEY\_LOCAL\_MACHINE**</span></span>                                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="fc10b-164">**msidbRegistryRootUsers**</span><span class="sxs-lookup"><span data-stu-id="fc10b-164">**msidbRegistryRootUsers**</span></span>        | <span data-ttu-id="fc10b-165">0x003</span><span class="sxs-lookup"><span data-stu-id="fc10b-165">0x003</span></span>       | <span data-ttu-id="fc10b-166">3</span><span class="sxs-lookup"><span data-stu-id="fc10b-166">3</span></span>       | <span data-ttu-id="fc10b-167">**\_utenti HKEY**</span><span class="sxs-lookup"><span data-stu-id="fc10b-167">**HKEY\_USERS**</span></span>                                                                                                                                                                                                                                                                                                                              |



 

<span data-ttu-id="fc10b-168">Si noti che è consigliabile che le voci del registro di sistema scritte nell'hive **HKCU** facciano riferimento a un componente con il bit RegistryKeyPath impostato nella colonna Attributes della [tabella Component](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="fc10b-168">Note that it is recommended that registry entries written to the **HKCU** hive reference a component having the RegistryKeyPath bit set in the Attributes column of the [Component table](component-table.md).</span></span> <span data-ttu-id="fc10b-169">Ciò garantisce che il programma di installazione scriva le voci del registro di sistema necessarie quando sono presenti più utenti nello stesso computer.</span><span class="sxs-lookup"><span data-stu-id="fc10b-169">This ensures that the installer writes the necessary registry entries when there are multiple users on the same computer.</span></span>

</dd> <dt>

<span data-ttu-id="fc10b-170"><span id="Key"></span><span id="key"></span><span id="KEY"></span>Chiave</span><span class="sxs-lookup"><span data-stu-id="fc10b-170"><span id="Key"></span><span id="key"></span><span id="KEY"></span>Key</span></span>
</dt> <dd>

<span data-ttu-id="fc10b-171">Chiave localizzabile per il valore del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="fc10b-171">The localizable key for the registry value.</span></span>

</dd> <dt>

<span data-ttu-id="fc10b-172"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Nome</span><span class="sxs-lookup"><span data-stu-id="fc10b-172"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span></span>
</dt> <dd>

<span data-ttu-id="fc10b-173">Questa colonna contiene il nome del valore del registro di sistema (localizzabile).</span><span class="sxs-lookup"><span data-stu-id="fc10b-173">This column contains the registry value name (localizable).</span></span> <span data-ttu-id="fc10b-174">Se è null, i dati immessi nella colonna valore vengono scritti nella chiave del registro di sistema predefinita.</span><span class="sxs-lookup"><span data-stu-id="fc10b-174">If this is Null, then the data entered into the Value column are written to the default registry key.</span></span>

<span data-ttu-id="fc10b-175">Se la colonna valore è null, le stringhe mostrate nella tabella seguente nella colonna Name hanno un significato speciale.</span><span class="sxs-lookup"><span data-stu-id="fc10b-175">If the Value column is Null, then the strings shown in the following table in the Name column have special significance.</span></span>



| <span data-ttu-id="fc10b-176">string</span><span class="sxs-lookup"><span data-stu-id="fc10b-176">String</span></span> | <span data-ttu-id="fc10b-177">Significato</span><span class="sxs-lookup"><span data-stu-id="fc10b-177">Meaning</span></span>                                                                                                                                                                                          |
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \+     | <span data-ttu-id="fc10b-178">La chiave deve essere creata, se assente, durante l'installazione del componente.</span><span class="sxs-lookup"><span data-stu-id="fc10b-178">The key is to be created, if absent, when the component is installed.</span></span>                                                                                                                            |
| \-     | <span data-ttu-id="fc10b-179">La chiave deve essere eliminata, se presente, con tutti i relativi valori e sottochiavi, quando viene disinstallato il componente.</span><span class="sxs-lookup"><span data-stu-id="fc10b-179">The key is to be deleted, if present, with all of its values and subkeys, when the component is uninstalled.</span></span>                                                                                     |
| \*     | <span data-ttu-id="fc10b-180">La chiave deve essere creata, se assente, durante l'installazione del componente.</span><span class="sxs-lookup"><span data-stu-id="fc10b-180">The key is to be created, if absent, when the component is installed.</span></span> <span data-ttu-id="fc10b-181">Inoltre, la chiave deve essere eliminata, se presente, con tutti i relativi valori e sottochiavi quando il componente viene disinstallato.</span><span class="sxs-lookup"><span data-stu-id="fc10b-181">Additionally, the key is to be deleted, if present, with all of its values and subkeys, when the component is uninstalled.</span></span> |



 

<span data-ttu-id="fc10b-182">Si noti che è necessario usare la [tabella RemoveRegistry](removeregistry-table.md) se è necessario eliminare una chiave del registro di sistema installata, con i relativi valori e sottochiavi, quando viene installato il componente.</span><span class="sxs-lookup"><span data-stu-id="fc10b-182">Note that the [RemoveRegistry table](removeregistry-table.md) must be used if an installed registry key is to be deleted, with its values and subkeys, when the component is installed.</span></span>

</dd> <dt>

<span data-ttu-id="fc10b-183"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valore</span><span class="sxs-lookup"><span data-stu-id="fc10b-183"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Value</span></span>
</dt> <dd>

<span data-ttu-id="fc10b-184">Questa colonna è il valore del registro di sistema localizzabile.</span><span class="sxs-lookup"><span data-stu-id="fc10b-184">This column is the localizable registry value.</span></span> <span data-ttu-id="fc10b-185">Il campo è [formattato](formatted.md).</span><span class="sxs-lookup"><span data-stu-id="fc10b-185">The field is [Formatted](formatted.md).</span></span> <span data-ttu-id="fc10b-186">Se il valore è collegato a uno dei seguenti prefissi (ovvero \# % *valore*), il valore viene interpretato come descritto nella tabella.</span><span class="sxs-lookup"><span data-stu-id="fc10b-186">If the value is attached to one of the following prefixes (i.e. \#%*value*) then the value is interpreted as described in the table.</span></span> <span data-ttu-id="fc10b-187">Si noti che ogni prefisso inizia con un simbolo di cancelletto ( \# ).</span><span class="sxs-lookup"><span data-stu-id="fc10b-187">Note that each prefix begins with a number sign (\#).</span></span> <span data-ttu-id="fc10b-188">Se il valore inizia con due o più segni di cancelletto consecutivi ( \# ), il primo \# viene ignorato e il valore viene interpretato e archiviato come stringa.</span><span class="sxs-lookup"><span data-stu-id="fc10b-188">If the value begins with two or more consecutive number signs (\#), the first \# is ignored and value is interpreted and stored as a string.</span></span>



| <span data-ttu-id="fc10b-189">Prefisso</span><span class="sxs-lookup"><span data-stu-id="fc10b-189">Prefix</span></span> | <span data-ttu-id="fc10b-190">Significato</span><span class="sxs-lookup"><span data-stu-id="fc10b-190">Meaning</span></span>                                                                        |
|--------|--------------------------------------------------------------------------------|
| <span data-ttu-id="fc10b-191">\#x</span><span class="sxs-lookup"><span data-stu-id="fc10b-191">\#x</span></span>    | <span data-ttu-id="fc10b-192">Il valore viene interpretato e archiviato come valore esadecimale (REG \_ Binary).</span><span class="sxs-lookup"><span data-stu-id="fc10b-192">The value is interpreted and stored as a hexadecimal value (REG\_BINARY).</span></span>      |
| \#%    | <span data-ttu-id="fc10b-193">Il valore viene interpretato e archiviato come stringa espandibile (REG \_ expand \_ SZ).</span><span class="sxs-lookup"><span data-stu-id="fc10b-193">The value is interpreted and stored as an expandable string (REG\_EXPAND\_SZ).</span></span> |
| \#     | <span data-ttu-id="fc10b-194">Il valore viene interpretato e archiviato come Integer (REG \_ DWORD).</span><span class="sxs-lookup"><span data-stu-id="fc10b-194">The value is interpreted and stored as an integer (REG\_DWORD).</span></span>                |



 

-   <span data-ttu-id="fc10b-195">Se il valore contiene la tilde della sequenza \[ ~ \] , il valore viene interpretato come un elenco di stringhe delimitato da valori null ( \_ reg \_ multisz).</span><span class="sxs-lookup"><span data-stu-id="fc10b-195">If the value contains the sequence tilde \[~\], then the value is interpreted as a Null-delimited list of strings (REG\_MULTI\_SZ).</span></span> <span data-ttu-id="fc10b-196">Per specificare, ad esempio, un elenco contenente le tre stringhe a, b e c, utilizzare "a \[ ~ \] b \[ ~ \] c".</span><span class="sxs-lookup"><span data-stu-id="fc10b-196">For example, to specify a list containing the three strings a, b and c, use "a\[~\]b\[~\]c".</span></span>
-   <span data-ttu-id="fc10b-197">La sequenza \[ ~ \] all'interno del valore separa le singole stringhe e viene interpretata e archiviata come carattere null.</span><span class="sxs-lookup"><span data-stu-id="fc10b-197">The sequence \[~\] within the value separates the individual strings and is interpreted and stored as a Null character.</span></span>
-   <span data-ttu-id="fc10b-198">Se un oggetto \[ ~ \] precede l'elenco di stringhe, le stringhe devono essere aggiunte alle stringhe dei valori del registro di sistema esistenti.</span><span class="sxs-lookup"><span data-stu-id="fc10b-198">If a \[~\] precedes the string list, the strings are to be appended to any existing registry value strings.</span></span> <span data-ttu-id="fc10b-199">Se nel valore del registro di sistema è già presente una stringa di Accodamento, viene rimossa l'occorrenza originale della stringa.</span><span class="sxs-lookup"><span data-stu-id="fc10b-199">If an appending string already occurs in the registry value, the original occurrence of the string is removed.</span></span>
-   <span data-ttu-id="fc10b-200">Se un oggetto \[ ~ \] segue la fine dell'elenco di stringhe, le stringhe devono essere antepone alle stringhe dei valori del registro di sistema esistenti.</span><span class="sxs-lookup"><span data-stu-id="fc10b-200">If a \[~\] follows the end of the string list, the strings are to be prepended to any existing registry value strings.</span></span> <span data-ttu-id="fc10b-201">Se una stringa in sospeso si trova già nel valore del registro di sistema, viene rimossa l'occorrenza originale della stringa.</span><span class="sxs-lookup"><span data-stu-id="fc10b-201">If a prepending string already occurs in the registry value, the original occurrence of the string is removed.</span></span>
-   <span data-ttu-id="fc10b-202">Se un oggetto \[ ~ \] si trova sia all'inizio che alla fine o all'inizio o alla fine dell'elenco di stringhe, le stringhe devono sostituire tutte le stringhe del valore del registro di sistema esistenti.</span><span class="sxs-lookup"><span data-stu-id="fc10b-202">If a \[~\] is at both the beginning and the end or at neither the beginning nor the end of the string list, the strings are to replace any existing registry value strings.</span></span>
-   <span data-ttu-id="fc10b-203">In caso contrario, il valore viene interpretato e archiviato come stringa (REG \_ SZ).</span><span class="sxs-lookup"><span data-stu-id="fc10b-203">Otherwise, the value is interpreted and stored as a string (REG\_SZ).</span></span>

</dd> <dt>

<span data-ttu-id="fc10b-204"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_</span><span class="sxs-lookup"><span data-stu-id="fc10b-204"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="fc10b-205">Chiave esterna nella prima colonna della tabella dei [componenti](component-table.md) che fa riferimento al componente che controlla l'installazione del valore del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="fc10b-205">External key into the first column of the [Component table](component-table.md) referencing the component that controls the installation of the registry value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fc10b-206">Commenti</span><span class="sxs-lookup"><span data-stu-id="fc10b-206">Remarks</span></span>

<span data-ttu-id="fc10b-207">Le azioni [WriteRegistryValori consente](writeregistryvalues-action.md) e [RemoveRegistryValues](removeregistryvalues-action.md) nelle [*tabelle di sequenza*](s-gly.md) elaborano le informazioni contenute in questa tabella.</span><span class="sxs-lookup"><span data-stu-id="fc10b-207">The [WriteRegistryValues](writeregistryvalues-action.md) and [RemoveRegistryValues](removeregistryvalues-action.md) actions in [*sequence tables*](s-gly.md) process the information in this table.</span></span> <span data-ttu-id="fc10b-208">Per informazioni sull'utilizzo di *tabelle di sequenza*, vedere [utilizzo di una tabella di sequenza](using-a-sequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="fc10b-208">For information about using *sequence tables*, see [Using a Sequence Table](using-a-sequence-table.md).</span></span>

<span data-ttu-id="fc10b-209">Le informazioni del registro di sistema vengono scritte nel registro di sistema quando il componente corrispondente è stato selezionato per l'installazione locale o per l'esecuzione dall'origine.</span><span class="sxs-lookup"><span data-stu-id="fc10b-209">The registry information is written out to the system registry when the corresponding component has been selected to be installed locally or run from source.</span></span>

<span data-ttu-id="fc10b-210">Si noti che il programma di installazione rimuove una chiave del registro di sistema dopo la rimozione dell'ultimo valore o della sottochiave sotto la chiave.</span><span class="sxs-lookup"><span data-stu-id="fc10b-210">Note that the installer removes a registry key after removing the last value or subkey under the key.</span></span> <span data-ttu-id="fc10b-211">Per evitare la rimozione di una chiave del registro di sistema vuota durante la disinstallazione di, scrivere un valore fittizio sotto la chiave che deve essere mantenuta e immettere + nella colonna nome.</span><span class="sxs-lookup"><span data-stu-id="fc10b-211">To prevent an empty registry key from being removed when uninstalling, write a dummy value under the key you need to keep and enter + in the Name column.</span></span> <span data-ttu-id="fc10b-212">Se \* è nella colonna nome, la chiave viene eliminata con tutti i relativi valori e sottochiavi quando il componente viene rimosso.</span><span class="sxs-lookup"><span data-stu-id="fc10b-212">If \* is in the Name column, the key is deleted, with all of its values and subkeys, when the component is removed.</span></span>

<span data-ttu-id="fc10b-213">È possibile utilizzare un'azione personalizzata per aggiungere righe alla tabella del registro di sistema durante un'installazione, una disinstallazione o una transazione di ripristino.</span><span class="sxs-lookup"><span data-stu-id="fc10b-213">A custom action can be used to add rows to the Registry table during an installation, uninstallation, or repair transaction.</span></span> <span data-ttu-id="fc10b-214">Queste righe non vengono mantenute nella tabella del registro di sistema e le informazioni sono disponibili solo durante la transazione corrente.</span><span class="sxs-lookup"><span data-stu-id="fc10b-214">These rows do not persist in the Registry table and the information is only available during the current transaction.</span></span> <span data-ttu-id="fc10b-215">L'azione personalizzata deve pertanto essere eseguita in ogni installazione, disinstallazione o ripristino della transazione che richiede le informazioni contenute in queste righe aggiuntive.</span><span class="sxs-lookup"><span data-stu-id="fc10b-215">The custom action must therefore be run in every installation, uninstallation, or repair transaction that requires the information in these additional rows.</span></span> <span data-ttu-id="fc10b-216">L'azione personalizzata deve precedere le azioni [RemoveRegistryValues](removeregistryvalues-action.md) e [WriteRegistryValori consente](writeregistryvalues-action.md) nella sequenza di azione.</span><span class="sxs-lookup"><span data-stu-id="fc10b-216">The custom action must come before the [RemoveRegistryValues](removeregistryvalues-action.md) and [WriteRegistryValues](writeregistryvalues-action.md) actions in the action sequence.</span></span>

<span data-ttu-id="fc10b-217">Per informazioni su come proteggere una chiave del registro di sistema, vedere la [tabella MsiLockPermissionsEx](msilockpermissionsex-table.md) e la [tabella LockPermissions](lockpermissions-table.md).</span><span class="sxs-lookup"><span data-stu-id="fc10b-217">For information on how to secure a registry key see the [MsiLockPermissionsEx Table](msilockpermissionsex-table.md) and [LockPermissions Table](lockpermissions-table.md).</span></span>

## <a name="validation"></a><span data-ttu-id="fc10b-218">Convalida</span><span class="sxs-lookup"><span data-stu-id="fc10b-218">Validation</span></span>

<dl>

[<span data-ttu-id="fc10b-219">ICE02</span><span class="sxs-lookup"><span data-stu-id="fc10b-219">ICE02</span></span>](ice02.md)  
[<span data-ttu-id="fc10b-220">ICE03</span><span class="sxs-lookup"><span data-stu-id="fc10b-220">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="fc10b-221">ICE06</span><span class="sxs-lookup"><span data-stu-id="fc10b-221">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="fc10b-222">ICE32</span><span class="sxs-lookup"><span data-stu-id="fc10b-222">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="fc10b-223">ICE38</span><span class="sxs-lookup"><span data-stu-id="fc10b-223">ICE38</span></span>](ice38.md)  
[<span data-ttu-id="fc10b-224">ICE43</span><span class="sxs-lookup"><span data-stu-id="fc10b-224">ICE43</span></span>](ice43.md)  
[<span data-ttu-id="fc10b-225">ICE46</span><span class="sxs-lookup"><span data-stu-id="fc10b-225">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="fc10b-226">ICE49</span><span class="sxs-lookup"><span data-stu-id="fc10b-226">ICE49</span></span>](ice49.md)  
[<span data-ttu-id="fc10b-227">ICE53</span><span class="sxs-lookup"><span data-stu-id="fc10b-227">ICE53</span></span>](ice53.md)  
[<span data-ttu-id="fc10b-228">ICE55</span><span class="sxs-lookup"><span data-stu-id="fc10b-228">ICE55</span></span>](ice55.md)  
[<span data-ttu-id="fc10b-229">ICE57</span><span class="sxs-lookup"><span data-stu-id="fc10b-229">ICE57</span></span>](ice57.md)  
[<span data-ttu-id="fc10b-230">ICE70</span><span class="sxs-lookup"><span data-stu-id="fc10b-230">ICE70</span></span>](ice70.md)  
[<span data-ttu-id="fc10b-231">ICE80</span><span class="sxs-lookup"><span data-stu-id="fc10b-231">ICE80</span></span>](ice80.md)  
</dl>

 

 




