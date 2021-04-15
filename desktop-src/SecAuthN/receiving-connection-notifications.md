---
description: Per alcune applicazioni è necessario ricevere una notifica degli eventi di connessione, prima dell'evento, subito dopo che si è verificata o entrambi. È possibile creare una DLL per ricevere una notifica avanzata e successiva al fatto degli eventi di connessione.
ms.assetid: 692eb8f2-1c53-4535-b44d-babb30eecd9c
title: Ricezione di notifiche di connessione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c054d4f7bb78f610afe6c1cbdf028416de7b5596
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524876"
---
# <a name="receiving-connection-notifications"></a>Ricezione di notifiche di connessione

Per alcune applicazioni è necessario ricevere una notifica degli eventi di connessione, prima dell'evento, subito dopo che si è verificata o entrambi. È possibile creare una DLL per ricevere una notifica avanzata e successiva al fatto degli eventi di connessione.

Un esempio di applicazione che deve ricevere una notifica di avanzamento di un evento di connessione è il servizio di accesso remoto (RAS). Prima di stabilire una connessione, è necessario informare RAS perché potrebbe essere necessario stabilire una connessione modem prima di effettuare la connessione di rete.

Analogamente, è possibile che le applicazioni debbano pulire le risorse dopo aver effettuato la connessione, richiedendo pertanto una notifica post-connessione.

Le applicazioni interessate a ricevere notifiche avanzate e successive al fatto degli eventi di connessione devono fornire una DLL che esporta due funzioni, [**AddConnectNotify**](/windows/desktop/api/Npapi/nf-npapi-addconnectnotify) e [**CancelConnectNotify**](/windows/desktop/api/Npapi/nf-npapi-cancelconnectnotify).

Dopo aver implementato queste funzioni, è necessario registrare la DLL come descritto in [registrazione per ricevere notifiche di connessione](registering-to-receive-connection-notifications.md).

 

 



