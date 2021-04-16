---
description: Gli handle forniscono un mezzo efficace per fare riferimento a tecniche, passaggi, annotazioni e parametri con ID3DXEffectCompiler o ID3DXEffect.
ms.assetid: 2494ecf9-88a7-43dc-a75b-ed743b11993a
title: Handle (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9e0dbbcbbc38685cae7c89b334bfb5458bc8386
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521426"
---
# <a name="handles-direct3d-9"></a>Handle (Direct3D 9)

Gli handle forniscono un mezzo efficace per fare riferimento a tecniche, passaggi, annotazioni e parametri con [**ID3DXEffectCompiler**](id3dxeffectcompiler.md) o [**ID3DXEffect**](id3dxeffect.md). Vengono generate in modo dinamico quando si chiamano funzioni del form Get \[ Parameter \| annotation \| Function \| Technique \| pass \] \[ ByName \| BySemantic \| elemento \] .

Durante l'esecuzione di un programma, la generazione di un handle per lo stesso oggetto più volte restituirà lo stesso handle ogni volta. Tuttavia, non fare affidamento sull'handle che rimane costante quando si esegue più volte il programma. Tenere inoltre presente che gli handle generati da diverse istanze di [**ID3DXEffect**](id3dxeffect.md) e [**ID3DXEffectCompiler**](id3dxeffectcompiler.md) saranno diversi.

Se si visualizzano i file di intestazione, si noterà che gli handle (D3DXHANDLEs) sono tecnicamente puntatori di stringa.

Gli handle passati in funzioni come l'elemento GetParameter \[ ByName \| \| BySemantic \] o GetAnnotation \[ ByName \] possono essere in tre forme, come indicato di seguito:

1.  Handle restituiti da funzioni come l'elemento GetParameter \[ ByName \| \| BySemantic \] .
2.  Stringhe quali, ad esempio, datavariablename, datatechniquename o ArrayList \[ 0 \] .
3.  Handle = **null**. Sono disponibili quattro casi.
    -   Se si tratta di un valore restituito dal metodo, il metodo non è riuscito a trovare l'handle.
    -   Se un handle **null** viene passato come primo parametro dell'elemento GetParameter \[ ByName \| \| BySemantic \] , la funzione restituisce un parametro di primo livello. Viceversa, se l'handle è diverso da **null**, la funzione restituisce un membro della struttura o un elemento identificato dall'handle.
    -   Se un handle **null** viene passato come primo argomento di ValidateTechnique o il secondo argomento di IsParameterUsed, viene convalidata la tecnica corrente.
    -   Se un handle **null** viene passato come primo argomento di FindNextValidTechnique, la ricerca di una tecnica valida inizia in corrispondenza della prima tecnica nell'effetto.

Suggerimento per le prestazioni all'avvio dell'applicazione, eseguire un passaggio di inizializzazione per generare handle dalle stringhe. Da questo punto in poi, usare solo gli handle. Il passaggio delle stringhe anziché degli handle generati è più lento.

## <a name="examples"></a>Esempio

Di seguito sono riportati alcuni esempi che usano le \[ funzioni dell'elemento Get Parameter \| annotation \| \| Technique \| pass \] \[ ByName \| BySemantic \| \] per generare handle.


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

 

 



