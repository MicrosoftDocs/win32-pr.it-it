---
description: Dopo aver creato una DLL per ricevere le notifiche di connessione, è necessario registrarla con il sistema.
ms.assetid: 1a389de1-367d-4b07-a420-4af431d48b7f
title: Registrazione per ricevere notifiche di connessione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe3a25e26e290700b8f343d3d543af4fbd7b709ff8b099522e4cd4b02b3d587f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118919474"
---
# <a name="registering-to-receive-connection-notifications"></a>Registrazione per ricevere notifiche di connessione

Dopo aver creato una DLL per ricevere le notifiche di connessione, è necessario registrarla con il sistema. A tale scopo, aggiungere un **valore \_ REG EXPAND \_ SZ** sotto

**HKEY \_ Local \_ MACHINE** \\ **SYSTEM** \\ **CurrentControlSet** \\ **Control** \\ **NetworkProvider** \\ **Notifyees**

disponga di una chiave. Questo valore specifica il percorso della DLL che implementa l'oggetto [Connection Notification API](connection-notification-api.md).

Il valore può avere qualsiasi nome. Tutti i valori nella **chiave Notifyees** vengono trattati come percorsi di DLL che vengono notificati agli eventi di connessione. È consigliabile usare un nome che identifichi la DLL. In questo modo si verifica un conflitto di nomi con altre applicazioni di notifica della connessione.

Per altre informazioni su come creare un'applicazione che riceve notifiche di connessione, vedere [Ricezione di notifiche di connessione.](receiving-connection-notifications.md)

 

 



