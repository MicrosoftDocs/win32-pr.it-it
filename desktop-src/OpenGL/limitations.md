---
title: Limitazioni
description: Limitazioni
ms.assetid: 5f41620d-dde0-4e82-92f0-ada9d4acf127
keywords:
- OpenGL per Windows, limitazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 478a139326f74c236ca0109fddbbc3d4ffb46e1a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709724"
---
# <a name="limitations"></a>Limitazioni

L'implementazione generica presenta le limitazioni seguenti:

-   Stampa.

    È possibile stampare un'immagine OpenGL direttamente in una stampante usando solo i metafile. Per altre informazioni, vedere [stampa di un'immagine OpenGL](printing-an-opengl-image.md).

-   Non è possibile combinare grafica OpenGL e GDI in una finestra con doppio buffer.

    Un'applicazione può creare direttamente grafica OpenGL e grafica GDI in una finestra con singolo buffer, ma non in una finestra con doppio buffer.

-   Non sono disponibili tavolozze dei colori hardware per ogni finestra.

    Windows ha una singola tavolozza dei colori hardware del sistema, applicabile all'intero schermo. Una finestra OpenGL non può avere una propria tavolozza hardware, ma può avere una propria tavolozza logica. A tale scopo, deve diventare un'applicazione in grado di riconoscere la tavolozza. Per ulteriori informazioni, vedere [modalità colori OpenGL e gestione tavolozza di Windows](opengl-color-modes-and-windows-palette-management.md).

-   Non è disponibile alcun supporto diretto per gli appunti, DDE (Dynamic Data Exchange) o OLE.

    Una finestra con grafica OpenGL non supporta direttamente queste funzionalità di Windows. Tuttavia, esistono soluzioni alternative per l'utilizzo degli Appunti. Per altre informazioni, vedere [copia di un'immagine OpenGL negli Appunti](copying-an-opengl-image-to-the-clipboard.md).

-   La libreria di classi di Inventory 2,0 C++ non è inclusa.

    La libreria di classi Inventory basata su OpenGL fornisce costrutti di livello superiore per la programmazione di grafica 3D. Non è incluso nella versione corrente dell'implementazione di Microsoft OpenGL per Windows.

-   Non è disponibile alcun supporto per le funzionalità di formato pixel seguenti: immagini stereoscopiche, alfa bitplane e buffer ausiliari.

    È tuttavia disponibile il supporto per diversi buffer ausiliari, tra cui il buffer dello stencil, il buffer di accumulo, il buffer nascosto (doppio buffer), il buffer del piano sottoposto a sovrapposizione e il buffer di profondità (asse z).

 

 




