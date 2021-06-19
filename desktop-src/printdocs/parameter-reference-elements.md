---
description: Leggere gli elementi ParameterRef in Print Schema Framework. Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica dello schema di stampa.
ms.assetid: 78df6acf-eb4e-46c1-bf1d-c0a99cf49bff
title: Elementi ParameterRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2935317bc4107e2071911ab1df826426b2bcec17
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396526"
---
# <a name="parameterref-elements"></a>Elementi ParameterRef

Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Gli elementi ParameterRef si applicano in modo specifico agli elementi Option, consentendo a tale elemento Option di fare riferimento a un particolare elemento ParameterDef. Per questi elementi Option, un elemento ScoredProperty che caratterizza l'opzione non è hard-coded nel documento PrintCapabilities come valore, ma è variabile. Per abilitare questa variabilità, questi elementi ScoredProperty contengono un elemento ParameterRef. Un elemento ScoredProperty non può contenere sia un elemento Value che un elemento ParameterRef. Gli elementi opzione contenenti uno o più elementi ParameterRef sono denominati elementi Option con parametri.

Print Schema Framework consente a un elemento Option di contenere un numero qualsiasi di elementi ScoredProperty che fanno riferimento agli elementi Parameter, insieme a qualsiasi numero di elementi ScoredProperty che contengono elementi Value. Framework consente anche a qualsiasi numero di elementi Feature di contenere elementi Option con parametri e a ogni elemento Feature è consentito un numero qualsiasi di elementi Option con parametri. Inoltre, lo stesso costrutto di parametro può essere indicato da diversi elementi Option, elementi Option che possono appartenere allo stesso elemento Feature o a elementi Feature diversi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



