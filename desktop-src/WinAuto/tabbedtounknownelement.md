---
title: TabbedToUnknownElement
description: TabbedToUnknownElement
ms.assetid: B0447B19-E281-4D30-8ED8-FC0EE13571C8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5acee341066ee5a456d412554ead3342c8513ae89e50a056a2372a291b0a88b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052399"
---
# <a name="tabbedtounknownelement"></a>TabbedToUnknownElement

## <a name="text"></a>Testo

La tabulazione è passata a un elemento esterno all'hwnd di destinazione.

## <a name="type"></a>Tipo

Errore

## <a name="description"></a>Descrizione

L'uso della navigazione da tastiera standard (TAB o MAIUSC+TAB) determina lo spostamento dello stato attivo all'esterno dell'HWND della destinazione di verifica.

AccChecker sposta l'albero degli elementi verso l'HWND di primo livello per la destinazione di verifica scelta prima di eseguire qualsiasi attività di verifica. In questo modo si riduce il numero di errori spuri generati se un HWND scelto per la verifica fa parte di un'area client più complessa.

## <a name="possible-causes"></a>Possibili cause

-   La destinazione della verifica non richiede un'implementazione di tabulazione per fornire funzionalità complete.
-   L'interazione dell'utente durante la verifica, ad esempio lo spostamento dello stato attivo su un HWND non di destinazione, ha interferito con il processo di verifica.

 

 




