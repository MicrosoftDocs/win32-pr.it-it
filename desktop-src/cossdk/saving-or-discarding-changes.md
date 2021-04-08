---
description: Salvataggio o eliminazione di modifiche
ms.assetid: eba4e794-0929-450c-a172-6de6c2f2f2c4
title: Salvataggio o eliminazione di modifiche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4946574facd0d41d68f4de8cf2f2f48410eb6e99
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877493"
---
# <a name="saving-or-discarding-changes"></a>Salvataggio o eliminazione di modifiche

Quando si impostano le proprietà in un elemento, nessuna modifica viene effettivamente registrata nel catalogo COM+ fino a quando non si salvano in modo esplicito le modifiche. A tale scopo, usare il metodo [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) sull'oggetto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) per la raccolta che contiene l'elemento.

Se si desidera annullare le modifiche di cui non è ancora stato eseguito il commit, è possibile chiamare il metodo [**Populate**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) sull'oggetto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) . Questa operazione consente di leggere tutti i dati persistenti dal catalogo COM+ per tutti gli elementi della raccolta, eliminando in tal modo tutte le modifiche in sospeso.

Quando si utilizza [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), le incoerenze nelle impostazioni delle proprietà selezionate generano un errore e **SaveChanges** non riesce a scrivere l'oggetto che ha restituito l'errore. Tutte le proprietà di un determinato elemento vengono scritte o non vengono scritte nel suo complesso.

Tuttavia, quando si verificano errori di scrittura, è possibile che non siano dovute a impostazioni incompatibili; potrebbero essersi verificati altri errori. È necessario esaminare i dettagli dell'errore in modo da essere certi. Per ulteriori informazioni, vedere [gestione degli errori di amministrazione com+](handling-com--administration-errors.md) e [interdipendenze tra le proprietà](interdependencies-between-properties.md).

Come regola generale, maggiore è il numero di modifiche che si tenta di salvare in una sola volta, in particolare modifiche a più oggetti, più è probabile che si ottenga un errore e più difficile tenere traccia del problema.

Inoltre, tra le chiamate a [**popolare**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) e [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), non è presente un blocco sugli elementi nella raccolta; la contesa è possibile. Per informazioni dettagliate, vedere [recupero e impostazione delle proprietà](getting-and-setting-properties.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Recupero e impostazione delle proprietà](getting-and-setting-properties.md)
</dt> <dt>

[Interdipendenze tra proprietà](interdependencies-between-properties.md)
</dt> <dt>

[Esecuzione di query per le proprietà disponibili](querying-for-available-properties.md)
</dt> </dl>

 

 



