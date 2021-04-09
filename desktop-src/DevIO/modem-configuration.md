---
description: Le funzioni di configurazione del modem consentono di configurare un modem prima di effettuare una connessione.
ms.assetid: 67d8f3c4-0295-4028-8b12-1a5e26979df5
title: Configurazione modem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7abd6c5319011b8821487b6adf0351dc799e61f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878121"
---
# <a name="modem-configuration"></a>Configurazione modem

Le funzioni di configurazione del modem consentono di configurare un modem prima di effettuare una connessione. Un'applicazione può impostare le opzioni del modem e determinare le funzionalità di un modem senza usare comandi specifici per qualsiasi dispositivo modem. Di seguito sono riportate le funzionalità generali che un'applicazione può impostare prima di effettuare una chiamata:

-   Modalità di funzionamento principale (sincrona, asincrona e se il controllo degli errori è abilitato).
-   Controllo degli errori v. 42 (definito da CCITT Recommendation V. 42), inclusi parametri specifici. CCITT è l'acronimo di International Telegraph and Phone consultive Committee.
-   V. 42bis (definito da CCITT Recommendation V. 42bis) e la compressione dei dati MNP5.
-   Opzioni di timeout, incluse la configurazione delle chiamate, l'inattività e il recapito dei dati memorizzati nel buffer.

Prima di impostare la configurazione di un modem, un'applicazione deve determinare le funzionalità del dispositivo modem utilizzando la funzione [**GetCommProperties**](/windows/desktop/api/Winbase/nf-winbase-getcommproperties) . Questa funzione compila una struttura [**COMMPROP**](/windows/desktop/api/WinBase/ns-winbase-commprop) . Questa struttura contiene una parte generale, applicabile a tutti i dispositivi di comunicazione, e una parte specifica per ogni sottotipo di provider. Per i dispositivi modem, la parte specifica del provider della struttura **COMMPROP** è una struttura [**MODEMDEVCAPS**](/windows/desktop/api/Mcx/ns-mcx-modemdevcaps) .

Un'applicazione può ottenere e impostare la configurazione corrente di un modem usando le funzioni [**GetCommConfig**](/windows/desktop/api/Winbase/nf-winbase-getcommconfig) e [**SetCommConfig**](/windows/desktop/api/Winbase/nf-winbase-setcommconfig) , entrambe che usano una struttura [**COMMCONFIG**](/windows/desktop/api/Winbase/ns-winbase-commconfig) . Questa struttura contiene una parte generale, applicabile a tutti i dispositivi di comunicazione, e una parte specifica per ogni sottotipo di provider. Per i dispositivi modem, la parte specifica del provider della struttura **COMMCONFIG** è una struttura [**MODEMSETTINGS**](/windows/desktop/api/Mcx/ns-mcx-modemsettings) .

Dopo la configurazione di un modem, un'applicazione può utilizzare l'interfaccia TAPI (Telephony Application Programming Interface) per stabilire effettivamente una connessione.

Le funzioni di configurazione del modem non forniscono la gestione e la manutenzione a lungo termine di un modem. I provider di servizi modem devono fornire le finestre di dialogo di configurazione modem a questo scopo.

 

 



