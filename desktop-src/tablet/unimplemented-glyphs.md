---
description: Di seguito è riportato un elenco di glifi di movimento che Microsoft prevede di supportare in futuro come parte del riconoscimento di movimento Microsoft.
ms.assetid: 4d504140-ff48-4a07-9bf7-a36913e44426
title: Glifi non implementati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90d479c6f3b486706b9e8d063ae2bc46daf5a0a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226048"
---
# <a name="unimplemented-glyphs"></a>Glifi non implementati

Di seguito è riportato un elenco di glifi di movimento che Microsoft prevede di supportare in futuro come parte del *riconoscimento di movimento Microsoft*. Il lavoro è in corso per garantire che l'accuratezza del riconoscimento per questi glifi sia elevata (per evitare l'attivazione accidentale) e che venga eseguito il mapping alle operazioni appropriate.

Per garantire la coerenza dei *movimenti* utilizzati per le *azioni* comuni tra le applicazioni, è necessario attenersi ai suggerimenti seguenti:

-   L' *azione* è il comportamento semantico suggerito associato al movimento.
-   Per i movimenti etichettati come *fixed* nella tabella seguente, è consigliabile non modificare il comportamento semantico suggerito. Se un'applicazione non ha bisogno del comportamento semantico specificato, è consigliabile non riutilizzare il movimento per un'altra azione o semantica.
-   È possibile associare i comportamenti semantici pertinenti a tutti gli altri movimenti. Questi movimenti sono contrassegnati come *specifici dell'applicazione*. Per i movimenti che presentano un comportamento semantico suggerito, è consigliabile usare il gesto per la semantica suggerita se la funzionalità corrispondente esiste nell'applicazione.
-   Il punto critico di un gesto è un punto di distinzione nella geometria del movimento. Il punto critico può essere utilizzato per determinare dove è stato eseguito il movimento. L'API gestures consente di determinare il punto critico per un determinato movimento. Tuttavia, non tutti i movimenti hanno un punto critico distintivo specifico. Per coloro che non hanno un punto critico distintivo specifico, il punto iniziale viene segnalato come punto critico.

> [!Note]  
> Alcuni movimenti hanno un punto critico distintivo che è semplicemente il punto di partenza. Questi sono distinti nella tabella.

 



