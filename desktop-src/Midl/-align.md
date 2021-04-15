---
title: opzione/align
description: L'opzione/align è funzionalmente identica all'opzione MIDL/ZP ed è riconosciuta dal compilatore MIDL esclusivamente per la compatibilità con le versioni precedenti di MkTypLib.
ms.assetid: 7f303c49-a6b5-4e3c-95e5-5c49e338c766
keywords:
- /align switch MIDL
topic_type:
- apiref
api_name:
- /align
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 019a06be10a4937127d98d508275b57dfe508399
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104516336"
---
# <a name="align-switch"></a>opzione/align

L'opzione **/align** è funzionalmente identica all'opzione MIDL [**/ZP**](-zp.md) ed è riconosciuta dal compilatore MIDL esclusivamente per la compatibilità con le versioni precedenti di mktyplib.

> [!Note]  
> Lo strumento Mktyplib.exe è obsoleto. Usare invece il compilatore MIDL.

 

``` syntax
midl /align:alignment
```

## <a name="switch-options"></a>Opzioni switch

<dl> <dt>

*allineamento* 
</dt> <dd>

Specifica l'allineamento per i tipi nella libreria. Il valore di *allineamento* può essere 1, 2, 4 o 8. Il valore 1 indica l'allineamento naturale; *n* indica l'allineamento sul byte *n*. Quando non si specifica l'opzione **/align** , il valore predefinito è 8.

</dd> </dl>

## <a name="remarks"></a>Commenti

Se si sta generando un nuovo Makefile, usare l'opzione [**/ZP**](-zp.md) .

Il valore di allineamento corrisponde al valore dell'opzione [**/ZP**](-zp.md) usato dal compilatore Microsoft C/C++. Assicurarsi di specificare lo stesso allineamento quando si richiama il compilatore C come quando si richiama il compilatore MIDL.

Per ulteriori informazioni, vedere la documentazione sulla programmazione in Microsoft C/C++. Per una descrizione dei potenziali rischi correlati all'uso di livelli di compressione non standard, vedere l'argomento della Guida di [**/ZP**](-zp.md) .

## <a name="examples"></a>Esempio

**MIDL/align: 4 nomefile. idl**

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Sintassi della riga di comando MIDL generale](general-midl-command-line-syntax.md)
</dt> <dt>

[**/ZP**](-zp.md)
</dt> </dl>

 

 




