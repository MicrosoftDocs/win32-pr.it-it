---
title: Sintassi di Stream out
description: Un geometry shader con flusso in uscita viene dichiarato con una particolare sintassi.
ms.assetid: 58cf6503-0dde-4c88-837d-ae0e0eda17d5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 535ea78d1b2109e343f01800b3a3d5e1bf6efaba
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104992792"
---
# <a name="stream-out-syntax"></a><span data-ttu-id="c654e-103">Sintassi di Stream out</span><span class="sxs-lookup"><span data-stu-id="c654e-103">Stream Out Syntax</span></span>

<span data-ttu-id="c654e-104">Un geometry shader con flusso in uscita viene dichiarato con una particolare sintassi.</span><span class="sxs-lookup"><span data-stu-id="c654e-104">A geometry shader with stream out is declared with a particular syntax.</span></span> <span data-ttu-id="c654e-105">In questo argomento viene descritta la sintassi di.</span><span class="sxs-lookup"><span data-stu-id="c654e-105">This topic describes the syntax.</span></span> <span data-ttu-id="c654e-106">Nel runtime degli effetti questa sintassi verrà convertita in una chiamata a [**ID3D11Device:: CreateGeometryShaderWithStreamOutput**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput).</span><span class="sxs-lookup"><span data-stu-id="c654e-106">In the effect runtime, this syntax will be converted to a call to [**ID3D11Device::CreateGeometryShaderWithStreamOutput**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput).</span></span>

## <a name="construct-syntax"></a><span data-ttu-id="c654e-107">Sintassi del costrutto</span><span class="sxs-lookup"><span data-stu-id="c654e-107">Construct Syntax</span></span>


```
[ StreamingShaderVar = ] ConstructGSWithSO( ShaderVar, "OutputDecl0" )
```





| <span data-ttu-id="c654e-108">Nome</span><span class="sxs-lookup"><span data-stu-id="c654e-108">Name</span></span>                   | <span data-ttu-id="c654e-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c654e-109">Description</span></span>                                                                                                                                                                                                                |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c654e-110">**StreamingShaderVar**</span><span class="sxs-lookup"><span data-stu-id="c654e-110">**StreamingShaderVar**</span></span> | <span data-ttu-id="c654e-111">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="c654e-111">Optional.</span></span> <span data-ttu-id="c654e-112">Stringa ASCI che identifica in modo univoco il nome di una variabile di shader Geometry con flusso in uscita. Questa operazione è facoltativa perché ConstructGSWithSO può essere inserito direttamente in una chiamata SetGeometryShader o BindInterfaces.</span><span class="sxs-lookup"><span data-stu-id="c654e-112">An ASCI string that uniquely identifies the name of a geometry shader variable with stream out. This is optional because ConstructGSWithSO can be placed directly in a SetGeometryShader or BindInterfaces call.</span></span> |
| <span data-ttu-id="c654e-113">**ShaderVar**</span><span class="sxs-lookup"><span data-stu-id="c654e-113">**ShaderVar**</span></span>          | <span data-ttu-id="c654e-114">Una variabile geometry shader o vertex shader.</span><span class="sxs-lookup"><span data-stu-id="c654e-114">A geometry shader or vertex shader variable.</span></span>                                                                                                                                                                               |
| <span data-ttu-id="c654e-115">**OutputDecl0**</span><span class="sxs-lookup"><span data-stu-id="c654e-115">**OutputDecl0**</span></span>        | <span data-ttu-id="c654e-116">Stringa che definisce quali output dello shader nel flusso 0 vengono trasmessi. Per la sintassi, vedere di seguito.</span><span class="sxs-lookup"><span data-stu-id="c654e-116">A string defining which shader outputs in stream 0 are streamed out. See below for syntax.</span></span>                                                                                                                                 |



 

<span data-ttu-id="c654e-117">Questa è la sintassi definita in file FX \_ 4 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="c654e-117">This is the syntax was defined in fx\_4\_0 files.</span></span> <span data-ttu-id="c654e-118">Si noti che negli \_ shader GS 4 \_ 0 e vs \_ x è presente un solo flusso di dati.</span><span class="sxs-lookup"><span data-stu-id="c654e-118">Note that in gs\_4\_0 and vs\_x shaders, there is only one stream of data.</span></span> <span data-ttu-id="c654e-119">Lo shader risultante restituirà un flusso all'unità di output del flusso e all'unità di rasterizzazione.</span><span class="sxs-lookup"><span data-stu-id="c654e-119">The resulting shader will output one stream to both the stream out unit and the rasterizer unit.</span></span>


```
[ StreamingShaderVar = ] ConstructGSWithSO( ShaderVar, "OutputDecl0", "OutputDecl1", "OutputDecl2", 
"OutputDecl3", RasterizedStream )
```





