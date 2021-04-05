---
description: Vengono illustrate le differenze tra SSP/APs e SSP.
ms.assetid: 0ed4291b-6562-440f-b892-4e6e5b4b49c8
title: SSP/APs e SSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8d089a27da6b0ab5d4228af924f738f27a1d728
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968137"
---
# <a name="sspaps-vs-ssps"></a>SSP/APs e SSP

I [*pacchetti di sicurezza*](../secgloss/s-gly.md) vengono distribuiti in uno dei seguenti tipi di librerie a collegamento dinamico (dll):

-   [SSP/APs](#sspaps-vs-ssps)
-   [Provider](#sspaps-vs-ssps)

Il fatto che un pacchetto di sicurezza si trovi in un pacchetto di Security Support Provider/[*autenticazione*](../secgloss/a-gly.md) (SSP/AP) o in una DLL di [*Security Support Provider*](../secgloss/s-gly.md) (SSP) è determinato dai tipi di servizi di sicurezza forniti e dal livello di integrazione con l' [*autorità di sicurezza locale*](../secgloss/l-gly.md) (LSA). Queste differenze determinano anche l'API implementata in un pacchetto di sicurezza personalizzato.

## <a name="sspaps"></a>SSP/APs

Un SSP/AP è una DLL che contiene uno o più [*pacchetti di sicurezza*](../secgloss/s-gly.md) e può fungere da SSP per le applicazioni client/server e come [pacchetto di autenticazione](authentication-packages.md) per le applicazioni di accesso. Per funzionare in entrambi i ruoli, SSP/APs vengono caricati nello spazio di elaborazione LSA all'avvio del sistema e possono essere caricati anche nei processi dell'applicazione client/server.

I pacchetti di sicurezza SSP/AP personalizzati devono implementare sia le [funzioni implementate da SSP/APS in modalità utente](authentication-functions.md)che le [funzioni implementate da SSP/APS](authentication-functions.md). Queste implementazioni di funzioni possono avvalersi delle funzioni di supporto LSA per offrire funzionalità di sicurezza avanzate, ad esempio la creazione di token, il supporto [*supplementare delle credenziali*](../secgloss/s-gly.md) e l'autenticazione pass-through.

Se un pacchetto di sicurezza SSP/AP personalizzato fornisce la gamma completa di funzioni di [*integrità*](../secgloss/i-gly.md) e privacy dei messaggi, implementa anche le [funzioni implementate da SSP/APS in modalità utente](authentication-functions.md).

## <a name="ssps"></a>Provider

Un SSP è una DLL che contiene uno o più pacchetti di sicurezza che forniscono servizi autenticati di connessione, integrità dei messaggi e crittografia messaggi alle applicazioni client/server. Gli SSP implementano le funzioni SSPI ( [Security Support Provider Interface](sspi.md) ). Le applicazioni possono accedere ai pacchetti di sicurezza in un SSP chiamando direttamente le funzioni SSPI. I SSP vengono caricati nei processi client e server; non sono integrati con LSA.

 

 