| Nome movimento                      | Azione                                         | Fisso                           | Punto critico                                                           |
|-----------------------------------|------------------------------------------------|---------------------------------|---------------------------------------------------------------------|
| Infinito<br/>               | Attivare e disattivare la modalità di movimento<br/> | Fisso<br/>                | Punto di partenza<br/>                                           |
| Cross<br/>                  | Delete<br/>                              | Specifico dell'applicazione<br/> | Intersezione dei tratti<br/>                              |
| Segno di paragrafo<br/>         | Nuovo paragrafo<br/>                       | Fisso<br/>                | Punto di partenza<br/>                                           |
| Sezione<br/>                | Nuova sezione<br/>                         | Fisso<br/>                | Punto di partenza<br/>                                           |
| Punto elenco<br/>                 | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Punto di partenza<br/>                                           |
| Bullet-Cross<br/>           | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Punto di partenza<br/>                                           |
| Zigzag<br/>               | Grassetto<br/>                                | Specifico dell'applicazione<br/> | Punto di partenza<br/>                                           |
| Scambio<br/>                   | Contenuto di Exchange<br/>                    | Specifico dell'applicazione<br/> | Al centro del tratto verso l'alto<br/>                                  |
| OpenUP<br/>                 | Apri spazio tra le parole<br/>         | Specifico dell'applicazione<br/> | Al centro del tratto verso il basso<br/>                                |
| Closeup<br/>                | Chiudi spazio aggiuntivo<br/>                | Specifico dell'applicazione<br/> | Al centro dello spazio verticale tra le due parentesi<br/> |
| Rettangolo<br/>              | Seleziona contenuto incluso<br/>            | Fisso<br/>                | Punto di partenza<br/>                                           |
| Toccare il cerchio<br/>             | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Tocco<br/>                                                      |
| Cerchio cerchio<br/>          | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Punto di partenza<br/>                                           |
| Cerchio incrociato<br/>           | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Punto di partenza<br/>                                           |
| Cerchio-linea-verticale<br/>   | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Punto di partenza<br/>                                           |
| Cerchio-linea-orizzontale<br/> | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Punto di partenza<br/>                                           |
| Doppia freccia su<br/>        | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Vertice dell'intestazione della freccia<br/>                                   |
| Doppia freccia giù<br/>      | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Vertice dell'intestazione della freccia<br/>                                   |
| Doppia freccia sinistra<br/>      | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Vertice dell'intestazione della freccia<br/>                                   |
| Doppia freccia a destra<br/>     | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Vertice dell'intestazione della freccia<br/>                                   |
| Freccia su-sinistra<br/>          | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Vertice dell'intestazione della freccia<br/>                                   |
| Freccia su-destra<br/>         | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Vertice dell'intestazione della freccia<br/>                                   |
| Freccia giù-sinistra<br/>        | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Vertice dell'intestazione della freccia<br/>                                   |
| Freccia giù-destra<br/>       | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Vertice dell'intestazione della freccia<br/>                                   |
| Freccia a sinistra<br/>          | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Vertice dell'intestazione della freccia<br/>                               |
| Freccia a sinistra<br/>        | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Vertice dell'intestazione della freccia<br/>                                   |
| Freccia a destra<br/>         | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Vertice dell'intestazione della freccia<br/>                                   |
| Freccia a destra<br/>       | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Vertice dell'intestazione della freccia<br/>                                   |
| Diagonale-leftup<br/>        | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Punto di partenza<br/>                                           |
| Diagonale-rightup<br/>       | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Punto di partenza<br/>                                           |
| Diagonale-Leftdown<br/>      | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Punto di partenza<br/>                                           |
| Diagonale-Rightdown<br/>     | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Punto di partenza<br/>                                           |
| Alfabeto latino-A<br/>         | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Punto di partenza<br/>                                           |
| Alfabeto latino-B<br/>         | Grassetto<br/>                                | Fisso<br/>                | Punto di partenza<br/>                                           |
| Alfabeto latino-C<br/>         | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Punto di partenza<br/>                                           |
| Latino-lettera-D<br/>         | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Punto di partenza<br/>                                           |
| Alfabeto latino-E<br/>         | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Punto di partenza<br/>                                           |
| Lettera latina-F<br/>         | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Punto di partenza<br/>                                           |
| Alfabeto latino<br/>         | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Punto di partenza<br/>                                           |
| Latino-lettera-H<br/>         | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Punto di partenza<br/>                                           |
| Alfabeto latino<br/>         | Corsivo<br/>                              | Specifico dell'applicazione<br/> | Punto di partenza<br/>                                           |
| Lettera latina-J<br/>         | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Punto di partenza<br/>                                           |
| Lettera latina-K<br/>         | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Punto di partenza<br/>                                           |
| Lettera latina-L<br/>         | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Punto di partenza<br/>                                           |
| Alfabeto latino-M<br/>         | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Punto di partenza<br/>                                           |
| Lettera latina-N<br/>         | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Punto di partenza<br/>                                           |
| Alfabeto latino<br/>         | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Punto di partenza<br/>                                           |
| Lettera latina-P<br/>         | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Punto di partenza<br/>                                           |
| Lettera latina-Q<br/>         | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Punto di partenza<br/>                                           |
| Alfabeto latino-R<br/>         | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Punto di partenza<br/>                                           |
| Alfabeto latino<br/>         | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Punto di partenza<br/>                                           |
| Lettera latina-T<br/>         | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Punto di partenza<br/>                                           |
| Alfabeto latino-U<br/>         | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Punto di partenza<br/>                                           |
| Alfabeto latino-V<br/>         | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Punto di partenza<br/>                                           |
| Latino-lettera-W<br/>         | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Punto di partenza<br/>                                           |
| Lettera latina-X<br/>         | Taglia<br/>                                 | Specifico dell'applicazione<br/> | Punto di partenza<br/>                                           |
| Lettera latina-Y<br/>         | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Punto di partenza<br/>                                           |
| Alfabeto latino-Z<br/>         | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Punto di partenza<br/>                                           |
| Digit-0<br/>                | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Punto di partenza<br/>                                           |
| Digit-1<br/>                | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Punto di partenza<br/>                                           |
| Cifra-2<br/>                | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Punto di partenza<br/>                                           |
| Digit-3<br/>                | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Punto di partenza<br/>                                           |
| Digit-4<br/>                | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Punto di partenza<br/>                                           |
| Digit-5<br/>                | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Punto di partenza<br/>                                           |
| Digit-6<br/>                | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Punto di partenza<br/>                                           |
| Digit-7<br/>                | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Punto di partenza<br/>                                           |
| Digit-8<br/>                | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Punto di partenza<br/>                                           |
| Digit-9<br/>                | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Punto di partenza<br/>                                           |
| Punto interrogativo<br/>          | Help<br/>                                | Fisso<br/>                | Centra lungo l'altezza della curva<br/>                     |
| Sharp<br/>                  | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Punto di partenza<br/>                                           |
| Dollaro<br/>                 | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Punto di partenza<br/>                                           |
| Asterisco<br/>               | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Center<br/>                                                   |
| Plus<br/>                   | Incolla<br/>                               | Fisso<br/>                | Intersezione dei tratti<br/>                              |
| Doppio<br/>              | Scorri verso l'alto<br/>                           | Fisso<br/>                | Punto di partenza<br/>                                           |
| Doppio<br/>            | Scorri verso il basso<br/>                         | Fisso<br/>                | Punto di partenza<br/>                                           |
| Doppio sinistro<br/>            | Scorrimento a sinistra<br/>                         | Fisso<br/>                | Punto di partenza<br/>                                           |
| Doppio a destra<br/>           | Scorri a destra<br/>                        | Fisso<br/>                | Punto di partenza<br/>                                           |
| Tripla<br/>              | Su di una pagina<br/>                             | Fisso<br/>                | Punto di partenza<br/>                                           |
| Tripla<br/>            | Giù di una pagina<br/>                           | Fisso<br/>                | Punto di partenza<br/>                                           |
| Tripla sinistra<br/>            | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Punto di partenza<br/>                                           |
| Tripla a destra<br/>           | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Punto di partenza<br/>                                           |
| Parentesi quadre<br/>           | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Midpoint<br/>                                                 |
| Tra parentesi quadre<br/>          | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Midpoint<br/>                                                 |
| Parentesi quadra a sinistra<br/>           | Inizio selezione<br/>                  | Fisso<br/>                | Midpoint<br/>                                                 |
| Parentesi quadra a destra<br/>          | Fine della selezione<br/>                    | Fisso<br/>                | Midpoint<br/>                                                 |
| Parentesi graffa sopra<br/>             | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Midpoint<br/>                                                 |
| Parentesi graffa-sotto<br/>            | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Midpoint<br/>                                                 |
| Parentesi graffa sinistra<br/>             | Inizio della selezione discontinui<br/>    | Fisso<br/>                | Midpoint<br/>                                                 |
| Parentesi graffa destra<br/>            | Fine della selezione discontinua<br/>      | Fisso<br/>                | Midpoint<br/>                                                 |
| Triple-Tap<br/>             | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Il punto di partenza sta distinguendo il punto critico<br/>               |
| Quadruplo-tocco<br/>          | Specifico dell'applicazione<br/>                | Specifico dell'applicazione<br/> | Il punto di partenza sta distinguendo il punto critico<br/>               |



 

 

 




