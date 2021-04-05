---
description: Viene illustrato come creare un pacchetto di sicurezza personalizzato.
ms.assetid: af8b9796-77e7-43c1-8f8e-acee01a62bf9
title: Creazione di pacchetti di sicurezza personalizzati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2136775d18e9d33f59d1b1f44fd817b3f3271ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882661"
---
# <a name="creating-custom-security-packages"></a>Creazione di pacchetti di sicurezza personalizzati

## <a name="ssp-security-packages"></a>Pacchetti di sicurezza SSP

Se un pacchetto di sicurezza di un Security Support Provider personalizzato (SSP) verrà utilizzato esclusivamente per il supporto della sicurezza client/server, può implementare l'interfaccia di Microsoft [Security Support Provider](sspi.md).

L'esempio SampSSP fornito con Platform Software Development Kit (SDK) contiene un'implementazione di pacchetto di sicurezza SSP di esempio.

## <a name="sspap-security-packages"></a>Pacchetti di sicurezza SSP/AP

I [](/windows/desktop/SecGloss/s-gly) / [*pacchetti di autenticazione*](/windows/desktop/SecGloss/a-gly) Security Support Provider personalizzati (SSP/APS) contengono pacchetti di sicurezza che funzionano come pacchetti di autenticazione (APS) e provider di supporto per la sicurezza (SSP). Questi pacchetti implementano API separate per supportare ogni ruolo.

Poiché funziona come punto di accesso, un [*pacchetto di sicurezza*](/windows/desktop/SecGloss/s-gly) SSP/AP personalizzato deve fornire implementazioni per tutte le [funzioni implementate dai pacchetti di autenticazione](authentication-functions.md).

Per garantire un supporto integrato per la sicurezza, un pacchetto di sicurezza SSP/AP personalizzato deve fornire implementazioni per le [funzioni implementate da SSP/APS](authentication-functions.md). Le [funzioni LSA chiamate da SSP/APS](authentication-functions.md) descrivono le funzioni di supporto disponibili per gli sviluppatori SSP/AP che vogliono interagire con LSA.

I pacchetti di sicurezza SSP/AP, per poter essere eseguiti sia come punto di accesso sia come provider di servizi condivisi, possono essere eseguiti come parte del sistema operativo e come parte di un'applicazione utente. Queste due modalità di esecuzione sono note rispettivamente come modalità LSA e modalità utente. Per informazioni dettagliate sui pacchetti di sicurezza personalizzati in modalità LSA, vedere [inizializzazione della modalità LSA](lsa-mode-initialization.md). Per informazioni dettagliate sulla modalità utente, vedere [inizializzazione della modalità utente](user-mode-initialization.md).

Se un pacchetto di sicurezza SSP/AP personalizzato offre servizi per le applicazioni client/server, deve fornire implementazioni per le funzioni descritte in [funzioni implementate da SSP/APS in modalità utente](authentication-functions.md). Le [funzioni LSA chiamate da SSP/APS in modalità utente](authentication-functions.md) descrivono le funzioni di supporto disponibili per un SSP/AP eseguito in un processo client o server.

Per informazioni sulla registrazione di una DLL SSP/AP, vedere la pagina relativa alla registrazione di DLL [SSP/AP](registering-ssp-ap-dlls.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Restrizioni relative alla registrazione e all'installazione di un pacchetto di sicurezza](restrictions-around-registering-and-installing-a-security-package.md)
</dt> </dl>

 

 
