---
description: L'area di aggiornamento identifica la parte di una finestra non aggiornata o non valida e che deve essere ridisegnata.
ms.assetid: 21228620-9491-4e1b-8658-15e9605951f2
title: Area di aggiornamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d9a8f847a1e2d479200cfe6ea4e60a1b3a8ebf4c02aaf7c89fc719f62d91e91
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119717971"
---
# <a name="the-update-region"></a>Area di aggiornamento

*L'area* di aggiornamento identifica la parte di una finestra non aggiornata o non valida e che deve essere ridisegnata. Il sistema usa l'area di aggiornamento per generare messaggi [**WM \_ PAINT**](wm-paint.md) per le applicazioni e ridurre al minimo il tempo che le applicazioni impiegano per aggiornare il contenuto delle finestre. Il sistema aggiunge solo la parte non valida della finestra all'area di aggiornamento, richiedendo solo tale parte da disegnare.

Quando il sistema determina che una finestra deve essere aggiornata, imposta le dimensioni dell'area di aggiornamento sulla parte non valida della finestra. L'impostazione dell'area di aggiornamento non determina immediatamente il disegno dell'applicazione. L'applicazione continua invece a recuperare i messaggi dalla coda di messaggi dell'applicazione fino a quando non rimane alcun messaggio. Il sistema controlla quindi l'area di aggiornamento e, se l'area non è vuota (non NULL), invia un [**messaggio WM \_ PAINT**](wm-paint.md) alla procedura della finestra.

Un'applicazione può usare l'area di aggiornamento per generare i [**messaggi WM \_ PAINT.**](wm-paint.md) Ad esempio, un'applicazione che carica dati da file aperti imposta in genere l'area di aggiornamento durante il caricamento in modo che i nuovi dati vengono disegnati durante l'elaborazione del messaggio **WM \_ PAINT** successivo. In generale, un'applicazione non deve disegnare al momento della modifica dei dati, ma indirizzare tutte le operazioni di disegno tramite il **messaggio WM \_ PAINT.**

 

 



