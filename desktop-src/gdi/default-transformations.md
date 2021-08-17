---
description: Ogni volta che un'applicazione crea un controller di dominio e inizia immediatamente a chiamare le funzioni di disegno o output GDI, sfrutta lo spazio di pagina predefinito per le trasformazioni device-space e device-space per l'area client.
ms.assetid: 64465eb4-d23a-44e7-ad0d-060b195d37b3
title: Trasformazioni predefinite
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ba34effd9d6d43ab3b0abc740250c58788a8ce2f1556e89c92b78af823e58c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119469681"
---
# <a name="default-transformations"></a>Trasformazioni predefinite

Ogni volta che un'applicazione crea un controller di dominio e inizia immediatamente a chiamare le funzioni di disegno o output GDI, sfrutta lo spazio di pagina predefinito per le trasformazioni device-space e device-space per l'area client. Non è possibile eseguire una trasformazione dello spazio da mondo a pagina finché l'applicazione non chiama prima la [**funzione SetGraphicsMode**](/windows/desktop/api/Wingdi/nf-wingdi-setgraphicsmode) per impostare la modalità su GM ADVANCED e quindi chiama la \_ funzione [**SetWorldTransform.**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform)

L'uso di MM TEXT (la trasformazione spazio pagina predefinita per lo spazio del dispositivo) comporta un mapping uno-a-uno, ovvero un determinato punto nello spazio della pagina viene mappato allo stesso punto nello spazio del \_ dispositivo. Come accennato in precedenza, questa trasformazione non viene specificata da una matrice. Viene invece ottenuto dividendo la larghezza del viewport per la larghezza della finestra e l'altezza del viewport per l'altezza della finestra. Nel caso predefinito, le dimensioni del viewport sono di 1 pixel per 1 pixel e le dimensioni della finestra sono unità di 1 pagina per unità di 1 pagina.

La trasformazione da spazio dispositivo a dispositivo fisico (area client, desktop o stampante) comporta sempre un mapping uno-a-uno; in altri, un'unità nello spazio del dispositivo equivale sempre a un'unità nell'area client, sul desktop o in una pagina. L'unico scopo di questa trasformazione è la traduzione; assicura che l'output venga visualizzato correttamente nella finestra di un'applicazione, indipendentemente dalla posizione in cui tale finestra viene spostata sul desktop.

L'unico aspetto univoco di MM \_ TEXT è l'orientamento dell'asse y nello spazio della pagina. In MM \_ TEXT l'asse y positivo si estende verso il basso e l'asse y negativo si estende verso l'alto.

 

 



