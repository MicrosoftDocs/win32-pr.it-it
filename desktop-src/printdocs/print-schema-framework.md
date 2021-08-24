---
description: Questi articoli forniscono informazioni più dettagliate sul significato e sull'utilizzo dei tipi di elementi dello schema di stampa.
ms.assetid: 05c7fd07-1c32-409d-8ca5-820038af3440
title: Framework dello schema di stampa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 986308ae2ce1308c7df090da295f8b5473efe99219339a906490299ec33b2ea6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119718601"
---
# <a name="print-schema-framework"></a>Framework dello schema di stampa

Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

In questa sezione vengono fornite informazioni più dettagliate sul significato e sull'utilizzo dei tipi di elementi dello schema di stampa. L'obiettivo principale della versione iniziale di Print Schema Framework è rappresentare le configurazioni e le funzionalità degli attributi del dispositivo. A livello di alto livello, questo framework offre due diversi stili di descrizione di un attributo del dispositivo: come costrutto Feature/Option o come costrutto di parametro. Se un attributo del dispositivo ha un numero ridotto di valori o stati disponibili, l'attributo deve essere caratterizzato come funzionalità con i valori consentiti o gli stati indicati come elementi Option. Al contrario, se un attributo del dispositivo ha un numero elevato di valori o stati disponibili e il set di tutti i valori possibili è facilmente definito senza ricorrere all'enumerazione esplicita, l'attributo del dispositivo deve essere caratterizzato come parametro. Un parametro viene definito tramite un elemento ParameterDef e un'istanza di parametro viene inizializzata tramite un elemento ParameterInit. Gli elementi proprietà vengono usati all'interno di costrutti feature/opzione e parametri per fornire un livello di differenziazione più fine.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



