---
description: L'API Print Ticket consente alle applicazioni di gestire e convertire i ticket di stampa.
ms.assetid: 4f854c1a-f2e1-48c4-9cc1-8a0fcf1bebed
title: Print Ticket API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac91cc976addba630bae3f250d244442ba1dd3b61f741575fe21cb250bab4a2f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119947796"
---
# <a name="print-ticket-api"></a>Print Ticket API

L'API Print Ticket consente alle applicazioni di gestire e convertire i ticket di stampa.

Un ticket di stampa è un componente di documento XPS che contiene le impostazioni della stampante preferite per una pagina di un documento o per un intero documento o per un processo di stampa che contiene uno o più documenti. Si noti che i ticket di stampa si trovano solo nei documenti XPS.

Prima che la stampante possa usare il ticket di stampa, il ticket di stampa deve essere convalidato in base alle caratteristiche della stampante, definite nelle funzionalità di stampa della stampante. L'applicazione esegue tale convalida chiamando l'API Print Ticket.

PrintTicket e PrintCapabilities vengono descritti usando gli elementi dello schema di stampa, definiti dalla [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Questo argomento contiene informazioni sugli elementi API seguenti:

-   [Funzioni dell'API Print Ticket](print-ticket-api-functions.md)
-   [Enumerazioni dell'API Print Ticket](print-ticket-api-enumerations.md)

Il diagramma seguente illustra la relazione dell'API Print Ticket con le altre API di stampa che un'Windows nativa può usare.

![diagramma che illustra la relazione dell'API print ticket con le altre API di stampa che un'applicazione windows nativa può usare](images/print-apis-pt.png)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[API di stampa XPS](xps-printing.md)
</dt> <dt>

[API Spooler di stampa](print-spooler-api.md)
</dt> <dt>

[API di stampa GDI](gdi-printing.md)
</dt> <dt>

[Specifica dello schema di stampa](https://go.microsoft.com/fwlink/?linkid=2022117)
</dt> <dt>

[XML Paper Specification](https://go.microsoft.com/fwlink/?linkid=2022122)
</dt> </dl>

 

 



