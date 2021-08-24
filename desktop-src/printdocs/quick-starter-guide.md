---
description: Questo articolo offre una guida introduttiva all'implementazione di PrintTicket e PrintCapabilities per l'applicazione o il driver di dispositivo.
ms.assetid: 2c1d912e-464e-48d2-ba4f-c0b9a811b25e
title: Guida introduttiva
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2730048a001f33563ad6beb95ea2e3c17974e8f29f11425a077f86bbf97c51f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119824061"
---
# <a name="quick-starter-guide"></a>Guida introduttiva

Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Questa pagina è progettata per offrire una guida introduttiva all'implementazione di PrintTicket e PrintCapabilities per l'applicazione o il driver di dispositivo. Anche se è consigliabile leggere la specifica dello schema di stampa in modo completo, questa pagina consente di iniziare rapidamente nelle aree principali a cui è necessario prestare attenzione.

1) Per una [panoramica delle tecnologie](print-schema-related-technologies.md) printTicket e delle funzionalità di stampa, vedere Tecnologie di Schema-Related stampa

2) Assicurarsi di avere una conoscenza del riepilogo dei tipi di [elemento](summary-of-element-types.md) usati per esprimere le tecnologie correlate allo schema di stampa.

3) I documenti PrintCapabilities e i PrintTicket sono definiti a tre livelli di prefisso di ambito: Processo, Documento e Pagina. [](scoping-prefix.md)

4) Leggere i diversi attributi [XML usati](xml-attributes.md) all'interno di diversi tipi di elemento dello schema di stampa

5) Esaminare [l'elenco di controllo per la costruzione di documenti PrintCapabilities](printcapabilities-document-construction-checklist.md) e l'esempio [di documento PrintCapabilities fornito](printcapabilities-document-example.md)

6) Esaminare gli [elenchi di controllo per la costruzione di PrintTicket](printticket-construction-checklists.md) e l'esempio di [PrintTicket fornito](printticket-example.md)

7) I provider PrintTicket devono anche esaminare l'elenco [di controllo per la convalida di PrintTicket](printticket-validation-checklist.md) per garantire la conformità alla specifica PrintSchema

8) Esaminare sia le parole [](parameter-definitions.md) chiave dello schema [di](user-configurable-elements.md) stampa pubblico degli elementi configurabili dall'utente che le definizioni dei parametri che possono essere visualizzate in un documento PrintCapabilities

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



