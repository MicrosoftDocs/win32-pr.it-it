---
description: Ogni elemento in una raccolta espone le proprietà.
ms.assetid: d9af57ea-c5b3-4017-bdc2-e43b86b3ddcd
title: Modifica di proprietà nel catalogo COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94ed2bade8886fe08bb7ed1ece179b35677569f1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748274"
---
# <a name="editing-properties-in-the-com-catalog"></a>Modifica di proprietà nel catalogo COM+

Ogni elemento in una raccolta espone le proprietà. Queste proprietà consentono di conservare i dati di configurazione per qualsiasi elemento rappresentato dall'elemento. Nello strumento di amministrazione Servizi componenti, queste proprietà vengono visualizzate in una pagina delle proprietà a cui si accede facendo clic con il pulsante destro del mouse su un elemento in una cartella.

Poiché gli elementi di una raccolta specifica rappresentano tutti lo stesso tipo di elemento, tali elementi espongono un set di proprietà coerenti nell'intera raccolta. La raccolta [**Applications**](applications.md) , ad esempio, espone una proprietà Name, una proprietà AppID e così via. Questo è analogo al modo in cui per ogni applicazione nello strumento di amministrazione Servizi componenti è disponibile una pagina delle proprietà strutturata in modo coerente. Per un elenco delle proprietà disponibili per la raccolta di **applicazioni** , vedere **Applications (applicazioni**). Per un elenco delle proprietà disponibili per la raccolta [**Components**](components.md) , vedere **Components**.

Per un elenco completo delle proprietà esposte da elementi in ogni raccolta, vedere la pagina relativa alle [raccolte di amministrazione com+](com--administration-collections.md).

Rappresenta un elemento in una raccolta usando un oggetto creato dalla classe [**COMAdminCatalogObject**](comadmincatalogobject.md) . Questo oggetto consente di impostare e ottenere le proprietà esposte dall'elemento. Quando si impostano le proprietà, è anche possibile che si stia tendendo con un altro writer al catalogo COM+. Per ulteriori informazioni, vedere [recupero e impostazione delle proprietà](getting-and-setting-properties.md).

Dopo aver impostato le proprietà, non viene eseguito il commit delle modifiche fino a quando non si salvano in modo esplicito le modifiche. Per ulteriori informazioni, vedere [salvataggio o eliminazione di modifiche](saving-or-discarding-changes.md).

Quando si salvano le modifiche, il catalogo COM+ applica una logica di configurazione per assicurarsi di non impostare elementi su configurazioni incompatibili. Modifica anche alcune proprietà quando si modificano in modo esplicito determinate altre proprietà. Per ulteriori informazioni, vedere [interdipendenze tra proprietà](interdependencies-between-properties.md).

COM+ dispone inoltre di una funzionalità che consente di eseguire query in modo dinamico per vedere quali proprietà sono disponibili per gli elementi di una raccolta specifica. Per informazioni dettagliate, vedere [esecuzione di query per le proprietà disponibili](querying-for-available-properties.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Operazioni di amministrazione COM+ all'interno delle transazioni](com--administration-operations-within-transactions.md)
</dt> <dt>

[Gestione degli errori di amministrazione COM+](handling-com--administration-errors.md)
</dt> <dt>

[Esempio introduttivo di utilizzo del catalogo di amministrazione COM+](introductory-example-using-the-com--administration-catalog.md)
</dt> <dt>

[Panoramica degli oggetti COMAdmin](overview-of-the-comadmin-objects.md)
</dt> <dt>

[Recupero di raccolte nel catalogo COM+](retrieving-collections-on-the-com--catalog.md)
</dt> </dl>

 

 



