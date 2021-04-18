---
description: Supporto del proxy per le origini di rete
ms.assetid: e739746d-2a09-4237-a7c1-0aed4e4516d7
title: Supporto del proxy per le origini di rete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97bc1172c072a54f9f76cbcd3a297a972efbde29
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309023"
---
# <a name="proxy-support-for-network-sources"></a>Supporto del proxy per le origini di rete

Un server proxy è un server intermedio tra la rete Intranet e Internet, che instrada le richieste dall'applicazione client al server multimediale e recupera i file dal server multimediale.

Media Foundation crea in modo implicito un oggetto *localizzatore proxy* quando un'applicazione client tenta di accedere a un URL di origine. L'oggetto localizzatore proxy espone l'interfaccia [**IMFNetProxyLocator**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocator) . Durante la risoluzione del codice sorgente, Media Foundation controlla l'archivio delle proprietà passato al metodo del resolver di origine.

Se l'archivio delle proprietà contiene la proprietà [ \_ PROXYLOCATORFACTORY di MFNETSOURCE](mfnetsource-proxylocatorfactory-property.md) impostata su un oggetto factory del localizzatore proxy implementato dall'applicazione, richiama il metodo [**IMFNetProxyLocatorFactory:: CreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-imfnetproxylocatorfactory-createproxylocator) per creare un localizzatore proxy con impostazioni di configurazione personalizzate.

Se l'archivio delle proprietà non è impostato, Media Foundation crea il localizzatore proxy con la configurazione predefinita. Queste impostazioni sono le seguenti:

-   Se è impostato un criterio utente, il localizzatore proxy usa le impostazioni specificate nel registro di sistema.

-   Per HTTP, il localizzatore proxy usa le impostazioni del proxy del browser.

-   Per RTSP, il localizzatore proxy è configurato in modo da ignorare i server proxy durante la connessione al server multimediale.

Questa configurazione predefinita può essere modificata dall'applicazione. Gli argomenti seguenti contengono informazioni sulle impostazioni di configurazione per un localizzatore proxy:

-   [Impostazioni di configurazione del localizzatore proxy](proxy-locator-configuration-settings.md)

-   [Come configurare il localizzatore proxy](how-to-configure-the-proxy-locator.md)

Media Foundation Inizializza il localizzatore proxy per l'URL di origine specificato nel [resolver di origine](source-resolver.md). Il localizzatore proxy rileva un server proxy da usare in base alle impostazioni di configurazione. Quando il localizzatore proxy tenta il set di un server proxy, registra il risultato dell'esito positivo o negativo nel registro di sistema. Questo valore viene verificato durante il successivo processo di rilevamento del proxy. Se è noto che un determinato server proxy ha causato errori in passato, il localizzatore proxy lo ignora.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Attributi e proprietà](attributes-and-properties.md)
</dt> <dt>

[Rete in Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 



