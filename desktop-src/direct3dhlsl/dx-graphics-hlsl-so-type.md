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
# <a name="stream-output-object"></a>Oggetto Stream-Output

Un oggetto Stream-output è un oggetto basato su modelli che trasmette i dati fuori dalla [fase geometry-shader](/previous-versions//bb205146(v=vs.85)). Usare la sintassi seguente per dichiarare un oggetto Stream-output.



| nome del tipo di dati *StreamOutputObject* di InOut <  >  *;* |
|------------------------------------------------------|



 

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="StreamOutputObject___________________________DataType_________________________________________Name"></span><span id="streamoutputobject___________________________datatype_________________________________________name"></span><span id="STREAMOUTPUTOBJECT___________________________DATATYPE_________________________________________NAME"></span>*StreamOutputObject*  <  *Tipo*  >  di dati   *Nome*
</dt> <dd>

Dichiarazione dell'oggetto Stream-output (SO).



| Tipi di oggetti Stream-Output | Descrizione                       |
|----------------------------|-----------------------------------|
| *PointStream*              | Sequenza di primitive di punti    |
| *LineStream*               | Sequenza di primitive di linea     |
| *TriangleStream*           | Sequenza di primitive triangolari |



 

*DataType* -tipo di dati di output; può essere qualsiasi [tipo di dati HLSL](dx-graphics-hlsl-data-types.md). Deve essere racchiuso tra parentesi acute.

*Nome: nome* della variabile; stringa ASCII che identifica in modo univoco l'oggetto.

</dd> </dl>

## <a name="example"></a>Esempio

Questo è un esempio di dichiarazione di un oggetto di output di flusso che trasmette le primitive triangolari i cui dati sono definiti da PS \_ mappa cubi \_ nella struttura. Geometry shader è limitato alla generazione di 18 vertici.


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



Si tratta di un frammento di codice dell' [esempio CubeMapGS](https://msdn.microsoft.com/library/Ee416398(v=VS.85).aspx).

## <a name="stream-output-object-methods"></a>Metodi dell'oggetto Stream-Output

Usare la sintassi seguente per chiamare i metodi Stream-output-Object.


```
Object.Method
```



Vengono implementati i metodi seguenti.



| Metodi                                              | Descrizione                                                      |
|------------------------------------------------------|------------------------------------------------------------------|
| [Accoda](dx-graphics-hlsl-so-append.md)             | Accodare i dati di output a un flusso esistente.                        |
| [RestartStrip](dx-graphics-hlsl-so-restartstrip.md) | Terminare la striscia primitiva corrente e avviare una nuova striscia primitiva. |



 

## <a name="minimum-shader-model"></a>Modello Shader minimo

Questo oggetto è supportato nei modelli shader seguenti.



| Modello di shader                                                        | Supportato |
|---------------------------------------------------------------------|-----------|
| [Shader Model 4](dx-graphics-hlsl-sm4.md) e versioni successive shader Models | sì       |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modello Shader 4](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 