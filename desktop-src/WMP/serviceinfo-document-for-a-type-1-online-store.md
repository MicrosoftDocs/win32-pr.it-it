---
title: Documento ServiceInfo per un negozio online di tipo 1
description: Documento ServiceInfo per un negozio online di tipo 1
ms.assetid: 9ca424a1-c29a-4078-8d56-9d0fea52f150
keywords:
- Windows Media Player Online Stores, documento ServiceInfo
- archivi online, documento ServiceInfo
- digitare 1 negozi online, documento ServiceInfo
- Documento ServiceInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d47ce17cf2494a84193116fc340f843934b6f073
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044861"
---
# <a name="serviceinfo-document-for-a-type-1-online-store"></a>Documento ServiceInfo per un negozio online di tipo 1

Gli archivi online di tipo 1 devono fornire a Microsoft l'URL di un documento XML che descrive l'archivio online. Windows Media Player 11 utilizza questo documento per determinare come configurare l'interfaccia utente per ospitare lo Store online.

Il documento ServiceInfo per un archivio di tipo 1 fornisce le informazioni seguenti a Windows Media Player:

-   Informazioni utilizzate per configurare il pulsante **Store online** (chiamato anche scheda), ad esempio il testo del pulsante, il colore del pulsante e la descrizione comando per il pulsante.
-   URL per le immagini visualizzate da Windows Media Player per identificare il negozio online.
-   URL di pagine Web, fornite dallo Store online, che Windows Media Player ospita nell'interfaccia utente.
-   URL in cui Windows Media Player può recuperare il plug-in del negozio online, in modo che sia possibile installare il plug-in nel computer dell'utente.

Quando Windows Media Player Recupera il documento ServiceInfo dal Web, aggiunge una stringa di query all'URL. La stringa di query contiene parametri che forniscono informazioni sulle impostazioni locali e sulla posizione geografica dell'utente e sulla versione di Windows Media Player.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni sugli archivi online di tipo 1**](about-type-1-online-stores.md)
</dt> <dt>

[**Creazione dinamica del documento ServiceInfo**](creating-the-serviceinfo-document-dynamically.md)
</dt> <dt>

[**Documento ServiceInfo di esempio per un negozio online di tipo 1**](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[**Documento ServiceInfo**](serviceinfo-document.md)
</dt> </dl>

 

 




