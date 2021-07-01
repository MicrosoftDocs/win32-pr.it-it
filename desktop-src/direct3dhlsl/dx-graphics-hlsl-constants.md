---
title: Costanti dello shader (HLSL)
description: In Shader Model 4 le costanti shader vengono archiviate in una o più risorse del buffer in memoria.
ms.assetid: 89fe874a-8009-4901-bebe-2d9e45f894bb
keywords:
- cbuffer
- tbuffer
- buffer costante
- buffer di trama
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f314be4b8da98ff80bd7404c270479855e13fb6e
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/01/2021
ms.locfileid: "113129960"
---
# <a name="shader-constants-hlsl"></a><span data-ttu-id="6507a-107">Costanti dello shader (HLSL)</span><span class="sxs-lookup"><span data-stu-id="6507a-107">Shader Constants (HLSL)</span></span>

<span data-ttu-id="6507a-108">In Shader Model 4 le costanti shader vengono archiviate in una o più risorse del buffer in memoria.</span><span class="sxs-lookup"><span data-stu-id="6507a-108">In Shader Model 4, shader constants are stored in one or more buffer resources in memory.</span></span> <span data-ttu-id="6507a-109">Possono essere organizzati in due tipi di buffer: buffer costanti (cbuffer) e buffer di trama (tbuffer).</span><span class="sxs-lookup"><span data-stu-id="6507a-109">They can be organized into two types of buffers: constant buffers (cbuffers) and texture buffers (tbuffers).</span></span> <span data-ttu-id="6507a-110">I buffer costanti sono ottimizzati per l'utilizzo di variabili costanti, caratterizzato da un accesso a bassa latenza e da un aggiornamento più frequente dalla CPU.</span><span class="sxs-lookup"><span data-stu-id="6507a-110">Constant buffers are optimized for constant-variable usage, which is characterized by lower-latency access and more frequent update from the CPU.</span></span> <span data-ttu-id="6507a-111">Per questo motivo, a queste risorse si applicano restrizioni aggiuntive per dimensioni, layout e accesso.</span><span class="sxs-lookup"><span data-stu-id="6507a-111">For this reason, additional size, layout, and access restrictions apply to these resources.</span></span> <span data-ttu-id="6507a-112">I buffer di trama sono accessibili come trame e hanno prestazioni migliori per i dati indicizzati arbitrariamente.</span><span class="sxs-lookup"><span data-stu-id="6507a-112">Texture buffers are accessed like textures and perform better for arbitrarily indexed data.</span></span> <span data-ttu-id="6507a-113">Indipendentemente dal tipo di risorsa in uso, non esiste alcun limite al numero di buffer costanti o di trame che un'applicazione può creare.</span><span class="sxs-lookup"><span data-stu-id="6507a-113">Regardless of which type of resource you use, there is no limit to the number of constant buffers or texture buffers an application can create.</span></span>

<span data-ttu-id="6507a-114">La dichiarazione di un buffer costante o di un buffer di trama è molto simile a una dichiarazione di struttura in C, con l'aggiunta delle parole chiave **register** e **packoffset** per l'assegnazione manuale di registri o di dati di pacchetto.</span><span class="sxs-lookup"><span data-stu-id="6507a-114">Declaring a constant buffer or a texture buffer looks very much like a structure declaration in C, with the addition of the **register** and **packoffset** keywords for manually assigning registers or packing data.</span></span>



|                                                                                                                         |
|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6507a-115">*BufferType* \[ *Nome* \] \[: **register**(b \# ) { \] *VariableDeclaration* \[ : **packoffset**(c \# .xyzw) \] ;      ... };</span><span class="sxs-lookup"><span data-stu-id="6507a-115">*BufferType* \[*Name*\] \[: **register**(b\#)\] {     *VariableDeclaration* \[: **packoffset**(c\#.xyzw)\];      ... };</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="6507a-116">Parametri</span><span class="sxs-lookup"><span data-stu-id="6507a-116">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6507a-117"><span id="BufferType"></span><span id="buffertype"></span><span id="BUFFERTYPE"></span>*BufferType*</span><span class="sxs-lookup"><span data-stu-id="6507a-117"><span id="BufferType"></span><span id="buffertype"></span><span id="BUFFERTYPE"></span>*BufferType*</span></span>
</dt> <dd>

<span data-ttu-id="6507a-118">\[in \] Tipo di buffer.</span><span class="sxs-lookup"><span data-stu-id="6507a-118">\[in\] The buffer type.</span></span>



