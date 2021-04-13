---
title: Parametro Durata messaggio
description: Le applicazioni utilizzano in genere finestre popup per visualizzare brevemente messaggi di notifica importanti all'utente. Un'applicazione crea la finestra, la Visualizza per una durata definita dall'applicazione, quindi Elimina la finestra.
ms.assetid: a3f7a8d8-78e7-4fb0-8ee2-bd9341857153
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2a99a43ace763da94944da334b0865c768cc920
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399151"
---
# <a name="message-duration-parameter"></a>Parametro Durata messaggio

Le applicazioni utilizzano in genere finestre popup per visualizzare brevemente messaggi di notifica importanti all'utente. Un'applicazione crea la finestra, la Visualizza per una durata definita dall'applicazione, quindi Elimina la finestra.

Poiché gli utenti con condizioni cognitive o di problemi visivi potrebbero avere bisogno di più tempo per leggere i popup delle notifiche, le applicazioni non dovrebbero scrivere codice per la durata. Al contrario, un'applicazione deve impostare la durata in base al valore del parametro di sistema **\_ GETMESSAGEDURATION SPI** . Per recuperare questo parametro, usare la funzione [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) .

Le applicazioni Assistive Technology possono impostare la durata dei messaggi, in base all'input dell'utente, impostando il parametro di sistema **SPI \_ SETMESSAGEDURATION** .

 

 