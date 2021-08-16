---
description: Recupero e impostazione delle proprietà
ms.assetid: 259612e7-70df-4f0f-90bc-766008dfdce7
title: Recupero e impostazione di proprietà (Servizi componenti)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 805d98463e1f9b8f08c1018b49554c95e2735bfa7ea6dca21d90243eb324df49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118306756"
---
# <a name="getting-and-setting-properties-component-services"></a>Recupero e impostazione di proprietà (Servizi componenti)

Prima di poter leggere o scrivere determinate proprietà esposte da un elemento in una raccolta, è necessario eseguire i passaggi seguenti:

1.  Recuperare la raccolta.
2.  Popolare la raccolta per leggere i dati dal catalogo COM+.
3.  Recuperare l'elemento specifico nella raccolta, che lo rappresenta con un oggetto dalla [**classe COMAdminCatalogObject.**](comadmincatalogobject.md)

Per un esempio che illustra questi passaggi, vedere Esplorazione della gerarchia [di raccolte COM+.](navigating-the-com--collection-hierarchy.md)

Poiché le particolari proprietà esposte possono variare a seconda di ciò che rappresenta l'elemento; ciò significa che un elemento che rappresenta un componente ha proprietà diverse rispetto a un elemento che rappresenta un'applicazione COM+. Impostare una di queste proprietà usando una singola proprietà generica, la proprietà Value, in [**COMAdminCatalogObject.**](comadmincatalogobject.md)

La proprietà Value consente di ottenere o impostare qualsiasi proprietà denominata specifica esposta da un elemento, di restituire un valore per una proprietà denominata durante il recupero e di ottenere un nome e un valore durante l'impostazione.

Nessuna modifica viene effettivamente registrata nel catalogo COM+ fino a quando non si salvano in modo esplicito le modifiche usando il metodo [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) [**nell'oggetto COMAdminCatalogCollection.**](comadmincatalogcollection.md) Le modifiche in sospeso per tutte le proprietà di tutti gli elementi in una determinata raccolta vengono salvate tutte contemporaneamente. Per informazioni dettagliate, vedere [Salvataggio o rimozione delle modifiche.](saving-or-discarding-changes.md)

Non tutte le modifiche apportate verranno accettate. Il catalogo COM+ applica una logica di coerenza per garantire la configurazione degli elementi in modo ragionevole. Inoltre, quando si modificano alcune proprietà, altre potrebbero cambiare automaticamente in base alla stessa logica di coerenza. Questi effetti vengono visualizzati quando si tenta di salvare le modifiche.

> [!Note]  
> È possibile che l'utente sia in disezione con un altro writer nel catalogo COM+. Tra le [**chiamate a Populate**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) e [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) per una determinata raccolta, non è presente un blocco su nessuno di questi dati nel catalogo. Più parti possono configurare contemporaneamente gli elementi in una determinata raccolta e possono essere in contesa quando salvano le modifiche. Ciò significa che un altro utente potrebbe modificare le impostazioni di un oggetto prima o dopo l'esecuzione, eseguendo un tipo di programma usando gli oggetti COMAdmin o lo strumento amministrativo Servizi componenti, in locale o in remoto. La regola generale per la scrittura di oggetti nel catalogo è che tutte le proprietà di un oggetto vengono scritte contemporaneamente. Ovvero, l'ultimo writer ha la precedenza, ovvero l'oggetto viene salvato nel catalogo esattamente come è stato configurato dall'ultimo writer.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Interdipendenze tra proprietà](interdependencies-between-properties.md)
</dt> <dt>

[Esecuzione di query per le proprietà disponibili](querying-for-available-properties.md)
</dt> <dt>

[Salvataggio o rimozione delle modifiche](saving-or-discarding-changes.md)
</dt> </dl>

 

 



