---
title: Decompressione e compressione DXGI_FORMAT per la modifica di immagini In-Place
description: Il \_ file D3DX DXGIFormatConvert. inl contiene le funzioni di conversione del formato inline che è possibile usare in compute shader o pixel shader su hardware Direct3D 11.
ms.assetid: 328c4488-9758-4359-a37b-ac50f20e2940
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c613a3f0068537733961b58a8a4c2b4528d21f25
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329071"
---
# <a name="unpacking-and-packing-dxgi_format-for-in-place-image-editing"></a><span data-ttu-id="29af2-103">Decompressione e compressione \_ del formato DXGI per la modifica dell'immagine In-Place</span><span class="sxs-lookup"><span data-stu-id="29af2-103">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>

<span data-ttu-id="29af2-104">Il \_ file D3DX DXGIFormatConvert. inl contiene le funzioni di conversione del formato inline che è possibile usare in compute shader o pixel shader su hardware Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="29af2-104">The D3DX\_DXGIFormatConvert.inl file contains inline format conversion functions that you can use in the compute shader or pixel shader on Direct3D 11 hardware.</span></span> <span data-ttu-id="29af2-105">È possibile usare queste funzioni nell'applicazione per eseguire contemporaneamente la lettura e la scrittura in una trama.</span><span class="sxs-lookup"><span data-stu-id="29af2-105">You can use these functions in your application to simultaneously both read from and write to a texture.</span></span> <span data-ttu-id="29af2-106">Ovvero, è possibile eseguire la modifica dell'immagine sul posto.</span><span class="sxs-lookup"><span data-stu-id="29af2-106">That is, you can perform in-place image editing.</span></span> <span data-ttu-id="29af2-107">Per usare queste funzioni di conversione del formato inline, includere il \_ file D3DX DXGIFormatConvert. inl nell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="29af2-107">To use these inline format conversion functions, include the D3DX\_DXGIFormatConvert.inl file in your application.</span></span>

<span data-ttu-id="29af2-108">Il Unordered Access View (UAV) di Direct3D 11 di una risorsa Texture1D, Texture2D o Texture3D supporta letture e scritture di accesso casuale in memoria da un compute shader o pixel shader.</span><span class="sxs-lookup"><span data-stu-id="29af2-108">Direct3D 11's Unordered Access View (UAV) of a Texture1D, Texture2D, or Texture3D resource supports random access reads and writes to memory from a compute shader or pixel shader.</span></span> <span data-ttu-id="29af2-109">Tuttavia, Direct3D 11 supporta contemporaneamente sia la lettura che la scrittura solo nel \_ formato DXGI formato \_ R32 \_ uint texture.</span><span class="sxs-lookup"><span data-stu-id="29af2-109">However, Direct3D 11 supports simultaneously both reading from and writing to only the DXGI\_FORMAT\_R32\_UINT texture format.</span></span> <span data-ttu-id="29af2-110">Ad esempio, Direct3D 11 non supporta simultaneamente sia la lettura che la scrittura in altri formati più utili, ad esempio DXGI \_ Format \_ R8G8B8A8 \_ UNORM.</span><span class="sxs-lookup"><span data-stu-id="29af2-110">For example, Direct3D 11 does not support simultaneously both reading from and writing to other, more useful formats, such as DXGI\_FORMAT\_R8G8B8A8\_UNORM.</span></span> <span data-ttu-id="29af2-111">È possibile usare solo un UAV per accedere in modo casuale alla scrittura in altri formati oppure è possibile usare solo un Shader Resource View (SRV) per accedere in modo casuale alla lettura da tali formati.</span><span class="sxs-lookup"><span data-stu-id="29af2-111">You can use only a UAV to random access write to such other formats, or you can use only a Shader Resource View (SRV) to random access read from such other formats.</span></span> <span data-ttu-id="29af2-112">L'hardware per la conversione del formato non è disponibile per la lettura e la scrittura simultanee in altri formati.</span><span class="sxs-lookup"><span data-stu-id="29af2-112">Format conversion hardware is not available to simultaneously both read from and write to such other formats.</span></span>

