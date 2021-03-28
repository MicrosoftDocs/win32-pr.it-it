---
title: Sintassi di dichiarazione di funzione
description: Le funzioni HLSL sono dichiarate con la sintassi seguente.
ms.assetid: f8968de2-7b2d-4a2e-8312-cec5b652f700
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7358a59dba0096f5c8ffe58072a974ebff9a1050
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399570"
---
# <a name="function-declaration-syntax"></a>Sintassi di dichiarazione di funzione

Le funzioni HLSL sono dichiarate con la sintassi seguente.



|                                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------------|
| \[*StorageClass* \] \[clipplanes () \] \[ nome preciso del \] \_ valore restituito  ( \[ *argomento argument* \] ) \[ : *semantica* \] { \[ *StatementBlock* \] }; |



 

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="StorageClass"></span><span id="storageclass"></span><span id="STORAGECLASS"></span>*StorageClass*
</dt> <dd>

Modificatore che ridefinisce una dichiarazione di funzione. **inline** è attualmente l'unico valore del modificatore. Il valore del modificatore deve essere **inline** perché è anche il valore predefinito. Una funzione è quindi inline indipendentemente dal fatto che sia stato specificato **inline** e che tutte le funzioni in HLSL siano inline. Una funzione inline genera una copia del corpo della funzione (durante la compilazione) per ogni chiamata di funzione. Questa operazione viene eseguita per ridurre l'overhead associato alla chiamata alla funzione.

</dd> <dt>

<span id="Clipplanes"></span><span id="clipplanes"></span><span id="CLIPPLANES"></span>*Clipplanes*
</dt> <dd>

Elenco facoltativo di piani di ritaglio, ovvero fino a 6 piani di ritaglio specificati dall'utente. Si tratta di un meccanismo alternativo per [SV \_ Clipdistance](dx-graphics-hlsl-semantics.md) che funziona a [livello di funzionalità](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9 \_ x e versioni successive.

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

Stringa facoltativa che identifica l'utilizzo previsto dei dati restituiti (vedere [semantica (DirectX HLSL)](dx-graphics-hlsl-semantics.md)).

</dd> <dt>

<span id="StatementBlock"></span><span id="statementblock"></span><span id="STATEMENTBLOCK"></span>*StatementBlock*
</dt> <dd>

[Istruzioni](dx-graphics-hlsl-statement-blocks.md) facoltative che compongono il corpo della funzione. Una funzione definita senza un corpo viene chiamata prototipo di funzione. il corpo di una funzione Prototype deve essere definito altrove prima che la funzione possa essere chiamata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il tipo restituito può essere uno di questi [tipi di HLSL](dx-graphics-hlsl-data-types.md).

## <a name="remarks"></a>Commenti

La sintassi in questa pagina descrive quasi tutti i tipi di funzione HLSL, inclusi vertex shader, pixel shader e funzioni helper. Anche se un geometry shader viene implementato con una funzione, la sua sintassi è leggermente più complicata, quindi esiste una pagina separata che definisce una dichiarazione di funzione geometry shader (vedere [oggetto Geometry-shader (DirectX HLSL)](dx-graphics-hlsl-geometry-shader.md)).

Una funzione può essere sottoposto a overload purché venga fornita una combinazione univoca di tipi di parametro e/o ordine dei parametri. HLSL implementa anche una serie di [**funzioni intrinseche**](dx-graphics-hlsl-intrinsic-functions.md)o predefinite.

È possibile specificare i piani di ritaglio specifici dell'utente con l'attributo **clipplanes** . Windows applica questi piani di ritaglio a tutte le primitive disegnate. L'attributo **clipplanes** funziona come [SV \_ Clipdistance](dx-graphics-hlsl-semantics.md) ma funziona su tutti i [livelli di funzionalità](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) hardware 9 \_ x e versioni successive. Per altre informazioni, vedere la pagina [relativa ai piani di ritaglio utente su hardware di livello funzionalità 9](/windows/desktop/direct3dhlsl/user-clip-planes-on-10level9).

## <a name="examples"></a>Esempio

Questo esempio è riportato da BasicHLSL10. FX dell' [esempio BasicHLSL10](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx).


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



Questo esempio di AdvancedParticles. FX dell' [esempio AdvancedParticles](https://msdn.microsoft.com/library/Ee416394(v=VS.85).aspx)illustra l'uso di una semantica per il tipo restituito.


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

 

 