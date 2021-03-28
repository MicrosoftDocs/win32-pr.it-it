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
# <a name="unpacking-and-packing-dxgi_format-for-in-place-image-editing"></a>Decompressione e compressione \_ del formato DXGI per la modifica dell'immagine In-Place

Il \_ file D3DX DXGIFormatConvert. inl contiene le funzioni di conversione del formato inline che è possibile usare in compute shader o pixel shader su hardware Direct3D 11. È possibile usare queste funzioni nell'applicazione per eseguire contemporaneamente la lettura e la scrittura in una trama. Ovvero, è possibile eseguire la modifica dell'immagine sul posto. Per usare queste funzioni di conversione del formato inline, includere il \_ file D3DX DXGIFormatConvert. inl nell'applicazione.

Il Unordered Access View (UAV) di Direct3D 11 di una risorsa Texture1D, Texture2D o Texture3D supporta letture e scritture di accesso casuale in memoria da un compute shader o pixel shader. Tuttavia, Direct3D 11 supporta contemporaneamente sia la lettura che la scrittura solo nel \_ formato DXGI formato \_ R32 \_ uint texture. Ad esempio, Direct3D 11 non supporta simultaneamente sia la lettura che la scrittura in altri formati più utili, ad esempio DXGI \_ Format \_ R8G8B8A8 \_ UNORM. È possibile usare solo un UAV per accedere in modo casuale alla scrittura in altri formati oppure è possibile usare solo un Shader Resource View (SRV) per accedere in modo casuale alla lettura da tali formati. L'hardware per la conversione del formato non è disponibile per la lettura e la scrittura simultanee in altri formati.

Tuttavia, è comunque possibile eseguire contemporaneamente la lettura e la scrittura in questi altri formati eseguendo il cast della trama al formato DXGI \_ \_ R32 \_ uint texture format quando si crea un UAV, purché il formato originale della risorsa supporti il cast al formato DXGI \_ \_ R32 \_ uint. La maggior parte dei formati di 32 bit per elemento supporta il cast nel \_ formato DXGI \_ R32 \_ uint. Eseguendo il cast della trama al formato \_ DXGI \_ R32 \_ uint texture format quando si crea un UAV, è quindi possibile eseguire simultaneamente letture e scritture nella trama, purché lo shader esegua la decompressione manuale del formato durante la lettura e la compressione durante la scrittura.

Il vantaggio di eseguire il cast della trama al formato DXGI \_ \_ R32 \_ uint texture format è che in un secondo momento è possibile usare il formato appropriato (ad esempio, DXGI \_ Format \_ R16G16 \_ float) con altre visualizzazioni nella stessa trama, ad esempio le visualizzazioni di destinazione di rendering (RTVs) o SRVs. Di conseguenza, l'hardware può eseguire il tipico formato automatico depack e Pack, può eseguire filtri di trama e così via, in cui non sono presenti limitazioni hardware.

Lo scenario seguente richiede che un'applicazione prenda la sequenza di azioni seguente per eseguire la modifica dell'immagine sul posto.

Si supponga di voler creare una trama in cui è possibile utilizzare un pixel shader o compute shader per eseguire la modifica sul posto e si desidera che i dati della trama siano archiviati in un formato discendente di uno dei seguenti formati di tipo:

-   \_Formato DXGI \_ R10G10B10A2 non \_ tipizzato
-   \_Formato DXGI \_ R8G8B8A8 non \_ tipizzato
-   \_Formato DXGI \_ B8G8R8A8 non \_ tipizzato
-   \_Formato DXGI \_ B8G8R8X8 non \_ tipizzato
-   \_Formato DXGI \_ R16G16 non \_ tipizzato

Ad esempio, il formato \_ DXGI \_ R10G10B10A2 \_ UNORM format è un discendente del formato DXGI R10G10B10A2 il formato di \_ \_ \_ tipo. Pertanto, DXGI \_ Format \_ R10G10B10A2 \_ UNORM supporta il modello di utilizzo descritto nella sequenza seguente. I formati che derivano dal \_ formato DXGI \_ R32 \_ senza tipo, ad esempio \_ il formato DXGI \_ R32 \_ float, sono supportati in modo banale senza richiedere alcuna guida alla conversione del formato descritta nella sequenza seguente.

