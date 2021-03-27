---
title: Costanti dello shader (HLSL)
description: Nel modello di Shader 4, le costanti dello shader vengono archiviate in una o più risorse del buffer in memoria.
ms.assetid: 89fe874a-8009-4901-bebe-2d9e45f894bb
keywords:
- cbuffer
- tbuffer
- buffer costante
- buffer trama
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a1b78da747a248bf4bb5774add1bf97f14f048c4
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "103739431"
---
# <a name="shader-constants-hlsl"></a><span data-ttu-id="0bea3-107">Costanti dello shader (HLSL)</span><span class="sxs-lookup"><span data-stu-id="0bea3-107">Shader Constants (HLSL)</span></span>

<span data-ttu-id="0bea3-108">Nel modello di Shader 4, le costanti dello shader vengono archiviate in una o più risorse del buffer in memoria.</span><span class="sxs-lookup"><span data-stu-id="0bea3-108">In Shader Model 4, shader constants are stored in one or more buffer resources in memory.</span></span> <span data-ttu-id="0bea3-109">Possono essere organizzati in due tipi di buffer: buffer costanti (cBuffers) e buffer di trama (tbuffers).</span><span class="sxs-lookup"><span data-stu-id="0bea3-109">They can be organized into two types of buffers: constant buffers (cbuffers) and texture buffers (tbuffers).</span></span> <span data-ttu-id="0bea3-110">I buffer costanti sono ottimizzati per l'utilizzo costante-variabile, caratterizzato dall'accesso con latenza inferiore e dall'aggiornamento più frequente dalla CPU.</span><span class="sxs-lookup"><span data-stu-id="0bea3-110">Constant buffers are optimized for constant-variable usage, which is characterized by lower-latency access and more frequent update from the CPU.</span></span> <span data-ttu-id="0bea3-111">Per questo motivo, per queste risorse si applicano le restrizioni aggiuntive relative a dimensioni, layout e accesso.</span><span class="sxs-lookup"><span data-stu-id="0bea3-111">For this reason, additional size, layout, and access restrictions apply to these resources.</span></span> <span data-ttu-id="0bea3-112">I buffer di trama sono accessibili come le trame ed eseguono le prestazioni migliori per i dati indicizzati in modo arbitrario.</span><span class="sxs-lookup"><span data-stu-id="0bea3-112">Texture buffers are accessed like textures and perform better for arbitrarily indexed data.</span></span> <span data-ttu-id="0bea3-113">Indipendentemente dal tipo di risorsa in uso, non esiste alcun limite al numero di buffer costanti o di buffer di trama che un'applicazione può creare.</span><span class="sxs-lookup"><span data-stu-id="0bea3-113">Regardless of which type of resource you use, there is no limit to the number of constant buffers or texture buffers an application can create.</span></span>

<span data-ttu-id="0bea3-114">La dichiarazione di un buffer costante o di un buffer di trama ha un aspetto molto simile a una dichiarazione di struttura in C, con l'aggiunta delle parole chiave **Register** e **packoffset** per l'assegnazione manuale di registri o di pacchetti di dati.</span><span class="sxs-lookup"><span data-stu-id="0bea3-114">Declaring a constant buffer or a texture buffer looks very much like a structure declaration in C, with the addition of the **register** and **packoffset** keywords for manually assigning registers or packing data.</span></span>



|                                                                                                                         |
|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0bea3-115">*BufferType* \[ *Nome* \] \[: **Register**(b \# ) \] { *VariableDeclaration* \[ : **packoffset**(c \# . xyzw) \] ;      ... };</span><span class="sxs-lookup"><span data-stu-id="0bea3-115">*BufferType* \[*Name*\] \[: **register**(b\#)\] {     *VariableDeclaration* \[: **packoffset**(c\#.xyzw)\];      ... };</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="0bea3-116">Parametri</span><span class="sxs-lookup"><span data-stu-id="0bea3-116">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0bea3-117"><span id="BufferType"></span><span id="buffertype"></span><span id="BUFFERTYPE"></span>*BufferType*</span><span class="sxs-lookup"><span data-stu-id="0bea3-117"><span id="BufferType"></span><span id="buffertype"></span><span id="BUFFERTYPE"></span>*BufferType*</span></span>
</dt> <dd>

<span data-ttu-id="0bea3-118">\[nel \] tipo di buffer.</span><span class="sxs-lookup"><span data-stu-id="0bea3-118">\[in\] The buffer type.</span></span>



