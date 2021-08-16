---
description: "Quando si decide quando e come usare l'oggetto Divider in un'applicazione, tenere presente quanto segue:"
ms.assetid: 17404789-7f08-4cf1-88f8-e1f70296c163
title: Altre considerazioni sui divisori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3328fd553a16aeee1e1dfa5459b78a45732a55494e0481950d730dab7ce0d73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118449361"
---
# <a name="other-divider-considerations"></a>Altre considerazioni sui divisori

Quando si decide quando e come usare l'oggetto [**Divider**](inkdivider-class.md) in un'applicazione, tenere presente quanto segue:

-   [**L'oggetto Divisore**](inkdivider-class.md) è progettato per separare disegni e blocchi di scrittura manuale, ma non per riconoscere livelli di struttura più elevati, ad esempio tabelle o colonne.
-   [**L'oggetto Divider**](inkdivider-class.md) non fornisce interfacce specifiche per la correzione dei risultati dell'analisi del layout.
-   L'uso di timeout e numero di euristiche dei tratti per aggiungere o rimuovere più tratti contemporaneamente dai tratti nell'oggetto [**Divider**](inkdivider-class.md) può migliorare le prestazioni.

## <a name="reanalysis-considerations"></a>Considerazioni sulla rianalisi

Se si sta valutando l'uso dell'oggetto [**Divider**](inkdivider-class.md) in un'applicazione in cui l'oggetto **Divider** potrebbe essere necessario rianalyizzare grandi quantità di input penna, tenere presente quanto segue.

### <a name="retaining-copies-of-ink-and-strokes"></a>Mantenimento di copie di input penna e tratti

Un'applicazione può conservare copie degli oggetti [**Ink**](inkdisp-class.md) e [**DivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) per gli elementi dell'applicazione che possono essere rivisitato più avanti nella sessione dell'applicazione. In questo modo si elimina la necessità di rianalyizzare **l'oggetto Ink** se l'utente torna all'elemento. Questo approccio scambia la memoria per ottenere prestazioni migliori.

### <a name="data-reduction-heuristics"></a>Euristica della riduzione dei dati

È possibile registrare i risultati dell'analisi come dati dell'applicazione e implementare l'euristica per determinare quando rianare un set di tratti. Questa procedura ridurrebbe la necessità di rianalyizzare tutto l'input penna nell'applicazione tra le sessioni dell'applicazione. È tuttavia necessario fare attenzione a mantenere i limiti degli elementi strutturali o a rianalizzare tutti i tratti per gli elementi interessati.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Classe InkDivider**](inkdivider-class.md)
</dt> <dt>

[Classe Microsoft.Ink.Divider](/previous-versions/ms583616(v=vs.100))
</dt> </dl>

 

 
