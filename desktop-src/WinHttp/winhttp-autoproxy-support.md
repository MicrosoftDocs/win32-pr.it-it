---
description: Per semplificare la configurazione delle impostazioni proxy, WinHTTP 5,1 implementa il protocollo WPAD (Web Proxy Auto-Discovery), noto anche come AutoProxy.
ms.assetid: f766f37b-a1aa-420f-ac3b-d03485630d88
title: Supporto del proxy AutoProxy WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26584bd0b1809f3866ed42adc7198275f40f991c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307106"
---
# <a name="winhttp-autoproxy-support"></a>Supporto del proxy AutoProxy WinHTTP

Per semplificare la configurazione delle impostazioni proxy, WinHTTP 5,1 implementa il protocollo WPAD (Web Proxy Auto-Discovery), noto anche come AutoProxy.

## <a name="overview-of-autoproxy"></a>Panoramica di AutoProxy

Le applicazioni e i componenti che usano WinHTTP per inviare richieste HTTP devono assicurarsi che la configurazione del proxy sia impostata correttamente. A meno che il client non disponga di una connessione Internet diretta, una richiesta HTTP deve essere normalmente inviata tramite un server proxy Web che connette la rete locale del client a Internet (ad esempio, questo è spesso il caso per i client Web in una LAN aziendale). Per le applicazioni basate su server, la configurazione del proxy viene in genere gestita dall'amministratore del server tramite l'utilità WinHTTP ProxyCfg.exe. L'amministratore del server conosce in anticipo il nome del server proxy e USA ProxyCfg.exe per registrare questa impostazione nel registro di sistema in cui WinHTTP può cercarlo. Tuttavia, è problematico richiedere agli utenti finali del desktop client di configurare manualmente le impostazioni proxy WinHTTP. È possibile che l'utente finale non conosca il nome del server proxy. richiedere all'utente finale di eseguire l'utilità di ProxyCfg.exe può essere un onere del supporto per un'organizzazione. Per supportare un'esperienza utente ottimale, un'applicazione client abilitata per il Web deve determinare la configurazione del proxy senza l'intervento dell'utente.

Per semplificare la configurazione delle impostazioni proxy per le applicazioni basate su WinHTTP, WinHTTP ora implementa il [protocollo WPAD (Web Proxy Auto-Discovery)](https://tools.ietf.org/html/draft-ietf-wrec-wpad-01), spesso definito *AutoProxy*. Si tratta dello stesso protocollo implementato dai Web browser per individuare automaticamente la configurazione del proxy senza richiedere a un utente finale di specificare manualmente un server proxy. Questa funzionalità è disponibile a partire da WinHTTP versione 5,1 in Windows 2000 Service Pack 3, Windows XP Service Pack 1 e Windows Server 2003. Si noti che, sebbene Microsoft Internet Explorer e Microsoft WinHTTP supportino WPAD, la specifica non progredisce mai oltre la fase "Internet-Draft" ed è scaduta il 2001 maggio.

Il protocollo WPAD funziona nel modo seguente:

1.  Utilizzando i protocolli di rete DHCP e/o DNS, viene individuato l'URL di un file di configurazione automatica proxy (PAC). L'URL identifica un file PAC nella rete locale del client. WinHTTP supporta solo gli URL PAC "http:" e "https:"; non supporta, ad esempio, gli URL "file:".
2.  Il file PAC viene scaricato e, facoltativamente, memorizzato nella cache nel computer del client. Il file PAC è uno script eseguibile che genera un elenco di uno o più server proxy, dato un nome host e un URL di destinazione. WinHTTP supporta solo file PAC basati su ECMAScript.
3.  Per ogni richiesta HTTP, viene eseguito il codice di script PAC con il nome host e l'URL della richiesta HTTP passati come parametri. WinHTTP prevede che il codice di script PAC contenga una funzione denominata **FindProxyForURL**, nel formato seguente:
4.  ``` syntax
    FindProxyForURL( url, host );
    ```

    Questa funzione calcola un elenco di uno o più server proxy che possono essere usati dal client HTTP per trasmettere la richiesta. Se lo script PAC determina che il client HTTP può raggiungere direttamente il server di destinazione senza passare attraverso un server proxy, indica che l'uso di un valore restituito speciale.

## <a name="autoproxy-topics"></a>Argomenti relativi a AutoProxy

-   [Funzioni proxy AutoProxy WinHTTP](winhttp-autoproxy-api.md)
-   [Individuazione senza un file di configurazione automatica](discovery-without-an-auto-config-file.md)
-   [Problemi di proxy AutoProxy in WinHTTP](autoproxy-issues-in-winhttp.md)
-   [Impostazione delle configurazioni del proxy WinInet in WinHTTP](setting-wininet-proxy-configurations-in-winhttp.md)
-   [Cache AutoProxy](autoproxy-cache.md)
-   [Estensioni IPv6 per il formato di file di configurazione automatica dello strumento di navigazione](ipv6-extensions-to-navigator-auto-config-file-format.md)

 

 



