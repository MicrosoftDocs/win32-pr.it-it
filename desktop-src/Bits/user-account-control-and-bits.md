---
title: Controllo dell'account utente e BITS
description: Quando un utente amministratore accede al computer, vengono creati due token di accesso. Uno è un token di accesso utente standard filtrato e l'altro è un token di accesso amministratore completo.
ms.assetid: 02439ab3-b885-4a2f-b507-0c48d2b30b76
ms.topic: article
ms.date: 7/12/2019
ms.openlocfilehash: 3017b3a0d816ba393d1427c5c1d2315a68b2dcc0
ms.sourcegitcommit: be77ed1f97d3be57a2f42070589de21b66034adf
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/29/2020
ms.locfileid: "103956269"
---
# <a name="bits-security-tokens-and-administrator-accounts"></a>Sicurezza BITS, token e account amministratore

## <a name="http-server-certificate-callbacks"></a>Callback del certificato del server HTTP
La convalida corretta dei certificati server è una parte fondamentale della gestione della sicurezza HTTPS. BITS consente di convalidare sempre i certificati del server in base a un elenco di requisiti specificati da [**SetSecurityFlags**](/windows/desktop/api/bits2_5/nf-bits2_5-ibackgroundcopyjobhttpoptions-setsecurityflags). Per impostazione predefinita, BITS usa la convalida del certificato di tipo "browser".

È anche possibile specificare una funzione personalizzata da chiamare per convalidare ulteriormente il certificato. Impostare il callback del certificato server con il metodo [**SetServerCertificateValidationInterface**](/windows/desktop/api/Bits10_3/nf-bits10_3-ibackgroundcopyjobhttpoptions3-setservercertificatevalidationinterface) . Il metodo verrà chiamato solo dopo che il sistema operativo ha convalidato il certificato in base alla chiamata di [ **SetSecurityFlag** s](/windows/desktop/api/bits2_5/nf-bits2_5-ibackgroundcopyjobhttpoptions-setsecurityflags) . 

## <a name="http-client-certificates"></a>Certificati client HTTP
È possibile impostare un certificato client in un processo HTTP con due diversi metodi di impostazioni del certificato. È possibile impostare un certificato in base all' [ID](/windows/desktop/api/bits2_5/nf-bits2_5-ibackgroundcopyjobhttpoptions-setclientcertificatebyid) o al [nome del soggetto](/windows/desktop/api/bits2_5/nf-bits2_5-ibackgroundcopyjobhttpoptions-setclientcertificatebyname)del certificato. Il certificato client verrà usato durante la negoziazione TLS (o la rinegoziazione) se il server richiede l'autenticazione client.

## <a name="write-only-http-headers"></a>Intestazioni HTTP di sola scrittura
BITS consente di proteggere i token di autenticazione HTTP da accessi non desiderati. Spesso un server HTTP necessita di un tipo di token o stringa di sicurezza durante il download o il caricamento di un file nei server HTTP.

BITS protegge i token di autenticazione in diversi modi.
* BITS consente di usare connessioni HTTP protette da TLS e SSL specificando un URL HTTPS.
* Le intestazioni personalizzate sono sempre mantenute in un formato crittografato su disco.
* È possibile impedire che le intestazioni dei clienti vengano restituite ad altri programmi con il metodo [**IBackgroundCopyJobHttpOptions3:: MakeCustomHeadersWriteOnly**](/windows/win32/api/Bits10_3/nf-bits10_3-ibackgroundcopyjobhttpoptions3-makecustomheaderswriteonly) .


## <a name="standard-and-administrator-users"></a>Utenti standard e amministratori
Un utente appartenente al gruppo Administrator può eseguire un processo con accesso utente standard o con privilegi di amministratore. BITS eseguirà il processo in uno dei due Stati, a condizione che l'utente venga registrato nel computer. Tuttavia, se l'utente ha creato il processo o ha assunto la proprietà del processo con privilegi elevati, l'utente deve essere nello stato con privilegi elevati per recuperare o modificare il processo. in caso contrario, la chiamata ha esito negativo con accesso negato (0x80070005). Per determinare lo stato con privilegi elevati di un processo, chiamare il metodo [**IBackgroundCopyJob4:: GetOwnerElevationState**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyjob4-getownerelevationstate) .

Un utente standard non può enumerare o modificare i processi di proprietà di altri utenti.

## <a name="integrity-level"></a>Livello di integrità
Oltre allo stato con privilegi elevati, il livello di integrità del token può determinare se l'utente può modificare un processo. Un client non può modificare i processi creati da un token con un livello di integrità superiore. In particolare, molti token di sistema locale presentano un livello di integrità superiore al livello di integrità di una finestra con privilegi elevati e pertanto non possono essere modificati da un amministratore da una finestra di comando con privilegi elevati. Ad esempio, i processi Windows Update e SMS vengono eseguiti come LocalSystem con un livello di integrità superiore rispetto a un token con privilegi elevati, in modo che un amministratore non possa modificare o eliminare questi processi. Per modificare il processo, creare un'attività Utilità di pianificazione eseguita come sistema locale. L'attività può eseguire un'applicazione console che usa l'API BITS oppure l'attività potrebbe eseguire uno script che chiama BitsAdmin.exe. Per determinare il livello di integrità usato, chiamare il metodo [**IBackgroundCopyJob4:: GetOwnerIntegrityLevel**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyjob4-getownerintegritylevel) .

## <a name="service-identity"></a>Identità del servizio
A partire da Windows 10 può 2019 aggiornamento (10,0; Compilazione 18362), i processi BITS avviati da un servizio manterranno l'identità del servizio. Questo consente ai servizi che vogliono usare BITS di scaricare file o caricare file da una directory le cui autorizzazioni sono associate al SID del servizio. Inoltre, il traffico di rete verrà attribuito correttamente al servizio che ha richiesto il processo BITS anziché essere attribuito a BITS.

 




