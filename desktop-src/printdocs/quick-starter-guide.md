---
description: Questo articolo offre una guida introduttiva all'implementazione di PrintTicket e PrintCapabilities per l'applicazione o il driver di dispositivo.
ms.assetid: 2c1d912e-464e-48d2-ba4f-c0b9a811b25e
title: Guida introduttiva rapida
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6060de551d3fb663e148cf80f661c4d517a51b93
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405314"
---
# <a name="quick-starter-guide"></a>Guida introduttiva rapida

Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Questa pagina è progettata per offrire una guida introduttiva all'implementazione di PrintTicket e PrintCapabilities per l'applicazione o il driver di dispositivo. Anche se è consigliabile leggere la specifica dello schema di stampa per intero, questa pagina consente di iniziare a fare un salto nelle aree chiave a cui prestare attenzione.

1) Leggere [print Schema-Related Technologies](print-schema-related-technologies.md) per una panoramica delle tecnologie PrintTicket e Print Capabilities

2) Assicurarsi di avere a portata di mano il riepilogo [dei tipi](summary-of-element-types.md) di elementi usati per esprimere le tecnologie correlate allo schema di stampa.

3) I documenti PrintCapabilities e PrintTicket [](scoping-prefix.md) sono definiti a tre livelli di prefisso di ambito, Job, Document e Page.

4) Leggere i diversi attributi [XML usati](xml-attributes.md) all'interno di diversi tipi di elementi dello schema di stampa

5) Esaminare [l'elenco di controllo per la costruzione di documenti PrintCapabilities](printcapabilities-document-construction-checklist.md) e anche l'esempio [di documento PrintCapabilities fornito](printcapabilities-document-example.md)

6) Esaminare gli [elenchi di controllo per la costruzione di PrintTicket](printticket-construction-checklists.md) e anche l'esempio [printticket fornito](printticket-example.md)

7) I provider PrintTicket devono anche esaminare [l'elenco di controllo di convalida PrintTicket](printticket-validation-checklist.md) per garantire la conformità alla specifica PrintSchema

8) Esaminare sia le parole [](parameter-definitions.md) [chiave dello](user-configurable-elements.md) schema di stampa pubbliche degli elementi configurabili dall'utente che le definizioni dei parametri che possono essere visualizzate in un documento PrintCapabilities

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



