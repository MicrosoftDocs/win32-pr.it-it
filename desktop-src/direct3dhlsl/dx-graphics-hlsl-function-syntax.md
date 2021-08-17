---
title: Sintassi di dichiarazione di funzione
description: Le funzioni HLSL vengono dichiarate con la sintassi seguente.
ms.assetid: f8968de2-7b2d-4a2e-8312-cec5b652f700
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ce8c6ec83963dac74dce32d248b23548c767192a604ddb8afbe35cf932dedee9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118514606"
---
# <a name="function-declaration-syntax"></a>Sintassi di dichiarazione di funzione

Le funzioni HLSL vengono dichiarate con la sintassi seguente.

\[*StorageClass* \] \[clipplanes() \] \[ precise \] Return Value \_ *Name* ( \[ *ArgumentList* \] ) : \[ *Semantic* \] { \[ *StatementBlock* \] };



 

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="StorageClass"></span><span id="storageclass"></span><span id="STORAGECLASS"></span>*StorageClass*
</dt> <dd>

Modificatore che ridefinisce una dichiarazione di funzione. **inline** è attualmente l'unico valore modificatore. Il valore del modificatore deve **essere inline** perché è anche il valore predefinito. Pertanto, una funzione è inline indipendentemente dal fatto che si specifica **inline** e tutte le funzioni in HLSL siano inline. Una funzione inline genera una copia del corpo della funzione (durante la compilazione) per ogni chiamata di funzione. Questa operazione viene eseguita per ridurre l'overhead della chiamata alla funzione.

</dd> <dt>

<span id="Clipplanes"></span><span id="clipplanes"></span><span id="CLIPPLANES"></span>*Clipplan*
</dt> <dd>

Elenco facoltativo dei piani di ritaglio, ovvero fino a 6 piani di ritaglio specificati dall'utente. Si tratta di un meccanismo alternativo [per SV \_ ClipDistance](dx-graphics-hlsl-semantics.md) che funziona [sul](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) livello di funzionalità 9 x e versioni \_ successive.

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>*Nome*
</dt> <dd>

Stringa ASCII che identifica in modo univoco il nome della funzione shader.

</dd> <dt>

<span id="ArgumentList"></span><span id="argumentlist"></span><span id="ARGUMENTLIST"></span>*ArgumentList*
</dt> <dd>

Elenco di argomenti facoltativo, ovvero un elenco delimitato da virgole di [argomenti](dx-graphics-hlsl-function-parameters.md) passati in una funzione.

</dd> <dt>

<span id="Semantic"></span><span id="semantic"></span><span id="SEMANTIC"></span>*Semantica*
</dt> <dd>

Stringa facoltativa che identifica l'utilizzo previsto dei dati restituiti (vedere [Semantica (DirectX HLSL)](dx-graphics-hlsl-semantics.md)).

</dd> <dt>

<span id="StatementBlock"></span><span id="statementblock"></span><span id="STATEMENTBLOCK"></span>*StatementBlock*
</dt> <dd>

Istruzioni [facoltative](dx-graphics-hlsl-statement-blocks.md) che costituiscono il corpo della funzione. Una funzione definita senza corpo è denominata prototipo di funzione. Il corpo di una funzione prototipo deve essere definito altrove prima di poter chiamare la funzione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il tipo restituito può essere uno qualsiasi di [questi tipi HLSL.](dx-graphics-hlsl-data-types.md)

## <a name="remarks"></a>Commenti

La sintassi in questa pagina descrive quasi tutti i tipi di funzione HLSL, inclusi vertex shader, pixel shader e funzioni helper. Anche se un geometry shader viene implementato anche con una funzione, la relativa sintassi è un po' più complessa, quindi esiste una pagina separata che definisce una dichiarazione di funzione [geometry shader (vedere Oggetto Geometry-Shader (DirectX HLSL)](dx-graphics-hlsl-geometry-shader.md)).

È possibile eseguire l'overload di una funzione purché le sia data una combinazione univoca di tipi di parametro e/o ordine dei parametri. HLSL implementa anche una serie di funzioni intrinseche [**o incorporate.**](dx-graphics-hlsl-intrinsic-functions.md)

È possibile specificare piani di ritaglio specifici dell'utente con **l'attributo clipplanes.** Windows applica questi piani di ritaglio a tutte le primitive disegnate. **L'attributo clipplanes** funziona come [SV \_ ClipDistance,](dx-graphics-hlsl-semantics.md) ma funziona su tutti i livelli di funzionalità [hardware](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9 x e \_ versioni successive. Per altre informazioni, vedere [Piani di ritaglio utente nell'hardware del livello di funzionalità 9.](/windows/desktop/direct3dhlsl/user-clip-planes-on-10level9)

## <a name="examples"></a>Esempio

Questo esempio deriva da BasicHLSL10.fx [dell'esempio BasicHLSL10.](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx)


```hlsl
struct VS_OUTPUT
{
    float4 Position   : SV_POSITION; 
    float4 Diffuse    : COLOR0;
    float2 TextureUV  : TEXCOORD0;
};

VS_OUTPUT RenderSceneVS( float4 vPos : POSITION,
                         float3 vNormal : NORMAL,
                         float2 vTexCoord0 : TEXCOORD,
                         uniform int nNumLights,
                         uniform bool bTexture,
                         uniform bool bAnimate )
{
    VS_OUTPUT Output;
    ...
    return Output;    
}
```



Questo esempio di AdvancedParticles.fx dell'esempio [AdvancedParticles](https://msdn.microsoft.com/library/Ee416394(v=VS.85).aspx)illustra l'uso di una semantica per il tipo restituito.


```hlsl
//
// PS for particles
//
float4 PSPointSprite(PSSceneIn input) : SV_Target
{   
    return g_txDiffuse.Sample( g_samLinear, input.tex ) * input.color;
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Funzioni (DirectX HLSL)](dx-graphics-hlsl-functions.md)
</dt> </dl>

 

 
