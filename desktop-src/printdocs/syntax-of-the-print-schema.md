---
description: Informazioni sulla sintassi dello schema di stampa, espressa nella sintassi XML ed è costituita da un numero ridotto di tipi di elemento.
ms.assetid: d67518e3-c379-4a50-aeda-31afaa7f05dd
title: Sintassi dello schema di stampa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a55fbae9b74fe9537430c926870e422cb1a9cd0e025d4aedf702865a8822c740
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119662371"
---
# <a name="syntax-of-the-print-schema"></a>Sintassi dello schema di stampa

Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Lo schema di stampa è espresso nella sintassi XML. Si prevede pertanto che i lettori conoscano la sintassi e i termini XML, ad esempio elemento, tag di elemento, contenuto degli elementi, attributo e spazio dei nomi. Print Schema Framework è costituito da un numero ridotto di tipi di elementi. Ogni tipo di elemento svolge uno scopo specifico nelle tecnologie create in base allo schema di stampa.

I tipi di elemento si distinguono in base al tag dell'elemento XML. Print Schema Framework definisce la struttura generale e l'organizzazione delle tecnologie dipendenti, indicando per ogni tipo di elemento quali tipi di elemento sono consentiti come elementi figlio.

Molti tipi di elemento si differenziano dagli altri dello stesso tipo in base all'attributo name, che svolge un ruolo significativo nello schema. L'attributo name serve a identificare le istanze di ogni tipo di elemento. Le parole chiave dello schema di stampa definiscono un set di valori per l'attributo name per molti dei tipi di elemento. Nella maggior parte dei casi, i provider possono assegnare i propri valori all'attributo name. È necessario solo assicurarsi che i valori siano QName XML qualificati con uno spazio dei nomi univoco per il provider.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



