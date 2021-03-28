---
title: Registro colori di output
description: I registri di output del colore pixel shader (oC \) sono registri di sola scrittura che restituiscono risultati a più destinazioni di rendering.
ms.assetid: 88e69189-3956-47de-a336-921f1e62c025
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 316160e39ce172d56e4ecac17dfbd1d53077005b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399520"
---
# <a name="output-color-register"></a>Registro colori di output

I registri di output del colore di pixel shader (oC #) sono registri di sola scrittura che restituiscono risultati a più destinazioni di rendering.

Sintassi



| oC # |
|------|



 

Dove:



| Nome | Descrizione       |
|------|-------------------|
| oC0  | destinazione di rendering \# 0 |
| oC1  | destinazione di rendering \# 1 |
| oC2  | destinazione di rendering \# 2 |
| oC3  | destinazione di rendering \# 3 |



 

## <a name="remarks"></a>Commenti

-   Se oCn è scritto ma non esiste alcuna destinazione di rendering corrispondente, la scrittura in oCn viene ignorata.
-   Gli Stati di rendering D3DRS \_ COLORWRITEENABLE, D3DRS \_ COLORWRITEENABLE1, D3DRS \_ COLORWRITEENABLE2 e D3DRS COLORWRITEENABLE3 \_ determinano i componenti di oCn che vengono infine scritti nella destinazione di rendering (dopo Blend, se applicabile). Se lo shader scrive alcuni ma non tutti i componenti definiti dagli \_ Stati di rendering COLORWRITEENABLE di D3DRS \* per un registro oCn specificato, i canali non scritti producono valori non definiti nella destinazione di rendering corrispondente. Se non viene scritto alcun componente di un oCn, la destinazione di rendering corrispondente non deve essere aggiornata (come indicato in precedenza), quindi gli Stati di \_ rendering D3DRS COLORWRITEENABLE non \* si applicano.

### <a name="shader-model-2-restrictions"></a>Restrizioni del modello di shader 2

-   oCn può essere scritto solo con l'istruzione [MOV-PS](mov---ps.md) .
-   oC0 deve essere sempre scritto nello shader.
-   Non sono consentiti swizzle di origine (eccetto. xyzw = default swizzle) o modificatore di origine durante la scrittura in qualsiasi oCn.
-   Non sono consentite maschere di scrittura di destinazione (eccetto. xyzw = default mask) o il modificatore di istruzione durante la scrittura in qualsiasi oCn.
-   Se viene scritto oCn, è necessario scrivere anche oC0-oCn-1. Ad esempio, per scrivere in oC2, è necessario scrivere anche in oC0 e oC1.
-   È consentita al massimo una scrittura in qualsiasi numero oC per shader.
-   Per PS \_ 2 \_ x e PS \_ 3 \_ 0, non è possibile scrivere nei registri OC # e od, \# all'interno del controllo di flusso dinamico o predicazione (le Scritture in OC # all'interno del controllo di flusso statico sono belle).

### <a name="shader-model-3-restrictions"></a>Restrizioni del modello di shader 3

-   Per PS \_ 3 \_ 0, i registri di output OC # e od \# possono essere scritti un numero qualsiasi di volte. L'output del pixel shader deriva dal contenuto dei registri di output alla fine dell'esecuzione dello shader. Se non si verifica una scrittura in un registro di output, probabilmente a causa del controllo di flusso o se lo shader non lo scrive, anche il renderTarget corrispondente non viene aggiornato. Se viene scritto un subset dei canali in un registro di output, i valori non definiti verranno scritti nei canali rimanenti.
-   Per PS \_ 3 \_ 0, i registri di OC # possono essere scritti con qualsiasi writemasks.
-   Per PS \_ 2 \_ x e PS \_ 3 \_ 0, non è possibile scrivere nei registri OC # e od, \# all'interno del controllo di flusso dinamico o predicazione (le Scritture in OC # all'interno del controllo di flusso statico sono belle).
-   Non è possibile eseguire alcun calcolo sfumato (o operazioni che richiamano in modo implicito i calcoli delle sfumature, ad esempio [texld-PS \_ 2 \_ 0 e up](texld---ps-2-0.md), [texldb-PS](texldb---ps.md), [texldp-PS](texldp---ps.md)) all'interno delle istruzioni di controllo di flusso le cui condizioni di diramazione variano in base alle primitive (ad esempio, istruzioni di controllo dinamico del flusso). L'istruzione predicazione non è considerata il controllo dinamico del flusso.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registri](dx9-graphics-reference-asm-ps-registers.md)
</dt> <dt>

[Più destinazioni di rendering (Direct3D 9)](/windows/desktop/direct3d9/multiple-render-targets)
</dt> </dl>

 

 