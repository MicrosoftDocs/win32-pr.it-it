---
title: Oggetto Geometry-Shader
description: Un oggetto Geometry shader elabora intere primitive. Usare la sintassi seguente per dichiarare un oggetto Geometry shader.
ms.assetid: d5c1c22b-6fa6-40a8-900f-6d74f74468c1
keywords:
- maxvertexcount (DirectX HLSL)
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: dadb0e8bb3ddda16305ac701b34523668bd9c1a5
ms.sourcegitcommit: 477b1efe7d9c2f91d5f2ac588a20edf348b1c734
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2019
ms.locfileid: "103719753"
---
# <a name="geometry-shader-object"></a><span data-ttu-id="49f9d-105">Oggetto Geometry-Shader</span><span class="sxs-lookup"><span data-stu-id="49f9d-105">Geometry-Shader Object</span></span>

<span data-ttu-id="49f9d-106">Un oggetto Geometry shader elabora intere primitive.</span><span class="sxs-lookup"><span data-stu-id="49f9d-106">A geometry-shader object processes entire primitives.</span></span> <span data-ttu-id="49f9d-107">Usare la sintassi seguente per dichiarare un oggetto Geometry shader.</span><span class="sxs-lookup"><span data-stu-id="49f9d-107">Use the following syntax to declare a geometry-shader object.</span></span>



|                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49f9d-108">\[maxvertexcount (*NumVerts*) \] void *ShaderName* ( *PrimitiveType DataType Name \[ NumElements \]*, InOut *StreamOutputObject* );</span><span class="sxs-lookup"><span data-stu-id="49f9d-108">\[maxvertexcount(*NumVerts*)\] void *ShaderName* (   *PrimitiveType DataType Name \[ NumElements \]*,   inout *StreamOutputObject*  );</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="49f9d-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="49f9d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49f9d-110"><span id="_maxvertexcount_NumVerts__"></span><span id="_maxvertexcount_numverts__"></span><span id="_MAXVERTEXCOUNT_NUMVERTS__"></span>\[maxvertexcount (*NumVerts*)\]</span><span class="sxs-lookup"><span data-stu-id="49f9d-110"><span id="_maxvertexcount_NumVerts__"></span><span id="_maxvertexcount_numverts__"></span><span id="_MAXVERTEXCOUNT_NUMVERTS__"></span>\[maxvertexcount(*NumVerts*)\]</span></span>
</dt> <dd>

<span data-ttu-id="49f9d-111">\[nella \] dichiarazione per il numero massimo di vertici da creare.</span><span class="sxs-lookup"><span data-stu-id="49f9d-111">\[in\] Declaration for the maximum number of vertices to create.</span></span>

-   <span data-ttu-id="49f9d-112">\[maxvertexcount () \] : parola chiave obbligatoria. le parentesi quadre e le parentesi sono i caratteri necessari per la sintassi corretta.</span><span class="sxs-lookup"><span data-stu-id="49f9d-112">\[maxvertexcount()\] - required keyword; brackets and parenthesis are required characters for correct syntax.</span></span>
-   <span data-ttu-id="49f9d-113">*NumVerts* : numero intero che rappresenta il numero di vertici.</span><span class="sxs-lookup"><span data-stu-id="49f9d-113">*NumVerts* - An integer number representing the number of vertices.</span></span>

</dd> <dt>

<span data-ttu-id="49f9d-114"><span id="ShaderName"></span><span id="shadername"></span><span id="SHADERNAME"></span>*ShaderName*</span><span class="sxs-lookup"><span data-stu-id="49f9d-114"><span id="ShaderName"></span><span id="shadername"></span><span id="SHADERNAME"></span>*ShaderName*</span></span>
</dt> <dd>

<span data-ttu-id="49f9d-115">\[in \] una stringa ASCII contenente un nome univoco per la funzione geometry-shader.</span><span class="sxs-lookup"><span data-stu-id="49f9d-115">\[in\] An ASCII string that contains a unique name for the geometry-shader function.</span></span>

</dd> <dt>

<span data-ttu-id="49f9d-116"><span id="PrimitiveType_DataType_Name___NumElements__"></span><span id="primitivetype_datatype_name___numelements__"></span><span id="PRIMITIVETYPE_DATATYPE_NAME___NUMELEMENTS__"></span>*Nome del tipo di dati PrimitiveType \[ NumElements \]*</span><span class="sxs-lookup"><span data-stu-id="49f9d-116"><span id="PrimitiveType_DataType_Name___NumElements__"></span><span id="primitivetype_datatype_name___numelements__"></span><span id="PRIMITIVETYPE_DATATYPE_NAME___NUMELEMENTS__"></span>*PrimitiveType DataType Name \[ NumElements \]*</span></span>
</dt> <dd>

<span data-ttu-id="49f9d-117">*PrimitiveType* : tipo primitivo, che determina l'ordine dei dati primitivi.</span><span class="sxs-lookup"><span data-stu-id="49f9d-117">*PrimitiveType* - Primitive type, which determines the order of the primitive data.</span></span>



