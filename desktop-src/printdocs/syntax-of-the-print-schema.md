---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: d67518e3-c379-4a50-aeda-31afaa7f05dd
title: Sintassi dello schema di stampa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2503b3f44ff8b4bdda41f0feefe374c27d78bd41
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106321033"
---
# <a name="syntax-of-the-print-schema"></a>Sintassi dello schema di stampa

Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Lo schema di stampa è espresso in sintassi XML. È quindi previsto che i lettori abbiano familiarità con la sintassi XML e con termini quali elemento, tag dell'elemento, contenuto dell'elemento, attributo e spazio dei nomi. Il Framework dello schema di stampa è costituito da un numero ridotto di tipi di elementi. ogni tipo di elemento svolge uno scopo specifico nelle tecnologie basate sullo schema di stampa.

I tipi di elemento sono distinti in base al tag dell'elemento XML. Il Framework dello schema di stampa definisce la struttura complessiva e l'organizzazione delle tecnologie dipendenti, indicando per ogni tipo di elemento quali tipi di elemento sono consentiti come elementi figlio.

Molti tipi di elementi sono differenziati rispetto ad altri dello stesso tipo dall'attributo Name, che svolge un ruolo significativo nello schema. L'attributo Name serve a identificare le istanze di ogni tipo di elemento. Le parole chiave Print Schema definiscono un set di valori per l'attributo Name per molti tipi di elemento. Nella maggior parte dei casi, i provider possono assegnare i propri valori all'attributo Name. Sono necessarie solo per assicurarsi che i valori siano QName XML qualificati con uno spazio dei nomi univoco per il provider.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



