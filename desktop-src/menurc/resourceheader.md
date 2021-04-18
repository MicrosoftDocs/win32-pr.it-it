---
title: Struttura RESOURCEHEADER
description: Contiene informazioni sull'intestazione della risorsa stessa e i dati specifici per questa risorsa.
ms.assetid: e0eba7b3-a275-4ffe-9347-46361213cf48
keywords:
- Menu struttura RESOURCEHEADER e altre risorse
topic_type:
- apiref
api_name:
- RESOURCEHEADER
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 41b436ebd6aeb5dc31f8ed773fbe7b12a1586185
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301194"
---
# <a name="resourceheader-structure"></a><span data-ttu-id="8f6fe-104">Struttura RESOURCEHEADER</span><span class="sxs-lookup"><span data-stu-id="8f6fe-104">RESOURCEHEADER structure</span></span>

<span data-ttu-id="8f6fe-105">Contiene informazioni sull'intestazione della risorsa stessa e i dati specifici per questa risorsa.</span><span class="sxs-lookup"><span data-stu-id="8f6fe-105">Contains information about the resource header itself and the data specific to this resource.</span></span> <span data-ttu-id="8f6fe-106">Questa struttura non è una vera struttura del linguaggio C, perché contiene membri a lunghezza variabile.</span><span class="sxs-lookup"><span data-stu-id="8f6fe-106">This structure is not a true C-language structure, because it contains variable-length members.</span></span> <span data-ttu-id="8f6fe-107">La definizione della struttura fornita qui è solo per la spiegazione. non è presente in alcun file di intestazione standard.</span><span class="sxs-lookup"><span data-stu-id="8f6fe-107">The structure definition provided here is for explanation only; it is not present in any standard header file.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f6fe-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8f6fe-108">Syntax</span></span>


```C++
typedef struct {
  DWORD DataSize;
  DWORD HeaderSize;
  DWORD TYPE;
  DWORD NAME;
  DWORD DataVersion;
  WORD  MemoryFlags;
  WORD  LanguageId;
  DWORD Version;
  DWORD Characteristics;
} RESOURCEHEADER;
```



## <a name="members"></a><span data-ttu-id="8f6fe-109">Members</span><span class="sxs-lookup"><span data-stu-id="8f6fe-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="8f6fe-110">**DataSize**</span><span class="sxs-lookup"><span data-stu-id="8f6fe-110">**DataSize**</span></span>
</dt> <dd>

<span data-ttu-id="8f6fe-111">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="8f6fe-111">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="8f6fe-112">Dimensioni, in byte, dei dati che seguono l'intestazione della risorsa per la risorsa specifica.</span><span class="sxs-lookup"><span data-stu-id="8f6fe-112">The size, in bytes, of the data that follows the resource header for this particular resource.</span></span> <span data-ttu-id="8f6fe-113">Non include alcun riempimento di file tra questa risorsa e tutte le risorse che lo seguono nel file di risorse.</span><span class="sxs-lookup"><span data-stu-id="8f6fe-113">It does not include any file padding between this resource and any resource that follows it in the resource file.</span></span>

</dd> <dt>

<span data-ttu-id="8f6fe-114">**HeaderSize**</span><span class="sxs-lookup"><span data-stu-id="8f6fe-114">**HeaderSize**</span></span>
</dt> <dd>

<span data-ttu-id="8f6fe-115">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="8f6fe-115">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="8f6fe-116">Dimensione, in byte, dei dati dell'intestazione della risorsa che seguono.</span><span class="sxs-lookup"><span data-stu-id="8f6fe-116">The size, in bytes, of the resource header data that follows.</span></span>

</dd> <dt>

<span data-ttu-id="8f6fe-117">**TYPE**</span><span class="sxs-lookup"><span data-stu-id="8f6fe-117">**TYPE**</span></span>
</dt> <dd>