**Per eseguire la modifica dell'immagine sul posto**

1.  Creare una trama con il formato appropriato dipendente dal tipo specificato nello scenario precedente insieme ai flag di binding necessari, ad esempio D3D11 \_ binding \_ unordered \_ Access \| d3d11 \_ Bind \_ shader \_ Resource.
2.  Per la modifica dell'immagine sul posto, creare un UAV con il formato DXGI \_ \_ R32 \_ uint format. L'API Direct3D 11 non consente in genere il cast tra i diversi formati "famiglie". Tuttavia, l'API Direct3D 11 crea un'eccezione con il formato \_ DXGI \_ R32 \_ uint.
3.  In compute shader o pixel shader usare il pacchetto di formato inline appropriato e decomprimere le funzioni fornite nel \_ file D3DX DXGIFormatConvert. inl. Si supponga, ad esempio, che il \_ formato DXGI \_ R32 \_ uint UAV della trama contenga effettivamente il \_ formato DXGI \_ R10G10B10A2 i dati in formato \_ UNORM. Dopo che l'applicazione legge un uint da UAV nello shader, deve chiamare la funzione seguente per decomprimere il formato di trama:

    ```
    XMFLOAT4 D3DX_R10G10B10A2_UNORM_to_FLOAT4(UINT packedInput)
    ```

    

    Quindi, per scrivere nel UAV nello stesso shader, l'applicazione chiama la funzione seguente per comprimere i dati dello shader in un uint che l'applicazione può scrivere nell'UAV:

    ```
    UINT D3DX_FLOAT4_to_R10G10B10A2_UNORM(hlsl_precise XMFLOAT4 unpackedInput)
    ```

    

4.  L'applicazione può quindi creare altre viste, ad esempio SRVs, con il formato richiesto. Ad esempio, l'applicazione può creare un SRV con il formato \_ DXGI \_ R10G10B10A2 \_ UNORM se la risorsa è stata creata come dxgi \_ Format \_ R10G10B10A2 senza \_ tipo. Quando uno shader accede a tale SRV, l'hardware può eseguire la conversione automatica dei tipi come di consueto.

> [!Note]  
> Se lo shader deve scrivere solo in un UAV o essere letto come SRV, nessuna di queste operazioni di conversione è necessaria perché è possibile usare UAV o SRVs completamente tipizzati. Le funzioni di conversione del formato fornite in D3DX \_ DXGIFormatConvert. inl sono potenzialmente utili solo se si vuole eseguire la lettura simultanea e la scrittura in un UAV di una trama.

 

Di seguito è riportato l'elenco delle funzioni di conversione del formato incluse nel \_ file D3DX DXGIFormatConvert. inl. Queste funzioni sono classificate in base al \_ formato DXGI che decomprimere e comprimere. Ognuno dei formati supportati discende da uno dei formati di tipo elencati nello scenario precedente e supporta il cast nel \_ formato DXGI \_ R32 \_ uint come UAV.

<dl> <dt>

<span id="DXGI_FORMAT_R10G10B10A2_UNORM"></span><span id="dxgi_format_r10g10b10a2_unorm"></span>\_Formato DXGI \_ R10G10B10A2 \_ UNORM
</dt> <dd>


```
XMFLOAT4 D3DX_R10G10B10A2_UNORM_to_FLOAT4(UINT packedInput)
UINT     D3DX_FLOAT4_to_R10G10B10A2_UNORM(hlsl_precise XMFLOAT4 unpackedInput)
```



</dd> <dt>

<span id="DXGI_FORMAT_R10G10B10A2_UINT"></span><span id="dxgi_format_r10g10b10a2_uint"></span>\_Formato DXGI \_ R10G10B10A2 \_ uint
</dt> <dd>


```
XMUINT4 D3DX_R10G10B10A2_UINT_to_UINT4(UINT packedInput)
UINT    D3DX_UINT4_to_R10G10B10A2_UINT(XMUINT4 unpackedInput)
```



</dd> <dt>

