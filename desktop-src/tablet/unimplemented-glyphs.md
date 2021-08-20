---
description: Di seguito è riportato un elenco di glifi di movimento che Microsoft prevede di supportare in futuro come parte del riconoscimento dei movimenti Microsoft.
ms.assetid: 4d504140-ff48-4a07-9bf7-a36913e44426
title: Glifi non implementati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8f3966ef2e4bec268bc4b45b65b6778abd434f4169ec1e2aa971703032f07ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118966710"
---
# <a name="unimplemented-glyphs"></a>Glifi non implementati

Di seguito è riportato un elenco di glifi di movimento che Microsoft prevede di supportare in futuro come parte del riconoscimento *dei movimenti Microsoft.* È in corso un lavoro per garantire che l'accuratezza del riconoscimento per questi glifi sia elevata (per evitare l'attivazione accidentale) e che sia mappata alle operazioni appropriate.

Per garantire la coerenza *dei movimenti usati* per le azioni comuni *tra* le applicazioni, è necessario rispettare i suggerimenti seguenti:

-   *L'azione* è il comportamento semantico suggerito associato al movimento.
-   Per i movimenti con etichetta *Fixed nella* tabella seguente, è consigliabile non modificare il comportamento semantico suggerito. Se un'applicazione non richiede il comportamento semantico specificato, è consigliabile non riutilizzare il movimento per un'altra azione o semantica.
-   È consigliabile associare i comportamenti semantici pertinenti a tutti gli altri movimenti. Questi movimenti sono etichettati come specifici *dell'applicazione.* Per i movimenti che hanno un comportamento semantico suggerito, è consigliabile usare il movimento per la semantica suggerita se la funzionalità corrispondente esiste nell'applicazione.
-   Il punto caldo di un movimento è un punto distintivo nella geometria del movimento. Il punto di accesso rapido può essere usato per determinare dove è stato effettuato il movimento. L'API movimenti consente di determinare il punto di accesso rapido per un determinato movimento. Tuttavia, non tutti i movimenti hanno un punto di accesso specifico che distingue. Per quelli che non hanno un punto ad accesso più caldo distinguibili specifico, il punto iniziale viene segnalato come punto ad accesso più caldo.

> [!Note]  
> Alcuni movimenti hanno un punto di accesso che distingue solo come punto di partenza. Questi valori sono distinti nella tabella .

 



