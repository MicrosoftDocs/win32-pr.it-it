---
description: Il sistema riduce la finestra principale di un'applicazione (stile sovrapposto) a una finestra ridotta a icona quando l'utente fa clic su Riduci a icona dal menu finestra o l'applicazione chiama la funzione ShowWindow e specifica un valore come SW \_ Riduci a icona.
ms.assetid: a52dba49-e4ec-45e2-a00f-211a58e28773
title: Finestre ridotte a icona
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c792a90dba2526b6d09fabf8281fc74ebfe96667
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103754378"
---
# <a name="minimized-windows"></a>Finestre ridotte a icona

Il sistema riduce la finestra principale di un'applicazione (stile sovrapposto) a una finestra ridotta a icona quando l'utente fa clic su Riduci a icona dal menu finestra o l'applicazione chiama la funzione [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) e specifica un valore come SW \_ Riduci a icona. Per ridurre al minimo una finestra, è possibile velocizzare le prestazioni del sistema riducendo la quantità di lavoro che un'applicazione deve eseguire durante l'aggiornamento della finestra principale.

Per un'applicazione tipica, il sistema disegna un'icona, denominata icona della classe, quando la finestra è ridotta a icona, etichettando l'icona con il nome della finestra. L'icona della classe, un'immagine statica che rappresenta l'applicazione, viene specificata dall'applicazione quando registra la classe della finestra. L'applicazione assegna un handle all'icona della classe al membro **HICON** di [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) prima di chiamare [**registerClass**](/windows/win32/api/winuser/nf-winuser-registerclassa). L'applicazione può usare la funzione [**LoadIcon**](/windows/win32/api/winuser/nf-winuser-loadicona) per recuperare l'handle dell'icona.

 

 
