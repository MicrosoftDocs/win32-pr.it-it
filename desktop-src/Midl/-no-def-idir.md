---
title: /no_def_idir opzione
description: Quando si specificano le directory con l'opzione/I, \_ l' \_ opzione/No def Idir indica al compilatore MIDL di eseguire la ricerca solo nelle directory specificate con l'opzione/i.
ms.assetid: 9a396de4-332d-4832-8e8b-291690cd3a10
keywords:
- /no_def_idir switch MIDL
topic_type:
- apiref
api_name:
- /no_def_idir
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62ed845c73c36fbbfe4ea7dea952ee4541b043a7
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103857585"
---
# <a name="no_def_idir-switch"></a>/No \_ def \_ Idir switch

Quando si specificano le directory con l'opzione [**/i**](-i.md) , l'opzione **/No \_ def \_ Idir** indica al compilatore MIDL di eseguire la ricerca solo nelle directory specificate con l'opzione **/i** , ignorando la directory corrente e le directory specificate dalla variabile di ambiente include.

``` syntax
midl /no_def_idir
```

## <a name="switch-options"></a>Opzioni switch

Questa opzione non ha parametri.

## <a name="remarks"></a>Commenti

Quando non viene specificata alcuna directory con l'opzione [**/i**](-i.md) , l'opzione **/No \_ def \_ Idir** indica al compilatore MIDL di eseguire la ricerca solo nella directory corrente.

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

[**/I**](-i.md)
</dt> </dl>

 

 




