---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: 055e502d-631f-49d2-8577-65396373d478
title: Rappresentazione di attributi come costrutti di funzionalità o di opzioni o come parametri
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2c24843a175337f40a84dcdacc41e1a2ab1e15e
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "104058482"
---
# <a name="representing-attributes-as-featureoption-constructs-or-as-parameters"></a>Rappresentazione di attributi come costrutti di funzionalità o di opzioni o come parametri

Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

L'autore di un documento PrintCapabilities definisce gli attributi del dispositivo che costituiscono la configurazione. Nel documento PrintCapabilities l'autore può scegliere di rappresentare un attributo di dispositivo come costrutto di funzionalità/opzione o come costrutto di parametro.

Se un attributo del dispositivo ha un numero relativamente ridotto di stati possibili che non rientrano in una sorta di modello ovvio, un costrutto di funzionalità/opzione è in genere la scelta migliore. Se, ad esempio, i valori consentiti per l'attributo del dispositivo PageMediaSize sono i valori lettera, Legal, A4ISO, tabloid e Envelope10, un costrutto di funzionalità/opzione sarebbe la scelta migliore per la rappresentazione. A causa della difficoltà e dell'ambiguità associate all'espressione dei valori consentiti senza enumerazione esplicita, il costrutto di parametro non è appropriato per l'attributo PageMediaSize.

Se un attributo del dispositivo può essere rappresentato da un intervallo di numeri interi, la rappresentazione del parametro rappresenta in genere la scelta migliore, specialmente per gli intervalli che includono molti valori. Se, ad esempio, l'attributo del dispositivo CopyCount per un determinato modello di stampante può variare da 1 a 99.999, questo attributo deve essere categorizzato come parametro, definendo un'istanza di ParameterDef. Assegnare i valori alle istanze di proprietà standard MinValue e MaxValue dell'elemento ParameterDef per definire l'intervallo di valori per l'attributo JobCopyCount. A causa dell'elevato numero di valori che devono essere elencati in modo esplicito come elementi option, la rappresentazione di funzionalità/opzioni non è appropriata per l'attributo del dispositivo JobCopyCount.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



