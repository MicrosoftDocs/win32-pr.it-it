---
description: Uniscribe usa più motori di shaping che contengono la conoscenza del layout per determinati script.
ms.assetid: 3cdd18f3-51d3-4d1c-be31-f5709074cbe7
title: Uso di shaping Engine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a106e993aba515af38edd2b809ef60454a186cde
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319470"
---
# <a name="using-shaping-engines"></a>Uso di shaping Engine

Uniscribe usa più motori di shaping che contengono la conoscenza del layout per determinati script. Sfrutta inoltre il motore di shaping del layout OpenType per la gestione di funzionalità di script specifiche del tipo di carattere, come la generazione di glifi, la misurazione dell'extent e il supporto per l'interruzione delle parole. Uniscribe gestisce il riordinamento dei caratteri bidirezionali usando l'algoritmo bidirezionale Unicode e riconosce i formati dei tipi di carattere del layout non OpenType per il data shaping arabo, ebraico e tailandese.

Poiché l'esatto intervallo di punti di codice assegnato a ogni motore di shaping può variare, i numeri di script non vengono pubblicati, ad eccezione dello SCRIPT non \_ definito. Tuttavia, l'applicazione può testare gli attributi degli script chiamando la funzione [**ScriptGetProperties**](/windows/desktop/api/Usp10/nf-usp10-scriptgetproperties) , che accede alla tabella delle proprietà dello script globale. L'applicazione può usare le proprietà dello script globale per combinare le proprie regole di layout con le divisioni del motore di data shaping richieste.

L'applicazione accede a un motore di shaping con una chiamata alla funzione [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) . Tutti i motori di creazione di script complessi, i motori per la definizione delle cifre e i motori di shaping ASCII convalidano il tipo di carattere indicato nell'handle del contesto di dispositivo prima del data shaping. Per essere leggibili, gli script complessi devono essere modellati utilizzando lo script restituito dalla funzione [**ScriptItemize**](/windows/desktop/api/Usp10/nf-usp10-scriptitemize) . Le altre esecuzioni restano leggibili se deformate con uno SCRIPT \_ non definito nel membro **escript** della struttura di [**\_ analisi dello script**](/windows/win32/api/usp10/ns-usp10-script_analysis) , anche se potrebbero perdere la qualità tipografica.

[**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) restituisce 0 se ha esito positivo \_ oppure \_ lo script USP E \_ non è \_ in \_ un tipo di carattere se il tipo di carattere fornito dall'applicazione non contiene glifi o tabelle di shaping sufficienti. Se l'applicazione specifica uno SCRIPT \_ non definito e alcuni caratteri non sono supportati dal tipo di carattere, la funzione ha ancora esito positivo. In questo caso, l'applicazione deve analizzare il buffer di output del glifo per la presenza di glifi mancanti. Per le strategie di gestione dei glifi mancanti, vedere [uso del fallback dei tipi di carattere](using-font-fallback.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di Uniscribe](using-uniscribe.md)
</dt> </dl>

 

 



