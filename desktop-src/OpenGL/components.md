---
title: Componenti
description: Componenti
ms.assetid: 9fbd957d-ee6b-475f-8a04-51effa206ad5
keywords:
- OpenGL per Windows, componenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c1294745938e245deda8296f2ce4d1df386b9f2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298599"
---
# <a name="components"></a>Componenti

L'implementazione Microsoft di OpenGL in Windows include i componenti seguenti:

-   Set completo di comandi OpenGL correnti

    OpenGL contiene una libreria di funzioni di base per le operazioni di grafica 3D. Queste funzioni di base vengono usate per gestire la descrizione della forma dell'oggetto, la trasformazione della matrice, l'illuminazione, la colorazione, la trama, il ritaglio, le bitmap, la nebbia e l'anti-aliasing. I nomi per queste funzioni principali hanno un prefisso "GL".

    Molti dei comandi di OpenGL hanno diverse varianti, che differiscono per il numero e il tipo dei parametri. Il conteggio di tutte le varianti include più di 300 comandi OpenGL.

-   Libreria dell'utilità OpenGL (GLU)

    Questa libreria di funzioni ausiliarie integra le funzioni di base di OpenGL. I comandi gestiscono supporto per la trama, trasformazione delle coordinate, suddivisione a mosaico del poligono, sfere di rendering, cilindri e dischi, curve e superfici di base non uniforme, NURBS e gestione degli errori.

-   Libreria ausiliaria della Guida per programmatori OpenGL

    Si tratta di una semplice libreria indipendente dalla piattaforma di funzioni per la gestione di Windows, la gestione degli eventi di input, il disegno di oggetti 3D classici, la gestione di un processo in background e l'esecuzione di un programma. Le routine di gestione e input della finestra forniscono un livello di base di funzionalità con cui è possibile iniziare a programmare rapidamente in OpenGL.

    Non utilizzarli, tuttavia, in un'applicazione di produzione. Ecco alcuni motivi per questo avviso:

    -   Il ciclo di messaggi si trova nel codice della libreria.
    -   Non è possibile aggiungere gestori per messaggi WM aggiuntivi \* .
    -   Il supporto per le tavolozze logiche è minimo.

    La libreria viene descritta e usata nella *Guida alla programmazione di OpenGL*.

-   Funzioni WGL

    Questo set di funzioni connette OpenGL al sistema Windows windowing. Le funzioni gestiscono i contesti di rendering, gli elenchi di visualizzazione, le funzioni di estensione e le bitmap dei tipi di carattere. Le funzioni WGL sono analoghe alle estensioni GLX che connettono OpenGL al sistema X Window. I nomi di queste funzioni hanno un prefisso "WGL".

-   Nuove funzioni di Windows per formati pixel e doppio buffering

    Queste funzioni supportano i formati pixel per finestra e il doppio buffer (per le modifiche apportate alle immagini) di Windows. Queste nuove funzioni si applicano solo alle finestre grafiche OpenGL.

 

 




