---
description: Popolamento di raccolte COM+
ms.assetid: df86cbab-dcb8-46ac-aebf-8516276b6e81
title: Popolamento di raccolte COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 256c246a4f5d176e6b706515d02c0dd5cf68f7ae5a9aff7f89949da14510636b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119990671"
---
# <a name="populating-com-collections"></a>Popolamento di raccolte COM+

Dopo aver recuperato una raccolta e prima di poter lavorare direttamente con gli elementi in essa contenuti, è necessario popolare la raccolta usando il [**metodo Populate.**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) In questo modo vengono recuperati i dati per il contenuto della raccolta dal catalogo COM+.

È importante comprendere che ogni volta che si usano gli oggetti COMAdmin per modificare gli elementi o i dati nelle raccolte, si lavora realmente sui dati memorizzati nella cache temporanei. non si sta lavorando direttamente con il catalogo persistente. Nessuna operazione da eseguire con una raccolta o uno dei relativi elementi viene riflessa nel catalogo fino a quando non si chiama [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) nella raccolta. Per altre informazioni, vedere [Salvataggio o rimozione delle modifiche](saving-or-discarding-changes.md).

Qualsiasi chiamata successiva a [**Populate**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate), prima di chiamare [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), ha l'effetto di eliminare le modifiche in sospeso per tutti gli elementi nella raccolta. **Popolamento** popola sempre la cache in uso con tutti i dati persistenti nell'archivio dati del catalogo sottostante.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esplorazione della gerarchia di raccolte COM+](navigating-the-com--collection-hierarchy.md)
</dt> <dt>

[Esecuzione di query per le raccolte correlate disponibili](querying-for-available-related-collections.md)
</dt> <dt>

[Recupero di raccolte nel catalogo COM+](retrieving-collections-on-the-com--catalog.md)
</dt> </dl>

 

 



