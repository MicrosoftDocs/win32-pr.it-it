---
description: Il sistema modifica la dimensione di una finestra quando l'utente sceglie i comandi del menu finestra, ad esempio dimensioni e Ingrandisci, o quando l'applicazione chiama funzioni, ad esempio la funzione SetWindowPos.
ms.assetid: 6f997cba-e4c9-4e27-8309-42b9892ec620
title: Finestre ridimensionate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88f740191f8b85038f17a687ebc547305f882383
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880270"
---
# <a name="resized-windows"></a>Finestre ridimensionate

Il sistema modifica la dimensione di una finestra quando l'utente sceglie i comandi del menu finestra, ad esempio dimensioni e Ingrandisci, o quando l'applicazione chiama funzioni, ad esempio la funzione [**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos) . Quando le dimensioni di una finestra cambiano, il sistema presuppone che il contenuto della parte esposta in precedenza della finestra non sia interessato e non debba essere ridisegnato. Il sistema invalida solo la parte appena esposta della finestra, che consente di risparmiare tempo quando il messaggio di [**\_ disegno WM**](wm-paint.md) finale viene elaborato dall'applicazione. In questo caso, **la \_ vernice WM** non viene generata quando viene ridotta la dimensione della finestra.

Per alcune finestre, qualsiasi modifica apportata alle dimensioni della finestra invalida il contenuto. Ad esempio, un'applicazione Clock che adatta la faccia del clock a adattarla perfettamente all'interno della finestra deve ricreare il clock ogni volta che la finestra cambia dimensione. Per forzare il sistema a invalidare l'intera area client della finestra quando viene apportata una modifica verticale, orizzontale o verticale e orizzontale, un'applicazione deve specificare lo \_ stile cs VREDRAW o cs \_ HREDRAW, o entrambi, durante la registrazione della classe Window. Qualsiasi finestra appartenente a una classe di finestra con questi stili viene invalidata ogni volta che l'utente o l'applicazione modifica la dimensione della finestra.

 

 
