---
description: La tabella della classe contiene informazioni relative al server COM che devono essere generate come parte dell'annuncio del prodotto. Ogni riga può generare un set di chiavi e valori del registro di sistema. Le informazioni sul ProgId associate sono incluse in questa tabella.
ms.assetid: 0fa00a3f-2a5d-411d-9fc6-9486a600f018
title: Tabella classi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29e7584fcb0440b8754179d8e274158cc64e3b74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310982"
---
# <a name="class-table"></a><span data-ttu-id="194d1-105">Tabella classi</span><span class="sxs-lookup"><span data-stu-id="194d1-105">Class Table</span></span>

<span data-ttu-id="194d1-106">La tabella della classe contiene informazioni relative al server COM che devono essere generate come parte dell'annuncio del prodotto.</span><span class="sxs-lookup"><span data-stu-id="194d1-106">The Class table contains COM server-related information that must be generated as a part of the product advertisement.</span></span> <span data-ttu-id="194d1-107">Ogni riga può generare un set di chiavi e valori del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="194d1-107">Each row may generate a set of registry keys and values.</span></span> <span data-ttu-id="194d1-108">Le informazioni sul ProgId associate sono incluse in questa tabella.</span><span class="sxs-lookup"><span data-stu-id="194d1-108">The associated ProgId information is included in this table.</span></span>

<span data-ttu-id="194d1-109">La tabella della classe contiene le colonne seguenti.</span><span class="sxs-lookup"><span data-stu-id="194d1-109">The Class table has the following columns.</span></span>