<span data-ttu-id="29af2-113">Tuttavia, è comunque possibile eseguire contemporaneamente la lettura e la scrittura in questi altri formati eseguendo il cast della trama al formato DXGI \_ \_ R32 \_ uint texture format quando si crea un UAV, purché il formato originale della risorsa supporti il cast al formato DXGI \_ \_ R32 \_ uint.</span><span class="sxs-lookup"><span data-stu-id="29af2-113">However, you can still simultaneously both read from and write to such other formats by casting the texture to the DXGI\_FORMAT\_R32\_UINT texture format when you create a UAV, as long as the original format of the resource supports casting to DXGI\_FORMAT\_R32\_UINT.</span></span> <span data-ttu-id="29af2-114">La maggior parte dei formati di 32 bit per elemento supporta il cast nel \_ formato DXGI \_ R32 \_ uint.</span><span class="sxs-lookup"><span data-stu-id="29af2-114">Most 32 bit per element formats support casting to DXGI\_FORMAT\_R32\_UINT.</span></span> <span data-ttu-id="29af2-115">Eseguendo il cast della trama al formato \_ DXGI \_ R32 \_ uint texture format quando si crea un UAV, è quindi possibile eseguire simultaneamente letture e scritture nella trama, purché lo shader esegua la decompressione manuale del formato durante la lettura e la compressione durante la scrittura.</span><span class="sxs-lookup"><span data-stu-id="29af2-115">By casting the texture to the DXGI\_FORMAT\_R32\_UINT texture format when you create a UAV, you can then simultaneous perform reads and writes to the texture as long as the shader performs manual format unpacking on read and packing on write.</span></span>

<span data-ttu-id="29af2-116">Il vantaggio di eseguire il cast della trama al formato DXGI \_ \_ R32 \_ uint texture format è che in un secondo momento è possibile usare il formato appropriato (ad esempio, DXGI \_ Format \_ R16G16 \_ float) con altre visualizzazioni nella stessa trama, ad esempio le visualizzazioni di destinazione di rendering (RTVs) o SRVs.</span><span class="sxs-lookup"><span data-stu-id="29af2-116">The benefit of casting the texture to the DXGI\_FORMAT\_R32\_UINT texture format is that later on you can use the appropriate format (for example, DXGI\_FORMAT\_R16G16\_FLOAT) with other views on the same texture, such as Render Target Views (RTVs) or SRVs.</span></span> <span data-ttu-id="29af2-117">Di conseguenza, l'hardware può eseguire il tipico formato automatico depack e Pack, può eseguire filtri di trama e così via, in cui non sono presenti limitazioni hardware.</span><span class="sxs-lookup"><span data-stu-id="29af2-117">Therefore, the hardware can perform the typical automatic format unpack and pack, can perform texture filtering, and so on where there are no hardware limitations.</span></span>

<span data-ttu-id="29af2-118">Lo scenario seguente richiede che un'applicazione prenda la sequenza di azioni seguente per eseguire la modifica dell'immagine sul posto.</span><span class="sxs-lookup"><span data-stu-id="29af2-118">The following scenario requires that an application take the following sequence of actions to perform in-place image editing.</span></span>

<span data-ttu-id="29af2-119">Si supponga di voler creare una trama in cui è possibile utilizzare un pixel shader o compute shader per eseguire la modifica sul posto e si desidera che i dati della trama siano archiviati in un formato discendente di uno dei seguenti formati di tipo:</span><span class="sxs-lookup"><span data-stu-id="29af2-119">Suppose you want to make a texture on which you can use a pixel shader or compute shader to perform in-place editing, and you want the texture data to be stored in a format that is a descendant of one of the following TYPELESS formats:</span></span>

