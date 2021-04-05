---
title: Servizi di autorizzazione
description: Un servizio di autorizzazione è il metodo utilizzato dal provider di servizi condivisi per autorizzare l'accesso a una procedura remota. Gli SSP possono fornire più di un servizio di autorizzazione. Tuttavia, in genere ne selezionano uno come valore predefinito.
ms.assetid: 5ea3cde9-96e9-4208-bb61-d0f98f23b90c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 548f834c69726425a52a033e0dbb08bf6f1f3a38
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045024"
---
# <a name="authorization-services"></a>Servizi di autorizzazione

Un servizio di autorizzazione è il metodo utilizzato dal provider di servizi condivisi per autorizzare l'accesso a una procedura remota. Gli SSP possono fornire più di un servizio di autorizzazione. Tuttavia, in genere ne selezionano uno come valore predefinito.

L'applicazione può usare il metodo di autorizzazione predefinito per il provider di servizi condivisi corrente oppure può specificarne uno. Attualmente, Microsoft RPC supporta due metodi di autorizzazione. Uno riguarda il server per fornire l'autorizzazione in base al nome del programma client. L'altro è che il server confronti le credenziali di autenticazione del client con l'elenco di controllo di accesso (ACL) del server.

Per un elenco di servizi di autorizzazione, vedere [costanti del servizio di autorizzazione](authorization-service-constants.md).

> [!Note]  
> Si consiglia agli sviluppatori di usare RPC \_ C \_ AUTHZ \_ None.

 

 

 