| <span data-ttu-id="c654e-120">Nome</span><span class="sxs-lookup"><span data-stu-id="c654e-120">Name</span></span>                   | <span data-ttu-id="c654e-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c654e-121">Description</span></span>                                                                                                                                                                                                                |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c654e-122">**StreamingShaderVar**</span><span class="sxs-lookup"><span data-stu-id="c654e-122">**StreamingShaderVar**</span></span> | <span data-ttu-id="c654e-123">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="c654e-123">Optional.</span></span> <span data-ttu-id="c654e-124">Stringa ASCI che identifica in modo univoco il nome di una variabile di shader Geometry con flusso in uscita. Questa operazione è facoltativa perché ConstructGSWithSO può essere inserito direttamente in una chiamata SetGeometryShader o BindInterfaces.</span><span class="sxs-lookup"><span data-stu-id="c654e-124">An ASCI string that uniquely identifies the name of a geometry shader variable with stream out. This is optional because ConstructGSWithSO can be placed directly in a SetGeometryShader or BindInterfaces call.</span></span> |
| <span data-ttu-id="c654e-125">**ShaderVar**</span><span class="sxs-lookup"><span data-stu-id="c654e-125">**ShaderVar**</span></span>          | <span data-ttu-id="c654e-126">Una variabile geometry shader o vertex shader.</span><span class="sxs-lookup"><span data-stu-id="c654e-126">A geometry shader or vertex shader variable.</span></span>                                                                                                                                                                               |
| <span data-ttu-id="c654e-127">**OutputDecl0**</span><span class="sxs-lookup"><span data-stu-id="c654e-127">**OutputDecl0**</span></span>        | <span data-ttu-id="c654e-128">Stringa che definisce quali output dello shader nel flusso 0 vengono trasmessi. Per la sintassi, vedere di seguito.</span><span class="sxs-lookup"><span data-stu-id="c654e-128">A string defining which shader outputs in stream 0 are streamed out. See below for syntax.</span></span>                                                                                                                                 |
| <span data-ttu-id="c654e-129">**OutputDecl1**</span><span class="sxs-lookup"><span data-stu-id="c654e-129">**OutputDecl1**</span></span>        | <span data-ttu-id="c654e-130">Stringa che definisce quali output dello shader nel flusso 1 vengono trasmessi. Per la sintassi, vedere di seguito.</span><span class="sxs-lookup"><span data-stu-id="c654e-130">A string defining which shader outputs in stream 1 are streamed out. See below for syntax.</span></span>                                                                                                                                 |
| <span data-ttu-id="c654e-131">**OutputDecl2**</span><span class="sxs-lookup"><span data-stu-id="c654e-131">**OutputDecl2**</span></span>        | <span data-ttu-id="c654e-132">Stringa che definisce quali output dello shader nel flusso 2 vengono trasmessi. Per la sintassi, vedere di seguito.</span><span class="sxs-lookup"><span data-stu-id="c654e-132">A string defining which shader outputs in stream 2 are streamed out. See below for syntax.</span></span>                                                                                                                                 |
| <span data-ttu-id="c654e-133">**OutputDecl3**</span><span class="sxs-lookup"><span data-stu-id="c654e-133">**OutputDecl3**</span></span>        | <span data-ttu-id="c654e-134">Stringa che definisce quali output dello shader nel flusso 3 vengono trasmessi. Per la sintassi, vedere di seguito.</span><span class="sxs-lookup"><span data-stu-id="c654e-134">A string defining which shader outputs in stream 3 are streamed out. See below for syntax.</span></span>                                                                                                                                 |
| <span data-ttu-id="c654e-135">**RasterizedStream**</span><span class="sxs-lookup"><span data-stu-id="c654e-135">**RasterizedStream**</span></span>   | <span data-ttu-id="c654e-136">Intero che specifica quale flusso verrà inviato al rasterizzatore.</span><span class="sxs-lookup"><span data-stu-id="c654e-136">An integer specifying which stream will be sent to the rasterizer.</span></span>                                                                                                                                                         |



 

<span data-ttu-id="c654e-137">Si noti che \_ gli \_ shader GS 5 0 possono definire fino a quattro flussi di dati.</span><span class="sxs-lookup"><span data-stu-id="c654e-137">Note that gs\_5\_0 shaders can define up to four streams of data.</span></span> <span data-ttu-id="c654e-138">Lo shader risultante restituirà un flusso all'unità di output del flusso per ogni dichiarazione di output non **null** e un flusso dell'unità di rasterizzazione.</span><span class="sxs-lookup"><span data-stu-id="c654e-138">The resulting shader will output one stream to the stream out unit for each non-**NULL** output declaration and one stream the rasterizer unit.</span></span>

## <a name="stream-out-declaration-syntax"></a><span data-ttu-id="c654e-139">Sintassi della dichiarazione di flusso out</span><span class="sxs-lookup"><span data-stu-id="c654e-139">Stream Out Declaration Syntax</span></span>