<span data-ttu-id="8f6fe-118">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="8f6fe-118">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="8f6fe-119">Tipo di risorsa.</span><span class="sxs-lookup"><span data-stu-id="8f6fe-119">The resource type.</span></span> <span data-ttu-id="8f6fe-120">Il membro del **tipo** può essere un valore numerico o una stringa Unicode con terminazione null che specifica il nome del tipo.</span><span class="sxs-lookup"><span data-stu-id="8f6fe-120">The **TYPE** member can either be a numeric value or a null-terminated Unicode string that specifies the name of the type.</span></span> <span data-ttu-id="8f6fe-121">Per una descrizione dei membri di tipo **nome** o **ordinale** , vedere la sezione Osservazioni riportata di seguito.</span><span class="sxs-lookup"><span data-stu-id="8f6fe-121">See the following Remarks section for a description of **Name** or **Ordinal** type members.</span></span>

<span data-ttu-id="8f6fe-122">Se il membro del **tipo** è un valore numerico, può specificare un tipo di risorsa standard o definito dall'utente.</span><span class="sxs-lookup"><span data-stu-id="8f6fe-122">If the **TYPE** member is a numeric value, it can specify either a standard or a user-defined resource type.</span></span> <span data-ttu-id="8f6fe-123">Se il membro è una stringa, si tratta di un tipo di risorsa definito dall'utente.</span><span class="sxs-lookup"><span data-stu-id="8f6fe-123">If the member is a string, then it is a user-defined resource type.</span></span> <span data-ttu-id="8f6fe-124">Per un elenco dei tipi di risorsa predefiniti, vedere [tipi di risorse](/windows/desktop/menurc/resource-types).</span><span class="sxs-lookup"><span data-stu-id="8f6fe-124">For a list of the predefined resource types, see [Resource Types](/windows/desktop/menurc/resource-types).</span></span>

<span data-ttu-id="8f6fe-125">I valori minori di 256 sono riservati per l'utilizzo da parte del sistema.</span><span class="sxs-lookup"><span data-stu-id="8f6fe-125">Values less than 256 are reserved for system use.</span></span>

</dd> <dt>

<span data-ttu-id="8f6fe-126">**NOME**</span><span class="sxs-lookup"><span data-stu-id="8f6fe-126">**NAME**</span></span>
</dt> <dd>

<span data-ttu-id="8f6fe-127">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="8f6fe-127">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="8f6fe-128">Nome che identifica la risorsa specifica.</span><span class="sxs-lookup"><span data-stu-id="8f6fe-128">A name that identifies the particular resource.</span></span> <span data-ttu-id="8f6fe-129">Il membro del **nome** , ad esempio il membro del **tipo** , può essere un valore numerico o una stringa Unicode con terminazione null.</span><span class="sxs-lookup"><span data-stu-id="8f6fe-129">The **NAME** member, like the **TYPE** member, can either be a numeric value or a null-terminated Unicode string.</span></span> <span data-ttu-id="8f6fe-130">Per una descrizione dei membri di tipo **nome** o **ordinale** , vedere la sezione Osservazioni riportata di seguito.</span><span class="sxs-lookup"><span data-stu-id="8f6fe-130">See the following Remarks section for a description of **Name** or **Ordinal** type members.</span></span>

<span data-ttu-id="8f6fe-131">Non è necessario aggiungere la spaziatura interna per l'allineamento **DWORD** tra i membri del **tipo** e del **nome** perché contengono dati di **Word** .</span><span class="sxs-lookup"><span data-stu-id="8f6fe-131">You do not need to add padding for **DWORD** alignment between the **TYPE** and **NAME** members because they contain **WORD** data.</span></span> <span data-ttu-id="8f6fe-132">Tuttavia, potrebbe essere necessario aggiungere una **parola** di riempimento dopo il membro del **nome** per allineare il resto dell'intestazione ai limiti **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="8f6fe-132">However, you may need to add a **WORD** of padding after the **NAME** member to align the rest of the header on **DWORD** boundaries.</span></span>

</dd> <dt>

<span data-ttu-id="8f6fe-133">**Dataversion**</span><span class="sxs-lookup"><span data-stu-id="8f6fe-133">**DataVersion**</span></span>
</dt> <dd>

