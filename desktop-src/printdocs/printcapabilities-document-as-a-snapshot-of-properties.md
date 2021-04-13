---
title: Documento come snapshot delle proprietà
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: 476c98e6-face-42cf-874d-cfa7a54b0666
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d73fc190ed8c259e64fdd60cc291c6ae5b58f80
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "104401840"
---
# <a name="printcapabilities-document-as-a-snapshot-of-properties"></a>Documento PrintCapabilities come snapshot delle proprietà

Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Il dispositivo descritto dall'oggetto PrintCapabilities potrebbe avere proprietà che dipendono dallo stato o dalla configurazione del dispositivo. Mentre l'oggetto PrintCapabilities rappresenta lo spazio di configurazione completo di un dispositivo, il provider PrintCapabilities produce un'istanza dipendente dalla configurazione della classe PrintCapabilities denominata documento PrintCapabilities. Questo documento PrintCapabilities dipendente dalla configurazione evita di sovraccaricare lo schema PrintCapabilities con la complessità della rappresentazione dei dati multivalore. Ancora più importante, per alleviare un consumer del documento PrintCapabilities dal carico di estrarre il valore appropriato da una rappresentazione dati multivalore, tutte le istanze Property e ScoredProperty in un documento PrintCapabilities devono essere a valore singolo. In altre parole, ogni proprietà e istanza di ScoredProperty in un documento PrintCapabilities deve avere un valore fisso rispetto alla configurazione di input. Ogni documento PrintCapabilities può essere considerato come uno snapshot delle proprietà del dispositivo quando il dispositivo si trova in un determinato stato. Di conseguenza, prima di poter costruire un documento PrintCapabilities, è necessario fornire la configurazione da utilizzare.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



