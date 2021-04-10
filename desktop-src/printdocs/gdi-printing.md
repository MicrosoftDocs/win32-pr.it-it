---
description: L'API di stampa GDI fornisce le applicazioni con un'interfaccia di stampa indipendente dal dispositivo.
ms.assetid: 3115c9e0-05c9-462d-8238-fc035ea32d4e
title: API di stampa GDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0239282543a68c6fe8b5d6503d085582fd9c20db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227468"
---
# <a name="gdi-print-api"></a>API di stampa GDI

L'API di stampa GDI fornisce le applicazioni con un'interfaccia di stampa indipendente dal dispositivo. Utilizzare questa interfaccia se l'applicazione utilizza GDI per il rendering di testo e grafica.

Se si scrivono applicazioni per Windows Vista o versioni successive di Windows, è consigliabile usare l' [API di documento XPS](/previous-versions/windows/desktop/dd316976(v=vs.85)) e l' [API di stampa XPS](xps-printing.md) per usare le interfacce grafiche a prestazioni elevate supportate dai driver di stampa XPSDrv.

In questa sezione vengono fornite informazioni sui seguenti argomenti.



| Argomento                                                                                             | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Informazioni sull'API di stampa GDI](about-the-gdi-print-api.md)<br/>                                 | Panoramica della funzionalità di stampa GDI.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [Uso dell'API di stampa GDI](using-the-printing-functions.md)<br/>                            | Informazioni sull'utilizzo dell'API di stampa GDI in un'applicazione.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [Informazioni di riferimento sulle API di stampa GDI](gdi-print-api-reference.md)<br/>                                 | Descrizioni dettagliate delle funzioni, delle strutture e di altri elementi dell'API di stampa GDI.<br/>                                                                                                                                                                                                                                                                                                                                                                                                               |
| [Microsoft XPS Document Converter (MXDC)](microsoft-xps-document-converter--mxdc-.md)<br/> | [Microsoft XPS Document Converter (MXDC)](microsoft-xps-document-converter--mxdc-.md) è un componente che consente alle applicazioni di utilizzare l'API di stampa GDI con stampanti che dispongono di un driver di stampa XPSDrv.<br/>                                                                                                                                                                                                                                                                                               |
| [Microsoft XPS Document Writer (MXDW)](microsoft-xps-document-writer.md)<br/>              | [Microsoft XPS Document Writer (MXDW)](microsoft-xps-document-writer.md) fornisce applicazioni con la funzionalità "Save As XPS" o "Export to XPS". Le applicazioni che non creano in modo nativo contenuto del documento XPS possono usare MXDW per creare file di documento XPS senza usare l' [API documento XPS](/previous-versions/windows/desktop/dd316976(v=vs.85)). L'API documenti XPS, tuttavia, fornisce a un'applicazione la possibilità di utilizzare le interfacce grafiche con prestazioni più elevate supportate dai driver di stampa XPSDrv.<br/> |



 

Nel diagramma seguente viene illustrata la relazione tra l'API di stampa GDI e le altre API di stampa che un'applicazione può utilizzare.

![diagramma che mostra la relazione tra l'API di stampa GDI e le altre API di stampa che un'applicazione Win32 può utilizzare](images/print-apis-gdi.png)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**AddJob**](addjob.md)
</dt> <dt>

[API documenti XPS](/previous-versions/windows/desktop/dd316976(v=vs.85))
</dt> <dt>

[API di stampa XPS](xps-printing.md)
</dt> <dt>

[API spooler di stampa](print-spooler-api.md)
</dt> <dt>

[API Print Ticket](print-ticket-api.md)
</dt> </dl>

 