| <span data-ttu-id="49f9d-118">Tipo primitivo</span><span class="sxs-lookup"><span data-stu-id="49f9d-118">Primitive Type</span></span> | <span data-ttu-id="49f9d-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="49f9d-119">Description</span></span>                                                   |
|----------------|---------------------------------------------------------------|
| <span data-ttu-id="49f9d-120">*punto*</span><span class="sxs-lookup"><span data-stu-id="49f9d-120">*point*</span></span>        | <span data-ttu-id="49f9d-121">Elenco di punti</span><span class="sxs-lookup"><span data-stu-id="49f9d-121">Point list</span></span>                                                    |
| <span data-ttu-id="49f9d-122">*linea*</span><span class="sxs-lookup"><span data-stu-id="49f9d-122">*line*</span></span>         | <span data-ttu-id="49f9d-123">Elenco linee o striscia di linea</span><span class="sxs-lookup"><span data-stu-id="49f9d-123">Line list or line strip</span></span>                                       |
| <span data-ttu-id="49f9d-124">*triangolo*</span><span class="sxs-lookup"><span data-stu-id="49f9d-124">*triangle*</span></span>     | <span data-ttu-id="49f9d-125">Elenco di triangolo o striscia di triangolo</span><span class="sxs-lookup"><span data-stu-id="49f9d-125">Triangle list or triangle strip</span></span>                               |
| <span data-ttu-id="49f9d-126">*lineadj*</span><span class="sxs-lookup"><span data-stu-id="49f9d-126">*lineadj*</span></span>      | <span data-ttu-id="49f9d-127">Elenco di righe con adiacenza o striping di riga con adiacenza</span><span class="sxs-lookup"><span data-stu-id="49f9d-127">Line list with adjacency or line strip with adjacency</span></span>         |
| <span data-ttu-id="49f9d-128">*triangleadj*</span><span class="sxs-lookup"><span data-stu-id="49f9d-128">*triangleadj*</span></span>  | <span data-ttu-id="49f9d-129">Elenco di triangolo con adiacenza o striscia di triangolo con adiacenza</span><span class="sxs-lookup"><span data-stu-id="49f9d-129">Triangle list with adjacency or triangle strip with adjacency</span></span> |



 

<span data-ttu-id="49f9d-130">  -  Tipo \[ di dati in \] un tipo di dati di input; può essere qualsiasi [tipo di dati HLSL](dx-graphics-hlsl-data-types.md).</span><span class="sxs-lookup"><span data-stu-id="49f9d-130">*DataType* - \[in\] An input data type; can be any [HLSL data type](dx-graphics-hlsl-data-types.md).</span></span>

<span data-ttu-id="49f9d-131">*Nome* -argomento nome; si tratta di una stringa ASCII.</span><span class="sxs-lookup"><span data-stu-id="49f9d-131">*Name* - Argument name; this is an ASCII string.</span></span>

<span data-ttu-id="49f9d-132">*NumElements* : dimensioni della matrice dell'input, che dipendono da *PrimitiveType* , come illustrato nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="49f9d-132">*NumElements* - Array size of the input, which depends on the *PrimitiveType* as shown in the following table.</span></span>

| <span data-ttu-id="49f9d-133">Tipo primitivo</span><span class="sxs-lookup"><span data-stu-id="49f9d-133">Primitive Type</span></span> | <span data-ttu-id="49f9d-134">NumElements</span><span class="sxs-lookup"><span data-stu-id="49f9d-134">NumElements</span></span>                                                                                                  |
|----------------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49f9d-135">*punto*</span><span class="sxs-lookup"><span data-stu-id="49f9d-135">*point*</span></span>        | <span data-ttu-id="49f9d-136">\[1\]</span><span class="sxs-lookup"><span data-stu-id="49f9d-136">\[1\]</span></span><br/> <span data-ttu-id="49f9d-137">Si opera su un solo punto alla volta.</span><span class="sxs-lookup"><span data-stu-id="49f9d-137">You operate on only one point at a time.</span></span><br/>                                         |
| <span data-ttu-id="49f9d-138">*linea*</span><span class="sxs-lookup"><span data-stu-id="49f9d-138">*line*</span></span>         | <span data-ttu-id="49f9d-139">\[2\]</span><span class="sxs-lookup"><span data-stu-id="49f9d-139">\[2\]</span></span><br/> <span data-ttu-id="49f9d-140">Una linea richiede due vertici.</span><span class="sxs-lookup"><span data-stu-id="49f9d-140">A line requires two vertices.</span></span><br/>                                                    |
| <span data-ttu-id="49f9d-141">*triangolo*</span><span class="sxs-lookup"><span data-stu-id="49f9d-141">*triangle*</span></span>     | <span data-ttu-id="49f9d-142">\[3\]</span><span class="sxs-lookup"><span data-stu-id="49f9d-142">\[3\]</span></span><br/> <span data-ttu-id="49f9d-143">Un triangolo richiede tre vertici.</span><span class="sxs-lookup"><span data-stu-id="49f9d-143">A triangle requires three vertices.</span></span><br/>                                              |
| <span data-ttu-id="49f9d-144">*lineadj*</span><span class="sxs-lookup"><span data-stu-id="49f9d-144">*lineadj*</span></span>      | <span data-ttu-id="49f9d-145">\[4\]</span><span class="sxs-lookup"><span data-stu-id="49f9d-145">\[4\]</span></span><br/> <span data-ttu-id="49f9d-146">Un lineadj ha due estremità. Pertanto, richiede quattro vertici.</span><span class="sxs-lookup"><span data-stu-id="49f9d-146">A lineadj has two ends; therefore, it requires four vertices.</span></span><br/>                    |
| <span data-ttu-id="49f9d-147">*triangleadj*</span><span class="sxs-lookup"><span data-stu-id="49f9d-147">*triangleadj*</span></span>  | <span data-ttu-id="49f9d-148">\[6\]</span><span class="sxs-lookup"><span data-stu-id="49f9d-148">\[6\]</span></span><br/> <span data-ttu-id="49f9d-149">Un triangleadj delimita altri tre triangoli; Pertanto, richiede sei vertici.</span><span class="sxs-lookup"><span data-stu-id="49f9d-149">A triangleadj borders three more triangles; therefore, it requires six vertices.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="49f9d-150"><span id="StreamOutputObject"></span><span id="streamoutputobject"></span><span id="STREAMOUTPUTOBJECT"></span>*StreamOutputObject*</span><span class="sxs-lookup"><span data-stu-id="49f9d-150"><span id="StreamOutputObject"></span><span id="streamoutputobject"></span><span id="STREAMOUTPUTOBJECT"></span>*StreamOutputObject*</span></span>
</dt> <dd>