| <span data-ttu-id="194d1-110">Colonna</span><span class="sxs-lookup"><span data-stu-id="194d1-110">Column</span></span>           | <span data-ttu-id="194d1-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="194d1-111">Type</span></span>                         | <span data-ttu-id="194d1-112">Chiave</span><span class="sxs-lookup"><span data-stu-id="194d1-112">Key</span></span> | <span data-ttu-id="194d1-113">Nullable</span><span class="sxs-lookup"><span data-stu-id="194d1-113">Nullable</span></span> |
|------------------|------------------------------|-----|----------|
| <span data-ttu-id="194d1-114">CLSID</span><span class="sxs-lookup"><span data-stu-id="194d1-114">CLSID</span></span>            | [<span data-ttu-id="194d1-115">GUID</span><span class="sxs-lookup"><span data-stu-id="194d1-115">GUID</span></span>](guid.md)             | <span data-ttu-id="194d1-116">S</span><span class="sxs-lookup"><span data-stu-id="194d1-116">Y</span></span>   | <span data-ttu-id="194d1-117">N</span><span class="sxs-lookup"><span data-stu-id="194d1-117">N</span></span>        |
| <span data-ttu-id="194d1-118">Context</span><span class="sxs-lookup"><span data-stu-id="194d1-118">Context</span></span>          | [<span data-ttu-id="194d1-119">Identificatore</span><span class="sxs-lookup"><span data-stu-id="194d1-119">Identifier</span></span>](identifier.md) | <span data-ttu-id="194d1-120">S</span><span class="sxs-lookup"><span data-stu-id="194d1-120">Y</span></span>   | <span data-ttu-id="194d1-121">N</span><span class="sxs-lookup"><span data-stu-id="194d1-121">N</span></span>        |
| <span data-ttu-id="194d1-122">Componente\_</span><span class="sxs-lookup"><span data-stu-id="194d1-122">Component\_</span></span>      | [<span data-ttu-id="194d1-123">Identificatore</span><span class="sxs-lookup"><span data-stu-id="194d1-123">Identifier</span></span>](identifier.md) | <span data-ttu-id="194d1-124">S</span><span class="sxs-lookup"><span data-stu-id="194d1-124">Y</span></span>   | <span data-ttu-id="194d1-125">N</span><span class="sxs-lookup"><span data-stu-id="194d1-125">N</span></span>        |
| <span data-ttu-id="194d1-126">\_Valore predefinito ProgID</span><span class="sxs-lookup"><span data-stu-id="194d1-126">ProgId\_Default</span></span>  | [<span data-ttu-id="194d1-127">Text</span><span class="sxs-lookup"><span data-stu-id="194d1-127">Text</span></span>](text.md)             | <span data-ttu-id="194d1-128">N</span><span class="sxs-lookup"><span data-stu-id="194d1-128">N</span></span>   | <span data-ttu-id="194d1-129">S</span><span class="sxs-lookup"><span data-stu-id="194d1-129">Y</span></span>        |
| <span data-ttu-id="194d1-130">Descrizione</span><span class="sxs-lookup"><span data-stu-id="194d1-130">Description</span></span>      | [<span data-ttu-id="194d1-131">Text</span><span class="sxs-lookup"><span data-stu-id="194d1-131">Text</span></span>](text.md)             | <span data-ttu-id="194d1-132">N</span><span class="sxs-lookup"><span data-stu-id="194d1-132">N</span></span>   | <span data-ttu-id="194d1-133">S</span><span class="sxs-lookup"><span data-stu-id="194d1-133">Y</span></span>        |
| <span data-ttu-id="194d1-134">AppId\_</span><span class="sxs-lookup"><span data-stu-id="194d1-134">AppId\_</span></span>          | [<span data-ttu-id="194d1-135">GUID</span><span class="sxs-lookup"><span data-stu-id="194d1-135">GUID</span></span>](guid.md)             | <span data-ttu-id="194d1-136">N</span><span class="sxs-lookup"><span data-stu-id="194d1-136">N</span></span>   | <span data-ttu-id="194d1-137">S</span><span class="sxs-lookup"><span data-stu-id="194d1-137">Y</span></span>        |
| <span data-ttu-id="194d1-138">FileTypeMask</span><span class="sxs-lookup"><span data-stu-id="194d1-138">FileTypeMask</span></span>     | [<span data-ttu-id="194d1-139">Text</span><span class="sxs-lookup"><span data-stu-id="194d1-139">Text</span></span>](text.md)             | <span data-ttu-id="194d1-140">N</span><span class="sxs-lookup"><span data-stu-id="194d1-140">N</span></span>   | <span data-ttu-id="194d1-141">S</span><span class="sxs-lookup"><span data-stu-id="194d1-141">Y</span></span>        |
| <span data-ttu-id="194d1-142">Icona\_</span><span class="sxs-lookup"><span data-stu-id="194d1-142">Icon\_</span></span>           | [<span data-ttu-id="194d1-143">Identificatore</span><span class="sxs-lookup"><span data-stu-id="194d1-143">Identifier</span></span>](identifier.md) | <span data-ttu-id="194d1-144">N</span><span class="sxs-lookup"><span data-stu-id="194d1-144">N</span></span>   | <span data-ttu-id="194d1-145">S</span><span class="sxs-lookup"><span data-stu-id="194d1-145">Y</span></span>        |
| <span data-ttu-id="194d1-146">IconIndex</span><span class="sxs-lookup"><span data-stu-id="194d1-146">IconIndex</span></span>        | [<span data-ttu-id="194d1-147">Integer</span><span class="sxs-lookup"><span data-stu-id="194d1-147">Integer</span></span>](integer.md)       | <span data-ttu-id="194d1-148">N</span><span class="sxs-lookup"><span data-stu-id="194d1-148">N</span></span>   | <span data-ttu-id="194d1-149">S</span><span class="sxs-lookup"><span data-stu-id="194d1-149">Y</span></span>        |
| <span data-ttu-id="194d1-150">DefInprocHandler</span><span class="sxs-lookup"><span data-stu-id="194d1-150">DefInprocHandler</span></span> | [<span data-ttu-id="194d1-151">Filename</span><span class="sxs-lookup"><span data-stu-id="194d1-151">Filename</span></span>](filename.md)     | <span data-ttu-id="194d1-152">N</span><span class="sxs-lookup"><span data-stu-id="194d1-152">N</span></span>   | <span data-ttu-id="194d1-153">S</span><span class="sxs-lookup"><span data-stu-id="194d1-153">Y</span></span>        |
| <span data-ttu-id="194d1-154">Argomento</span><span class="sxs-lookup"><span data-stu-id="194d1-154">Argument</span></span>         | [<span data-ttu-id="194d1-155">Formattato</span><span class="sxs-lookup"><span data-stu-id="194d1-155">Formatted</span></span>](formatted.md)   | <span data-ttu-id="194d1-156">N</span><span class="sxs-lookup"><span data-stu-id="194d1-156">N</span></span>   | <span data-ttu-id="194d1-157">S</span><span class="sxs-lookup"><span data-stu-id="194d1-157">Y</span></span>        |
| <span data-ttu-id="194d1-158">Funzionalità\_</span><span class="sxs-lookup"><span data-stu-id="194d1-158">Feature\_</span></span>        | [<span data-ttu-id="194d1-159">Identificatore</span><span class="sxs-lookup"><span data-stu-id="194d1-159">Identifier</span></span>](identifier.md) | <span data-ttu-id="194d1-160">N</span><span class="sxs-lookup"><span data-stu-id="194d1-160">N</span></span>   | <span data-ttu-id="194d1-161">N</span><span class="sxs-lookup"><span data-stu-id="194d1-161">N</span></span>        |
| <span data-ttu-id="194d1-162">Attributi</span><span class="sxs-lookup"><span data-stu-id="194d1-162">Attributes</span></span>       | [<span data-ttu-id="194d1-163">Integer</span><span class="sxs-lookup"><span data-stu-id="194d1-163">Integer</span></span>](integer.md)       | <span data-ttu-id="194d1-164">N</span><span class="sxs-lookup"><span data-stu-id="194d1-164">N</span></span>   | <span data-ttu-id="194d1-165">S</span><span class="sxs-lookup"><span data-stu-id="194d1-165">Y</span></span>        |



 

