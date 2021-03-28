---
description: L'area di aggiornamento identifica la parte di una finestra non aggiornata o non valida e che deve essere ridisegnata.
ms.assetid: 21228620-9491-4e1b-8658-15e9605951f2
title: Area di aggiornamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e670bac065782a1e09c4d142f964aaea97d4b96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104995093"
---
# <a name="the-update-region"></a>Area di aggiornamento

L' *area di aggiornamento* identifica la parte di una finestra non aggiornata o non valida e che deve essere ridisegnata. Il sistema usa l'area di aggiornamento per generare messaggi di [**\_ disegno WM**](wm-paint.md) per le applicazioni e per ridurre al minimo il tempo impiegato dalle applicazioni per rendere aggiornato il contenuto delle finestre. Il sistema aggiunge solo la parte non valida della finestra all'area di aggiornamento, richiedendo la traccia solo di tale parte.

Quando il sistema determina che è necessario aggiornare una finestra, imposta le dimensioni dell'area di aggiornamento sulla parte non valida della finestra. L'impostazione dell'area di aggiornamento non comporta immediatamente il progetto dell'applicazione. Al contrario, l'applicazione continua a recuperare i messaggi dalla coda di messaggi dell'applicazione fino a quando non restano messaggi. Il sistema controlla quindi l'area di aggiornamento e, se l'area non è vuota (non NULL), invia un messaggio [**di \_ disegno WM**](wm-paint.md) alla routine della finestra.

Un'applicazione può usare l'area di aggiornamento per generare i messaggi di [**\_ disegno WM**](wm-paint.md) . Ad esempio, un'applicazione che carica i dati da file aperti in genere imposta l'area di aggiornamento durante il caricamento in modo da disegnare nuovi dati durante l'elaborazione del messaggio di **\_ disegno WM** successivo. In generale, un'applicazione non deve attingere al momento della modifica dei dati, ma instradare tutte le operazioni di disegno tramite il messaggio di disegno **WM \_** .

 

 