| <span data-ttu-id="6507a-119">BufferType</span><span class="sxs-lookup"><span data-stu-id="6507a-119">BufferType</span></span> | <span data-ttu-id="6507a-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6507a-120">Description</span></span>     |
|------------|-----------------|
| <span data-ttu-id="6507a-121">cbuffer</span><span class="sxs-lookup"><span data-stu-id="6507a-121">cbuffer</span></span>    | <span data-ttu-id="6507a-122">buffer costante</span><span class="sxs-lookup"><span data-stu-id="6507a-122">constant buffer</span></span> |
| <span data-ttu-id="6507a-123">tbuffer</span><span class="sxs-lookup"><span data-stu-id="6507a-123">tbuffer</span></span>    | <span data-ttu-id="6507a-124">buffer di trama</span><span class="sxs-lookup"><span data-stu-id="6507a-124">texture buffer</span></span>  |



 

</dd> <dt>

<span data-ttu-id="6507a-125"><span id="Name"></span><span id="name"></span><span id="NAME"></span>*Nome*</span><span class="sxs-lookup"><span data-stu-id="6507a-125"><span id="Name"></span><span id="name"></span><span id="NAME"></span>*Name*</span></span>
</dt> <dd>

<span data-ttu-id="6507a-126">\[in \] Facoltativo, stringa ASCII contenente un nome di buffer univoco.</span><span class="sxs-lookup"><span data-stu-id="6507a-126">\[in\] Optional, ASCII string containing a unique buffer name.</span></span>

</dd> <dt>

