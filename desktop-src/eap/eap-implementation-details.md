---
title: Dettagli di implementazione EAP
description: I punti di accesso (APs), ad esempio il servizio di accesso remoto (RAS), interagiscono con le implementazioni EAP tramite l'utilizzo di chiamate di funzione che devono essere esportate dalla DLL EAP di terze parti.
ms.assetid: 85775c03-7538-41a1-9f83-42e71025a79c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41115b16d843b0c1b087eac1c348a0491df1173a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104337142"
---
# <a name="eap-implementation-details"></a>Dettagli di implementazione EAP

I punti di accesso (APs), ad esempio il servizio di accesso remoto (RAS), interagiscono con le implementazioni EAP tramite l'utilizzo di chiamate di funzione che devono essere esportate dalla DLL EAP di terze parti. In altre parole, EAP è un'API del provider, vale a dire che i plug-in o le DLL implementano il codice per diventare un provider EAP, ma non devono chiamare le API EAP stesse. Ad esempio, un programmatore di una DLL EAP crea codice per una routine di inizializzazione EAP e inserisce il codice nella funzione predefinita EAP [**RasEapInitialize**](/previous-versions/windows/desktop/legacy/aa363527(v=vs.85)). Quindi, in fase di esecuzione, la gestione connessione AP chiama la funzione **RasEapInitialize** , che contiene il codice, per inizializzare l'implementazione EAP.

Negli argomenti seguenti viene illustrata in dettaglio questa interazione:

-   [Inizializzazione del punto di accesso di EAP](ras-initialization-of-eap.md)
-   [Inizializzazione del protocollo di autenticazione](authentication-protocol-initialization.md)
-   [Interazione del punto di accesso e del protocollo di autenticazione](ras-and-authentication-protocol-interaction-during-authentication.md)
-   [Completamento della sessione di autenticazione](completion-of-the-authentication-session.md)

 

 