---
description: Configurazione del localizzatore proxy Impostazioni
ms.assetid: d74a85cf-293e-4322-9aff-55b06d6fda5e
title: Configurazione del localizzatore proxy Impostazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa5b2f7bc8e8567fcb1d84ab48bdd2a9652045ecb0332de63b82db2652dfe86a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118058634"
---
# <a name="proxy-locator-configuration-settings"></a>Configurazione del localizzatore proxy Impostazioni

Questo argomento descrive le impostazioni di configurazione per il localizzatore proxy predefinito. Per informazioni sulla creazione del localizzatore proxy con impostazioni di configurazione personalizzate, vedere [How to Configure the Proxy Locator](how-to-configure-the-proxy-locator.md).

Il localizzatore proxy può essere configurato per operare in tre modalità: *modalità* manuale, *modalità* di rilevamento automatico e *modalità browser.* I valori sono definiti [**nell'enumerazione MFNET \_ PROXYSETTINGS.**](/windows/desktop/api/mfidl/ne-mfidl-mfnet_proxysettings) L'applicazione può configurare la modalità impostando la [**proprietà MFNETSOURCE \_ PROXYSETTINGS.**](mfnetsource-proxysettings-property.md) Il localizzatore proxy può anche essere configurato per non usare un server proxy impostando questa proprietà su **MFNET \_ PROXYSETTING \_ NONE.** Il server proxy non viene usato se il server multimediale è un host locale o l'applicazione richiede un indirizzo di classe A (127.x.x.x), riservato per i test di loopback.

> [!Caution]  
> Un server proxy è una barriera di sicurezza tra intranet e Internet. Il non utilizzo di un server proxy può esporre la rete a minacce alla sicurezza.

 

-   Modalità manuale. L'applicazione imposta questa modalità impostando la [**proprietà MFNETSOURCE \_ PROXYSETTING**](mfnetsource-proxysettings-property.md) su **MFNET \_ PROXYSETTING \_ MANUAL.** L'applicazione deve specificare le informazioni di connessione seguenti:

    -   Nome host del server proxy: [**proprietà \_ PROXYHOSTNAME di MFNETSOURCE.**](mfnetsource-proxyhostname-property.md)
    -   Numero di porta: [**proprietà \_ PROXYPORT MFNETSOURCE.**](mfnetsource-proxyport-property.md)
    -   Se usare un server proxy per gli indirizzi locali: [**proprietà MFNETSOURCE \_ PROXYBYPASSFORLOCAL.**](mfnetsource-proxybypassforlocal-property.md) Questa impostazione è facoltativa. Se non viene specificato, il localizzatore proxy usa il valore predefinito **FALSE**.

        > [!Note]  
        > Ignorando il server proxy, l'applicazione potrebbe essere in grado di connettersi ai server multimediali nella intranet più velocemente.

         

    -   Elenco di indirizzi del server multimediale che non richiedono un server proxy per stabilire una connessione: [**proprietà MFNETSOURCE \_ PROXYEXCEPTIONLIST.**](mfnetsource-proxyexceptionlist-property.md) Questa impostazione è facoltativa.

-   Modalità di rilevamento automatico. L'applicazione imposta questa modalità impostando la [**proprietà MFNETSOURCE \_ PROXYSETTING**](mfnetsource-proxysettings-property.md) su **MFNET \_ PROXYSETTING \_ AUTO.** In questa modalità, il localizzatore proxy usa il meccanismo WinHTTP AutoProxy per ottenere il nome host e il numero di porta per il server proxy. Queste informazioni di connessione vengono recuperate usando lo script proxy automatico WPAD, configurato dall'amministratore di dominio. Per altre informazioni su questo meccanismo, vedere il sito [Web Microsoft](../winhttp/winhttp-autoproxy-support.md).

    Il localizzatore proxy memorizza nella cache le informazioni di connessione nel Registro di sistema. Nelle chiamate di rilevamento proxy successive, il localizzatore proxy legge le informazioni proxy dalla cache del Registro di sistema per ridurre il sovraccarico del rilevamento automatico. Tuttavia, l'applicazione può forzare la ridenominazione automatica del proxy impostando la proprietà [**MFNETSOURCE \_ PROXYRERUNAUTODETECTION.**](mfnetsource-proxyrerunautodetection-property.md)

-   Modalità browser. L'applicazione imposta questa modalità impostando la [**proprietà MFNETSOURCE \_ PROXYSETTING**](mfnetsource-proxysettings-property.md) su **MFNET \_ PROXYSETTING \_ BROWSER**. In questa modalità, il localizzatore proxy usa le impostazioni proxy dell'applicazione browser. Questa modalità è impostata per impostazione predefinita se il protocollo è HTTP o HTTPD.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Supporto proxy per le origini di rete](proxy-support-for-network-sources.md)
</dt> </dl>

 

 