-   <span data-ttu-id="29af2-120">\_Formato DXGI \_ R10G10B10A2 non \_ tipizzato</span><span class="sxs-lookup"><span data-stu-id="29af2-120">DXGI\_FORMAT\_R10G10B10A2\_TYPELESS</span></span>
-   <span data-ttu-id="29af2-121">\_Formato DXGI \_ R8G8B8A8 non \_ tipizzato</span><span class="sxs-lookup"><span data-stu-id="29af2-121">DXGI\_FORMAT\_R8G8B8A8\_TYPELESS</span></span>
-   <span data-ttu-id="29af2-122">\_Formato DXGI \_ B8G8R8A8 non \_ tipizzato</span><span class="sxs-lookup"><span data-stu-id="29af2-122">DXGI\_FORMAT\_B8G8R8A8\_TYPELESS</span></span>
-   <span data-ttu-id="29af2-123">\_Formato DXGI \_ B8G8R8X8 non \_ tipizzato</span><span class="sxs-lookup"><span data-stu-id="29af2-123">DXGI\_FORMAT\_B8G8R8X8\_TYPELESS</span></span>
-   <span data-ttu-id="29af2-124">\_Formato DXGI \_ R16G16 non \_ tipizzato</span><span class="sxs-lookup"><span data-stu-id="29af2-124">DXGI\_FORMAT\_R16G16\_TYPELESS</span></span>

<span data-ttu-id="29af2-125">Ad esempio, il formato \_ DXGI \_ R10G10B10A2 \_ UNORM format è un discendente del formato DXGI R10G10B10A2 il formato di \_ \_ \_ tipo.</span><span class="sxs-lookup"><span data-stu-id="29af2-125">For example, the DXGI\_FORMAT\_R10G10B10A2\_UNORM format is a descendant of the DXGI\_FORMAT\_R10G10B10A2\_TYPELESS format.</span></span> <span data-ttu-id="29af2-126">Pertanto, DXGI \_ Format \_ R10G10B10A2 \_ UNORM supporta il modello di utilizzo descritto nella sequenza seguente.</span><span class="sxs-lookup"><span data-stu-id="29af2-126">Therefore, DXGI\_FORMAT\_R10G10B10A2\_UNORM supports the usage pattern that is described in the following sequence.</span></span> <span data-ttu-id="29af2-127">I formati che derivano dal \_ formato DXGI \_ R32 \_ senza tipo, ad esempio \_ il formato DXGI \_ R32 \_ float, sono supportati in modo banale senza richiedere alcuna guida alla conversione del formato descritta nella sequenza seguente.</span><span class="sxs-lookup"><span data-stu-id="29af2-127">Formats that descend from DXGI\_FORMAT\_R32\_TYPELESS, such as DXGI\_FORMAT\_R32\_FLOAT, are trivially supported without requiring any of the format conversion help that is described in the following sequence.</span></span>

<span data-ttu-id="29af2-128">**Per eseguire la modifica dell'immagine sul posto**</span><span class="sxs-lookup"><span data-stu-id="29af2-128">**To perform in-place image editing**</span></span>

