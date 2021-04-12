---
description: Recupero e impostazione delle proprietà
ms.assetid: 259612e7-70df-4f0f-90bc-766008dfdce7
title: Recupero e impostazione delle proprietà (Servizi componenti)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d151b08293cd32a35cd27bdba4dd3a37cdebfa4f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483445"
---
# <a name="getting-and-setting-properties-component-services"></a>Recupero e impostazione delle proprietà (Servizi componenti)

Prima di poter leggere o scrivere particolari proprietà esposte da un elemento in una raccolta, è necessario eseguire i passaggi seguenti:

1.  Recuperare la raccolta.
2.  Compilare la raccolta per leggere i dati dal catalogo COM+.
3.  Recuperare l'elemento specifico della raccolta, che lo rappresenta con un oggetto della classe [**COMAdminCatalogObject**](comadmincatalogobject.md) .

Per un esempio in cui vengono illustrati questi passaggi, vedere [esplorazione della gerarchia della raccolta com+](navigating-the-com--collection-hierarchy.md).

Poiché le particolari proprietà esposte possono variare a seconda dell'elemento rappresentato dall'elemento; ovvero un elemento che rappresenta un componente ha proprietà diverse rispetto a una che rappresenta un'applicazione COM+. Impostare una di queste proprietà utilizzando una singola proprietà generica, ovvero la proprietà Value, su [**COMAdminCatalogObject**](comadmincatalogobject.md).

La proprietà Value consente di ottenere o impostare eventuali proprietà denominate specifiche esposte da un elemento, restituendo un valore per una proprietà denominata durante il recupero e accettando un nome e un valore quando si imposta.

Non vengono effettivamente registrate modifiche nel catalogo COM+ fino a quando non si salvano in modo esplicito le modifiche utilizzando il metodo [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) sull'oggetto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) . Le modifiche in sospeso per tutte le proprietà di tutti gli elementi di una raccolta specifica vengono salvate in una sola volta. Per informazioni dettagliate, vedere [salvataggio o eliminazione di modifiche](saving-or-discarding-changes.md).

Non tutte le modifiche apportate verranno accettate. Il catalogo COM+ applica una logica coerenza per assicurarsi di configurare gli elementi in modo ragionevole. Inoltre, quando si modificano alcune proprietà, altre potrebbero cambiare automaticamente dalla stessa logica di coerenza. Questi effetti vengono visualizzati quando si tenta di salvare le modifiche.

> [!Note]  
> È possibile che si sia in conflitto con un altro writer nel catalogo COM+. Tra le chiamate a [**popolare**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) e [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) per una determinata raccolta, non si dispone di un blocco su nessuno dei dati nel catalogo. Più parti possono contemporaneamente configurare gli elementi in una raccolta specificata e potrebbero essere in conflitto quando salvano le modifiche. Ciò significa che un altro utente potrebbe modificare le impostazioni di un oggetto prima o dopo l'esecuzione, eseguendo un tipo di programma usando gli oggetti COMAdmin o utilizzando lo strumento di amministrazione Servizi componenti, in locale o in remoto. La regola generale per la scrittura di oggetti nel catalogo è che tutte le proprietà di un oggetto vengono scritte in una sola volta. Ovvero l'ultimo writer WINS, l'oggetto viene salvato nel catalogo esattamente come l'ultimo autore lo ha configurato.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Interdipendenze tra proprietà](interdependencies-between-properties.md)
</dt> <dt>

[Esecuzione di query per le proprietà disponibili](querying-for-available-properties.md)
</dt> <dt>

[Salvataggio o eliminazione di modifiche](saving-or-discarding-changes.md)
</dt> </dl>

 

 