<span data-ttu-id="49f9d-151">Dichiarazione dell' [oggetto flusso di output](dx-graphics-hlsl-so-type.md).</span><span class="sxs-lookup"><span data-stu-id="49f9d-151">The declaration of the [stream-output object](dx-graphics-hlsl-so-type.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49f9d-152">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="49f9d-152">Return Value</span></span>

<span data-ttu-id="49f9d-153">nessuno</span><span class="sxs-lookup"><span data-stu-id="49f9d-153">None</span></span>

## <a name="remarks"></a><span data-ttu-id="49f9d-154">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="49f9d-154">Remarks</span></span>

<span data-ttu-id="49f9d-155">Il diagramma seguente mostra i vari tipi primitivi per un oggetto Geometry shader.</span><span class="sxs-lookup"><span data-stu-id="49f9d-155">The following diagram shows the various primitive types for a geometry shader object.</span></span>

![illustrazione dei vari tipi primitivi per un oggetto Geometry shader](images/d3d11-gsinputs1.png)

<span data-ttu-id="49f9d-157">Il diagramma seguente illustra le chiamate a geometry shader.</span><span class="sxs-lookup"><span data-stu-id="49f9d-157">The following diagram shows geometry shader invocations.</span></span>

![illustrazione delle chiamate geometry shader](images/d3d11-gsinputs2.png)

## <a name="examples"></a><span data-ttu-id="49f9d-159">Esempio</span><span class="sxs-lookup"><span data-stu-id="49f9d-159">Examples</span></span>

<span data-ttu-id="49f9d-160">Questo esempio è relativo all'esercizio 1 del [workshop Direct3D 10 Shader Model 4,0](https://msdn.microsoft.com/library/Ee416554(v=VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="49f9d-160">This example is from exercise 1 from the [Direct3D 10 Shader Model 4.0 Workshop](https://msdn.microsoft.com/library/Ee416554(v=VS.85).aspx).</span></span>


```
[maxvertexcount(3)]
void GSScene( triangleadj GSSceneIn input[6], inout TriangleStream<PSSceneIn> OutputStream )
{   
    PSSceneIn output = (PSSceneIn)0;

    for( uint i=0; i<6; i+=2 )
    {
        output.Pos = input[i].Pos;
        output.Norm = input[i].Norm;
        output.Tex = input[i].Tex;
        
        OutputStream.Append( output );
    }
    
    OutputStream.RestartStrip();
}
```



## <a name="minimum-shader-model"></a><span data-ttu-id="49f9d-161">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="49f9d-161">Minimum Shader Model</span></span>

<span data-ttu-id="49f9d-162">Questo oggetto è supportato nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="49f9d-162">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="49f9d-163">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="49f9d-163">Shader Model</span></span>                                                        | <span data-ttu-id="49f9d-164">Supportato</span><span class="sxs-lookup"><span data-stu-id="49f9d-164">Supported</span></span> |
|---------------------------------------------------------------------|-----------|
| <span data-ttu-id="49f9d-165">[Shader Model 4](dx-graphics-hlsl-sm4.md) e versioni successive shader Models</span><span class="sxs-lookup"><span data-stu-id="49f9d-165">[Shader Model 4](dx-graphics-hlsl-sm4.md) and higher shader models</span></span> | <span data-ttu-id="49f9d-166">sì</span><span class="sxs-lookup"><span data-stu-id="49f9d-166">yes</span></span>       |



 

## <a name="related-topics"></a><span data-ttu-id="49f9d-167">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="49f9d-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="49f9d-168">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="49f9d-168">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 





