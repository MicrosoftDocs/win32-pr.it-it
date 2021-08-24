---
description: Per semplificare la configurazione delle impostazioni proxy, WinHTTP 5.1 implementa il protocollo WPAD (Web Proxy Auto-Discovery), noto anche come proxy automatico.
ms.assetid: f766f37b-a1aa-420f-ac3b-d03485630d88
title: Supporto del proxy automatico WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0f6a07645fd7d8bcd401bf399d2a9f525499c4d3a725e49b9d170c067092f70
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119614081"
---
# <a name="winhttp-autoproxy-support"></a>Supporto del proxy automatico WinHTTP

Per semplificare la configurazione delle impostazioni proxy, WinHTTP 5.1 implementa il protocollo WPAD (Web Proxy Auto-Discovery), noto anche come proxy automatico.

## <a name="overview-of-autoproxy"></a>Panoramica di AutoProxy

Le applicazioni e i componenti che usano WinHTTP per inviare richieste HTTP devono garantire che la configurazione del proxy sia impostata correttamente. A meno che il client non abbia una connessione Internet diretta, in genere una richiesta HTTP deve essere inviata tramite un server proxy Web che connette la rete locale del client a Internet (ad esempio, questo è spesso il caso dei client Web in una rete LAN aziendale). Per le applicazioni basate su server, la configurazione del proxy viene in genere gestita dall'amministratore del server usando l'utilità winHTTP ProxyCfg.exe. L'amministratore del server conosce in anticipo il nome del server proxy e usa ProxyCfg.exe per registrare questa impostazione nel Registro di sistema in cui WinHTTP può cercarla. Tuttavia, richiedere agli utenti finali del desktop client di configurare manualmente le impostazioni proxy WinHTTP è problematico. L'utente finale potrebbe non conoscere il nome del server proxy. richiedere all'utente finale di eseguire l'utilità ProxyCfg.exe può essere un onere di supporto per un'organizzazione. Per supportare un'esperienza utente ottimale, un'applicazione client abilitata per il Web deve determinare la configurazione del proxy senza l'intervento dell'utente.

Per semplificare la configurazione delle impostazioni proxy per le applicazioni basate su WinHTTP, WinHTTP implementa ora il protocollo [WPAD (Web Proxy Auto-Discovery),](https://tools.ietf.org/html/draft-ietf-wrec-wpad-01)spesso definito *autoproxy.* Si tratta dello stesso protocollo che i Web browser implementano per individuare automaticamente la configurazione del proxy senza richiedere a un utente finale di specificare manualmente un server proxy. Questa funzionalità è disponibile a partire da WinHTTP versione 5.1 in Windows 2000 Service Pack 3, Windows XP Service Pack 1 e Windows Server 2003. Si noti che, sebbene Microsoft Internet Explorer e Microsoft WinHTTP supportino WPAD, la specifica non è mai progredita oltre la fase "Internet-Draft" ed è scaduta nel maggio 2001.

Il protocollo WPAD funziona come segue:

1.  Usando i protocolli di rete DHCP e/o DNS, viene individuato l'URL di un file DIP (Proxy Auto-Configuration). L'URL identifica un file PAC nella rete locale del client. WinHTTP supporta solo gli URL PAC "http:" e "https:". non supporta, ad esempio, GLI URL "file:".
2.  Il file PAC viene scaricato e facoltativamente memorizzato nella cache nel computer del client. Il file PAC è uno script eseguibile che genera un elenco di uno o più server proxy con un nome host e un URL di destinazione. WinHTTP supporta solo file PAC basati su ECMAScript.
3.  In ogni richiesta HTTP viene eseguito il codice script PAC, con il nome host e l'URL della richiesta HTTP passati come parametri. WinHTTP prevede che il codice script PAC contenga una funzione denominata **FindProxyForURL** nel formato seguente:
4.  ``` syntax
    FindProxyForURL( url, host );
    ```

    Questa funzione calcola un elenco di uno o più server proxy che possono essere usati dal client HTTP per trasmettere la richiesta. Se lo script PAC determina che il client HTTP può raggiungere direttamente il server di destinazione senza passare attraverso un server proxy, lo indica usando un valore restituito speciale.

## <a name="autoproxy-topics"></a>Argomenti di AutoProxy

-   [Funzioni del proxy automatico WinHTTP](winhttp-autoproxy-api.md)
-   [Individuazione senza un file di configurazione automatica](discovery-without-an-auto-config-file.md)
-   [Problemi di AutoProxy in WinHTTP](autoproxy-issues-in-winhttp.md)
-   [Impostazione delle configurazioni del proxy WinInet in WinHTTP](setting-wininet-proxy-configurations-in-winhttp.md)
-   [Cache del proxy automatico](autoproxy-cache.md)
-   [Estensioni IPv6 per il formato di file di configurazione automatica dello strumento di navigazione](ipv6-extensions-to-navigator-auto-config-file-format.md)

 

 