<span data-ttu-id="8f6fe-134">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="8f6fe-134">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="8f6fe-135">Versione di dati della risorsa predefinita.</span><span class="sxs-lookup"><span data-stu-id="8f6fe-135">A predefined resource data version.</span></span> <span data-ttu-id="8f6fe-136">In questo modo verrà determinata la versione dei dati della risorsa che l'applicazione deve utilizzare.</span><span class="sxs-lookup"><span data-stu-id="8f6fe-136">This will determine which version of the resource data the application should use.</span></span>

</dd> <dt>

<span data-ttu-id="8f6fe-137">**MemoryFlags**</span><span class="sxs-lookup"><span data-stu-id="8f6fe-137">**MemoryFlags**</span></span>
</dt> <dd>

<span data-ttu-id="8f6fe-138">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="8f6fe-138">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="8f6fe-139">Set di flag di attributo che possono descrivere lo stato della risorsa.</span><span class="sxs-lookup"><span data-stu-id="8f6fe-139">A set of attribute flags that can describe the state of the resource.</span></span> <span data-ttu-id="8f6fe-140">Modificatori in. Il file di script RC assegna questi attributi alla risorsa.</span><span class="sxs-lookup"><span data-stu-id="8f6fe-140">Modifiers in the .RC script file assign these attributes to the resource.</span></span> <span data-ttu-id="8f6fe-141">Gli identificatori di script possono assegnare i valori dei flag seguenti.</span><span class="sxs-lookup"><span data-stu-id="8f6fe-141">The script identifiers can assign the following flag values.</span></span>

<span data-ttu-id="8f6fe-142">Le applicazioni non utilizzano uno di questi attributi.</span><span class="sxs-lookup"><span data-stu-id="8f6fe-142">Applications do not use any of these attributes.</span></span> <span data-ttu-id="8f6fe-143">Gli attributi sono consentiti nello script per la compatibilità con le versioni precedenti degli script esistenti, ma vengono ignorati.</span><span class="sxs-lookup"><span data-stu-id="8f6fe-143">The attributes are permitted in the script for backward compatibility with existing scripts, but they are ignored.</span></span> <span data-ttu-id="8f6fe-144">Le risorse vengono caricate quando viene caricato il modulo corrispondente e vengono liberate quando il modulo viene scaricato.</span><span class="sxs-lookup"><span data-stu-id="8f6fe-144">Resources are loaded when the corresponding module is loaded, and are freed when the module is unloaded.</span></span>

<dt>

<span id="MOVEABLE"></span><span id="moveable"></span>

<span data-ttu-id="8f6fe-145">**Mobile** (0x0010)</span><span class="sxs-lookup"><span data-stu-id="8f6fe-145">**MOVEABLE** (0x0010)</span></span>


</dt> <dd></dd> <dt>

<span id="FIXED"></span><span id="fixed"></span>

<span data-ttu-id="8f6fe-146">**corretto** (~ mobile)</span><span class="sxs-lookup"><span data-stu-id="8f6fe-146">**FIXED** (~MOVEABLE)</span></span>


</dt> <dd></dd> <dt>

<span id="PURE"></span><span id="pure"></span>

<span data-ttu-id="8f6fe-147">**Pure** (0x0020)</span><span class="sxs-lookup"><span data-stu-id="8f6fe-147">**PURE** (0x0020)</span></span>


</dt> <dd></dd> <dt>

<span id="IMPURE"></span><span id="impure"></span>

<span data-ttu-id="8f6fe-148">**impure** (~ pure)</span><span class="sxs-lookup"><span data-stu-id="8f6fe-148">**IMPURE** (~PURE)</span></span>


</dt> <dd></dd> <dt>

<span id="PRELOAD"></span><span id="preload"></span>

<span data-ttu-id="8f6fe-149">**Precaricamento** (0x0040)</span><span class="sxs-lookup"><span data-stu-id="8f6fe-149">**PRELOAD** (0x0040)</span></span>


</dt> <dd></dd> <dt>