<span id="DXGI_FORMAT_R8G8B8A8_UNORM"></span><span id="dxgi_format_r8g8b8a8_unorm"></span>\_Formato DXGI \_ R8G8B8A8 \_ UNORM
</dt> <dd>


```
XMFLOAT4 D3DX_R8G8B8A8_UNORM_to_FLOAT4(UINT packedInput)
UINT     D3DX_FLOAT4_to_R8G8B8A8_UNORM(hlsl_precise XMFLOAT4 unpackedInput)
```



</dd> <dt>

<span id="DXGI_FORMAT_R8G8B8A8_UNORM_SRGB"></span><span id="dxgi_format_r8g8b8a8_unorm_srgb"></span>\_Formato DXGI \_ R8G8B8A8 \_ UNORM \_ sRGB
</dt> <dd>


```
XMFLOAT4 D3DX_R8G8B8A8_UNORM_SRGB_to_FLOAT4_inexact(UINT packedInput) *
XMFLOAT4 D3DX_R8G8B8A8_UNORM_SRGB_to_FLOAT4(UINT packedInput)
UINT     D3DX_FLOAT4_to_R8G8B8A8_UNORM_SRGB(hlsl_precise XMFLOAT4 unpackedInput)
```



> [!Note]  
> La \_ funzione di tipo inesatto usa istruzioni shader che non hanno una precisione sufficientemente elevata per fornire la risposta esatta. La funzione alternativa usa una tabella di ricerca archiviata nello shader per fornire una conversione del float >SRGB esatta.

 

</dd> <dt>

<span id="DXGI_FORMAT_R8G8B8A8_UINT"></span><span id="dxgi_format_r8g8b8a8_uint"></span>\_Formato DXGI \_ R8G8B8A8 \_ uint
</dt> <dd>


```
XMUINT4 D3DX_R8G8B8A8_UINT_to_UINT4(UINT packedInput)
XMUINT  D3DX_UINT4_to_R8G8B8A8_UINT(XMUINT4 unpackedInput)
```



</dd> <dt>

<span id="DXGI_FORMAT_R8G8B8A8_SNORM"></span><span id="dxgi_format_r8g8b8a8_snorm"></span>DXGI \_ Format \_ R8G8B8A8 \_ russar
</dt> <dd>


```
XMFLOAT4 D3DX_R8G8B8A8_SNORM_to_FLOAT4(UINT packedInput)
UINT     D3DX_FLOAT4_to_R8G8B8A8_SNORM(hlsl_precise XMFLOAT4 unpackedInput)
```



</dd> <dt>

<span id="DXGI_FORMAT_R8G8B8A8_SINT"></span><span id="dxgi_format_r8g8b8a8_sint"></span>\_Formato DXGI \_ R8G8B8A8 \_ Sint
</dt> <dd>


```
XMINT4 D3DX_R8G8B8A8_SINT_to_INT4(UINT packedInput)
UINT   D3DX_INT4_to_R8G8B8A8_SINT(XMINT4 unpackedInput)
```



</dd> <dt>

<span id="DXGI_FORMAT_B8G8R8A8_UNORM"></span><span id="dxgi_format_b8g8r8a8_unorm"></span>\_Formato DXGI \_ B8G8R8A8 \_ UNORM
</dt> <dd>


```
XMFLOAT4 D3DX_B8G8R8A8_UNORM_to_FLOAT4(UINT packedInput)
UINT     D3DX_FLOAT4_to_B8G8R8A8_UNORM(hlsl_precise XMFLOAT4 unpackedInput)
```



</dd> <dt>

<span id="DXGI_FORMAT_B8G8R8A8_UNORM_SRGB"></span><span id="dxgi_format_b8g8r8a8_unorm_srgb"></span>\_Formato DXGI \_ B8G8R8A8 \_ UNORM \_ sRGB
</dt> <dd>


```
XMFLOAT4 D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4_inexact(UINT packedInput) *
XMFLOAT4 D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4(UINT packedInput)
UINT     D3DX_FLOAT4_to_R8G8B8A8_UNORM_SRGB(hlsl_precise XMFLOAT4 unpackedInput)
```



