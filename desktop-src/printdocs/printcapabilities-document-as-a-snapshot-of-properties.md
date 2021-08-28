---
title: Documento come snapshot delle proprietà
description: Esaminare il documento PrintCapabilities come snapshot delle proprietà. Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica dello schema di stampa.
ms.assetid: 476c98e6-face-42cf-874d-cfa7a54b0666
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a031334e820b140cb27f7c293741a84e0d8a89c6c9d1c47f89cf83a87a2d3cd4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119033909"
---
# <a name="printcapabilities-document-as-a-snapshot-of-properties"></a>Documento PrintCapabilities come snapshot delle proprietà

Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Il dispositivo descritto da PrintCapabilities può avere proprietà che dipendono dallo stato o dalla configurazione del dispositivo. Mentre PrintCapabilities rappresenta l'intero spazio di configurazione di un dispositivo, il provider PrintCapabilities produce un'istanza dipendente dalla configurazione di PrintCapabilities denominata documento PrintCapabilities. Questo documento PrintCapabilities dipendente dalla configurazione evita di gravare sullo schema PrintCapabilities con la complessità della rappresentazione di dati multivalore. Ancora più importante, per liberare un consumer del documento PrintCapabilities dall'onere di estrarre il valore appropriato da una rappresentazione dei dati multivalore, tutte le istanze Property e ScoredProperty in un documento PrintCapabilities devono essere a valore singolo. In altre parole, ogni istanza Property e ScoredProperty in un documento PrintCapabilities deve avere un valore fisso, relativo alla configurazione di input. Ogni documento PrintCapabilities può essere pensato come uno snapshot delle proprietà del dispositivo quando il dispositivo si trova in uno stato specifico. Di conseguenza, prima di poter costruire un documento PrintCapabilities, è necessario specificare la configurazione da usare.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