1.  <span data-ttu-id="29af2-129">Creare una trama con il formato appropriato dipendente dal tipo specificato nello scenario precedente insieme ai flag di binding necessari, ad esempio D3D11 \_ binding \_ unordered \_ Access \| d3d11 \_ Bind \_ shader \_ Resource.</span><span class="sxs-lookup"><span data-stu-id="29af2-129">Create a texture with the appropriate TYPELESS-dependent format that is specified in the previous scenario together with the required bind flags, such as D3D11\_BIND\_UNORDERED\_ACCESS \| D3D11\_BIND\_SHADER\_RESOURCE.</span></span>
2.  <span data-ttu-id="29af2-130">Per la modifica dell'immagine sul posto, creare un UAV con il formato DXGI \_ \_ R32 \_ uint format.</span><span class="sxs-lookup"><span data-stu-id="29af2-130">For in-place image editing, create a UAV with the DXGI\_FORMAT\_R32\_UINT format.</span></span> <span data-ttu-id="29af2-131">L'API Direct3D 11 non consente in genere il cast tra i diversi formati "famiglie".</span><span class="sxs-lookup"><span data-stu-id="29af2-131">The Direct3D 11 API typically does not allow casting between different format "families."</span></span> <span data-ttu-id="29af2-132">Tuttavia, l'API Direct3D 11 crea un'eccezione con il formato \_ DXGI \_ R32 \_ uint.</span><span class="sxs-lookup"><span data-stu-id="29af2-132">However, the Direct3D 11 API makes an exception with the DXGI\_FORMAT\_R32\_UINT format.</span></span>
3.  <span data-ttu-id="29af2-133">In compute shader o pixel shader usare il pacchetto di formato inline appropriato e decomprimere le funzioni fornite nel \_ file D3DX DXGIFormatConvert. inl.</span><span class="sxs-lookup"><span data-stu-id="29af2-133">In the compute shader or pixel shader, use the appropriate inline format pack and unpack functions that are provided in the D3DX\_DXGIFormatConvert.inl file.</span></span> <span data-ttu-id="29af2-134">Si supponga, ad esempio, che il \_ formato DXGI \_ R32 \_ uint UAV della trama contenga effettivamente il \_ formato DXGI \_ R10G10B10A2 i dati in formato \_ UNORM.</span><span class="sxs-lookup"><span data-stu-id="29af2-134">For example, suppose the DXGI\_FORMAT\_R32\_UINT UAV of the texture really holds DXGI\_FORMAT\_R10G10B10A2\_UNORM-formatted data.</span></span> <span data-ttu-id="29af2-135">Dopo che l'applicazione legge un uint da UAV nello shader, deve chiamare la funzione seguente per decomprimere il formato di trama:</span><span class="sxs-lookup"><span data-stu-id="29af2-135">After the application reads a uint from the UAV into the shader, it must call the following function to unpack the texture format:</span></span>

    ```
    XMFLOAT4 D3DX_R10G10B10A2_UNORM_to_FLOAT4(UINT packedInput)
    ```

    

    <span data-ttu-id="29af2-136">Quindi, per scrivere nel UAV nello stesso shader, l'applicazione chiama la funzione seguente per comprimere i dati dello shader in un uint che l'applicazione può scrivere nell'UAV:</span><span class="sxs-lookup"><span data-stu-id="29af2-136">Then, to write to the UAV in the same shader, the application calls the following function to pack shader data into a uint that the application can write to the UAV:</span></span>

    ```
    UINT D3DX_FLOAT4_to_R10G10B10A2_UNORM(hlsl_precise XMFLOAT4 unpackedInput)
    ```

    

4.  <span data-ttu-id="29af2-137">L'applicazione può quindi creare altre viste, ad esempio SRVs, con il formato richiesto.</span><span class="sxs-lookup"><span data-stu-id="29af2-137">The application can then create other views, such as SRVs, with the required format.</span></span> <span data-ttu-id="29af2-138">Ad esempio, l'applicazione può creare un SRV con il formato \_ DXGI \_ R10G10B10A2 \_ UNORM se la risorsa è stata creata come dxgi \_ Format \_ R10G10B10A2 senza \_ tipo.</span><span class="sxs-lookup"><span data-stu-id="29af2-138">For example, the application can create a SRV with the DXGI\_FORMAT\_R10G10B10A2\_UNORM format if the resource was created as DXGI\_FORMAT\_R10G10B10A2\_TYPELESS.</span></span> <span data-ttu-id="29af2-139">Quando uno shader accede a tale SRV, l'hardware può eseguire la conversione automatica dei tipi come di consueto.</span><span class="sxs-lookup"><span data-stu-id="29af2-139">When a shader accesses that SRV, the hardware can perform automatic type conversion as usual.</span></span>

> [!Note]  
> <span data-ttu-id="29af2-140">Se lo shader deve scrivere solo in un UAV o essere letto come SRV, nessuna di queste operazioni di conversione è necessaria perché è possibile usare UAV o SRVs completamente tipizzati.</span><span class="sxs-lookup"><span data-stu-id="29af2-140">If the shader must write only to a UAV, or read as an SRV, none of this conversion work is needed because you can use fully typed UAVs or SRVs.</span></span> <span data-ttu-id="29af2-141">Le funzioni di conversione del formato fornite in D3DX \_ DXGIFormatConvert. inl sono potenzialmente utili solo se si vuole eseguire la lettura simultanea e la scrittura in un UAV di una trama.</span><span class="sxs-lookup"><span data-stu-id="29af2-141">The format conversion functions provided in D3DX\_DXGIFormatConvert.inl are potentially useful only if you want to perform simultaneous reading from and writing to a UAV of a texture.</span></span>

 

