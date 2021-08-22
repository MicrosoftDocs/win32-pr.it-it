---
description: Alcune applicazioni devono ricevere una notifica degli eventi di connessione, prima dell'evento, subito dopo che si verifica o entrambi. È possibile creare una DLL per ricevere la notifica anticipata e dopo il fatto degli eventi di connessione.
ms.assetid: 692eb8f2-1c53-4535-b44d-babb30eecd9c
title: Ricezione di notifiche di connessione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3a581855ef134536df8c4c728521e796e541c963a780e2f572ad88dc704c677
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118919690"
---
# <a name="receiving-connection-notifications"></a>Ricezione di notifiche di connessione

Alcune applicazioni devono ricevere una notifica degli eventi di connessione, prima dell'evento, subito dopo che si verifica o entrambi. È possibile creare una DLL per ricevere la notifica anticipata e dopo il fatto degli eventi di connessione.

Un esempio di un'applicazione che deve ricevere una notifica anticipata di un evento di connessione è il servizio di accesso remoto (RAS). RAS deve essere informato prima di stabilire una connessione perché potrebbe essere necessario stabilire una connessione modem prima di stabilire la connessione di rete.

Analogamente, le applicazioni potrebbero dover pulire le risorse dopo la connessione, quindi richiedere una notifica post-connessione.

Le applicazioni interessate a ricevere notifiche avanzate e dopo il fatto degli eventi di connessione devono fornire una DLL che esporta due funzioni, [**AddConnectNotify**](/windows/desktop/api/Npapi/nf-npapi-addconnectnotify) [**e CancelConnectNotify.**](/windows/desktop/api/Npapi/nf-npapi-cancelconnectnotify)

Dopo aver implementato queste funzioni, è necessario registrare la DLL come descritto in [Registrazione per ricevere notifiche di connessione](registering-to-receive-connection-notifications.md).

 

 



