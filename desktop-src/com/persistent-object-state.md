---
title: Stato oggetto permanente
description: Stato oggetto permanente
ms.assetid: 731fef03-d204-48e7-b33a-801e97a9d2c2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c08d4dd1175b5a7681f79fa9049772af245a031
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328980"
---
# <a name="persistent-object-state"></a>Stato oggetto permanente

Alcuni oggetti COM possono salvare lo stato interno quando viene richiesto da un client.

COM definisce gli standard mediante i quali i client possono richiedere l'inizializzazione, il caricamento e il salvataggio di oggetti da e verso un archivio dati (ad esempio file flat, archiviazione strutturata o memoria). È responsabilità del cliente gestire la posizione in cui vengono archiviati i dati persistenti dell'oggetto, ma non il formato dei dati. Gli oggetti COM che rispettano questi standard sono detti *oggetti permanenti*.

Per altre informazioni, vedere i seguenti argomenti:

-   [Interfacce oggetto permanenti](persistent-object-interfaces.md)
-   [Inizializzazione di oggetti permanenti](initializing-persistent-objects.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Client e server COM](com-clients-and-servers.md)
</dt> </dl>

 

 