<span data-ttu-id="29af2-142">Di seguito è riportato l'elenco delle funzioni di conversione del formato incluse nel \_ file D3DX DXGIFormatConvert. inl.</span><span class="sxs-lookup"><span data-stu-id="29af2-142">The following is the list of format conversion functions that are included in the D3DX\_DXGIFormatConvert.inl file.</span></span> <span data-ttu-id="29af2-143">Queste funzioni sono classificate in base al \_ formato DXGI che decomprimere e comprimere.</span><span class="sxs-lookup"><span data-stu-id="29af2-143">These functions are categorized by the DXGI\_FORMAT that they unpack and pack.</span></span> <span data-ttu-id="29af2-144">Ognuno dei formati supportati discende da uno dei formati di tipo elencati nello scenario precedente e supporta il cast nel \_ formato DXGI \_ R32 \_ uint come UAV.</span><span class="sxs-lookup"><span data-stu-id="29af2-144">Each of the supported formats descends from one of the TYPELESS formats listed in the preceding scenario and supports casting to DXGI\_FORMAT\_R32\_UINT as a UAV.</span></span>

<dl> <dt>

<span data-ttu-id="29af2-145"><span id="DXGI_FORMAT_R10G10B10A2_UNORM"></span><span id="dxgi_format_r10g10b10a2_unorm"></span>\_Formato DXGI \_ R10G10B10A2 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="29af2-145"><span id="DXGI_FORMAT_R10G10B10A2_UNORM"></span><span id="dxgi_format_r10g10b10a2_unorm"></span>DXGI\_FORMAT\_R10G10B10A2\_UNORM</span></span>
</dt> <dd>


```
XMFLOAT4 D3DX_R10G10B10A2_UNORM_to_FLOAT4(UINT packedInput)
UINT     D3DX_FLOAT4_to_R10G10B10A2_UNORM(hlsl_precise XMFLOAT4 unpackedInput)
```



</dd> <dt>

<span data-ttu-id="29af2-146"><span id="DXGI_FORMAT_R10G10B10A2_UINT"></span><span id="dxgi_format_r10g10b10a2_uint"></span>\_Formato DXGI \_ R10G10B10A2 \_ uint</span><span class="sxs-lookup"><span data-stu-id="29af2-146"><span id="DXGI_FORMAT_R10G10B10A2_UINT"></span><span id="dxgi_format_r10g10b10a2_uint"></span>DXGI\_FORMAT\_R10G10B10A2\_UINT</span></span>
</dt> <dd>


```
XMUINT4 D3DX_R10G10B10A2_UINT_to_UINT4(UINT packedInput)
UINT    D3DX_UINT4_to_R10G10B10A2_UINT(XMUINT4 unpackedInput)
```



</dd> <dt>

<span data-ttu-id="29af2-147"><span id="DXGI_FORMAT_R8G8B8A8_UNORM"></span><span id="dxgi_format_r8g8b8a8_unorm"></span>\_Formato DXGI \_ R8G8B8A8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="29af2-147"><span id="DXGI_FORMAT_R8G8B8A8_UNORM"></span><span id="dxgi_format_r8g8b8a8_unorm"></span>DXGI\_FORMAT\_R8G8B8A8\_UNORM</span></span>
</dt> <dd>


```
XMFLOAT4 D3DX_R8G8B8A8_UNORM_to_FLOAT4(UINT packedInput)
UINT     D3DX_FLOAT4_to_R8G8B8A8_UNORM(hlsl_precise XMFLOAT4 unpackedInput)
```



</dd> <dt>

<span data-ttu-id="29af2-148"><span id="DXGI_FORMAT_R8G8B8A8_UNORM_SRGB"></span><span id="dxgi_format_r8g8b8a8_unorm_srgb"></span>\_Formato DXGI \_ R8G8B8A8 \_ UNORM \_ sRGB</span><span class="sxs-lookup"><span data-stu-id="29af2-148"><span id="DXGI_FORMAT_R8G8B8A8_UNORM_SRGB"></span><span id="dxgi_format_r8g8b8a8_unorm_srgb"></span>DXGI\_FORMAT\_R8G8B8A8\_UNORM\_SRGB</span></span>
</dt> <dd>


```
XMFLOAT4 D3DX_R8G8B8A8_UNORM_SRGB_to_FLOAT4_inexact(UINT packedInput) *
XMFLOAT4 D3DX_R8G8B8A8_UNORM_SRGB_to_FLOAT4(UINT packedInput)
UINT     D3DX_FLOAT4_to_R8G8B8A8_UNORM_SRGB(hlsl_precise XMFLOAT4 unpackedInput)
```



