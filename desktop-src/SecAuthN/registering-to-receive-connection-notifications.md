---
description: Dopo aver creato una DLL per ricevere le notifiche di connessione, è necessario registrarla nel sistema.
ms.assetid: 1a389de1-367d-4b07-a420-4af431d48b7f
title: Registrazione per la ricezione delle notifiche di connessione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 812c47ba43fe13e4908a1812f7c67f38a94bce5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756422"
---
# <a name="registering-to-receive-connection-notifications"></a>Registrazione per la ricezione delle notifiche di connessione

Dopo aver creato una DLL per ricevere le notifiche di connessione, è necessario registrarla nel sistema. A tale scopo, aggiungere un valore **reg \_ expand \_ SZ** sotto il

**HKEY \_ \_** \\  \\  \\  \\  \\ **Avvisi** NetworkProvider del controllo CurrentControlSet del computer locale

disponga di una chiave. Questo valore specifica il percorso della DLL che implementa l' [API di notifica della connessione](connection-notification-api.md).

Il valore può avere qualsiasi nome. Tutti i valori della chiave **notifyd** vengono trattati come percorsi per le dll che ricevono notifiche di eventi di connessione. Si consiglia di usare un nome che identifichi la DLL. In questo modo si riduce la probabilità che si verifichi un conflitto di nomi con altre applicazioni di notifica della connessione.

Per ulteriori informazioni sulla creazione di un'applicazione che riceve le notifiche di connessione, vedere [ricezione di notifiche di connessione](receiving-connection-notifications.md).

 

 



