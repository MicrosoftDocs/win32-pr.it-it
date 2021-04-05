---
title: Documento ServiceInfo per un negozio online di tipo 2
description: Documento ServiceInfo per un negozio online di tipo 2
ms.assetid: ca83e9bf-c7fb-4212-8fa2-1fae11ed26e9
keywords:
- Windows Media Player Online Stores, documento ServiceInfo
- archivi online, documento ServiceInfo
- digitare 2 archivi online, documento ServiceInfo
- Documento ServiceInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fb558661332ab08edd2057fa024a1a0e2034b9f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044859"
---
# <a name="serviceinfo-document-for-a-type-2-online-store"></a>Documento ServiceInfo per un negozio online di tipo 2

I provider di archivio online di tipo 2 devono fornire a Microsoft l'URL di un documento XML che descrive l'archivio online. Windows Media Player 10 e Windows Media Player 11 usano questo documento per determinare come configurare l'interfaccia utente per ospitare lo Store online.

In Windows Media Player 10, il documento ServiceInfo offre quanto segue:

-   Informazioni su come configurare i riquadri attività visualizzati da Windows Media Player quando lo Store online è attivo. Un archivio online può avere uno, due o tre riquadri attività.
-   Informazioni utilizzate per configurare i pulsanti del riquadro attività, ad esempio il testo del pulsante, il colore del pulsante e le descrizioni comandi per i pulsanti.
-   URL per le immagini visualizzate da Windows Media Player per identificare il negozio online.
-   URL di pagine Web, fornite dallo Store online, che Windows Media Player ospita nell'interfaccia utente.
-   Informazioni sul modo in cui il programma di installazione di Windows Media Player deve configurare il primo negozio online visualizzato dall'utente.

In Windows Media Player 11, il documento ServiceInfo offre quanto segue:

-   Informazioni utilizzate per configurare il pulsante per la scheda Store online, ad esempio il testo del pulsante e la descrizione comando per il pulsante.
-   URL per le immagini visualizzate da Windows Media Player per identificare il negozio online.
-   URL di pagine Web, fornite dallo Store online, che Windows Media Player ospita nell'interfaccia utente.

Quando si inizia a sviluppare lo Store online, è necessario fornire a Microsoft l'URL del documento ServiceInfo. Durante la fase di sviluppo, il negozio online verrà visualizzato in Windows Media Player solo quando viene impostata una speciale chiave del registro di sistema.

Dopo la pubblicazione del negozio online, lo scenario ususal è che Windows Media Player recupera automaticamente il documento ServiceInfo dal Web. In alcuni casi, tuttavia, Windows Media Player Recupera il documento ServiceInfo dal computer dell'utente. Per ulteriori informazioni, vedere [impostazione dell'archivio online iniziale](setting-the-initial-online-store.md).

Quando Windows Media Player Recupera il documento ServiceInfo dal Web, aggiunge una stringa di query all'URL. La stringa di query contiene parametri che forniscono informazioni sulle impostazioni locali dell'utente e sulla versione di Windows Media Player.

È possibile creare documenti ServiceInfo statici o dinamici. Un documento ServiceInfo statico ha un'estensione di file XML. Un documento ServiceInfo dinamico è una pagina ASP con estensione di file ASP o aspx.

Non tutti gli elementi disponibili per l'uso nel documento ServiceInfo possono essere usati da ogni negozio online e alcuni elementi sono facoltativi per tutti i negozi online. Per informazioni sui tipi di negozi online che è possibile creare e sulle funzionalità disponibili per ogni tipo, vedere [Windows Media Player Online Stores](windows-media-player-online-stores.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni sui negozi online di tipo 2**](about-type-2-online-stores.md)
</dt> <dt>

[**Creazione dinamica del documento ServiceInfo**](creating-the-serviceinfo-document-dynamically.md)
</dt> <dt>

[**Documento ServiceInfo di esempio per un negozio online di tipo 2**](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**Documento ServiceInfo**](serviceinfo-document.md)
</dt> </dl>

 

 




