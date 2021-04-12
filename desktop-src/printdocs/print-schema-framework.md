---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: 05c7fd07-1c32-409d-8ca5-820038af3440
title: Print Schema Framework
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 617f747b950676f2359645684c9e672fb5c87ee3
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "104234546"
---
# <a name="print-schema-framework"></a>Print Schema Framework

Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

In questa sezione vengono fornite informazioni più dettagliate sul significato e sull'utilizzo dei tipi di elemento dello schema di stampa. L'obiettivo principale della versione iniziale di Print Schema Framework consiste nel rappresentare le configurazioni e le funzionalità degli attributi del dispositivo. A livello generale, questo Framework offre due stili diversi per descrivere un attributo del dispositivo: come costrutto di funzionalità/opzione o come costrutto di parametro. Se un attributo del dispositivo ha un numero ridotto di valori o stati disponibili, l'attributo deve essere caratterizzato da una funzionalità con i valori consentiti o gli stati definiti elementi option. Viceversa, se un attributo del dispositivo ha un numero elevato di valori o stati disponibili e il set di tutti i valori possibili è facilmente definito senza ricorrere all'enumerazione esplicita, l'attributo del dispositivo deve essere caratterizzato da un parametro. (Un parametro viene definito tramite un elemento ParameterDef e un'istanza di parametro viene inizializzata tramite un elemento ParameterInit). Gli elementi Property vengono utilizzati all'interno di costrutti di funzionalità, opzioni e parametri per offrire un livello di differenziazione più preciso.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



