---
description: Il sistema modifica le dimensioni di una finestra quando l'utente sceglie i comandi di menu della finestra, ad esempio Dimensioni e Ingrandisci, o quando l'applicazione chiama funzioni, ad esempio la funzione SetWindowPos.
ms.assetid: 6f997cba-e4c9-4e27-8309-42b9892ec620
title: Ridimensionato Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9efd6f71d1657c0d01b3df9101fc15fa35f54ecfc01b1588b696cd9110dad317
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119602721"
---
# <a name="resized-windows"></a>Ridimensionato Windows

Il sistema modifica le dimensioni di una finestra quando l'utente sceglie i comandi di menu della finestra, ad esempio Dimensioni e Ingrandisci, o quando l'applicazione chiama funzioni, ad esempio la [**funzione SetWindowPos.**](/windows/win32/api/winuser/nf-winuser-setwindowpos) Quando le dimensioni di una finestra cambiano, il sistema presuppone che il contenuto della parte esposta in precedenza della finestra non sia interessato e non deve essere ridisegnato. Il sistema invalida solo la parte appena esposta della finestra, risparmiando tempo quando l'eventuale messaggio [**WM \_ PAINT**](wm-paint.md) viene elaborato dall'applicazione. In questo caso, **WM \_ PAINT** non viene generato quando le dimensioni della finestra vengono ridotte.

Per alcune finestre, qualsiasi modifica apportata alle dimensioni della finestra invalida il contenuto. Ad esempio, un'applicazione di clock che adatta il viso dell'orologio per adattarsi perfettamente all'interno della finestra deve ridisegnare l'orologio ogni volta che le dimensioni della finestra cambiano. Per forzare il sistema a invalidare l'intera area client della finestra quando viene apportata una modifica verticale, orizzontale o verticale e orizzontale, un'applicazione deve specificare lo stile \_ CS VREDRAW o CS HREDRAW o entrambi durante la registrazione della classe \_ della finestra. Qualsiasi finestra appartenente a una classe finestra con questi stili viene invalidata ogni volta che l'utente o l'applicazione modifica le dimensioni della finestra.

 

 
