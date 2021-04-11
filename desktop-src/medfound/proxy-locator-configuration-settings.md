---
description: Impostazioni di configurazione del localizzatore proxy
ms.assetid: d74a85cf-293e-4322-9aff-55b06d6fda5e
title: Impostazioni di configurazione del localizzatore proxy
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3503a90bcccc990865769b6bf02a65fc383511f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130486"
---
# <a name="proxy-locator-configuration-settings"></a>Impostazioni di configurazione del localizzatore proxy

Questo argomento descrive le impostazioni di configurazione per il localizzatore proxy predefinito. Per informazioni sulla creazione del localizzatore proxy con le impostazioni di configurazione personalizzate, vedere [How to configure the proxy Locator](how-to-configure-the-proxy-locator.md).

Il localizzatore proxy può essere configurato in modo da funzionare in tre modalità: modalità *manuale*, *modalità di rilevamento automatico* e *modalità browser*. I valori sono definiti nell'enumerazione [**MFNET \_ PROXYSETTINGS**](/windows/desktop/api/mfidl/ne-mfidl-mfnet_proxysettings) . L'applicazione può configurare la modalità impostando la proprietà [**MFNETSOURCE \_ PROXYSETTINGS**](mfnetsource-proxysettings-property.md) . Il localizzatore proxy può anche essere configurato in modo da non usare un server proxy impostando questa proprietà su **MFNET \_ PROXYSETTING \_ None**. Il server proxy non viene usato se il server multimediale è un host locale o l'applicazione richiede un indirizzo di classe (127. x.x. x), riservato per i test di loopback.

> [!Caution]  
> Un server proxy è una barriera di sicurezza tra la rete Intranet e Internet. Il mancato utilizzo di un server proxy può esporre la rete a minacce alla sicurezza.

 

-   Modalità manuale. Questa modalità viene impostata dall'applicazione impostando la proprietà [**MFNETSOURCE \_ PROXYSETTING**](mfnetsource-proxysettings-property.md) su **MFNET \_ PROXYSETTING \_ Manual**. L'applicazione deve specificare le seguenti informazioni di connessione:

    -   Nome host del server proxy: [**MFNETSOURCE proprietà \_ PROXYHOSTNAME**](mfnetsource-proxyhostname-property.md) .
    -   Numero porta: [**MFNETSOURCE proprietà \_ PROXYPORT**](mfnetsource-proxyport-property.md) .
    -   Indica se usare un server proxy per gli indirizzi locali: proprietà [**\_ PROXYBYPASSFORLOCAL di MFNETSOURCE**](mfnetsource-proxybypassforlocal-property.md) . Questa impostazione è facoltativa. Se non viene specificato, il localizzatore proxy usa il valore predefinito **false**.

        > [!Note]  
        > Ignorando il server proxy, l'applicazione potrebbe essere in grado di connettersi più rapidamente a server multimediali nella Intranet.

         

    -   Elenco di indirizzi del server multimediale per i quali non è necessario un server proxy per stabilire una connessione: [**MFNETSOURCE \_ PROXYEXCEPTIONLIST**](mfnetsource-proxyexceptionlist-property.md) Property. Questa impostazione è facoltativa.

-   Modalità di rilevamento automatico. Questa modalità viene impostata dall'applicazione impostando la proprietà [**MFNETSOURCE \_ PROXYSETTING**](mfnetsource-proxysettings-property.md) su **MFNET \_ PROXYSETTING \_ auto**. In questa modalità, il localizzatore proxy usa il meccanismo di AutoProxy WinHTTP per ottenere il nome host e il numero di porta per il server proxy. Queste informazioni di connessione vengono recuperate tramite lo script del proxy automatico WPAD, configurato dall'amministratore di dominio. Per ulteriori informazioni su questo meccanismo, vedere il [sito Web Microsoft](../winhttp/winhttp-autoproxy-support.md).

    Il localizzatore proxy memorizza nella cache le informazioni di connessione nel registro di sistema. Nelle successive chiamate al rilevamento proxy, il localizzatore proxy legge le informazioni sul proxy dalla cache del registro di sistema per ridurre l'overhead dovuto al rilevamento automatico. Tuttavia, l'applicazione può forzare il ririlevamento automatico del proxy impostando la proprietà [**MFNETSOURCE \_ PROXYRERUNAUTODETECTION**](mfnetsource-proxyrerunautodetection-property.md) .

-   Modalità browser. Questa modalità viene impostata dall'applicazione impostando la proprietà [**MFNETSOURCE \_ PROXYSETTING**](mfnetsource-proxysettings-property.md) su **MFNET \_ PROXYSETTING \_ browser**. In questa modalità, il localizzatore proxy usa le impostazioni proxy dell'applicazione browser. Questa modalità è impostata per impostazione predefinita se il protocollo è HTTP o HTTPD.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Supporto del proxy per le origini di rete](proxy-support-for-network-sources.md)
</dt> </dl>

 

 
