---
title: Sintassi delle variabili
description: Usare le regole di sintassi seguenti per dichiarare le variabili HLSL.
ms.assetid: 684c42d1-2dd4-42e1-9cff-580edb5c6bcd
keywords:
- extern, sintassi variabile (DirectX HLSL)
- interpolazione, sintassi variabile (DirectX HLSL)
- Sintassi condivisa, variabile (DirectX HLSL)
- groupshared, sintassi variabile (DirectX HLSL)
- static, sintassi variabile (DirectX HLSL)
- Uniform, sintassi variabile (DirectX HLSL)
- Sintassi volatile, Variable (DirectX HLSL)
- Sintassi precisa, variabile (DirectX HLSL)
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f6e63bafa62a9857af678e0848c81237dcd0d585
ms.sourcegitcommit: 4e0bde7dfa48a0b60bca4a5230eb2b05be3778d3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/11/2020
ms.locfileid: "104993645"
---
# <a name="variable-syntax"></a><span data-ttu-id="d76e5-111">Sintassi delle variabili</span><span class="sxs-lookup"><span data-stu-id="d76e5-111">Variable Syntax</span></span>

<span data-ttu-id="d76e5-112">Usare le regole di sintassi seguenti per dichiarare le variabili HLSL.</span><span class="sxs-lookup"><span data-stu-id="d76e5-112">Use the following syntax rules to declare HLSL variables.</span></span>



|                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d76e5-113">\[*Archiviazione \_* \] \[ *\_ Modificatore tipo* di classe \] *nome tipo* \[ *index* \] \[ *: Semantic* \] \[ *: Packoffset* \] \[ *: Register* \] ;    \[ *Annotazioni* \] \[ *= Iniziale \_ Valore* di                    \]</span><span class="sxs-lookup"><span data-stu-id="d76e5-113">\[*Storage\_Class*\] \[*Type\_Modifier*\] *Type Name*\[*Index*\]     \[*: Semantic*\]     \[*: Packoffset*\]     \[*: Register*\];    \[*Annotations*\]     \[*= Initial\_Value*\]</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="d76e5-114">Parametri</span><span class="sxs-lookup"><span data-stu-id="d76e5-114">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d76e5-115"><span id="Storage_Class_"></span><span id="storage_class_"></span><span id="STORAGE_CLASS_"></span>*Classe di archiviazione \_*</span><span class="sxs-lookup"><span data-stu-id="d76e5-115"><span id="Storage_Class_"></span><span id="storage_class_"></span><span id="STORAGE_CLASS_"></span>*Storage\_Class*</span></span> 
</dt> <dd>

<span data-ttu-id="d76e5-116">Modificatori della classe di archiviazione facoltativi che forniscono gli hint del compilatore sull'ambito e sulla durata delle variabili; i modificatori possono essere specificati in qualsiasi ordine.</span><span class="sxs-lookup"><span data-stu-id="d76e5-116">Optional storage-class modifiers that give the compiler hints about variable scope and lifetime; the modifiers can be specified in any order.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d76e5-117">Valore</span><span class="sxs-lookup"><span data-stu-id="d76e5-117">Value</span></span></th>
<th><span data-ttu-id="d76e5-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d76e5-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d76e5-119"><strong>extern</strong></span><span class="sxs-lookup"><span data-stu-id="d76e5-119"><strong>extern</strong></span></span></td>
<td><span data-ttu-id="d76e5-120">Contrassegna una variabile globale come input esterno per lo shader; si tratta del contrassegno predefinito per tutte le variabili globali.</span><span class="sxs-lookup"><span data-stu-id="d76e5-120">Mark a global variable as an external input to the shader; this is the default marking for all global variables.</span></span> <span data-ttu-id="d76e5-121">Non può essere combinato con <strong>static</strong>.</span><span class="sxs-lookup"><span data-stu-id="d76e5-121">Cannot be combined with <strong>static</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d76e5-122"><strong>interpolazione</strong></span><span class="sxs-lookup"><span data-stu-id="d76e5-122"><strong>nointerpolation</strong></span></span></td>
<td><span data-ttu-id="d76e5-123">Non interpolare gli output di un vertex shader prima di passarli a un pixel shader.</span><span class="sxs-lookup"><span data-stu-id="d76e5-123">Do not interpolate the outputs of a vertex shader before passing them to a pixel shader.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d76e5-124"><strong>preciso</strong></span><span class="sxs-lookup"><span data-stu-id="d76e5-124"><strong>precise</strong></span></span></td>
<td><span data-ttu-id="d76e5-125">La parola chiave <strong>precisa</strong> quando viene applicata a una variabile limita tutti i calcoli utilizzati per produrre il valore assegnato a tale variabile nei modi seguenti:</span><span class="sxs-lookup"><span data-stu-id="d76e5-125">The <strong>precise</strong> keyword when applied to a variable will restrict any calculations used to produce the value assigned to that variable in the following ways:</span></span>