| <span data-ttu-id="0bea3-119">BufferType</span><span class="sxs-lookup"><span data-stu-id="0bea3-119">BufferType</span></span> | <span data-ttu-id="0bea3-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0bea3-120">Description</span></span>     |
|------------|-----------------|
| <span data-ttu-id="0bea3-121">cbuffer</span><span class="sxs-lookup"><span data-stu-id="0bea3-121">cbuffer</span></span>    | <span data-ttu-id="0bea3-122">buffer costante</span><span class="sxs-lookup"><span data-stu-id="0bea3-122">constant buffer</span></span> |
| <span data-ttu-id="0bea3-123">tbuffer</span><span class="sxs-lookup"><span data-stu-id="0bea3-123">tbuffer</span></span>    | <span data-ttu-id="0bea3-124">buffer trama</span><span class="sxs-lookup"><span data-stu-id="0bea3-124">texture buffer</span></span>  |



 

</dd> <dt>

<span data-ttu-id="0bea3-125"><span id="Name"></span><span id="name"></span><span id="NAME"></span>*Nome*</span><span class="sxs-lookup"><span data-stu-id="0bea3-125"><span id="Name"></span><span id="name"></span><span id="NAME"></span>*Name*</span></span>
</dt> <dd>

<span data-ttu-id="0bea3-126">\[in \] una stringa ASCII facoltativa contenente un nome di buffer univoco.</span><span class="sxs-lookup"><span data-stu-id="0bea3-126">\[in\] Optional, ASCII string containing a unique buffer name.</span></span>

</dd> <dt>

