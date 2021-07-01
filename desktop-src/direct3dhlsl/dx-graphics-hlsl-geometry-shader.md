---
title: oggetto Geometry-Shader
description: Un oggetto geometry shader elabora intere primitive. Usare la sintassi seguente per dichiarare un oggetto geometry shader.
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
ms.openlocfilehash: e06bbc184a4b5f82d5edaaf7fdbfbd55f1906f12
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120616"
---
# <a name="geometry-shader-object"></a><span data-ttu-id="4a022-105">oggetto Geometry-Shader</span><span class="sxs-lookup"><span data-stu-id="4a022-105">Geometry-Shader Object</span></span>

<span data-ttu-id="4a022-106">Un oggetto geometry shader elabora intere primitive.</span><span class="sxs-lookup"><span data-stu-id="4a022-106">A geometry-shader object processes entire primitives.</span></span> <span data-ttu-id="4a022-107">Usare la sintassi seguente per dichiarare un oggetto geometry shader.</span><span class="sxs-lookup"><span data-stu-id="4a022-107">Use the following syntax to declare a geometry-shader object.</span></span>

<span data-ttu-id="4a022-108">\[maxvertexcount(*NumVerts*) \] void *ShaderName* ( *PrimitiveType DataType Name \[ NumElements \]*, inout *StreamOutputObject* );</span><span class="sxs-lookup"><span data-stu-id="4a022-108">\[maxvertexcount(*NumVerts*)\] void *ShaderName* (   *PrimitiveType DataType Name \[ NumElements \]*,   inout *StreamOutputObject*  );</span></span>



 

## <a name="parameters"></a><span data-ttu-id="4a022-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="4a022-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a022-110"><span id="_maxvertexcount_NumVerts__"></span><span id="_maxvertexcount_numverts__"></span><span id="_MAXVERTEXCOUNT_NUMVERTS__"></span>\[maxvertexcount(*NumVerts*)\]</span><span class="sxs-lookup"><span data-stu-id="4a022-110"><span id="_maxvertexcount_NumVerts__"></span><span id="_maxvertexcount_numverts__"></span><span id="_MAXVERTEXCOUNT_NUMVERTS__"></span>\[maxvertexcount(*NumVerts*)\]</span></span>
</dt> <dd>

<span data-ttu-id="4a022-111">\[in \] Dichiarazione per il numero massimo di vertici da creare.</span><span class="sxs-lookup"><span data-stu-id="4a022-111">\[in\] Declaration for the maximum number of vertices to create.</span></span>

-   <span data-ttu-id="4a022-112">\[maxvertexcount(): parola chiave obbligatoria. Le parentesi quadre e le parentesi sono caratteri \] obbligatori per la sintassi corretta.</span><span class="sxs-lookup"><span data-stu-id="4a022-112">\[maxvertexcount()\] - required keyword; brackets and parenthesis are required characters for correct syntax.</span></span>
-   <span data-ttu-id="4a022-113">*NumVerts:* numero intero che rappresenta il numero di vertici.</span><span class="sxs-lookup"><span data-stu-id="4a022-113">*NumVerts* - An integer number representing the number of vertices.</span></span>

</dd> <dt>

<span data-ttu-id="4a022-114"><span id="ShaderName"></span><span id="shadername"></span><span id="SHADERNAME"></span>*ShaderName*</span><span class="sxs-lookup"><span data-stu-id="4a022-114"><span id="ShaderName"></span><span id="shadername"></span><span id="SHADERNAME"></span>*ShaderName*</span></span>
</dt> <dd>

<span data-ttu-id="4a022-115">\[in \] Una stringa ASCII che contiene un nome univoco per la funzione geometry shader.</span><span class="sxs-lookup"><span data-stu-id="4a022-115">\[in\] An ASCII string that contains a unique name for the geometry-shader function.</span></span>

</dd> <dt>

<span data-ttu-id="4a022-116"><span id="PrimitiveType_DataType_Name___NumElements__"></span><span id="primitivetype_datatype_name___numelements__"></span><span id="PRIMITIVETYPE_DATATYPE_NAME___NUMELEMENTS__"></span>*PrimitiveType DataType Name \[ NumElements \]*</span><span class="sxs-lookup"><span data-stu-id="4a022-116"><span id="PrimitiveType_DataType_Name___NumElements__"></span><span id="primitivetype_datatype_name___numelements__"></span><span id="PRIMITIVETYPE_DATATYPE_NAME___NUMELEMENTS__"></span>*PrimitiveType DataType Name \[ NumElements \]*</span></span>
</dt> <dd>

<span data-ttu-id="4a022-117">*PrimitiveType:* tipo primitivo, che determina l'ordine dei dati primitivi.</span><span class="sxs-lookup"><span data-stu-id="4a022-117">*PrimitiveType* - Primitive type, which determines the order of the primitive data.</span></span>