<span data-ttu-id="6507a-127"><span id="register_b__"></span><span id="REGISTER_B__"></span>**register**(b \# )</span><span class="sxs-lookup"><span data-stu-id="6507a-127"><span id="register_b__"></span><span id="REGISTER_B__"></span>**register**(b\#)</span></span>
</dt> <dd>

<span data-ttu-id="6507a-128">\[in \] Parola chiave Facoltativa, usata per inserire manualmente i dati costanti.</span><span class="sxs-lookup"><span data-stu-id="6507a-128">\[in\] Optional keyword, used to manually pack constant data.</span></span> <span data-ttu-id="6507a-129">Le costanti possono essere imballate in un registro solo in un buffer costante, in cui il registro iniziale viene fornito dal numero di registro ( *\#* ).</span><span class="sxs-lookup"><span data-stu-id="6507a-129">Constants can be packed in a register only in a constant buffer, where the starting register is given by the register number (*\#*).</span></span>

</dd> <dt>

<span data-ttu-id="6507a-130"><span id="VariableDeclaration"></span><span id="variabledeclaration"></span><span id="VARIABLEDECLARATION"></span>*VariableDeclaration*</span><span class="sxs-lookup"><span data-stu-id="6507a-130"><span id="VariableDeclaration"></span><span id="variabledeclaration"></span><span id="VARIABLEDECLARATION"></span>*VariableDeclaration*</span></span>
</dt> <dd>

<span data-ttu-id="6507a-131">\[nella \] dichiarazione di variabile, simile a una dichiarazione di membro di struttura.</span><span class="sxs-lookup"><span data-stu-id="6507a-131">\[in\] Variable declaration, similar to a structure member declaration.</span></span> <span data-ttu-id="6507a-132">Può trattarsi di qualsiasi tipo HLSL o oggetto effetto (ad eccezione di una trama o di un oggetto sampler).</span><span class="sxs-lookup"><span data-stu-id="6507a-132">This can be any HLSL type or effect object (except a texture or a sampler object).</span></span>

</dd> <dt>

<span data-ttu-id="6507a-133"><span id="packoffset_c_.xyzw_"></span><span id="PACKOFFSET_C_.XYZW_"></span>**packoffset**(c \# .xyzw)</span><span class="sxs-lookup"><span data-stu-id="6507a-133"><span id="packoffset_c_.xyzw_"></span><span id="PACKOFFSET_C_.XYZW_"></span>**packoffset**(c\#.xyzw)</span></span>
</dt> <dd>

<span data-ttu-id="6507a-134">\[in \] Parola chiave Facoltativa, usata per inserire manualmente i dati costanti.</span><span class="sxs-lookup"><span data-stu-id="6507a-134">\[in\] Optional keyword, used to manually pack constant data.</span></span> <span data-ttu-id="6507a-135">Le costanti possono essere imballate in qualsiasi buffer costante, in cui il numero di registro viene fornito da ( *\#* ).</span><span class="sxs-lookup"><span data-stu-id="6507a-135">Constants can be packed in any constant buffer, where the register number is given by (*\#*).</span></span> <span data-ttu-id="6507a-136">L'impacchettamento dei componenti secondari (con xyzw swizzling) è disponibile per le costanti le cui dimensioni rientrano in un singolo registro (non attraversare un limite di registro).</span><span class="sxs-lookup"><span data-stu-id="6507a-136">Sub-component packing (using xyzw swizzling) is available for constants whose size fit within a single register (do not cross a register boundary).</span></span> <span data-ttu-id="6507a-137">Ad esempio, non è stato possibile inserire un float4 in un singolo registro a partire dal componente y perché non rientra in un registro a quattro componenti.</span><span class="sxs-lookup"><span data-stu-id="6507a-137">For instance, a float4 could not be packed in a single register starting with the y-component because it would not fit in a four-component register.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6507a-138">Commenti</span><span class="sxs-lookup"><span data-stu-id="6507a-138">Remarks</span></span>

<span data-ttu-id="6507a-139">I buffer costanti riducono la larghezza di banda necessaria per aggiornare le costanti shader consentendo il raggruppamento e il commit delle costanti shader contemporaneamente anziché effettuare singole chiamate per eseguire separatamente il commit di ogni costante.</span><span class="sxs-lookup"><span data-stu-id="6507a-139">Constant buffers reduce the bandwidth required to update shader constants by allowing shader constants to be grouped together and committed at the same time rather than making individual calls to commit each constant separately.</span></span>

<span data-ttu-id="6507a-140">Un buffer costante è una risorsa buffer specializzata a cui si accede come un buffer.</span><span class="sxs-lookup"><span data-stu-id="6507a-140">A constant buffer is a specialized buffer resource that is accessed like a buffer.</span></span> <span data-ttu-id="6507a-141">Ogni buffer costante può contenere fino a 4096 [vettori](dx-graphics-hlsl-vector.md); ogni vettore contiene fino a quattro valori a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="6507a-141">Each constant buffer can hold up to 4096 [vectors](dx-graphics-hlsl-vector.md); each vector contains up to four 32-bit values.</span></span> <span data-ttu-id="6507a-142">È possibile associare fino a 14 buffer costanti per ogni fase della pipeline (2 slot aggiuntivi sono riservati per l'uso interno).</span><span class="sxs-lookup"><span data-stu-id="6507a-142">You can bind up to 14 constant buffers per pipeline stage (2 additional slots are reserved for internal use).</span></span>

<span data-ttu-id="6507a-143">Un buffer di trama è una risorsa buffer specializzata a cui si accede come una trama.</span><span class="sxs-lookup"><span data-stu-id="6507a-143">A texture buffer is a specialized buffer resource that is accessed like a texture.</span></span> <span data-ttu-id="6507a-144">L'accesso alla trama (rispetto all'accesso al buffer) può avere prestazioni migliori per i dati indicizzati arbitrariamente.</span><span class="sxs-lookup"><span data-stu-id="6507a-144">Texture access (as compared with buffer access) can have better performance for arbitrarily indexed data.</span></span> <span data-ttu-id="6507a-145">È possibile associare fino a 128 buffer di trama per ogni fase della pipeline.</span><span class="sxs-lookup"><span data-stu-id="6507a-145">You can bind up to 128 texture buffers per pipeline stage.</span></span>

<span data-ttu-id="6507a-146">Una risorsa buffer è progettata per ridurre al minimo il sovraccarico dell'impostazione delle costanti shader.</span><span class="sxs-lookup"><span data-stu-id="6507a-146">A buffer resource is designed to minimize the overhead of setting shader constants.</span></span> <span data-ttu-id="6507a-147">Il framework degli effetti (vedere [**l'interfaccia ID3D10Effect**](/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effect)) gestirà l'aggiornamento dei buffer delle costanti e delle trame oppure è possibile usare l'API Direct3D per aggiornare i buffer (per informazioni, vedere Copia e accesso ai dati delle risorse [(Direct3D 10).](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-mapping)</span><span class="sxs-lookup"><span data-stu-id="6507a-147">The effect framework (see [**ID3D10Effect Interface**](/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effect)) will manage updating constant and texture buffers, or you can use the Direct3D API to update buffers (see [Copying and Accessing Resource Data (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-mapping) for information).</span></span> <span data-ttu-id="6507a-148">Un'applicazione può anche copiare dati da un altro buffer,ad esempio una destinazione di rendering o una destinazione di output di flusso, in un buffer costante.</span><span class="sxs-lookup"><span data-stu-id="6507a-148">An application can also copy data from another buffer (such as a render target or a stream-output target) into a constant buffer.</span></span>

<span data-ttu-id="6507a-149">Per altre informazioni sull'uso dei buffer costanti in un'applicazione D3D10, vedere Tipi di risorse [(Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) e Creazione di risorse [buffer (Direct3D 10).](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-creating)</span><span class="sxs-lookup"><span data-stu-id="6507a-149">For more info on using constant buffers in a D3D10 application, see [Resource Types (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) and [Creating Buffer Resources (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-creating).</span></span>

<span data-ttu-id="6507a-150">Per altre informazioni sull'uso dei buffer costanti in un'applicazione D3D11, vedere Introduzione ai buffer [in Direct3D 11](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-intro) e [Procedura: Creare un buffer costante.](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-constant-how-to)</span><span class="sxs-lookup"><span data-stu-id="6507a-150">For morel info on using constant buffers in a D3D11 application, see [Introduction to Buffers in Direct3D 11](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-intro) and [How to: Create a Constant Buffer](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-constant-how-to).</span></span>

<span data-ttu-id="6507a-151">Un buffer costante non richiede che [una vista](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-access-views) sia associata alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="6507a-151">A constant buffer does not require a [view](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-access-views) to be bound to the pipeline.</span></span> <span data-ttu-id="6507a-152">Un buffer di trama, tuttavia, richiede una visualizzazione e deve essere associato a uno slot di trama (o deve essere associato a [**SetTextureBuffer**](/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effectconstantbuffer-settexturebuffer) quando si usa un effetto).</span><span class="sxs-lookup"><span data-stu-id="6507a-152">A texture buffer, however, requires a view and must be bound to a texture slot (or must be bound with [**SetTextureBuffer**](/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effectconstantbuffer-settexturebuffer) when using an effect).</span></span>

<span data-ttu-id="6507a-153">Esistono due modi per imballare i dati delle costanti: usando le parole chiave [register (DirectX HLSL)](dx-graphics-hlsl-variable-register.md) e [packoffset (DirectX HLSL).](dx-graphics-hlsl-variable-packoffset.md)</span><span class="sxs-lookup"><span data-stu-id="6507a-153">There are two ways to pack constants data: using the [register (DirectX HLSL)](dx-graphics-hlsl-variable-register.md) and [packoffset (DirectX HLSL)](dx-graphics-hlsl-variable-packoffset.md) keywords.</span></span>

<span data-ttu-id="6507a-154">Differenze tra Direct3D 9 e Direct3D 10 e 11:</span><span class="sxs-lookup"><span data-stu-id="6507a-154">Differences between Direct3D 9 and Direct3D 10 and 11:</span></span>

- <span data-ttu-id="6507a-155">A differenza dell'allocazione automatica delle costanti in Direct3D 9, che non ha eseguito il packing e ha invece assegnato ogni variabile a un set di registri float4, le variabili costanti HLSL seguono le regole di packing in Direct3D 10 e 11.</span><span class="sxs-lookup"><span data-stu-id="6507a-155">Unlike the auto-allocation of constants in Direct3D 9, which did not perform packing and instead assigned each variable to a set of float4 registers, HLSL constant variables follow packing rules in Direct3D 10 and 11.</span></span>



 

### <a name="organizing-constant-buffers"></a><span data-ttu-id="6507a-156">Organizzazione dei buffer costanti</span><span class="sxs-lookup"><span data-stu-id="6507a-156">Organizing constant buffers</span></span>

<span data-ttu-id="6507a-157">I buffer costanti riducono la larghezza di banda necessaria per aggiornare le costanti shader consentendo il raggruppamento e il commit delle costanti shader contemporaneamente anziché effettuare singole chiamate per eseguire separatamente il commit di ogni costante.</span><span class="sxs-lookup"><span data-stu-id="6507a-157">Constant buffers reduce the bandwidth required to update shader constants by allowing shader constants to be grouped together and committed at the same time rather than making individual calls to commit each constant separately.</span></span>

<span data-ttu-id="6507a-158">Il modo migliore per usare in modo efficiente i buffer costanti consiste nell'organizzare le variabili dello shader in buffer costanti in base alla rispettiva frequenza di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="6507a-158">The best way to efficiently use constant buffers is to organize shader variables into constant buffers based on their frequency of update.</span></span> <span data-ttu-id="6507a-159">Ciò consente a un'applicazione di ridurre al minimo la larghezza di banda necessaria per l'aggiornamento delle costanti shader.</span><span class="sxs-lookup"><span data-stu-id="6507a-159">This allows an application to minimize the bandwidth required for updating shader constants.</span></span> <span data-ttu-id="6507a-160">Ad esempio, uno shader potrebbe dichiarare due buffer costanti e organizzare i dati in ognuno in base alla frequenza di aggiornamento: i dati che devono essere aggiornati per ogni oggetto (ad esempio una matrice globale) vengono raggruppati in un buffer costante che può essere aggiornato per ogni oggetto.</span><span class="sxs-lookup"><span data-stu-id="6507a-160">For example, a shader might declare two constant buffers and organize the data in each based on their frequency of update: data that needs to be updated on a per-object basis (like a world matrix) is grouped into a constant buffer which could be updated for each object.</span></span> <span data-ttu-id="6507a-161">Questo è separato dai dati che caratterizzano una scena e pertanto è probabile che siano aggiornati molto meno spesso (quando la scena cambia).</span><span class="sxs-lookup"><span data-stu-id="6507a-161">This is separate from data that characterizes a scene and is therefore likely to be updated much less often (when the scene changes).</span></span>


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



### <a name="default-constant-buffers"></a><span data-ttu-id="6507a-162">Buffer costanti predefiniti</span><span class="sxs-lookup"><span data-stu-id="6507a-162">Default constant buffers</span></span>

<span data-ttu-id="6507a-163">Sono disponibili due buffer costanti predefiniti, $Global e $Param.</span><span class="sxs-lookup"><span data-stu-id="6507a-163">There are two default constant buffers available, $Global and $Param.</span></span> <span data-ttu-id="6507a-164">Le variabili inserite nell'ambito globale vengono aggiunte in modo implicito al $Global cbuffer, usando lo stesso metodo di pacchetto usato per cbuffer.</span><span class="sxs-lookup"><span data-stu-id="6507a-164">Variables that are placed in the global scope are added implicitly to the $Global cbuffer, using the same packing method that is used for cbuffers.</span></span> <span data-ttu-id="6507a-165">I parametri uniformi nell'elenco di parametri di una funzione vengono visualizzati nel buffer $Param costante quando uno shader viene compilato all'esterno del framework degli effetti.</span><span class="sxs-lookup"><span data-stu-id="6507a-165">Uniform parameters in the parameter list of a function appear in the $Param constant buffer when a shader is compiled outside of the effects framework.</span></span> <span data-ttu-id="6507a-166">Quando vengono compilate all'interno del framework degli effetti, tutte le uniformi devono essere risolte in variabili definite nell'ambito globale.</span><span class="sxs-lookup"><span data-stu-id="6507a-166">When compiled inside the effects framework, all uniforms must resolve to variables defined in the global scope.</span></span>

## <a name="examples"></a><span data-ttu-id="6507a-167">Esempio</span><span class="sxs-lookup"><span data-stu-id="6507a-167">Examples</span></span>

<span data-ttu-id="6507a-168">Ecco un esempio di [Skinning10 Sample che](https://msdn.microsoft.com/library/Ee416429(v=VS.85).aspx) è un buffer di trama costituito da una matrice di matrici.</span><span class="sxs-lookup"><span data-stu-id="6507a-168">Here is an example from [Skinning10 Sample](https://msdn.microsoft.com/library/Ee416429(v=VS.85).aspx) that is a texture buffer made up of an array of matrices.</span></span>


```
tbuffer tbAnimMatrices
{
    matrix g_mTexBoneWorld[MAX_BONE_MATRICES];
};
      
```



<span data-ttu-id="6507a-169">Questa dichiarazione di esempio assegna manualmente un buffer costante per iniziare da un registro specifico e include anche elementi specifici in base ai sottocomponenti.</span><span class="sxs-lookup"><span data-stu-id="6507a-169">This example declaration manually assigns a constant buffer to start at a particular register, and also packs particular elements by subcomponents.</span></span>


```
cbuffer MyBuffer : register(b3)
{
    float4 Element1 : packoffset(c0);
    float1 Element2 : packoffset(c1);
    float1 Element3 : packoffset(c1.y);
}
      
```



## <a name="related-topics"></a><span data-ttu-id="6507a-170">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6507a-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6507a-171">Modello shader 4</span><span class="sxs-lookup"><span data-stu-id="6507a-171">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