```
" [ Buffer: ] Semantic[ SemanticIndex ] [ .Mask ]; [ ... ; ] ... [ ... ;]"
```





| <span data-ttu-id="c654e-140">Nome</span><span class="sxs-lookup"><span data-stu-id="c654e-140">Name</span></span>              | <span data-ttu-id="c654e-141">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c654e-141">Description</span></span>                                                                                           |
|-------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c654e-142">**Buffer**</span><span class="sxs-lookup"><span data-stu-id="c654e-142">**Buffer**</span></span>        | <span data-ttu-id="c654e-143">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="c654e-143">Optional.</span></span> <span data-ttu-id="c654e-144">Numero intero, 0 <= buffer < 4, che specifica a quale flusso viene inviato il buffer a cui andrà il valore.</span><span class="sxs-lookup"><span data-stu-id="c654e-144">An integer, 0 <= Buffer < 4, specifying which stream out buffer the value will go to.</span></span> |
| <span data-ttu-id="c654e-145">**Semantica**</span><span class="sxs-lookup"><span data-stu-id="c654e-145">**Semantic**</span></span>      | <span data-ttu-id="c654e-146">Stringa, insieme a SemanticIndex, che specifica il valore da restituire.</span><span class="sxs-lookup"><span data-stu-id="c654e-146">A string, along with SemanticIndex, specifying which value to output.</span></span>                                 |
| <span data-ttu-id="c654e-147">**SemanticIndex**</span><span class="sxs-lookup"><span data-stu-id="c654e-147">**SemanticIndex**</span></span> | <span data-ttu-id="c654e-148">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="c654e-148">Optional.</span></span> <span data-ttu-id="c654e-149">Indice associato a Semantic.</span><span class="sxs-lookup"><span data-stu-id="c654e-149">The index associated with Semantic.</span></span>                                                         |
| <span data-ttu-id="c654e-150">**Mask**</span><span class="sxs-lookup"><span data-stu-id="c654e-150">**Mask**</span></span>          | <span data-ttu-id="c654e-151">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="c654e-151">Optional.</span></span> <span data-ttu-id="c654e-152">Maschera di componenti, che indica i componenti del valore da restituire.</span><span class="sxs-lookup"><span data-stu-id="c654e-152">A component mask, indicating which components of the value to output.</span></span>                       |



 

<span data-ttu-id="c654e-153">Esiste una semantica speciale, denominata "$SKIP" che indica una semantica vuota, lasciando invariata la memoria corrispondente nel buffer di flusso.</span><span class="sxs-lookup"><span data-stu-id="c654e-153">There is one special Semantic, labeled "$SKIP" which indicates an empty semantic, leaving the corresponding memory in the stream out buffer untouched.</span></span> <span data-ttu-id="c654e-154">La semantica $SKIP non può avere un SemanticIndex, ma può avere una maschera.</span><span class="sxs-lookup"><span data-stu-id="c654e-154">The $SKIP semantic cannot have a SemanticIndex, but can have a Mask.</span></span>

<span data-ttu-id="c654e-155">L'intera dichiarazione out del flusso può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="c654e-155">The entire stream out declaration can be **NULL**.</span></span>

## <a name="example"></a><span data-ttu-id="c654e-156">Esempio</span><span class="sxs-lookup"><span data-stu-id="c654e-156">Example</span></span>


```
struct GSOutput
{
int4 Pos : Position;
int4 Color : Color;
int4 Texcoord : Texcoord;
};

[maxvertexcount(1)]
void gsBase (inout PointStream<GSOutput> OutputStream, inout PointStream<GSOutput> OutputStream1)
{
GSOutput output;
output.Pos = int4(1,2,3,4);
output.Color = int4(5,6,7,8);
output.Texcoord = int4(9,10,11,12);
OutputStream.Append(output);

output.Pos = int4(1,2,3,4);
    output.Color = int4(5,6,7,8);
output.Texcoord = int4(9,10,11,12);
OutputStream1.Append(output);
};


GeometryShader pGSComp = CompileShader(gs_5_0, gsBase());
GeometryShader pGSwSO = ConstructGSWithSO(pGSComp, "0:Position.xy; 1:Position.zw; 2:Color.xy", 
                                                   "3:Texcoord.xyzw; 3:$SKIP.x;", NULL, NULL, 1);

// The following two passes perform the same operation
technique11 SOPoints
{
    pass 
    {
        SetGeometryShader(ConstructGSWithSO(pGSComp, "0:Position.xy; 1:Position.zw; 2:Color.xy", 
                                                     "3:Texcoord.xyzw; 3:$SKIP.x;", NULL, NULL, 1));
    }
    pass 
    {
        SetGeometryShader(pGSwSO);
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="c654e-157">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c654e-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c654e-158">Effetti (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="c654e-158">Effects (Direct3D 11)</span></span>](d3d11-graphics-programming-guide-effects.md)
</dt> </dl>

 

 