> [!Note]  
> La \_ funzione di tipo inesatto usa istruzioni shader che non hanno una precisione sufficientemente elevata per fornire la risposta esatta. La funzione alternativa usa una tabella di ricerca archiviata nello shader per fornire una conversione del float >SRGB esatta.

 

</dd> <dt>

<span id="DXGI_FORMAT_B8G8R8X8_UNORM"></span><span id="dxgi_format_b8g8r8x8_unorm"></span>\_Formato DXGI \_ B8G8R8X8 \_ UNORM
</dt> <dd>


```
XMFLOAT3 D3DX_B8G8R8X8_UNORM_to_FLOAT3(UINT packedInput)
UINT     D3DX_FLOAT3_to_B8G8R8X8_UNORM(hlsl_precise XMFLOAT3 unpackedInput)
```



</dd> <dt>

<span id="DXGI_FORMAT_B8G8R8X8_UNORM_SRGB"></span><span id="dxgi_format_b8g8r8x8_unorm_srgb"></span>\_Formato DXGI \_ B8G8R8X8 \_ UNORM \_ sRGB
</dt> <dd>


```
XMFLOAT3 D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3_inexact(UINT packedInput) *
XMFLOAT3 D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3(UINT packedInput)
UINT     D3DX_FLOAT3_to_B8G8R8X8_UNORM_SRGB(hlsl_precise XMFLOAT3 unpackedInput)
```



> [!Note]  
> La \_ funzione di tipo inesatto usa istruzioni shader che non hanno una precisione sufficientemente elevata per fornire la risposta esatta. La funzione alternativa usa una tabella di ricerca archiviata nello shader per fornire una conversione del float >SRGB esatta.

 

</dd> <dt>

<span id="DXGI_FORMAT_R16G16_FLOAT"></span><span id="dxgi_format_r16g16_float"></span>\_Formato DXGI \_ R16G16 \_ float
</dt> <dd>


```
XMFLOAT2 D3DX_R16G16_FLOAT_to_FLOAT2(UINT packedInput)
UINT     D3DX_FLOAT2_to_R16G16_FLOAT(hlsl_precise XMFLOAT2 unpackedInput)
```



</dd> <dt>

<span id="DXGI_FORMAT_R16G16_UNORM"></span><span id="dxgi_format_r16g16_unorm"></span>\_Formato DXGI \_ R16G16 \_ UNORM
</dt> <dd>


```
XMFLOAT2 D3DX_R16G16_UNORM_to_FLOAT2(UINT packedInput)
UINT     D3DX_FLOAT2_to_R16G16_UNORM(hlsl_precise FLOAT2 unpackedInput)
```



</dd> <dt>

<span id="DXGI_FORMAT_R16G16_UINT"></span><span id="dxgi_format_r16g16_uint"></span>\_Formato DXGI \_ R16G16 \_ uint
</dt> <dd>


```
XMUINT2 D3DX_R16G16_UINT_to_UINT2(UINT packedInput)
UINT    D3DX_UINT2_to_R16G16_UINT(XMUINT2 unpackedInput)
```



</dd> <dt>

<span id="DXGI_FORMAT_R16G16_SNORM"></span><span id="dxgi_format_r16g16_snorm"></span>DXGI \_ Format \_ R16G16 \_ russar
</dt> <dd>


```
XMFLOAT2 D3DX_R16G16_SNORM_to_FLOAT2(UINT packedInput)
UINT     D3DX_FLOAT2_to_R16G16_SNORM(hlsl_precise XMFLOAT2 unpackedInput)
```



</dd> <dt>

<span id="DXGI_FORMAT_R16G16_SINT"></span><span id="dxgi_format_r16g16_sint"></span>\_Formato DXGI \_ R16G16 \_ Sint
</dt> <dd>


```
XMINT2 D3DX_R16G16_SINT_to_INT2(UINT packedInput)
UINT   D3DX_INT2_to_R16G16_SINT(XMINT2 unpackedInput)
```



</dd> </dl>

## <a name="related-topics"></a>Argomenti correlati

[Guida alla programmazione per HLSL](dx-graphics-hlsl-pguide.md)


## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida alla programmazione per HLSL](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

 




