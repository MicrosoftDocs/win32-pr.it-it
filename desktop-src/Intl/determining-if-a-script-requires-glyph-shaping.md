---
description: Nell'esempio seguente viene chiamato ScriptGetProperties per verificare se lo script di ognuno dei vari elementi successivi richiede la definizione di un glifo.
ms.assetid: 75c5946b-de38-48d9-a5e2-1e0b2dc9f3c7
title: Determinare se uno script richiede la definizione del glifo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62eb20fb0335c5779352f15221653dad0c5320c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233312"
---
# <a name="determining-if-a-script-requires-glyph-shaping"></a>Determinare se uno script richiede la definizione del glifo

Nell'esempio seguente viene chiamato [**ScriptGetProperties**](/windows/desktop/api/Usp10/nf-usp10-scriptgetproperties) per verificare se lo script di ognuno dei vari [elementi](uniscribe-glossary.md) successivi richiede la definizione di un glifo.


```C++
const SCRIPT_PROPERTIES **g_ppScriptProperties;
int g_iMaxScript;

WCHAR *pwcInChars = L"Unicode string to itemize";
int cInChars = wcslen(pwcInChars);
const int cMaxItems = 20;
SCRIPT_ITEM si[cMaxItems + 1];
SCRIPT_ITEM *pItems = si;
int cItems;

ScriptGetProperties(&g_ppScriptProperties,
                    &g_iMaxScript);

HRESULT hResult = ScriptItemize(pwcInChars,
                                cInChars,
                                cMaxItems,
                                NULL,
                                NULL,
                                pItems,
                                &cItems);
if (hResult == 0) {
    for (int i=0; i<cItems; i++) {
        if (g_ppScriptProperties[pItems[i].a.eScript]->fComplex) {

            // Item [i] is complex script text
            // requiring glyph shaping.

        } else {

            // The text may be rendered legibly without using Uniscribe. 
            // However, Uniscribe may still be used as a means of accessing 
            // font typographic features. 
        }
    }
} else {
    // Handle the error.
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di Uniscribe](using-uniscribe.md)
</dt> </dl>

 

 



