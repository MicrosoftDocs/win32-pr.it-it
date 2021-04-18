---
description: Modifiche al formato dinamico
ms.assetid: ff60de5a-3edc-405d-aa02-8704b96d5e87
title: Modifiche al formato dinamico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49496e0b43d9b120f6daf27007cde98191a7765b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304009"
---
# <a name="dynamic-format-changes"></a>Modifiche al formato dinamico

Quando due filtri si connettono, accettano un tipo di supporto che descrive il formato dei dati che verranno recapitati dal filtro upstream. Nella maggior parte dei casi, il tipo di supporto è fisso per la durata della connessione. Tuttavia, DirectShow offre un supporto limitato per i filtri per modificare il tipo di supporto. Quando un filtro cambia i tipi di supporto, viene chiamato *modifica del formato dinamico*. Se si sta scrivendo un filtro DirectShow, è necessario essere a conoscenza dei meccanismi per le modifiche del formato dinamico. Anche se il filtro non supporta tali modifiche, dovrebbe rispondere correttamente se un altro filtro richiede un nuovo formato.

DirectShow definisce diversi meccanismi distinti per le modifiche del formato dinamico, a seconda dello stato del grafico del filtro e del tipo di modifica richiesto.

-   Se il grafo viene arrestato, i pin possono riconnettersi e rinegoziare il tipo di supporto. Per ulteriori informazioni, vedere [riconnessione dei pin](reconnecting-pins.md).
-   Alcuni filtri possono riconnettere i pin anche quando il grafico è attivo (in esecuzione o in pausa). Per ulteriori informazioni su questo meccanismo, vedere [riconnessione dinamica](dynamic-reconnection.md).

In caso contrario, se il grafico è attivo, ma i filtri in questione non supportano la riconnessione dinamica dei pin, esistono tre meccanismi possibili per modificare il formato:

-   [QueryAccept (downstream)](queryaccept--downstream.md) viene usato quando un pin di output propone una modifica di formato al relativo peer downstream, ma solo se il nuovo formato non richiede un buffer più grande.
-   [QueryAccept (upstream)](queryaccept--upstream.md) viene usato quando un pin di input propone una modifica al formato del peer upstream. Il nuovo formato può avere le stesse dimensioni oppure può essere più grande.
-   [ReceiveConnection](receiveconnection.md) viene usato quando un pin di output propone una modifica di formato al peer downstream e il nuovo formato richiede un buffer più grande.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Gestione delle modifiche al formato dal renderer video](handling-format-changes-from-the-video-renderer.md)
</dt> </dl>

 

 



