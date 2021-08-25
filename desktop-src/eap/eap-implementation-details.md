---
title: Dettagli di implementazione EAP
description: I punti di accesso, ad esempio il servizio di accesso remoto (RAS, Remote Access Service), interagiscono con le implementazioni EAP tramite l'uso di chiamate di funzione che devono essere esportate dalla DLL EAP di terze parti.
ms.assetid: 85775c03-7538-41a1-9f83-42e71025a79c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8772d839e6d6fb748f56de0329a958057400d37afeb92a2f3ec89b3ab462e3a1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119852411"
---
# <a name="eap-implementation-details"></a>Dettagli di implementazione EAP

I punti di accesso, ad esempio il servizio di accesso remoto (RAS, Remote Access Service), interagiscono con le implementazioni EAP tramite l'uso di chiamate di funzione che devono essere esportate dalla DLL EAP di terze parti. In altre parole, EAP è un'API del provider, vale a dire che i plug-in o le DLL implementano il codice per diventare un provider EAP, ma non devono chiamare le API EAP stesse. Ad esempio, un programmatore di una DLL EAP crea il codice per una routine di inizializzazione EAP e inserisce questo codice nella funzione predefinita EAP [**RasEapInitialize.**](/previous-versions/windows/desktop/legacy/aa363527(v=vs.85)) In fase di esecuzione, la gestione connessione AP chiama quindi la funzione **RasEapInitialize,** che contiene il codice, per inizializzare l'implementazione EAP.

Gli argomenti seguenti descrivono in dettaglio questa interazione:

-   [Inizializzazione del punto di accesso di EAP](ras-initialization-of-eap.md)
-   [Inizializzazione del protocollo di autenticazione](authentication-protocol-initialization.md)
-   [Interazione tra il punto di accesso e il protocollo di autenticazione](ras-and-authentication-protocol-interaction-during-authentication.md)
-   [Completamento della sessione di autenticazione](completion-of-the-authentication-session.md)

 

 