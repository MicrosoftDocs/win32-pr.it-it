---
description: Ogni volta che un'applicazione crea un controller di dominio e inizia immediatamente a chiamare le funzioni di disegno o di output GDI, sfrutta lo spazio di pagina predefinito per lo spazio del dispositivo e le trasformazioni dello spazio del dispositivo a quelle dell'area client.
ms.assetid: 64465eb4-d23a-44e7-ad0d-060b195d37b3
title: Trasformazioni predefinite
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab5f13c764a92c005fad36c9f2599b99a654284f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978687"
---
# <a name="default-transformations"></a>Trasformazioni predefinite

Ogni volta che un'applicazione crea un controller di dominio e inizia immediatamente a chiamare le funzioni di disegno o di output GDI, sfrutta lo spazio di pagina predefinito per lo spazio del dispositivo e le trasformazioni dello spazio del dispositivo a quelle dell'area client. Non è possibile eseguire una trasformazione dello spazio globale fino a quando l'applicazione non chiama prima la funzione [**SetGraphicsMode**](/windows/desktop/api/Wingdi/nf-wingdi-setgraphicsmode) per impostare la modalità su GM \_ Advanced, quindi chiama la funzione [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) .

L'uso del \_ testo mm (la trasformazione dello spazio della pagina predefinita nella trasformazione dello spazio del dispositivo) comporta un mapping uno-a-uno, ovvero un punto specifico nello spazio della pagina viene mappato allo stesso punto nello spazio del dispositivo. Come indicato in precedenza, questa trasformazione non è specificata da una matrice. Viene invece ottenuto dividendo la larghezza del viewport per la larghezza della finestra e l'altezza del viewport in base all'altezza della finestra. Nel caso predefinito, le dimensioni del viewport sono di 1 pixel per 1 pixel e le dimensioni della finestra sono unità di 1 pagina per unità di 1 pagina.

La trasformazione spazio-dispositivo a dispositivo fisico (area client, desktop o carta stampante) produce sempre un mapping uno-a-uno. ovvero, un'unità nello spazio del dispositivo è sempre equivalente a un'unità nell'area client, sul desktop o in una pagina. L'unico scopo di questa trasformazione è la traduzione; garantisce che l'output venga visualizzato correttamente nella finestra di un'applicazione, indipendentemente dalla posizione in cui tale finestra viene spostata sul desktop.

L'aspetto univoco del testo MM \_ è l'orientamento dell'asse y nello spazio della pagina. Nel \_ testo mm l'asse y positivo si estende verso il basso e l'asse y negativo si estende verso l'alto.

 

 



