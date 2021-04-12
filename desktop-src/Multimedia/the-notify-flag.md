---
title: Flag di notifica
description: Flag di notifica
ms.assetid: ed5dbb0b-ce4d-4bda-8daa-c62cfda717d1
keywords:
- Flag di MCI_NOTIFY
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9093e539becb4ba2f09b48d628a57d8243bd837c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104398984"
---
# <a name="the-notify-flag"></a>Flag di notifica

Il flag di notifica (MCI \_ Notify) indica al dispositivo di inserire un messaggio [**mm MCINOTIFY**](mm-mcinotify.md) quando il dispositivo completa un'azione. L'applicazione deve disporre di una routine della finestra per elaborare il \_ messaggio MCINOTIFY mm affinché la notifica abbia effetto. Un \_ messaggio mm MCINOTIFY indica che l'elaborazione di un comando è stata completata, ma non indica se il comando è stato completato correttamente, non è riuscito oppure è stato sostituito o interrotto.

L'applicazione specifica l'handle per la finestra di destinazione per il messaggio quando emette un comando. Nell'interfaccia della stringa di comando, questo handle è l'ultimo parametro della funzione [**mciSendString**](/previous-versions//dd757161(v=vs.85)) . Nell'interfaccia del messaggio di comando, l'handle viene specificato nella parola di ordine inferiore del membro **dwCallBack** della struttura inviata con il messaggio di comando. (Ogni struttura associata a un messaggio di comando contiene questo membro).

 

 