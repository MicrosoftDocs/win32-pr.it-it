---
title: Opzione /no_def_idir
description: Quando le directory vengono specificate con l'opzione /I, l'opzione /no def idir indica al compilatore MIDL di cercare solo le directory specificate con \_ \_ l'opzione /I.
ms.assetid: 9a396de4-332d-4832-8e8b-291690cd3a10
keywords:
- /no_def_idir l'opzione MIDL
topic_type:
- apiref
api_name:
- /no_def_idir
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c93d61bff28ad0aa4306047755c88419d0b925431f9b3ea476ec957dcd62b98
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119811301"
---
# <a name="no_def_idir-switch"></a>Opzione /no \_ def \_ idir

Quando le directory vengono specificate con l'opzione [**/I,**](-i.md) l'opzione **/no \_ def \_ idir** indica al compilatore MIDL di cercare solo le directory specificate con l'opzione **/I,** ignorando la directory corrente e le directory specificate dalla variabile di ambiente INCLUDE.

``` syntax
midl /no_def_idir
```

## <a name="switch-options"></a>Opzioni di cambio

Questa opzione non ha parametri.

## <a name="remarks"></a>Commenti

Quando non viene specificata alcuna directory con l'opzione [**/I,**](-i.md) l'opzione **/no \_ def \_ idir** indica al compilatore MIDL di cercare solo la directory corrente.

## <a name="examples"></a>Esempi

``` syntax
; search only the current directory 
midl /no_def_idir filename.idl  

; search only the specified directories 
midl /no_def_idir /I c:\c700\include filename.idl 
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[Sintassi della riga di comando MIDL generale](general-midl-command-line-syntax.md)
</dt> <dt>

[**/acf**](-acf.md)
</dt> <dt>

[**/i**](-i.md)
</dt> </dl>

 

 




