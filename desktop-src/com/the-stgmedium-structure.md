---
title: Struttura STGMEDIUM
description: Struttura STGMEDIUM
ms.assetid: ff1e1128-d228-45a6-a19d-2875b6c4e003
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9da0adc98b5d774754bd2cbbccb415092d6498684a60189d6346afac82bd270a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992271"
---
# <a name="the-stgmedium-structure"></a>Struttura STGMEDIUM

Proprio come la struttura [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) è un miglioramento dell'identificatore di formato degli Appunti Windows, quindi la struttura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) è un miglioramento dell'handle di memoria globale usato per trasferire i dati. La struttura **STGMEDIUM** include un membro, **tymed**, che indica il supporto da usare, e un'unione che include puntatori e un handle per ottenere qualsiasi supporto specificato in **tymed**.

La [**struttura STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) consente sia alle origini dati che ai consumer di scegliere il supporto di scambio più efficiente in base al rendering. Se i dati sono così grandi che devono essere conservati su disco, l'origine dati può indicare un supporto basato su disco nel formato preferito, usando solo la memoria globale come backup se questo è l'unico supporto che il consumer comprende. La possibilità di usare il supporto migliore per gli scambi, in quanto l'impostazione predefinita migliora le prestazioni complessive dello scambio di dati tra le applicazioni. Ad esempio, se alcuni dei dati da trasferire sono già su disco, l'applicazione di origine può spostarla o copiarla in una nuova destinazione, nella stessa applicazione o in un'altra, senza dover prima caricare i dati nella memoria globale. All'estremità ricevente, il consumer dei dati non deve scriverlo su disco.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Formati di dati e supporti di trasferimento](data-formats-and-transfer-media.md)
</dt> </dl>

 

 




