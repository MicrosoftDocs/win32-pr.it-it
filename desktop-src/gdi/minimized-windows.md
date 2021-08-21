---
description: Il sistema riduce la finestra principale di un'applicazione (stile sovrapposto) a una finestra ridotta a icona quando l'utente fa clic su Riduci a icona dal menu della finestra o l'applicazione chiama la funzione ShowWindow e specifica un valore come SW \_ MINIMIZE.
ms.assetid: a52dba49-e4ec-45e2-a00f-211a58e28773
title: Riduzione a icona Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d9633c3bcba452e4708c6a48557fe547eff03c4e2a6801e3669da2faa768272
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118760031"
---
# <a name="minimized-windows"></a>Riduzione a icona Windows

Il sistema riduce la finestra principale di un'applicazione (stile sovrapposto) a una finestra ridotta a icona quando l'utente fa clic su Riduci a icona dal menu della finestra o l'applicazione chiama la funzione [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) e specifica un valore come SW \_ MINIMIZE. La riduzione al minimo di una finestra consente di velocizzare le prestazioni del sistema riducendo la quantità di lavoro che un'applicazione deve eseguire durante l'aggiornamento della finestra principale.

Per un'applicazione tipica, il sistema disegna un'icona, denominata icona della classe, quando la finestra è ridotta a icona, etichettando l'icona con il nome della finestra. L'icona della classe, un'immagine statica che rappresenta l'applicazione, viene specificata dall'applicazione quando registra la classe della finestra. L'applicazione assegna un handle all'icona della classe al membro **hIcon** di [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) prima di [**chiamare RegisterClass**](/windows/win32/api/winuser/nf-winuser-registerclassa). L'applicazione può usare la [**funzione LoadIcon**](/windows/win32/api/winuser/nf-winuser-loadicona) per recuperare l'handle dell'icona.

 

 
