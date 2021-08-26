---
title: Componenti
description: Componenti
ms.assetid: 9fbd957d-ee6b-475f-8a04-51effa206ad5
keywords:
- OpenGL in Windows,componenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c11c8d23130393102f39b716e16c0a6433a40122ad176a525b40e2e1a21b0360
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119868781"
---
# <a name="components"></a>Componenti

L'implementazione microsoft di OpenGL in Windows include i componenti seguenti:

-   Set completo di comandi OpenGL correnti

    OpenGL contiene una libreria di funzioni di base per operazioni grafiche 3D. Queste funzioni di base vengono usate per gestire la descrizione della forma degli oggetti, la trasformazione della matrice, l'illuminazione, la colorazione, la trama, il ritaglio, le bitmap, la nebbia e l'antialiasing. I nomi per queste funzioni di base hanno un prefisso "gl".

    Molti dei comandi OpenGL hanno diverse varianti, che differiscono per il numero e il tipo dei relativi parametri. Contando tutte le varianti, sono disponibili più di 300 comandi OpenGL.

-   Libreria dell'utilità OpenGL (GLU)

    Questa libreria di funzioni ausiliarie integra le funzioni OpenGL di base. I comandi gestiscono il supporto delle trame, la trasformazione delle coordinate, la tessellazione dei poligoni, le sfera di rendering, i cilindri e i dischi, le curve e le superfici NURBS (Non-Uniform Rational B-Spline) e la gestione degli errori.

-   Libreria ausiliaria della Guida per programmatori OpenGL

    Si tratta di una libreria semplice e indipendente dalla piattaforma di funzioni per la gestione delle finestre, la gestione degli eventi di input, il disegno di oggetti 3D classici, la gestione di un processo in background e l'esecuzione di un programma. La gestione delle finestre e le routine di input forniscono un livello di base di funzionalità con cui è possibile iniziare rapidamente a programmare in OpenGL.

    Non usarli, tuttavia, in un'applicazione di produzione. Ecco alcuni motivi per questo avviso:

    -   Il ciclo di messaggi si trova nel codice della libreria.
    -   Non è possibile aggiungere gestori per altri messaggi \* WM.
    -   Il supporto per i palette logici è molto scarso.

    La libreria viene descritta e usata nella Guida *per programmatori OpenGL.*

-   Funzioni WGL

    Questo set di funzioni connette OpenGL al Windows windowing. Le funzioni gestiscono contesti di rendering, elenchi di visualizzazione, funzioni di estensione e bitmap dei tipi di carattere. Le funzioni WGL sono analoghe alle estensioni GLX che connettono OpenGL al sistema X Window. I nomi di queste funzioni hanno un prefisso "wgl".

-   Nuove Windows funzioni per i formati pixel e il doppio buffer

    Queste funzioni supportano i formati pixel per finestra e il doppio buffer (per le modifiche delle immagini uniformi) delle finestre. Queste nuove funzioni si applicano solo alle finestre grafiche OpenGL.

 

 




