---
title: Geometry-Shader Object
description: Un oggetto geometry shader elabora intere primitive. Usare la sintassi seguente per dichiarare un oggetto geometry-shader.
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
ms.openlocfilehash: 5b95f0bb99bd3a225afb7a63824b301b102030a4f132caa7a2a4ff1743eefb58
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119120145"
---
# <a name="geometry-shader-object"></a>Geometry-Shader Object

Un oggetto geometry shader elabora intere primitive. Usare la sintassi seguente per dichiarare un oggetto geometry-shader.

\[maxvertexcount(*NumVerts*) \] void *ShaderName* ( *PrimitiveType DataType Name \[ NumElements, \]* inout *StreamOutputObject* );



 

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="_maxvertexcount_NumVerts__"></span><span id="_maxvertexcount_numverts__"></span><span id="_MAXVERTEXCOUNT_NUMVERTS__"></span>\[maxvertexcount(*NumVerts*)\]
</dt> <dd>

\[in \] Dichiarazione per il numero massimo di vertici da creare.

-   \[maxvertexcount() - parola chiave obbligatoria. Le parentesi e le parentesi sono caratteri \] obbligatori per la sintassi corretta.
-   *NumVerts:* numero intero che rappresenta il numero di vertici.

</dd> <dt>

<span id="ShaderName"></span><span id="shadername"></span><span id="SHADERNAME"></span>*ShaderName*
</dt> <dd>

\[in \] Una stringa ASCII che contiene un nome univoco per la funzione geometry-shader.

</dd> <dt>

<span id="PrimitiveType_DataType_Name___NumElements__"></span><span id="primitivetype_datatype_name___numelements__"></span><span id="PRIMITIVETYPE_DATATYPE_NAME___NUMELEMENTS__"></span>*PrimitiveType DataType Name \[ NumElements \]*
</dt> <dd>

*PrimitiveType:* tipo primitivo, che determina l'ordine dei dati primitivi.



| Tipo primitivo | Descrizione                                                   |
|----------------|---------------------------------------------------------------|
| *Punto*        | Elenco di punti                                                    |
| *Linea*         | Elenco di righe o striscia riga                                       |
| *Triangolo*     | Elenco a triangolo o striscia triangolare                               |
| *lineadj*      | Elenco di righe con adicenza o striscia con adicenza         |
| *triangleadj*  | Elenco triangolo con adicenza o striscia triangolare con adicenza |



 

*Tipo di dati*  -  \[ in \] Un tipo di dati di input; può essere qualsiasi tipo di dati [HLSL.](dx-graphics-hlsl-data-types.md)

*Nome:* nome dell'argomento. si tratta di una stringa ASCII.

*NumElements* : dimensione della matrice dell'input, che dipende da *PrimitiveType,* come illustrato nella tabella seguente.

| Tipo primitivo | NumElements                                                                                                  |
|----------------|--------------------------------------------------------------------------------------------------------------|
| *Punto*        | \[1\]<br/> Si opera su un solo punto alla volta.<br/>                                         |
| *Linea*         | \[2\]<br/> Una linea richiede due vertici.<br/>                                                    |
| *Triangolo*     | \[3\]<br/> Un triangolo richiede tre vertici.<br/>                                              |
| *lineadj*      | \[4\]<br/> Un oggetto lineadj ha due estremità; di conseguenza, sono necessari quattro vertici.<br/>                    |
| *triangleadj*  | \[6\]<br/> Un triangolo è un triangolo con altri tre triangoli; Pertanto, richiede sei vertici.<br/> |



 

</dd> <dt>

<span id="StreamOutputObject"></span><span id="streamoutputobject"></span><span id="STREAMOUTPUTOBJECT"></span>*StreamOutputObject*
</dt> <dd>

Dichiarazione [dell'oggetto stream-output](dx-graphics-hlsl-so-type.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

nessuno

## <a name="remarks"></a>Osservazioni

Il diagramma seguente illustra i vari tipi primitivi per un oggetto geometry shader.

![Illustrazione dei vari tipi primitivi per un oggetto geometry shader](images/d3d11-gsinputs1.png)

Il diagramma seguente illustra le chiamate geometry shader.

![Illustrazione delle chiamate geometry shader](images/d3d11-gsinputs2.png)

## <a name="examples"></a>Esempio

Questo esempio deriva dall'esercizio 1 di [Direct3D 10 Shader Model 4.0 Workshop](https://msdn.microsoft.com/library/Ee416554(v=VS.85).aspx).


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



## <a name="minimum-shader-model"></a>Modello shader minimo

Questo oggetto è supportato nei modelli shader seguenti.



| Modello di shader                                                        | Supportato |
|---------------------------------------------------------------------|-----------|
| [Modelli shader modello 4](dx-graphics-hlsl-sm4.md) e versioni successive | sì       |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modello shader 4](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 





