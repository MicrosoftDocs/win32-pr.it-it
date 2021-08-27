---
description: Viene illustrato come creare un pacchetto di sicurezza personalizzato.
ms.assetid: af8b9796-77e7-43c1-8f8e-acee01a62bf9
title: Creazione di pacchetti di sicurezza personalizzati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88093ba7faed1ac2287c2a54391015984e83d4ad3878a60453978a9924706f2b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008849"
---
# <a name="creating-custom-security-packages"></a>Creazione di pacchetti di sicurezza personalizzati

## <a name="ssp-security-packages"></a>Pacchetti di sicurezza SSP

Se un pacchetto di sicurezza SSP (Security Support Provider) personalizzato verrà usato esclusivamente per il supporto della sicurezza client/server, può implementare Microsoft [Security Support Provider Interface.](sspi.md)

L'esempio SampSSP fornito con Platform Software Development Kit (SDK) contiene un'implementazione del pacchetto di sicurezza SSP di esempio.

## <a name="sspap-security-packages"></a>Pacchetti di sicurezza SSP/AP

I [*pacchetti di autenticazione*](/windows/desktop/SecGloss/s-gly)del provider di supporto per la sicurezza / [](/windows/desktop/SecGloss/a-gly) (SSP/APs) personalizzati contengono pacchetti di sicurezza che funzionano come pacchetti di autenticazione (AP) e provider di supporto per la sicurezza (SSP). Questi pacchetti implementano API separate per supportare ogni ruolo.

Poiché funziona come un punto di accesso, un pacchetto di sicurezza SSP/AP [](/windows/desktop/SecGloss/s-gly) personalizzato deve fornire implementazioni per tutte le funzioni [implementate dai pacchetti di autenticazione.](authentication-functions.md)

Per fornire supporto integrato per la sicurezza, un pacchetto di sicurezza SSP/AP personalizzato deve fornire implementazioni per le funzioni implementate da [SSP/APs.](authentication-functions.md) [Funzioni LSA chiamate da SSP/APs](authentication-functions.md) descrive le funzioni di supporto disponibili per gli sviluppatori SSP/AP che vogliono interagire con l'LSA.

I pacchetti di sicurezza SSP/AP, per poter essere eseguiti sia come punto di accesso che come SSP, possono essere eseguiti come parte del sistema operativo e come parte di un'applicazione utente. Queste due modalità di esecuzione sono note rispettivamente come modalità LSA e modalità utente. Per informazioni dettagliate sui pacchetti di sicurezza personalizzati in modalità LSA, vedere [Inizializzazione in modalità LSA.](lsa-mode-initialization.md) Per informazioni dettagliate sulla modalità utente, vedere [Inizializzazione in modalità utente.](user-mode-initialization.md)

Se un pacchetto di sicurezza SSP/AP personalizzato offre servizi per le applicazioni client/server, deve fornire implementazioni per le funzioni descritte in Funzioni implementate da provider di servizi di [configurazione/provider](authentication-functions.md)di servizi di configurazione in modalità utente. [LSA Functions Called By User-mode SSP/APs](authentication-functions.md) (Funzioni LSA chiamate da provider di servizi di configurazione/provider di servizi di configurazione in modalità utente) descrive le funzioni di supporto disponibili per un provider di servizi di configurazione/punto di accesso in esecuzione in un processo client o server.

Per informazioni sulla registrazione di una DLL SSP/AP, vedere [Registrazione di DLL SSP/AP.](registering-ssp-ap-dlls.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Restrizioni relative alla registrazione e all'installazione di un pacchetto di sicurezza](restrictions-around-registering-and-installing-a-security-package.md)
</dt> </dl>

 

 
