---
title: Server-Side registrazione
description: La registrazione lato server è disponibile in un gruppo di URL o in una sessione del server.
ms.assetid: e1fcd87f-382a-42bf-b53f-1e1cb1dbbfc5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db8caf7475fe6d2b408f6e2a1f924bad73df64c315ef5e0acd1c7c317ce5eac6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829841"
---
# <a name="server-side-logging"></a>Server-Side registrazione

La registrazione lato server è disponibile in un gruppo di URL o in una sessione del server. Quando la registrazione è abilitata in una sessione del server, funziona come forma centralizzata di registrazione per tutti i gruppi di URL nella sessione del server. Quando la registrazione è abilitata in un gruppo di URL, la registrazione viene eseguita solo sulle richieste indirizzate al gruppo di URL. L'API server HTTP supporta i tipi di registrazione seguenti:

-   [Registrazione W3C:](w3c-logging.md)disponibile nella sessione del server e nel gruppo di URL.
-   [Registrazione NCSA:](ncsa-logging.md)disponibile nel gruppo di URL.
-   [Registrazione IIS:](iis-logging.md)disponibile nel gruppo di URL.
-   [Registrazione binaria centralizzata:](centralized-binary-logging.md)disponibile nella sessione del server.

Per sfruttare la funzionalità di registrazione HTTP, l'applicazione abilita e configura un tipo di registrazione nella sessione del server o nel gruppo di URL. Per altre informazioni, vedere [Configurazione e abilitazione della registrazione lato server](configuring-and-enabling-server-side-logging.md)

 

 




