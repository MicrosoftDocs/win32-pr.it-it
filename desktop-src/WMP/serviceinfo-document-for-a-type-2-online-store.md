---
title: Documento ServiceInfo per un Negozio online di tipo 2
description: Documento ServiceInfo per un Negozio online di tipo 2
ms.assetid: ca83e9bf-c7fb-4212-8fa2-1fae11ed26e9
keywords:
- Windows Media Player negozi online, documento ServiceInfo
- negozi online, documento ServiceInfo
- Tipo 2 negozi online, documento ServiceInfo
- Documento ServiceInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd6830b4c54b037f254adb21624ed893ec16fa9b3973dfe1536170dff1b4f9e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995431"
---
# <a name="serviceinfo-document-for-a-type-2-online-store"></a>Documento ServiceInfo per un Negozio online di tipo 2

I provider di negozi online di tipo 2 devono fornire a Microsoft l'URL di un documento XML che descrive il negozio online. Windows Media Player 10 e Windows Media Player 11 usare questo documento per determinare come configurare l'interfaccia utente per ospitare il negozio online.

In Windows Media Player 10, il documento ServiceInfo fornisce quanto segue:

-   Informazioni su come configurare i riquadri attività visualizzati Windows Media Player quando il negozio online è attivo. Un negozio online può avere uno, due o tre riquadri attività.
-   Informazioni usate per configurare i pulsanti del riquadro attività, ad esempio il testo del pulsante, il colore del pulsante e le descrizioni comandi per i pulsanti.
-   URL per le immagini Windows Media Player per identificare il negozio online.
-   URL delle pagine Web, forniti dal negozio online, che Windows Media Player host nell'interfaccia utente.
-   Informazioni su come Windows Media Player configurazione deve configurare il primo negozio online visualizzato dall'utente.

Nella Windows Media Player 11 il documento ServiceInfo fornisce quanto segue:

-   Informazioni usate per configurare il pulsante per la scheda Online Stores, ad esempio il testo del pulsante e la descrizione comando per il pulsante.
-   URL per le immagini Windows Media Player per identificare il negozio online.
-   URL delle pagine Web, forniti dal negozio online, che Windows Media Player host nell'interfaccia utente.

Quando si inizia a sviluppare il negozio online, è necessario fornire a Microsoft l'URL del documento ServiceInfo. Durante la fase di sviluppo, il negozio online verrà visualizzato Windows Media Player solo quando è impostata una chiave del Registro di sistema speciale.

Dopo la pubblicazione del negozio online, lo scenario ususale è che Windows Media Player il documento ServiceInfo dal Web automaticamente. In alcuni casi, tuttavia, Windows Media Player il documento ServiceInfo dal computer dell'utente. Per altre informazioni, vedere [Impostazione dello Store online iniziale.](setting-the-initial-online-store.md)

Quando Windows Media Player il documento ServiceInfo dal Web, aggiunge una stringa di query all'URL. La stringa di query contiene parametri che forniscono informazioni sulle impostazioni locali dell'utente e sulla Windows Media Player versione.

È possibile creare documenti ServiceInfo statici o dinamici. Un documento ServiceInfo statico ha un'.xml di file. Un documento ServiceInfo dinamico è una pagina ASP con estensione asp o aspx.

Non tutti gli elementi disponibili per l'uso nel documento ServiceInfo possono essere usati da ogni negozio online e alcuni elementi sono facoltativi per tutti i negozi online. Per informazioni sui tipi di negozi online che è possibile creare e sulle funzionalità disponibili per ogni [tipo,](windows-media-player-online-stores.md)vedere Windows Media Player Online Stores .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni sui negozi online di tipo 2**](about-type-2-online-stores.md)
</dt> <dt>

[**Creazione dinamica del documento ServiceInfo**](creating-the-serviceinfo-document-dynamically.md)
</dt> <dt>

[**Esempio di documento ServiceInfo per un negozio online di tipo 2**](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**Documento ServiceInfo**](serviceinfo-document.md)
</dt> </dl>

 

 




