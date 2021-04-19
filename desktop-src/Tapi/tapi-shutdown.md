---
description: È necessario arrestare correttamente le sessioni di comunicazione e un'intera applicazione per evitare che le risorse rimangano vincolate nelle chiamate o nelle applicazioni che non sono più necessarie.
ms.assetid: 40694b7f-474b-41aa-be3f-48e4ca517a6f
title: Arresto TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 661273a3d72559d965fa1ea6066f1090f8e6b6e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317635"
---
# <a name="tapi-shutdown"></a>Arresto TAPI

È necessario arrestare correttamente le sessioni di comunicazione e un'intera applicazione per evitare che le risorse rimangano vincolate nelle chiamate o nelle applicazioni che non sono più necessarie.

TAPI fornisce una serie di funzioni e metodi che consentono di semplificare il processo. Ovviamente, l'applicazione deve anche essere responsabile del rilascio corretto della memoria allocata, sia sotto forma di strutture di dati che di riferimenti COM.



| Funzioni di TAPI 2. x                                                            | Descrizione                                                            |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [**lineRegisterRequestRecipient**](/windows/win32/api/tapi/nf-tapi-lineregisterrequestrecipient) | Annulla la registrazione dell'applicazione come gestore per le chiamate di telefonia assistita. |
| [**lineClose**](/windows/win32/api/tapi/nf-tapi-lineclose)                                       | Disconnette l'applicazione come responsabile per le chiamate sulla riga specificata.  |
| [**lineShutdown**](/windows/win32/api/tapi/nf-tapi-lineshutdown)                                 | Arresta l'utilizzo dell'applicazione dell'astrazione di riga.            |



 



| Interfacce o metodi di TAPI 3. x                                            | Descrizione                                                                |
|---------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [**ITTAPI::UnregisterNotifications**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-unregisternotifications) | Rimuove tutte le registrazioni di notifiche degli eventi eseguite dall'applicazione. |
| [**ITTAPI:: Shutdown**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-shutdown)                               | Disconnette l'applicazione come gestione chiamate.                             |



 

 

 