*   <span data-ttu-id="d76e5-126">Le operazioni separate vengono mantenute separate.</span><span class="sxs-lookup"><span data-stu-id="d76e5-126">Separate operations are kept separate.</span></span> <span data-ttu-id="d76e5-127">Se, ad esempio, un'operazione MUL e Add potrebbe essere stata fusa in un'operazione MAD <strong>, impone</strong> che le operazioni rimangano separate.</span><span class="sxs-lookup"><span data-stu-id="d76e5-127">For example, where a mul and add operation might have been fused into a mad operation, <strong>precise</strong> forces the operations to remain separate.</span></span> <span data-ttu-id="d76e5-128">È invece necessario usare in modo esplicito la funzione intrinseca MAD.</span><span class="sxs-lookup"><span data-stu-id="d76e5-128">Instead, you must explicitly use the mad intrinsic function.</span></span>
*   <span data-ttu-id="d76e5-129">L'ordine delle operazioni viene mantenuto.</span><span class="sxs-lookup"><span data-stu-id="d76e5-129">Order of operations are maintained.</span></span> <span data-ttu-id="d76e5-130">Se è possibile che l'ordine delle istruzioni sia stato mischiato per migliorare le prestazioni, <strong>precisa</strong> garantisce che il compilatore mantenga l'ordine come scritto.</span><span class="sxs-lookup"><span data-stu-id="d76e5-130">Where the order of instructions might have been shuffled to improve performance, <strong>precise</strong> ensures that the compiler preserves the order as written.</span></span>
*   <span data-ttu-id="d76e5-131">Le operazioni non sicure IEEE sono limitate.</span><span class="sxs-lookup"><span data-stu-id="d76e5-131">IEEE unsafe operations are restricted.</span></span> <span data-ttu-id="d76e5-132">Quando il compilatore potrebbe avere utilizzato operazioni matematiche veloci che non considerano i valori NaN (non un numero) e INF (infinito), <strong>precisamente</strong> impone che i requisiti IEEE relativi ai valori NaN e inf siano rispettati.</span><span class="sxs-lookup"><span data-stu-id="d76e5-132">Where the compiler might have used fast math operations that don't account for NaN (not a number) and INF (infinite) values, <strong>precise</strong> forces IEEE requirements concerning NaN and INF values to be respected.</span></span> <span data-ttu-id="d76e5-133">Senza alcuna <strong>precisione</strong>, queste ottimizzazioni e operazioni matematiche non sono sicure IEEE.</span><span class="sxs-lookup"><span data-stu-id="d76e5-133">Without <strong>precise</strong>, these optimizations and mathematical operations are not IEEE safe.</span></span>
*   <span data-ttu-id="d76e5-134">Se si qualifica una variabile <strong>precisa</strong> , le operazioni che usano la variabile sono <strong>precise</strong>.</span><span class="sxs-lookup"><span data-stu-id="d76e5-134">Qualifying a variable <strong>precise</strong> doesn't make operations that use the variable <strong>precise</strong>.</span></span> <span data-ttu-id="d76e5-135">Dato che la <strong>precisione</strong> viene propagata solo alle operazioni che contribuiscono ai valori assegnati alla variabile qualificata <strong>precisa</strong>, l'esecuzione corretta dei <strong>calcoli</strong> desiderati può risultare complessa, quindi è consigliabile contrassegnare gli output dello shader in modo <strong>preciso</strong> direttamente dove vengono dichiarati, sia che si trovino in un campo della struttura, che in un parametro di output o il tipo restituito della funzione entry.</span><span class="sxs-lookup"><span data-stu-id="d76e5-135">Since <strong>precise</strong> propagates only to operations that contribute to the values that are assigned to the <strong>precise</strong>-qualified variable, correctly making desired calculations <strong>precise</strong> can be tricky, so we recommended that you mark the shader outputs <strong>precise</strong> directly where you declare them, whether that's on a structure field, or on an output parameter, or the return type of the entry function.</span></span>