| Nome movimento                      | Azione                                         | Fisso                           | Punto di accesso                                                           |
|-----------------------------------|------------------------------------------------|---------------------------------|---------------------------------------------------------------------|
| Infinito<br/>               | Attivare e disattivare la modalità movimento<br/> | Fisso<br/>                | Punto di partenza<br/>                                           |
| Cross<br/>                  | Elimina<br/>                              | Specifico dell'applicazione<br/> | Intersezione dei tratti<br/>                              |
| Segno di paragrafo<br/>         | Nuovo paragrafo<br/>                       | Fisso<br/>                | Punto di partenza<br/>                                           |
| Sezione<br/>                | Nuova sezione<br/>                         | Fisso<br/>                | Punto di partenza<br/>                                           |
| Proiettile<br/>                 | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Punto di partenza<br/>                                           |
| Punto elenco<br/>           | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Punto di partenza<br/>                                           |
| Scarabocchio<br/>               | Bold<br/>                                | Specifico dell'applicazione<br/> | Punto di partenza<br/>                                           |
| Scambio<br/>                   | Exchange contenuto<br/>                    | Specifico dell'applicazione<br/> | Al centro del tratto verso l'alto<br/>                                  |
| Apertura<br/>                 | Aprire uno spazio tra le parole<br/>         | Specifico dell'applicazione<br/> | Al centro del tratto verso il basso<br/>                                |
| Primo piano<br/>                | Close up extra space (Chiudi spazio aggiuntivo)<br/>                | Specifico dell'applicazione<br/> | Centro dello spazio verticale tra le due parentesi<br/> |
| Rettangolo<br/>              | Seleziona il contenuto incluso<br/>            | Fisso<br/>                | Punto di partenza<br/>                                           |
| Tocco circolare<br/>             | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Tocco<br/>                                                      |
| Cerchio-cerchio<br/>          | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Punto di partenza<br/>                                           |
| Cerchio incrociato<br/>           | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Punto di partenza<br/>                                           |
| Linea-cerchio-verticale<br/>   | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Punto di partenza<br/>                                           |
| Linea circolare orizzontale<br/> | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Punto di partenza<br/>                                           |
| Doppia freccia verso l'alto<br/>        | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Apice della freccia<br/>                                   |
| Doppia freccia verso il basso<br/>      | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Apice della freccia<br/>                                   |
| Doppia freccia a sinistra<br/>      | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Apice della freccia<br/>                                   |
| Doppia freccia destra<br/>     | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Apice della freccia<br/>                                   |
| Freccia SU-sinistra<br/>          | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Apice della freccia<br/>                                   |
| Freccia SU-destra<br/>         | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Apice della freccia<br/>                                   |
| Freccia GIÙ-sinistra<br/>        | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Apice della freccia<br/>                                   |
| Freccia GIÙ-destra<br/>       | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Apice della freccia<br/>                                   |
| Freccia sinistra-su<br/>          | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Apice della freccia<br/>                               |
| Freccia SINISTRA-FRECCIA GIÙ<br/>        | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Apice della freccia<br/>                                   |
| Freccia destra-su<br/>         | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Apice della freccia<br/>                                   |
| Freccia destra-giù<br/>       | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Apice della freccia<br/>                                   |
| Diagonale a sinistra<br/>        | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Punto di partenza<br/>                                           |
| Diagonale a destra<br/>       | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Punto di partenza<br/>                                           |
| Diagonale verso il basso<br/>      | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Punto di partenza<br/>                                           |
| Diagonale a destra<br/>     | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Punto di partenza<br/>                                           |
| Lettera latina-A<br/>         | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Punto di partenza<br/>                                           |
| Latin-Letter-B<br/>         | Bold<br/>                                | Fisso<br/>                | Punto di partenza<br/>                                           |
| Lettera-alfabeto latino-C<br/>         | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Punto di partenza<br/>                                           |
| Latin-Letter-D<br/>         | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Punto di partenza<br/>                                           |
| Latin-Letter-E<br/>         | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Punto di partenza<br/>                                           |
| Lettera-alfabeto latino-F<br/>         | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Punto di partenza<br/>                                           |
| Latin-Letter-G<br/>         | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Punto di partenza<br/>                                           |
| Lettera-alfabeto latino-H<br/>         | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Punto di partenza<br/>                                           |
| Lettera-I latino<br/>         | Corsivo<br/>                              | Specifico dell'applicazione<br/> | Punto di partenza<br/>                                           |
| Lettera-alfabeto latino-J<br/>         | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Punto di partenza<br/>                                           |
| Lettera-alfabeto latino-K<br/>         | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Punto di partenza<br/>                                           |
| Lettera-alfabeto latino-L<br/>         | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Punto di partenza<br/>                                           |
| Latin-Letter-M<br/>         | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Punto di partenza<br/>                                           |
| Lettera-alfabeto latino-N<br/>         | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Punto di partenza<br/>                                           |
| Latin-Letter-O<br/>         | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Punto di partenza<br/>                                           |
| Lettera-alfabeto latino-P<br/>         | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Punto di partenza<br/>                                           |
| Latin-Letter-Q<br/>         | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Punto di partenza<br/>                                           |
| Lettera-alfabeto latino-R<br/>         | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Punto di partenza<br/>                                           |
| Latin-Letter-S<br/>         | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Punto di partenza<br/>                                           |
| Latin-Letter-T<br/>         | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Punto di partenza<br/>                                           |
| Latin-Letter-U<br/>         | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Punto di partenza<br/>                                           |
| Latin-Letter-V<br/>         | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Punto di partenza<br/>                                           |
| Latin-Letter-W<br/>         | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Punto di partenza<br/>                                           |
| Lettera-X latina<br/>         | Taglia<br/>                                 | Specifico dell'applicazione<br/> | Punto di partenza<br/>                                           |
| Latin-Letter-Y<br/>         | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Punto di partenza<br/>                                           |
| Latin-Letter-Z<br/>         | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Punto di partenza<br/>                                           |
| Digit-0<br/>                | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Punto di partenza<br/>                                           |
| Digit-1<br/>                | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Punto di partenza<br/>                                           |
| Digit-2<br/>                | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Punto di partenza<br/>                                           |
| Digit-3<br/>                | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Punto di partenza<br/>                                           |
| Digit-4<br/>                | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Punto di partenza<br/>                                           |
| Digit-5<br/>                | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Punto di partenza<br/>                                           |
| Digit-6<br/>                | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Punto di partenza<br/>                                           |
| Digit-7<br/>                | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Punto di partenza<br/>                                           |
| Digit-8<br/>                | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Punto di partenza<br/>                                           |
| Digit-9<br/>                | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Punto di partenza<br/>                                           |
| Punto interrogativo<br/>          | Help<br/>                                | Fisso<br/>                | Centrare lungo l'altezza della curva<br/>                     |
| Affilato<br/>                  | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Punto di partenza<br/>                                           |
| Dollaro<br/>                 | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Punto di partenza<br/>                                           |
| Asterisco<br/>               | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Center<br/>                                                   |
| Plus<br/>                   | Incolla<br/>                               | Fisso<br/>                | Intersezione dei tratti<br/>                              |
| Double-up<br/>              | Scorri verso l'alto<br/>                           | Fisso<br/>                | Punto di partenza<br/>                                           |
| Double-down<br/>            | Scorri verso il basso<br/>                         | Fisso<br/>                | Punto di partenza<br/>                                           |
| Doppio sinistro<br/>            | Scorrere verso sinistra<br/>                         | Fisso<br/>                | Punto di partenza<br/>                                           |
| Doppio destro<br/>           | Scorrere verso destra<br/>                        | Fisso<br/>                | Punto di partenza<br/>                                           |
| Triple-up<br/>              | Su di una pagina<br/>                             | Fisso<br/>                | Punto di partenza<br/>                                           |
| Triplo down<br/>            | Giù di una pagina<br/>                           | Fisso<br/>                | Punto di partenza<br/>                                           |
| A sinistra tripla<br/>            | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Punto di partenza<br/>                                           |
| Triplo destro<br/>           | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Punto di partenza<br/>                                           |
| Parentesi quadre<br/>           | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Midpoint<br/>                                                 |
| Parentesi quadre sotto<br/>          | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Midpoint<br/>                                                 |
| Parentesi quadre a sinistra<br/>           | Inizio della selezione<br/>                  | Fisso<br/>                | Midpoint<br/>                                                 |
| Parentesi quadra chiusa<br/>          | Fine della selezione<br/>                    | Fisso<br/>                | Midpoint<br/>                                                 |
| Parentesi graffa<br/>             | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Midpoint<br/>                                                 |
| Parentesi graffa sotto<br/>            | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Midpoint<br/>                                                 |
| Parentesi graffa a sinistra<br/>             | Inizio della selezione discontinua<br/>    | Fisso<br/>                | Midpoint<br/>                                                 |
| Parentesi graffa destra<br/>            | Fine della selezione discontinua<br/>      | Fisso<br/>                | Midpoint<br/>                                                 |
| Triplo tocco<br/>             | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Il punto di partenza è la distinzione del punto caldo<br/>               |
| Tocco quadruplo<br/>          | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Il punto di partenza è la distinzione del punto caldo<br/>               |



 

 

 




