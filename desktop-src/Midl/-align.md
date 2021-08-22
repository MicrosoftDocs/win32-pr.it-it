---
title: Opzione /align
description: Dal punto di vista funzionale, l'opzione /align è uguale all'opzione MIDL /Zp ed è riconosciuta dal compilatore MIDL esclusivamente per la compatibilità con le versioni precedenti di MkTypLib.
ms.assetid: 7f303c49-a6b5-4e3c-95e5-5c49e338c766
keywords:
- Opzione /align MIDL
topic_type:
- apiref
api_name:
- /align
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 187607b783678d3045224daec021eabf436fa8ba1884128789f44b06ac4365ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067651"
---
# <a name="align-switch"></a>Opzione /align

Dal punto di vista funzionale, l'opzione **/align** è uguale all'opzione MIDL [**/Zp**](-zp.md) ed è riconosciuta dal compilatore MIDL esclusivamente per la compatibilità con le versioni precedenti di MkTypLib.

> [!Note]  
> Lo Mktyplib.exe è obsoleto. In alternativa, usare il compilatore MIDL.

 

``` syntax
midl /align:alignment
```

## <a name="switch-options"></a>Opzioni switch

<dl> <dt>

*Allineamento* 
</dt> <dd>

Specifica l'allineamento per i tipi nella libreria. Il *valore* di allineamento può essere 1, 2, 4 o 8. Il valore 1 indica l'allineamento naturale. *n* indica l'allineamento sul byte *n*. Quando non si specifica **l'opzione /align,** il valore predefinito è 8.

</dd> </dl>

## <a name="remarks"></a>Commenti

Se si sta generando un nuovo makefile, usare [**l'opzione /Zp.**](-zp.md)

Il valore di allineamento corrisponde al [**valore dell'opzione /Zp**](-zp.md) usato dal compilatore Microsoft C/C++. Assicurarsi di specificare lo stesso allineamento quando si richiama il compilatore C come quando si richiama il compilatore MIDL.

Per altre informazioni, vedere la documentazione sulla programmazione microsoft C/C++. Per una descrizione dei potenziali rischi per l'uso di livelli di packing non standard, vedere l'argomento della Guida [**/Zp.**](-zp.md)

## <a name="examples"></a>Esempio

**midl /align:4 filename.idl**

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Sintassi generale della riga di comando MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/Zp**](-zp.md)
</dt> </dl>

 

 




