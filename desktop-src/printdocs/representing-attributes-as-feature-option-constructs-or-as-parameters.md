---
description: Rappresentano gli attributi come costrutti di funzionalità/opzione o come parametri. Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print Schema Specification( Specifica dello schema di stampa).
ms.assetid: 055e502d-631f-49d2-8577-65396373d478
title: Rappresentazione di attributi come costrutti di funzionalità/opzioni o come parametri
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c93f4de56709ed310a7f0aa259b1dbfd3377ed42
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120056"
---
# <a name="representing-attributes-as-featureoption-constructs-or-as-parameters"></a>Rappresentazione di attributi come costrutti di funzionalità/opzioni o come parametri

Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

L'autore di un documento PrintCapabilities definisce gli attributi del dispositivo che costituiscono la configurazione. Nel documento PrintCapabilities l'autore può scegliere di rappresentare un attributo del dispositivo come costrutto Feature/Option o come costrutto di parametro.

Se un attributo del dispositivo ha un numero relativamente ridotto di possibili stati che non rientrano in alcun tipo di modello ovvio, un costrutto di funzionalità/opzione è in genere la scelta migliore. Ad esempio, se i valori consentiti per l'attributo di dispositivo PageMediaSize sono i valori Letter, Legal, A4ISO, Tabloid e Envelope10, un costrutto Feature/Option è la scelta migliore per la rappresentazione. A causa della difficoltà e dell'ambiguità associate all'espressione dei valori consentiti senza enumerazione esplicita, il costrutto di parametro non è appropriato per l'attributo PageMediaSize.

Se un attributo del dispositivo può essere rappresentato da un intervallo di numeri interi, la rappresentazione dei parametri è in genere la scelta migliore, soprattutto per gli intervalli che includono molti valori. Ad esempio, se l'attributo di dispositivo CopyCount per un particolare modello di stampante può variare da 1 a 99.999, questo attributo deve essere categorizzato come parametro, definendo un'istanza ParameterDef. Assegnare valori alle istanze delle proprietà standard MinValue e MaxValue dell'elemento ParameterDef per definire l'intervallo di valori per l'attributo JobCopyCount. A causa del numero elevato di valori che devono essere elencati in modo esplicito come elementi Option, la rappresentazione di funzionalità/opzioni non è appropriata per l'attributo del dispositivo JobCopyCount.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



