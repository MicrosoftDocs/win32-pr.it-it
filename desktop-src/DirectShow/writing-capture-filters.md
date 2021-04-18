---
description: Scrittura dei filtri di acquisizione
ms.assetid: 7dfd1009-da09-49dc-a200-3d7a9f1c70c1
title: Scrittura dei filtri di acquisizione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8de1a64de2b56dbc0728432307036fc46387f539
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313389"
---
# <a name="writing-capture-filters"></a>Scrittura dei filtri di acquisizione

La scrittura di un filtro di acquisizione audio o video per DirectShow non è consigliata. DirectShow fornisce invece il supporto automatico per i dispositivi di acquisizione audio e video, usando i filtri wrapper e l' [enumeratore di dispositivi di sistema](system-device-enumerator.md). Per ulteriori informazioni sull'implementazione di un driver di dispositivo, consultare la documentazione di Windows Driver Kit (WDK).

Questa sezione è destinata solo agli sviluppatori che devono acquisire alcuni tipi di dati personalizzati da un dispositivo hardware insolito.

In questo articolo sono contenute le sezioni seguenti:

-   [Requisiti PIN per i filtri di acquisizione](pin-requirements-for-capture-filters.md)
-   [Implementazione di un pin di anteprima (facoltativo)](implementing-a-preview-pin--optional.md)
-   [Produzione di dati in un filtro di acquisizione](producing-data-in-a-capture-filter.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Scrittura di filtri DirectShow](writing-directshow-filters.md)
</dt> </dl>

 

 



