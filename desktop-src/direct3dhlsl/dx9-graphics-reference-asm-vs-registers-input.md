---
title: Registro di input
description: Registro di input
ms.assetid: 7cd8e555-4e69-4905-a541-62e09b41a602
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 983f0520ccc50fa1683d4b8254ac436fff7491a1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955614"
---
# <a name="input-register"></a>Registro di input

Registro di input vertex shader.

I dati di ogni vertice (usando uno o più flussi di vertici di input) vengono caricati nei registri di input dei vertici prima dell'esecuzione del vertex shader. I registri di input sono costituiti da vettori a virgola mobile a 16 4 componenti, designati come V0 tramite versione 15. Questi registri sono di sola lettura. Un registro di input è associato ai dati dei vertici tramite una dichiarazione di vertice.

Le proprietà Register seguenti controllano il comportamento di ogni registro:



| Proprietà        | Descrizione                                                                                   |
|-----------------|-----------------------------------------------------------------------------------------------|
| Nome            | v \[ n \] -n è un numero di registro facoltativo. 0 è il valore predefinito usato, se viene omesso.     |
| Conteggio           | Un massimo di 16 registri, V0-versione 15.                                                          |
| Autorizzazioni di I/O | Di sola lettura. Questo registro non può essere scritto dall'API o nello shader.                   |
| Leggere le porte      | 1. indica il numero di volte in cui è possibile leggere un registro all'interno di un'unica istruzione. Vedere qui di seguito. |



 

Ogni singola istruzione può accedere a un solo registro di input del vertice. Tuttavia, ogni origine nell'istruzione può swizzle in modo indipendente e negare il vettore mentre viene letto.

## <a name="example"></a>Esempio

Di seguito è riportato un esempio di utilizzo di una dichiarazione vertex per associare i dati della posizione del vertice 2D al registro V0.

La dichiarazione di vertice appartiene all'applicazione:


```
D3DVERTEXELEMENT9 decl[] =
{
    { 0, 0, D3DDECLTYPE_FLOAT2, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_POSITION, 0 },
      D3DDECL_END()
};
```



Di seguito è illustrata la dichiarazione vertex shader corrispondente:


```
dcl_position v0
```





| Versioni vertex shader | 1\_1 | 2 \_ 0 | 2 \_ SW | 2 \_ x | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|-------|------|------|-------|
| Posizione registro      | x    | x    | x     | x    | x    | x     |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registri vertex shader](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