| <span data-ttu-id="4a022-118">Tipo primitivo</span><span class="sxs-lookup"><span data-stu-id="4a022-118">Primitive Type</span></span> | <span data-ttu-id="4a022-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4a022-119">Description</span></span>                                                   |
|----------------|---------------------------------------------------------------|
| <span data-ttu-id="4a022-120">*Punto*</span><span class="sxs-lookup"><span data-stu-id="4a022-120">*point*</span></span>        | <span data-ttu-id="4a022-121">Elenco di punti</span><span class="sxs-lookup"><span data-stu-id="4a022-121">Point list</span></span>                                                    |
| <span data-ttu-id="4a022-122">*Linea*</span><span class="sxs-lookup"><span data-stu-id="4a022-122">*line*</span></span>         | <span data-ttu-id="4a022-123">Elenco di righe o striscia di linee</span><span class="sxs-lookup"><span data-stu-id="4a022-123">Line list or line strip</span></span>                                       |
| <span data-ttu-id="4a022-124">*Triangolo*</span><span class="sxs-lookup"><span data-stu-id="4a022-124">*triangle*</span></span>     | <span data-ttu-id="4a022-125">Elenco triangolare o striscia triangolare</span><span class="sxs-lookup"><span data-stu-id="4a022-125">Triangle list or triangle strip</span></span>                               |
| <span data-ttu-id="4a022-126">*lineadj*</span><span class="sxs-lookup"><span data-stu-id="4a022-126">*lineadj*</span></span>      | <span data-ttu-id="4a022-127">Elenco di righe con adicenza o striscia di linee con adicenza</span><span class="sxs-lookup"><span data-stu-id="4a022-127">Line list with adjacency or line strip with adjacency</span></span>         |
| <span data-ttu-id="4a022-128">*triangleadj*</span><span class="sxs-lookup"><span data-stu-id="4a022-128">*triangleadj*</span></span>  | <span data-ttu-id="4a022-129">Elenco di triangoli con adicenza o striscia triangolare con adicenza</span><span class="sxs-lookup"><span data-stu-id="4a022-129">Triangle list with adjacency or triangle strip with adjacency</span></span> |



 

<span data-ttu-id="4a022-130">*Tipo di dati*  -  \[ in \] Un tipo di dati di input; può essere qualsiasi tipo di dati [HLSL](dx-graphics-hlsl-data-types.md).</span><span class="sxs-lookup"><span data-stu-id="4a022-130">*DataType* - \[in\] An input data type; can be any [HLSL data type](dx-graphics-hlsl-data-types.md).</span></span>

<span data-ttu-id="4a022-131">*Nome* : nome dell'argomento; si tratta di una stringa ASCII.</span><span class="sxs-lookup"><span data-stu-id="4a022-131">*Name* - Argument name; this is an ASCII string.</span></span>

<span data-ttu-id="4a022-132">*NumElements:* dimensione della matrice dell'input, che dipende da *PrimitiveType,* come illustrato nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="4a022-132">*NumElements* - Array size of the input, which depends on the *PrimitiveType* as shown in the following table.</span></span>

| <span data-ttu-id="4a022-133">Tipo primitivo</span><span class="sxs-lookup"><span data-stu-id="4a022-133">Primitive Type</span></span> | <span data-ttu-id="4a022-134">NumElements</span><span class="sxs-lookup"><span data-stu-id="4a022-134">NumElements</span></span>                                                                                                  |
|----------------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a022-135">*Punto*</span><span class="sxs-lookup"><span data-stu-id="4a022-135">*point*</span></span>        | <span data-ttu-id="4a022-136">\[1\]</span><span class="sxs-lookup"><span data-stu-id="4a022-136">\[1\]</span></span><br/> <span data-ttu-id="4a022-137">Si opera su un solo punto alla volta.</span><span class="sxs-lookup"><span data-stu-id="4a022-137">You operate on only one point at a time.</span></span><br/>                                         |
| <span data-ttu-id="4a022-138">*Linea*</span><span class="sxs-lookup"><span data-stu-id="4a022-138">*line*</span></span>         | <span data-ttu-id="4a022-139">\[2\]</span><span class="sxs-lookup"><span data-stu-id="4a022-139">\[2\]</span></span><br/> <span data-ttu-id="4a022-140">Una linea richiede due vertici.</span><span class="sxs-lookup"><span data-stu-id="4a022-140">A line requires two vertices.</span></span><br/>                                                    |
| <span data-ttu-id="4a022-141">*Triangolo*</span><span class="sxs-lookup"><span data-stu-id="4a022-141">*triangle*</span></span>     | <span data-ttu-id="4a022-142">\[3\]</span><span class="sxs-lookup"><span data-stu-id="4a022-142">\[3\]</span></span><br/> <span data-ttu-id="4a022-143">Un triangolo richiede tre vertici.</span><span class="sxs-lookup"><span data-stu-id="4a022-143">A triangle requires three vertices.</span></span><br/>                                              |
| <span data-ttu-id="4a022-144">*lineadj*</span><span class="sxs-lookup"><span data-stu-id="4a022-144">*lineadj*</span></span>      | <span data-ttu-id="4a022-145">\[4\]</span><span class="sxs-lookup"><span data-stu-id="4a022-145">\[4\]</span></span><br/> <span data-ttu-id="4a022-146">Una lineadj ha due estremità; pertanto richiede quattro vertici.</span><span class="sxs-lookup"><span data-stu-id="4a022-146">A lineadj has two ends; therefore, it requires four vertices.</span></span><br/>                    |
| <span data-ttu-id="4a022-147">*triangleadj*</span><span class="sxs-lookup"><span data-stu-id="4a022-147">*triangleadj*</span></span>  | <span data-ttu-id="4a022-148">\[6\]</span><span class="sxs-lookup"><span data-stu-id="4a022-148">\[6\]</span></span><br/> <span data-ttu-id="4a022-149">Un triangoloadj snoda altri tre triangoli; pertanto richiede sei vertici.</span><span class="sxs-lookup"><span data-stu-id="4a022-149">A triangleadj borders three more triangles; therefore, it requires six vertices.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="4a022-150"><span id="StreamOutputObject"></span><span id="streamoutputobject"></span><span id="STREAMOUTPUTOBJECT"></span>*StreamOutputObject*</span><span class="sxs-lookup"><span data-stu-id="4a022-150"><span id="StreamOutputObject"></span><span id="streamoutputobject"></span><span id="STREAMOUTPUTOBJECT"></span>*StreamOutputObject*</span></span>
</dt> <dd>

