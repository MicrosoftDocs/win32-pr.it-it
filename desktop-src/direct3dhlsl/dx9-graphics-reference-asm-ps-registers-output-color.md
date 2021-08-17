---
title: Output Color Register
description: I pixel shader di output dei colori (oC\ ) sono registri di sola scrittura che re come output dei risultati in più destinazioni di rendering.
ms.assetid: 88e69189-3956-47de-a336-921f1e62c025
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 038446bb7d588222e04028727a447b6a47c941ab6a18a3ba4216f46e93440961
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119705"
---
# <a name="output-color-register"></a>Output Color Register

I pixel shader di output dei colori (oC#) sono registri di sola scrittura che reseguono l'output dei risultati in più destinazioni di rendering.

Sintassi



| Oc # |
|------|



 

Dove:



| Nome | Descrizione       |
|------|-------------------|
| oC0  | destinazione di \# rendering 0 |
| oC1  | destinazione di \# rendering 1 |
| oC2  | destinazione di rendering \# 2 |
| oC3  | destinazione di rendering \# 3 |



 

## <a name="remarks"></a>Commenti

-   Se oCn viene scritto ma non esiste una destinazione di rendering corrispondente, la scrittura in oCn viene ignorata.
-   Gli stati di rendering D3DRS \_ COLORWRITEENABLE, D3DRS \_ COLORWRITEENABLE1, D3DRS \_ COLORWRITEENABLE2 e D3DRS COLORWRITEENABLE3 determinano quali componenti di oCn vengono infine scritti nella destinazione di rendering (dopo la \_ fusione, se applicabile). Se lo shader scrive alcuni ma non tutti i componenti definiti dagli stati di rendering COLORWRITEENABLE di D3DRS per un registro \_ oCn specificato, i canali non scritti producono valori non definiti nella destinazione di rendering \* corrispondente. Se non viene scritto nessuno dei componenti di un oCn, la destinazione di rendering corrispondente non deve essere aggiornata (come indicato in precedenza), quindi gli stati di rendering D3DRS COLORWRITEENABLE non sono \_ \* applicabili.

### <a name="shader-model-2-restrictions"></a>Restrizioni del modello shader 2

-   oCn può essere scritto solo con [l'istruzione mov - ps.](mov---ps.md)
-   OC0 deve essere sempre scritto nello shader.
-   Non è consentito alcun swizzle di origine (ad eccezione di .xyzw = swizzle predefinito) o modificatore di origine durante la scrittura in qualsiasi oCn.
-   Non è consentita alcuna maschera di scrittura di destinazione (ad eccezione di .xyzw = maschera predefinita) o modificatore di istruzione durante la scrittura in qualsiasi oCn.
-   Se oCn viene scritto, deve essere scritto anche oC0 - oCn-1. Ad esempio, per scrivere in oC2, è necessario scrivere anche in oC0 e oC1.
-   È consentita al massimo una scrittura in qualsiasi oC# per shader.
-   Per ps 2 x e \_ ps 3 0, non è possibile scrivere nei registri oC# e oD all'interno del controllo di flusso dinamico o del predicato (le scritture in \_ \_ \_ oC# all'interno del controllo di flusso statico sono \# a posto).

### <a name="shader-model-3-restrictions"></a>Restrizioni del modello di shader 3

-   Per ps \_ 3 \_ 0, i registri di output oC# e oD \# possono essere scritti un numero qualsiasi di volte. L'output del pixel shader deriva dal contenuto dei registri di output alla fine dell'esecuzione dello shader. Se non si verifica una scrittura in un registro di output, ad esempio a causa del controllo di flusso o se lo shader non lo ha appena scritto, anche la destinazione di rendering corrispondente non viene aggiornata. Se viene scritto un subset dei canali in un registro di output, i valori non definiti verranno scritti nei canali rimanenti.
-   Per ps \_ 3 \_ 0, i registri oC# possono essere scritti con qualsiasi maschera di scrittura.
-   Per ps 2 x e \_ ps 3 0, non è possibile scrivere nei registri oC# e oD all'interno del controllo di flusso dinamico o del predicato (le scritture in \_ \_ \_ oC# all'interno del controllo di flusso statico sono \# a posto).
-   Non è possibile eseguire calcoli delle sfumature (o operazioni che richiamano in modo implicito i calcoli delle sfumature, ad esempio [texld - ps \_ 2 \_ 0](texld---ps-2-0.md)e up , [texldb - ps](texldb---ps.md), [texldp - ps](texldp---ps.md)) all'interno di istruzioni di controllo di flusso le cui condizioni di diramazione variano in base alle primitive (ad esempio, istruzioni di controllo dinamico del flusso). Il predicato dell'istruzione non è considerato controllo dinamico del flusso.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registri](dx9-graphics-reference-asm-ps-registers.md)
</dt> <dt>

[Più destinazioni di rendering (Direct3D 9)](/windows/desktop/direct3d9/multiple-render-targets)
</dt> </dl>

 

 