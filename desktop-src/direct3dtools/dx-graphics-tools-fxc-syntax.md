---
title: Sintassi
description: Di seguito è illustrata la sintassi per chiamare FXC.exe, lo strumento compilatore di effetti. Per un esempio, vedere Compilazione offline.
ms.assetid: 3aee89bd-02e1-4de1-8552-ba36814f8464
keywords:
- FXC, sintassi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6241a728b4835b11d10ea6e39d67fd73a8576cd7
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/08/2020
ms.locfileid: "106300600"
---
# <a name="syntax"></a><span data-ttu-id="0ae45-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0ae45-105">Syntax</span></span>

<span data-ttu-id="0ae45-106">Di seguito è illustrata la sintassi per chiamare FXC.exe, lo strumento compilatore di effetti.</span><span class="sxs-lookup"><span data-stu-id="0ae45-106">Here is the syntax for calling FXC.exe, the effect-compiler tool.</span></span> <span data-ttu-id="0ae45-107">Per un esempio, vedere [compilazione offline](dx-graphics-tools-fxc-using.md).</span><span class="sxs-lookup"><span data-stu-id="0ae45-107">For an example, see [Offline Compiling](dx-graphics-tools-fxc-using.md).</span></span>

-   [<span data-ttu-id="0ae45-108">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="0ae45-108">Usage</span></span>](#usage)
-   [<span data-ttu-id="0ae45-109">Argomenti</span><span class="sxs-lookup"><span data-stu-id="0ae45-109">Arguments</span></span>](#arguments)
-   [<span data-ttu-id="0ae45-110">Osservazioni:</span><span class="sxs-lookup"><span data-stu-id="0ae45-110">Remarks</span></span>](#remarks)
-   [<span data-ttu-id="0ae45-111">Profili</span><span class="sxs-lookup"><span data-stu-id="0ae45-111">Profiles</span></span>](#profiles)
-   [<span data-ttu-id="0ae45-112">Note sulla versione</span><span class="sxs-lookup"><span data-stu-id="0ae45-112">Version notes</span></span>](#version-notes)
-   [<span data-ttu-id="0ae45-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0ae45-113">Related topics</span></span>](#related-topics)

## <a name="usage"></a><span data-ttu-id="0ae45-114">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="0ae45-114">Usage</span></span>

<span data-ttu-id="0ae45-115">*nomi file* *SwitchOptions* **FXC**</span><span class="sxs-lookup"><span data-stu-id="0ae45-115">**fxc** *SwitchOptions* *Filenames*</span></span>

## <a name="arguments"></a><span data-ttu-id="0ae45-116">Argomenti</span><span class="sxs-lookup"><span data-stu-id="0ae45-116">Arguments</span></span>
<span data-ttu-id="0ae45-117">Separare ogni opzione con uno spazio o un segno di due punti.</span><span class="sxs-lookup"><span data-stu-id="0ae45-117">Separate each switch option with a space or a colon.</span></span>

### <a name="switchoptions"></a><span data-ttu-id="0ae45-118">*SwitchOptions*</span><span class="sxs-lookup"><span data-stu-id="0ae45-118">*SwitchOptions*</span></span>
<span data-ttu-id="0ae45-119">\[in \] Opzioni di compilazione.</span><span class="sxs-lookup"><span data-stu-id="0ae45-119">\[in\] Compile options.</span></span> <span data-ttu-id="0ae45-120">È disponibile solo un'opzione obbligatoria e molte altre sono facoltative.</span><span class="sxs-lookup"><span data-stu-id="0ae45-120">There is just one required option, and many more that are optional.</span></span> <span data-ttu-id="0ae45-121">Separare ognuno con uno spazio o due punti.</span><span class="sxs-lookup"><span data-stu-id="0ae45-121">Separate each with a space or colon.</span></span>

#### <a name="required-option"></a><span data-ttu-id="0ae45-122">Opzione obbligatoria</span><span class="sxs-lookup"><span data-stu-id="0ae45-122">Required option</span></span>
##### <a name="t-profile"></a><span data-ttu-id="0ae45-123">/T <*profilo*></span><span class="sxs-lookup"><span data-stu-id="0ae45-123">/T <*profile*></span></span>
<span data-ttu-id="0ae45-124">Modello shader (vedere [profili](#profiles)).</span><span class="sxs-lookup"><span data-stu-id="0ae45-124">Shader model (see [Profiles](#profiles)).</span></span>

#### <a name="optional-options"></a><span data-ttu-id="0ae45-125">Opzioni facoltative</span><span class="sxs-lookup"><span data-stu-id="0ae45-125">Optional options</span></span>
##### <a name="-help"></a><span data-ttu-id="0ae45-126">/?, /help</span><span class="sxs-lookup"><span data-stu-id="0ae45-126">/?, /help</span></span>
<span data-ttu-id="0ae45-127">Stampa la guida per `FXC.exe` .</span><span class="sxs-lookup"><span data-stu-id="0ae45-127">Print help for `FXC.exe`.</span></span>

##### <a name="commandoptionfile"></a><span data-ttu-id="0ae45-128">@<*Command. Option. file*></span><span class="sxs-lookup"><span data-stu-id="0ae45-128">@<*command.option.file*></span></span>
<span data-ttu-id="0ae45-129">File che contiene altre opzioni di compilazione.</span><span class="sxs-lookup"><span data-stu-id="0ae45-129">File that contains additional compile options.</span></span> <span data-ttu-id="0ae45-130">Questa opzione può essere combinata con altre opzioni di compilazione della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="0ae45-130">This option can be mixed with other command line compile options.</span></span> <span data-ttu-id="0ae45-131">Il *comando. Option. file* deve contenere solo un'opzione per riga.</span><span class="sxs-lookup"><span data-stu-id="0ae45-131">The *command.option.file* must contain only one option per line.</span></span> <span data-ttu-id="0ae45-132">Il *comando. Option. file* non può contenere righe vuote.</span><span class="sxs-lookup"><span data-stu-id="0ae45-132">The *command.option.file* cannot contain any blank lines.</span></span> <span data-ttu-id="0ae45-133">Le opzioni specificate nel file non devono contenere spazi iniziali o finali.</span><span class="sxs-lookup"><span data-stu-id="0ae45-133">Options specified in the file must not contain any leading or trailing spaces.</span></span>

##### <a name="all_resources_bound"></a><span data-ttu-id="0ae45-134">/all_resources_bound</span><span class="sxs-lookup"><span data-stu-id="0ae45-134">/all_resources_bound</span></span>
<span data-ttu-id="0ae45-135">Abilitare la flatità aggressiva in SM 5.1 +.</span><span class="sxs-lookup"><span data-stu-id="0ae45-135">Enable aggressive flattening in SM5.1+.</span></span> <span data-ttu-id="0ae45-136">Novità per Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="0ae45-136">New for Direct3D 12.</span></span>

##### <a name="cc"></a><span data-ttu-id="0ae45-137">/CC</span><span class="sxs-lookup"><span data-stu-id="0ae45-137">/Cc</span></span>
<span data-ttu-id="0ae45-138">Colore di output: assembly codificato.</span><span class="sxs-lookup"><span data-stu-id="0ae45-138">Output color-coded assembly.</span></span>

##### <a name="compress"></a><span data-ttu-id="0ae45-139">/Compress</span><span class="sxs-lookup"><span data-stu-id="0ae45-139">/compress</span></span>
<span data-ttu-id="0ae45-140">Comprime il bytecode dello shader DX10 dai file.</span><span class="sxs-lookup"><span data-stu-id="0ae45-140">Compress DX10 shader bytecode from files.</span></span>

##### <a name="d-idtext"></a><span data-ttu-id="0ae45-141">/D < >=< *testo* ID></span><span class="sxs-lookup"><span data-stu-id="0ae45-141">/D <*id*>=<*text*></span></span>
<span data-ttu-id="0ae45-142">Definire la macro.</span><span class="sxs-lookup"><span data-stu-id="0ae45-142">Define macro.</span></span>

##### <a name="decompress"></a><span data-ttu-id="0ae45-143">/decompress</span><span class="sxs-lookup"><span data-stu-id="0ae45-143">/decompress</span></span>
<span data-ttu-id="0ae45-144">Decomprimere il bytecode dello shader DX10 dal primo file.</span><span class="sxs-lookup"><span data-stu-id="0ae45-144">Decompress DX10 shader bytecode from first file.</span></span> <span data-ttu-id="0ae45-145">I file di output devono essere elencati nell'ordine in cui si trovavano durante la compressione.</span><span class="sxs-lookup"><span data-stu-id="0ae45-145">Output files should be listed in the order they were in during compression.</span></span>

##### <a name="dumpbin"></a><span data-ttu-id="0ae45-146">/dumpbin</span><span class="sxs-lookup"><span data-stu-id="0ae45-146">/dumpbin</span></span>
<span data-ttu-id="0ae45-147">Carica un file binario anziché compilare uno shader.</span><span class="sxs-lookup"><span data-stu-id="0ae45-147">Loads a binary file rather than compiling a shader.</span></span>

##### <a name="e-name"></a><span data-ttu-id="0ae45-148">/E <name></span><span class="sxs-lookup"><span data-stu-id="0ae45-148">/E <name></span></span>
<span data-ttu-id="0ae45-149">Punto di ingresso dello shader.</span><span class="sxs-lookup"><span data-stu-id="0ae45-149">Shader entry point.</span></span> <span data-ttu-id="0ae45-150">Se non viene specificato alcun punto di ingresso, **Main** viene considerato il nome della voce dello shader.</span><span class="sxs-lookup"><span data-stu-id="0ae45-150">If no entry point is given, **main** is considered to be the shader entry name.</span></span>

##### <a name="enable_unbounded_descriptor_tables"></a><span data-ttu-id="0ae45-151">/enable_unbounded_descriptor_tables</span><span class="sxs-lookup"><span data-stu-id="0ae45-151">/enable_unbounded_descriptor_tables</span></span>
<span data-ttu-id="0ae45-152">Abilita le tabelle dei descrittori non vincolate.</span><span class="sxs-lookup"><span data-stu-id="0ae45-152">Enables unbounded descriptor tables.</span></span> <span data-ttu-id="0ae45-153">Novità per Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="0ae45-153">New for Direct3D 12.</span></span>

##### <a name="extractrootsignature-file"></a><span data-ttu-id="0ae45-154">*file* </extractrootsignature></span><span class="sxs-lookup"><span data-stu-id="0ae45-154">/extractrootsignature <*file*></span></span>
<span data-ttu-id="0ae45-155">Estrae la firma radice dal bytecode dello shader.</span><span class="sxs-lookup"><span data-stu-id="0ae45-155">Extract root signature from shader bytecode.</span></span> <span data-ttu-id="0ae45-156">Novità per Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="0ae45-156">New for Direct3D 12.</span></span>

##### <a name="fc-file"></a><span data-ttu-id="0ae45-157">*File* </FC></span><span class="sxs-lookup"><span data-stu-id="0ae45-157">/Fc <*file*></span></span>
<span data-ttu-id="0ae45-158">File di listato di codice dell'assembly di output.</span><span class="sxs-lookup"><span data-stu-id="0ae45-158">Output assembly code listing file.</span></span>

##### <a name="fd-file"></a><span data-ttu-id="0ae45-159">*File* </FD></span><span class="sxs-lookup"><span data-stu-id="0ae45-159">/Fd <*file*></span></span>
<span data-ttu-id="0ae45-160">Estrae le informazioni del database di programma shader (PDB) e scrive nel file specificato. Quando si compila lo shader, usare/FD per generare un file PDB con le informazioni di debug dello shader.</span><span class="sxs-lookup"><span data-stu-id="0ae45-160">Extract shader program database (PDB) info and write to the given file.When you compile the shader, use /Fd to generate a PDB file with shader debugging info.</span></span>

##### <a name="fe-file"></a><span data-ttu-id="0ae45-161">*File* </Fe></span><span class="sxs-lookup"><span data-stu-id="0ae45-161">/Fe <*file*></span></span>
<span data-ttu-id="0ae45-162">Genera avvisi ed errori nel file specificato.</span><span class="sxs-lookup"><span data-stu-id="0ae45-162">Output warnings and errors to the given file.</span></span>

##### <a name="fh-file"></a><span data-ttu-id="0ae45-163">*File* </FH></span><span class="sxs-lookup"><span data-stu-id="0ae45-163">/Fh <*file*></span></span>
<span data-ttu-id="0ae45-164">File di intestazione di output contenente il codice oggetto.</span><span class="sxs-lookup"><span data-stu-id="0ae45-164">Output header file containing object code.</span></span>

##### <a name="fl-file"></a><span data-ttu-id="0ae45-165">*File* </FL</span><span class="sxs-lookup"><span data-stu-id="0ae45-165">/Fl <*file*</span></span>
<span data-ttu-id="0ae45-166">Output di una libreria.</span><span class="sxs-lookup"><span data-stu-id="0ae45-166">Output a library.</span></span> <span data-ttu-id="0ae45-167">Richiede la \_47.dll D3dcompiler o una versione successiva della dll.</span><span class="sxs-lookup"><span data-stu-id="0ae45-167">Requires the D3dcompiler\_47.dll or a later version of the DLL.</span></span>

##### <a name="fo-file"></a><span data-ttu-id="0ae45-168">*File* </fo></span><span class="sxs-lookup"><span data-stu-id="0ae45-168">/Fo <*file*></span></span>
<span data-ttu-id="0ae45-169">File oggetto di output.</span><span class="sxs-lookup"><span data-stu-id="0ae45-169">Output object file.</span></span> <span data-ttu-id="0ae45-170">Spesso è stata assegnata l'estensione &quot; . fxc &quot; , anche se vengono usate altre estensioni, ad esempio &quot; . o &quot; , &quot; . obj &quot; o &quot; . dxbc &quot; .</span><span class="sxs-lookup"><span data-stu-id="0ae45-170">Often given the extension &quot;.fxc&quot;, though other extensions are used, such as &quot;.o&quot;, &quot;.obj&quot; or &quot;.dxbc&quot;.</span></span>

##### <a name="fx-file"></a><span data-ttu-id="0ae45-171">*File* </FX></span><span class="sxs-lookup"><span data-stu-id="0ae45-171">/Fx <*file*></span></span>
<span data-ttu-id="0ae45-172">Codice dell'assembly di output e file di elenco esadecimale.</span><span class="sxs-lookup"><span data-stu-id="0ae45-172">Output assembly code and hex listing file.</span></span>

##### <a name="gch"></a><span data-ttu-id="0ae45-173">/Gch</span><span class="sxs-lookup"><span data-stu-id="0ae45-173">/Gch</span></span>
<span data-ttu-id="0ae45-174">Compilare come effetto figlio per i profili di fx_4_x.</span><span class="sxs-lookup"><span data-stu-id="0ae45-174">Compile as a child effect for fx_4_x profiles.</span></span>

> [!NOTE]
> <span data-ttu-id="0ae45-175">Il supporto per i profili degli effetti legacy è deprecato.</span><span class="sxs-lookup"><span data-stu-id="0ae45-175">Support for legacy Effects profiles is deprecated.</span></span>

##### <a name="gdp"></a><span data-ttu-id="0ae45-176">/Gdp</span><span class="sxs-lookup"><span data-stu-id="0ae45-176">/Gdp</span></span>
<span data-ttu-id="0ae45-177">Disabilitare la modalità prestazioni effetto.</span><span class="sxs-lookup"><span data-stu-id="0ae45-177">Disable effect performance mode.</span></span>

##### <a name="gec"></a><span data-ttu-id="0ae45-178">/Gec</span><span class="sxs-lookup"><span data-stu-id="0ae45-178">/Gec</span></span>
<span data-ttu-id="0ae45-179">Abilitare la modalità di compatibilità con le versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="0ae45-179">Enable backward compatibility mode.</span></span>

##### <a name="ges"></a><span data-ttu-id="0ae45-180">/Ges</span><span class="sxs-lookup"><span data-stu-id="0ae45-180">/Ges</span></span>
<span data-ttu-id="0ae45-181">Abilitare la modalità Strict.</span><span class="sxs-lookup"><span data-stu-id="0ae45-181">Enable strict mode.</span></span>

##### <a name="getprivate-file"></a><span data-ttu-id="0ae45-182">*file* </getprivate></span><span class="sxs-lookup"><span data-stu-id="0ae45-182">/getprivate <*file*></span></span>
<span data-ttu-id="0ae45-183">Salvare i dati privati dal BLOB dello shader (Binary shader compilato) al file specificato.</span><span class="sxs-lookup"><span data-stu-id="0ae45-183">Save private data from the shader blob (compiled shader binary) to the given file.</span></span> <span data-ttu-id="0ae45-184">Estrae i dati privati, incorporati in precedenza da/SetPrivate, dal BLOB dello shader.</span><span class="sxs-lookup"><span data-stu-id="0ae45-184">Extracts private data, previously embedded by /setprivate, from the shader blob.</span></span>

<span data-ttu-id="0ae45-185">È necessario specificare l'opzione/DUMPBIN con/getprivate.</span><span class="sxs-lookup"><span data-stu-id="0ae45-185">You must specify the /dumpbin option with /getprivate.</span></span> <span data-ttu-id="0ae45-186">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="0ae45-186">For example:</span></span>

```console
fxc /getprivate ps01.private.data 
    /dumpbin ps01.with.private.obj
```
    
##### <a name="gfa"></a><span data-ttu-id="0ae45-187">/Gfa</span><span class="sxs-lookup"><span data-stu-id="0ae45-187">/Gfa</span></span>
<span data-ttu-id="0ae45-188">Evitare costrutti di controllo di flusso.</span><span class="sxs-lookup"><span data-stu-id="0ae45-188">Avoid flow control constructs.</span></span>

##### <a name="gfp"></a><span data-ttu-id="0ae45-189">/GFP</span><span class="sxs-lookup"><span data-stu-id="0ae45-189">/Gfp</span></span>
<span data-ttu-id="0ae45-190">Preferisce i costrutti di controllo di flusso.</span><span class="sxs-lookup"><span data-stu-id="0ae45-190">Prefer flow control constructs.</span></span>

##### <a name="gis"></a><span data-ttu-id="0ae45-191">/Gis</span><span class="sxs-lookup"><span data-stu-id="0ae45-191">/Gis</span></span>
<span data-ttu-id="0ae45-192">Forza la rigidità IEEE.</span><span class="sxs-lookup"><span data-stu-id="0ae45-192">Force IEEE strictness.</span></span>

##### <a name="gpp"></a><span data-ttu-id="0ae45-193">/Gpp</span><span class="sxs-lookup"><span data-stu-id="0ae45-193">/Gpp</span></span>
<span data-ttu-id="0ae45-194">Forza la precisione parziale.</span><span class="sxs-lookup"><span data-stu-id="0ae45-194">Force partial precision.</span></span>
    
##### <a name="i-include"></a><span data-ttu-id="0ae45-195">/I <*includere*></span><span class="sxs-lookup"><span data-stu-id="0ae45-195">/I <*include*></span></span>
<span data-ttu-id="0ae45-196">Percorso di inclusione aggiuntivo.</span><span class="sxs-lookup"><span data-stu-id="0ae45-196">Additional include path.</span></span>

##### <a name="lx"></a><span data-ttu-id="0ae45-197">/Lx</span><span class="sxs-lookup"><span data-stu-id="0ae45-197">/Lx</span></span>
<span data-ttu-id="0ae45-198">Output valori letterali esadecimali.</span><span class="sxs-lookup"><span data-stu-id="0ae45-198">Output hexadecimal literals.</span></span> <span data-ttu-id="0ae45-199">Richiede la \_47.dll D3dcompiler o una versione successiva della dll.</span><span class="sxs-lookup"><span data-stu-id="0ae45-199">Requires the D3dcompiler\_47.dll or a later version of the DLL.</span></span>

##### <a name="matchuavs"></a><span data-ttu-id="0ae45-200">/matchUAVs</span><span class="sxs-lookup"><span data-stu-id="0ae45-200">/matchUAVs</span></span>
<span data-ttu-id="0ae45-201">Corrisponde alle allocazioni degli slot UAV del modello shader nello shader corrente.</span><span class="sxs-lookup"><span data-stu-id="0ae45-201">Match template shader UAV slot allocations in the current shader.</span></span> <span data-ttu-id="0ae45-202">Per ulteriori informazioni, vedere la <a href="#remarks">sezione Osservazioni</a>.</span><span class="sxs-lookup"><span data-stu-id="0ae45-202">For more info, see <a href="#remarks">Remarks</a>.</span></span>

##### <a name="mergeuavs"></a><span data-ttu-id="0ae45-203">/mergeUAVs</span><span class="sxs-lookup"><span data-stu-id="0ae45-203">/mergeUAVs</span></span>
<span data-ttu-id="0ae45-204">Unire le allocazioni degli slot UAV del modello shader e dello shader corrente.</span><span class="sxs-lookup"><span data-stu-id="0ae45-204">Merge UAV slot allocations of template shader and the current shader.</span></span> <span data-ttu-id="0ae45-205">Per ulteriori informazioni, vedere la <a href=""></a> <a href="#remarks">sezione Osservazioni</a>.</span><span class="sxs-lookup"><span data-stu-id="0ae45-205">For more info, see <a href=""></a><a href="#remarks">Remarks</a>.</span></span>

##### <a name="ni"></a><span data-ttu-id="0ae45-206">/Ni</span><span class="sxs-lookup"><span data-stu-id="0ae45-206">/Ni</span></span>
<span data-ttu-id="0ae45-207">Numeri di istruzioni di output negli elenchi di assembly.</span><span class="sxs-lookup"><span data-stu-id="0ae45-207">Output instruction numbers in assembly listings.</span></span>

##### <a name="no"></a><span data-ttu-id="0ae45-208">/No</span><span class="sxs-lookup"><span data-stu-id="0ae45-208">/No</span></span>
<span data-ttu-id="0ae45-209">Offset di byte dell'istruzione di output negli elenchi di assembly.</span><span class="sxs-lookup"><span data-stu-id="0ae45-209">Output instruction byte offset in assembly listings.</span></span> <span data-ttu-id="0ae45-210">Quando si genera un assembly, usare/No per annotarlo con l'offset dei byte per ogni istruzione.</span><span class="sxs-lookup"><span data-stu-id="0ae45-210">When you produce assembly, use /No to annotate it with the byte offset for each instruction.</span></span>

##### <a name="nologo"></a><span data-ttu-id="0ae45-211">/nologo</span><span class="sxs-lookup"><span data-stu-id="0ae45-211">/nologo</span></span>
<span data-ttu-id="0ae45-212">Non visualizza le informazioni sul copyright.</span><span class="sxs-lookup"><span data-stu-id="0ae45-212">Suppress copyright message.</span></span>

##### <a name="od"></a><span data-ttu-id="0ae45-213">/Od</span><span class="sxs-lookup"><span data-stu-id="0ae45-213">/Od</span></span>
<span data-ttu-id="0ae45-214">Disabilita le ottimizzazioni.</span><span class="sxs-lookup"><span data-stu-id="0ae45-214">Disable optimizations.</span></span> <span data-ttu-id="0ae45-215">/Od implica/GFP, anche se l'output potrebbe non essere identico a/od/GFP.</span><span class="sxs-lookup"><span data-stu-id="0ae45-215">/Od implies /Gfp, though output may not be identical to /Od /Gfp.</span></span>

##### <a name="op"></a><span data-ttu-id="0ae45-216">/Op</span><span class="sxs-lookup"><span data-stu-id="0ae45-216">/Op</span></span>
<span data-ttu-id="0ae45-217">Disabilitare i preshader (deprecato).</span><span class="sxs-lookup"><span data-stu-id="0ae45-217">Disable preshaders (deprecated).</span></span>

##### <a name="o0-o1-o2-o3"></a><span data-ttu-id="0ae45-218">/O0/O1,/O2,/O3</span><span class="sxs-lookup"><span data-stu-id="0ae45-218">/O0 /O1, /O2, /O3</span></span>
<span data-ttu-id="0ae45-219">Livelli di ottimizzazione.</span><span class="sxs-lookup"><span data-stu-id="0ae45-219">Optimization levels.</span></span> <span data-ttu-id="0ae45-220">O1 è l'impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="0ae45-220">O1 is the default setting.</span></span>
- <span data-ttu-id="0ae45-221">O0-Disabilita il riordinamento delle istruzioni.</span><span class="sxs-lookup"><span data-stu-id="0ae45-221">O0 - Disables instruction reordering.</span></span> <span data-ttu-id="0ae45-222">In questo modo è possibile ridurre il carico del registro e velocizzare la simulazione del ciclo.</span><span class="sxs-lookup"><span data-stu-id="0ae45-222">This helps reduce register load and enables faster loop simulation.</span></span>
- <span data-ttu-id="0ae45-223">O1: Disabilita il riordinamento delle istruzioni per ps_3_0 e su.</span><span class="sxs-lookup"><span data-stu-id="0ae45-223">O1 - Disables instruction reordering for ps_3_0 and up.</span></span>
- <span data-ttu-id="0ae45-224">O2: uguale a o1.</span><span class="sxs-lookup"><span data-stu-id="0ae45-224">O2 - Same as O1.</span></span> <span data-ttu-id="0ae45-225">Riservato per utilizzi futuri.</span><span class="sxs-lookup"><span data-stu-id="0ae45-225">Reserved for future use.</span></span>
- <span data-ttu-id="0ae45-226">O3: uguale a o1.</span><span class="sxs-lookup"><span data-stu-id="0ae45-226">O3 - Same as O1.</span></span> <span data-ttu-id="0ae45-227">Riservato per utilizzi futuri.</span><span class="sxs-lookup"><span data-stu-id="0ae45-227">Reserved for future use.</span></span>

##### <a name="p-file"></a><span data-ttu-id="0ae45-228">/P <*file*></span><span class="sxs-lookup"><span data-stu-id="0ae45-228">/P <*file*></span></span>
<span data-ttu-id="0ae45-229">Pre-elabora nel file (deve essere usato da solo).</span><span class="sxs-lookup"><span data-stu-id="0ae45-229">Preprocess to file (must be used alone).</span></span>

##### <a name="qstrip_debug"></a><span data-ttu-id="0ae45-230">/Qstrip_debug</span><span class="sxs-lookup"><span data-stu-id="0ae45-230">/Qstrip_debug</span></span>
<span data-ttu-id="0ae45-231">Rimuove i dati di debug dal bytecode dello shader per 4_0 + profili.</span><span class="sxs-lookup"><span data-stu-id="0ae45-231">Strip debug data from shader bytecode for 4_0+ profiles.</span></span>

##### <a name="qstrip_priv"></a><span data-ttu-id="0ae45-232">/Qstrip_priv</span><span class="sxs-lookup"><span data-stu-id="0ae45-232">/Qstrip_priv</span></span>
<span data-ttu-id="0ae45-233">Rimuovere i dati privati da 4_0 + bytecode shader.</span><span class="sxs-lookup"><span data-stu-id="0ae45-233">Strip the private data from 4_0+ shader bytecode.</span></span> <span data-ttu-id="0ae45-234">Rimuove i dati privati (sequenza arbitraria di byte) dal BLOB dello shader (Binary shader compilato) precedentemente incorporato con l' `/setprivate <file>` opzione.</span><span class="sxs-lookup"><span data-stu-id="0ae45-234">Removes private data (arbitrary sequence of bytes) from the shader blob (compiled shader binary) that you previously embedded with the `/setprivate <file>` option.</span></span>

<span data-ttu-id="0ae45-235">È necessario specificare l'opzione/DUMPBIN con/Qstrip_priv.</span><span class="sxs-lookup"><span data-stu-id="0ae45-235">You must specify the /dumpbin option with /Qstrip_priv.</span></span> <span data-ttu-id="0ae45-236">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="0ae45-236">For example:</span></span>

```console
fxc /Qstrip_priv /dumpbin /Fo ps01.no.private.obj 
    ps01.with.private.obj
```

##### <a name="qstrip_reflect"></a><span data-ttu-id="0ae45-237">/Qstrip_reflect</span><span class="sxs-lookup"><span data-stu-id="0ae45-237">/Qstrip_reflect</span></span>
<span data-ttu-id="0ae45-238">Rimuove i dati di reflection dal bytecode dello shader per 4_0 + profili.</span><span class="sxs-lookup"><span data-stu-id="0ae45-238">Strip reflection data from shader bytecode for 4_0+ profiles.</span></span>

##### <a name="qstrip_rootsignature"></a><span data-ttu-id="0ae45-239">/Qstrip_rootsignature</span><span class="sxs-lookup"><span data-stu-id="0ae45-239">/Qstrip_rootsignature</span></span>
<span data-ttu-id="0ae45-240">Rimuovere la firma radice dal bytecode dello shader.</span><span class="sxs-lookup"><span data-stu-id="0ae45-240">Strip root signature from shader bytecode.</span></span> <span data-ttu-id="0ae45-241">Novità per Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="0ae45-241">New for Direct3D 12.</span></span>

##### <a name="res_may_alias"></a><span data-ttu-id="0ae45-242">/res_may_alias</span><span class="sxs-lookup"><span data-stu-id="0ae45-242">/res_may_alias</span></span>
<span data-ttu-id="0ae45-243">Si supponga che UAV/SRVs possa essere alias per cs_5_0 +.</span><span class="sxs-lookup"><span data-stu-id="0ae45-243">Assume that UAVs/SRVs may alias for cs_5_0+.</span></span> <span data-ttu-id="0ae45-244">Richiede la \_47.dll D3dcompiler o una versione successiva della dll.</span><span class="sxs-lookup"><span data-stu-id="0ae45-244">Requires the D3dcompiler\_47.dll or a later version of the DLL.</span></span>

##### <a name="setprivate-file"></a><span data-ttu-id="0ae45-245">*file* </SetPrivate></span><span class="sxs-lookup"><span data-stu-id="0ae45-245">/setprivate <*file*></span></span>
<span data-ttu-id="0ae45-246">Aggiungere i dati privati nel file specificato al BLOB dello shader compilato.</span><span class="sxs-lookup"><span data-stu-id="0ae45-246">Add private data in the given file to the compiled shader blob.</span></span> <span data-ttu-id="0ae45-247">Incorpora il file specificato, che viene considerato come un buffer non elaborato, nel BLOB dello shader.</span><span class="sxs-lookup"><span data-stu-id="0ae45-247">Embeds the given file, which is treated as a raw buffer, to the shader blob.</span></span> <span data-ttu-id="0ae45-248">Usare/SetPrivate per aggiungere dati privati quando si compila uno shader.</span><span class="sxs-lookup"><span data-stu-id="0ae45-248">Use /setprivate to add private data when you compile a shader.</span></span> <span data-ttu-id="0ae45-249">In alternativa, usare l'opzione/DUMPBIN con/SetPrivate per caricare un oggetto shader esistente e quindi, dopo che l'oggetto è in memoria, per aggiungere il BLOB di dati privati.</span><span class="sxs-lookup"><span data-stu-id="0ae45-249">Or, use the /dumpbin option with /setprivate to load an existing shader object, and then after the object is in memory, to add the private data blob.</span></span> <span data-ttu-id="0ae45-250">Ad esempio, usare un singolo comando con/SetPrivate per aggiungere dati privati a un BLOB dello shader compilato:</span><span class="sxs-lookup"><span data-stu-id="0ae45-250">For example, use either a single command with /setprivate to add private data to a compiled shader blob:</span></span>

```console
fxc /T ps_4_0 /Fo ps01.with.private.obj ps01.fx 
    /setprivate ps01.private.data
```
    
<span data-ttu-id="0ae45-251">In alternativa, usare due comandi dove il secondo comando carica un oggetto shader e quindi aggiunge dati privati:</span><span class="sxs-lookup"><span data-stu-id="0ae45-251">Or, use two commands where the second command loads a shader object and then adds private data:</span></span>

```console
fxc /T ps_4_0 /Fo ps01.no.private.obj ps01.fx
fxc /dumpbin /Fo ps01.with.private.obj ps01.no.private.obj 
    /setprivate ps01.private.data
```
    
##### <a name="setrootsignature-file"></a><span data-ttu-id="0ae45-252">*file* </setrootsignature></span><span class="sxs-lookup"><span data-stu-id="0ae45-252">/setrootsignature <*file*></span></span>
<span data-ttu-id="0ae45-253">Associa la firma radice al bytecode dello shader.</span><span class="sxs-lookup"><span data-stu-id="0ae45-253">Attach root signature to shader bytecode.</span></span> <span data-ttu-id="0ae45-254">Novità per Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="0ae45-254">New for Direct3D 12.</span></span>

##### <a name="shtemplate-file"></a><span data-ttu-id="0ae45-255">*file* </shtemplate></span><span class="sxs-lookup"><span data-stu-id="0ae45-255">/shtemplate <*file*></span></span>
<span data-ttu-id="0ae45-256">Usare il file shader del modello specificato per unire (/mergeUAVs) e le risorse corrispondenti (/matchUAVs).</span><span class="sxs-lookup"><span data-stu-id="0ae45-256">Use given template shader file for merging (/mergeUAVs) and matching (/matchUAVs) resources.</span></span> <span data-ttu-id="0ae45-257">Per ulteriori informazioni, vedere la <a href="#remarks">sezione Osservazioni</a>.</span><span class="sxs-lookup"><span data-stu-id="0ae45-257">For more info, see <a href="#remarks">Remarks</a>.</span></span>

##### <a name="vd"></a><span data-ttu-id="0ae45-258">/VD</span><span class="sxs-lookup"><span data-stu-id="0ae45-258">/Vd</span></span>
<span data-ttu-id="0ae45-259">Disabilitare la convalida.</span><span class="sxs-lookup"><span data-stu-id="0ae45-259">Disable validation.</span></span>

##### <a name="verifyrootsignature-file"></a><span data-ttu-id="0ae45-260">*file* </verifyrootsignature></span><span class="sxs-lookup"><span data-stu-id="0ae45-260">/verifyrootsignature <*file*></span></span>
<span data-ttu-id="0ae45-261">Verificare il bytecode dello shader rispetto alla firma radice.</span><span class="sxs-lookup"><span data-stu-id="0ae45-261">Verify shader bytecode against root signature.</span></span> <span data-ttu-id="0ae45-262">Novità per Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="0ae45-262">New for Direct3D 12.</span></span>

##### <a name="vi"></a><span data-ttu-id="0ae45-263">/Vi</span><span class="sxs-lookup"><span data-stu-id="0ae45-263">/Vi</span></span>
<span data-ttu-id="0ae45-264">Visualizza i dettagli sul processo di inclusione.</span><span class="sxs-lookup"><span data-stu-id="0ae45-264">Display details about the include process.</span></span>

##### <a name="vn-name"></a><span data-ttu-id="0ae45-265">*Nome* </VN></span><span class="sxs-lookup"><span data-stu-id="0ae45-265">/Vn <*name*></span></span>
<span data-ttu-id="0ae45-266">Usare nome come nome della variabile nel file di intestazione.</span><span class="sxs-lookup"><span data-stu-id="0ae45-266">Use name as variable name in header file.</span></span>

##### <a name="wx"></a><span data-ttu-id="0ae45-267">/WX</span><span class="sxs-lookup"><span data-stu-id="0ae45-267">/WX</span></span>
<span data-ttu-id="0ae45-268">Considera gli avvisi come errori.</span><span class="sxs-lookup"><span data-stu-id="0ae45-268">Treat warnings as errors.</span></span>

##### <a name="zi"></a><span data-ttu-id="0ae45-269">/Zi</span><span class="sxs-lookup"><span data-stu-id="0ae45-269">/Zi</span></span>
<span data-ttu-id="0ae45-270">Abilita le informazioni di debug.</span><span class="sxs-lookup"><span data-stu-id="0ae45-270">Enable debugging information.</span></span>

##### <a name="zpc"></a><span data-ttu-id="0ae45-271">/Zpc</span><span class="sxs-lookup"><span data-stu-id="0ae45-271">/Zpc</span></span>
<span data-ttu-id="0ae45-272">Comprimere le matrici in base all'ordine delle colonne.</span><span class="sxs-lookup"><span data-stu-id="0ae45-272">Pack matrices in column-major order.</span></span>

##### <a name="zpr"></a><span data-ttu-id="0ae45-273">/Zpr</span><span class="sxs-lookup"><span data-stu-id="0ae45-273">/Zpr</span></span>
<span data-ttu-id="0ae45-274">Comprimere le matrici in ordine di riga.</span><span class="sxs-lookup"><span data-stu-id="0ae45-274">Pack matrices in row-major order.</span></span>

### <a name="filenames"></a><span data-ttu-id="0ae45-275">*Nomi file*</span><span class="sxs-lookup"><span data-stu-id="0ae45-275">*Filenames*</span></span>

<span data-ttu-id="0ae45-276">\[nei \] file che contengono gli shader e/o l'effetto o i.</span><span class="sxs-lookup"><span data-stu-id="0ae45-276">\[in\] The files that contains the shader(s) and/or the effect(s).</span></span>

## <a name="remarks"></a><span data-ttu-id="0ae45-277">Commenti</span><span class="sxs-lookup"><span data-stu-id="0ae45-277">Remarks</span></span>

<span data-ttu-id="0ae45-278">Usare le `/mergeUAVs` `/matchUAVs` Opzioni, e `/shtemplate` per allineare gli slot di binding UAV per una catena di shader.</span><span class="sxs-lookup"><span data-stu-id="0ae45-278">Use the `/mergeUAVs`, `/matchUAVs`, and `/shtemplate` options to align the UAV binding slots for a chain of shaders.</span></span>

<span data-ttu-id="0ae45-279">Si supponga di avere shader A. FX, B. FX e C. fx.</span><span class="sxs-lookup"><span data-stu-id="0ae45-279">Suppose you have shaders A.fx, B.fx, and C.fx.</span></span> <span data-ttu-id="0ae45-280">Per allineare gli slot di binding UAV per questa catena di shader, sono necessari due passaggi di compilazione:</span><span class="sxs-lookup"><span data-stu-id="0ae45-280">To align the UAV binding slots for this chain of shaders, you need two passes of compilation:</span></span>

<span data-ttu-id="0ae45-281">**Per allineare gli slot di binding UAV per una catena di shader**</span><span class="sxs-lookup"><span data-stu-id="0ae45-281">**To align the UAV binding slots for a chain of shaders**</span></span>

1.  <span data-ttu-id="0ae45-282">Usare/mergeUAVs per compilare shader e specificare un BLOB dello shader compilato in precedenza con/shtemplate.</span><span class="sxs-lookup"><span data-stu-id="0ae45-282">Use /mergeUAVs to compile shaders, and specify a previously-compiled shader blob with /shtemplate.</span></span> <span data-ttu-id="0ae45-283">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="0ae45-283">For example:</span></span>
    ```
    fxc.exe /T cs_5_0 C.fx /Fo C.o /mergeUAVs /shtemplate Btmp.o
    ```
2.  <span data-ttu-id="0ae45-284">Usare/matchUAVs per compilare shader e specificare l'ultimo BLOB dello shader dal primo passaggio con/shtemplate.</span><span class="sxs-lookup"><span data-stu-id="0ae45-284">Use /matchUAVs to compile shaders, and specify the last shader blob from the first pass with /shtemplate.</span></span> <span data-ttu-id="0ae45-285">È possibile compilare in qualsiasi ordine.</span><span class="sxs-lookup"><span data-stu-id="0ae45-285">You can compile in any order.</span></span> <span data-ttu-id="0ae45-286">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="0ae45-286">For example:</span></span>
    ```
    fxc.exe /T cs_5_0 A.fx /Fo A.o /matchUAVs /shtemplate C.o
    ```
<span data-ttu-id="0ae45-287">Non è necessario ricompilare C. fx nel secondo passaggio.</span><span class="sxs-lookup"><span data-stu-id="0ae45-287">You don't have to recompile C.fx in the second pass.</span></span>

<span data-ttu-id="0ae45-288">Dopo aver eseguito le due passate di compilazione precedenti, è possibile usare un. o, B. o e C. o come BLOB dello shader finale con slot UAV allineati.</span><span class="sxs-lookup"><span data-stu-id="0ae45-288">After you perform the preceding two compilation passes, you can use A.o, B.o, and C.o as final shader blobs with aligned UAV slots.</span></span>

## <a name="profiles"></a><span data-ttu-id="0ae45-289">Profiles</span><span class="sxs-lookup"><span data-stu-id="0ae45-289">Profiles</span></span>

<span data-ttu-id="0ae45-290">Ogni modello shader è contrassegnato con un profilo HLSL.</span><span class="sxs-lookup"><span data-stu-id="0ae45-290">Each shader model is labeled with an HLSL profile.</span></span> <span data-ttu-id="0ae45-291">Per compilare uno shader rispetto a un particolare modello shader, scegliere il profilo shader appropriato nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="0ae45-291">To compile a shader against a particular shader model, choose the appropriate shader profile from the following table.</span></span>

<table><thead><tr class="header"><th><span data-ttu-id="0ae45-292">Tipo shader</span><span class="sxs-lookup"><span data-stu-id="0ae45-292">Shader Type</span></span></th><th><span data-ttu-id="0ae45-293">Profiles</span><span class="sxs-lookup"><span data-stu-id="0ae45-293">Profiles</span></span></th></tr></thead><tbody><tr class="odd"><td><span data-ttu-id="0ae45-294">Compute Shader</span><span class="sxs-lookup"><span data-stu-id="0ae45-294">Compute Shader</span></span></td><td><dl> <span data-ttu-id="0ae45-295">cs_4_0</span><span class="sxs-lookup"><span data-stu-id="0ae45-295">cs_4_0</span></span><br />
<span data-ttu-id="0ae45-296">cs_4_1</span><span class="sxs-lookup"><span data-stu-id="0ae45-296">cs_4_1</span></span><br />
<span data-ttu-id="0ae45-297">cs_5_0</span><span class="sxs-lookup"><span data-stu-id="0ae45-297">cs_5_0</span></span><br />
<span data-ttu-id="0ae45-298">cs_5_1</span><span class="sxs-lookup"><span data-stu-id="0ae45-298">cs_5_1</span></span><br />
</dl></td></tr><tr class="even"><td><span data-ttu-id="0ae45-299">Domain shader</span><span class="sxs-lookup"><span data-stu-id="0ae45-299">Domain Shader</span></span></td><td><dl> <span data-ttu-id="0ae45-300">ds_5_0</span><span class="sxs-lookup"><span data-stu-id="0ae45-300">ds_5_0</span></span><br />
<span data-ttu-id="0ae45-301">ds_5_1</span><span class="sxs-lookup"><span data-stu-id="0ae45-301">ds_5_1</span></span><br />
</dl></td></tr><tr class="odd"><td><span data-ttu-id="0ae45-302">Geometry shader</span><span class="sxs-lookup"><span data-stu-id="0ae45-302">Geometry Shader</span></span></td><td><dl> <span data-ttu-id="0ae45-303">gs_4_0</span><span class="sxs-lookup"><span data-stu-id="0ae45-303">gs_4_0</span></span><br />
<span data-ttu-id="0ae45-304">gs_4_1</span><span class="sxs-lookup"><span data-stu-id="0ae45-304">gs_4_1</span></span><br />
<span data-ttu-id="0ae45-305">gs_5_0</span><span class="sxs-lookup"><span data-stu-id="0ae45-305">gs_5_0</span></span><br />
<span data-ttu-id="0ae45-306">gs_5_1</span><span class="sxs-lookup"><span data-stu-id="0ae45-306">gs_5_1</span></span><br />
</dl></td></tr><tr class="even"><td><span data-ttu-id="0ae45-307">Collegamento dello shader HLSL</span><span class="sxs-lookup"><span data-stu-id="0ae45-307">HLSL shader linking</span></span> </td><td><dl> <span data-ttu-id="0ae45-308">lib_4_0</span><span class="sxs-lookup"><span data-stu-id="0ae45-308">lib_4_0</span></span><br />
<span data-ttu-id="0ae45-309">lib_4_1</span><span class="sxs-lookup"><span data-stu-id="0ae45-309">lib_4_1</span></span><br />
<span data-ttu-id="0ae45-310">lib_4_0_level_9_1</span><span class="sxs-lookup"><span data-stu-id="0ae45-310">lib_4_0_level_9_1</span></span><br />
<span data-ttu-id="0ae45-311">lib_4_0_level_9_1_vs_only</span><span class="sxs-lookup"><span data-stu-id="0ae45-311">lib_4_0_level_9_1_vs_only</span></span><br />
<span data-ttu-id="0ae45-312">lib_4_0_level_9_1_ps_only</span><span class="sxs-lookup"><span data-stu-id="0ae45-312">lib_4_0_level_9_1_ps_only</span></span><br />
<span data-ttu-id="0ae45-313">lib_4_0_level_9_3</span><span class="sxs-lookup"><span data-stu-id="0ae45-313">lib_4_0_level_9_3</span></span><br />
<span data-ttu-id="0ae45-314">lib_4_0_level_9_3_vs_only</span><span class="sxs-lookup"><span data-stu-id="0ae45-314">lib_4_0_level_9_3_vs_only</span></span><br />
<span data-ttu-id="0ae45-315">lib_4_0_level_9_3_ps_only</span><span class="sxs-lookup"><span data-stu-id="0ae45-315">lib_4_0_level_9_3_ps_only</span></span><br />
<span data-ttu-id="0ae45-316">lib_5_0</span><span class="sxs-lookup"><span data-stu-id="0ae45-316">lib_5_0</span></span><br />
</dl> <span data-ttu-id="0ae45-317">Per ulteriori informazioni sul collegamento di shader, vedere <a href="/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linker"><strong>ID3D11Linker</strong></a> e <a href="/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11functionlinkinggraph"><strong>ID3D11FunctionLinkingGraph</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="0ae45-317">For more info about shader linking, see <a href="/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linker"><strong>ID3D11Linker</strong></a> and <a href="/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11functionlinkinggraph"><strong>ID3D11FunctionLinkingGraph</strong></a>.</span></span> <br/></td></tr><tr class="odd"><td><span data-ttu-id="0ae45-318">Hull shader</span><span class="sxs-lookup"><span data-stu-id="0ae45-318">Hull Shader</span></span></td><td><dl> <span data-ttu-id="0ae45-319">hs_5_0</span><span class="sxs-lookup"><span data-stu-id="0ae45-319">hs_5_0</span></span><br />
<span data-ttu-id="0ae45-320">hs_5_1</span><span class="sxs-lookup"><span data-stu-id="0ae45-320">hs_5_1</span></span><br />
</dl></td></tr><tr class="even"><td><span data-ttu-id="0ae45-321">Pixel shader</span><span class="sxs-lookup"><span data-stu-id="0ae45-321">Pixel Shader</span></span></td><td><dl> <span data-ttu-id="0ae45-322">ps_2_0</span><span class="sxs-lookup"><span data-stu-id="0ae45-322">ps_2_0</span></span><br />
<span data-ttu-id="0ae45-323">ps_2_a</span><span class="sxs-lookup"><span data-stu-id="0ae45-323">ps_2_a</span></span><br />
<span data-ttu-id="0ae45-324">ps_2_b</span><span class="sxs-lookup"><span data-stu-id="0ae45-324">ps_2_b</span></span><br />
<span data-ttu-id="0ae45-325">ps_2_sw</span><span class="sxs-lookup"><span data-stu-id="0ae45-325">ps_2_sw</span></span><br />
<span data-ttu-id="0ae45-326">ps_3_0</span><span class="sxs-lookup"><span data-stu-id="0ae45-326">ps_3_0</span></span><br />
<span data-ttu-id="0ae45-327">ps_3_sw</span><span class="sxs-lookup"><span data-stu-id="0ae45-327">ps_3_sw</span></span><br />
<span data-ttu-id="0ae45-328">ps_4_0</span><span class="sxs-lookup"><span data-stu-id="0ae45-328">ps_4_0</span></span><br />
<span data-ttu-id="0ae45-329">ps_4_0_level_9_0</span><span class="sxs-lookup"><span data-stu-id="0ae45-329">ps_4_0_level_9_0</span></span><br />
<span data-ttu-id="0ae45-330">ps_4_0_level_9_1</span><span class="sxs-lookup"><span data-stu-id="0ae45-330">ps_4_0_level_9_1</span></span><br />
<span data-ttu-id="0ae45-331">ps_4_0_level_9_3</span><span class="sxs-lookup"><span data-stu-id="0ae45-331">ps_4_0_level_9_3</span></span><br />
<span data-ttu-id="0ae45-332">ps_4_1</span><span class="sxs-lookup"><span data-stu-id="0ae45-332">ps_4_1</span></span><br />
<span data-ttu-id="0ae45-333">ps_5_0</span><span class="sxs-lookup"><span data-stu-id="0ae45-333">ps_5_0</span></span><br />
<span data-ttu-id="0ae45-334">ps_5_1</span><span class="sxs-lookup"><span data-stu-id="0ae45-334">ps_5_1</span></span><br />
</dl></td></tr><tr class="odd"><td><span data-ttu-id="0ae45-335">Firma radice</span><span class="sxs-lookup"><span data-stu-id="0ae45-335">Root Signature</span></span></td><td><dl> <span data-ttu-id="0ae45-336">rootsig_1_0</span><span class="sxs-lookup"><span data-stu-id="0ae45-336">rootsig_1_0</span></span><br />
</dl></td></tr><tr class="even"><td><span data-ttu-id="0ae45-337">Trama shader</span><span class="sxs-lookup"><span data-stu-id="0ae45-337">Texture Shader</span></span></td><td><dl> <span data-ttu-id="0ae45-338">tx_1_0</span><span class="sxs-lookup"><span data-stu-id="0ae45-338">tx_1_0</span></span><br />
</dl></td></tr><tr class="odd"><td><span data-ttu-id="0ae45-339">Vertex shader</span><span class="sxs-lookup"><span data-stu-id="0ae45-339">Vertex Shader</span></span></td><td><dl> <span data-ttu-id="0ae45-340">vs_1_1</span><span class="sxs-lookup"><span data-stu-id="0ae45-340">vs_1_1</span></span><br />
<span data-ttu-id="0ae45-341">vs_2_0</span><span class="sxs-lookup"><span data-stu-id="0ae45-341">vs_2_0</span></span><br />
<span data-ttu-id="0ae45-342">vs_2_a</span><span class="sxs-lookup"><span data-stu-id="0ae45-342">vs_2_a</span></span><br />
<span data-ttu-id="0ae45-343">vs_2_sw</span><span class="sxs-lookup"><span data-stu-id="0ae45-343">vs_2_sw</span></span><br />
<span data-ttu-id="0ae45-344">vs_3_0</span><span class="sxs-lookup"><span data-stu-id="0ae45-344">vs_3_0</span></span><br />
<span data-ttu-id="0ae45-345">vs_3_sw</span><span class="sxs-lookup"><span data-stu-id="0ae45-345">vs_3_sw</span></span><br />
<span data-ttu-id="0ae45-346">vs_4_0</span><span class="sxs-lookup"><span data-stu-id="0ae45-346">vs_4_0</span></span><br />
<span data-ttu-id="0ae45-347">vs_4_0_level_9_0</span><span class="sxs-lookup"><span data-stu-id="0ae45-347">vs_4_0_level_9_0</span></span><br />
<span data-ttu-id="0ae45-348">vs_4_0_level_9_1</span><span class="sxs-lookup"><span data-stu-id="0ae45-348">vs_4_0_level_9_1</span></span><br />
<span data-ttu-id="0ae45-349">vs_4_0_level_9_3</span><span class="sxs-lookup"><span data-stu-id="0ae45-349">vs_4_0_level_9_3</span></span><br />
<span data-ttu-id="0ae45-350">vs_4_1</span><span class="sxs-lookup"><span data-stu-id="0ae45-350">vs_4_1</span></span><br />
<span data-ttu-id="0ae45-351">vs_5_0</span><span class="sxs-lookup"><span data-stu-id="0ae45-351">vs_5_0</span></span><br />
<span data-ttu-id="0ae45-352">vs_5_1</span><span class="sxs-lookup"><span data-stu-id="0ae45-352">vs_5_1</span></span><br />
</dl></td></tr></tbody></table>

## <a name="version-notes"></a><span data-ttu-id="0ae45-353">Note sulla versione</span><span class="sxs-lookup"><span data-stu-id="0ae45-353">Version notes</span></span>

<span data-ttu-id="0ae45-354">Per Direct3D 12, vedere [specifica delle firme radice in HLSL](/windows/desktop/direct3d12/specifying-root-signatures-in-hlsl), [associazione di risorse in HLSL](/windows/desktop/direct3d12/resource-binding-in-hlsl) e [indicizzazione dinamica con HLSL 5,1](/windows/desktop/direct3d12/dynamic-indexing-using-hlsl-5-1).</span><span class="sxs-lookup"><span data-stu-id="0ae45-354">For Direct3D 12 refer to [Specifying Root Signatures in HLSL](/windows/desktop/direct3d12/specifying-root-signatures-in-hlsl), [Resource Binding in HLSL](/windows/desktop/direct3d12/resource-binding-in-hlsl) and [Dynamic Indexing using HLSL 5.1](/windows/desktop/direct3d12/dynamic-indexing-using-hlsl-5-1).</span></span>

<span data-ttu-id="0ae45-355">In Direct3D 10 usare l'API per ottenere il profilo vertex, Geometry e pixel shader più adatto a un determinato dispositivo chiamando le funzioni seguenti: [**D3D10GetVertexShaderProfile**](/windows/desktop/api/d3d10shader/nf-d3d10shader-d3d10getvertexshaderprofile), [**D3D10GetPixelShaderProfile**](/windows/desktop/api/d3d10shader/nf-d3d10shader-d3d10getpixelshaderprofile)e [**D3D10GetGeometryShaderProfile**](/windows/desktop/api/d3d10shader/nf-d3d10shader-d3d10getgeometryshaderprofile).</span><span class="sxs-lookup"><span data-stu-id="0ae45-355">In Direct3D 10 use the API to get the vertex, geometry, and pixel-shader profile best suited to a given device by calling these functions: [**D3D10GetVertexShaderProfile**](/windows/desktop/api/d3d10shader/nf-d3d10shader-d3d10getvertexshaderprofile), [**D3D10GetPixelShaderProfile**](/windows/desktop/api/d3d10shader/nf-d3d10shader-d3d10getpixelshaderprofile), and [**D3D10GetGeometryShaderProfile**](/windows/desktop/api/d3d10shader/nf-d3d10shader-d3d10getgeometryshaderprofile).</span></span>

<span data-ttu-id="0ae45-356">In Direct3D 9 usare i metodi [**GetDeviceCaps**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9-getdevicecaps) o [**GetDeviceCaps**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getdevicecaps) per recuperare i profili Vertex e pixel shader supportati da un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0ae45-356">In Direct3D 9 use the [**GetDeviceCaps**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9-getdevicecaps) or [**GetDeviceCaps**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getdevicecaps) methods to retrieve the vertex and pixel-shader profiles supported by a device.</span></span> <span data-ttu-id="0ae45-357">La struttura [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9) restituita da tali metodi indica i profili Vertex e pixel shader supportati da un dispositivo nei relativi membri **VertexShaderVersion** e **PixelShaderVersion** .</span><span class="sxs-lookup"><span data-stu-id="0ae45-357">The [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9) structure returned by those methods indicates the vertex and pixel-shader profiles supported by a device in its **VertexShaderVersion** and **PixelShaderVersion** members.</span></span>

<span data-ttu-id="0ae45-358">Per esempi, vedere [compilazione con il compilatore corrente](dx-graphics-tools-fxc-using.md).</span><span class="sxs-lookup"><span data-stu-id="0ae45-358">For examples, see [Compiling with the Current Compiler](dx-graphics-tools-fxc-using.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0ae45-359">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0ae45-359">Related topics</span></span>

* [<span data-ttu-id="0ae45-360">Effect-strumento compilatore</span><span class="sxs-lookup"><span data-stu-id="0ae45-360">Effect-Compiler Tool</span></span>](fxc.md)