---
title: Oggetto Stream-Output
description: Un oggetto Stream-output è un oggetto basato su modelli che trasmette i dati fuori dalla fase geometry-shader. Usare la sintassi seguente per dichiarare un oggetto Stream-output.
ms.assetid: 07a5489c-c238-4466-9282-5b168448aff7
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 98063ddb45633dda6c897abf0f82f29a394c3f95
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399177"
---
# <a name="stream-output-object"></a><span data-ttu-id="9c7f4-104">Oggetto Stream-Output</span><span class="sxs-lookup"><span data-stu-id="9c7f4-104">Stream-Output Object</span></span>

<span data-ttu-id="9c7f4-105">Un oggetto Stream-output è un oggetto basato su modelli che trasmette i dati fuori dalla [fase geometry-shader](/previous-versions//bb205146(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9c7f4-105">A stream-output object is a templated object that streams data out of the [geometry-shader stage](/previous-versions//bb205146(v=vs.85)).</span></span> <span data-ttu-id="9c7f4-106">Usare la sintassi seguente per dichiarare un oggetto Stream-output.</span><span class="sxs-lookup"><span data-stu-id="9c7f4-106">Use the following syntax to declare a stream-output object.</span></span>



| <span data-ttu-id="9c7f4-107">nome del tipo di dati *StreamOutputObject* di InOut <  >  *;*</span><span class="sxs-lookup"><span data-stu-id="9c7f4-107">inout *StreamOutputObject*<*DataType*> *Name;*</span></span> |
|------------------------------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="9c7f4-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="9c7f4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c7f4-109"><span id="StreamOutputObject___________________________DataType_________________________________________Name"></span><span id="streamoutputobject___________________________datatype_________________________________________name"></span><span id="STREAMOUTPUTOBJECT___________________________DATATYPE_________________________________________NAME"></span>*StreamOutputObject*  <  *Tipo*  >  di dati   *Nome*</span><span class="sxs-lookup"><span data-stu-id="9c7f4-109"><span id="StreamOutputObject___________________________DataType_________________________________________Name"></span><span id="streamoutputobject___________________________datatype_________________________________________name"></span><span id="STREAMOUTPUTOBJECT___________________________DATATYPE_________________________________________NAME"></span>*StreamOutputObject* < *DataType* >   *Name*</span></span>
</dt> <dd>

<span data-ttu-id="9c7f4-110">Dichiarazione dell'oggetto Stream-output (SO).</span><span class="sxs-lookup"><span data-stu-id="9c7f4-110">The stream-output object (SO) declaration.</span></span>



| <span data-ttu-id="9c7f4-111">Tipi di oggetti Stream-Output</span><span class="sxs-lookup"><span data-stu-id="9c7f4-111">Stream-Output Object Types</span></span> | <span data-ttu-id="9c7f4-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9c7f4-112">Description</span></span>                       |
|----------------------------|-----------------------------------|
| <span data-ttu-id="9c7f4-113">*PointStream*</span><span class="sxs-lookup"><span data-stu-id="9c7f4-113">*PointStream*</span></span>              | <span data-ttu-id="9c7f4-114">Sequenza di primitive di punti</span><span class="sxs-lookup"><span data-stu-id="9c7f4-114">A sequence of point primitives</span></span>    |
| <span data-ttu-id="9c7f4-115">*LineStream*</span><span class="sxs-lookup"><span data-stu-id="9c7f4-115">*LineStream*</span></span>               | <span data-ttu-id="9c7f4-116">Sequenza di primitive di linea</span><span class="sxs-lookup"><span data-stu-id="9c7f4-116">A sequence of line primitives</span></span>     |
| <span data-ttu-id="9c7f4-117">*TriangleStream*</span><span class="sxs-lookup"><span data-stu-id="9c7f4-117">*TriangleStream*</span></span>           | <span data-ttu-id="9c7f4-118">Sequenza di primitive triangolari</span><span class="sxs-lookup"><span data-stu-id="9c7f4-118">A sequence of triangle primitives</span></span> |



 

<span data-ttu-id="9c7f4-119">*DataType* -tipo di dati di output; può essere qualsiasi [tipo di dati HLSL](dx-graphics-hlsl-data-types.md).</span><span class="sxs-lookup"><span data-stu-id="9c7f4-119">*DataType* - Output data type; can be any [HLSL data type](dx-graphics-hlsl-data-types.md).</span></span> <span data-ttu-id="9c7f4-120">Deve essere racchiuso tra parentesi acute.</span><span class="sxs-lookup"><span data-stu-id="9c7f4-120">Must be surrounded by the angle brackets.</span></span>

<span data-ttu-id="9c7f4-121">*Nome: nome* della variabile; stringa ASCII che identifica in modo univoco l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="9c7f4-121">*Name* - Variable name; an ASCII string that uniquely identifies the object.</span></span>

</dd> </dl>

## <a name="example"></a><span data-ttu-id="9c7f4-122">Esempio</span><span class="sxs-lookup"><span data-stu-id="9c7f4-122">Example</span></span>

<span data-ttu-id="9c7f4-123">Questo è un esempio di dichiarazione di un oggetto di output di flusso che trasmette le primitive triangolari i cui dati sono definiti da PS \_ mappa cubi \_ nella struttura.</span><span class="sxs-lookup"><span data-stu-id="9c7f4-123">This is an example of a stream-output object declaration that streams out triangle primitives whose data is defined by the PS\_CUBEMAP\_IN structure.</span></span> <span data-ttu-id="9c7f4-124">Geometry shader è limitato alla generazione di 18 vertici.</span><span class="sxs-lookup"><span data-stu-id="9c7f4-124">The geometry-shader is limited to generating 18 vertices.</span></span>


```
struct PS_CUBEMAP_IN
{
    float4 Pos : SV_POSITION;     // Projection coord
    float2 Tex : TEXCOORD0;       // Texture coord
    uint RTIndex : SV_RenderTargetArrayIndex;
};

[maxvertexcount(18)]
void main( inout TriangleStream<PS_CUBEMAP_IN> CubeMapStream, triangle PS_CUBEMAP_INT[3] )
{
    ...
}
```



<span data-ttu-id="9c7f4-125">Si tratta di un frammento di codice dell' [esempio CubeMapGS](https://msdn.microsoft.com/library/Ee416398(v=VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="9c7f4-125">This is a code snippet from the [CubeMapGS Sample](https://msdn.microsoft.com/library/Ee416398(v=VS.85).aspx).</span></span>

## <a name="stream-output-object-methods"></a><span data-ttu-id="9c7f4-126">Metodi dell'oggetto Stream-Output</span><span class="sxs-lookup"><span data-stu-id="9c7f4-126">Stream-Output Object Methods</span></span>

<span data-ttu-id="9c7f4-127">Usare la sintassi seguente per chiamare i metodi Stream-output-Object.</span><span class="sxs-lookup"><span data-stu-id="9c7f4-127">Use the following syntax to call stream-output-object methods.</span></span>


```
Object.Method
```



<span data-ttu-id="9c7f4-128">Vengono implementati i metodi seguenti.</span><span class="sxs-lookup"><span data-stu-id="9c7f4-128">The following methods are implemented.</span></span>



| <span data-ttu-id="9c7f4-129">Metodi</span><span class="sxs-lookup"><span data-stu-id="9c7f4-129">Methods</span></span>                                              | <span data-ttu-id="9c7f4-130">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9c7f4-130">Description</span></span>                                                      |
|------------------------------------------------------|------------------------------------------------------------------|
| [<span data-ttu-id="9c7f4-131">Accoda</span><span class="sxs-lookup"><span data-stu-id="9c7f4-131">Append</span></span>](dx-graphics-hlsl-so-append.md)             | <span data-ttu-id="9c7f4-132">Accodare i dati di output a un flusso esistente.</span><span class="sxs-lookup"><span data-stu-id="9c7f4-132">Append output data to an existing stream.</span></span>                        |
| [<span data-ttu-id="9c7f4-133">RestartStrip</span><span class="sxs-lookup"><span data-stu-id="9c7f4-133">RestartStrip</span></span>](dx-graphics-hlsl-so-restartstrip.md) | <span data-ttu-id="9c7f4-134">Terminare la striscia primitiva corrente e avviare una nuova striscia primitiva.</span><span class="sxs-lookup"><span data-stu-id="9c7f4-134">End the current primitive strip and start a new primitive strip.</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="9c7f4-135">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="9c7f4-135">Minimum Shader Model</span></span>

<span data-ttu-id="9c7f4-136">Questo oggetto è supportato nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="9c7f4-136">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="9c7f4-137">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="9c7f4-137">Shader Model</span></span>                                                        | <span data-ttu-id="9c7f4-138">Supportato</span><span class="sxs-lookup"><span data-stu-id="9c7f4-138">Supported</span></span> |
|---------------------------------------------------------------------|-----------|
| <span data-ttu-id="9c7f4-139">[Shader Model 4](dx-graphics-hlsl-sm4.md) e versioni successive shader Models</span><span class="sxs-lookup"><span data-stu-id="9c7f4-139">[Shader Model 4](dx-graphics-hlsl-sm4.md) and higher shader models</span></span> | <span data-ttu-id="9c7f4-140">sì</span><span class="sxs-lookup"><span data-stu-id="9c7f4-140">yes</span></span>       |



 

## <a name="related-topics"></a><span data-ttu-id="9c7f4-141">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9c7f4-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9c7f4-142">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="9c7f4-142">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 