---
title: Stream-Output Object
description: Un oggetto di output di flusso è un oggetto basato su modelli che consente di trasmettere dati dalla fase geometry-shader. Usare la sintassi seguente per dichiarare un oggetto di output di flusso.
ms.assetid: 07a5489c-c238-4466-9282-5b168448aff7
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 79e0247b424ebb6f72622565845c17b622ab715cd8860a83ce24ae58ac7420c6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119789481"
---
# <a name="stream-output-object"></a>Stream-Output Object

Un oggetto di output di flusso è un oggetto basato su modelli che consente di trasmettere dati dalla [fase geometry-shader](/previous-versions//bb205146(v=vs.85)). Usare la sintassi seguente per dichiarare un oggetto di output di flusso.



| inout *StreamOutputObject* < *DataType* >  *Name;* |
|------------------------------------------------------|



 

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="StreamOutputObject___________________________DataType_________________________________________Name"></span><span id="streamoutputobject___________________________datatype_________________________________________name"></span><span id="STREAMOUTPUTOBJECT___________________________DATATYPE_________________________________________NAME"></span>*StreamOutputObject*  <  *Tipo di dati*  >    *Nome*
</dt> <dd>

Dichiarazione so (Stream-Output Object).



| Stream-Output tipi di oggetto | Descrizione                       |
|----------------------------|-----------------------------------|
| *PointStream*              | Sequenza di primitive di punti    |
| *LineStream*               | Sequenza di primitive di riga     |
| *TriangleStream*           | Sequenza di primitive di triangoli |



 

*Tipo di dati* : tipo di dati di output; può essere qualsiasi [tipo di dati HLSL](dx-graphics-hlsl-data-types.md). Deve essere racchiuso tra parentesi angolari.

*Nome* - Nome variabile; Stringa ASCII che identifica in modo univoco l'oggetto .

</dd> </dl>

## <a name="example"></a>Esempio

Questo è un esempio di dichiarazione di oggetto di output di flusso che genera il flusso di primitive triangolo i cui dati sono definiti dalla struttura PS \_ CUBEMAP \_ IN. Lo shader geometry è limitato alla generazione di 18 vertici.


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



Si tratta di un frammento di codice [dell'esempio CubeMapGS](https://msdn.microsoft.com/library/Ee416398(v=VS.85).aspx).

## <a name="stream-output-object-methods"></a>Stream-Output metodi dell'oggetto

Usare la sintassi seguente per chiamare i metodi stream-output-object.


```
Object.Method
```



Vengono implementati i metodi seguenti.



| Metodi                                              | Descrizione                                                      |
|------------------------------------------------------|------------------------------------------------------------------|
| [Accoda](dx-graphics-hlsl-so-append.md)             | Aggiungere i dati di output a un flusso esistente.                        |
| [RestartStrip](dx-graphics-hlsl-so-restartstrip.md) | Terminare la striscia primitiva corrente e avviare una nuova striscia primitiva. |



 

## <a name="minimum-shader-model"></a>Modello di shader minimo

Questo oggetto è supportato nei modelli shader seguenti.



| Modello di shader                                                        | Supportato |
|---------------------------------------------------------------------|-----------|
| [Modelli shader modello 4](dx-graphics-hlsl-sm4.md) e versioni successive | sì       |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modello shader 4](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 