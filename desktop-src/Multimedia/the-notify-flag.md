---
title: Flag di notifica
description: Flag di notifica
ms.assetid: ed5dbb0b-ce4d-4bda-8daa-c62cfda717d1
keywords:
- MCI_NOTIFY flag
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbec671a9810d31078eedf9b8557bcdc4fa7c3e82f688b7fd005f85cb4127476
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119688271"
---
# <a name="the-notify-flag"></a>Flag di notifica

Il flag "notify" (NOTIFICA MCI) indica al dispositivo di inviare un messaggio \_ [**MM MCINOTIFY**](mm-mcinotify.md) quando il dispositivo completa un'azione. L'applicazione deve disporre di una procedura finestra per elaborare il messaggio \_ MM MCINOTIFY perché la notifica abbia effetto. Un messaggio MM MCINOTIFY indica che l'elaborazione di un comando è stata completata, ma non indica se il comando è stato completato correttamente, non è riuscito o è stato sostituito o \_ interrotto.

L'applicazione specifica l'handle per la finestra di destinazione per il messaggio quando esegue un comando. Nell'interfaccia della stringa di comando questo handle è l'ultimo parametro della [**funzione mciSendString.**](/previous-versions//dd757161(v=vs.85)) Nell'interfaccia del messaggio di comando l'handle viene specificato nella parola di ordine più basso del membro **dwCallBack** della struttura inviata con il messaggio di comando. Ogni struttura associata a un messaggio di comando contiene questo membro.

 

 