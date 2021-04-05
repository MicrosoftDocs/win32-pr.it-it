---
title: pointer_default (attributo)
description: L'attributo \ Pointer \_ default \ specifica l'attributo puntatore predefinito per tutti i puntatori eccetto i puntatori di primo livello visualizzati negli elenchi di parametri.
ms.assetid: a6e83034-8adb-483d-8d1e-432a1aed22c6
keywords:
- attributo pointer_default MIDL
topic_type:
- apiref
api_name:
- pointer_default
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08555358eb0abd42957d60527e18a4fd4f49165a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104046598"
---
# <a name="pointer_default-attribute"></a>\_attributo predefinito puntatore

L'attributo **\[ \_ default \] del puntatore** specifica l'attributo del puntatore predefinito per tutti i puntatori ad eccezione dei puntatori di primo livello visualizzati negli elenchi di parametri.

``` syntax
pointer_default ( ptr | ref | unique )
```

## <a name="parameters"></a>Parametri

Questo attributo non ha parametri.

## <a name="examples"></a>Esempi

``` syntax
[
    uuid(6B29FC40-CA47-1067-B31D-00DD010662DA), 
    version(3.3), 
    pointer_default(unique)
] 
interface dictionary 
{
    // Interface definition statements.
}
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[**interfaccia**](interface.md)
</dt> <dt>

[Attributi array e Sized-Pointer](array-and-sized-pointer-attributes.md)
</dt> <dt>

[**matrici**](arrays-1.md)
</dt> <dt>

[Matrici e puntatori](/windows/desktop/Rpc/arrays-and-pointers)
</dt> <dt>

[**ptr**](ptr.md)
</dt> <dt>

[**ref**](ref.md)
</dt> <dt>

[**unico**](unique.md)
</dt> <dt>

[Tipi di puntatore predefiniti](/windows/desktop/Rpc/default-pointer-types)
</dt> </dl>

 

 