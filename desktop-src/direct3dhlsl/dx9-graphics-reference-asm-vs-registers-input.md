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
ms.openlocfilehash: b6682d8987f2df3ba3fb06427d41b722abb5eb003a4226a155c104cc3239d0f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119982761"
---
# <a name="input-register"></a>Registro di input

Registro di input vertex shader.

I dati di ogni vertice (usando uno o più flussi dei vertici di input) vengono caricati nei registri di input dei vertici prima dell'esecuzione del vertex shader. I registri di input sono costituiti da 16 vettori a virgola mobile a quattro componenti, designati da v0 a v15. Questi registri sono di sola lettura. Un registro di input viene associato ai dati dei vertici tramite una dichiarazione di vertice.

Le proprietà del registro seguenti controllano il comportamento di ogni registro:



| Proprietà        | Descrizione                                                                                   |
|-----------------|-----------------------------------------------------------------------------------------------|
| Nome            | v \[ n - n è un numero di registro \] facoltativo. 0 è il valore predefinito utilizzato, se viene omesso.     |
| Conteggio           | Un massimo di 16 registri, v0 - v15.                                                          |
| Autorizzazioni di I/O | Di sola lettura. Questo registro non può essere scritto dall'API o all'interno dello shader.                   |
| Leggere le porte      | 1. Numero di volte in cui un registro può essere letto all'interno di una singola istruzione. Vedere qui di seguito. |



 

Qualsiasi singola istruzione può accedere a un solo registro di input dei vertici. Tuttavia, ogni origine nell'istruzione può eseguire lo swizzle in modo indipendente e negare tale vettore durante la lettura.

## <a name="example"></a>Esempio

Di seguito è riportato un esempio dell'uso di una dichiarazione di vertice per associare i dati della posizione dei vertici 2D per registrare v0.

La dichiarazione del vertice appartiene all'applicazione:


```
D3DVERTEXELEMENT9 decl[] =
{
    { 0, 0, D3DDECLTYPE_FLOAT2, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_POSITION, 0 },
      D3DDECL_END()
};
```



Ecco la dichiarazione di vertex shader corrispondente:


```
dcl_position v0
```





| Versioni vertex shader | 1\_1 | 2 \_ 0 | 2 \_ sw | 2 \_ x | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|-------|------|------|-------|
| Registro delle posizioni      | x    | x    | x     | x    | x    | x     |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registri vertex shader](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




