---
description: Ogni elemento di una raccolta espone le proprietà.
ms.assetid: d9af57ea-c5b3-4017-bdc2-e43b86b3ddcd
title: Modifica delle proprietà nel catalogo COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50ace2809fef4510a9c89b5faf31df555cb76426a06dd445aff9438c0d19e887
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118546230"
---
# <a name="editing-properties-in-the-com-catalog"></a>Modifica delle proprietà nel catalogo COM+

Ogni elemento di una raccolta espone le proprietà. Queste proprietà servono a contenere i dati di configurazione per qualsiasi elemento rappresentato dall'elemento. Nello strumento di amministrazione Servizi componenti queste proprietà vengono visualizzate in una pagina delle proprietà a cui si accede facendo clic con il pulsante destro del mouse su un elemento in una cartella.

Poiché gli elementi in una determinata raccolta rappresentano tutti lo stesso tipo di elemento, tali elementi espongono un set di proprietà coerente nell'insieme. Ad esempio, la [**raccolta Applications**](applications.md) espone una proprietà Name, una proprietà AppID e così via. Ciò è analogo al modo in cui per ogni applicazione nello strumento di amministrazione Servizi componenti è disponibile una pagina delle proprietà strutturata in modo coerente. Per un elenco delle proprietà disponibili per la **raccolta Applications,** vedere **Applicazioni.** Per un elenco delle proprietà disponibili per la [**raccolta Components,**](components.md) vedere **Components.**

Per un elenco completo delle proprietà esposte dagli elementi in ogni raccolta, vedere [Raccolte di amministrazione COM+.](com--administration-collections.md)

Per rappresentare un elemento in una raccolta, usare un oggetto creato dalla [**classe COMAdminCatalogObject.**](comadmincatalogobject.md) Questo oggetto consente di impostare e ottenere qualsiasi proprietà esposta dall'elemento. Quando si impostano le proprietà, è anche possibile che ci si contendono altri writer al catalogo COM+. Per altre informazioni, vedere [Recupero e impostazione delle proprietà.](getting-and-setting-properties.md)

Dopo aver impostato le proprietà, non viene eseguito il commit di alcuna modifica fino a quando non si salvano in modo esplicito le modifiche. Per altre informazioni, vedere [Salvataggio o rimozione delle modifiche.](saving-or-discarding-changes.md)

Quando si salvano le modifiche, il catalogo COM+ applica una logica di configurazione per assicurarsi di non impostare elementi su configurazioni incompatibili. Vengono inoltre modificate alcune proprietà quando si modificano in modo esplicito altre proprietà. Per altre informazioni, vedere [Interdipendenze tra proprietà.](interdependencies-between-properties.md)

COM+ dispone inoltre di una funzionalità che consente di eseguire query in modo dinamico per visualizzare le proprietà disponibili per gli elementi in una determinata raccolta. Per informazioni dettagliate, vedere [Esecuzione di query per le proprietà disponibili.](querying-for-available-properties.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Operazioni di amministrazione COM+ all'interno di transazioni](com--administration-operations-within-transactions.md)
</dt> <dt>

[Gestione degli errori di amministrazione COM+](handling-com--administration-errors.md)
</dt> <dt>

[Esempio introduttivo di utilizzo del catalogo di amministrazione COM+](introductory-example-using-the-com--administration-catalog.md)
</dt> <dt>

[Panoramica degli oggetti COMAdmin](overview-of-the-comadmin-objects.md)
</dt> <dt>

[Recupero di raccolte nel catalogo COM+](retrieving-collections-on-the-com--catalog.md)
</dt> </dl>

 

 



