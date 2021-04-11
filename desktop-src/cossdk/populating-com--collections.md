---
description: Popolamento di raccolte COM+
ms.assetid: df86cbab-dcb8-46ac-aebf-8516276b6e81
title: Popolamento di raccolte COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 521d85521eb7e3750d06920a570ddeaf4d7e9b20
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342251"
---
# <a name="populating-com-collections"></a>Popolamento di raccolte COM+

Dopo aver recuperato una raccolta e prima di poter usare direttamente gli elementi in esso contenuti, è necessario popolare la raccolta usando il metodo [**popolare**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) . Recupera i dati per il contenuto della raccolta dal catalogo COM+.

È importante tenere presente che ogni volta che si utilizzano gli oggetti COMAdmin per modificare gli elementi o i dati nelle raccolte, si sta effettivamente lavorando sui dati memorizzati temporaneamente nella cache. non si sta lavorando direttamente con il catalogo permanente. Non viene eseguita alcuna operazione con una raccolta o con i relativi elementi nel catalogo fino a quando non si chiama [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) sulla raccolta. Per informazioni dettagliate, vedere [salvataggio o eliminazione di modifiche](saving-or-discarding-changes.md).

Tutte le chiamate successive a [**popolare**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate), prima di chiamare [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), hanno l'effetto di ignorare le modifiche in sospeso in tutti gli elementi della raccolta. **Popola** popola sempre la cache con cui si sta lavorando con i dati salvati in modalità permanente nell'archivio dati del catalogo sottostante.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esplorazione della gerarchia della raccolta COM+](navigating-the-com--collection-hierarchy.md)
</dt> <dt>

[Esecuzione di query per le raccolte correlate disponibili](querying-for-available-related-collections.md)
</dt> <dt>

[Recupero di raccolte nel catalogo COM+](retrieving-collections-on-the-com--catalog.md)
</dt> </dl>

 

 



