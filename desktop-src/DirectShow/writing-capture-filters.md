---
description: Scrittura di filtri di acquisizione
ms.assetid: 7dfd1009-da09-49dc-a200-3d7a9f1c70c1
title: Scrittura di filtri di acquisizione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0aa4807f381dc925a68fa3c60e45d5c8c5c444653230f366895b370e97aaccb8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120049091"
---
# <a name="writing-capture-filters"></a>Scrittura di filtri di acquisizione

La scrittura di un filtro di acquisizione audio o video DirectShow è sconsigliata. Al contrario, DirectShow supporto automatico per i dispositivi di acquisizione audio e video, usando filtri wrapper ed [Enumeratore dispositivo di sistema](system-device-enumerator.md). Per altre informazioni sull'implementazione di un driver di dispositivo, vedere la documentazione di Windows Driver Kit (WDK).

Questa sezione è destinata solo agli sviluppatori che devono acquisire alcuni tipi di dati personalizzati da un dispositivo hardware insolito.

In questo articolo sono contenute le sezioni seguenti:

-   [Requisiti dei pin per i filtri di acquisizione](pin-requirements-for-capture-filters.md)
-   [Implementazione di un pin di anteprima (facoltativo)](implementing-a-preview-pin--optional.md)
-   [Generazione di dati in un filtro di acquisizione](producing-data-in-a-capture-filter.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Scrittura DirectShow filtri](writing-directshow-filters.md)
</dt> </dl>

 

 