<span data-ttu-id="4a022-151">Dichiarazione dell'oggetto [stream-output](dx-graphics-hlsl-so-type.md).</span><span class="sxs-lookup"><span data-stu-id="4a022-151">The declaration of the [stream-output object](dx-graphics-hlsl-so-type.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a022-152">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4a022-152">Return Value</span></span>

<span data-ttu-id="4a022-153">nessuno</span><span class="sxs-lookup"><span data-stu-id="4a022-153">None</span></span>

## <a name="remarks"></a><span data-ttu-id="4a022-154">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="4a022-154">Remarks</span></span>

<span data-ttu-id="4a022-155">Il diagramma seguente illustra i vari tipi primitivi per un oggetto geometry shader.</span><span class="sxs-lookup"><span data-stu-id="4a022-155">The following diagram shows the various primitive types for a geometry shader object.</span></span>

![illustrazione dei vari tipi primitivi per un oggetto geometry shader](images/d3d11-gsinputs1.png)

<span data-ttu-id="4a022-157">Il diagramma seguente mostra le chiamate di shader geometrici.</span><span class="sxs-lookup"><span data-stu-id="4a022-157">The following diagram shows geometry shader invocations.</span></span>

![illustrazione delle chiamate di geometry shader](images/d3d11-gsinputs2.png)

## <a name="examples"></a><span data-ttu-id="4a022-159">Esempio</span><span class="sxs-lookup"><span data-stu-id="4a022-159">Examples</span></span>

<span data-ttu-id="4a022-160">Questo esempio è stato creato nell'esercizio 1 di [Direct3D 10 Shader Model 4.0 Workshop](https://msdn.microsoft.com/library/Ee416554(v=VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="4a022-160">This example is from exercise 1 from the [Direct3D 10 Shader Model 4.0 Workshop](https://msdn.microsoft.com/library/Ee416554(v=VS.85).aspx).</span></span>


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



## <a name="minimum-shader-model"></a><span data-ttu-id="4a022-161">Modello di shader minimo</span><span class="sxs-lookup"><span data-stu-id="4a022-161">Minimum Shader Model</span></span>

<span data-ttu-id="4a022-162">Questo oggetto è supportato nei modelli di shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="4a022-162">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="4a022-163">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="4a022-163">Shader Model</span></span>                                                        | <span data-ttu-id="4a022-164">Supportato</span><span class="sxs-lookup"><span data-stu-id="4a022-164">Supported</span></span> |
|---------------------------------------------------------------------|-----------|
| <span data-ttu-id="4a022-165">[Modello shader 4 e](dx-graphics-hlsl-sm4.md) modelli di shader superiori</span><span class="sxs-lookup"><span data-stu-id="4a022-165">[Shader Model 4](dx-graphics-hlsl-sm4.md) and higher shader models</span></span> | <span data-ttu-id="4a022-166">yes</span><span class="sxs-lookup"><span data-stu-id="4a022-166">yes</span></span>       |



 

## <a name="related-topics"></a><span data-ttu-id="4a022-167">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4a022-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4a022-168">Modello shader 4</span><span class="sxs-lookup"><span data-stu-id="4a022-168">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 





