---
description: ICE31 convalida tutti gli stili di carattere predefiniti usati nei controlli che visualizzano il testo. Consente inoltre di verificare che la proprietà DefaultUIFont faccia riferimento a uno stile del tipo di carattere valido.
ms.assetid: 07e60774-0e26-4a50-b818-a8f074512e3e
title: ICE31
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4797d577ceaa2a2b7838f1f03a8577d9a633fb65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232246"
---
# <a name="ice31"></a>ICE31

ICE31 convalida tutti gli stili di carattere predefiniti usati nei [controlli](controls.md) che visualizzano il testo. Consente inoltre di verificare che la proprietà [**DefaultUIFont**](defaultuifont.md) faccia riferimento a uno stile del tipo di carattere valido.

I controlli possono avere uno stile del carattere predefinito, come descritto in [aggiunta di controlli e testo](adding-controls-and-text.md). Per impostare il tipo di carattere e lo stile del carattere di una stringa di testo, anteporre alla stringa dei caratteri visualizzati lo stile { \\ Style} o {&*Style*}. Dove Style è un identificatore elencato nella colonna TextStyle della [tabella TextStyle](textstyle-table.md). Se nessuna di queste è presente, ma la proprietà [**DefaultUIFont**](defaultuifont.md) è definita come uno stile di testo valido, verrà usato tale tipo di carattere.

ICE31 controlla la colonna di testo per ogni controllo nella [tabella dei controlli](control-table.md) per verificare che sia presente una voce valida nella [tabella TextStyle](textstyle-table.md).

ICE31 ignora il [controllo ScrollableText](scrollabletext-control.md).

## <a name="results"></a>Risultati

ICE31 Invia un messaggio di errore per gli stili non definiti, i nomi di stile troppo lunghi, una tabella TextStyle mancante e i tag di stile senza parentesi graffa di chiusura.

ICE31 pubblica un avviso se il tag di stile non si trova all'inizio della riga o se un controllo ha più tag di stile.

## <a name="example"></a>Esempio

ICE31 invia gli errori seguenti per l'esempio illustrato:

-   Il controllo DialogB. Control1 USA undefined TextStyle BadStyle.
-   Il controllo DialogB. Controllo2 USA undefined TextStyle BadStyle.
-   Per il controllo DialogB. Control6 manca la parentesi graffa di chiusura nello stile del testo.
-   Il controllo DialogB. Control3 specifica uno stile del testo troppo lungo per essere valido.

ICE31 invia l'avviso seguente per l'esempio illustrato:

-   Il tag di stile testo in DialogB. Control4 non ha alcun effetto. Si vuole che venga visualizzato come testo?

[Tabella di controllo](control-table.md) (parziale)



| Finestra di dialogo  | Control  | Testo                                                                                                                                                                |
|---------|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Finestra di dialogo | Control0 | { \\ OKStyle} questo è il testo da visualizzare.                                                                                                                             |
| Finestra di dialogo | Control1 | {&OKStyle} Testo da visualizzare.                                                                                                                              |
| DialogB | Control1 | {&BadStyle} Testo da visualizzare.                                                                                                                             |
| DialogB | Controllo2 | { \\ BadStyle} questo è il testo da visualizzare.                                                                                                                            |
| DialogB | Control3 | {&stile costituito da più di 72 caratteri e pertanto non può essere uno stile anche se in qualche modo si è gestito per ottenerlo nella tabella TextStyle} Testo da visualizzare. |
| DialogB | Control4 | Avviso { \\ OKStyle} questo è il testo da visualizzare.                                                                                                                     |
| DialogB | Control5 | { \\ OKStyle} {&OKStyle} questo è il testo da visualizzare.                                                                                                                   |
| DialogB | Control6 | { \\ OKStyle questo è il testo da visualizzare.                                                                                                                             |



 

[Tabella TextStyle](textstyle-table.md) (parziale)



| TextStyle |
|-----------|
| OkStyle   |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento ghiaccio](ice-reference.md)
</dt> </dl>

 

 