> [!Note]  
> <span data-ttu-id="29af2-149">La \_ funzione di tipo inesatto usa istruzioni shader che non hanno una precisione sufficientemente elevata per fornire la risposta esatta.</span><span class="sxs-lookup"><span data-stu-id="29af2-149">The \_inexact-type function uses shader instructions that do not have high enough precision to give the exact answer.</span></span> <span data-ttu-id="29af2-150">La funzione alternativa usa una tabella di ricerca archiviata nello shader per fornire una conversione del float >SRGB esatta.</span><span class="sxs-lookup"><span data-stu-id="29af2-150">The alternative function uses a lookup table stored in the shader to give an exact SRGB->float conversion.</span></span>

 

</dd> <dt>

<span data-ttu-id="29af2-151"><span id="DXGI_FORMAT_R8G8B8A8_UINT"></span><span id="dxgi_format_r8g8b8a8_uint"></span>\_Formato DXGI \_ R8G8B8A8 \_ uint</span><span class="sxs-lookup"><span data-stu-id="29af2-151"><span id="DXGI_FORMAT_R8G8B8A8_UINT"></span><span id="dxgi_format_r8g8b8a8_uint"></span>DXGI\_FORMAT\_R8G8B8A8\_UINT</span></span>
</dt> <dd>


```
XMUINT4 D3DX_R8G8B8A8_UINT_to_UINT4(UINT packedInput)
XMUINT  D3DX_UINT4_to_R8G8B8A8_UINT(XMUINT4 unpackedInput)
```



</dd> <dt>

<span data-ttu-id="29af2-152"><span id="DXGI_FORMAT_R8G8B8A8_SNORM"></span><span id="dxgi_format_r8g8b8a8_snorm"></span>DXGI \_ Format \_ R8G8B8A8 \_ russar</span><span class="sxs-lookup"><span data-stu-id="29af2-152"><span id="DXGI_FORMAT_R8G8B8A8_SNORM"></span><span id="dxgi_format_r8g8b8a8_snorm"></span>DXGI\_FORMAT\_R8G8B8A8\_SNORM</span></span>
</dt> <dd>


```
XMFLOAT4 D3DX_R8G8B8A8_SNORM_to_FLOAT4(UINT packedInput)
UINT     D3DX_FLOAT4_to_R8G8B8A8_SNORM(hlsl_precise XMFLOAT4 unpackedInput)
```



</dd> <dt>

<span data-ttu-id="29af2-153"><span id="DXGI_FORMAT_R8G8B8A8_SINT"></span><span id="dxgi_format_r8g8b8a8_sint"></span>\_Formato DXGI \_ R8G8B8A8 \_ Sint</span><span class="sxs-lookup"><span data-stu-id="29af2-153"><span id="DXGI_FORMAT_R8G8B8A8_SINT"></span><span id="dxgi_format_r8g8b8a8_sint"></span>DXGI\_FORMAT\_R8G8B8A8\_SINT</span></span>
</dt> <dd>


```
XMINT4 D3DX_R8G8B8A8_SINT_to_INT4(UINT packedInput)
UINT   D3DX_INT4_to_R8G8B8A8_SINT(XMINT4 unpackedInput)
```



</dd> <dt>

<span data-ttu-id="29af2-154"><span id="DXGI_FORMAT_B8G8R8A8_UNORM"></span><span id="dxgi_format_b8g8r8a8_unorm"></span>\_Formato DXGI \_ B8G8R8A8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="29af2-154"><span id="DXGI_FORMAT_B8G8R8A8_UNORM"></span><span id="dxgi_format_b8g8r8a8_unorm"></span>DXGI\_FORMAT\_B8G8R8A8\_UNORM</span></span>
</dt> <dd>


```
XMFLOAT4 D3DX_B8G8R8A8_UNORM_to_FLOAT4(UINT packedInput)
UINT     D3DX_FLOAT4_to_B8G8R8A8_UNORM(hlsl_precise XMFLOAT4 unpackedInput)
```



</dd> <dt>

