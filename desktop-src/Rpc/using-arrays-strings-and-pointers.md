---
title: Utilizzo di matrici, stringhe e puntatori
description: Il programma Doctor (vedere \\ Samples \\ RPC \\ Doctor in the Platform Software Development Kit (SDK)) è un valido esempio di applicazione che illustra i compromessi di progettazione necessari per gli attributi di matrice e stringa.
ms.assetid: 9aea94a1-ae1f-4bd6-9dd3-146edf0b5fec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 542a174b9ffd742ecf88de7231449a780be8dca9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104117874"
---
# <a name="using-arrays-strings-and-pointers"></a>Utilizzo di matrici, stringhe e puntatori

Il programma Doctor (vedere \\ Samples \\ RPC \\ Doctor in the Platform Software Development Kit (SDK)) è un valido esempio di applicazione che illustra i compromessi di progettazione necessari per gli attributi di matrice e stringa. Il programma Doctor è una piccola versione di esempio di un programma migliore, Eliza, sviluppato da Artificial Intelligence Researcher Joseph Weizenbaum presso MIT negli anni sessanta. Il programma simula un terapeuta usando semplici criteri di ricerca per rispondere all'input del linguaggio naturale.

Il programma Eliza ha registrato la sessione seguente.



| User                                                | Eliza                                                     |
|-----------------------------------------------------|-----------------------------------------------------------|
| Gli uomini sono tutti uguali.                                  | In che modo?                                              |
| Si tratta sempre di un problema. | Si può pensare a un esempio specifico?                      |
| Il mio fidanzato mi ha fatto andare qui.               | Il tuo fidanzato ti ha reso disponibile.                        |
| Dice che la maggior parte del tempo.             | Sono spiacenti di aver sentito che si è depressi.                |
| È vero, sono infelice.                            | Pensiamo che ci consentirà di non essere felici? |
| Ho bisogno di aiuto; sembra certo.          | Che cosa significa se si ha un aiuto?           |
| Forse ho imparato a usare la mia madre.  | Ulteriori informazioni sulla famiglia.                           |
| Mia madre mi occupa di me.                         | Quali altri utenti della famiglia si occupano dell'utente?                |
| Mio padre.                                          | Il padre.                                              |
| Il mio padre è in qualche modo.                | Qual è la somiglianza visualizzata?                              |



 

Il programma Doctor può essere suddiviso in applicazioni lato client e lato server. Il lato client richiede al paziente l'input e visualizza la risposta del medico. Il lato server elabora l'input del paziente e genera la risposta del medico. Si tratta di un esempio classico di applicazione client-server: il client è responsabile dell'interazione dell'utente mentre il server gestisce il carico computazionale esteso. I dati non vengono passati e restituiti dalla funzione, ma poiché i dati possono richiedere una quantità significativa di elaborazione, il server lo elabora.

Il programma Doctor usa una matrice di caratteri per l'input e restituisce un'altra matrice di caratteri come output. La tabella seguente elenca quattro modi per passare matrici di caratteri tra il client e il server e gli attributi e le funzioni necessari per implementare ogni approccio.



| Approccio                       | Attributi o funzioni                                                                                                        |
|--------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| Matrici di caratteri conteggiate       | \[[size \_ è](/windows/desktop/Midl/size-is) \] , \[ [length \_ è](/windows/desktop/Midl/length-is) \] , \[ [ref](/windows/desktop/Midl/ref)\]                                         |
| Stringhe gestite da Stub           | \[[String](/windows/desktop/Midl/string) \] , \[ [ref](/windows/desktop/Midl/ref) \] , [MIDL \_ User \_ allocate](/windows/desktop/Midl/midl-user-allocate-1) nel server                  |
| Stringhe gestite da Stub           | \[[stringa](/windows/desktop/Midl/string) \] , \[ [univoco](/windows/desktop/Midl/unique) \] , [ \_ utente MIDL \_ allocato](/windows/desktop/Midl/midl-user-allocate-1) su client e server |
| Funzione che restituisce una stringa | \[[univoco](/windows/desktop/Midl/unique)\]                                                                                                     |



 

All'interno dei vincoli associati a queste combinazioni di attributi, esistono modi alternativi di inviare una matrice di caratteri da client a server e di restituire un'altra matrice di caratteri da server a client.

Negli argomenti seguenti vengono illustrati i compromessi di progettazione tra le varie interfacce che possono gestire questi parametri.

-   [Matrici di caratteri conteggiate](counted-character-arrays.md)
-   [Stringhe](strings.md)
-   [Più livelli di puntatori](multiple-levels-of-pointers.md)

 

 