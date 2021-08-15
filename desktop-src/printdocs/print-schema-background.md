---
description: Lo schema di stampa risolve l'opacità e l'ambiguità nella comunicazione tra i componenti del sottosistema di stampa e tra il sottosistema di stampa e le applicazioni.
ms.assetid: 193dd600-7cbb-4f4e-bb7d-7f7117e9d16a
title: Stampare lo sfondo dello schema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ab366429623f2bb1f187294705d1a83e93acd1e5fb500d4b1e9d224496ac39e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118731761"
---
# <a name="print-schema-background"></a>Stampare lo sfondo dello schema

Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Lo schema di stampa è progettato per risolvere i problemi di opacità e ambiguità associati alla comunicazione interna tra i componenti del sottosistema di stampa e alla comunicazione esterna tra il sottosistema di stampa e le applicazioni.

L'interazione del sottosistema di stampa corrente con i plug-in di applicazioni e fornitori di hardware usa la struttura DEVMODE binaria basata su indice e devCaps binaria. Impostazioni da ogni componente sono in gran parte opache rispetto ad altri componenti, impedendo la portabilità delle impostazioni tra i dispositivi o anche tra versioni diverse del driver nello stesso dispositivo. Inoltre, PrintCapabilities non può essere facilmente sfruttato dalle applicazioni client senza conoscenza proprietaria del dispositivo o tramite l'interfaccia utente del driver. Oltre a queste limitazioni, in senso più ampio non esiste un linguaggio ben definito per descrivere gli attributi generali del dispositivo, PrintCapabilities, le configurazioni del dispositivo o la formattazione del processo. Lo schema di stampa e le tecnologie correlate sono progettati per risolvere queste limitazioni, fornendo un metodo coerente, non ambiguo ed estendibile di comunicazione delle impostazioni e delle funzionalità in modo consolidato e logico.

Le basi concettuali delle parole chiave dello schema di stampa e di Print Schema Framework sono la coerenza, la mancanza di ambiguità e di estendibilità. La coerenza viene ottenuta tramite l'uso delle parole chiave dello schema di stampa e del framework dello schema di stampa come blocchi predefiniti per la comunicazione tra componenti di stampa di nuova generazione. Le applicazioni, il sottosistema di stampa Windows Microsoft e i plug-in e i driver IHV interagiscono usando questo meccanismo comune. Queste parole chiave, la struttura e il relativo significato saranno ben definiti dallo schema pubblico. Ciò impedisce l'ambiguità nel significato di una determinata parola chiave e impedisce parole chiave ridondanti o duplicate. Tutti i componenti possono basarsi sull'uso di una determinata parola chiave per comunicare una determinata finalità e avere tale finalità ben compresa dal destinatario. L'estendibilità è fondamentale per essere la longevità delle parole chiave dello schema di stampa, garantendo che lo schema pubblico sia un'entità dinamica. La struttura consente anche estensioni private, che concedono agli IHV la flessibilità necessaria per innovare in base alle esigenze, tenendo presente che l'inclusione futura di una parola chiave privata nello schema pubblico è essenziale per mantenere la coerenza e prevenire l'ambiguità.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