<span data-ttu-id="29af2-155"><span id="DXGI_FORMAT_B8G8R8A8_UNORM_SRGB"></span><span id="dxgi_format_b8g8r8a8_unorm_srgb"></span>\_Formato DXGI \_ B8G8R8A8 \_ UNORM \_ sRGB</span><span class="sxs-lookup"><span data-stu-id="29af2-155"><span id="DXGI_FORMAT_B8G8R8A8_UNORM_SRGB"></span><span id="dxgi_format_b8g8r8a8_unorm_srgb"></span>DXGI\_FORMAT\_B8G8R8A8\_UNORM\_SRGB</span></span>
</dt> <dd>


```
XMFLOAT4 D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4_inexact(UINT packedInput) *
XMFLOAT4 D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4(UINT packedInput)
UINT     D3DX_FLOAT4_to_R8G8B8A8_UNORM_SRGB(hlsl_precise XMFLOAT4 unpackedInput)
```



> [!Note]  
> <span data-ttu-id="29af2-156">La \_ funzione di tipo inesatto usa istruzioni shader che non hanno una precisione sufficientemente elevata per fornire la risposta esatta.</span><span class="sxs-lookup"><span data-stu-id="29af2-156">The \_inexact-type function uses shader instructions that do not have high enough precision to give the exact answer.</span></span> <span data-ttu-id="29af2-157">La funzione alternativa usa una tabella di ricerca archiviata nello shader per fornire una conversione del float >SRGB esatta.</span><span class="sxs-lookup"><span data-stu-id="29af2-157">The alternative function uses a lookup table stored in the shader to give an exact SRGB->float conversion.</span></span>

 

</dd> <dt>

<span data-ttu-id="29af2-158"><span id="DXGI_FORMAT_B8G8R8X8_UNORM"></span><span id="dxgi_format_b8g8r8x8_unorm"></span>\_Formato DXGI \_ B8G8R8X8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="29af2-158"><span id="DXGI_FORMAT_B8G8R8X8_UNORM"></span><span id="dxgi_format_b8g8r8x8_unorm"></span>DXGI\_FORMAT\_B8G8R8X8\_UNORM</span></span>
</dt> <dd>


```
XMFLOAT3 D3DX_B8G8R8X8_UNORM_to_FLOAT3(UINT packedInput)
UINT     D3DX_FLOAT3_to_B8G8R8X8_UNORM(hlsl_precise XMFLOAT3 unpackedInput)
```



</dd> <dt>

<span data-ttu-id="29af2-159"><span id="DXGI_FORMAT_B8G8R8X8_UNORM_SRGB"></span><span id="dxgi_format_b8g8r8x8_unorm_srgb"></span>\_Formato DXGI \_ B8G8R8X8 \_ UNORM \_ sRGB</span><span class="sxs-lookup"><span data-stu-id="29af2-159"><span id="DXGI_FORMAT_B8G8R8X8_UNORM_SRGB"></span><span id="dxgi_format_b8g8r8x8_unorm_srgb"></span>DXGI\_FORMAT\_B8G8R8X8\_UNORM\_SRGB</span></span>
</dt> <dd>


```
XMFLOAT3 D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3_inexact(UINT packedInput) *
XMFLOAT3 D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3(UINT packedInput)
UINT     D3DX_FLOAT3_to_B8G8R8X8_UNORM_SRGB(hlsl_precise XMFLOAT3 unpackedInput)
```



> [!Note]  
> <span data-ttu-id="29af2-160">La \_ funzione di tipo inesatto usa istruzioni shader che non hanno una precisione sufficientemente elevata per fornire la risposta esatta.</span><span class="sxs-lookup"><span data-stu-id="29af2-160">The \_inexact-type function uses shader instructions that do not have high enough precision to give the exact answer.</span></span> <span data-ttu-id="29af2-161">La funzione alternativa usa una tabella di ricerca archiviata nello shader per fornire una conversione del float >SRGB esatta.</span><span class="sxs-lookup"><span data-stu-id="29af2-161">The alternative function uses a lookup table stored in the shader to give an exact SRGB->float conversion.</span></span>

 

</dd> <dt>

