---
description: L'API di stampa GDI fornisce alle applicazioni un'interfaccia di stampa indipendente dal dispositivo.
ms.assetid: 3115c9e0-05c9-462d-8238-fc035ea32d4e
title: API di stampa GDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fc2a872b3a310ea44ddfc84103ddbd11cff61998d4884dca5f490e88c3d73f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119949197"
---
# <a name="gdi-print-api"></a>API di stampa GDI

L'API di stampa GDI fornisce alle applicazioni un'interfaccia di stampa indipendente dal dispositivo. Usare questa interfaccia se l'applicazione usa GDI per eseguire il rendering di testo e grafica.

Se si scrivono applicazioni per Windows Vista o versioni successive di Windows, è consigliabile usare l'API documento [XPS](/previous-versions/windows/desktop/dd316976(v=vs.85)) e l'API di stampa [XPS](xps-printing.md) per usare le interfacce grafiche con prestazioni più elevate supportate dai driver di stampa XPSDrv.

In questa sezione vengono fornite informazioni sugli argomenti seguenti.



| Argomento                                                                                             | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Informazioni sull'API di stampa GDI](about-the-gdi-print-api.md)<br/>                                 | Panoramica della funzionalità di stampa GDI.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [Uso dell'API di stampa GDI](using-the-printing-functions.md)<br/>                            | Informazioni sull'uso dell'API di stampa GDI in un'applicazione.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [Informazioni di riferimento sulle API di stampa GDI](gdi-print-api-reference.md)<br/>                                 | Descrizioni dettagliate di funzioni, strutture e altri elementi dell'API di stampa GDI.<br/>                                                                                                                                                                                                                                                                                                                                                                                                               |
| [Microsoft XPS Document Converter (MXDC)](microsoft-xps-document-converter--mxdc-.md)<br/> | [Microsoft XPS Document Converter (MXDC)](microsoft-xps-document-converter--mxdc-.md) è un componente che consente alle applicazioni di usare l'API di stampa GDI con stampanti con un driver di stampa XPSDrv.<br/>                                                                                                                                                                                                                                                                                               |
| [Microsoft XPS Document Writer (MXDW)](microsoft-xps-document-writer.md)<br/>              | Il [Microsoft XPS Document Writer (MXDW)](microsoft-xps-document-writer.md) fornisce alle applicazioni la funzionalità "salva come XPS" o "esporta in XPS". Le applicazioni che non creano in modo nativo il contenuto del documento XPS possono usare MXDW per creare file di documento XPS senza usare [l'API documento XPS](/previous-versions/windows/desktop/dd316976(v=vs.85)). L'API documento XPS, tuttavia, offre a un'applicazione la possibilità di usare le interfacce grafiche con prestazioni più elevate supportate dai driver di stampa XPSDrv.<br/> |



 

Il diagramma seguente illustra la relazione dell'API di stampa GDI con le altre API di stampa che un'applicazione può usare.

![diagramma che mostra la relazione dell'API di stampa gdi con le altre API di stampa che un'applicazione win32 può usare](images/print-apis-gdi.png)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**AddJob**](addjob.md)
</dt> <dt>

[API documento XPS](/previous-versions/windows/desktop/dd316976(v=vs.85))
</dt> <dt>

[API di stampa XPS](xps-printing.md)
</dt> <dt>

[API Spooler di stampa](print-spooler-api.md)
</dt> <dt>

[Print Ticket API](print-ticket-api.md)
</dt> </dl>

 