<span id="LOADONCALL"></span><span id="loadoncall"></span>

<span data-ttu-id="8f6fe-150">**LOADONCALL** (~ preload)</span><span class="sxs-lookup"><span data-stu-id="8f6fe-150">**LOADONCALL** (~PRELOAD)</span></span>


</dt> <dd></dd> <dt>

<span id="DISCARDABLE"></span><span id="discardable"></span>

<span data-ttu-id="8f6fe-151">Annullabile **(0x1000** )</span><span class="sxs-lookup"><span data-stu-id="8f6fe-151">**DISCARDABLE** (0x1000)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="8f6fe-152">**LanguageId**</span><span class="sxs-lookup"><span data-stu-id="8f6fe-152">**LanguageId**</span></span>
</dt> <dd>

<span data-ttu-id="8f6fe-153">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="8f6fe-153">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="8f6fe-154">Lingua della risorsa o del set di risorse.</span><span class="sxs-lookup"><span data-stu-id="8f6fe-154">The language for the resource or set of resources.</span></span> <span data-ttu-id="8f6fe-155">Impostare il valore di questo membro con l'istruzione di definizione della risorsa della [lingua](./language-statement.md) facoltativa.</span><span class="sxs-lookup"><span data-stu-id="8f6fe-155">Set the value for this member with the optional [LANGUAGE](./language-statement.md) resource definition statement.</span></span> <span data-ttu-id="8f6fe-156">I parametri sono costanti dal file Winnt. h.</span><span class="sxs-lookup"><span data-stu-id="8f6fe-156">The parameters are constants from the Winnt.h file.</span></span>

<span data-ttu-id="8f6fe-157">Ogni risorsa include un identificatore di lingua, in modo che il sistema o l'applicazione possa selezionare una lingua appropriata per le impostazioni locali correnti del sistema.</span><span class="sxs-lookup"><span data-stu-id="8f6fe-157">Each resource includes a language identifier so the system or application can select a language appropriate for the current locale of the system.</span></span> <span data-ttu-id="8f6fe-158">Se sono presenti più risorse dello stesso tipo e del nome che differiscono solo per la lingua delle stringhe all'interno delle risorse, è necessario specificare un **LanguageID** per ciascuna di esse.</span><span class="sxs-lookup"><span data-stu-id="8f6fe-158">If there are multiple resources of the same type and name that differ only in the language of the strings within the resources, you will need to specify a **LanguageId** for each one.</span></span>

</dd> <dt>

<span data-ttu-id="8f6fe-159">**Versione**</span><span class="sxs-lookup"><span data-stu-id="8f6fe-159">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="8f6fe-160">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="8f6fe-160">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="8f6fe-161">Numero di versione definito dall'utente per i dati della risorsa che gli strumenti possono usare per leggere e scrivere i file di risorse.</span><span class="sxs-lookup"><span data-stu-id="8f6fe-161">A user-defined version number for the resource data that tools can use to read and write resource files.</span></span> <span data-ttu-id="8f6fe-162">Impostare questo valore con l'istruzione facoltativa della definizione della risorsa della [versione](./version-statement.md) .</span><span class="sxs-lookup"><span data-stu-id="8f6fe-162">Set this value with the optional [VERSION](./version-statement.md) resource definition statement.</span></span>

</dd> <dt>

<span data-ttu-id="8f6fe-163">**Caratteristiche**</span><span class="sxs-lookup"><span data-stu-id="8f6fe-163">**Characteristics**</span></span>
</dt> <dd>

<span data-ttu-id="8f6fe-164">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="8f6fe-164">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="8f6fe-165">Specifica le informazioni definite dall'utente sulla risorsa che gli strumenti possono usare per leggere e scrivere i file di risorse.</span><span class="sxs-lookup"><span data-stu-id="8f6fe-165">Specifies user-defined information about the resource that tools can use to read and write resource files.</span></span> <span data-ttu-id="8f6fe-166">Impostare questo valore con l'istruzione di definizione di risorsa delle [caratteristiche](./characteristics-statement.md) facoltative.</span><span class="sxs-lookup"><span data-stu-id="8f6fe-166">Set this value with the optional [CHARACTERISTICS](./characteristics-statement.md) resource definition statement.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8f6fe-167">Commenti</span><span class="sxs-lookup"><span data-stu-id="8f6fe-167">Remarks</span></span>

