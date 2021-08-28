---
description: ICE31 convalida tutti gli stili di carattere predefiniti usati nei controlli che visualizzano testo. Verifica inoltre che la proprietà DefaultUIFont faccia riferimento a uno stile di carattere valido.
ms.assetid: 07e60774-0e26-4a50-b818-a8f074512e3e
title: ICE31
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 783c8b842f80707bbd1ca833fbc7ad1f154a47a0d3aa24377ee58a1c6549bf7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119528671"
---
# <a name="ice31"></a>ICE31

ICE31 convalida tutti gli stili di carattere predefiniti usati nei [controlli che](controls.md) visualizzano testo. Verifica inoltre che la proprietà [**DefaultUIFont faccia**](defaultuifont.md) riferimento a uno stile di carattere valido.

I controlli possono avere uno stile di carattere predefinito, come descritto in [Aggiunta di controlli e testo](adding-controls-and-text.md). Per impostare il tipo di carattere e lo stile del carattere di una stringa di testo, antessare alla stringa di caratteri visualizzati { style} o \\ {&*style*}. Dove style è un identificatore elencato nella colonna TextStyle della [tabella TextStyle](textstyle-table.md). Se nessuna di queste proprietà è presente, ma la [**proprietà DefaultUIFont**](defaultuifont.md) è definita come stile di testo valido, verrà usato tale tipo di carattere.

ICE31 controlla la colonna Text per ogni controllo nella tabella [di](control-table.md) controllo per verificare che esista una voce valida nella [tabella TextStyle](textstyle-table.md).

ICE31 ignora il [controllo ScrollableText](scrollabletext-control.md).

## <a name="results"></a>Risultati

ICE31 invia un messaggio di errore per gli stili non definiti, i nomi di stile troppo lunghi, una tabella TextStyle mancante e i tag di stile senza parentesi graffa di chiusura.

ICE31 invia un avviso se il tag di stile non si trova all'inizio della riga o se un controllo ha più tag di stile.

## <a name="example"></a>Esempio

ICE31 registra gli errori seguenti per l'esempio illustrato:

-   Il controllo DialogB.Control1 usa Undefined TextStyle BadStyle.
-   Il controllo DialogB.Control2 usa Undefined TextStyle BadStyle.
-   Controllo DialogB.Control6 mancante parentesi graffa di chiusura nello stile del testo.
-   Control DialogB.Control3 specifica uno stile di testo troppo lungo per essere valido.

ICE31 pubblica l'avviso seguente per l'esempio illustrato:

-   Il tag Stile testo in DialogB.Control4 non ha alcun effetto. Si vuole che venga effettivamente visualizzato come testo?

[Tabella di controllo](control-table.md) (parziale)



| Finestra di dialogo  | Control  | Testo                                                                                                                                                                |
|---------|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Finestra di dialogoA | Controllo0 | { \\ OKStyle}Si tratta del testo da visualizzare.                                                                                                                             |
| Finestra di dialogoA | Control1 | {&OKStyle} Si tratta del testo da visualizzare.                                                                                                                              |
| DialogB | Control1 | {&BadStyle} Si tratta del testo da visualizzare.                                                                                                                             |
| DialogB | Controllo2 | { \\ BadStyle}Si tratta del testo da visualizzare.                                                                                                                            |
| DialogB | Controllo3 | {&style con più di 72 caratteri e pertanto non può essere uno stile anche se in qualche modo è stato possibile ottenerlo nella tabella TextStyle} Si tratta del testo da visualizzare. |
| DialogB | Controllo4 | Avviso { \\ OKStyle}Si tratta del testo da visualizzare.                                                                                                                     |
| DialogB | Controllo5 | { \\ OKStyle}{&OKStyle}Questo è il testo da visualizzare.                                                                                                                   |
| DialogB | Controllo6 | { \\ OKStyle È il testo da visualizzare.                                                                                                                             |



 

[Tabella TextStyle](textstyle-table.md) (parziale)



| TextStyle |
|-----------|
| OkStyle   |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento su ICE](ice-reference.md)
</dt> </dl>

 

 



