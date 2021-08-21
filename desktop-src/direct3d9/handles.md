---
description: Gli handle forniscono un mezzo efficiente per fare riferimento a tecniche, passaggi, annotazioni e parametri con ID3DXEffectCompiler o ID3DXEffect.
ms.assetid: 2494ecf9-88a7-43dc-a75b-ed743b11993a
title: Handle (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3601696dc0849903d98fb3f2308b6229c6307a03665605741fc630c4e1256e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118094708"
---
# <a name="handles-direct3d-9"></a>Handle (Direct3D 9)

Gli handle forniscono un mezzo efficiente per fare riferimento a tecniche, passaggi, annotazioni e parametri [**con ID3DXEffectCompiler**](id3dxeffectcompiler.md) [**o ID3DXEffect**](id3dxeffect.md). Vengono generati dinamicamente quando si chiamano funzioni nel formato Get \[ Parameter Annotation Function Technique Pass \| \| \| \| \] \[ ByName \| BySemantic \| Element \] .

Durante l'esecuzione di un programma, la generazione di un handle per lo stesso oggetto più volte restituirà lo stesso handle ogni volta. Tuttavia, non affidarsi all'handle rimanendo costante quando si esegue il programma più volte. Tenere inoltre presente che gli handle generati da istanze diverse di [**ID3DXEffect**](id3dxeffect.md) e [**ID3DXEffectCompiler**](id3dxeffectcompiler.md) saranno diversi.

Se si visualizzano i file di intestazione, si noterà che gli handle (D3DXHANDLEs) sono tecnicamente puntatori di stringa.

Gli handle passati in funzioni come GetParameter \[ ByName \| Element \| BySemantic o \] GetAnnotation \[ ByName possono essere in tre \] formati:

1.  Handle restituiti da funzioni come GetParameter \[ ByName \| Element \| BySemantic. \]
2.  Stringhe come MyVariableName, MyTechniqueName o MyArray \[ \] 0.
3.  Handle = **NULL.** Esistono quattro casi.
    -   Se si tratta di un valore restituito dal metodo, il metodo non è riuscito a trovare l'handle.
    -   Se un handle **NULL** viene passato come primo parametro dell'elemento \[ GetParameter ByName \| \| BySemantic, la funzione \] restituisce un parametro di primo livello. Al contrario, se l'handle non è **NULL,** la funzione restituisce un membro della struttura o un elemento identificato dall'handle.
    -   Se un handle **NULL** viene passato come primo argomento di ValidateTechnique o nel secondo argomento di IsParameterUsed, viene convalidata la tecnica corrente.
    -   Se viene passato un handle **NULL** come primo argomento di FindNextValidTechnique, la ricerca di una tecnica valida inizia dalla prima tecnica dell'effetto.

Suggerimento sulle prestazioni All'avvio dell'applicazione, eseguire un passaggio di inizializzazione per generare handle dalle stringhe. Da quel momento in avanti, usare solo handle. Il passaggio di stringhe anziché di handle generati è più lento.

## <a name="examples"></a>Esempio

Ecco alcuni esempi che usano le funzioni Pass \[ \| \| \| \| \] \[ ByName \| BySemantic \| Element \] della funzione Get Parameter Annotation per generare handle.


```
// Gets handle of second top-level parameter handle in the effect file
h1 = GetParameter(NULL, 1);    

// Gets handle of the third struct member of MyStruct
h2 = GetParameter("MyStruct", 2); 

// Gets handle of the third array element handle of MyArray
h3 = GetParameterElement("MyArray", 2); 

// Gets handle of first member of h1 (that is, the second top-level param)
h4 = GetParameter(h1, 0);    

// Gets handle of MyStruct.Data
h5 = GetParameterByName("MyStruct", "Data");    
// or 
h6 = GetParameterByName(NULL, "MyStruct.Data");    

// Gets handle of MyStruct.Data.SubData
h7 = GetParameterByName("MyStruct.Data", "SubData"); 
// or 
h8 = GetParameterByName(NULL, "MyStruct.Data.SubData");

// Gets handle of fifth annotation of h1 (that is, second top-level param)
h9 = GetAnnotation(h1, 4);    

// Gets handle of MyStruct's annotation, called Author
h10 = GetAnnotationByName("MyStruct", "Author");  
// or
h11 = GetParameterByName(NULL, "MyStruct@Author"); 
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Formato effetto](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 



