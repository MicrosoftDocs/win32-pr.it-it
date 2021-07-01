---
title: Append (oggetto Stream-Output DirectX HLSL)
description: Aggiungere dati di output geometry shader a un flusso esistente.
ms.assetid: 7df51383-7fc7-4a6f-aaa2-6c929f0443a3
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 19d767f3c501cc42e21bbc44a196ba08cd6f1883
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120186"
---
# <a name="append-directx-hlsl-stream-output-object"></a>Append (oggetto Stream-Output DirectX HLSL)

Aggiungere dati di output geometry shader a un flusso esistente.

Append( *StreamDataType*);



 

## <a name="parameters"></a>Parametri



| Elemento                                                                                                                             | Descrizione                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="StreamDataType"></span><span id="streamdatatype"></span><span id="STREAMDATATYPE"></span>**StreamDataType**<br/> | Descrizione dell'input di dati. Questa descrizione deve corrispondere al parametro del modello stream-object denominato [DataType](dx-graphics-hlsl-so-type.md).<br/> |



 

## <a name="return-value"></a>Valore restituito

nessuno

## <a name="example"></a>Esempio

Questo frammento di codice (dall'esempio [CubeMapGS)](https://msdn.microsoft.com/library/Ee416398(v=VS.85).aspx)illustra un esempio parziale di aggiunta di primitive di striscia triangolare a un oggetto di output del flusso.


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



## <a name="minimum-shader-model"></a>Modello di shader minimo

Questa funzione è supportata nei modelli di shader seguenti.



| Modello di shader                                              | Supportato |
|-----------------------------------------------------------|-----------|
| [Modello shader 4](dx-graphics-hlsl-sm4.md)                | yes       |
| [Modello shader 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | No        |
| [Modello shader 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | No        |
| [Modello shader 1 (HLSL DirectX)](dx-graphics-hlsl-sm1.md) | No        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Oggetto Stream-Output](dx-graphics-hlsl-so-type.md)
</dt> </dl>

 

 





