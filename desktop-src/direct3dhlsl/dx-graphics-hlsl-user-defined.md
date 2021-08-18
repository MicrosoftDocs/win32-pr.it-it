---
title: Tipo definito dall'utente
description: Usare la sintassi seguente per dichiarare un tipo definito dall'utente.
ms.assetid: 8ef18864-f456-4b52-af83-f9b1050a0bba
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ee73cd5afcda15bcc821d7fea5b648924829d483a33b9c67c140eed0b100e861
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119789311"
---
# <a name="user-defined-type"></a>Tipo definito dall'utente

Usare la sintassi seguente per dichiarare un tipo definito dall'utente.



|                                           |
|-------------------------------------------|
| typedef **\[ const \] Type Name \[ Index \]**; |



 

## <a name="parameters"></a>Parametri



| Elemento                                                                                         | Descrizione                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="_const_"></span><span id="_CONST_"></span>**\[Const\]**<br/>                 | facoltativo. Questa parola chiave contrassegna in modo esplicito il tipo come costante.<br/>             |
| <span id="Type"></span><span id="type"></span><span id="TYPE"></span>**digitare**<br/>     | Identifica il tipo di dati. deve essere uno dei tipi di dati intrinseci HLSL.<br/>     |
| <span id="Name"></span><span id="name"></span><span id="NAME"></span>**Nome**<br/>     | Stringa ASCII che identifica in modo univoco il nome della variabile.<br/>                 |
| <span id="Index"></span><span id="index"></span><span id="INDEX"></span>**Indice**<br/> | Dimensioni facoltative della matrice. Deve essere un intero senza segno compreso tra 1 e 4 inclusi.<br/> |



 

Oltre ai tipi di dati intrinseci predefiniti, HLSL supporta tipi definiti dall'utente o personalizzati che seguono questa sintassi:

## <a name="remarks"></a>Commenti

Per i tipi definiti dall'utente non viene fatto distinzione tra maiuscole e minuscole. Per praticità, i tipi seguenti vengono definiti automaticamente nell'ambito super-globale.


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



Il cancelletto ( \# ) rappresenta una cifra intera compresa tra 1 e 4.

Per garantire la compatibilità con gli effetti directx 8, i tipi seguenti vengono definiti automaticamente nell'ambito super globale:


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

 

 





