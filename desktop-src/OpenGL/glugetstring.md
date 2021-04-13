---
title: funzione gluGetString (Glu. h)
description: La funzione gluGetString ottiene una stringa che descrive il numero di versione di GLU o le chiamate all'estensione GLU supportate.
ms.assetid: e6d9ce03-3218-4145-8bb5-3989afe62436
keywords:
- funzione gluGetString OpenGL
topic_type:
- apiref
api_name:
- gluGetString
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 574ed93c9c6f8d1f964e38ee14541d57bd5c34da
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400525"
---
# <a name="glugetstring-function"></a>gluGetString (funzione)

La funzione **GluGetString** ottiene una stringa che descrive il numero di versione di Glu o le chiamate all'estensione Glu supportate.

## <a name="syntax"></a>Sintassi


```C++
const GLubyte* WINAPI gluGetString(
   GLenum name
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*nome* 
</dt> <dd>

Il numero di versione di GLU (GLU \_ Version) o delle chiamate di estensione specifiche del fornitore disponibili (Glu \_ Extensions).

</dd> </dl>

## <a name="remarks"></a>Commenti

La funzione **GluGetString** restituisce un puntatore a una stringa statica con terminazione null. Quando *Name* è la \_ versione Glu, la stringa restituita è un valore che rappresenta il numero di versione di Glu. Il formato del numero di versione è il seguente:

``` syntax
<version number><space><vendor-specific information> 
(for example, "1.2.11 Microsoft Windows")
```

Il numero di versione ha il formato "numero principale \_ . \_ numero secondario" o "numero principale. numero \_ secondario \_ . \_ numero versione". Le informazioni specifiche del fornitore sono facoltative e il formato e il contenuto dipendono dall'implementazione di.

Quando *Name* è \_ il nome dell'estensione Glu, la stringa restituita contiene un elenco di nomi di estensioni Glu supportate separate da spazi. Il formato dell'elenco di nomi restituito è il seguente:

``` syntax
<extension_name><space><extension_name><space> . . .
(for example, "GLU_NURBS GL_TESSELATION")
```

I nomi di estensione non possono contenere spazi.

La funzione **GluGetString** è valida per GLU versione 1,1 o successiva.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Glu. h</dt> </dl>     |
| Libreria<br/>                  | <dl> <dt>Glu32. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Glu32.dll</dt> </dl> |



 

 