## <a name="column-information"></a><span data-ttu-id="194d1-166">Informazioni sulle colonne</span><span class="sxs-lookup"><span data-stu-id="194d1-166">Column Information</span></span>

<dl> <dt>

<span data-ttu-id="194d1-167"><span id="CLSID"></span><span id="clsid"></span>CLSID</span><span class="sxs-lookup"><span data-stu-id="194d1-167"><span id="CLSID"></span><span id="clsid"></span>CLSID</span></span>
</dt> <dd>

<span data-ttu-id="194d1-168">Identificatore di classe (ID) di un server COM.</span><span class="sxs-lookup"><span data-stu-id="194d1-168">The Class identifier (ID) of a COM server.</span></span>

</dd> <dt>

<span data-ttu-id="194d1-169"><span id="Context"></span><span id="context"></span><span id="CONTEXT"></span>Contesto</span><span class="sxs-lookup"><span data-stu-id="194d1-169"><span id="Context"></span><span id="context"></span><span id="CONTEXT"></span>Context</span></span>
</dt> <dd>

<span data-ttu-id="194d1-170">Contesto server per questo server.</span><span class="sxs-lookup"><span data-stu-id="194d1-170">The server context for this server.</span></span> <span data-ttu-id="194d1-171">Immettere uno dei valori seguenti per la chiave CLSID.</span><span class="sxs-lookup"><span data-stu-id="194d1-171">Enter one of the following values for the CLSID Key.</span></span>



