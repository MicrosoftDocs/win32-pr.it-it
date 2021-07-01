---
title: oggetto Geometry-Shader
description: Un oggetto geometry shader elabora intere primitive. Usare la sintassi seguente per dichiarare un oggetto geometry shader.
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
ms.openlocfilehash: e06bbc184a4b5f82d5edaaf7fdbfbd55f1906f12
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120616"
---
# <a name="geometry-shader-object"></a>oggetto Geometry-Shader

Un oggetto geometry shader elabora intere primitive. Usare la sintassi seguente per dichiarare un oggetto geometry shader.

\[maxvertexcount(*NumVerts*) \] void *ShaderName* ( *PrimitiveType DataType Name \[ NumElements \]*, inout *StreamOutputObject* );



 

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="_maxvertexcount_NumVerts__"></span><span id="_maxvertexcount_numverts__"></span><span id="_MAXVERTEXCOUNT_NUMVERTS__"></span>\[maxvertexcount(*NumVerts*)\]
</dt> <dd>

\[in \] Dichiarazione per il numero massimo di vertici da creare.

-   \[maxvertexcount(): parola chiave obbligatoria. Le parentesi quadre e le parentesi sono caratteri \] obbligatori per la sintassi corretta.
-   *NumVerts:* numero intero che rappresenta il numero di vertici.

</dd> <dt>

<span id="ShaderName"></span><span id="shadername"></span><span id="SHADERNAME"></span>*ShaderName*
</dt> <dd>

\[in \] Una stringa ASCII che contiene un nome univoco per la funzione geometry shader.

</dd> <dt>

<span id="PrimitiveType_DataType_Name___NumElements__"></span><span id="primitivetype_datatype_name___numelements__"></span><span id="PRIMITIVETYPE_DATATYPE_NAME___NUMELEMENTS__"></span>*PrimitiveType DataType Name \[ NumElements \]*
</dt> <dd>

*PrimitiveType:* tipo primitivo, che determina l'ordine dei dati primitivi.



| Tipo primitivo | Descrizione                                                   |
|----------------|---------------------------------------------------------------|
| *Punto*        | Elenco di punti                                                    |
| *Linea*         | Elenco di righe o striscia di linee                                       |
| *Triangolo*     | Elenco triangolare o striscia triangolare                               |
| *lineadj*      | Elenco di righe con adicenza o striscia di linee con adicenza         |
| *triangleadj*  | Elenco di triangoli con adicenza o striscia triangolare con adicenza |



 

*Tipo di dati*  -  \[ in \] Un tipo di dati di input; può essere qualsiasi tipo di dati [HLSL](dx-graphics-hlsl-data-types.md).

*Nome* : nome dell'argomento; si tratta di una stringa ASCII.

*NumElements:* dimensione della matrice dell'input, che dipende da *PrimitiveType,* come illustrato nella tabella seguente.

| Tipo primitivo | NumElements                                                                                                  |
|----------------|--------------------------------------------------------------------------------------------------------------|
| *Punto*        | \[1\]<br/> Si opera su un solo punto alla volta.<br/>                                         |
| *Linea*         | \[2\]<br/> Una linea richiede due vertici.<br/>                                                    |
| *Triangolo*     | \[3\]<br/> Un triangolo richiede tre vertici.<br/>                                              |
| *lineadj*      | \[4\]<br/> Una lineadj ha due estremità; pertanto richiede quattro vertici.<br/>                    |
| *triangleadj*  | \[6\]<br/> Un triangoloadj snoda altri tre triangoli; pertanto richiede sei vertici.<br/> |



 

</dd> <dt>

<span id="StreamOutputObject"></span><span id="streamoutputobject"></span><span id="STREAMOUTPUTOBJECT"></span>*StreamOutputObject*
</dt> <dd>

Dichiarazione dell'oggetto [stream-output](dx-graphics-hlsl-so-type.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

nessuno

## <a name="remarks"></a>Osservazioni

Il diagramma seguente illustra i vari tipi primitivi per un oggetto geometry shader.

![illustrazione dei vari tipi primitivi per un oggetto geometry shader](images/d3d11-gsinputs1.png)

Il diagramma seguente mostra le chiamate di shader geometrici.

![illustrazione delle chiamate di geometry shader](images/d3d11-gsinputs2.png)

## <a name="examples"></a>Esempio

Questo esempio è stato creato nell'esercizio 1 di [Direct3D 10 Shader Model 4.0 Workshop](https://msdn.microsoft.com/library/Ee416554(v=VS.85).aspx).


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



## <a name="minimum-shader-model"></a>Modello di shader minimo

Questo oggetto è supportato nei modelli di shader seguenti.



| Modello di shader                                                        | Supportato |
|---------------------------------------------------------------------|-----------|
| [Modello shader 4 e](dx-graphics-hlsl-sm4.md) modelli di shader superiori | yes       |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modello shader 4](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 





