---
title: Oggetto Geometry-Shader
description: Un oggetto Geometry shader elabora intere primitive. Usare la sintassi seguente per dichiarare un oggetto Geometry shader.
ms.assetid: d5c1c22b-6fa6-40a8-900f-6d74f74468c1
keywords:
- maxvertexcount (DirectX HLSL)
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: dadb0e8bb3ddda16305ac701b34523668bd9c1a5
ms.sourcegitcommit: 477b1efe7d9c2f91d5f2ac588a20edf348b1c734
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2019
ms.locfileid: "103719753"
---
# <a name="geometry-shader-object"></a>Oggetto Geometry-Shader

Un oggetto Geometry shader elabora intere primitive. Usare la sintassi seguente per dichiarare un oggetto Geometry shader.



|                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------|
| \[maxvertexcount (*NumVerts*) \] void *ShaderName* ( *PrimitiveType DataType Name \[ NumElements \]*, InOut *StreamOutputObject* ); |



 

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="_maxvertexcount_NumVerts__"></span><span id="_maxvertexcount_numverts__"></span><span id="_MAXVERTEXCOUNT_NUMVERTS__"></span>\[maxvertexcount (*NumVerts*)\]
</dt> <dd>

\[nella \] dichiarazione per il numero massimo di vertici da creare.

-   \[maxvertexcount () \] : parola chiave obbligatoria. le parentesi quadre e le parentesi sono i caratteri necessari per la sintassi corretta.
-   *NumVerts* : numero intero che rappresenta il numero di vertici.

</dd> <dt>

<span id="ShaderName"></span><span id="shadername"></span><span id="SHADERNAME"></span>*ShaderName*
</dt> <dd>

\[in \] una stringa ASCII contenente un nome univoco per la funzione geometry-shader.

</dd> <dt>

<span id="PrimitiveType_DataType_Name___NumElements__"></span><span id="primitivetype_datatype_name___numelements__"></span><span id="PRIMITIVETYPE_DATATYPE_NAME___NUMELEMENTS__"></span>*Nome del tipo di dati PrimitiveType \[ NumElements \]*
</dt> <dd>

*PrimitiveType* : tipo primitivo, che determina l'ordine dei dati primitivi.



| Tipo primitivo | Descrizione                                                   |
|----------------|---------------------------------------------------------------|
| *punto*        | Elenco di punti                                                    |
| *linea*         | Elenco linee o striscia di linea                                       |
| *triangolo*     | Elenco di triangolo o striscia di triangolo                               |
| *lineadj*      | Elenco di righe con adiacenza o striping di riga con adiacenza         |
| *triangleadj*  | Elenco di triangolo con adiacenza o striscia di triangolo con adiacenza |



 

  -  Tipo \[ di dati in \] un tipo di dati di input; può essere qualsiasi [tipo di dati HLSL](dx-graphics-hlsl-data-types.md).

*Nome* -argomento nome; si tratta di una stringa ASCII.

*NumElements* : dimensioni della matrice dell'input, che dipendono da *PrimitiveType* , come illustrato nella tabella seguente.

| Tipo primitivo | NumElements                                                                                                  |
|----------------|--------------------------------------------------------------------------------------------------------------|
| *punto*        | \[1\]<br/> Si opera su un solo punto alla volta.<br/>                                         |
| *linea*         | \[2\]<br/> Una linea richiede due vertici.<br/>                                                    |
| *triangolo*     | \[3\]<br/> Un triangolo richiede tre vertici.<br/>                                              |
| *lineadj*      | \[4\]<br/> Un lineadj ha due estremità. Pertanto, richiede quattro vertici.<br/>                    |
| *triangleadj*  | \[6\]<br/> Un triangleadj delimita altri tre triangoli; Pertanto, richiede sei vertici.<br/> |



 

</dd> <dt>

<span id="StreamOutputObject"></span><span id="streamoutputobject"></span><span id="STREAMOUTPUTOBJECT"></span>*StreamOutputObject*
</dt> <dd>

Dichiarazione dell' [oggetto flusso di output](dx-graphics-hlsl-so-type.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

nessuno

## <a name="remarks"></a>Osservazioni

Il diagramma seguente mostra i vari tipi primitivi per un oggetto Geometry shader.

![illustrazione dei vari tipi primitivi per un oggetto Geometry shader](images/d3d11-gsinputs1.png)

Il diagramma seguente illustra le chiamate a geometry shader.

![illustrazione delle chiamate geometry shader](images/d3d11-gsinputs2.png)

## <a name="examples"></a>Esempio

Questo esempio è relativo all'esercizio 1 del [workshop Direct3D 10 Shader Model 4,0](https://msdn.microsoft.com/library/Ee416554(v=VS.85).aspx).


```
[maxvertexcount(3)]
void GSScene( triangleadj GSSceneIn input[6], inout TriangleStream<PSSceneIn> OutputStream )
{   
    PSSceneIn output = (PSSceneIn)0;

    for( uint i=0; i<6; i+=2 )
    {
        output.Pos = input[i].Pos;
        output.Norm = input[i].Norm;
        output.Tex = input[i].Tex;
        
        OutputStream.Append( output );
    }
    
    OutputStream.RestartStrip();
}
```



## <a name="minimum-shader-model"></a>Modello Shader minimo

Questo oggetto è supportato nei modelli shader seguenti.



| Modello di shader                                                        | Supportato |
|---------------------------------------------------------------------|-----------|
| [Shader Model 4](dx-graphics-hlsl-sm4.md) e versioni successive shader Models | sì       |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modello Shader 4](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 





