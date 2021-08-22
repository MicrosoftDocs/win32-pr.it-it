---
description: ICE23 convalida l'ordine di tabulazione del controllo per ogni finestra di dialogo.
ms.assetid: d425f8c6-4615-439d-8194-3a0325eb3cc3
title: ICE23
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbab2d50c07fce208edc845e64cff0061f513c102a55da2d56b49c4a4c17e867
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119529001"
---
# <a name="ice23"></a>ICE23

ICE23 convalida l'ordine di tabulazione del controllo per ogni finestra di dialogo.

ICE23 convalida quanto segue nella tabella [Dialog e](dialog-table.md) nella [tabella Control](control-table.md):

-   Ogni record nella tabella Dialog specifica un controllo nella colonna Control First presente nella finestra di dialogo \_ specificata dalla colonna Dialog.
-   Ogni record nella tabella Control specifica un controllo nella colonna Control Next nella stessa finestra di dialogo del controllo elencato nella colonna Control oppure Control Next contiene \_ \_ il valore Null.
-   Ciò che segue le voci Control Next dal controllo al controllo nella tabella Control crea un singolo ciclo chiuso che torna \_ al controllo iniziale. Non tutti i controlli devono essere nel ciclo, ma il ciclo deve passare attraverso ogni controllo con una voce nella colonna Control \_ Next.

## <a name="result"></a>Risultato

ICE23 invia un messaggio di errore se l'ordine di tabulazione dei controlli non forma un singolo ciclo chiuso nella finestra di dialogo.

## <a name="example"></a>Esempio

ICE23 pubblica i messaggi di errore seguenti per l'esempio illustrato.

-   Dialog1 non ha alcun controllo \_ prima di tutto.
-   Control \_ First della finestra di dialogo Dialog2 fa riferimento al controllo ControlX inesistente.
-   Dialog3 ha un ordine di tabulazione non corretto in ControlB.
-   Dialog4 ha un ordine di tabulazione in formato non corretto nel controllo ControlC
-   Dialog5 ha un ordine di tabulazione in formato non corretto nel controllo ControlC.
-   Controllo \_ Avanti del controllo Dialog6.ControlC collega a un controllo sconosciuto.

[Tabella delle finestre](dialog-table.md) di dialogo (parziale)



| Finestra di dialogo  | Control \_ First |
|---------|----------------|
| Finestra di dialogo1 |                |
| Finestra di dialogo2 | ControlX       |
| Finestra di dialogo3 | ControlloA       |
| Finestra di dialogo4 | ControlloA       |
| Finestra di dialogo5 | ControlloA       |



 

[Tabella di controllo](control-table.md) (parziale)



| Finestra di dialogo  | Control  | Controllo \_ successivo |
|---------|----------|---------------|
| Finestra di dialogo1 | ControlloA |               |
| Finestra di dialogo1 | ControlB | ControlloA      |
| Finestra di dialogo2 | ControlloA | ControlB      |
| Finestra di dialogo2 | ControlB | ControlloA      |
| Finestra di dialogo3 | ControlloA | ControlB      |
| Finestra di dialogo3 | ControlB |               |
| Finestra di dialogo4 | ControlloA | ControlB      |
| Finestra di dialogo4 | ControlB | ControlC      |
| Finestra di dialogo4 | ControlC | ControlB      |
| Finestra di dialogo5 | ControlloA | ControlB      |
| Finestra di dialogo5 | ControlB | ControlC      |
| Finestra di dialogo5 | ControlC | ControlloA      |
| Finestra di dialogo5 | ControlD | ControlloA      |
| Finestra di dialogo6 | ControlloA | ControlB      |
| Finestra di dialogo6 | ControlB | ControlC      |
| Finestra di dialogo6 | ControlC | ControlX      |
| Finestra di dialogo6 | ControlD | ControlloA      |



 

Per correggere questi errori, tenere presente quanto segue nelle tabelle precedenti e apportare le modifiche indicate.

Non tutte le righe della tabella Dialog hanno un controllo specificato nella colonna Control \_ First. Modificare la colonna Control First del record Dialog1 nella tabella Dialog in \_ un controllo presente in Dialog1.

Non tutte le righe della tabella Dialog hanno un controllo specificato nella colonna Control \_ First presente nella finestra di dialogo. Modificare la colonna Control \_ First di Dialog2 in un controllo presente in Dialog2.

Dopo le voci Control Next nella tabella Control da controllo a controllo non viene fatto un \_ ciclo chiuso in ogni caso. Modificare la colonna Control \_ Next per ControlB in Dialog3 in ControlA.

Dopo le voci Control Next nella tabella Control da controllo a controllo non si torna al \_ controllo iniziale in ogni caso. Modificare la colonna Control \_ Next per ControlC in Dialog4 in modo che faccia riferimento a ControlA.

Dopo le voci Control Next nella tabella Control da control a control non passa attraverso ogni controllo nella finestra di dialogo con una voce \_ nella colonna Control \_ Next. Modificare la colonna \_ Control Next per ControlC in Dialog5 in ControlD.

Il controllo Avanti non fa riferimento a un controllo valido presente nella stessa finestra di dialogo \_ del controllo elencato nella colonna Controllo . Modificare la colonna Control \_ Next per ControlC in Dialog6 in modo che faccia riferimento a ControlD.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento su ICE](ice-reference.md)
</dt> </dl>

 

 



