---
description: Definisce alcuni o tutti gli attributi carattere, glifi, larghezze di avanzamento, posizioni x e y, mapping da carattere a glifo e così via, per una stringa.
ms.assetid: aa93d631-3cfc-449d-9d04-c1f851129c6c
title: SCRIPT_STRING_ANALYSIS (Usp10.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9481c641f182015d7a318c21c490f45fcc934e0df1baa52483707628eb4daa1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118390300"
---
# <a name="script_string_analysis"></a>ANALISI \_ DELLE STRINGHE DI \_ SCRIPT

Definisce alcuni o tutti gli attributi carattere, glifi, larghezze di avanzamento, posizioni x e y, mapping da carattere a glifo e così via, per una stringa.


```C++
typedef void* SCRIPT_STRING_ANALYSIS;
```



## <a name="remarks"></a>Commenti

Si tratta di una struttura opaca allocata dinamicamente e recuperata da [**ScriptStringAnalyse**](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse). È necessario anche per tutte **le altre funzioni ScriptString. \***

Poiché l'analisi può essere di grandi dimensioni, è importante che l'applicazione chiami [**ScriptStringFree**](/windows/desktop/api/Usp10/nf-usp10-scriptstringfree) non appena ha completato la stringa.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                         |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                               |
| Componente ridistribuibile<br/>          | Internet Explorer 5 o versioni successive inWindows Me/98/95<br/>                         |
| Intestazione<br/>                   | <dl> <dt>Usp10.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Uniscribe](uniscribe.md)
</dt> <dt>

[Uniscribe Structures](uniscribe-structures.md)
</dt> <dt>

[**ScriptStringAnalyse**](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse)
</dt> <dt>

[**ScriptStringFree**](script-string-analysis.md)
</dt> </dl>

 

 




