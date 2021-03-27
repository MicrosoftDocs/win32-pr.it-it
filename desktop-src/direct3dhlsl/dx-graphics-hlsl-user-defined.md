---
title: Tipo definito dall'utente
description: Utilizzare la sintassi seguente per dichiarare un tipo definito dall'utente.
ms.assetid: 8ef18864-f456-4b52-af83-f9b1050a0bba
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2107e3eb2b2dc2362776a1a9ecd50830519c6627
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395575"
---
# <a name="user-defined-type"></a>Tipo definito dall'utente

Utilizzare la sintassi seguente per dichiarare un tipo definito dall'utente.



|                                           |
|-------------------------------------------|
| **\[ \] \[ indice \] del nome di tipo const** di typedef; |



 

## <a name="parameters"></a>Parametri



| Elemento                                                                                         | Descrizione                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="_const_"></span><span id="_CONST_"></span>**\[const\]**<br/>                 | facoltativo. Questa parola chiave contrassegna in modo esplicito il tipo come costante.<br/>             |
| <span id="Type"></span><span id="type"></span><span id="TYPE"></span>**Tipo**<br/>     | Identifica il tipo di dati. deve essere uno dei tipi di dati intrinseci HLSL.<br/>     |
| <span id="Name"></span><span id="name"></span><span id="NAME"></span>**Nome**<br/>     | Stringa ASCII che identifica in modo univoco il nome della variabile.<br/>                 |
| <span id="Index"></span><span id="index"></span><span id="INDEX"></span>**Indice**<br/> | Dimensioni della matrice facoltative. Deve essere un Unsigned Integer compreso tra 1 e 4 inclusi.<br/> |



 

Oltre ai tipi di dati intrinseci incorporati, HLSL supporta i tipi definiti dall'utente o personalizzati che seguono questa sintassi:

## <a name="remarks"></a>Commenti

I tipi definiti dall'utente non fanno distinzione tra maiuscole e minuscole. Per praticità, i tipi seguenti vengono definiti automaticamente in ambito super-globale.


```
typedef vector <bool, #> bool#;
typedef vector <int, #> int#;
typedef vector <uint, #> uint#;
typedef vector <half, #> half#;
typedef vector <float, #> float#;
typedef vector <double, #> double#;

typedef matrix <bool, #, #> bool#x#;
typedef matrix <int, #, #> int#x#;
typedef matrix <uint, #, #> uint#x#;
typedef matrix <half, #, #> half#x#;
typedef matrix <float, #, #> float#x#;
typedef matrix <double, #, #> double#x#;
```



Il segno di cancelletto ( \# ) rappresenta una cifra intera compresa tra 1 e 4.

Per la compatibilità con gli effetti di DirectX 8, i tipi seguenti vengono definiti automaticamente in ambito super-globale:


```
typedef int DWORD;
typedef float FLOAT; 
typedef vector <float, 4> VECTOR;
typedef matrix <float, 4, 4> MATRIX;
typedef string STRING;
typedef texture TEXTURE;
typedef pixelshader PIXELSHADER;
typedef vertexshader VERTEXSHADER;
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tipi di dati (DirectX HLSL)](dx-graphics-hlsl-data-types.md)
</dt> </dl>

 

 