| <span data-ttu-id="194d1-172">CHIAVE CLSID</span><span class="sxs-lookup"><span data-stu-id="194d1-172">CLSID KEY</span></span>                             | <span data-ttu-id="194d1-173">Descrizione</span><span class="sxs-lookup"><span data-stu-id="194d1-173">Description</span></span>                                                               |
|---------------------------------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="194d1-174">LocalServer</span><span class="sxs-lookup"><span data-stu-id="194d1-174">LocalServer</span></span>](../com/localserver.md)       | <span data-ttu-id="194d1-175">Specifica il percorso completo di un'applicazione server locale a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="194d1-175">Specifies the full path to a 16-bit local server application.</span></span>             |
| [<span data-ttu-id="194d1-176">LocalServer32</span><span class="sxs-lookup"><span data-stu-id="194d1-176">LocalServer32</span></span>](../com/localserver32.md)   | <span data-ttu-id="194d1-177">Specifica il percorso completo di un'applicazione server locale a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="194d1-177">Specifies the full path to a 32-bit local server application.</span></span>             |
| [<span data-ttu-id="194d1-178">InprocServer</span><span class="sxs-lookup"><span data-stu-id="194d1-178">InprocServer</span></span>](../com/inprocserver.md)     | <span data-ttu-id="194d1-179">Specifica il percorso di una DLL del server in-process.</span><span class="sxs-lookup"><span data-stu-id="194d1-179">Specifies the path to an in-process server DLL.</span></span>                           |
| [<span data-ttu-id="194d1-180">InprocServer32</span><span class="sxs-lookup"><span data-stu-id="194d1-180">InprocServer32</span></span>](../com/inprocserver32.md) | <span data-ttu-id="194d1-181">Specifica il percorso di un server in-process a 32 bit e il modello di Threading.</span><span class="sxs-lookup"><span data-stu-id="194d1-181">Specifies the path to a 32-bit in-process server and the threading model.</span></span> |



 

</dd> <dt>

<span data-ttu-id="194d1-182"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_</span><span class="sxs-lookup"><span data-stu-id="194d1-182"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="194d1-183">Chiave esterna nella [tabella dei componenti](component-table.md) che specifica il componente il cui file di chiave fornisce il server com.</span><span class="sxs-lookup"><span data-stu-id="194d1-183">External key into the [Component table](component-table.md) specifying the component whose key file provides the COM server.</span></span>

</dd> <dt>

<span data-ttu-id="194d1-184"><span id="ProgId_Default"></span><span id="progid_default"></span><span id="PROGID_DEFAULT"></span>\_Valore predefinito ProgID</span><span class="sxs-lookup"><span data-stu-id="194d1-184"><span id="ProgId_Default"></span><span id="progid_default"></span><span id="PROGID_DEFAULT"></span>ProgId\_Default</span></span>
</dt> <dd>

