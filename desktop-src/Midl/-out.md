---
title: /out (opzione)
description: L'opzione /out specifica la directory predefinita in cui il compilatore MIDL scrive i file di output.
ms.assetid: 37cfe989-137a-4336-8c66-e6b9c23473df
keywords:
- Opzione /out MIDL
topic_type:
- apiref
api_name:
- /out
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b29c97438c0db1a60d94a8ae88ed99f73c33ea16a820d1aec5ca7a6be737e5d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014099"
---
# <a name="out-switch"></a>/out (opzione)

**L'opzione /out** specifica la directory predefinita in cui il compilatore MIDL scrive i file di output.

``` syntax
midl /out path-specification
```

## <a name="switch-options"></a>Opzioni di cambio

<dl> <dt>

*specifica del percorso* 
</dt> <dd>

Specifica il percorso della directory in cui vengono generati i file stub, header e switch. È possibile specificare una specifica di unità, un percorso di directory assoluto o entrambi. I percorsi possono essere racchiusi in modo esplicito tra virgolette doppie (") per impedire alla shell di interpretare i caratteri speciali.

</dd> </dl>

## <a name="remarks"></a>Commenti

La directory di output può essere specificata con una lettera di unità, un nome di percorso assoluto o entrambi. **L'opzione /out** può essere usata con qualsiasi opzione che abilita la specifica del singolo file di output.

Quando **l'opzione /out** non è specificata, i file vengono scritti nella directory corrente.

La directory predefinita specificata dall'opzione **/out** può essere sostituita da un nome di percorso esplicito specificato come parte dell'opzione [**/cstub**](-cstub.md), [**/header**](-header.md), [**/proxy**](-proxy.md)o [**/sstub.**](-sstub.md)

## <a name="examples"></a>Esempio

**midl /out c: \\ mydir \\ mysubdir \\ subdir2 deeper filename.idl**

**midl /out c: filename.idl**

**midl /out \\ mydir \\ mysubdir \\ altro nomefile.idl**

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Sintassi della riga di comando MIDL generale](general-midl-command-line-syntax.md)
</dt> <dt>

[**/cstub**](-cstub.md)
</dt> <dt>

[**/header**](-header.md)
</dt> <dt>

[**/proxy**](-proxy.md)
</dt> <dt>

[**/sstub**](-sstub.md)
</dt> </dl>

 

 




