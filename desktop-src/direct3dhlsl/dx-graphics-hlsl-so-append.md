---
title: Append (oggetto Stream-Output DirectX HLSL)
description: Aggiungere dati geometry-shader-output a un flusso esistente.
ms.assetid: 7df51383-7fc7-4a6f-aaa2-6c929f0443a3
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 956d4b2e37c4430e20fc4b75b2847c096c7832369d036f5224d8c36d86b7c66c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120068171"
---
# <a name="append-directx-hlsl-stream-output-object"></a>Append (oggetto Stream-Output DirectX HLSL)

Aggiungere dati geometry-shader-output a un flusso esistente.

Append( *StreamDataType*);



 

## <a name="parameters"></a>Parametri



| Elemento                                                                                                                             | Descrizione                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="StreamDataType"></span><span id="streamdatatype"></span><span id="STREAMDATATYPE"></span>**StreamDataType**<br/> | Descrizione dell'input di dati. Questa descrizione deve corrispondere al parametro del modello stream-object denominato [DataType](dx-graphics-hlsl-so-type.md).<br/> |



 

## <a name="return-value"></a>Valore restituito

nessuno

## <a name="example"></a>Esempio

Questo frammento di codice (dall'esempio [CubeMapGS](https://msdn.microsoft.com/library/Ee416398(v=VS.85).aspx)) mostra un esempio parziale di aggiunta di primitive di striscia triangolare a un oggetto di output di flusso.


```
[maxvertexcount(18)]
void GS_CubeMap( triangle GS_CUBEMAP_IN input[3], 
                 inout TriangleStream<PS_CUBEMAP_IN> CubeMapStream )
{
    for( int f = 0; f < 6; ++f )
    {
        // Compute screen coordinates
        PS_CUBEMAP_IN output;
        output.RTIndex = f;
        for( int v = 0; v < 3; v++ )
        {
            output.Pos = mul( input[v].Pos, g_mViewCM[f] );
            output.Pos = mul( output.Pos, mProj );
            output.Tex = input[v].Tex;
            CubeMapStream.Append( output );
        }
        CubeMapStream.RestartStrip();
    }
}
```



## <a name="minimum-shader-model"></a>Modello shader minimo

Questa funzione è supportata nei modelli shader seguenti.



| Modello di shader                                              | Supportato |
|-----------------------------------------------------------|-----------|
| [Modello shader 4](dx-graphics-hlsl-sm4.md)                | sì       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Modello shader 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Modello shader 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Oggetto stream-output](dx-graphics-hlsl-so-type.md)
</dt> </dl>

 

 





