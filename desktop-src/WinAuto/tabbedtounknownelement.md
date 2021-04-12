---
title: TabbedToUnknownElement
description: TabbedToUnknownElement
ms.assetid: B0447B19-E281-4D30-8ED8-FC0EE13571C8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 612476d81779c882eeca807a9c3b82c41594f218
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395678"
---
# <a name="tabbedtounknownelement"></a>TabbedToUnknownElement

## <a name="text"></a>Testo

La tabulazione è stata spostata in un elemento al di fuori dell'HWND di destinazione.

## <a name="type"></a>Tipo

Errore

## <a name="description"></a>Descrizione

Se si utilizza la navigazione da tastiera standard (TAB o MAIUSC + TAB), lo stato attivo viene spostato all'esterno dell'HWND della destinazione di verifica.

AccChecker sposta l'albero degli elementi nell'HWND di primo livello per la destinazione di verifica scelta prima di eseguire qualsiasi attività di verifica. In questo modo si riduce il numero di errori non corretti generati se un HWND scelto per la verifica fa parte di un'area client più complessa.

## <a name="possible-causes"></a>Possibili cause

-   La destinazione di verifica non richiede un'implementazione di tabulazione per fornire funzionalità complete.
-   Interazione dell'utente durante la verifica, ad esempio lo spostare lo stato attivo su un HWND non di destinazione, interferisce con il processo di verifica.

 

 




