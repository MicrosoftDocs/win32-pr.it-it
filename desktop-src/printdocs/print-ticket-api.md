---
description: L'API Print Ticket consente alle applicazioni di gestire e convertire i ticket di stampa.
ms.assetid: 4f854c1a-f2e1-48c4-9cc1-8a0fcf1bebed
title: API Print Ticket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e19cfd8d624a1390b8afacd625e92fcee2704dd
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "104058478"
---
# <a name="print-ticket-api"></a>API Print Ticket

L'API Print Ticket consente alle applicazioni di gestire e convertire i ticket di stampa.

Un Print Ticket è un componente del documento XPS che contiene le impostazioni della stampante preferite per una pagina in un documento o per un intero documento o per un processo di stampa che contiene uno o più documenti. Si noti che i ticket di stampa sono disponibili solo nei documenti XPS.

Prima che la stampante possa utilizzare il ticket di stampa, il ticket di stampa deve essere convalidato in base alle caratteristiche della stampante, definite nelle funzionalità di stampa della stampante. L'applicazione esegue tale convalida chiamando l'API del ticket di stampa.

PrintTicket e PrintCapabilities vengono descritti utilizzando gli elementi dello schema di stampa, definito dalla [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Questo argomento contiene informazioni sugli elementi API seguenti:

-   [Funzioni API del ticket di stampa](print-ticket-api-functions.md)
-   [Enumerazioni API del ticket di stampa](print-ticket-api-enumerations.md)

Il diagramma seguente mostra la relazione tra l'API del ticket di stampa e le altre API di stampa che un'applicazione Windows nativa può usare.

![diagramma che mostra la relazione tra l'API del ticket di stampa e le altre API di stampa che possono essere utilizzate da un'applicazione Windows nativa](images/print-apis-pt.png)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[API di stampa XPS](xps-printing.md)
</dt> <dt>

[API spooler di stampa](print-spooler-api.md)
</dt> <dt>

[API di stampa GDI](gdi-printing.md)
</dt> <dt>

[Specifica dello schema di stampa](https://go.microsoft.com/fwlink/?linkid=2022117)
</dt> <dt>

[XML Paper Specification](https://go.microsoft.com/fwlink/?linkid=2022122)
</dt> </dl>

 

 