<span data-ttu-id="d76e5-136">La possibilità di controllare le ottimizzazioni in questo modo mantiene l'invarianza dei risultati per la variabile di output modificata disabilitando le ottimizzazioni che potrebbero influire sui risultati finali a causa delle differenze nelle differenze di precisione accumulate.</span><span class="sxs-lookup"><span data-stu-id="d76e5-136">The ability to control optimizations in this way maintains result invariance for the modified output variable by disabling optimizations that might affect final results due to differences in accumulated precision differences.</span></span> <span data-ttu-id="d76e5-137">È utile quando si desidera che gli shader per lo schema a mosaico mantengano le cuciture delle patch con l'acqua o i valori di profondità corrispondenti a più passaggi.</span><span class="sxs-lookup"><span data-stu-id="d76e5-137">It is useful when you want shaders for tessellation to maintain water-tight patch seams or match depth values over multiple passes.</span></span>

<span data-ttu-id="d76e5-138">[Codice di esempio](https://github.com/microsoft/DirectXShaderCompiler/blob/master/tools/clang/test/HLSLFileCheck/hlsl/types/modifiers/precise/precise4.hlsl):</span><span class="sxs-lookup"><span data-stu-id="d76e5-138">[Sample code](https://github.com/microsoft/DirectXShaderCompiler/blob/master/tools/clang/test/HLSLFileCheck/hlsl/types/modifiers/precise/precise4.hlsl):</span></span> 
```HLSL
matrix g_mWorldViewProjection;
void main(in float3 InPos : Position, out precise float4 OutPos : SV_Position)
{
  // operation is precise because it contributes to the precise parameter OutPos
  OutPos = mul( float4( InPos, 1.0 ), g_mWorldViewProjection );
}
```
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="d76e5-139"><strong>condiviso</strong></span><span class="sxs-lookup"><span data-stu-id="d76e5-139"><strong>shared</strong></span></span></td>
<td><span data-ttu-id="d76e5-140">Contrassegnare una variabile per la condivisione tra gli effetti; si tratta di un suggerimento per il compilatore.</span><span class="sxs-lookup"><span data-stu-id="d76e5-140">Mark a variable for sharing between effects; this is a hint to the compiler.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d76e5-141"><strong>groupshared</strong></span><span class="sxs-lookup"><span data-stu-id="d76e5-141"><strong>groupshared</strong></span></span></td>
<td><span data-ttu-id="d76e5-142">Contrassegnare una variabile per la memoria condivisa del gruppo di thread per i compute shader.</span><span class="sxs-lookup"><span data-stu-id="d76e5-142">Mark a variable for thread-group-shared memory for compute shaders.</span></span> <span data-ttu-id="d76e5-143">In D3D10 la dimensione totale massima di tutte le variabili con la classe di archiviazione groupshared è 16KB, in D3D11 la dimensione massima è 32 KB.</span><span class="sxs-lookup"><span data-stu-id="d76e5-143">In D3D10 the maximum total size of all variables with the groupshared storage class is 16kb, in D3D11 the maximum size is 32kb.</span></span> <span data-ttu-id="d76e5-144">Vedere gli esempi.</span><span class="sxs-lookup"><span data-stu-id="d76e5-144">See examples.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d76e5-145"><strong>static</strong></span><span class="sxs-lookup"><span data-stu-id="d76e5-145"><strong>static</strong></span></span></td>
<td><span data-ttu-id="d76e5-146">Contrassegnare una variabile locale in modo che venga inizializzata una sola volta e venga mantenute tra le chiamate di funzione.</span><span class="sxs-lookup"><span data-stu-id="d76e5-146">Mark a local variable so that it is initialized one time and persists between function calls.</span></span> <span data-ttu-id="d76e5-147">Se la dichiarazione non include un inizializzatore, il valore viene impostato su zero.</span><span class="sxs-lookup"><span data-stu-id="d76e5-147">If the declaration does not include an initializer, the value is set to zero.</span></span> <span data-ttu-id="d76e5-148">Una variabile globale contrassegnata come <strong>statica</strong> non è visibile per un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d76e5-148">A global variable marked <strong>static</strong> is not visible to an application.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d76e5-149"><strong>Uniform</strong></span><span class="sxs-lookup"><span data-stu-id="d76e5-149"><strong>uniform</strong></span></span></td>
<td><span data-ttu-id="d76e5-150">Contrassegnare una variabile i cui dati sono costanti durante l'esecuzione di uno shader, ad esempio un colore del materiale in un vertex shader. per impostazione predefinita, le variabili globali sono considerate <strong>uniformi</strong> .</span><span class="sxs-lookup"><span data-stu-id="d76e5-150">Mark a variable whose data is constant throughout the execution of a shader (such as a material color in a vertex shader); global variables are considered <strong>uniform</strong> by default.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d76e5-151"><strong>volatile</strong></span><span class="sxs-lookup"><span data-stu-id="d76e5-151"><strong>volatile</strong></span></span></td>
<td><span data-ttu-id="d76e5-152">Contrassegna una variabile che cambia di frequente; si tratta di un suggerimento per il compilatore.</span><span class="sxs-lookup"><span data-stu-id="d76e5-152">Mark a variable that changes frequently; this is a hint to the compiler.</span></span> <span data-ttu-id="d76e5-153">Questo modificatore di classe di archiviazione si applica solo a una variabile locale.</span><span class="sxs-lookup"><span data-stu-id="d76e5-153">This storage class modifier only applies to a local variable.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="d76e5-154">Il compilatore HLSL attualmente ignora questo modificatore di classe di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="d76e5-154">The HLSL compiler currently ignores this storage class modifier.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="d76e5-155"><span id="Type_Modifier"></span><span id="type_modifier"></span><span id="TYPE_MODIFIER"></span>*\_Modificatore di tipo*</span><span class="sxs-lookup"><span data-stu-id="d76e5-155"><span id="Type_Modifier"></span><span id="type_modifier"></span><span id="TYPE_MODIFIER"></span>*Type\_Modifier*</span></span>
</dt> <dd>

<span data-ttu-id="d76e5-156">Modificatore di tipo variabile facoltativo.</span><span class="sxs-lookup"><span data-stu-id="d76e5-156">Optional variable-type modifier.</span></span>



| <span data-ttu-id="d76e5-157">Valore</span><span class="sxs-lookup"><span data-stu-id="d76e5-157">Value</span></span>             | <span data-ttu-id="d76e5-158">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d76e5-158">Description</span></span>                                                                                                                                                                                                                                  |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d76e5-159">**const**</span><span class="sxs-lookup"><span data-stu-id="d76e5-159">**const**</span></span>         | <span data-ttu-id="d76e5-160">Contrassegnare una variabile che non può essere modificata da uno shader, pertanto deve essere inizializzata nella dichiarazione di variabile.</span><span class="sxs-lookup"><span data-stu-id="d76e5-160">Mark a variable that cannot be changed by a shader, therefore, it must be initialized in the variable declaration.</span></span> <span data-ttu-id="d76e5-161">Le variabili globali sono considerate **const** per impostazione predefinita (Elimina questo comportamento fornendo il flag/GEC al compilatore).</span><span class="sxs-lookup"><span data-stu-id="d76e5-161">Global variables are considered **const** by default (suppress this behavior by supplying the /Gec flag to the compiler).</span></span> |
| <span data-ttu-id="d76e5-162">**riga \_ principale**</span><span class="sxs-lookup"><span data-stu-id="d76e5-162">**row\_major**</span></span>    | <span data-ttu-id="d76e5-163">Contrassegnare una variabile che archivia quattro componenti in una singola riga in modo che possano essere archiviati in un unico registro costante.</span><span class="sxs-lookup"><span data-stu-id="d76e5-163">Mark a variable that stores four components in a single row so they can be stored in a single constant register.</span></span>                                                                                                                             |
| <span data-ttu-id="d76e5-164">**colonna \_ principale**</span><span class="sxs-lookup"><span data-stu-id="d76e5-164">**column\_major**</span></span> | <span data-ttu-id="d76e5-165">Contrassegnare una variabile che archivia 4 componenti in una singola colonna per ottimizzare la matematica della matrice.</span><span class="sxs-lookup"><span data-stu-id="d76e5-165">Mark a variable that stores 4 components in a single column to optimize matrix math.</span></span>                                                                                                                                                         |



 

> [!Note]  
> <span data-ttu-id="d76e5-166">Se non si specifica un valore del modificatore di tipo, il compilatore usa la **colonna \_ Major** come valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="d76e5-166">If you do not specify a type-modifier value, the compiler uses **column\_major** as the default value.</span></span>

 

</dd> <dt>

<span data-ttu-id="d76e5-167"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>*Tipo*</span><span class="sxs-lookup"><span data-stu-id="d76e5-167"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>*Type*</span></span>
</dt> <dd>

<span data-ttu-id="d76e5-168">Qualsiasi tipo di HLSL elencato in [tipi di dati (DirectX HLSL)](dx-graphics-hlsl-data-types.md).</span><span class="sxs-lookup"><span data-stu-id="d76e5-168">Any HLSL type listed in [Data Types (DirectX HLSL)](dx-graphics-hlsl-data-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="d76e5-169"><span id="Name_Index_"></span><span id="name_index_"></span><span id="NAME_INDEX_"></span>*Nome* \[ *Indice* di\]</span><span class="sxs-lookup"><span data-stu-id="d76e5-169"><span id="Name_Index_"></span><span id="name_index_"></span><span id="NAME_INDEX_"></span>*Name*\[*Index*\]</span></span>
</dt> <dd>

<span data-ttu-id="d76e5-170">Stringa ASCII che identifica in modo univoco una variabile shader.</span><span class="sxs-lookup"><span data-stu-id="d76e5-170">ASCII string that uniquely identifies a shader variable.</span></span> <span data-ttu-id="d76e5-171">Per definire una matrice facoltativa, usare **index** per la dimensione della matrice, ovvero un numero intero positivo = 1.</span><span class="sxs-lookup"><span data-stu-id="d76e5-171">To define an optional array, use **index** for the array size, which is a positive integer = 1.</span></span>

</dd> <dt>

<span data-ttu-id="d76e5-172"><span id="Semantic"></span><span id="semantic"></span><span id="SEMANTIC"></span>*Semantica*</span><span class="sxs-lookup"><span data-stu-id="d76e5-172"><span id="Semantic"></span><span id="semantic"></span><span id="SEMANTIC"></span>*Semantic*</span></span>
</dt> <dd>

<span data-ttu-id="d76e5-173">Informazioni facoltative sull'utilizzo dei parametri, utilizzate dal compilatore per collegare gli input e gli output dello shader.</span><span class="sxs-lookup"><span data-stu-id="d76e5-173">Optional parameter-usage information, used by the compiler to link shader inputs and outputs.</span></span> <span data-ttu-id="d76e5-174">Per gli shader Vertex e pixel sono disponibili diverse [semantiche](dx-graphics-hlsl-semantics.md) predefinite.</span><span class="sxs-lookup"><span data-stu-id="d76e5-174">There are several predefined [semantics](dx-graphics-hlsl-semantics.md) for vertex and pixel shaders.</span></span> <span data-ttu-id="d76e5-175">Il compilatore ignora la semantica a meno che non vengano dichiarate in una variabile globale o un parametro passato a uno shader.</span><span class="sxs-lookup"><span data-stu-id="d76e5-175">The compiler ignores semantics unless they are declared on a global variable, or a parameter passed into a shader.</span></span>

</dd> <dt>

<span data-ttu-id="d76e5-176"><span id="Packoffset"></span><span id="packoffset"></span><span id="PACKOFFSET"></span>*Packoffset*</span><span class="sxs-lookup"><span data-stu-id="d76e5-176"><span id="Packoffset"></span><span id="packoffset"></span><span id="PACKOFFSET"></span>*Packoffset*</span></span>
</dt> <dd>

<span data-ttu-id="d76e5-177">Parola chiave facoltativa per la compressione manuale delle costanti shader.</span><span class="sxs-lookup"><span data-stu-id="d76e5-177">Optional keyword for manually packing shader constants.</span></span> <span data-ttu-id="d76e5-178">Vedere [packoffset (DirectX HLSL)](dx-graphics-hlsl-variable-packoffset.md).</span><span class="sxs-lookup"><span data-stu-id="d76e5-178">See [packoffset (DirectX HLSL)](dx-graphics-hlsl-variable-packoffset.md).</span></span>

</dd> <dt>

<span data-ttu-id="d76e5-179"><span id="Register"></span><span id="register"></span><span id="REGISTER"></span>*Registro*</span><span class="sxs-lookup"><span data-stu-id="d76e5-179"><span id="Register"></span><span id="register"></span><span id="REGISTER"></span>*Register*</span></span>
</dt> <dd>

<span data-ttu-id="d76e5-180">Parola chiave facoltativa per l'assegnazione manuale di una variabile shader a un particolare registro.</span><span class="sxs-lookup"><span data-stu-id="d76e5-180">Optional keyword for manually assigning a shader variable to a particular register.</span></span> <span data-ttu-id="d76e5-181">Vedere [Register (DirectX HLSL)](dx-graphics-hlsl-variable-register.md).</span><span class="sxs-lookup"><span data-stu-id="d76e5-181">See [register (DirectX HLSL)](dx-graphics-hlsl-variable-register.md).</span></span>

</dd> <dt>

<span data-ttu-id="d76e5-182"><span id="Annotation_s_"></span><span id="annotation_s_"></span><span id="ANNOTATION_S_"></span>*Annotazioni*</span><span class="sxs-lookup"><span data-stu-id="d76e5-182"><span id="Annotation_s_"></span><span id="annotation_s_"></span><span id="ANNOTATION_S_"></span>*Annotation(s)*</span></span>
</dt> <dd>

<span data-ttu-id="d76e5-183">Metadati facoltativi, sotto forma di stringa, collegati a una variabile globale.</span><span class="sxs-lookup"><span data-stu-id="d76e5-183">Optional metadata, in the form of a string, attached to a global variable.</span></span> <span data-ttu-id="d76e5-184">Un'annotazione viene utilizzata dal framework degli effetti e ignorata da HLSL; per visualizzare una sintassi più dettagliata, vedere [sintassi dell'annotazione](/windows/desktop/direct3d10/d3d10-effect-annotation-syntax).</span><span class="sxs-lookup"><span data-stu-id="d76e5-184">An annotation is used by the effect framework and ignored by HLSL; to see more detailed syntax, see [annotation syntax](/windows/desktop/direct3d10/d3d10-effect-annotation-syntax).</span></span>

</dd> <dt>

<span data-ttu-id="d76e5-185"><span id="Initial_Value"></span><span id="initial_value"></span><span id="INITIAL_VALUE"></span>*\_Valore iniziale*</span><span class="sxs-lookup"><span data-stu-id="d76e5-185"><span id="Initial_Value"></span><span id="initial_value"></span><span id="INITIAL_VALUE"></span>*Initial\_Value*</span></span>
</dt> <dd>

<span data-ttu-id="d76e5-186">Valore iniziale facoltativo/i. il numero di valori deve corrispondere al numero di componenti nel *tipo*.</span><span class="sxs-lookup"><span data-stu-id="d76e5-186">Optional initial value(s); the number of values should match the number of components in *Type*.</span></span> <span data-ttu-id="d76e5-187">Ogni variabile globale contrassegnata come **extern** deve essere inizializzata con un valore letterale. ogni variabile contrassegnata come **statica** deve essere inizializzata con una costante.</span><span class="sxs-lookup"><span data-stu-id="d76e5-187">Each global variable marked **extern** must be initialized with a literal value; each variable marked **static** must be initialized with a constant.</span></span>

<span data-ttu-id="d76e5-188">Le variabili globali non contrassegnate come **static** o **extern** non vengono compilate nello shader.</span><span class="sxs-lookup"><span data-stu-id="d76e5-188">Global variables that are not marked **static** or **extern** are not compiled into the shader.</span></span> <span data-ttu-id="d76e5-189">Il compilatore non imposta automaticamente i valori predefiniti per le variabili globali e non può usarli nelle ottimizzazioni.</span><span class="sxs-lookup"><span data-stu-id="d76e5-189">The compiler does not automatically set default values for global variables and cannot use them in optimizations.</span></span> <span data-ttu-id="d76e5-190">Per inizializzare questo tipo di variabile globale, utilizzare la reflection per ottenere il relativo valore e quindi copiare il valore in un buffer costante.</span><span class="sxs-lookup"><span data-stu-id="d76e5-190">To initialize this type of global variable, use reflection to get its value and then copy the value to a constant buffer.</span></span> <span data-ttu-id="d76e5-191">Ad esempio, è possibile usare il metodo [**ID3D11ShaderReflection:: GetVariableByName**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflection-getvariablebyname) per ottenere la variabile, usare il metodo [**ID3D11ShaderReflectionVariable:: getdesc**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflectionvariable-getdesc) per ottenere la descrizione della variabile shader e ottenere il valore iniziale dal membro **DefaultValue** della struttura [**\_ \_ \_ desc della variabile di d3d11 shader**](/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_shader_variable_desc) .</span><span class="sxs-lookup"><span data-stu-id="d76e5-191">For example, you can use the [**ID3D11ShaderReflection::GetVariableByName**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflection-getvariablebyname) method to get the variable, use the [**ID3D11ShaderReflectionVariable::GetDesc**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflectionvariable-getdesc) method to get the shader-variable description, and get the initial value from the **DefaultValue** member of the [**D3D11\_SHADER\_VARIABLE\_DESC**](/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_shader_variable_desc) structure.</span></span> <span data-ttu-id="d76e5-192">Per copiare il valore nel buffer costante, è necessario assicurarsi che il buffer sia stato creato con accesso in scrittura alla CPU ([**\_ \_ \_ scrittura di accesso alla CPU d3d11**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_cpu_access_flag)).</span><span class="sxs-lookup"><span data-stu-id="d76e5-192">To copy the value to the constant buffer, you must ensure that the buffer was created with CPU write access ([**D3D11\_CPU\_ACCESS\_WRITE**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_cpu_access_flag)).</span></span> <span data-ttu-id="d76e5-193">Per altre informazioni su come creare un buffer costante, vedere [procedura: creare un buffer costante](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-constant-how-to).</span><span class="sxs-lookup"><span data-stu-id="d76e5-193">For more information about how to create a constant buffer, see [How to: Create a Constant Buffer](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-constant-how-to).</span></span>

<span data-ttu-id="d76e5-194">È anche possibile usare il [Framework degli effetti](../direct3d11/d3d11-graphics-programming-guide-effects.md) per elaborare automaticamente la reflection e impostare il valore iniziale.</span><span class="sxs-lookup"><span data-stu-id="d76e5-194">You can also use the [effects framework](../direct3d11/d3d11-graphics-programming-guide-effects.md) to automatically process the reflecting and setting the initial value.</span></span> <span data-ttu-id="d76e5-195">Ad esempio, è possibile usare il metodo [**ID3DX11EffectPass:: Apply**](/windows/desktop/direct3d11/id3dx11effectpass-apply) .</span><span class="sxs-lookup"><span data-stu-id="d76e5-195">For example, you can use the [**ID3DX11EffectPass::Apply**](/windows/desktop/direct3d11/id3dx11effectpass-apply) method.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="d76e5-196">Esempio</span><span class="sxs-lookup"><span data-stu-id="d76e5-196">Examples</span></span>

<span data-ttu-id="d76e5-197">Di seguito sono riportati alcuni esempi di dichiarazioni di variabili shader.</span><span class="sxs-lookup"><span data-stu-id="d76e5-197">Here are several examples of shader-variable declarations.</span></span>


```
float fVar;
```




```
float4 color;
float fVar = 3.1f;

int iVar[3];

int iVar[3] = {1,2,3};

uniform float4 position : SV_POSITION; 
const float4 lightDirection = {0,0,1};
      
```



### <a name="group-shared"></a><span data-ttu-id="d76e5-198">Gruppo condiviso</span><span class="sxs-lookup"><span data-stu-id="d76e5-198">Group Shared</span></span>

<span data-ttu-id="d76e5-199">HLSL consente ai thread di un compute shader di scambiare valori tramite memoria condivisa.</span><span class="sxs-lookup"><span data-stu-id="d76e5-199">HLSL enables threads of a compute shader to exchange values via shared memory.</span></span> <span data-ttu-id="d76e5-200">HLSL fornisce le primitive di barriera, ad esempio [**GroupMemoryBarrierWithGroupSync**](groupmemorybarrierwithgroupsync.md), e così via, per garantire l'ordinamento corretto delle letture e scritture nella memoria condivisa nello shader ed evitare le gare di dati.</span><span class="sxs-lookup"><span data-stu-id="d76e5-200">HLSL provides barrier primitives such as [**GroupMemoryBarrierWithGroupSync**](groupmemorybarrierwithgroupsync.md), and so on to ensure the correct ordering of reads and writes to shared memory in the shader and to avoid data races.</span></span>

> [!Note]  
> <span data-ttu-id="d76e5-201">L'hardware esegue thread in gruppi (distorsioni o front-end) e la sincronizzazione delle barriere può talvolta essere omessa per migliorare le prestazioni quando solo la sincronizzazione di thread appartenenti allo stesso gruppo è corretta.</span><span class="sxs-lookup"><span data-stu-id="d76e5-201">Hardware executes threads in groups (warps or wave-fronts), and barrier synchronization can sometimes be omitted to increase performance when only synchronizing threads that belong to the same group is correct.</span></span> <span data-ttu-id="d76e5-202">Questa omissione viene tuttavia sconsigliata per i motivi seguenti:</span><span class="sxs-lookup"><span data-stu-id="d76e5-202">But we highly discourage this omission for these reasons:</span></span>
>
> -   <span data-ttu-id="d76e5-203">Questa omissione genera codice non portabile, che potrebbe non funzionare su hardware e non funziona in rasterizzatori software che in genere eseguono i thread in gruppi più piccoli.</span><span class="sxs-lookup"><span data-stu-id="d76e5-203">This omission results in non-portable code, which might not work on some hardware and doesn't work on software rasterizers that typically execute threads in smaller groups.</span></span>
> -   <span data-ttu-id="d76e5-204">I miglioramenti delle prestazioni che è possibile ottenere con questa omissione saranno minori rispetto all'uso della barriera all-thread.</span><span class="sxs-lookup"><span data-stu-id="d76e5-204">The performance improvements that you might achieve with this omission will be minor compared to using all-thread barrier.</span></span>

 

<span data-ttu-id="d76e5-205">In Direct3D 10 non viene sincronizzato alcun thread durante la scrittura in **groupshared**, quindi questo significa che ogni thread è limitato a una singola posizione in una matrice per la scrittura.</span><span class="sxs-lookup"><span data-stu-id="d76e5-205">In Direct3D 10 there is no synchronization of threads when writing to **groupshared**, so this means that each thread is limited to a single location in an array for writing.</span></span> <span data-ttu-id="d76e5-206">Usare il valore del sistema [SV \_ groupIndex](dx-graphics-hlsl-semantics.md) per eseguire l'indicizzazione in questa matrice durante la scrittura per assicurarsi che non ci siano due thread in conflitto.</span><span class="sxs-lookup"><span data-stu-id="d76e5-206">Use the [SV\_GroupIndex](dx-graphics-hlsl-semantics.md) system value to index into this array when writing to ensure that no two threads can collide.</span></span> <span data-ttu-id="d76e5-207">In termini di lettura, tutti i thread hanno accesso all'intera matrice per la lettura.</span><span class="sxs-lookup"><span data-stu-id="d76e5-207">In terms of reading, all threads have access to the entire array for reading.</span></span>


```
struct GSData
{
    float4 Color;
    float Factor;
}

groupshared GSData data[5*5*1];

[numthreads(5,5,1)]
void main( uint index : SV_GroupIndex )
{
    data[index].Color = (float4)0;
    data[index].Factor = 2.0f;
    GroupMemoryBarrierWithGroupSync();
    ...
}
```



### <a name="packing"></a><span data-ttu-id="d76e5-208">Compressione</span><span class="sxs-lookup"><span data-stu-id="d76e5-208">Packing</span></span>

<span data-ttu-id="d76e5-209">Comprimere i sottocomponenti di vettori e scalari la cui dimensione è sufficientemente grande da impedire i limiti del registro di attraversamento.</span><span class="sxs-lookup"><span data-stu-id="d76e5-209">Pack subcomponents of vectors and scalars whose size is large enough to prevent crossing register boundarys.</span></span> <span data-ttu-id="d76e5-210">Ad esempio, sono tutti validi:</span><span class="sxs-lookup"><span data-stu-id="d76e5-210">For example, these are all valid:</span></span>


```
cbuffer MyBuffer
{
    float4 Element1 : packoffset(c0);
    float1 Element2 : packoffset(c1);
    float1 Element3 : packoffset(c1.y);
}
        
```



<span data-ttu-id="d76e5-211">Impossibile combinare tipi di compressione.</span><span class="sxs-lookup"><span data-stu-id="d76e5-211">Cannot mix packing types.</span></span>

<span data-ttu-id="d76e5-212">Analogamente alla parola chiave register, un packoffset può essere specifico della destinazione.</span><span class="sxs-lookup"><span data-stu-id="d76e5-212">Like the register keyword, a packoffset can be target specific.</span></span> <span data-ttu-id="d76e5-213">La compressione dei sottocomponenti è disponibile solo con la parola chiave packoffset, non con la parola chiave register.</span><span class="sxs-lookup"><span data-stu-id="d76e5-213">Subcomponent packing is only available with the packoffset keyword, not the register keyword.</span></span> <span data-ttu-id="d76e5-214">All'interno di una dichiarazione cbuffer, la parola chiave register viene ignorata per le destinazioni Direct3D 10, perché si presuppone che sia per la compatibilità multipiattaforma.</span><span class="sxs-lookup"><span data-stu-id="d76e5-214">Inside a cbuffer declaration, the register keyword is ignored for Direct3D 10 targets as it is assumed to be for cross-platform compatibility.</span></span>

<span data-ttu-id="d76e5-215">Gli elementi compressi possono sovrapporsi e il compilatore non restituirà alcun errore o avviso.</span><span class="sxs-lookup"><span data-stu-id="d76e5-215">Packed elements may overlap and the compiler will give no error or warning.</span></span> <span data-ttu-id="d76e5-216">In questo esempio, element2 e Element3 si sovrappongono con element1. x e element1. y.</span><span class="sxs-lookup"><span data-stu-id="d76e5-216">In this example, Element2 and Element3 will overlap with Element1.x and Element1.y.</span></span>


```
cbuffer MyBuffer
{
    float4 Element1 : packoffset(c0);
    float1 Element2 : packoffset(c0);
    float1 Element3 : packoffset(c0.y);
}
        
```



<span data-ttu-id="d76e5-217">Un esempio che usa packoffset è: [HLSLWithoutFX10 Sample](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="d76e5-217">A sample that uses packoffset is: [HLSLWithoutFX10 Sample](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d76e5-218">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d76e5-218">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d76e5-219">Variabili (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d76e5-219">Variables (DirectX HLSL)</span></span>](dx-graphics-hlsl-variables.md)
</dt> </dl>

 