<span data-ttu-id="8f6fe-168">Un membro del tipo di variabile è denominato membro di **nome** o **ordinale** e viene usato nella maggior parte delle posizioni nel file di risorse in cui viene visualizzato un identificatore.</span><span class="sxs-lookup"><span data-stu-id="8f6fe-168">A variable type member is called a **Name** or **Ordinal** member, and it is used in most places in the resource file where an identifier appears.</span></span> <span data-ttu-id="8f6fe-169">La prima **parola** di un membro di tipo **nome** o **ordinale** indica se il membro è un valore numerico o una stringa.</span><span class="sxs-lookup"><span data-stu-id="8f6fe-169">The first **WORD** of a **Name** or **Ordinal** type member indicates whether the member is a numeric value or a string.</span></span> <span data-ttu-id="8f6fe-170">Se la prima **parola** nel membro è uguale al valore 0xFFFF, che è un carattere Unicode non valido, la **parola** seguente è un numero di tipo.</span><span class="sxs-lookup"><span data-stu-id="8f6fe-170">If the first **WORD** in the member is equal to the value 0xffff, which is an invalid Unicode character, then the following **WORD** is a type number.</span></span> <span data-ttu-id="8f6fe-171">In caso contrario, il membro contiene una stringa Unicode e la prima **parola** nel membro è il primo carattere nella stringa del nome.</span><span class="sxs-lookup"><span data-stu-id="8f6fe-171">Otherwise, the member contains a Unicode string and the first **WORD** in the member is the first character in the name string.</span></span> <span data-ttu-id="8f6fe-172">Per ulteriori informazioni sulle istruzioni di definizione di risorsa, vedere [istruzioni di definizione di risorse](./resource-definition-statements.md).</span><span class="sxs-lookup"><span data-stu-id="8f6fe-172">For additional information about resource definition statements, see [Resource-Definition Statements](./resource-definition-statements.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8f6fe-173">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8f6fe-173">Requirements</span></span>



| <span data-ttu-id="8f6fe-174">Requisito</span><span class="sxs-lookup"><span data-stu-id="8f6fe-174">Requirement</span></span> | <span data-ttu-id="8f6fe-175">Valore</span><span class="sxs-lookup"><span data-stu-id="8f6fe-175">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="8f6fe-176">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8f6fe-176">Minimum supported client</span></span><br/> | <span data-ttu-id="8f6fe-177">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="8f6fe-177">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="8f6fe-178">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8f6fe-178">Minimum supported server</span></span><br/> | <span data-ttu-id="8f6fe-179">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="8f6fe-179">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="8f6fe-180">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8f6fe-180">See also</span></span>

<dl> <dt>

<span data-ttu-id="8f6fe-181">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="8f6fe-181">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="8f6fe-182">Risorse</span><span class="sxs-lookup"><span data-stu-id="8f6fe-182">Resources</span></span>](resources.md)
</dt> <dt>

<span data-ttu-id="8f6fe-183">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="8f6fe-183">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="8f6fe-184">Caratteristiche (istruzione)</span><span class="sxs-lookup"><span data-stu-id="8f6fe-184">CHARACTERISTICS Statement</span></span>](./characteristics-statement.md)
</dt> <dt>

[<span data-ttu-id="8f6fe-185">LANGUAGE (istruzione)</span><span class="sxs-lookup"><span data-stu-id="8f6fe-185">LANGUAGE Statement</span></span>](./language-statement.md)
</dt> <dt>

[<span data-ttu-id="8f6fe-186">Istruzione VERSION</span><span class="sxs-lookup"><span data-stu-id="8f6fe-186">VERSION Statement</span></span>](./version-statement.md)
</dt> </dl>

 

