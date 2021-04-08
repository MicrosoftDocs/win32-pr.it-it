---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: 193dd600-7cbb-4f4e-bb7d-7f7117e9d16a
title: Sfondo dello schema di stampa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93280b6c8de62c76acdd59e2e596a0f600702451
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "103761566"
---
# <a name="print-schema-background"></a>Sfondo dello schema di stampa

Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Lo schema di stampa è concepito per risolvere i problemi di opacità e ambiguità associati alla comunicazione interna tra i componenti del sottosistema di stampa e la comunicazione esterna tra il sottosistema di stampa e le applicazioni.

L'interazione corrente del sottosistema di stampa con i plug-in applicazioni e fornitori di hardware usa la struttura DEVMODE binaria basata su indice e la DevCaps binaria. Le impostazioni apportate da ogni componente sono ampiamente opache per altri componenti, impedendo la portabilità delle impostazioni tra i dispositivi o persino tra diverse versioni del driver sullo stesso dispositivo. Inoltre, PrintCapabilities non può essere facilmente sfruttato dalle applicazioni client senza alcuna conoscenza proprietaria del dispositivo o mediante l'interfaccia utente del driver (UI). Oltre a queste limitazioni, in un senso più ampio non esiste alcun linguaggio ben definito per descrivere gli attributi generali del dispositivo, PrintCapabilities, le configurazioni dei dispositivi o la formattazione dei processi. Lo schema di stampa e le tecnologie correlate sono progettati per risolvere queste limitazioni, offrendo un metodo coerente, non ambiguo ed estendibile per la comunicazione di impostazioni e funzionalità in modo consolidato e logico.

I fondamenti concettuali delle parole chiave dello schema di stampa e del Framework dello schema di stampa sono la coerenza, la mancanza di ambiguità e l'estendibilità. La coerenza viene eseguita tramite l'utilizzo delle parole chiave dello schema di stampa e del Framework dello schema di stampa come blocchi predefiniti per la comunicazione tra i componenti di stampa di nuova generazione. Le applicazioni, il sottosistema di stampa di Microsoft Windows e i plug-in e i driver IHV interagiscono con questo meccanismo comune. Queste parole chiave, la loro struttura e il loro significato saranno ben definite dallo schema pubblico. Ciò impedisce l'ambiguità nel significato di una parola chiave specifica e impedisce le parole chiave ridondanti o duplicate. Tutti i componenti possono basarsi sull'uso di una particolare parola chiave per fornire un determinato scopo e far sì che tale finalità venga riconosciuta dal destinatario. L'estendibilità è essenziale per la longevità delle parole chiave dello schema di stampa, assicurando che lo schema pubblico sia un'entità dinamica. La struttura consente anche le estensioni private, che garantiscono a IHV la flessibilità di innovazione desiderata, tenendo presente che l'inclusione futura di una parola chiave privata nello schema pubblico è essenziale per mantenere la coerenza e impedire l'ambiguità.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



