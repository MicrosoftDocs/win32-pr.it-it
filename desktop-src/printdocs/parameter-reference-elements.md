---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: 78df6acf-eb4e-46c1-bf1d-c0a99cf49bff
title: Elementi ParameterRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30c0e145e99b1ee705d63449cf693c6fc87f6463
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "104058484"
---
# <a name="parameterref-elements"></a>Elementi ParameterRef

Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Gli elementi ParameterRef si applicano in modo specifico agli elementi option, consentendo a tale elemento option di fare riferimento a un particolare elemento ParameterDef. Per questi elementi di opzioni, un elemento ScoredProperty che caratterizza l'opzione non è hardcoded nel documento PrintCapabilities come valore, ma è invece una variabile. Per abilitare questa variabilità, questi elementi ScoredProperty contengono un elemento ParameterRef. Un elemento ScoredProperty non può contenere sia un elemento Value che un elemento ParameterRef. Gli elementi option che contengono uno o più elementi ParameterRef sono denominati elementi option con parametri.

Print Schema Framework consente a un elemento option di contenere un numero qualsiasi di elementi ScoredProperty che fanno riferimento a elementi Parameter, insieme a un numero qualsiasi di elementi ScoredProperty che contengono elementi di valore. Il Framework consente inoltre a qualsiasi numero di elementi di funzionalità di contenere elementi di opzioni con parametri e un numero qualsiasi di elementi di opzioni con parametri è consentito per ogni elemento Feature. Inoltre, è possibile fare riferimento allo stesso costrutto di parametro da più elementi option diversi, elementi option che possono appartenere allo stesso o a elementi di funzionalità diversi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