<span data-ttu-id="29af2-162"><span id="DXGI_FORMAT_R16G16_FLOAT"></span><span id="dxgi_format_r16g16_float"></span>\_Formato DXGI \_ R16G16 \_ float</span><span class="sxs-lookup"><span data-stu-id="29af2-162"><span id="DXGI_FORMAT_R16G16_FLOAT"></span><span id="dxgi_format_r16g16_float"></span>DXGI\_FORMAT\_R16G16\_FLOAT</span></span>
</dt> <dd>


```
XMFLOAT2 D3DX_R16G16_FLOAT_to_FLOAT2(UINT packedInput)
UINT     D3DX_FLOAT2_to_R16G16_FLOAT(hlsl_precise XMFLOAT2 unpackedInput)
```



</dd> <dt>

<span data-ttu-id="29af2-163"><span id="DXGI_FORMAT_R16G16_UNORM"></span><span id="dxgi_format_r16g16_unorm"></span>\_Formato DXGI \_ R16G16 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="29af2-163"><span id="DXGI_FORMAT_R16G16_UNORM"></span><span id="dxgi_format_r16g16_unorm"></span>DXGI\_FORMAT\_R16G16\_UNORM</span></span>
</dt> <dd>


```
XMFLOAT2 D3DX_R16G16_UNORM_to_FLOAT2(UINT packedInput)
UINT     D3DX_FLOAT2_to_R16G16_UNORM(hlsl_precise FLOAT2 unpackedInput)
```



</dd> <dt>

<span data-ttu-id="29af2-164"><span id="DXGI_FORMAT_R16G16_UINT"></span><span id="dxgi_format_r16g16_uint"></span>\_Formato DXGI \_ R16G16 \_ uint</span><span class="sxs-lookup"><span data-stu-id="29af2-164"><span id="DXGI_FORMAT_R16G16_UINT"></span><span id="dxgi_format_r16g16_uint"></span>DXGI\_FORMAT\_R16G16\_UINT</span></span>
</dt> <dd>


```
XMUINT2 D3DX_R16G16_UINT_to_UINT2(UINT packedInput)
UINT    D3DX_UINT2_to_R16G16_UINT(XMUINT2 unpackedInput)
```



</dd> <dt>

<span data-ttu-id="29af2-165"><span id="DXGI_FORMAT_R16G16_SNORM"></span><span id="dxgi_format_r16g16_snorm"></span>DXGI \_ Format \_ R16G16 \_ russar</span><span class="sxs-lookup"><span data-stu-id="29af2-165"><span id="DXGI_FORMAT_R16G16_SNORM"></span><span id="dxgi_format_r16g16_snorm"></span>DXGI\_FORMAT\_R16G16\_SNORM</span></span>
</dt> <dd>


```
XMFLOAT2 D3DX_R16G16_SNORM_to_FLOAT2(UINT packedInput)
UINT     D3DX_FLOAT2_to_R16G16_SNORM(hlsl_precise XMFLOAT2 unpackedInput)
```



</dd> <dt>

<span data-ttu-id="29af2-166"><span id="DXGI_FORMAT_R16G16_SINT"></span><span id="dxgi_format_r16g16_sint"></span>\_Formato DXGI \_ R16G16 \_ Sint</span><span class="sxs-lookup"><span data-stu-id="29af2-166"><span id="DXGI_FORMAT_R16G16_SINT"></span><span id="dxgi_format_r16g16_sint"></span>DXGI\_FORMAT\_R16G16\_SINT</span></span>
</dt> <dd>


```
XMINT2 D3DX_R16G16_SINT_to_INT2(UINT packedInput)
UINT   D3DX_INT2_to_R16G16_SINT(XMINT2 unpackedInput)
```



</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="29af2-167">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="29af2-167">Related Topics</span></span>

[<span data-ttu-id="29af2-168">Guida alla programmazione per HLSL</span><span class="sxs-lookup"><span data-stu-id="29af2-168">Programming Guide for HLSL</span></span>](dx-graphics-hlsl-pguide.md)


## <a name="related-topics"></a><span data-ttu-id="29af2-169">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="29af2-169">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="29af2-170">Guida alla programmazione per HLSL</span><span class="sxs-lookup"><span data-stu-id="29af2-170">Programming Guide for HLSL</span></span>](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

 




