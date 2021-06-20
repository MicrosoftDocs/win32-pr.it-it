---
description: Informazioni sulla sintassi dello schema di stampa, espressa nella sintassi XML ed è costituita da un numero ridotto di tipi di elementi.
ms.assetid: d67518e3-c379-4a50-aeda-31afaa7f05dd
title: Sintassi dello schema di stampa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ef52dbdbdfacc2d3cc947b46558319577a75b1b
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405294"
---
# <a name="syntax-of-the-print-schema"></a>Sintassi dello schema di stampa

Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Lo schema di stampa è espresso nella sintassi XML. È quindi previsto che i lettori conoscano la sintassi XML e termini come elemento, tag di elemento, contenuto degli elementi, attributo e spazio dei nomi. Print Schema Framework è costituito da un numero ridotto di tipi di elementi. ogni tipo di elemento ha uno scopo specifico nelle tecnologie create sullo schema di stampa.

I tipi di elemento vengono distinti in base al tag dell'elemento XML. Print Schema Framework definisce la struttura complessiva e l'organizzazione delle tecnologie dipendenti, indicando per ogni tipo di elemento quali tipi di elemento sono consentiti come elementi figlio.

Molti tipi di elementi sono differenziati da altri dello stesso tipo in base all'attributo name, che svolge un ruolo significativo nello schema. L'attributo name serve per identificare le istanze di ogni tipo di elemento. Le parole chiave dello schema di stampa definiscono un set di valori per l'attributo name per molti dei tipi di elemento. Nella maggior parte dei casi, i provider possono assegnare i propri valori all'attributo name. È necessario assicurarsi che i valori siano QName XML qualificati con uno spazio dei nomi univoco per il provider.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



