---
title: LANGUAGE (istruzione)
description: Definisce la lingua per tutte le risorse fino alla successiva istruzione del linguaggio o alla fine del file.
ms.assetid: 175e27e2-903a-4aaf-89ef-532166b167e8
keywords:
- Menu di istruzioni della lingua e altre risorse
topic_type:
- apiref
api_name:
- LANGUAGE
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9563ba2ec00362a3b9caa3911a701919a81cae1e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104516780"
---
# <a name="language-statement"></a>LANGUAGE (istruzione)

Definisce la lingua per tutte le risorse fino alla successiva istruzione del **linguaggio** o alla fine del file.

Quando l'istruzione **Language** viene visualizzata prima dell'inizio del corpo di un [**acceleratore**](accelerators-resource.md), [**DIALOGEX**](dialogex-resource.md), [**menu**](menu-resource.md), [**RCDATA**](rcdata-resource.md)o [**un'STRINGTABLE**](stringtable-resource.md) , la lingua specificata si applica solo a tale risorsa.

``` syntax
LANGUAGE language, sublanguage
```

<dl> <dt>

<span id="language"></span><span id="LANGUAGE"></span>*linguaggio*
</dt> <dd>

Identificatore della lingua.

</dd> <dt>

<span id="sublanguage"></span><span id="SUBLANGUAGE"></span>*sottolingua*
</dt> <dd>

Identificatore del linguaggio di sottolinguaggio.

</dd> </dl>

Per altre informazioni, vedere [costanti e stringhe degli identificatori di lingua](/windows/desktop/Intl/language-identifier-constants-and-strings).

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ACCELERATORI**](accelerators-resource.md)
</dt> <dt>

[**CARATTERISTICHE**](characteristics-statement.md)
</dt> <dt>

[**MENU**](menu-resource.md)
</dt> <dt>

[**RCDATA**](rcdata-resource.md)
</dt> <dt>

[**UN'STRINGTABLE**](stringtable-resource.md)
</dt> <dt>

[**Versione**](version-statement.md)
</dt> </dl>

 

 