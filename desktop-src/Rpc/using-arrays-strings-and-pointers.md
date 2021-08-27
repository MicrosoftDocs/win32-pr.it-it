---
title: Uso di matrici, stringhe e puntatori
description: Il programma Doctor (vedere gli esempi \\ rpc doctor in Platform Software Development Kit \\ (SDK)) è un buon esempio di un'applicazione che illustra i compromessi di progettazione relativi agli attributi di matrice \\ e stringa.
ms.assetid: 9aea94a1-ae1f-4bd6-9dd3-146edf0b5fec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8371c9c60f19e6ce59c62da637cbe2e844e919984b9c2c905053b61e6deb251b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010840"
---
# <a name="using-arrays-strings-and-pointers"></a>Uso di matrici, stringhe e puntatori

Il programma Doctor (vedere gli esempi \\ rpc doctor in Platform Software Development Kit \\ (SDK)) è un buon esempio di un'applicazione che illustra i compromessi di progettazione relativi agli attributi di matrice \\ e stringa. Il programma Doctor è una piccola versione di esempio di un programma più noto, Eliza, sviluppato dal ricercatore di intelligenza artificiale Joseph Weizenbaum al MIT negli anni '60. Il programma simula un terapeuta usando semplici criteri di ricerca per rispondere all'input del linguaggio naturale.

Il programma Eliza ha registrato la sessione seguente.



| Utente                                                | Eliza                                                     |
|-----------------------------------------------------|-----------------------------------------------------------|
| Gli uomini sono tutti uguali.                                  | In che modo?                                              |
| Ci stanno sempre insoddendo su qualcosa o altro. | Si può pensare a un esempio specifico?                      |
| Il mio amico mi ha fatto venire qui.               | Il tuo amico ti ha fatto venire qui.                        |
| Dice che sono in stato di depressione per la maggior parte del tempo.             | Sono dispiaciuto sapere che si è in stato di sconforto.                |
| È vero, non sono soddisfatto.                            | Pensi che venire qui ti aiuterà a non essere insoddisfatti? |
| Ho bisogno di aiuto. sembra molto certo.          | Cosa significherebbe per te se ti fosse stato utile?           |
| Forse potrei imparare ad andare d'accordo con mia madre.  | Altre informazioni sulla famiglia.                           |
| Mia madre si occupa di me.                         | Who'altro nella famiglia si occupa di te?                |
| Mio padre.                                          | Tuo padre.                                              |
| Sei come mio padre in qualche modo.                | Quale somiglianza si vede?                              |



 

Il programma Doctor può essere suddiviso in applicazioni lato client e lato server. Il lato client richiede l'input al paziente e visualizza la risposta del medico. Il lato server elabora l'input del paziente e genera la risposta del medico. Questo è un esempio classico di applicazione client-server: il client è responsabile dell'interazione dell'utente mentre il server gestisce il carico di calcolo esteso. Non vengono passati molti dati a e restituiti dalla funzione , ma, poiché i dati possono richiedere una quantità significativa di elaborazione, il server lo elabora.

Il programma Doctor usa una matrice di caratteri per l'input e restituisce un'altra matrice di caratteri come output. La tabella seguente elenca quattro modi per passare matrici di caratteri tra il client e il server e gli attributi e le funzioni necessari per implementare ogni approccio.



| Approccio                       | Attributi o funzioni                                                                                                        |
|--------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| Matrici di caratteri conteggiate       | \[[size \_ è](/windows/desktop/Midl/size-is) \] , length \[ [ \_ è](/windows/desktop/Midl/length-is) \] , \[ [ref](/windows/desktop/Midl/ref)\]                                         |
| Stringhe gestite da stub           | \[[string](/windows/desktop/Midl/string) \] , \[ [ref](/windows/desktop/Midl/ref) \] , [midl user \_ \_ allocate](/windows/desktop/Midl/midl-user-allocate-1) nel server                  |
| Stringhe gestite da stub           | \[[string](/windows/desktop/Midl/string) \] , \[ [unique](/windows/desktop/Midl/unique) \] , [midl user \_ \_ allocate](/windows/desktop/Midl/midl-user-allocate-1) nel client e nel server |
| Funzione che restituisce una stringa | \[[unique](/windows/desktop/Midl/unique)\]                                                                                                     |



 

All'interno dei vincoli associati a queste combinazioni di attributi, esistono modi alternativi per inviare una matrice di caratteri dal client al server e restituire un'altra matrice di caratteri dal server al client.

Negli argomenti seguenti vengono illustrati i compromessi di progettazione tra le diverse interfacce in grado di gestire questi parametri.

-   [Matrici di caratteri conteggiate](counted-character-arrays.md)
-   [Stringhe](strings.md)
-   [Più livelli di puntatori](multiple-levels-of-pointers.md)

 

 