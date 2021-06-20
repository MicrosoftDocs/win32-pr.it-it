---
description: Lo schema di stampa risolve l'opacità e l'ambiguità nella comunicazione tra i componenti del sottosistema di stampa e tra il sottosistema di stampa e le applicazioni.
ms.assetid: 193dd600-7cbb-4f4e-bb7d-7f7117e9d16a
title: Stampare lo sfondo dello schema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d46990e92c1125d33cced67f596ebcfc1db96053
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407154"
---
# <a name="print-schema-background"></a>Stampare lo sfondo dello schema

Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Lo schema di stampa è progettato per risolvere i problemi di opacità e ambiguità associati alla comunicazione interna tra i componenti del sottosistema di stampa e alla comunicazione esterna tra il sottosistema di stampa e le applicazioni.

L'interazione del sottosistema di stampa corrente con le applicazioni e i plug-in dei fornitori di hardware usa la struttura DEVMODE binaria basata su indice e devCaps binari. Le impostazioni effettuate da ogni componente sono in gran parte opache rispetto ad altri componenti, impedendo la portabilità delle impostazioni tra i dispositivi o anche tra versioni diverse dei driver nello stesso dispositivo. Inoltre, PrintCapabilities non può essere facilmente sfruttato dalle applicazioni client senza conoscenza proprietaria del dispositivo o tramite l'interfaccia utente del driver. Oltre a queste limitazioni, in senso più ampio non esiste un linguaggio ben definito per descrivere gli attributi generali del dispositivo, PrintCapabilities, le configurazioni del dispositivo o la formattazione dei processi. Lo schema di stampa e le tecnologie correlate sono progettati per risolvere queste limitazioni, offrendo un metodo coerente, non ambiguo ed estendibile di comunicazione di impostazioni e funzionalità in modo consolidato e logico.

Le nozioni di base concettuali delle parole chiave dello schema di stampa e del framework dello schema di stampa sono la coerenza, la mancanza di ambiguità e l'estendibilità. La coerenza viene ottenuta tramite l'uso delle parole chiave dello schema di stampa e del framework dello schema di stampa come blocchi predefiniti per la comunicazione tra componenti di stampa di nuova generazione. Le applicazioni, il sottosistema di stampa di Microsoft Windows e i plug-in e i driver IHV interagiscono usando questo meccanismo comune. Queste parole chiave, la relativa struttura e il relativo significato saranno ben definiti dallo schema pubblico. In questo modo si evita ambiguità nel significato di una particolare parola chiave e si evitano parole chiave ridondanti o duplicate. Tutti i componenti possono basarsi sull'uso di una particolare parola chiave per comunicare una determinata finalità e fare in modo che tale finalità sia ben compresa dal destinatario. L'estendibilità è fondamentale per essere la longevità delle parole chiave dello schema di stampa, assicurando che lo schema pubblico sia un'entità dinamica. La struttura consente anche estensioni private, che concedono agli IHV la flessibilità di innovare in base alle esigenze, tenendo presente che l'inclusione futura di una parola chiave privata nello schema pubblico è essenziale per mantenere la coerenza e prevenire l'ambiguità.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



