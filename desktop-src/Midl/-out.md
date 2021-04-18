---
title: /out (opzione)
description: L'opzione/out specifica la directory predefinita in cui il compilatore MIDL scrive i file di output.
ms.assetid: 37cfe989-137a-4336-8c66-e6b9c23473df
keywords:
- opzione/out MIDL
topic_type:
- apiref
api_name:
- /out
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d688f17957170c6f3a8887030ea2c67140c0ff8c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "106299185"
---
# <a name="out-switch"></a>/out (opzione)

L'opzione **/out** specifica la directory predefinita in cui il compilatore MIDL scrive i file di output.

``` syntax
midl /out path-specification
```

## <a name="switch-options"></a>Opzioni switch

<dl> <dt>

*Specifica percorso* 
</dt> <dd>

Specifica il percorso della directory in cui vengono generati lo stub, l'intestazione e i file di commutazione. È possibile specificare una specifica di unità, un percorso di directory assoluto o entrambi. I percorsi possono essere racchiusi tra virgolette doppie (") per impedire alla shell di interpretare i caratteri speciali.

</dd> </dl>

## <a name="remarks"></a>Commenti

La directory di output può essere specificata con una lettera di unità, un nome di percorso assoluto o entrambi. È possibile utilizzare l'opzione **/out** con una qualsiasi delle opzioni che consentono la specifica del singolo file di output.

Se non si specifica l'opzione **/out** , i file vengono scritti nella directory corrente.

La directory predefinita specificata dall'opzione **/out** può essere sostituita da un nome di percorso esplicito specificato come parte dell'opzione [**/cstub**](-cstub.md), [**/header**](-header.md), [**/proxy**](-proxy.md)o [**/sstub**](-sstub.md) .

## <a name="examples"></a>Esempio

**MIDL/out c: \\ mydir \\ mysubdir \\ SubDir2 più profondo nomefile. idl**

**MIDL/out c: filename. idl**

**MIDL/out \\ mydir \\ mysubdir \\ un altro nomefile. idl**

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

 

 