<span data-ttu-id="0bea3-127"><span id="register_b__"></span><span id="REGISTER_B__"></span>**registra**(b \# )</span><span class="sxs-lookup"><span data-stu-id="0bea3-127"><span id="register_b__"></span><span id="REGISTER_B__"></span>**register**(b\#)</span></span>
</dt> <dd>

<span data-ttu-id="0bea3-128">\[nella \] parola chiave Optional utilizzata per inserire manualmente i dati costanti.</span><span class="sxs-lookup"><span data-stu-id="0bea3-128">\[in\] Optional keyword, used to manually pack constant data.</span></span> <span data-ttu-id="0bea3-129">Le costanti possono essere compresse in un registro solo in un buffer costante, dove il registro iniziale viene fornito dal numero di registro ( *\#* ).</span><span class="sxs-lookup"><span data-stu-id="0bea3-129">Constants can be packed in a register only in a constant buffer, where the starting register is given by the register number (*\#*).</span></span>

</dd> <dt>

<span data-ttu-id="0bea3-130"><span id="VariableDeclaration"></span><span id="variabledeclaration"></span><span id="VARIABLEDECLARATION"></span>*VariableDeclaration*</span><span class="sxs-lookup"><span data-stu-id="0bea3-130"><span id="VariableDeclaration"></span><span id="variabledeclaration"></span><span id="VARIABLEDECLARATION"></span>*VariableDeclaration*</span></span>
</dt> <dd>

<span data-ttu-id="0bea3-131">\[nella \] dichiarazione di variabile, simile a una dichiarazione di membro di struttura.</span><span class="sxs-lookup"><span data-stu-id="0bea3-131">\[in\] Variable declaration, similar to a structure member declaration.</span></span> <span data-ttu-id="0bea3-132">Può trattarsi di qualsiasi tipo di HLSL o oggetto effetto (ad eccezione di una trama o di un oggetto campionatore).</span><span class="sxs-lookup"><span data-stu-id="0bea3-132">This can be any HLSL type or effect object (except a texture or a sampler object).</span></span>

</dd> <dt>

<span data-ttu-id="0bea3-133"><span id="packoffset_c_.xyzw_"></span><span id="PACKOFFSET_C_.XYZW_"></span>**packoffset**(c \# . xyzw)</span><span class="sxs-lookup"><span data-stu-id="0bea3-133"><span id="packoffset_c_.xyzw_"></span><span id="PACKOFFSET_C_.XYZW_"></span>**packoffset**(c\#.xyzw)</span></span>
</dt> <dd>

<span data-ttu-id="0bea3-134">\[nella \] parola chiave Optional utilizzata per inserire manualmente i dati costanti.</span><span class="sxs-lookup"><span data-stu-id="0bea3-134">\[in\] Optional keyword, used to manually pack constant data.</span></span> <span data-ttu-id="0bea3-135">Le costanti possono essere compresse in qualsiasi buffer costante, in cui il numero di registro è fornito da ( *\#* ).</span><span class="sxs-lookup"><span data-stu-id="0bea3-135">Constants can be packed in any constant buffer, where the register number is given by (*\#*).</span></span> <span data-ttu-id="0bea3-136">La compressione dei componenti secondari (usando xyzw swizzling) è disponibile per le costanti le cui dimensioni rientrano in un unico registro (non superare un limite di registro).</span><span class="sxs-lookup"><span data-stu-id="0bea3-136">Sub-component packing (using xyzw swizzling) is available for constants whose size fit within a single register (do not cross a register boundary).</span></span> <span data-ttu-id="0bea3-137">Ad esempio, un float4 non può essere compresso in un unico registro che inizia con il componente y, perché non si adatterebbe a un registro a quattro componenti.</span><span class="sxs-lookup"><span data-stu-id="0bea3-137">For instance, a float4 could not be packed in a single register starting with the y-component because it would not fit in a four-component register.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0bea3-138">Commenti</span><span class="sxs-lookup"><span data-stu-id="0bea3-138">Remarks</span></span>

<span data-ttu-id="0bea3-139">I buffer costanti consentono di ridurre la larghezza di banda necessaria per aggiornare le costanti dello shader consentendo il raggruppamento e il commit delle costanti dello shader, anziché eseguire chiamate singole per eseguire il commit di ogni costante separatamente.</span><span class="sxs-lookup"><span data-stu-id="0bea3-139">Constant buffers reduce the bandwidth required to update shader constants by allowing shader constants to be grouped together and committed at the same time rather than making individual calls to commit each constant separately.</span></span>

<span data-ttu-id="0bea3-140">Un buffer costante è una risorsa di buffer specializzata a cui si accede come un buffer.</span><span class="sxs-lookup"><span data-stu-id="0bea3-140">A constant buffer is a specialized buffer resource that is accessed like a buffer.</span></span> <span data-ttu-id="0bea3-141">Ogni buffer costante può avere fino a 4096 [vettori](dx-graphics-hlsl-vector.md); ogni vettore contiene valori fino a 4 32 bit.</span><span class="sxs-lookup"><span data-stu-id="0bea3-141">Each constant buffer can hold up to 4096 [vectors](dx-graphics-hlsl-vector.md); each vector contains up to four 32-bit values.</span></span> <span data-ttu-id="0bea3-142">È possibile associare fino a 14 buffer costanti per fase della pipeline. 2 slot aggiuntivi sono riservati per uso interno.</span><span class="sxs-lookup"><span data-stu-id="0bea3-142">You can bind up to 14 constant buffers per pipeline stage (2 additional slots are reserved for internal use).</span></span>

<span data-ttu-id="0bea3-143">Un buffer di trama è una risorsa di buffer specializzata a cui si accede come una trama.</span><span class="sxs-lookup"><span data-stu-id="0bea3-143">A texture buffer is a specialized buffer resource that is accessed like a texture.</span></span> <span data-ttu-id="0bea3-144">L'accesso alla trama (rispetto all'accesso al buffer) può migliorare le prestazioni per i dati indicizzati in modo arbitrario.</span><span class="sxs-lookup"><span data-stu-id="0bea3-144">Texture access (as compared with buffer access) can have better performance for arbitrarily indexed data.</span></span> <span data-ttu-id="0bea3-145">È possibile associare fino a 128 buffer di trama per fase della pipeline.</span><span class="sxs-lookup"><span data-stu-id="0bea3-145">You can bind up to 128 texture buffers per pipeline stage.</span></span>

<span data-ttu-id="0bea3-146">Una risorsa di buffer è progettata per ridurre al minimo l'overhead dovuto all'impostazione delle costanti dello shader.</span><span class="sxs-lookup"><span data-stu-id="0bea3-146">A buffer resource is designed to minimize the overhead of setting shader constants.</span></span> <span data-ttu-id="0bea3-147">Il Framework degli effetti (vedere [**interfaccia ID3D10Effect**](/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effect)) gestirà l'aggiornamento dei buffer di trama e costanti, oppure è possibile usare l'API Direct3D per aggiornare i buffer. per informazioni, vedere [copia e accesso ai dati delle risorse (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-mapping) .</span><span class="sxs-lookup"><span data-stu-id="0bea3-147">The effect framework (see [**ID3D10Effect Interface**](/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effect)) will manage updating constant and texture buffers, or you can use the Direct3D API to update buffers (see [Copying and Accessing Resource Data (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-mapping) for information).</span></span> <span data-ttu-id="0bea3-148">Un'applicazione può anche copiare dati da un altro buffer, ad esempio una destinazione di rendering o una destinazione di output di flusso, in un buffer costante.</span><span class="sxs-lookup"><span data-stu-id="0bea3-148">An application can also copy data from another buffer (such as a render target or a stream-output target) into a constant buffer.</span></span>

<span data-ttu-id="0bea3-149">Per altre informazioni sull'uso di buffer costanti in un'applicazione D3D10, vedere [tipi di risorse (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) e [creazione di risorse di buffer (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-creating).</span><span class="sxs-lookup"><span data-stu-id="0bea3-149">For more info on using constant buffers in a D3D10 application, see [Resource Types (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) and [Creating Buffer Resources (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-creating).</span></span>

<span data-ttu-id="0bea3-150">Per informazioni su Morel sull'uso di buffer costanti in un'applicazione D3D11, vedere [Introduzione ai buffer in Direct3D 11](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-intro) e [procedura: creare un buffer costante](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-constant-how-to).</span><span class="sxs-lookup"><span data-stu-id="0bea3-150">For morel info on using constant buffers in a D3D11 application, see [Introduction to Buffers in Direct3D 11](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-intro) and [How to: Create a Constant Buffer](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-constant-how-to).</span></span>

<span data-ttu-id="0bea3-151">Un buffer costante non richiede l'associazione di una [vista](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-access-views) alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="0bea3-151">A constant buffer does not require a [view](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-access-views) to be bound to the pipeline.</span></span> <span data-ttu-id="0bea3-152">Un buffer di trama, tuttavia, richiede una visualizzazione e deve essere associato a uno slot di trama (oppure deve essere associato a [**SetTextureBuffer**](/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effectconstantbuffer-settexturebuffer) quando si utilizza un effetto).</span><span class="sxs-lookup"><span data-stu-id="0bea3-152">A texture buffer, however, requires a view and must be bound to a texture slot (or must be bound with [**SetTextureBuffer**](/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effectconstantbuffer-settexturebuffer) when using an effect).</span></span>

<span data-ttu-id="0bea3-153">Esistono due modi per comprimere i dati delle costanti: usando le parole chiave [Register (DirectX HLSL)](dx-graphics-hlsl-variable-register.md) e [PACKOFFSET (DirectX HLSL)](dx-graphics-hlsl-variable-packoffset.md) .</span><span class="sxs-lookup"><span data-stu-id="0bea3-153">There are two ways to pack constants data: using the [register (DirectX HLSL)](dx-graphics-hlsl-variable-register.md) and [packoffset (DirectX HLSL)](dx-graphics-hlsl-variable-packoffset.md) keywords.</span></span>



|                                                                                                                                                                                                                                                                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0bea3-154">Differenze tra Direct3D 9 e Direct3D 10 e 11:</span><span class="sxs-lookup"><span data-stu-id="0bea3-154">Differences between Direct3D 9 and Direct3D 10 and 11:</span></span><br/> <span data-ttu-id="0bea3-155">A differenza dell'allocazione automatica di costanti in Direct3D 9, che non hanno eseguito la compressione e assegnavano invece ogni variabile a un set di registri float4, le variabili costanti HLSL seguono le regole di compressione in Direct3D 10 e 11.</span><span class="sxs-lookup"><span data-stu-id="0bea3-155">Unlike the auto-allocation of constants in Direct3D 9, which did not perform packing and instead assigned each variable to a set of float4 registers, HLSL constant variables follow packing rules in Direct3D 10 and 11.</span></span><br/> |



 

### <a name="organizing-constant-buffers"></a><span data-ttu-id="0bea3-156">Organizzazione dei buffer costanti</span><span class="sxs-lookup"><span data-stu-id="0bea3-156">Organizing constant buffers</span></span>

<span data-ttu-id="0bea3-157">I buffer costanti consentono di ridurre la larghezza di banda necessaria per aggiornare le costanti dello shader consentendo il raggruppamento e il commit delle costanti dello shader, anziché eseguire chiamate singole per eseguire il commit di ogni costante separatamente.</span><span class="sxs-lookup"><span data-stu-id="0bea3-157">Constant buffers reduce the bandwidth required to update shader constants by allowing shader constants to be grouped together and committed at the same time rather than making individual calls to commit each constant separately.</span></span>

<span data-ttu-id="0bea3-158">Il modo migliore per usare in modo efficiente i buffer costanti consiste nell'organizzare le variabili dello shader in buffer costanti in base alla rispettiva frequenza di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="0bea3-158">The best way to efficiently use constant buffers is to organize shader variables into constant buffers based on their frequency of update.</span></span> <span data-ttu-id="0bea3-159">Questo consente a un'applicazione di ridurre al minimo la larghezza di banda necessaria per l'aggiornamento delle costanti dello shader.</span><span class="sxs-lookup"><span data-stu-id="0bea3-159">This allows an application to minimize the bandwidth required for updating shader constants.</span></span> <span data-ttu-id="0bea3-160">Uno shader, ad esempio, può dichiarare due buffer costanti e organizzare i dati in ognuno in base alla relativa frequenza di aggiornamento: i dati che devono essere aggiornati in base all'oggetto, ad esempio una matrice globale, vengono raggruppati in un buffer costante che può essere aggiornato per ogni oggetto.</span><span class="sxs-lookup"><span data-stu-id="0bea3-160">For example, a shader might declare two constant buffers and organize the data in each based on their frequency of update: data that needs to be updated on a per-object basis (like a world matrix) is grouped into a constant buffer which could be updated for each object.</span></span> <span data-ttu-id="0bea3-161">Questo è separato dai dati che caratterizzano una scena ed è quindi probabile che vengano aggiornati molto meno spesso (quando cambia la scena).</span><span class="sxs-lookup"><span data-stu-id="0bea3-161">This is separate from data that characterizes a scene and is therefore likely to be updated much less often (when the scene changes).</span></span>


```
cbuffer myObject
{       
    float4x4 matWorld;
    float3   vObjectPosition;
    int      arrayIndex;
}
 
cbuffer myScene
{
    float3   vSunPosition;
    float4x4 matView;
}
        
```



### <a name="default-constant-buffers"></a><span data-ttu-id="0bea3-162">Buffer costanti predefiniti</span><span class="sxs-lookup"><span data-stu-id="0bea3-162">Default constant buffers</span></span>

<span data-ttu-id="0bea3-163">Sono disponibili due buffer costanti predefiniti, $Global e $Param.</span><span class="sxs-lookup"><span data-stu-id="0bea3-163">There are two default constant buffers available, $Global and $Param.</span></span> <span data-ttu-id="0bea3-164">Le variabili inserite nell'ambito globale vengono aggiunte in modo implicito alla $Global cbuffer, usando lo stesso metodo di compressione usato per cBuffers.</span><span class="sxs-lookup"><span data-stu-id="0bea3-164">Variables that are placed in the global scope are added implicitly to the $Global cbuffer, using the same packing method that is used for cbuffers.</span></span> <span data-ttu-id="0bea3-165">I parametri uniformi nell'elenco di parametri di una funzione vengono visualizzati nel buffer costante $Param quando uno shader viene compilato all'esterno del Framework effetti.</span><span class="sxs-lookup"><span data-stu-id="0bea3-165">Uniform parameters in the parameter list of a function appear in the $Param constant buffer when a shader is compiled outside of the effects framework.</span></span> <span data-ttu-id="0bea3-166">Quando vengono compilati all'interno del Framework degli effetti, tutte le uniformi devono essere risolte in variabili definite nell'ambito globale.</span><span class="sxs-lookup"><span data-stu-id="0bea3-166">When compiled inside the effects framework, all uniforms must resolve to variables defined in the global scope.</span></span>

## <a name="examples"></a><span data-ttu-id="0bea3-167">Esempio</span><span class="sxs-lookup"><span data-stu-id="0bea3-167">Examples</span></span>

<span data-ttu-id="0bea3-168">Di seguito è riportato un esempio dell' [esempio Skinning10](https://msdn.microsoft.com/library/Ee416429(v=VS.85).aspx) che rappresenta un buffer di trama costituito da una matrice di matrici.</span><span class="sxs-lookup"><span data-stu-id="0bea3-168">Here is an example from [Skinning10 Sample](https://msdn.microsoft.com/library/Ee416429(v=VS.85).aspx) that is a texture buffer made up of an array of matrices.</span></span>


```
tbuffer tbAnimMatrices
{
    matrix g_mTexBoneWorld[MAX_BONE_MATRICES];
};
      
```



<span data-ttu-id="0bea3-169">In questa dichiarazione di esempio viene assegnata manualmente un buffer costante per iniziare a un particolare registro e vengono inoltre inseriti elementi specifici in base ai sottocomponenti.</span><span class="sxs-lookup"><span data-stu-id="0bea3-169">This example declaration manually assigns a constant buffer to start at a particular register, and also packs particular elements by subcomponents.</span></span>


```
cbuffer MyBuffer : register(b3)
{
    float4 Element1 : packoffset(c0);
    float1 Element2 : packoffset(c1);
    float1 Element3 : packoffset(c1.y);
}
      
```



## <a name="related-topics"></a><span data-ttu-id="0bea3-170">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0bea3-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0bea3-171">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="0bea3-171">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

