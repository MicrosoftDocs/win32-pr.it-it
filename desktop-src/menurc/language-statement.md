---
title: Istruzione LANGUAGE
description: Definisce la lingua per tutte le risorse fino all'istruzione LANGUAGE successiva o alla fine del file.
ms.assetid: 175e27e2-903a-4aaf-89ef-532166b167e8
keywords:
- Menu e altre risorse dell'istruzione LANGUAGE
topic_type:
- apiref
api_name:
- LANGUAGE
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b40971044f12897cd9c797fc2a2c44b0f34f81f4e1323e9689ea70905cac76da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117687466"
---
# <a name="language-statement"></a>Istruzione LANGUAGE

Definisce la lingua per tutte le risorse fino all'istruzione **LANGUAGE** successiva o alla fine del file.

Quando **l'istruzione LANGUAGE** viene visualizzata prima dell'inizio del corpo di una definizione di risorsa [**ACCELERATORS**](accelerators-resource.md), [**DIALOGEX**](dialogex-resource.md), [**MENU**](menu-resource.md), [**RCDATA**](rcdata-resource.md)o [**STRINGTABLE,**](stringtable-resource.md) la lingua specificata si applica solo a tale risorsa.

``` syntax
LANGUAGE language, sublanguage
```

<dl> <dt>

<span id="language"></span><span id="LANGUAGE"></span>*Lingua*
</dt> <dd>

Identificatore di lingua.

</dd> <dt>

<span id="sublanguage"></span><span id="SUBLANGUAGE"></span>*sottolinguaggio*
</dt> <dd>

Identificatore del sottolinguaggio.

</dd> </dl>

Per altre informazioni, vedere [Costanti e stringhe degli identificatori di linguaggio](/windows/desktop/Intl/language-identifier-constants-and-strings).

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Acceleratori**](accelerators-resource.md)
</dt> <dt>

[**Caratteristiche**](characteristics-statement.md)
</dt> <dt>

[**Menu**](menu-resource.md)
</dt> <dt>

[**RCDATA**](rcdata-resource.md)
</dt> <dt>

[**Stringtable**](stringtable-resource.md)
</dt> <dt>

[**Versione**](version-statement.md)
</dt> </dl>

 

 