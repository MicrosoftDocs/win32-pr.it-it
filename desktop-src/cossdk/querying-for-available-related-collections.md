---
description: Esecuzione di query per le raccolte correlate disponibili
ms.assetid: 9c7d2a01-5dc3-4d35-b938-f1d0525a8286
title: Esecuzione di query per le raccolte correlate disponibili
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0203df5bb7b5bf89396d5687dc28b19e9b183d56
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342321"
---
# <a name="querying-for-available-related-collections"></a>Esecuzione di query per le raccolte correlate disponibili

Se si scrive uno strumento di amministrazione di uso generico, è probabile che sia necessario scrivere routine per spostarsi nell'intera gerarchia di raccolta. Per supportare questa operazione, COM+ dispone di una funzionalità che consente di eseguire query in modo dinamico per le raccolte correlate disponibili in una raccolta specifica.

La raccolta [**RelatedCollectionInfo**](relatedcollectioninfo.md) è disponibile da qualsiasi raccolta che è possibile mantenere e contiene un elemento per ogni raccolta correlata disponibile. È possibile enumerare questi elementi per determinare se una determinata raccolta è disponibile.

È possibile ottenere la raccolta [**RelatedCollectionInfo**](relatedcollectioninfo.md) da qualsiasi raccolta che si sta tenendo usando il metodo [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) nell'oggetto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) , lasciando vuoto il secondo parametro, dove normalmente si specifica la proprietà chiave di un elemento padre.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esplorazione della gerarchia della raccolta COM+](navigating-the-com--collection-hierarchy.md)
</dt> <dt>

[Popolamento di raccolte COM+](populating-com--collections.md)
</dt> <dt>

[Recupero di raccolte nel catalogo COM+](retrieving-collections-on-the-com--catalog.md)
</dt> </dl>

 

 



