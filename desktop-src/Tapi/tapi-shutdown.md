---
description: L'arresto corretto delle sessioni di comunicazione e di un'intera applicazione è necessario per impedire alle risorse di rimanere legate a chiamate o applicazioni che non ne hanno più bisogno.
ms.assetid: 40694b7f-474b-41aa-be3f-48e4ca517a6f
title: Arresto TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88303d2475a2ce0a21478575483c0fd93e44e96b71efa83790b7973343d6d9f1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120080441"
---
# <a name="tapi-shutdown"></a>Arresto TAPI

L'arresto corretto delle sessioni di comunicazione e di un'intera applicazione è necessario per impedire alle risorse di rimanere legate a chiamate o applicazioni che non ne hanno più bisogno.

TAPI offre una serie di funzioni e metodi utili per il processo. Ovviamente, l'applicazione deve anche assumersi la responsabilità di rilasciare correttamente la memoria allocata, sia sotto forma di strutture di dati che di riferimenti COM.



| Funzioni TAPI 2.x                                                            | Descrizione                                                            |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [**lineRegisterRequestRecipient**](/windows/win32/api/tapi/nf-tapi-lineregisterrequestrecipient) | Annulla la registrazione dell'applicazione come gestore per le chiamate di telefonia assistita. |
| [**lineClose**](/windows/win32/api/tapi/nf-tapi-lineclose)                                       | Disconnette l'applicazione come gestore per le chiamate sulla riga specificata.  |
| [**lineShutdown**](/windows/win32/api/tapi/nf-tapi-lineshutdown)                                 | Arresta l'utilizzo dell'astrazione di riga da parte dell'applicazione.            |



 



| Interfacce o metodi TAPI 3.x                                            | Descrizione                                                                |
|---------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [**ITTAPI::UnregisterNotifications**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-unregisternotifications) | Rimuove tutte le registrazioni delle notifiche degli eventi eseguite dall'applicazione. |
| [**ITTAPI::Shutdown**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-shutdown)                               | Disconnette l'applicazione come gestore chiamate.                             |



 

 

 