<span data-ttu-id="194d1-185">ID di programma predefinito associato a questo ID di classe.</span><span class="sxs-lookup"><span data-stu-id="194d1-185">The default Program ID associated with this Class ID.</span></span> <span data-ttu-id="194d1-186">Questa colonna è una chiave esterna nella [tabella ProgId](progid-table.md).</span><span class="sxs-lookup"><span data-stu-id="194d1-186">This column is a foreign key into the [ProgID table](progid-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="194d1-187"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descrizione</span><span class="sxs-lookup"><span data-stu-id="194d1-187"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="194d1-188">Descrizione localizzata associata all'ID della classe e all'ID del programma.</span><span class="sxs-lookup"><span data-stu-id="194d1-188">Localized description associated with the Class ID and Program ID.</span></span>

</dd> <dt>

<span data-ttu-id="194d1-189"><span id="AppId_"></span><span id="appid_"></span><span id="APPID_"></span>AppId\_</span><span class="sxs-lookup"><span data-stu-id="194d1-189"><span id="AppId_"></span><span id="appid_"></span><span id="APPID_"></span>AppId\_</span></span>
</dt> <dd>

<span data-ttu-id="194d1-190">ID applicazione contenente le informazioni DCOM per l'applicazione associata ( [GUID](guid.md)della stringa).</span><span class="sxs-lookup"><span data-stu-id="194d1-190">Application ID containing DCOM information for the associated application (string [GUID](guid.md)).</span></span> <span data-ttu-id="194d1-191">Questa colonna è una chiave esterna nella [tabella AppID](appid-table.md).</span><span class="sxs-lookup"><span data-stu-id="194d1-191">This column is a foreign key into the [AppId table](appid-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="194d1-192"><span id="FileTypeMask"></span><span id="filetypemask"></span><span id="FILETYPEMASK"></span>FileTypeMask</span><span class="sxs-lookup"><span data-stu-id="194d1-192"><span id="FileTypeMask"></span><span id="filetypemask"></span><span id="FILETYPEMASK"></span>FileTypeMask</span></span>
</dt> <dd>

<span data-ttu-id="194d1-193">Contiene informazioni per la chiave HKCR (questo CLSID).</span><span class="sxs-lookup"><span data-stu-id="194d1-193">Contains information for the HKCR (this CLSID) key.</span></span>

<span data-ttu-id="194d1-194">Se esistono più modelli, questi devono essere delimitati da un punto e virgola e vengono generate sottochiavi numeriche: 0, 1, 2... Per ulteriori informazioni su questa funzionalità, vedere [**GetClassFile**](/windows/win32/api/objbase/nf-objbase-getclassfile).</span><span class="sxs-lookup"><span data-stu-id="194d1-194">If multiple patterns exist, they must be delimited by a semicolon, and numeric subkeys are generated: 0, 1, 2... For more information about this functionality, see [**GetClassFile**](/windows/win32/api/objbase/nf-objbase-getclassfile).</span></span>

</dd> <dt>

<span data-ttu-id="194d1-195"><span id="Icon_"></span><span id="icon_"></span><span id="ICON_"></span>Icona\_</span><span class="sxs-lookup"><span data-stu-id="194d1-195"><span id="Icon_"></span><span id="icon_"></span><span id="ICON_"></span>Icon\_</span></span>
</dt> <dd>

<span data-ttu-id="194d1-196">Il file che fornisce l'icona associata a questo CLSID.</span><span class="sxs-lookup"><span data-stu-id="194d1-196">The file providing the icon associated with this CLSID.</span></span> <span data-ttu-id="194d1-197">Il programma di installazione scrive la voce in questa colonna sotto la chiave DefaultIcon associata a ProgId.</span><span class="sxs-lookup"><span data-stu-id="194d1-197">The installer writes the entry in this column under the DefaultIcon key associated with the ProgId.</span></span> <span data-ttu-id="194d1-198">Se non è null, la colonna è una chiave esterna nella tabella delle [Icone](icon-table.md).</span><span class="sxs-lookup"><span data-stu-id="194d1-198">If it is not null, the column is a foreign key into the [Icon table](icon-table.md).</span></span> <span data-ttu-id="194d1-199">Se è null, il server COM fornisce la risorsa icona.</span><span class="sxs-lookup"><span data-stu-id="194d1-199">If it is null, the COM server provides the icon resource.</span></span> <span data-ttu-id="194d1-200">Le associazioni di file annunciati e i collegamenti richiedono un valore non null in questa colonna per la visualizzazione corretta.</span><span class="sxs-lookup"><span data-stu-id="194d1-200">Advertised file associations and shortcuts require a non-null value in this column to display properly.</span></span>

</dd> <dt>

<span data-ttu-id="194d1-201"><span id="IconIndex"></span><span id="iconindex"></span><span id="ICONINDEX"></span>IconIndex</span><span class="sxs-lookup"><span data-stu-id="194d1-201"><span id="IconIndex"></span><span id="iconindex"></span><span id="ICONINDEX"></span>IconIndex</span></span>
</dt> <dd>

<span data-ttu-id="194d1-202">Icona index nel file icona.</span><span class="sxs-lookup"><span data-stu-id="194d1-202">Icon index into the icon file.</span></span> <span data-ttu-id="194d1-203">Può essere Null.</span><span class="sxs-lookup"><span data-stu-id="194d1-203">This can be null.</span></span>

<span data-ttu-id="194d1-204">Solo numeri non negativi.</span><span class="sxs-lookup"><span data-stu-id="194d1-204">Non-negative numbers only.</span></span>

</dd> <dt>

<span data-ttu-id="194d1-205"><span id="DefInprocHandler"></span><span id="definprochandler"></span><span id="DEFINPROCHANDLER"></span>DefInprocHandler</span><span class="sxs-lookup"><span data-stu-id="194d1-205"><span id="DefInprocHandler"></span><span id="definprochandler"></span><span id="DEFINPROCHANDLER"></span>DefInprocHandler</span></span>
</dt> <dd>

<span data-ttu-id="194d1-206">Questo campo specifica il gestore predefinito in-process per il contesto server specificato nel campo di contesto.</span><span class="sxs-lookup"><span data-stu-id="194d1-206">This field specifies the default in-process handler for the server context specified in the Context field.</span></span>

<span data-ttu-id="194d1-207">Questo campo deve essere null se nel campo di contesto viene visualizzata una chiave CLSID InprocServer o InprocServer.</span><span class="sxs-lookup"><span data-stu-id="194d1-207">This field must be Null if an InprocServer or InprocServer CLSID key appears in the Context field.</span></span>

<span data-ttu-id="194d1-208">Se viene visualizzata una chiave CLSID LocalServer o LocalServer32 nel campo contesto, il valore nel campo DefInprocHandler identifica il gestore predefinito in-process.</span><span class="sxs-lookup"><span data-stu-id="194d1-208">If a LocalServer or LocalServer32 CLSID key appears in the Context field, the value in the DefInprocHandler field identifies the default in-process handler.</span></span>



| <span data-ttu-id="194d1-209">Valore</span><span class="sxs-lookup"><span data-stu-id="194d1-209">Value</span></span>                | <span data-ttu-id="194d1-210">Descrizione</span><span class="sxs-lookup"><span data-stu-id="194d1-210">Description</span></span>                                                                                                                                                                                                                                                                       |
|----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="194d1-211">valore non numerico</span><span class="sxs-lookup"><span data-stu-id="194d1-211">non-numeric value</span></span>    | <span data-ttu-id="194d1-212">Il programma di installazione considera un valore non numerico nel campo DefInprocHandler come un file di sistema che funge da gestore in-process a 32 bit specificato dalla chiave InprocHandler32.</span><span class="sxs-lookup"><span data-stu-id="194d1-212">The installer treats a non-numeric value in the DefInprocHandler field as a system file serving as the 32-bit in-process handler specified by the InprocHandler32 key.</span></span>                                                                                                            |
| <span data-ttu-id="194d1-213">Null</span><span class="sxs-lookup"><span data-stu-id="194d1-213">Null</span></span>                 | <span data-ttu-id="194d1-214">I campi DefInprocHandler e argument possono essere entrambi null per una chiave CLSID LocalServer o LocalServer32.</span><span class="sxs-lookup"><span data-stu-id="194d1-214">The DefInprocHandler and Argument fields can both be Null for a LocalServer or LocalServer32 CLSID key.</span></span>                                                                                                                                                                           |
| <span data-ttu-id="194d1-215">1 = valore predefinito (sistema)</span><span class="sxs-lookup"><span data-stu-id="194d1-215">1 = default (system)</span></span> | <span data-ttu-id="194d1-216">Il valore predefinito è il gestore in-process a 16 bit specificato da InprocHandler.</span><span class="sxs-lookup"><span data-stu-id="194d1-216">The default is the 16-bit in-process handler specified by InprocHandler.</span></span> <span data-ttu-id="194d1-217">In questo caso, il valore di InprocHandler è il nome nel registro di sistema in cui è archiviato il valore del gestore predefinito in-process.</span><span class="sxs-lookup"><span data-stu-id="194d1-217">In this case, the value of InprocHandler is the name in the registry under which the value of the default in-process handler is stored.</span></span> <span data-ttu-id="194d1-218">Ad esempio, HKEY \_ \_ \\ le classi software del computer locale \\ \\ CLSID.</span><span class="sxs-lookup"><span data-stu-id="194d1-218">For example, HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes\\CLSID.</span></span>     |
| <span data-ttu-id="194d1-219">2 = valore predefinito (sistema)</span><span class="sxs-lookup"><span data-stu-id="194d1-219">2 = default (system)</span></span> | <span data-ttu-id="194d1-220">Il valore predefinito è il gestore in-process a 32 bit specificato da InprocHandler32.</span><span class="sxs-lookup"><span data-stu-id="194d1-220">The default is the 32-bit in-process handler specified by InprocHandler32.</span></span> <span data-ttu-id="194d1-221">In questo caso, il valore di InprocHandler32 è il nome nel registro di sistema in cui è archiviato il valore del gestore predefinito in-process.</span><span class="sxs-lookup"><span data-stu-id="194d1-221">In this case, the value of InprocHandler32 is the name in the registry under which the value of the default in-process handler is stored.</span></span> <span data-ttu-id="194d1-222">Ad esempio, HKEY \_ \_ \\ le classi software del computer locale \\ \\ CLSID.</span><span class="sxs-lookup"><span data-stu-id="194d1-222">For example, HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes\\CLSID.</span></span> |
| <span data-ttu-id="194d1-223">3 = valore predefinito (sistema)</span><span class="sxs-lookup"><span data-stu-id="194d1-223">3 = default (system)</span></span> | <span data-ttu-id="194d1-224">Il valore predefinito è un gestore in-process a 16 bit o a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="194d1-224">The default is a 16-bit or 32-bit in-process handler.</span></span>                                                                                                                                                                                                                             |



 

</dd> <dt>

<span data-ttu-id="194d1-225"><span id="Argument"></span><span id="argument"></span><span id="ARGUMENT"></span>Argomento</span><span class="sxs-lookup"><span data-stu-id="194d1-225"><span id="Argument"></span><span id="argument"></span><span id="ARGUMENT"></span>Argument</span></span>
</dt> <dd>

<span data-ttu-id="194d1-226">Se viene visualizzata una chiave CLSID LocalServer o LocalServer32 nel campo contesto, il testo in questo campo viene registrato come argomento nel server e viene utilizzato da COM per richiamare il server.</span><span class="sxs-lookup"><span data-stu-id="194d1-226">If a LocalServer or LocalServer32 CLSID key appears in the Context field, the text in this field is registered as the argument against the server and is used by COM to invoke the server.</span></span> <span data-ttu-id="194d1-227">I campi DefInprocHandler e argument possono essere entrambi null se LocalServer o LocalServer32 vengono visualizzati nel campo di contesto.</span><span class="sxs-lookup"><span data-stu-id="194d1-227">The DefInprocHandler and Argument fields can both be Null if LocalServer or LocalServer32 appears in the Context field.</span></span>

<span data-ttu-id="194d1-228">Si noti che la risoluzione delle proprietà nel campo argument è limitata.</span><span class="sxs-lookup"><span data-stu-id="194d1-228">Note that the resolution of properties in the Argument field is limited.</span></span> <span data-ttu-id="194d1-229">Una proprietà formattata come \[ proprietà \] in questo campo può essere risolta solo se la proprietà dispone già del valore previsto quando viene installato il componente proprietario della classe.</span><span class="sxs-lookup"><span data-stu-id="194d1-229">A property formatted as \[Property\] in this field can only be resolved if the property already has the intended value when the component owning the class is installed.</span></span> <span data-ttu-id="194d1-230">Per l'argomento "MyDoc.doc", ad esempio, per \[ \# \] risolvere il valore corretto, è necessario che lo stesso processo stia installando il file MyDoc.doc e il componente proprietario della classe.</span><span class="sxs-lookup"><span data-stu-id="194d1-230">For example, for the argument "\[\#MyDoc.doc\]" to resolve to the correct value, the same process must be installing the file MyDoc.doc and the component that owns the class.</span></span>

</dd> <dt>

<span data-ttu-id="194d1-231"><span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Funzionalità\_</span><span class="sxs-lookup"><span data-stu-id="194d1-231"><span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Feature\_</span></span>
</dt> <dd>

<span data-ttu-id="194d1-232">Chiave esterna nella [tabella delle funzionalità](feature-table.md) che specifica la funzionalità che fornisce il server com.</span><span class="sxs-lookup"><span data-stu-id="194d1-232">External key into the [Feature table](feature-table.md) specifying the feature that provides the COM server.</span></span>

<span data-ttu-id="194d1-233">Chiave esterna per la colonna uno della tabella delle funzionalità.</span><span class="sxs-lookup"><span data-stu-id="194d1-233">External key to column one of the Feature table.</span></span>

</dd> <dt>

<span data-ttu-id="194d1-234"><span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributi</span><span class="sxs-lookup"><span data-stu-id="194d1-234"><span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>
</dt> <dd>

<span data-ttu-id="194d1-235">Se in questa colonna è impostato **msidbClassAttributesRelativePath** , il nome del file Bare può essere utilizzato per i server com.</span><span class="sxs-lookup"><span data-stu-id="194d1-235">If **msidbClassAttributesRelativePath** is set in this column, the bare file name can be used for COM servers.</span></span> <span data-ttu-id="194d1-236">Il programma di installazione registra solo il nome del file anziché il percorso completo.</span><span class="sxs-lookup"><span data-stu-id="194d1-236">The installer registers the file name only instead of the complete path.</span></span> <span data-ttu-id="194d1-237">In questo modo il server nella directory corrente avrà la precedenza e consentirà più copie dello stesso componente.</span><span class="sxs-lookup"><span data-stu-id="194d1-237">This enables the server in the current directory to take precedence and allows multiple copies of the same component.</span></span>



| <span data-ttu-id="194d1-238">Attributo</span><span class="sxs-lookup"><span data-stu-id="194d1-238">Attribute</span></span>                            | <span data-ttu-id="194d1-239">Decimal</span><span class="sxs-lookup"><span data-stu-id="194d1-239">Decimal</span></span> | <span data-ttu-id="194d1-240">Valore esadecimale</span><span class="sxs-lookup"><span data-stu-id="194d1-240">Hexadecimal</span></span> |
|--------------------------------------|---------|-------------|
| <span data-ttu-id="194d1-241">**msidbClassAttributesRelativePath**</span><span class="sxs-lookup"><span data-stu-id="194d1-241">**msidbClassAttributesRelativePath**</span></span> | <span data-ttu-id="194d1-242">1</span><span class="sxs-lookup"><span data-stu-id="194d1-242">1</span></span>       | <span data-ttu-id="194d1-243">0x001</span><span class="sxs-lookup"><span data-stu-id="194d1-243">0x001</span></span>       |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="194d1-244">Commenti</span><span class="sxs-lookup"><span data-stu-id="194d1-244">Remarks</span></span>

<span data-ttu-id="194d1-245">Questa tabella viene definita quando viene eseguita l'azione [registerClassInfo](registerclassinfo-action.md) o [UnregisterClassInfo](unregisterclassinfo-action.md) .</span><span class="sxs-lookup"><span data-stu-id="194d1-245">This table is referred to when the [RegisterClassInfo action](registerclassinfo-action.md) or the [UnregisterClassInfo action](unregisterclassinfo-action.md) are executed.</span></span>

## <a name="validation"></a><span data-ttu-id="194d1-246">Convalida</span><span class="sxs-lookup"><span data-stu-id="194d1-246">Validation</span></span>

<dl>

[<span data-ttu-id="194d1-247">ICE03</span><span class="sxs-lookup"><span data-stu-id="194d1-247">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="194d1-248">ICE06</span><span class="sxs-lookup"><span data-stu-id="194d1-248">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="194d1-249">ICE19</span><span class="sxs-lookup"><span data-stu-id="194d1-249">ICE19</span></span>](ice19.md)  
[<span data-ttu-id="194d1-250">ICE32</span><span class="sxs-lookup"><span data-stu-id="194d1-250">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="194d1-251">ICE36</span><span class="sxs-lookup"><span data-stu-id="194d1-251">ICE36</span></span>](ice36.md)  
[<span data-ttu-id="194d1-252">ICE41</span><span class="sxs-lookup"><span data-stu-id="194d1-252">ICE41</span></span>](ice41.md)  
[<span data-ttu-id="194d1-253">ICE42</span><span class="sxs-lookup"><span data-stu-id="194d1-253">ICE42</span></span>](ice42.md)  
[<span data-ttu-id="194d1-254">ICE46</span><span class="sxs-lookup"><span data-stu-id="194d1-254">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="194d1-255">ICE66</span><span class="sxs-lookup"><span data-stu-id="194d1-255">ICE66</span></span>](ice66.md)  
[<span data-ttu-id="194d1-256">ICE69</span><span class="sxs-lookup"><span data-stu-id="194d1-256">ICE69</span></span>](ice69.md)  
</dl>

 

 
