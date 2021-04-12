---
description: "Quando si decide quando e come usare l'oggetto divisore in un'applicazione, tenere presente quanto segue:"
ms.assetid: 17404789-7f08-4cf1-88f8-e1f70296c163
title: Altre considerazioni sul divisore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6e00ebc926dd51efb592304f6015351bdc2790b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232478"
---
# <a name="other-divider-considerations"></a>Altre considerazioni sul divisore

Quando si decide quando e come usare l'oggetto [**divisore**](inkdivider-class.md) in un'applicazione, tenere presente quanto segue:

-   L'oggetto [**divisore**](inkdivider-class.md) è progettato per separare i disegni e i blocchi di grafia, ma non per riconoscere livelli più elevati di struttura, ad esempio tabelle o colonne.
-   L'oggetto [**divisore**](inkdivider-class.md) non fornisce interfacce specifiche per la correzione dei risultati dell'analisi del layout.
-   L'utilizzo del timeout e del numero di euristiche del tratto per aggiungere o rimuovere più tratti alla volta dai tratti nell'oggetto [**divisore**](inkdivider-class.md) può migliorare le prestazioni.

## <a name="reanalysis-considerations"></a>Considerazioni sulla rianalisi

Se si sta prendendo in considerazione l'uso dell'oggetto [**divisore**](inkdivider-class.md) in un'applicazione in cui l'oggetto **divisore** potrebbe dover rianalizzare grandi quantità di input penna, tenere presente quanto segue.

### <a name="retaining-copies-of-ink-and-strokes"></a>Conservazione di copie di input penna e tratti

Un'applicazione può tenere copie degli oggetti [**Ink**](inkdisp-class.md) e [**DivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) per gli elementi dell'applicazione che possono essere rivisitati successivamente nella sessione dell'applicazione. In questo modo si elimina la necessità di rianalizzare l'oggetto **Ink** se l'utente torna all'elemento. Questo approccio viene compromesso dalla memoria per ottenere prestazioni migliori.

### <a name="data-reduction-heuristics"></a>Euristica di riduzione dei dati

Potrebbe essere possibile registrare i risultati dell'analisi come dati dell'applicazione e implementare l'euristica per determinare quando rianalizzare un set di tratti. Questa pratica ridurrebbe la necessità di analizzare di tutto l'input penna nell'applicazione tra le sessioni dell'applicazione. Tuttavia, è necessario prestare attenzione per mantenere i limiti degli elementi strutturali o per analizzare nuovamente tutti i tratti per gli elementi interessati.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Classe InkDivider**](inkdivider-class.md)
</dt> <dt>

[Classe Microsoft. Ink. Divider](/previous-versions/ms583616(v=vs.100))
</dt> </dl>

 

 
