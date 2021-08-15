---
title: pointer_default (attributo)
description: L'attributo \ pointer default\ specifica l'attributo puntatore predefinito per tutti i puntatori ad eccezione dei puntatori di primo livello \_ visualizzati negli elenchi di parametri.
ms.assetid: a6e83034-8adb-483d-8d1e-432a1aed22c6
keywords:
- pointer_default attributo MIDL
topic_type:
- apiref
api_name:
- pointer_default
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d246da98db6d3f98aa8c64e1316ee56648016402d1070ae571284148b8caf390
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013769"
---
# <a name="pointer_default-attribute"></a>Attributo predefinito \_ del puntatore

**\[ L'attributo predefinito \_ del \]** puntatore specifica l'attributo puntatore predefinito per tutti i puntatori ad eccezione dei puntatori di primo livello visualizzati negli elenchi di parametri.

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

[**Interfaccia**](interface.md)
</dt> <dt>

[Attributi di matrice Sized-Pointer matrice](array-and-sized-pointer-attributes.md)
</dt> <dt>

[**Matrici**](arrays-1.md)
</dt> <dt>

[Matrici e puntatori](/windows/desktop/Rpc/arrays-and-pointers)
</dt> <dt>

[**ptr**](ptr.md)
</dt> <dt>

[**ref**](ref.md)
</dt> <dt>

[**Unico**](unique.md)
</dt> <dt>

[Tipi di puntatore predefiniti](/windows/desktop/Rpc/default-pointer-types)
</dt> </dl>

 

 