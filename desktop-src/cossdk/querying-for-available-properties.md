---
description: Esecuzione di query per le proprietà disponibili
ms.assetid: 9acf10cd-19a8-4542-8078-3e4ee275d4d5
title: Esecuzione di query per le proprietà disponibili
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22238e04404d2b88efa81ce98d0b0fb0e09d245f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127402"
---
# <a name="querying-for-available-properties"></a>Esecuzione di query per le proprietà disponibili

Se si sta scrivendo uno strumento di amministrazione di uso generico, è molto probabile che sia necessario scrivere routine per l'impostazione delle proprietà in generale. Per supportare questa operazione, esiste una funzionalità che consente di eseguire query in modo dinamico per le proprietà disponibili per gli elementi in una raccolta specifica.

La raccolta [**PropertyInfo**](propertyinfo.md) è disponibile da qualsiasi raccolta che potrebbe essere in attesa. La raccolta **PropertyInfo** contiene un elemento per ogni proprietà disponibile. È possibile enumerare questi elementi per determinare se una determinata proprietà è disponibile.

È possibile ottenere la raccolta [**PropertyInfo**](propertyinfo.md) da qualsiasi raccolta che si sta tenendo usando il metodo [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) nell'oggetto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) , lasciando vuoto il secondo parametro, dove normalmente si specifica la proprietà chiave di un elemento padre.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Recupero e impostazione delle proprietà](getting-and-setting-properties.md)
</dt> <dt>

[Interdipendenze tra proprietà](interdependencies-between-properties.md)
</dt> <dt>

[Salvataggio o eliminazione di modifiche](saving-or-discarding-changes.md)
</dt> </dl>

 

 



