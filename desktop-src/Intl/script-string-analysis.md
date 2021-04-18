---
description: Definisce alcuni o tutti gli attributi carattere, i glifi, le larghezze di avanzamento, le posizioni x e y, i mapping da carattere a glifo e così via per una stringa.
ms.assetid: aa93d631-3cfc-449d-9d04-c1f851129c6c
title: SCRIPT_STRING_ANALYSIS (usp10. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ef9bf7e2a3a592a279b593d986220350a3d8f72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317141"
---
# <a name="script_string_analysis"></a>\_analisi della stringa di script \_

Definisce alcuni o tutti gli attributi carattere, i glifi, le larghezze di avanzamento, le posizioni x e y, i mapping da carattere a glifo e così via per una stringa.


```C++
typedef void* SCRIPT_STRING_ANALYSIS;
```



## <a name="remarks"></a>Commenti

Si tratta di una struttura opaca allocata in modo dinamico e recuperata da [**ScriptStringAnalyse**](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse). È obbligatorio anche per tutte le altre funzioni **scriptString \** _.

Poiché l'analisi può essere di grandi dimensioni, è importante che l'applicazione chiami [_ *ScriptStringFree* *](/windows/desktop/api/Usp10/nf-usp10-scriptstringfree) non appena termina con la stringa.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                         |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                               |
| Componente ridistribuibile<br/>          | Internet Explorer 5 o versioni successive onWindows me/98/95<br/>                         |
| Intestazione<br/>                   | <dl> <dt>Usp10. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Uniscribe](uniscribe.md)
</dt> <dt>

[Strutture Uniscribe](uniscribe-structures.md)
</dt> <dt>

[**ScriptStringAnalyse**](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse)
</dt> <dt>

[**ScriptStringFree**](script-string-analysis.md)
</dt> </dl>

 

 




