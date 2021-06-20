---
description: Questi articoli forniscono informazioni più dettagliate sul significato e sull'utilizzo dei tipi di elemento dello schema di stampa.
ms.assetid: 05c7fd07-1c32-409d-8ca5-820038af3440
title: Framework dello schema di stampa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 570701df700954ad85fb724b9528b7e7912f3174
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407164"
---
# <a name="print-schema-framework"></a>Framework dello schema di stampa

Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

In questa sezione vengono fornite informazioni più dettagliate sul significato e sull'utilizzo dei tipi di elemento dello schema di stampa. L'obiettivo principale della versione iniziale di Print Schema Framework è rappresentare le configurazioni e le funzionalità degli attributi del dispositivo. A livello elevato, questo framework offre due stili diversi per descrivere un attributo del dispositivo: come costrutto Feature/Option o come costrutto di parametro. Se un attributo dispositivo ha un numero ridotto di valori o stati disponibili, l'attributo deve essere caratterizzato come feature con i valori o gli stati consentiti definiti elementi Option. Viceversa, se un attributo del dispositivo ha un numero elevato di valori o stati disponibili e il set di tutti i valori possibili è facilmente definito senza ricorrere all'enumerazione esplicita, l'attributo dispositivo deve essere caratterizzato come parametro. Un parametro viene definito tramite un elemento ParameterDef e un'istanza del parametro viene inizializzata tramite un elemento ParameterInit. Gli elementi proprietà vengono usati all'interno di costrutti feature/option e parametri per fornire un livello di differenziazione più fine.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



