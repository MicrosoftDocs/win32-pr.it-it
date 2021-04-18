---
description: ICE23 convalida l'ordine di tabulazione del controllo per ogni finestra di dialogo.
ms.assetid: d425f8c6-4615-439d-8194-3a0325eb3cc3
title: ICE23
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c1823a70e50d7dd3c42c2e90d6a2d0f11f2fa5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314227"
---
# <a name="ice23"></a>ICE23

ICE23 convalida l'ordine di tabulazione del controllo per ogni finestra di dialogo.

ICE23 convalida quanto segue nella tabella della [finestra di dialogo](dialog-table.md) e nella [tabella dei controlli](control-table.md):

-   Che ogni record nella tabella della finestra di dialogo specifichi un controllo nella \_ prima colonna del controllo presente nella finestra di dialogo specificata dalla colonna della finestra di dialogo.
-   Che ogni record nella tabella dei controlli specifichi un controllo nella \_ colonna successiva del controllo che si trova nella stessa finestra di dialogo del controllo elencato nella colonna di controllo oppure \_ il controllo successivo contiene il valore null.
-   Che dopo il controllo delle \_ voci successive dal controllo al controllo nella tabella dei controlli viene eseguito un ciclo singolo, chiuso, che torna al controllo iniziale. Non è necessario che tutti i controlli siano presenti nel ciclo, ma il ciclo deve passare tutti i controlli con una voce nella colonna del controllo \_ successiva.

## <a name="result"></a>Risultato

ICE23 Invia un messaggio di errore se l'ordine di tabulazione dei controlli non costituisce un singolo ciclo chiuso nella finestra di dialogo.

## <a name="example"></a>Esempio

ICE23 invierà i messaggi di errore seguenti per l'esempio illustrato.

-   Dialog1 non dispone prima di controllo \_ .
-   Il \_ primo controllo della finestra di dialogo Dialog2 fa riferimento a ControlX del controllo inesistente.
-   Dialog3 ha un ordine di tabulazione non recapitabile a ControlB del controllo.
-   Dialog4 ha un ordine di tabulazione in formato non corretto nel controllo ControlC
-   Dialog5 dispone di un ordine di tabulazione in formato non corretto in ControlC del controllo.
-   Controllare il controllo \_ Next del controllo Dialog6. controlc collegamenti a un controllo sconosciuto.

[Tabella finestra di dialogo](dialog-table.md) (parziale)



| Finestra di dialogo  | \_Primo controllo |
|---------|----------------|
| Dialog1 |                |
| Dialog2 | ControlX       |
| Dialog3 | ControlA       |
| Dialog4 | ControlA       |
| Dialog5 | ControlA       |



 

[Tabella di controllo](control-table.md) (parziale)



| Finestra di dialogo  | Control  | Controllo \_ successivo |
|---------|----------|---------------|
| Dialog1 | ControlA |               |
| Dialog1 | ControlB | ControlA      |
| Dialog2 | ControlA | ControlB      |
| Dialog2 | ControlB | ControlA      |
| Dialog3 | ControlA | ControlB      |
| Dialog3 | ControlB |               |
| Dialog4 | ControlA | ControlB      |
| Dialog4 | ControlB | ControlC      |
| Dialog4 | ControlC | ControlB      |
| Dialog5 | ControlA | ControlB      |
| Dialog5 | ControlB | ControlC      |
| Dialog5 | ControlC | ControlA      |
| Dialog5 | ControlD | ControlA      |
| Dialog6 | ControlA | ControlB      |
| Dialog6 | ControlB | ControlC      |
| Dialog6 | ControlC | ControlX      |
| Dialog6 | ControlD | ControlA      |



 

Per correggere questi errori, tenere presente quanto riportato di seguito nelle tabelle precedenti e apportare le modifiche indicate.

Non tutte le righe nella tabella della finestra di dialogo hanno un controllo specificato nella \_ prima colonna del controllo. Modificare la \_ prima colonna controllo del record Dialog1 nella tabella della finestra di dialogo in un controllo presente in Dialog1.

Non tutte le righe della tabella della finestra di dialogo hanno un controllo specificato nella prima colonna del controllo presente nella finestra di \_ dialogo. Modificare la \_ prima colonna del controllo di Dialog2 in un controllo esistente in Dialog2.

Dopo il controllo \_ , le voci successive della tabella dei controlli dal controllo al controllo non rendono un ciclo chiuso in ogni caso. Modificare la colonna del controllo \_ successiva per ControlB in Dialog3 in ControlA.

Dopo il controllo \_ , le voci successive nella tabella dei controlli dal controllo al controllo non restituiscono il controllo iniziale in ogni caso. Modificare la colonna del controllo \_ successiva per controlc in Dialog4 per fare riferimento a ControlA.

Dopo il controllo \_ , le voci successive nella tabella dei controlli dal controllo al controllo non passano attraverso ogni controllo nella finestra di dialogo con una voce nella colonna del controllo \_ successiva. Modificare la colonna del controllo \_ successiva per controlc in Dialog5 in controllo.

Il controllo \_ successivo non fa riferimento a un controllo valido che si trova nella stessa finestra di dialogo del controllo elencato nella colonna del controllo. Modificare la colonna del controllo \_ successiva per controlc in Dialog6 per fare riferimento a controld.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento ghiaccio](ice-reference.md)
</dt> </dl>

 

 



